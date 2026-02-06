---
layout: post
title: Software is a Commodity
excerpt: If you think you have a software moat, you don't.
date: 2026-01-31
categories: ai
---

A couple years ago I wrote from the cradle of LLMs about where I saw them heading. At that time I could make the case that [algorithms are a commodity]({% post_url 2023-03-22-algorithms-are-a-commodity %}), and I focused on how to position LLMs themselves as a new algorithm to be commodified.

Fast-forward to today, the LLMs are now capably writing code in tools like Copilot, Claude, and Cursor. In response, I want to upgrade my perspective - all software is a commodity.

Software is no longer scarce. It is abundant thanks to the code-writing LLMs. A moat can only be built with scarcity. Your software is not a moat. Your competitors can have the exact same software as you, if they want. The only scarce digital assets that you can have now are data: home-grown proprietary data, and permission to access other people's data.

Data was already the king of value back when algorithms were commodities. But it was also the case that you could write software well enough, either with enough velocity or enough product-driven prescience, to stay ahead of the competition. Software itself was a kind of proprietary asset. This is no longer the case. You could hire the greatest product managers in the world, armed with the best vision. The software you then write will be in your competitors' hands shortly after. You're effectively nothing more than free R&D for their product roadmap.

For a timely example of this, look at how Cursor can't keep a meaningful lead on Copilot in VSCode. Cursor could come up with the most brilliant feature in the world, and Microsoft would say thanks for the idea and implement it next month. Claude is positioned more intelligently. Since Anthropic is training their own LLMs, a process that takes **data**, they can maintain a meaningful distinction from Microsoft. Even if Claude and Copilot end up with the exact same features, Anthropic will have options for monetizing their models. Unless Cursor can pivot, it is destined for obsolescence. Some of its investors will look back and say, woops, a feature isn't a business. But the bigger takeaway is that _software_ isn't a business.

I may be jumping the gun a bit. I think for a short time there will be some exceptions for mega-scale software. If you've spent the past 30 years building an industry staple that they teach kids about in textbooks -- we're talking operating systems, professional editing tools -- it's not like some new company with a fleet of LLMs is going to be competing with you overnight. But it won't take them 30 years to catch up, either.

For the vast majority of people though, who dream of creating software that solves a specific need and charging a justifiable recurring fee for access; your dream is dead. That's not a business plan anymore.

## What's changed in the last two years?

I was far more bearish about the value of LLM-generated code until mid-2025. There's been a few key advancements in the last year that changed my mind.

First, we found an effective way to index entire codebases and make them available to coding agents. These indexes understand code at the symbolic level, exceeding what was possible when LLMs only treated code as more text.

Second, software development roles were successfully separated out into three sub-agents. One researches a task, another takes that research and plans what to do, and the last one takes the plan and implements it. This separation of responsibilities addresses the key problems of "one-shotting". The agents are tightly scoped and don't stray off task. There's ample room for human review at the hand-off points. Hallucinations can be minimized and contained early.

And third, we discovered the importance of context management. Much like RAM in a classical computer, an agent performs better with more context. Gone are massive global header files telling the agents how to do every possible task they might need to do. This approach has been replaced by a brief index of tools that can be forked out to a sub-agent with its own context, who then returns only the juiciest data to the parent context.

The models themselves did also get smarter, with more specialized training data. But I think this is the least important advancement compared to the other three I mentioned. I'd rather have an older model in a modern Copilot/Claude/Cursor harness than a bleeding edge model in a plain chat interface.

The sum of all these advancements has created a moment that must feel like how lumberjacks felt when the chainsaw was invented. This thing that I used to do manually can now be done at an unquestionably faster rate with the help of automation. It didn't lead to tree service companies sending out fleets of unmanned chainsaws. That's science fiction. And so is replacing developers completely with coding agents. This is a new automatic tool that makes human programmers faster when you put it in their hands.

## How commodification happens

I should explain the mechanism by which software is being commodified. If software _used to_ be a moat, why was that? It was because the rate of development was slow enough that, if you got a lead on competitors, you had time to capitalize on the lead before they caught up. They couldn't just catch up with raw manpower. There is a sub-linear benefit to adding more headcount, because coordination costs increase as described by the Mythical Man Month. If you wanted to catch up, you had to pretty much walk the same path they walked, at roughly the same pace.

Historically we've been able to improve developer velocity by automating specific tasks by hand, like testing or deploying; this has led to incremental productivity gains. Agentic coding accelerates development velocity in an entirely new way that multiplies instead of increments. If you're copying books by hand, you can develop cursive writing to do it faster; but you're still nowhere near what can be achieved by inventing the printing press.

This increase to developer velocity triggers an inflection point in fast-following. Call it supersonic-following if you want to keep with the metaphor. We've broken the sound barrier on fast-following. Your competitors will always catch up to you now.

Why don't the competitors simply stay multiplicatively further ahead with the help of agentic coding? The LLMs have yet to make a similar supersonic jump in validating good ideas. Product vision is still moving at human speed. You still have to pound the pavement to validate ideas before you code them, or spread yourself thin with a shotgun approach. Knowing what to build is not any easier. But building it is multiplicatively easier. This is the same principle that fast-following exploits -- you can draft the thought leaders for a velocity boost. The boost is much bigger now.

## Putting it all together

It's time to think differently about how we evaluate viable businesses. Forget your software, it's a means to an end. Think instead about your data. Data will remain valuable because it can be tied to real-world relationships and trust. You can still build something no one else has off the back of that.

Do you ingest data, collate it, corroborate it, summarize it, reshape it, chart it, etc? Do new customers trust you enough to hand over access to their data? The more of these qualities you can stack, the more success you'll have in the age of commoditized software.

Everyone else, you're about to find out where all the blockchains went.