---
layout: post
title: "Energy Systems Are Back! Clash Royale"
date: '2016-03-19 16:14:26 -0700'
categories: game-design
---
Clash Royale is Supercell's latest hit and boy is it packing a surprise! Supercell has invented a brand new kind of energy system that doesn't punish players like traditional energy systems do. If you haven't played Clash Royale, it's a competitive game where two players go head-to-head in real time using customizable armies. Winning a match awards a locked chest and opening these chests gives you cards to improve your army. Chests take at least 3 hours to open, must be opened one at a time, and there's only room to hold four of them. This combination has the effect of creating an implicit energy system. Other deconstructions aren't going deep enough to study the relevance of this new design so let's see what we can learn!

![photo of clash royale home screen](/assets/Energy-Systems-Are-Back-Clash-Royale.jpg)

To give you a visual reference point, in the screenshot above all four of my chest slots are full. I'm unlocking a silver chest in the second slot which will be open in another two-ish hours; or I could pay 13 gems (about $0.11 USD). I also have a gold chest with rarer cards in it, but it takes eight hours or 48 gems (about $0.38 USD) so I'll save that for when I go to bed. There's little incentive to play another match right now because there will be nowhere to put my chest reward and I'll have wasted it. So you could say I have zero energy and I'll get 1 energy back when that chest finishes opening.

As you can see, energy in Clash Royale doesn't behave like energy in other games. It's also never explicitly referred to as an energy system. To find the differences between Royale's energy system and a more traditional one, and also prove their conceptual similarities, I built both Royale and Candy Crush's energy systems in Joris Dormans' wonderful Machinations tool. Machinations lets you easily model game economies and see the relationships between their parts. There's a nice article on Gamasutra covering the basics[^1] and even a textbook on the subject but I'll explain my diagrams fully so that you don't have to read other articles (or textbooks!) to follow this one.

Let's start with a familiar energy system like the one found in Candy Crush Saga.

![candy crush machination](/assets/Energy-Systems-Are-Back-Clash-Royale-1.jpg)

1. The labeled circle at the top of the diagram is the player's pool of energy. Players can have up to 5 energy in Candy Crush.
1. Anything drawn with a double outline represents player interaction. The decision diamond labeled ';Play' and the triangle labeled 'Wait' are both player actions.
1. When you click Play, for simplicity's sake the diagram gives you a 50/50 chance of winning or losing a game in Candy Crush.
1. Up and down triangles are very simple; they create and destroy energy respectively. The Wait triangle acts as a source of new energy into the system. Click it, and energy appears! The Lose triangle drains an energy from the system.
1. When you win a game, your energy hits that weird sideways triangle with a line through it; that thing is called a converter because it converts your energy into a new level unlock! The player starts at Level 1 and whenever they win they gain access to the next level.
1. Whenever you unlock a new level that dotted line acts as a trigger, telling the source triangle it's pointing at to create an energy and add it to your pool.

This simple diagram simulates Candy Crush's energy system perfectly. When you lose a game you lose an energy. Winning a game unlocks the next level and gives you back an energy, so as long as you win you can keep playing indefinitely.

Now let's look at a similar diagram for Clash Royale!

![clash royale machination](/assets/Energy-Systems-Are-Back-Clash-Royale-2.jpg)

Royale's energy diagram is slightly more complex than Candy Crush's but not by much.

1. You still have a pool of energy in Royale - your four empty chest slots.
1. There's still only two possible player actions: Play and Wait.
1. Losing a game doesn't give you a chest; so you effectively get your energy back.
1. When you win, a chest fills one of your slots and therefore you lose an energy. The diagram represents this with a converter, labeled Win, which takes an energy and converts it into a chest.
1. Players can wait (as long as they have a chest) which converts their chest into new cards and frees up the chest slot, returning an energy.

Now that we've had our salad, it's time for the meat and potatoes! What can we learn about each system with these diagrams? Here they are again next to each other for easy comparison.

![comparison of machinations](/assets/Energy-Systems-Are-Back-Clash-Royale-3.jpg)

