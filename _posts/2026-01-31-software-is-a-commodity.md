---
layout: post
title: Software is a Commodity
excerpt: If you think you have a software moat, you don't.
date: 2026-01-31
categories: internet
---

A couple years ago I wrote from the cradle of LLMs about where I saw them heading. At that time I could make the case that [algorithms are a commodity]({% post_url 2023-03-22-algorithms-are-a-commodity %}), and I focused on how to position LLMs themselves as a new algorithm to be commodified.

Fast-forward to today, the LLMs are now capably writing code in tools like Copilot, Claude, and Cursor. In response, I want to upgrade my perspective - all software is a commodity.

This is maybe not a big mental leap for programmers. Software `is-a` algorithm, so the new claim maps easily onto the old. However, I think this is still worth covering in detail because of the implication it has for business strategy. Consider SaaS, Software-as-a-service, where 'software' is more than a technological term -- it's also a business construct. The point I want to make, to anyone who _Does Business_, is that your entire software is a commodity now. If you sell software in 2026 and beyond, your software provides no inherent advantage over your competitors. Businesses who continue to think selling software is a compelling business plan, will find themselves softly gliding into the ground.

Software is no longer scarce; it is abundant, thanks to the code-writing LLMs. A moat can only be built with scarcity. Your software is not a moat. Your competitors can have the exact same software as you, if they want. The only scarce digital assets that you can have are data: home-grown proprietary data, and permission to access other people's data.

This was already true back when algorithms were commodities. But it was also the case that you could write software well enough, either with enough velocity or enough product-driven prescience, to stay ahead of the competition. This is no longer the case. You could hire the greatest product managers in the world, armed with the best vision. The software you then write, will be in your competitors' hands shortly after. You're effectively nothing more than free R&D for their product roadmap.

For a timely example of this, look at how Cursor can't keep a meaningful lead on Copilot in VSCode. Cursor could come up with the most brilliant feature in the world, and Microsoft would say thanks for the idea and implement it next month. Claude is positioned more intelligently. Since Anthropic is training their own LLMs, a process that takes **data**, they can maintain a meaningful distinction from Microsoft. Even if Claude and Copilot end up with the exact same features, Anthropic will have options for monetizing their models. Unless Cursor can pivot, it is destined for obsolescense. Some of its investors will look back and say, woops, a feature isn't a business. But the bigger takeaway is that _software_ isn't a business.

The term Software-as-a-service will stick around, because it has so much marketing cachet. But going forward, what people will really be buying is Data-Management-as-a-Service. I think this can be further distilled to Data-Trust-as-a-Service. Folks involved in signing SaaS contracts can see proof of this first hand. Every potential customer is going to ask you to fill out a Vendor Security Questionnaire. This is a trust-establishing document, because what you're really selling is trust.

## What's changed in the last two years?

I was far more bearish about the value of LLM-generated code until mid-2025. There's been a few key advancements in the last year that changed my mind.

First, coding tools found an effective way to index entire codebases and make them available to coding agents. They no longer waste precious context space searching and ingesting relevant portions of the codebase.

Second, software development roles were successfully separated out into three sub-agents. One researches a task, another takes that research and plans what to do, and the last one takes the plan and implements it. This separation of responsiblities addresses the key problems of "one-shotting". By introducing human review at the hand-off points, hallucinations can be minimized and corralled.

And third, there's been many optimizations for the sake of context management. Much like RAM in a classical computer, an agent performs better with more context. Gone are massive global header files telling the agents how to do every possible task they might need to do. This has been replaced by a brief index of tools that can be forked out to a sub-agent, who returns only the juciest data to the parent context.

The models themselves did also get smarter, with more specialized training data. But I think this is the least important advancement compared to the other three I mentioned. I'd rather have an older model in a Copilot/Claude/Cursor harness than a bleeding edge model in a plain chat interface.

The sum of all these advancements has created a moment that must feel like how lumberjacks felt when the chainsaw was invented. A thing that I used to do manually can now be done at a faster rate with the help of automation. No tree service is sending out fleets of unmanned chainsaws to cut down trees. That's science fiction. And so is replacing developers completely with coding agents. These are new automatic tools that make human programmers faster when you put it in their hands.

## What's all that have to do with the commodification of software?

I think it's important to explain the mechanism by which software is being commodified. If software _used to_ be a moat, why was that? The rate of development was slow enough that, if you got a lead on competitors, you had time to capitalize on the lead before they caught up. There was a sub-linear benefit to adding more headcount, because coordination costs would increase as described by the Mythical Man Month. If you wanted to catch up, you had to pretty much walk the same path they walked, at roughly the same pace they took.

Historically we've been able to incrementally improve developer velocity by getting into the weeds on infrastructure and static analysis, but these were fractional gains. Agentic coding accelerates development velocity in an entirely new way that multiplies instead of increments. If you're copying books by hand, you can develop cursive writing to do it faster; but you're still nowhere near what can be achieved by automating with a printing press.

This increase to developer velocity triggers an inflection point in fast-following. Call it supersonic-following if you want to keep with the metaphor. We've broken the sound barrier on fast-following. Your competitors will always catch up to you now.

Why don't the competitors simply stay multiplicitavely further ahead with the help of agentic coding? The LLMs have yet to make a similar supersonic jump in validating good ideas. Product vision is still moving at human speed. You still have to pound the pavement to validate ideas before you code them, or divide your velocity on a shotgun approach. Knowing what to build is not any easier. But building it is multiplicatively easier. This is the same principle fast-following exploited - draft thought leaders for a velocity boost. That boost is much bigger now.

## Putting it all together

It's time to think differently about how we evaluate viable businesses. Are you selling data management? Do you ingest data, collate it, corroborate it, summarize it, reshape it, chart it, etc? Do new customers trust you enough to hand over access to their data? If you can view your business through this lens, you're poised for success in the age of commoditized software.

Everyone else, you're about to find out where all the blockchains went.