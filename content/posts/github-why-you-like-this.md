---
title: "Github Why You Like This"
date: 2022-05-30T11:35:21-04:00
draft: true
author: "gigameow"
authorLink: "https://peculiar.monster"
description: ""

categories: ["coding"]
tags: ["tech", "github"]

images: []
featuredImage: ""
featuredImagePreview: ""

hiddenFromHomePage: false
hiddenFromSearch: false
twemoji: true
fontawesome: true
linkToMarkdown: false
rssFullText: true

toc:
  enable: false
  auto: true
code:
  copy: true
  maxShownLines: 50
---
And of course, no sooner than I finished my previous post and decided to deploy the site than I ran into a bunch of problems.
<!--more-->

First, I had to set the DNS record to point at GitHub Pages. And that takes time to propogate and I am impatient.

THe DNS wasn't propogating and GH was tellng me that I'd configured something wrong, so it recommended that I set `A` records to point at the GitHub Pages IP addresses...except it didn't actually link to where I could _find_ those IP addresses. I finally found them buried in GH's documentation, but I'll be damned if I can find the page again.

I also set up the `CNAME` record at the same time.

Then I had to set up the GitHub workflow to actually deploy from my repo to the page--and unbeknownst to me, there was a _critical_ piece of missing information from the workflow as written.

And that piece of information was setting `cname: peculiar.monster` in the deploy script. Seriously. `CNAME` kept on disappearing from the `gh-pages` branch and I couldn't figure out why until I looked at [this GH Action](https://github.com/marketplace/actions/github-pages-action#%EF%B8%8F-add-cname-file-cname) which mentioned setting `CNAME`, while [the Hugo-specific action](https://github.com/marketplace/actions/hugo-setup)--the one I chose to use--did not mention it anywhere. No wonder it was being removed!

So, with that sorted, I turned my attention to why either the theme or Hugo wasn't respecting my `<!--more-->` tag. Turned out that Hugo was respecting it and the theme absolutely was not.

After digging through the CSS, I figured out where the problem was, 