_(If you want an interactive version of the diagrams I've hosted one [here](/mirrors/clashroyalmachinations/){:target="_blank"}.)_

The biggest difference is what happens when you win or lose. They're complete opposites! Candy Crush punishes you for losing; and after enough punishments you can't play anymore unless you wait or pay money. This is a heavily criticized aspect of energy systems. King is a business and needs to make money. But the only way to make this diagram work for King's business goals is to weigh outcomes towards losing. Candy Crush does exactly that. Level difficulty ebbs and flows, giving you a handful of fun levels before stopping you in your tracks with a level tuned too tightly to reasonably win. You're gonna need a little luck to beat that level. King's hope is that you will be compelled to pay them for more tries or for cheats that re-balance the difficulty more in your favor.

Clash Royale on the other hand, has no punishment for losing. You can play as much as you want until you win! And when that win happens we see our next difference. Royale now asks you to wait to get your reward (the cards inside the chest) whereas Candy Crush gives you your reward immediately (unlocking the next level).

These two systems are built using nearly identical components, but they couldn't be any more different. Candy Crush's diagram sets King up as an adversary with its own customers. When the players are winning, King doesn't make any money. And when King is winning (at business), it means players are stuck repeating a frustrating level. Supercell on the other hand, only monetizes when its customers are succeeding at Royale.

By looking at these Machinations diagrams I would say Royale has a much healthier business model. It has been proven that the key to successful F2P is a positive long-term relationship with players.[^2] While players may still get frustrated at having to wait to open their chests, they at least know that when they're done waiting they will be given cards to improve their armies. Candy Crush can't make that promise. You can wait and wait and wait and each energy you earn may still result in a loss - netting you no progress. It's much more player friendly to only ask players to wait when you know you are going to have good news to tell them.

Another benefit to Royale's approach is that waiting is only tied to earning rewards - not playing the game itself. You could keep playing Royale even with no energy. You would still battle opponents and gain skill and knowledge. There's just no card rewards attached to your wins. We could say that Royale has _soft waiting_. You're asked to wait to play the game optimally but there is still a way to play the game indefinitely for free. Candy Crush on the other hand has _hard waiting_. You can't even replay old levels you've already beaten if you don't have any energy.

One last benefit I want to cover is the educational importance of changing energy consumption to happen on a win instead of a loss. Every game, even Candy Crush, has an element of skill and the best way to improve skill is to practice. Losses are important information when practicing because each loss tells you one thing that doesn't work. Building a collection of losses engages our human nature. What trends are present in my losses? How can I overcome them? Candy Crush limits your learning potential because you may run out of energy before you've reached an epiphany. Royale has no such limit. It allows players to fail forever until they learn a lesson. This is especially important in a deck building game where new deck ideas must be playtested to measure their viability. Players would be more reluctant to try new deck ideas if it meant eating into their energy supply.

## Monetization

Since both games attempt to monetize waiting, let's take a look at the price of skipping a timer in each game. Clash Royale's gems cost about $0.01 USD each and Candy Crush Jelly Saga's bars cost about $0.10 USD each. There are discounts for buying in bulk. I used that information to create these charts showing the cost for skipping a single energy timer at each purchase tier.

### Clash Royale Cost Per Energy (USD)

| +Energy | Desc | Gems | $0.99 Pack | $4.99 Pack | $9.99 Pack | $19.99 Pack | $49.99 Pack | $99.99 Pack |
|-:|-|-:|-:|-:|-:|-:|-:|-:|
| 1 | silver | 18 | $0.22 | $0.18 | $0.15 | $0.14 | $0.14 | $0.13 |
| 1 | gold | 48 | $0.59 | $0.48 | $0.40 | $0.38 | $0.37 | $0.34 |
| 1 | giant/magic | 72 | $0.89 | $0.72 | $0.60 | $0.58 | $0.55 | $0.51 |
| 1 | super magic | 144 | $1.78 | $1.44 | $1.20 | $1.15 | $1.11 | $1.03 |

### Candy Crush Jelly Saga Cost Per Energy (USD)

| +Energy | Desc | Bars | $0.99 Pack | $4.99 Pack | $9.99 Pack | $20.99 Pack | $39.99 Pack |
|-:|-|-:|-:|-:|-:|-:|-:|
| 5 | refill health | 9 | $0.18 | $0.16 | $0.16 | $0.15 | $0.14 |
| 1 | more moves | 9 | $0.89 | $0.82 | $0.78 | $0.73 | $0.71 |

Energy costs in each game fall within the same range, about $0.14 - $0.16 USD per energy. So immediately we can see that Royale is not suffering in its monetization potential as a result of flipping energy systems on their head.

In fact, the opposite is true. While 75% of the chests you receive in Royale are silver chests which are comparable to Candy Crush's costs, the remainder are special chests with longer timers and bigger costs. Those actually drop on a fixed schedule and players have figured it out. I'll spare you the calculations, but here is the overall average cost for 1 energy at each purchase tier once you've taken into account the chest rarity distribution.

### Average Clash Royale Cost Per Energy (USD)

| +Energy | Desc | Gems | $0.99 Pack | $4.99 Pack | $9.99 Pack | $19.99 Pack | $49.99 Pack | $99.99 Pack |
|-:|-|-:|-:|-:|-:|-:|-:|-:|
| 1 | avg | 27 | $0.33 | $0.27 | $0.22 | $0.22 | $0.21 | $0.19 |

This is actually much higher than Candy Crush! The bigger chests you receive aren't an arbitrary energy cost penalty, either. They contain more cards and rarer cards. Supercell is simply scheduling an occasional higher purchase, all made possible by their new energy system. By tweaking these timers and drop rates they have a lot of ability to tune the energy cost to their business needs. If Candy Crush wants to get more money out of energy they have to resort to less civilized techniques. Note that one of Jelly Saga's purchase tiers is $20.99 instead of the expected $19.99. This makes it harder to compare package discount rates, and Candy Crush relies on that confusion to move the needle a little. Not very player friendly.

Clash Royale's new energy system improves on traditional energy systems in nearly every category. A common and unfortunate perception of F2P is that monetization must come at the player's expense. (Pun intended.) Supercell defies that premise with a design that is both player friendly and financially capable. Since energy systems are somewhat generic design components that can be worked into all sorts of genres we are potentially looking at the keys to a F2P renaissance wherein more game developers can find success, because their new ideas can be built around existing successes like Royale's energy system. We should expect an energy system that works with players instead of against them to transform the F2P landscape just like rewarded video did for ad monetization. The energy system is back! Which of your old game ideas can you dust off and soup up?

---
[^1]: Ernest Adams, Joris Dormans, The Designer's Notebook: Machinations, A New Way to Design Game Mechanics, <a href="http://www.gamasutra.com/view/feature/176033/the_designers_notebook_.php" target="_blank">http://www.gamasutra.com/view/feature/176033/the_designers_notebook_.php</a> (August, 2012).

[^2]: Emily Greer, Building Games for the Long-Term: Maximizing Monetization and Player Satisfaction, <a href="http://www.gdcvault.com/play/1018265/Building-Games-for-the-Long" target="_blank">http://www.gdcvault.com/play/1018265/Building-Games-for-the-Long</a> (March, 2013).
