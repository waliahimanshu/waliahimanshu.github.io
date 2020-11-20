---
layout: post
title: "Pragmatic programmer summary"
comments: true
author: "waliahimanshu"
meta: "Pragmatic Programmer summary"
categories: Books
---

### Pragmatic Programmer - Notes

{% include category_include.html %}

### Chapter 1 - A Pragmatic Philosophy

Who are Pragmatic programers
Has attitude, a style,a philosophy of approaching problems and their solutions.
They think beyond the immediate problem, place it in  larger context and seeking out the bigger picture. 
They make intelligent compromises and informed decisions and most importantly take responsibility of everything they do.

### 1 . You have agency
Software development appear close to the top of any list of careers where
you have control. Our skills are in demand, our knowledge crosses geographic
boundaries, we can work remotely. Trick is to ask for anything you want from organization and always remember "you can change your organization or change your organization."
You’re investing in yourself, so doing it while you’re off-the-clock is only reasonable.

### 2. The Cat Ate My Source Code
Team trust - your team needs to be able to trust and rely on you, in a healty team environment you can speak up your mind.
Responsibility - when you accept the responsibility for an outcome, you should expect to be held accountable for it. When you make a mistake (as we all do ) try to offer solutions then blame.
**Provide Options, Don’t Make Lame Excuses**
Before you approach anyone to tell them why something can’t be done, is
late, or is broken, stop and listen to yourself. Talk to the rubber duck on your monitor, or the cat. Does your excuse sound reasonable, or stupid? How’s it going to sound to your boss?
Run through the *conversation in your mind*. What is the other person likely
to say? Sometimes, you just know what they are going to
say, so save them the trouble.

### 3. Software Entropy - means amount of disorder in any system. Software rot or tech debt.

*A broken window Analogy* 
One broken window, left unrepaired for any substantial length of time, instills
in the inhabitants of the building a sense of abandonment—So another window gets broken.
People start littering. Graffiti appears. Serious structural damage begins. In
a relatively short span of time, the building becomes damaged beyond the
owner’s desire to fix it, and the sense of abandonment becomes reality.

*Don’t Live with Broken Windows*
Don’t leave “broken windows’’ (bad designs, wrong decisions, or poor code)
unrepaired.  Comment, fix the broken window or comment to suggest the improvements and come back to it. But don't leave broken windows.

*A fire fighter analagy* : 
The house was immaculate, loaded with priceless antiques
The fire department rushed in to save burning house one day. But before they
dragged their big, dirty hoses into the house, they stopped—with the fire
raging—to roll out a mat between the front door and the source of the fire.
They didn’t want to mess up the carpet.
Now that sounds pretty extreme. Surely the fire department’s first priority is
to put out the fire. But they clearly had assessed
the situation, were confident of their ability to manage the fire, and were
careful not to inflict unnecessary damage to the property. That’s the way it
must be with software: don’t cause collateral damage just because there’s a
crisis of some sort.

If you find yourself working on a project with quite a few broken windows, it’s all too easy to slip into the mindset of “All the rest of this code is crap. By the same token, if you find yourself on a project where the code is
pristinely beautiful—cleanly written, well designed, and elegant—you will
likely take extra special care not to mess it up, just like the firefighters. Even if there’s a fire raging (deadline, release date, trade show demo, etc.),you don’t want to be the first one to make a mess and inflict additional damage.

### 4. Stone soup and boiled frog
*Be a Catalyst for Change*

You may be in a situation where you know exactly what needs doing and how
to do it. The entire system just appears before your eyes—you know it’s right.
But ask permission to tackle the whole thing and you’ll be met with delays
and blank stares. People will form committees, budgets will need approval,
and things will get complicated. Everyone will guard their own resources.
Sometimes this is called “start-up fatigue.’
It’s time to bring out the stones. Work out what you can reasonably ask for.
Develop it well. Once you’ve got it, show people, and let them marvel. Then
say “of course, it would be better if we added…’’ Pretend it’s not important.
Sit back and wait for them to start asking you to add the functionality you
originally wanted. People find it easier to join an ongoing success.

### 5. Good-Enough Software
Bug-free software is a myth.
Time, technology, and temperament all conspire against us.
Make good enough for your users, for future maintainers, for your own peace of mind. You’ll find that you are more productive and your users are happier.
Involve Your Users in the Trade-Off

Make Quality a Requirements Issue - As a user,
would you rather (1) wait for them to get all the bugs out, (2) have complex
software and accept some bugs, or (3) opt for simpler software with fewer
defects?


### 6. Your Knowledge Portfolio
- Invest Regularly in Your Knowledge Portfolio

The early bird might get the worm, but what happens to the early worm?
Your knowledge and
experience are your most important day-to-day professional assets.
Unfortunately, they’re expiring assets.7 Your knowledge becomes out of date
as new techniques, languages, and environments are developed

1. Serious investors invest regularly—as a habit.
2. Diversification is the key to long-term success. (different domains, disciplines )
3. Smart investors balance their portfolios between conservative and highrisk,
high-reward investments. (new languages framework )
4. Investors try to buy low and sell high for maximum return.
5. Portfolios should be reviewed and rebalanced periodically.

** This can be learned. The trick is to make yourself do it initially and
form a habit. Develop a routine which you follow until your brain internalizes
it. At that point, you’ll find yourself sucking up new knowledge automatically **

When learning Critically Analyze What You Read and Hear
trick: ask “why?” at least five times. Ask a question,
and get an answer. Dig deeper by asking “why?”


### 7. Communicate!

Having the best ideas, the finest code, or the most
pragmatic thinking is ultimately sterile unless you can communicate with
other people. A good idea is an orphan without effective communication
**A large part of our day is spent communicating, so we need to do it well**

Continuously improve your knowledge of your audience as you communicate.Plan what you want to say. Write an outline. Then ask yourself, “Does this
communicate what I want to express to my audience in a way that works.

Make your style of communication and for make it look good (Your company may already have defined style sheets that you can use.).
Communicate well and listen well, when you don't know Get back to people.

When writing that Pull request description or a slack message or email.
Proofread, check for spelling mistakes. omit un-necessary words. Make is clear and short. User code snippets to explain where necessary 

### Chapter 2 - A Pragmatic Approach

### 8. The Essence of Good Design
Good design is easier to change .ETC.every design principle out there is a special case of ETC.
Decoupling? Because by isolating concerns we make each easier to change. ETC.
Single responsibility ? Because a change in requirements should not affect other un-related modules. ETC.
Why is naming important? Because good names make code easier to read,
and you have to read it to change it. ETC!

How to train yourself for ETC. It requires some initial conscious reinforcement. Spend a week or so deliberately
asking yourself “did the thing I just did make the overall system easier
or harder to change?” It’s really just thinking about keeping code
decoupled and cohesive.

### 9. DRY (Don't repeat yourself) - The Evils of Duplication
Code is ever changing, requirements change , client change, industry and government regulations change.

Most people assume that maintenance begins when an application is released,
that maintenance means fixing bugs and enhancing features. This is wrong. Programmers are constantly in maintenance mode. Our
understanding changes day by day. New requirements arrive and existing
requirements evolve as we’re heads-down on the project. Perhaps the environment changes. Whatever the reason, maintenance is not a discrete activity, but a routine part of the entire development process.

.....

### 10. Orthogonality


### 11. Reversibility
Requirements,users, and hardware change faster than we can get the software developed
Most of the time, calls to third-party products are entangled throughout the code. But we really abstracted the idea of a database out—to the point where it simply provides persistence as a service—then you have the flexibility to change horses in midstream

*Flexible Architecture* -> What you can do is make it easy to change. Hide third-party APIs behind your own abstraction layers. Break your code into components: even if you end up deploying them on a single massive server, this approach is a lot easier than taking a monolithic application and splitting it.

But think of code evolution along the same lines as a box full of
Schrödinger’s cats: every decision results in a different version of the
future. 
How many possible futures can your code support? Which ones
are more likely? 
How hard will it be to support them when the time comes?
Dare you open the box?

