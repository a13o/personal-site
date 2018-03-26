---
layout: post
title: The Danger of Game Options
date: '2014-06-12 06:01:50 -0700'
categories: game-design
---
There's a game night at the Folsom St Foundry every Tuesday in San Francisco. [Organizers](http://www.showdown.gg/) fill the block-sized event space with board games strewn across a dozen tables and hook up over twenty consoles running popular multiplayer games. In such a competitive mecca, could you conceive a scenario where two game experts are not able to play each other fairly?

I can, and it's due to the danger of game options.

I play [TowerFall](http://www.towerfall-game.com/) at this game night every time I go. It's a game where you're an archer and you try to kill the other archers. It was designed by [Matt Thorson](http://www.mattmakesgames.com/) to play like any competitive fighter: matches are primarily about positioning with lots of room for head games, counters, and complex feats of dexterity.

![](/assets/game-options/tf.png)

_This is TowerFall_

Before talking generally about the danger of game options let's dive into a specific case study using TowerFall.

### Fighting Game 101: Threatened Space

As a fighting game student you learn about concepts like positioning and threatened space. Here is a screenshot from the Super Street Fighter II: Turbo tutorial made by [David Sirlin](http://www.sirlin.net/), a prolific writer on competitive fighting game strategy. You can watch the whole tutorial video on [YouTube](https://www.youtube.com/watch?v=d0cFs5mHQC4).

![](/assets/game-options/st_threatened_space.png)

Notice the red rectangle, this shows the space Ryu (on the right) threatens with his fireball move. The idea is that you want to keep players in space you threaten while staying out of space they threaten. The long reach of Ryu's fireballs means Ryu can stay safely across the screen and out of reach of many of his opponent's attacks. Consequently, playing against Ryu means learning how to dodge fireballs long enough to close the gap and force Ryu into spaces you threaten.

Let's look at TowerFall's orange archer, about to shoot an arrow. What area do you think he threatens?

![](/assets/game-options/tf_threatened_space.png)

Arrows are small and you know how they behave in the real world so on first guess you might think the threatened space looks something like this:

![](/assets/game-options/tf_threatened_space_autoaim_off.png)

That's a pretty small amount of space. In the Street Fighter example, Ryu was threatening a full third of the screen! TowerFall has way more space to move around in and smaller projectiles. If arrows threatened like this it would be too hard to hit anything and matches would take too long. So instead, an arrow in TowerFall threatens this much space:

![](/assets/game-options/tf_threatened_space_autoaim_on.png)

How does one little arrow threaten all that space? TowerFall gives each arrow a slight amount of heat-seeking. If an opponent gets too close the arrow will begin to alter its velocity to lean towards the opponent. It would be a bad idea for the green archer to go anywhere into that triangle.

### Fighting Game 102: The Scrub

The next fighting game concept you learn is the scrub. Scrub is not simply a derogatory term used to describe players with little skill. The scrub is well defined in Sirlin's [Playing to Win](http://www.sirlin.net/ptw) book, available for free online. From the book:

> A scrub is a player who is handicapped by self-imposed rules that the game knows nothing about.

If you were playing TowerFall with a scrub they might complain that an arrow which kills them via seeking is "cheap" or "unfair". In the gif below the cyan archer's arrow first curves up and then down to kill the orange archer. This shot is not possible without seeking arrows. Yet it is easy to see why this shot should succeed when imagining the threatened area diagram from earlier.

<iframe src="http://gfycat.com/iframe/HighMagnificentAlbertosaurus" width="480" height="360" frameborder="0" scrolling="no"></iframe>

### Now Things Get Ugly

If all the scrub could do at this point is complain, the story would end. If they wish to continue playing TowerFall they have to make peace with seeking arrows. Unfortunately, TowerFall does just about the worst thing you could do in this situation. **TowerFall has a setting which disables seeking arrows.**

![](/assets/game-options/no_seeking_variant.png)

That setting legitimizes the scrub's complaint. They no longer have to learn. Instead they can say: "if the game lets you turn off seeking arrows, then it must be a valid way to play." In their mind, they have made TowerFall a more expert game by removing auto-aim for babies. In reality, they have undermined a core design tenet of the game. Remember that TowerFall only wishes to be a game about positioning and head games. It does not wish to be about parabolic trajectory simulation.

When you allow players to undermine core design tenets, you fracture your player base. In TowerFall's case, you get experts who play with seeking arrows and experts who play without. Every kill now comes with a caveat: "In _my_ rules that wouldn't kill me." The statement drips with superiority. No middle ground will ever be found between these players, they are simply incompatible.

### Balancing Accessibility with Competitive Goals

Matt Thorson was concerned that including the No Seeking Arrows option would fracture the competitive community and in a twitter conversation revealed he almost removed the option as a result.

> yeah this is why I almost took No Seeking Arrows out in the final release
>
> &mdash; Matt Thorson (@MattThorson) [June 6, 2014](https://twitter.com/MattThorson/statuses/474809726132563968)

The reasoning behind keeping the option in is noble. One of Matt's design goals was that TowerFall be an inclusive game and therefore he didn't want to remove any option which improves accessibility. A dad who likes to play with his younger daughter might disable seeking arrows for only himself as a way to make the matches more fair. If the setting weren't available at all, the two might not be able to battle in a way that is enjoyable for dad. TowerFall also contains about 70 other game options that are pure arcade fun such as laser arrows that bounce off walls infinitely. Turning off seeking arrows might combine in interesting ways with those other options to create entirely new ways to play the game.

> settled on adding the tournament rules presets instead
>
> &mdash; Matt Thorson (@MattThorson) [June 6, 2014](https://twitter.com/MattThorson/statuses/474809926418956288)

Keeping the option in the game negatively impacts the competitive scene but benefits casual play. This seems like an impasse. Matt's clever compromise was to add a button at the top of the settings page which turns on an explicit set of tournament rules -- rules which keeps seeking arrows enabled. This signals to the competitive community how they are meant to play the game without needing to remove the option entirely.

Unfortunately this solution is not without its flaws. I occasionally encounter scrubs who wish to play with No Seeking Arrows on the competitive level. As a fun design exercise, consider what modifications you would make to solve this issue.

### Options Shouldn't Mess With Core Design

So far we've gone into great detail on the TowerFall case study but you can probably think of lots of other games that fragmented their player base by providing options. Here's a few famous ones that come to mind:

1. Super Smash Bros Melee lets you turn off all items.
1. Team Fortress 2 allows server mods which increases max players from 24 to 32 and decreases respawn timers from 20 seconds to 5.
1. A popular Beer Pong rule doesn't count your shot if your elbow is over the table.

In each of these games the main problem is that a game option was added which gives players control over the behavior of a core design tenet. Items are an integral part of balancing Smash Bros characters, kind of a global move-set that homogenizes the characters. Take items out and you end up with the current Smash Bros competitive scene, which is playable with only 8 of the 26 characters on 5 of the 29 stages. Choke points are necessary for tension in Team Fortress 2 maps and those choke points become unbalanced and never-ending when too many players spawn too quickly. Beer Pong's elbow rule is completely unenforceable without a replay camera and leads to plenty of arguments and animosity.

### So Don't Have Options

37Signals, the software development team behind Basecamp, published a book called [Getting Real](https://basecamp.com/books/Getting%20Real.pdf) which covers their software design principles. Many of them are also great game design and development advice. Here is a relevant section on preferences:

> You're faced with a tough decision: how many messages do we
include on each page? Your first inclination may be to say, "Let's
just make it a preference where people can choose 25, 50, or
100." That's the easy way out though. Just make a decision.
Preferences are a way to avoid making tough decisions.

![](/assets/game-options/gmail_options.png)

_Gmail hasn't read the 37Signals book_

You should strive to have as few options in your game as possible. It's up to you as the designer to make the right call for the best play experience. If you are unsure which way to go on a particular option you might need to playtest with friends or spend a week with each option while you develop other features. Eventually you'll gain mastery of the topic and be able to make the right call.

### Takeaway

When designing a multiplayer game be aware that by providing game options, through nothing more than human nature, you are giving your players the tools they need to avoid playing with one another. You are actively working against the virality and social effects you are counting on to cultivate and grow a multiplayer scene. This is the danger of game options.

As for the TowerFall design exercise I mentioned earlier, I think the best solution would have been to create two top level game modes called Competitive Versus and Arcade Versus. Competitive Versus provides no option controls and locks the options to the official tournament rules. Arcade Versus is the existing versus mode with options controls. This creates two environments that explicitly state their purpose upfront and allow Matt to have authoritative control over the competitive design vision.
