---
title: "Seriously, you should be having fun writing software at work!"
date: 2023-07-18T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["learning", "neuro-science", "methods", "mob-programming", "TDD"]
author: "Nicolas Barbey"
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "(People working in other industries should probably not be miserable at work either, but that is not the concern of this article.)"
canonicalURL: "https://canonical.url/to/page"
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/nbarbey/nbarbey.github.io/blob/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

I recall how, when I was a junior developer, I often felt happy and reassured when I was writing software. It felt like a safe place compared to the overwhelming complexities of the world. The simple, deterministic functions, mechanical in their way of working, offered comfort. If you inject an input, it always gives the same output. It’s controllable, manageable, uncomplicated!

But when I started doing it at a much more professional level I found myself in situations that contradicted these feelings. I seemed to be regularly misinterpreting the requirements of the software I had to write. I repeatedly had bugs in pieces of code that had seemed easy. I would stare for days at code bases I could not make sense of, no matter how hard I tried.

In fact, I was of course slowly learning that software, being part of the world and needing to interact with it, contains all those complexities and subtleties I had been trying to avoid. And in the process, I was also slowly realizing that that is precisely the beauty of it.

## It’s all about learning

And so, to interact with this complex world, you need to be constantly learning. You need to learn what product to build. You need to learn how to build software, the programming languages, frameworks, tools, software practices, and architecture. You need to learn to be able to collaborate with other developers, so that you move forward in the same direction, building pieces of software that go well together. You need to learn what other companies are doing so that you do not end up attempting to reinvent the wheel, but rather leveraging things that already exist in the wild that can be useful to you. You may need to learn about learning too — maybe one of the most underrated abilities.

At this point you may be reminded of the long hours you spent sitting in a classroom at school, wondering if this is really what you should be doing for the rest of your life as a software developer. Or maybe you are considering asking your manager if you could attend a professional training session. Before you proceed, you should know that, although those ways of working have their place, they are not the only ones. And research has given us some insight into other ways of learning that could be more efficient. Would you like to hear more about a few of them? (Please don’t direct your answer to your screen, this is a rhetorical question.)

## Learning the fun way

Although many people share the view that learning is not all that fun, there is now a large body of research that shows that having fun is an important way of improving the efficiency of learning.

Actually, learning through fun is based on centuries-old wisdom and people often cite younger children as the best examples. No coincidence then that Lego games have a motto like “learning through play” stamped on their boxes. Children spend entire days playing around with anything they can get their hands on, free to explore and experiment. And, indeed, they learn really fast!

The study Teaching and Learning with Humor: Experiment and Replication by Avner Ziv proves that teaching with humor improves student scores. So I will ignore all opportunities for finesse and nuance in this article and assume that my tendency to inflict dad jokes on everyone around me is scientifically grounded.

An interesting development in the field of pedagogy is the use of neuroscience to investigate the physiological effects of different ways of learning. Studies along these lines tend to prove that having positive emotions does indeed improve the learning mechanisms. For instance, in her article “The Neuroscience of Joyful Education”, Judy Willis demonstrates the importance of novelty to activate the reticular system, and how having pleasant emotions while learning augments the level of dopamine in the brain.

## What motivates us

When thinking about this, the word “gamification” may come to mind. Indeed, the term describes practices that try to inject serious activities with fun components.

For instance, we could consider giving badges or awards to people closing the highest number of tickets in your favorite ticketing system. Sounds fun, right? RIGHT?

This line of thinking poses serious problems, though. These kinds of incentives fall into what we call extrinsic motivators. This has the drawback of decreasing the intrinsic value of the work being gamified as it assumes that the work is not considered interesting on its own. This is best explained in the book Drive: The Surprising Truth About What Motivates Us by Daniel H. Pink, which summarizes decades of research into what motivates people. The author favors what he calls intrinsic motivation, which is to say, finding value in the practice of the work in itself.

Often, when talking about fun at work, people come up with this one idea: “Let’s do some team building!” Polls then ensue, asking team members if they would prefer going on a beer-brewing course, visiting Paris by boat, or whatever. But those activities can even be detrimental to the team spirit. I recall a karting session that ended up with one employee being injured by another who was a bit too keen to win the race…

This is not to say that team building is necessarily a bad thing. But it requires a lot more time and effort than people are usually ready to commit to, as well as directing things toward collaboration rather than competition. With time this can inspire trust between colleagues and encourage them to help each other. It can translate into intrinsic motivation to care for one another.

## Writing software can be fun!

So how can we apply this to software programming?

### Enhance developer experience

First, we could start by ensuring the job doesn’t become painful. Let’s remove all the repetitive, tedious, menial tasks that can be got rid of. This means automating as much as possible. Investing in helpful tools, writing macros for code we often reuse. Using IDE shortcuts. Using tools with wonderful, convenient interfaces (developer experience, anyone?). But also, maybe, doing away with those not-so-useful meetings and gatherings.

Another aspect of the developer experience is the usage of code produced by other teams. Is it well documented or self-explanatory? Can we use it without needing any help? How well is the API designed? Is it coherent? Is it minimal yet powerful? We should probably always be striving to provide this kind of software and setting an example so that others provide great API too. The goal is that we all have a pleasant experience while using other people’s software.

### Fun-driven development

To be fair to the gamification community, it did acknowledge the need for intrinsic motivation and developed techniques to make use of it. For an example of this, take a look at the article “Top 4 Gamification Techniques with Dr Zac” by Dr Zac Fitz-Walter, which states that there are 4 characteristics that make a game: Goals, rules, challenge/conflict, and feedback. Interestingly, we can find these characteristics in the software-development practice of test-driven development (TDD). With TDD, you start by writing a test that defines a short-term goal of the coding session. You have to follow the rules of coding’s best practices to meet the challenge of implementing a function that passes the test. And you get instant feedback by executing the test against your implementation.

This is nice and all, but we know that playing solitaire is not the same as playing poker. Half-Life was good, but Counter-Strike was played so much more. Indeed, involving other people makes the game all the more fun, as it challenges the complexities of the mind.

### Role-playing games

So, can this be done with coding? You bet! It’s called mob programming, or ensemble programming, and has been an emerging practice in developer communities for almost a decade now. Combined with TDD it makes the game of coding all the more fun by introducing other humans to the game. Indeed, ensembles often structure themselves with rules that resemble those of a game to keep people engaged, such as switching the keyboard every five minutes. Some people have gone as far as creating different roles for people in their group using what is known as mob programming role-playing games (RPG). And indeed mob programming can easily be compared to role-playing games: If we can describe a role-playing game as the co-creation of a story inside a set of rules, then mob programming is the co-creation of software inside a set of rules.

This is not the only way that mob programming is embedded with patterns akin to gamification. In a mob programming RPG, as well as in pair programming, there are two important roles: Driver and navigator. The driver is the one holding the keyboard, implementing what the navigator instructs them to do. This is similar to the game master and player in a classic RPG. A good navigator will know the driver they are working with and will adapt the level of their instruction to the level of the driver. This is very similar to how it is important in games to adjust the difficulty of the challenges to the level of the player. It allows the player to avoid both boredom and frustration/failure.
## Are you up for a game?

I know that, from an outside perspective, it probably seems that these practices are not all that amusing, and inevitably they will not amuse everybody, but you should try them and see for yourself. I have actually introduced a fair number of people to mob programming and had them instantly telling me that it does feel like a kind of game. So who knows — maybe this game is for you!