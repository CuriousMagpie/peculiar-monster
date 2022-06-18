---
title: "Code, Why Are You Like This?"
slug: "code-why-are-you-like-this"
date: 2022-05-30T11:35:21-04:00
draft: false
author: "GigaMeow"
authorLink: "https://peculiar.monster"
description: ""

categories: ["coding"]
tags: ["tech", "github", "css"]

images: []
featuredImage: ""
featuredImagePreview: ""

hiddenFromHomePage: false
hiddenFromSearch: false
twemoji: true
fontawesome: true
linkToMarkdown: true
rssFullText: true

toc:
  enable: false
  auto: true
code:
  copy: true
  maxShownLines: 50
---
And of course, no sooner than I finished my previous post and decided to deploy the site than I ran into a bunch of problems, some bigger than others.

First, I had to set the DNS record to point at GitHub Pages. And that takes time to propogate and I am _impatient_.

The DNS wasn't propogating and GH was tellng me that I'd configured something wrong, so it recommended that I set `A` records to point at the GitHub Pages IP addresses...except it didn't actually link to where I could _find_ those IP addresses.

I finally found them buried in GH's documentation, but I'll be damned if I can find the page again, even with searching through my browser history.

I also set up the `CNAME` record at the same time.

Then I had to set up the GitHub workflow to actually deploy from my repo to the page--and unbeknownst to me, there was a _critical_ piece of missing information from the workflow as written.

And that piece of information was setting `cname: peculiar.monster` in the deploy script.

Seriously. `CNAME` kept on disappearing from the `gh-pages` branch and I couldn't figure out why until I looked at [this GH Action](https://github.com/marketplace/actions/github-pages-action#%EF%B8%8F-add-cname-file-cname) which mentioned setting `CNAME`, while [the Hugo-specific action](https://github.com/marketplace/actions/hugo-setup)--the one I chose to use--did not mention it anywhere. No wonder it was being removed!

So, with that sorted, I turned my attention to why either the theme or Hugo wasn't respecting my `<!--more-->` tag. Turned out that _Hugo_ was respecting it just fine and the theme absolutely was not--and of course, this isn't actually documented _in_ the theme.

After digging through the CSS, I figured out where the problem was, it was in a bit of code from `themes/LoveIt/assets/css/_page/_home.scss`:

```scss
.home[data-home=posts] {
  .summary {
    .content {
      @include box(vertical);
      -webkit-line-clamp: 3;
      margin-top: .3rem;
      width: 100%;
      overflow: hidden;
      text-overflow: ellipsis;
      @include overflow-wrap(break-word);
      color: $global-font-secondary-color;
    }
  }
}
```

I did delete the classes that weren't relevant to the problem at hand--the `home[data-home=posts]` class has a _lot_ going on, more than is relevant to explain the current problem.

A bit of research, however, quickly helped me to figure out that `-webkit-line-clamp: 3;` was the culprit. It was restricting the summary display to three lines, it was a class I am not familiar with, and I wasn't sure what the options were.

Now, how to fix it?

I am not a methodical sort of person, alas--and looking at the code condensed like I did above actually helped me to get to a solution--but my normal way of doing things is to just throw lines of code at the problem and see if anything sticks. This is a terrible habit that I'm trying to break--it was fine when coding was something I did occasionally and for fun, but it's not great when I'm trying to write code at work.

And here's the answer, to the LoveIt theme disrespecting summary length and the `<!--more-->` tag, placed within `assets/css/_custom.scss`. :sweat_smile:

```scss
.home[data-home=posts] {
  .summary {
    .content {
      -webkit-line-clamp: none;
    }
  }
}
```

Then there was the problem with the paragraphs not being properly separated and the spacing just being weird. That was easy to solve, just a few more lines:

```scss
.home[data-home=posts] {
  .summary {
    .content p {
      display: block;
    }
  }
}
```

And there, everything is so much more to my liking. :tada:
