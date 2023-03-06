---
author: Mauro Murru
pubDatetime: 2023-03-06T14:42:52.737Z
title: How would Italo Calvino and Sun Tzu explain refactoring?
postSlug: calvino-sun-tzu-refactoring
featured: true
ogImage: /images/directus.png
tags:
  - refactoring
description: |
    The day has flown by quickly, and I have a headache. I spent the day refactoring the code. Refactoring is not a simple task - there are many things to keep in mind and many things to discover along the way. Now is the time to relax and reread a beautiful book I read many years ago.
    Invisible Cities by Italo Calvino.
---

> Cities grow, cities evolve, cities have parts that simply die 
> while other parts flourish; each city has to be renewed in order 
> to meet the needs of its populace… Software-intensive systems 
> are like that. - Grady Booch (UML Inventor)

The day has flown by quickly, and I have a headache. 

I spent the day refactoring the code. Refactoring is not a simple task - there are many things to keep in mind and many things to discover along the way.

Now is the time to relax and reread a beautiful book I read many years ago.
"Invisible Cities" by Italo Calvino.

> The city of Leonia refashions itself every day: 
> every morning the people wake between fresh sheets, 
> wash with just-unwrapped cakes of soap, wear 
> brand-new clothing, take from the latest model 
> refrigerator still unopened tins, listening to the
> last-minute jingles from the most up-to-date radio.

![leonia](/images/leonia.jpg)
https://www.deviantart.com/anan001/art/Leonia-ciudades-invisibles-de-italo-calvino-349034977

As I read this, I'm reminded of Refactoring and all the conflicts and pains that come with it. 

The Refactoring approach works similarly to Rudolph Giuliani's crime reduction strategy in New York City in the 90s. 

Clean up the city, and the city will clean itself up. 

Even though these simple words may sound like a magic formula, we have no magic wand. They hide commitment and dedication to the code/city we want to carry into the future.

## What is refactoring?

Refactoring is an internal change or evolution (in the Darwinian sense) that does not alter the code's external behaviour and aims to improve the characteristics that make our code resilient, it is intended to fix bugs that are not merely code failures but rather that affect maintainability, complexity, and performance.

It is said that to develop a good habit, we must repeat it, repeat it again, and repeat it some more, and the same goes for refactoring. 

Refactoring is not a spot activity. We should create a routine following the infinite cycle of Test-Driven Development (TDD); write the test, develop the micro-functionality on the fly to make it work, and then refactor, clean up the site and improve the connections.

Every time we refactor, we must do it in the best way possible, constantly guided by pragmatism, in other words, organizing everything within the available timeframe.

And then, once again, a red test, a new feature, and refactoring...

## Tactical and Strategic Programming

The first step to understanding refactoring is to realize there are two ways of programming: tactical and strategic. 

Kent Beck uses the metaphor of two hats, one for writing code and the other for refactoring.

Whenever we write code, we put ourselves in the shoes of bricklayers -- the professionals who, in a **tactical** way, create something functional in the shortest time possible without being concerned about the complexity increase. 

![twohats](/images/twohats.png)
https://www.deviantart.com/goombablood/art/When-two-hats-aren-t-enough-863446109

On the other hand, the **strategic** hat resembles the engineer's point of view and presupposes a holistic vision of the context. His priorities are to reduce or at least contain the system's complexity, even with a medium-long-term perspective.

Therefore, one of the engineer's tasks is to establish the goal of refactoring. To be meaningful and beneficial, the **refactoring must always have a reason and a goal to achieve. This is the task from the engineer's perspective.**

