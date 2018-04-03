---
layout: post
title: Shut Up Everybody!
excerpt: A chrome plugin that hides comments on the internet.
date: 2013-06-08
categories: projects
---
The internet is full of opinions. If you're like me you can't help but wade into the comments thread on a controversial blog post. It's a guilty pleasure. Wouldn't it be nice if a computer could detect the most inane opinions and protect you from seeing them at all?

I developed a simple heuristic to determine if something is inane. If a block of text contains 'I', 'me', or 'my' we can say with acceptable confidence that that block of text is an opinion. This completely purges the internet of anecdotes and therefore anecdotal evidence -- one of the most inane and useless arguments someone can make.

Next I built that heuristic in javascript and wrote a Chrome extension that will scan any page you're on and hide the offending text. At first it just made the text node invisible, but that's not fun. With a little more javascript we can have the plugin blacking out lines of text, like an excited FBI intern declassifying her first document. It looks like this:

![](assets/shut-up-everybody/sue_redact_example_1.png)

And if you're wondering what excellent conversation Mr. Gunneh and EdgeX are having you can hover over the redacted bars to see through them:

![](assets/shut-up-everybody/sue_redact_example_2.png)

Mission friggin' accomplished.

[Get it from the Chrome Web Store by clicking here.](https://chrome.google.com/webstore/detail/shut-up-everybody/fblbhjoaifndkejdmllpimdpgmhddheg)

# Unintended Consequences

The heuristic is a little overzealous. For example this entire blog post, written as a first person story, gets decimated. That's why the extension comes with a button in the address bar that you can click to toggle it on and off. It's also disabled by default on Facebook, where the whole point is to share I/me/my stories.

I'm always on the lookout for ways to improve the heuristic. I've made it a lot better recently by ignoring certain DOM elements that are unlikely to contain user generated content; elements like forms, scripts, and links are now ignored.

There's going to be an upper limit to what I can do with DOM parsing, however. There's no generic way to tell the difference between an informational statement like "My house is three blocks from the liquor store" and an inane opinion like "I can prove that Obama isn't an American." To fix that I'd have to enter the infinitely deep rabbit hole of grammatical analysis and set up a backend for the machine learning.

# Unintended Benefits

The overzealous nature of the heuristic hasn't been without benefit. A few of the blog sites I frequent ended up getting large parts of their _article content_ redacted. I wasn't expecting that! The implications are profound. It turns out I'm reading lots of sites that I consider news sites, but are really opinion rags. What's worse is the articles that get their content redacted are the same ones that have the most pageviews and most comments.

I've stumbled onto a seedy motivator in the world of online journalism. I have a solution to that too, which you can read in my blog post about [creating accountability for opinions on the internet](creating-accountability-for-opinions-on-the-internet).
