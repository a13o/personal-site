---
layout: post
title: Search Isn't Solved
date: '2014-07-05 12:18:19 -0700'
categories: internet
---
Sometimes you'll hear people say that Search is a solved problem. It turns out that's not really true. What we've solved is a specific subset of Search where the person doing the searching already knows what it is they're looking for.

You can go to Google and search for "James Brown" or you can go to Amazon and search for "metal grabber utensil" and the search results are going to be the very things you seek. It doesn't matter how vague metal grabber utensil is, the second search result is for cooking tongs. _That_ search is solved.

![amazon search result for metal grabber utensil](/assets/search-isnt-solved/metal_grabber_utensil.png)

There's a whole other class of search problems, though, and computers are terrible at them. I call it concierge search and here are some example queries:

* What video game should I play while I'm commuting?
* What book should I read next?
* What movie should I watch for date night?

In concierge searches you don't know what you're looking for, but you'd like an answer anyway. You want someone or something more knowledgeable than you to help out. Probably the first thing you'll notice about these queries is that they're not really trivia questions where there is a definitive answer. Instead, they're the start of a conversation. The answer is going to be personalized to your needs.

If you want a game to play on your commute, you could ask a friend for some advice. They'll undoubtedly have some questions. What gaming device do you have with you? What kind of games do you usually play? Do you have internet on your commute and how reliable is it? They could ask a bucket of other really specific questions too, like: do you want to compete with your friends on a leaderboard? Are you okay with spending $20/month in microtransactions to stay competitive?

## Examples of Bad Concierge Search

There's some really bad half-assed attempts at concierge search. The biggest most successful sites use them, and they suck, and we all know they suck. Let's look at some sucky search implementations and go over why they suck. Suck.

### Taxonomy Drill-downs

Every book has a genre. Every game, every movie, a genre. At the start of your search you're presented with a list of these genres.

![netflix top level taxonomy](/assets/search-isnt-solved/netflix_taxonomy.png)

You already don't know where to begin. What if you tend to like movies in over half of the 20 listed genres? Which one should you explore first? I guess let's start by clicking on comedies. Now you need to figure out the next level of taxonomy. Are you looking for a dark comedy? A slapstick comedy? Satire? _I don't fucking know!_ They all sound cool!

The problem with taxonomy drill-downs is they are depth-first searches when you really want to do a breadth-first search. I want to read because I have six hours to fill on my plane ride. I just want a book I will like, the genre doesn't matter that much. Yet the website would have you believe it's the most important question of all.

Programmers and interface designers love taxonomy drill-downs because they are easy to implement and easy to navigate. Users hate them because taxonomy drill-downs are lousy at finding anything. Yet, this is how _Amazon_, the biggest book retailer on the planet, suggests you browse books. This is how Netflix suggests you browse videos. We are living in the Search equivalent of the Stone Age.

## Recommendation Engines

The next thing that doesn't work is to actually collect some data on what people are doing and then use that to make a suggestion. Here's the books Amazon suggests I read. This is an actual screen capture, honest to god:

![useless amazon book recommendations](/assets/search-isnt-solved/useless_amazon_book_recommedations.png)

I've been buying books on Amazon for over a decade. So you might think that if I went up to Amazon and said "what book should I read next?" they could make a reasonable suggestion. Instead, Amazon remembers that I just bought a Chromecast so I get a selection of three books which are all essentially Chromecast For Dummies. I've built entire computers from scratch with parts I bought off Amazon. You'd think they would know I don't need a book to figure out how Chromecast works.

Recommendation engines suck because they have no context for why you're doing the search. They naively assume that you like A, and the other people who like A also like B, so you'll like B too. They have no idea why anyone even likes A or likes B, or why there might be a relationship between A and B.

I added the musical group She & Him to my favorites. When I ask Xbox Music for recommendations they tell me to check out a group called Let's Go Sailing, because I enjoy artists like She & Him. Except Xbox Music doesn't know that I only listen to She & Him because I think Zooey Deschanel is hot and I like to imagine that she's singing me songs because she wants to impress me. So Let's Go Sailing isn't really my thing; it sounds like what I imagine every iPhone playlist in Portland sounds like. I turn it off halfway through the first song and replay another favorite, Lil Wayne.

Music suggestions for people who like Zooey Deschanel and Lil Wayne. Good luck getting your recommendation engine to do anything with _that_ knowledge, Xbox Music.