I have always said that a developer must be a monster with two personalities (that's why we are often thought of as crazy). We must learn to switch from one hat to the other quickly and with a good rhythm. In general, the more frequently we bounce between the two personalities, the better the quality of our code.

Developing a new feature or fixing a bug often increases coupling and complexity, sending style and coherence into hell. This is where we need to make a leap towards strategic thinking.

In "The Art of War", Sun Tzu says that the ideal future vision must influence present actions. 

To achieve victory, the commander must know whether the battle he is fighting today will lead him there.

> "Do not move unless you see an advantage; do not use your troops unless something is to be gained."

Unfortunately, the products we develop today often do not envision the future clearly. Our market moves quickly and is infamously mutable, so how can we guide our everyday work?

🧭 We can do it guided by **Values**.

## ****Consistency****


> On the sidewalks, encased in spotless plastic bags,
> the remains of yesterday's Leonia await the garbage
> truck. Not only squeezed tubes of toothpaste,
> blown-out light bulbs, newspapers, containers,
> wrappings, but also boilers, encyclopedias, pianos,
> procelain dinner services. It is not so much by the
> things that each day are manufactured, sold, bought
> that you can measure Leonia's opulence, but rather
> by the things that each day are thrown out to make
> room for the new.

To understand values, we must make our way through the garbage of Leonia. The first feeling we experience is disorientation. When we impact with this sensation, we notice the need for an essential value, a compass that we can call **consistency**.

The need for consistency usually arises when we sit behind our desks and face the monitor. Everything looks calm, but this is when we realize that our code looks alien to us. 

Our efforts to understand become more and more, and we spend considerable time doing so.
Frustration accumulates when the code is not designed to accommodate the modification we want, letting us with just the dream of an ideal world where the quality of our codebase equals what we imagined during the design phase.

In this situation, a dangerous driver has fueled: **fear**. TDD helps us not be overwhelmed by this feeling, at least eliminating the uncertainty of what will happen once the modification is applied. But is it enough? 
In a refactoring context where fear is present, refactoring turns into many little quick fixes. Small interventions that are driven by the intent to be less impactful as possible to avoid breaking things. Sounds scary, but here is a situation where a slight change in the code can have a ripple effect. Instead of bringing improvements, acting this way increases our code complexity, inconsistency, and instability. The code will need further refactoring again, triggering a negative spiral.

> This is the result: the more Leonia expels goods,
> the more it accumulates them; the scales of its past
> are soldered into a cuirass that cannot be removed.
> As the city is renewed each day, it preserves all of itself 
> in its only definitive form: yesterday's sweepings
> piled up on the sweepings of the day before yesterday
> and of all its days and years and decades.

This happens purely because we are not comfortable with our code. But why?

Because conventions help us orient ourselves and show us the way. What would a city be like if every neighbourhood had different street signs? 

Consistency allows us to learn things in one place and reuse/recognize them everywhere. 

Knowing the rules, we no longer need to rack our brains looking for patterns or making wrong assumptions.

Because of that, when we learn something that is not obvious from our code, we need to memorize it. But*,* unfortunately*,* our memorization ability is finite (mine is very limited), and, like the ancient scribes, when we achieve to solve the puzzle, we need to formalize our understood bringing it out from our minds and putting it into code (I mean not only on writing code but perhaps removing it is more important 😀).

## The pitfalls in the search for consistency

The need for consistency leads us to a compulsive and often unconscious search, and here are two everyday actions that arise in this situation.

The **comprehension refactoring** and the **aesthetic lifting** (Yuch refactoring).

The violent attack of comprehension refactoring is activated when we don't understand what's happening. When we are entangled in a dense maze of classes and functions, and we don't know why they are there and what they do. 

This is because nobody has yet realized that the only action needed is to bring the knowledge from the brain to code.

As Martin Fowler would say:

> Any fool can write code that a computer can understand. Good programmers write code that humans can understand. 

After all, I would say that our code is not a mystery novel.

The other trap lies behind the concept of aesthetic refactoring of our code.
When pronouncing “What is this rubbish, and who wrote it?” is the instant just before a lifting refactoring.

We, developers, dislike ugly or unfashionable code, and when we see something that does not adhere to our own standards of beauty, we refactor it.

Why do these two refactoring drivers hide a pitfall?

**The desire to throw everything away and rewrite everything from scratch is just around the corner, and we often do it without worrying too much about the sustainability of our decision.**

And so, to quote Calvino...

> he greater its height grows, the more the danger
> of a landslide looms: a tin can, an old tire, an unraveled 
> wine Bask, if it rolls toward Leonia, is enough
> to bring with it an avalanche of unmated shoes, calendars 
> of bygone years, withered Bowers, submerging the city in 
> its own past, which it had tried in
> vain to reject, mingling with the ~t of the neighboring cities, 
> finally clean. A cataclysm will Batten
> the sordid mountain range, canceling every trace of
> the metropolis always dressed in new clothes. In the
> nearby cities they are all ready, waiting with bulldozers to 
> Batten the terrain, to push into the new
> territory, expand, and drive the new street cleaners
> still farther out.


By rewriting everything, we **endanger our business**. Our decision to rewrite code is often driven by an incomplete analysis of our codebase caused often by an incomplete/limited vision given by our current perspective. When we start the rewrite, we must reconsider all of the decisions we have taken over weeks, months, and years, **facing a bill we cannot afford**.

Rewriting everything means redoing the work that has brought us to this point, including the team discussions. We also need to do new training about the new conventions.

## And then?

So, we have two paths to follow: accepting the compulsive refactoring cycle or recognizing what in our code is worth refactoring regardless of trends and/or compulsive attacks.

This is not an effortless decision, as it presupposes the development of a pragmatic awareness that leads to accepting imperfection and finding a balance between consistency and innovation.

To do this, it is essential to start with three questions:

- Do I have enough information to justify my action (whether it is a consistency break or innovation introduction),
- Wasn’t this information available in the design phase? And why was it not done that way if it was available in the design phase?
- Am I breaking conventions? How much does this cost me regarding training for people involved in the codebase?
- Does the change I am introducing really generate value in terms of maintenance from a product perspective?

Answering these questions will make it easy to see some considerations emerge.

- Refactoring the code complex areas is just the refactoring that makes sense. On the simple and understandable parts is often an effort waste.
- When estimating refactoring, we must always consider the full scope of the project, including edge cases. Often, the hidden costs and efforts are there.
- Reconsidering conventions can often become a waste of time. New conventions can improve our code, but sometimes distributing knowledge is a hidden heavy cost.
- When making decisions regarding refactoring, it is necessary to use a coordinated approach, involving all the stakeholders, sharing ownership and documenting decisions with ADR.

From what I have written so far, it might seem that I am not a fan of refactoring, but I like it.

I think that refactoring should be estimated implicitly in the project plan and diluted in the work of everyday life, avoiding the “formal refactoring moment” approach done to justify the "not done" in everyday work.

Refactoring should be automatic and probably should not have a name because it is implicit in the act of writing code (giving it a name mentally tends to purge it from the act of programming).

Refactoring should start by accepting imperfection, like in the Wabi-sabi Japanese philosophy. That vision or aesthetic is based on accepting the transience and imperfection of things. That vision of "imperfect, impermanent, and incomplete beauty" is typical of the Buddhist world.

![kintsugi](/images/kintsugi.jpg)
https://www.deviantart.com/elorie-portrait/art/Kintsugi-cap-3-650928093

So when can see refactoring as an evolution of conscious repair actions, which make our code tell a coherent story written over time, step by step.

Romantically, I like to imagine the value of code memory.

**Restoring code not to a state of newness but also to a state that keeps the memory like done in Kintsugi, the art of repairing ceramics with gold.**

Calvino describes this feeling and idea better than I in the final part of Invisible Cities when he says:

> “The inferno of the living is not something that will be; if there is one, it is what is already here, the inferno where we live every day, that we form by being together. 
> There are two ways to escape suffering it. The first is easy for many: accept the inferno and become such a part of it that you can no longer see it. The second is risky and demands constant vigilance and apprehension: seek and learn to recognize who and what, in the midst of inferno, are not inferno, then make them endure, give them space.”

---

I let you some links if you wan't to read more about Italo Calvino or Sun Tzu

<div class="display: flex">
<iframe sandbox="allow-popups allow-scripts allow-modals allow-forms allow-same-origin" style="width:120px;height:240px;" marginwidth="1" marginheight="0" scrolling="no" frameborder="0" src="//rcm-eu.amazon-adsystem.com/e/cm?lt1=_blank&bc1=000000&IS2=1&bg1=FFFFFF&fc1=000000&lc1=0000FF&t=gitbarpodcast-21&language=it_IT&o=29&p=8&l=as4&m=amazon&f=ifr&ref=as_ss_li_til&asins=B08WP95DCS&linkId=34c8e5d532893aa71f818b89dfde23cf"></iframe> &nbsp;
<iframe sandbox="allow-popups allow-scripts allow-modals allow-forms allow-same-origin" style="width:120px;height:240px;" marginwidth="1" marginheight="0" scrolling="no" frameborder="0" src="//rcm-eu.amazon-adsystem.com/e/cm?lt1=_blank&bc1=000000&IS2=1&bg1=FFFFFF&fc1=000000&lc1=0000FF&t=gitbarpodcast-21&language=it_IT&o=29&p=8&l=as4&m=amazon&f=ifr&ref=as_ss_li_til&asins=0156453800&linkId=a3756d2aeef0cfb2dfce3606c6b8320d"></iframe>
</div>

I also recorded one pocast episode / talk about it, but it is in Italian. If you come from the Dante's land  you can enjoy it :D

https://www.gitbar.it/episodes/ep52-la-programmazione-e-il-refactoring-secondo-italo-calvino


