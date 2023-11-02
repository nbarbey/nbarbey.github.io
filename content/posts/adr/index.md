---
title: "A note about Architecture Decision Records"
date: 2023-08-30T10:00:00+00:00
tags: ["architecture", "documentation", "group-thinking"]
author: "Nicolas Barbey"
showToc: true
TocOpen: false
draft: yes
comments: false
#description: "Some hints about how to use ADR"
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
    image: "Parental_Advisory_label_Boring.jpg"
    alt: "<alt text>" # alt text
    caption: "Parents, beware of boredom for your children ! It may have adverse physical and mental effects" # display caption undercover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/nbarbey/nbarbey.github.io/blob/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

## Boring !

Come on ! I hear you yawning already, just by reading the title !
Let's face it, talking about documentation and architecture decisions really is boring !
Actually, if people only knew this subject existed, it would probably be listed first in
the top ten most boring topics of conversation (gladly, nobody is aware of its existence).

But why ? Why is it so boring ? And what could we do about it ?

### What is boredom ?

But first we should probably try to define boredom.
This in itself can be pretty boring. What is more boring than documentation ?
Insisting on definitions of course !

Wikipedia goes like this :

> In conventional usage, boredom, ennui, or tedium is an emotional and 
> occasionally psychological state experienced when an individual is left
> without anything in particular to do, is listless and dissatisfied due to a
> lack of occupation or excitement, is not interested in their surroundings, or
> feels that a day or period is dull or tedious.

But follows like this :

> There is no universally accepted definition of boredom.

Ah ! Now that is interesting ! It seems that people cannot agree on what boredom
is exactly.


### Why documentation is so boring ?

How many times have I seen people suddenly realising: "we should write documentation !".
This is good practice after all. This is part of software quality to have a documentation.
This is like tests, we should have some.
All those arguments rely mostly on a call to authority with no clearly defined purpose.

There is often times not even an explicit audience for the documentation. It is not so
clear if the documentation is meant for other developers of the software, for administrators
of the software, or for end-users. And without this clarity of audience, there is no way
to connect to the human being at the other side of the documentation. The person we should
be thinking about. The one we are supposed to help. So much that it seems that we may feel
that the task is not helping anyone.

And finally, this is a never ending task. As the software evolve, we have to remind ourselves
at each change in the behavior of the code that we need to also report this change in the
documentation. I see two ways to end such a situation. Either the team writing the software
is very dedicated to documenting and end-up slowing up all development to maintain the documentation.
Adding, to a probably already big cognitive load. Or the team finally give up on maintaining
the documentation consciously or not. Making the documentation not trustworthy anymore.
Let us add that it could affect the morale of the people writing the software for the worse.


### Why architecture is so boring ?

I think I can also see why people can find software architecture to be boring.
After all, architects are people making random decisions on their own in their ivory
tower. They are producing tons of this already boring documents full of those decisions.
And those decisions could very well threaten the hard work already done by the good people
writing the software. Or else, add loads of extra work with no other purpose than conforming
to the norms and requirements fixed by them.

Also, architecture is no fun because it has such a big feedback loop ! It is about making
decisions that are hard to change. So, with no doubt, seeing the result of it will take time.
Months, if not years. There is no fun in doing something when you don't see the result of it
immediately.

Finally, architecture is a difficult endeavour. It often concerns decisions that are not so
well-defined. It requires a lot of expertise and knowledge of the people, practices and technologies
involves. And let's face it. Difficulty is no fun. Difficulty is boring.


## How to make ADR not boring ?

connect to purpose
connect to urgency
connect to people

[Bored]: https://www.scientificamerican.com/article/bored-find-something-to-live-for/ (Bored ? By Anna Gosline on December 1, 2007)