_(For the record, there is an album that meets these criteria. It's called [500 Days of Weezy](https://soundcloud.com/patrickmoberg/sets/500-days-of-weezy) and it's a mashup of the 500 Days of Summer soundtrack with Lil Wayne songs.)_

## Examples of Good Concierge Search

We're not completely stuck in the Stone Age, though. There's already some full-assed attempts at good concierge search.

### Curated Lists

I almost didn't put this one down because it's not really a technology. For any given concierge search query there is somebody who makes their living writing down the answer and posting it on the internet. This vast ecosystem covers everything from movie blog reviews to the New York Times bestseller list.

Over time you begin to trust curators. Maybe you've read so much of their work that you relate to them and feel that they _get_ you. Maybe the name is just so established you've never even questioned the curator's trustworthiness. The Michelin restaurant guide was started by a tire company because they wanted people to drive further and buy more tires. It doesn't stop anyone from humble-brag live-tweeting their French Laundry dinner.

This is actually a pretty good system. The only downside is that it's turtles all the way down. Which curators do you trust? How do you find them? I need a concierge search just to find a curator I like. Curated lists of curators. I think that's the most functional definition of Twitter I've ever seen.

### Really Really Invasive Matchmaking

If you've ever used the online dating site OKCupid then you are familiar with their approach to answering concierge search queries like "who should be my girlfriend?" OKCupid asks you as many personal questions as you can stomach and then as a follow-up asks you what answer you want your partner to give and how important it is that they give that answer. Then they compare your answers with everyone else's and as long as everyone is being truthful you'll get some pretty solid matches. Not bad.

![okcupid questions](/assets/search-isnt-solved/okcupid_question.png)

Cocktail Flow is an app that keeps track of which alcoholic beverage ingredients you have and then tells you what drinks you can make with them. It can suggest a shopping list containing specific ingredients your liquor cabinet needs if you want to make a wider variety of drinks.

![cocktail flow app shopping list](/assets/search-isnt-solved/cocktailflow_shopping.jpg)

These sorts of concierge searches are very useful if you take the time to give it all the information it needs -- which is not always a simple task.

### 20 Questions Concierge

Have you ever played the 20 Questions game? You pick an object and the computer asks you a series of yes/no questions before guessing the object you picked. It works like a binary search algorithm, trying to ask the best possible question to eliminate the most incorrect answers. This is a very clever approach to concierge search because it simulates what real live concierges do when they help you decide how to spend your vacation. An expert opens a dialog with you and after a few short minutes they've understood your motivations enough to make a recommendations.

Here is online radio site Songza in 2011.

![songza in 2011](/assets/search-isnt-solved/songza_2011.png)

It looks and operates like a recommendation engine and also is doing some 'social' stuff around trying to curate curators. Nobody was using Songza in 2011. At least, not compared to how many people started using Songza in 2012 when Songza decided to look like this:

![songza in 2014](/assets/search-isnt-solved/songza_2014.png)

In 2012 Songza released their concierge search which successfully converted their me-too radio app into a product in its own right. Other internet radios copied this feature click for click. Google _bought_ Songza in 2014.

Songza's concierge search works by seeing what day and time it is and then asking you what you're up to. I took the screenshot on Thursday morning so its opening question is a bunch of reasonable morning activities. Am I looking for a radio to play to get me out of bed and energetic? Do I want to sing in the shower? Am I... Sasha Fierce? I selected waking up happy so Sonza's next and final question is what kind of "bright, easy music" do I want to hear. _Thank you_, Songza.

## Solving Concierge Search

Google's acquisition of Songza is interesting. Obviously Songza's immediate benefit is to make Google's music service more robust. But it's not hard to imagine what impact Songza's expertise in concierge search can offer to other Google products like YouTube and the Google Play Store. Taking the long view, solving concierge search may be an integral part of Google maintaining its position on the Search throne.

I'm a game guy so I'll close out with an example of how Songza's concierge search can be applied to other forms of media search such as app store discovery.

![concierge search for games on the app store](/assets/search-isnt-solved/app_store_ex1.png)

I'd like a game to play during my commute.

![concierge search for games on the app store continued](/assets/search-isnt-solved/app_store_ex2.png)

Don't you wish searching for new things was this easy?

Unfortunately most websites we use -- even the biggest most successful ones -- are using bad implementations of concierge search. But as you can see from the good examples, there is hope! We've discovered some specific examples of concierge search that work for very narrow problems. For a while we will apply these narrow solutions to other narrow problems just like I've done above with app store discovery. Eventually we will learn the formula for a generalized concierge search and they will become as prolific on the web as the informational search box is today. And then Search will be solved.
