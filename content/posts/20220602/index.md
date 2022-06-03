---
title: "A Ridiculous Day"
slug: "ridiculous-day"
date: 2022-06-02T22:02:49-04:00
draft: false
author: "gigameow"
authorLink: "https://peculiar.monster"
description: ""

categories: ["coding", "personal"]
tags: ["github", "tech", "hugo", "health"]

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
Today's been a day of a lot of ridiculous all over the board.
<!--more-->

First off, the day started with therapy. Which wasn't ridiculous, but it was 8:15 in the morning so there's a certain degree of waaaah going on (every week, my appointment is at 8:15 am every week) just in general. Talked about EMDR a little bit to help me deal with my DESNOS/cPTSD (the _name_ of the thing is shifting: DESNOS is the name in the current edition of the DSM, cPTSD is what it's generally known by these days). I'm really good at masking, so it's often hard to tell when I'm losing my shit or really anxious orm, to be honest, even when I'm really depressed.

After therapy, I had to scoot along to my appointment with the PA at the Infectious Disease practice that's been following me since 2018. They're all great and the doctor who initially treated me, I'm convinced is the one who helped turn the tide for me--not just by treating the massive infection I had as a result of the necrosis happening in my abdomen, but by advocating for me with other hospital staff. Sadly, they're going to be following me for likely the rest of my life: I had sepsis 3 times in the fourth quarter of 2020[^1], so I'm on prophylactic oral antibiotics and need regular check-ins with them to make sure everything's still fine. I did graduate from every 3 months to every 6 months for appointments, though!

But see, I was sneaky and I took a little time before therapy and before my Infectious Disease appointment to mess around here; I decided last night that the theme I'd initially chosen was too complex both for my needs and for my level of ability, so I decided on Cactus as something a bit more streamlined if less flashy (I do like the color-changing cactus icon but I am going to replace it with something else). So I attempted to clone it in as a git submodule and I *really* shouldn't have done that--I have terrible luck with the git submodule at work, I don't know why I thought this was any different. Like I fucked things up so badly the site wouldn't deploy and I had to go to [Oh Shit, Git!?!](https://ohshitgit.com/) to find what I needed to fix things.

But fix them I did and after I got home it was to work! In the spare room![^2]

The first thing I do every day is review the to do list I (hopefully) made the day before--I only work 5-6 hours a day, so I have to make sure those hours count. By the time I got settled in and done with the list review, it was time for a meeting. The meeting ran short, so I started on my top task: pulling user IDs out of the beta database so we could award beta testers a special achievement in production. The PR for the achievement is still in queue to be deployed, but I wanted to have all the user IDs and usernames and email addresses in place.

...and it took me all fucking afternoon. Because our database is MongoDB, which is noSQL which means there are no relations between the different collections (they're not even tables, they're just JSON files, sob) and because the beta test involved testing group functionality and both parties and guilds fall under groups...and while you can only be in one party, you can be in as many guilds as you want. I only had the email address of one person per guild and needed to be able to award the achievement to everyone in the group that participated. And I'm not great at queryng MongoDB because the operands and syntax are just so foreign to me after so many years of working with a terribly design SQL database. So it took me all fucking afternoon.

With an intermission where I checked on the status of my insulin prescription, which was supposed to be released from hold earlier this week and was not. I've been trying to get it filled for the better part of a week--I was able to get all my other prescriptions transferred to my new insurance and filled with no problem, bu the insulin has been terrible.

First, there was no response from my doctor's office when CVS/caremark (OF COURSE IT'S THEM) contacted them for _either_ a new prescription _or_ a prior authorization--nevermind that those are _two completely different things_, why there's the same message for both statuses on the customer end is beyond my understanding but most things on the CVS/caremark website are beyond my understanding. Like why is it so slow? Why do the apps suck so much?

Anyhow, I digress.

I had to contact my doctor's office three times before someone got back to me--I sent a message, which was never forwarded, I called and spoke to someone who claimed that I hadn't sent a message and that they hadn't received anything from CVS/caremark, and then I finally sent a third message which did make it through. And it turned out that a prior authorization was needed.

For a medication without which I will [**_DIE A TERRIBLE DEATH_**](https://en.wikipedia.org/wiki/Diabetic_ketoacidosis).[^3]

I received a robo-call and then a form letter from my insurer informing me that they were going to allow me to continue to live by granting me a prior authoriztion for my insulin until I am 65, at which point I suppose I become Medicare's problem. If there still is a Medicare in 2039.

So on Tuesday, I called to see about getting the prescription off hold and filled. The person I spoke to assured me that she had accomplished this.

One thing that CVS/caremark is good at is sending email. I got a number of emails informing me about all sorts of things over the last two days, but nothing about my insulin. So I decided to take a small break from work and check the status online. It was still on hold. I called. The prior authorization had not yet made its way through the system to the point where my prescription could be filled. The rep told me I needed a prior authorization and I told him that I would be happy to tell him the reference number on the letter I received from my insurer. He did a bit more checking and lo, there it was. And now it's supposedly free to be filled and shipped to me next week.

Let us now take a moment to contemplate how this ridiculous system hurts people who can't manage their insurer or CVS/caremark's website either because they're hard to use or because lack of internet access. How it hurts people who can't make phone call after phone call to sort things out. How this hurts people who don't know that they need to keep that piece of paper they got in the mail. How this hurts people with various kinds of disabilities who have to rely on their caregivers to navigate this system on their behalf. On all sorts of people, really. I am _lucky_ that I am able to go Full Karen if needed to get this shit taken care of--not everyone can. And not everyone is as persistent or as stubborn as I am.

My stubbornness has served me well.

And after that delightful intermission, I went back to work. I finally got the data completed so we will be able to grant folks their achievement when it goes live and then I decided it would be fun to work on this site.

There's still a lot I want to do to move things around to my liking--the icon, the colors, the font and spacing--but the structure of this theme is significantly more simple than the other one and I was even able to leave a helpful comment on one of the issues on GitHub about the tags page. Even though it looks like the developer has abandoned the project--there are two open PRs to fix the same problem, but neither of them actually fix it!

But you know, it keeps me out of trouble. And only scares me a little bit, that I might be turning into my father, who spent most of my childhood and well into my adulthood sitting in front of a computer, coding. (In other words, I come by this naturally. Or something.)

Things I want to do, in no particular order:

- New image in the header
- Previous/Next links on individual pages
- Post wordcount because why not?
- Removing the "Home" menu link on the home page, golly that drives me up a wall
- New font and colors
  - Get rid of the embedded font files, who does that in the year of our Lord 2022 just find a nice Google font and let it goooooo
- Emoji support
- Stripping out all the code I don't want to use, like the comments and the jquery and the analytics
- Combining desktop and mobile page navigation into one file
- Killing the image gallery deader than a doornail
- Looking into adding support for [IndieWeb](https://indieweb.org/) stuff!

And here's your reward: a picture of the first roses of the season. This a polyanthus variety called "The Fairy," the blooms are only about 1" in diameter and there are loads of them. They don't smell, though, and they're prickly as all get out. I love them.

![First Roses of the Year](20220602-first-roses.jpeg)

[^1]:I was hospitalized for a week and was sent home with a PICC line for at-home IV antibiotics each time, which required time to administer and a weekly visit from a nurse to change the dressing. Before I had this series of hospitalizations, I was--according to my former manager--on track to achieve my goals for 2020. Afterwards, though, she characterized me in my annual review as "unreliable" and "inconsistent." Hmmmmm.

[^2]:I actually have a very nice WFH set up, thank you salary from OldJob, you're about the only thing I miss.

[^3]:Huh. Apparently the way the scientists were first able to extract and purify insulin for use in people was [by giving dogs what amounted to surgically induced pancreatic necrosis](https://en.wikipedia.org/wiki/Insulin#Extraction_and_purification). Those poor dogs.
