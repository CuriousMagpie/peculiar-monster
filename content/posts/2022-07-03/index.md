---
title: "Thoughts on Digital Gardening and Information Organization"
slug: "thoughts-on-digital-gardening-and-information-organization"
date: 2022-07-03T16:40:10-04:00
draft: false
author: "GigaMeow"
authorLink: "https://peculiar.monster"
description: ""

categories: [meta]
tags: [tech, digital gardening, slow web, blogging, history]

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
  auto: false
code:
  copy: true
  maxShownLines: 50
---
I've been spending a lot of time over the last week falling into various rabbit holes. So many.

But one thing I keep coming back to is how, on my previous blog, I felt paralyzed by the weight of perfection. As if I were under so much scrutiny that the smallest mistake would cause a shitstorm.

This feeling was only exacerbated by the fact that when I did say something stupid on Twitter, a group of leftier than thou folks who enjoy brigading other people for the tiniest of ideological differences decided to brigade me. And suddenly: I found that I was unable to speak in that space any longer--that the [years of abuse](https://peculiar.momnster/f-is-for-fungible/) had simply destroyed my ability to write or engage at all in that space.

That's the lens I have been looking through as I read through all these different essays and short pieces about being a person on the internet.

The first big concept I find myself intrigued by is that of digital gardening. [Maggie Appleton](https://maggieappleton.com) has written a fair bit about this; I found her [brief history of digital gardening](https://maggieappleton.com/garden-history) extremely informative and honestly, quite fascinating:

>A garden is a collection of evolving ideas that aren't strictly organised by their publication date. They're inherently exploratory – notes are linked through contextual associations. They aren't refined or complete - notes are published as half-finished thoughts that will grow and evolve over time. They're less rigid, less performative, and less perfect than the personal websites we're used to seeing.

I ended up reading a lot of the different essays on her site and found a lot of food for thought and I'm not sure how I'm going to integrate some of these concepts into this site, but I like the idea of getting away from the chronological blog post sort of situation.

So the second concept is around Amy Hoy's essay on [how the blog broke the web](https://stackingthebricks.com/how-blogs-broke-the-web/), rings very true to me despite there being a great honking factual error in it:

>[Movable Type] ...was also the first web-based CMS that you could download for free, install, and run on your own web host.

In fact, it was not the first. There was [Greymatter](https://en.wikipedia.org/wiki/Greymatter_(software)) (which I used) and possibly some other systems--Blogger was around at that time, but my hazy memory is that it was a royal pain in the ass to use, as the FTP portion of the software was fairly flaky.

At any rate, I think Amy Hoy is onto something in this essay: the fact that Movable Type was incredibly powerful *and* under constant development made it irresistible for folks who wanted to create personal websites but didn't want to deal with hand-coding everything. I remember that the templates were fairly easy to customize and you could import and export entries as part of the built in functionality. There wasn't a large or robust plug-in community like there is with what ultimately came to dominate the blogging software world: WordPress.

Movable Type is still around, but I know of only two blogs which still use it: [Making Light](https://nielsenhayden.com/makinglight/index.html), on a very old and lovingly maintained version on which it appears that the CSS is currently not working, and [Kottke](https://www.kottke.org/), who uses it but doesn't specify if he's using the commercial version or the open source version (the latter of which you have to do a *lot* of hunting for [in order to find](https://movabletype.org/downloads/stable/)).

Around the time of the great brouhaha around MT licensing happened, I was maintaining both my MT site and a LiveJournal. I eventually abandoned the MT site and wrote exclusively on LiveJournal until it was sold to the Russians, at which point I made all my posts private and stopped writing there.

But I digress. Hoy's central thesis is that tools like Movable Type were the thin part of the wedge that forced large chunks of the web into a reverse-chronological hellscape, a wedge the prioritized form over function: instead of allowing users to set up their sites however they wanted, the way you could when you were coding HTML by hand, you could make of of two choices. Here's Hoy on that:

>Homepage production became suddenly a question of economics:
>
>1.  Go with the system’s default format: zero work.
>2.  Customizing the system to your format: way more work than pure HTML ever was
>
> And who, once offered a path of least resistance, has the energy to fight it all the way?
>
>The format won.
>
> It was easier — faster! — to literally go with the flow… of *time*.

I really can't disagree with this: I remember spending hours tweaking my templates so they were just right.

But at least you *could*. Have you ever tried to modify a WordPress template? Not customize the stylesheet, but the actual template itself? Good luck. They're a maze of PHP with includes and god knows what else. And extraordinarily vulnerable to various exploits, including one that injected malicious JavaScript on my site and forced me to change templates about this time last year. An entire industry sprung up around frameworks--I mean "parent themes"--to optimize SEO and providing different hooks you could use to customize the functionality without touching much code.

But really, it was just *easier* to go with the templates that came with WordPress, to go with that flow, so every new blog looked the same. Hell, if you look at one of the most influential blogs in the SFF world, it's using a barely modified stock WordPress theme, to the point where it's just pathetic and laughable. The owner of the site has won a number of Hugos for it, you would think that he'd be able to get someone to make him a pretty site.

Another thing that came with WordPress was the plug-in community. There are a lot of plugins to enable what should be basic functionality: contact pages, dynamic tables, spam protection and other site security measures, and so on and so forth. And the problem with these plug-ins is that they have become a source of revenue for the folks who make them, so there's usually a freemium version as well as a paid one. I don't like the security and privacy implications of this model.

But the big advantage WordPress has, especially the hosted WordPress.com service has is that it just works. You can create a blog and be up and running in a matter of minutes. There's very little configuration to do and no template system to learn (unless you want to).

Whereas the amount of time it took me to get [Hugo](https://gohugo.io/) up and running--well, Hugo installed easily enough on my machines, but you also have to have a working knowledge of git, GitHub, and an understanding of the different options to deploy the working site. It took me quite a while to get the deploy script working because the instructions omitted setting `CNAME` on the `gh-pages` branch of my repo--but I was able to see that that was an issue.

There are *significant* technical barriers involved with using a static site generator for a blog: you have to be comfortable getting into the nuts and bolts of the templates and learn how to write a variant of [Go](https://go.dev/), which is a language I had no familiarity with prior to starting this project. I am *still* struggling to get pagination working.

But I find this sort of work satisfying and I'm able to surmount the gaps in my technical knowledge through sheer stubbornness, a willingness to make mistake, and making liberal use of a search engine. Not everyone does. Most folks want an out of the box tool that just works.

And the third concept and probably the most important one is from [this essay](https://matthiasott.com/notes/just-put-stuff-out-there) by Matthias Ott: Just put stuff out there:

>Maybe, we are overthinking it. Maybe, the one thing we should care most about is just putting stuff out there. At least, this is the primary reason we have a personal website, right? We have it to document and share random thoughts, things we learned, and nuggets we found. If we don’t put stuff out there, why have a website in the first place?

---

Another idea I've been poking at are personal knowledge bases and different ways of keeping all the threads of my life in some sort of knowledge management system.

I'm intrigued by the concepts behind Tiago Forte's [Building a Second Brain](https://www.buildingasecondbrain.com/) but considering that the website has no mention of how much the course costs and that there's a waitlist for the next cohort, I find that I have very little interest in taking the course. Instead, [I've looked over Maggie Appleton's notes from several years ago](https://maggieappleton.com/basb) (and I note that in her disclaimer she mentions the "blossoming" price which is a hilarious way of describing the inevitable upwards creep of course costs as the instructor/guru becomes more influential) and have come to the conclusion that I'll pick up the book when it comes out in paperback, probably next year.

But with this incredibly important caveat: ["People who write extensively about note-taking rarely have a serious context of use"](https://notes.andymatuschak.org/zUMFE66dxeweppDvgbNAb5hukXzXQu8ErVNv); that is: most productivity "experts" primary output is more advice on how to be productive and they are often disconnected from the contexts in which people take and use notes.

Until then, the Appleton's sketchnote version is good enough for me to get a reasonable overview. I have a significant file organization problem--I can usually find things, but I have literally over 30 years of different files stored (in the cloud) and I'd like to organize them a bit better and do better with my current working files.

So there's Forte's [PARA system](https://fortelabs.co/blog/para/), where the letters stand for:

- **P**rojects - a specific endpoint or deadline
- **A**reas of Responsibility - continuous areas of commitment
- **R**esources - topic or theme of ongoing interest
- **A**rchive - inactive items from the other categories.

Which, okay, but. It just doesn't seem to provide enough differentiation for me. I like the idea of keeping Resources and clearly identifying my Archive files, however, how to organize within each folder? That's sort of where I stumble. The PARA system calls for there to be no more than 4 levels of organization below each of the 4 major groupings. I don't know.

So a file structure organized with the PARA system would be:

```text
Projects
  Peculiar Monster Redesign 2022
    domain-registration-receipt.pdf
    Research and Inspiration
      Technology 1.md
      Technology 2.md
      Inspiration 1.png
      Research.md
    Design Files
      Images
        Logo Image.png
        Divider Image.png
      Mockups
        Template Mockup.png
    Code
      Tech Stack
        Tech Stack.md
      Styling
        Style.css
        Style2.css
        colors.sass
      Templates
        index.html
        archive.html
        partial-header.html
        partial-footer.html
      JavaScript
        cool script.js
        cooler script.js
  Knitting
    pattern1.pdf
    pattern2.pdf
  Crochet
    pattern1.pdf
  Writing
    poem1.md
    poem2.md
    Essay 1
      essay1.md
      notes.md
      links.md
    Essay 2
      notes.md
    
Areas
  Medical
    doctors.md
    hospitals.md
    medications.md
    Lab Results
      labcorp 2022-07-01
    Disability Paperwork
  Job #1
    Benefits
    Performance Evaluations
    Paystubs
      2022-04.pdf
      2022-05.pdf 
    
Research
  Area of Interest #1
  Area of Interest #2
  Area of Interest #3
  
Archive
  Peculiar Monster Redesign 2021
  Knitting
    completed pattern1.pdf
    completed pattern2.pdf
    completed pattern3.pdf
  Academic Work
    English Papers
    History Papers
  Writing
    Published Essays
    Trunked
```

Then there's [Johnny Decimal](https://johnnydecimal.com/), which I find really, really interesting. It's a lot more granular than the PARA but also has limits. With Johnny Decimal, you use a numbering system to set up ten different areas, and each area can have ten categories beneath it. So you can have a file that look something like this: `37.15 Grocery List 2022-07-03` where `3` is `Household` and `7` is `Shopping Lists` and `15` is the fifteenth item you've put in that category, so if you want to look at all your household shopping lists, you know to look in your main folder structure for a folder prepended with `30.07`.

Of course, the problem here is that this doesn't lend itself to keeping track of project-type work, something like `redesign website`. One could have a folder called `07 - websites` and then a subcategory for each website you have, so `07.01 - peculiar monster` for this site, and then you could just add a keyword at the beginning of each redesign-based file: `71.25 - redesign notes 2022-006-15.md` and `71.32 - redesign style ideas 2022-07-10.md` but then everything's all jumbled together and it would be useful if there were just a way to segregate out projects--and there is, with a [project-based addition](https://johnnydecimal.com/concepts/multiple-projects/) to the numbering schema: `000` through `999`, so a Johnny Decimal system with projects might look like this:

```text
100 Life Administration
  10-19 Administration
    10 Household Maintenance
  20-29 Finances
    21 Taxes
  22 Mortgage
  30-39 Medical
    30 Doctors, Hospitals, and Medications
      100.30.01 doctors.md
      100.30.02 hospitals.md
      100.30.02 medications.md
    31 Lab Results
      100.30.01 labcorp 2022-07-01
    32 Disability Paperwork
  40-49 Job #1
    41 Benefits
    42 Performance Evaluations
    43 Paystubs
      100.43.01 2022-04.pdf
      100.43.02 2022-05.pdf
      
101 Peculiar Monster Redesign 2022
  10-19 Administration
    10 Domain Registration
      101.10.01 registration receipt.pdf
  20-29 Research and Inspiration
    21 Technology 1
    22 Technology 2
    23 Inspiration 1
    24 Research
  30-39 Design Files
    31 Images
      101.31.01 Logo Image.png
      101.31.01 Divider Image.png
    32 Mockups
      101.32.01 Template Mockup.png
  40-49 Code
    41 Tech Stack
      101.41.01 Tech Stack.md
    42 Styling
      101.42.01 Style.css
      101.42.02 Style2.css
      101.42.03 colors.sass
    43 Templates
      101.43.01 index.html
      101.43.02 archive.html
      101.43.03 partial-header.html
      101.43.03 partial-footer.html
    44 JavaScript
      101.44.01 cool script.js
      101.44.01 cooler script.js

102 Textile Art
  10-19 Knitting Patterns
    10 Completed
    11 In Progress
    12 To Do
    13 Inspiration
  20-29 Crochet Patterns
    21 Completed
    22 In Progress
    23 To Do
    24 Inspiration
      
```

Or, with the PARA system you could have a project folder called `Peculiar Monster Redesign 2022-07` and then folders for each group of tasks: `Design`, `inspiration`, `Credits`, `Notes`, `Code`, et cetera.

Or, you could attempt to mash things up together, where your archived files are in the Johnny Decimal format subsumed under a PARA structure. (This is the way I'm leaning, but I'm not completely sure).

Then again, if you want to go completely overboard, you could build a [Zettelkasten](https://zettelkasten.de/introduction/). If you want to talk about overkill. That's more of a note-taking method than a full out organizational system, though.

The thing is, you read enough productivity books and you can trace each "system's" antecedents. The PARA system is highly influenced by David Allen's GTD methodology (which assumes you have people you can delegate tasks to, which I have always found to be a key weakness of the methodology; not everyone is an executive, David).

And all systems have baked-in biases. Like GTD implies the ability to delegate. PARA implies the ability to pay for either a book or what looks to be a very expensive course (and obviously, one which many people get value from, and Appleton's sketchnotes are really useful). Johnny Decimal assumes that you're going to be able to remember all those numbers.

So I'm still unsure how I want to organize my 30+ years of files, just that I need to pick something and *just do it* when I'm not in the mood to knit or crochet while watching television or if I need to take a 10 minute break from looking at my non-functional in a very specific way bit of code at work.

---

At any rate, what I'm aiming for ultimately is a space where I hit publish more often than not. A space where I'm comfortable posting incomplete thoughts. A space that *I* find useful in the future. A space which reflects who I am, with all my interests and ideas splattered all over the (virtual) pages. 

I'm really into the concept of the [slow web](https://indieweb.org/slow_web), which is the bedrock on which all the above noodling rests. I've been joking to myself that this is a hand-crafted, artisanal website, but--that actually *is* the goal.