### 12. Tracer Bullets
Particularly when you’re building something that hasn’t been built before. We use the term tracer bullet development to visually illustrate the need for immediate feedback under actual conditions with a moving goal

Tracer bullets work because they operate in the same environment and under
the same constraints as the real bullets. They get to the target fast, so the
gunner gets immediate feedback. They’re a relatively cheap solution.

Tracer code is not disposable: you write it for keeps. It contains all the error
checking, structuring, documentation, and self-checking that any piece of
production code has. It simply is not fully functional. However, once you have
achieved an end-to-end connection among the components of your system,
you can check how close to the target you are, adjusting if necessary. Once
you’re on target, adding functionality is easy.
Tracer development is consistent with the idea that a project is never finished: there will always be changes required and functions to add. It is an incremental approach.
The tracer code approach has many advantages

1. Users get to see something working early
2. Developers build a structure to work in
3. You have an integration platform
4. You have something to demonstrate
5. You have a better feel for progress

#### Tracer Code versus Prototyping
Prototyping generates disposable code. Tracer code is lean but complete, and forms part of the skeleton of the final system. Think of prototyping as the reconnaissance and intelligence gathering that takes place before a single tracer bullet is fired.

### 13. Prototypes and Post-it Notes
We tend to think of prototypes as code-based, but they don’t always have to
be. Like the car makers, we can build prototypes out of different materials.
Post-it notes are great for prototyping dynamic things such as workflow and
application logic.

But if you find yourself in an environment where you cannot give up the
details, then you need to ask yourself if you are really building a prototype
at all. Perhaps a tracer bullet style of development would be more appropriate
in this case

Anything you aren’t comfortable with. You can prototype:
• Architecture
• New functionality in an existing system
• Structure or contents of external data
• Third-party tools or components
• Performance issues
• User interface design

Prototyping is a learning experience. Its value lies not in the code produced,
but in the lessons learned. That’s really the point of prototyping.

*How to Use Prototypes*
When building a prototype, what details can you ignore?
1. Correctness - fake data
2. Robustness - Edge/error cases not covered
3. Style - may skip the guidelines, process etc

Prototypes gloss over details, and focus in on specific aspects of the system being considere.

#### How Not to Use Prototypes
Code-based prototyping, make sure that everyone understands that you are writing disposable code.
Prototypes can be deceptively attractive to people who don’t know that they are just prototypes. You
must make it very clear that this code is disposable, incomplete, and unable to be completed.

### 14. Domain Language
So when you force a business person to sign off on a requirements document, or get
them to agree to a set of Cucumber features, you’re doing the equivalent of getting
them to check the spelling in an essay written in Sumerian. They’ll make some random
changes to save face and sign it off to get you out of their office.
Give them code that runs, however, and they can play with it. That’s where their real
needs will surface.

Document using Test Rspec, cucumber, ansible or YAML.


### 15. Estimating

To some extent, all answers are estimates. It’s just that some are more
accurate than others. So the first question you have to ask yourself when
someone asks you for an estimate is the context in which your answer will
be taken. Do they need high accuracy, or are they looking for a ballpark figure?

1. Understand What’s Being Asked
2. Break the Model into Components
3. Give Each Parameter a Value
4. Keep Track of Your Estimating Prowess
5. Check requirements
6. Analyze risk (and prioritize riskiest items earlier)
7. Design, implement, integrate
8. Validate with the users

Based on that experience, you can refine your initial guess on the number of iterations and what can be included in
each.T he refinement gets better and better each time, and confidence in the
schedule grows along with it. This kind of estimating is often done during the
team’s review at the end of each iterative cycle.

This may not be popular with management, who typically want a single, hardand- fast number before the project even starts. You’ll have to help them understand that the team, their productivity, and the environment will determine the schedule. By formalizing this, and refining the schedule as part of each iteration, you’ll be giving them the most accurate scheduling
estimates you can.

#### What to Say When Asked for an Estimate
You say “I’ll get back to you.”
You almost always get better results if you slow the process down and spend some time going through the steps we describe in this section.

