# Proposal for Domain Centric Software
### By: Cory Gwin

## Overview

Technology is simply a tool for solving a problem. Arguably the most valuable tool any developer has in their tool chest is the ability to understand, communicate about, break down a problem and ultimately provide a proven solution. Most organization find this incredibly difficult to do and often organization focus on how fast they can ship instead of how well their solutions solve a problem. As software developers our problem-solving tools get nowhere near the attention that our text editor skills, language of choice or deployment skills get. Instead, we hand it off to other parts of the organization and later complain about them throwing requirements over the wall. The time has come to break down the wall and become closer to the problems we are solving.

The agile manifesto states we should prefer customer collaboration over contract negotiation. Most developers live in a process I will call task board shuffle leaving implementation to be done in a knowledge vacuum. This leads to a number of problems:

- Downstream communication issues.
- Misunderstood requirements.
- Incorrect implementations.
- Developer frustration.
- Scope change or creep. 
- Lost context over time.
- Code that does not properly convey the domain.
- Poorly modeled data.
- Mis-prioritization.

Our workflows and structures create communication barriers we must break down in order to move our implementations closer to their domains. As developers, our goals should include moving ourselves and our code closer to the domain. This requires understanding not only the problem being solved by a feature but also, more broadly an understanding of the field we are working in.

We seek to develop a toolset for gathering insight into the domain that can help engineers understand a user's problem leading to:

- A better understanding of the entire domain.
- A path toward a domain language.
- Bounded Contexts.
- Understanding problem nuance.
- Capturing valuable insight from domain experts.
- Clear task prioritization.
- Identifying focused solutions.
- Foresight into how an implementation may evolve.

Following the path of a team replacing a legacy application with a new application, this book will explore tools from Design Thinking, Domain Driven Design, and Agile introducing methods that can be utilized to break down a domain and better communicate with domain experts. 

After reading this book developers will feel equipped to:

- Interview domain experts.
- Capture domain knowledge and translate it into domain centered language in a software application.
- Better understand the problem space they are developing a solution for.
- Learn how to clearly communicate with domain experts about their business problems.
- Evaluate potential software solutions and implementation choices without bias.
- Engage domain experts earlier in implementation for feedback, in order to avoid mistakes as soon as possible.
- More cleanly represent the domain in code and data stores.
- Run blameless retrospectives.
- Engage methods to learn from outages and identify solutions.


## What this book will cover:

- Introduce the concept of design thinking.
- Introduce the following design thinking methodologies from the perspective of the developer:
    - Stakeholder mapping.
    - Interviewing.
    - Job Shadowing.
    - Rose Bud Thorn.
    - Affinity Mapping.
    - Experience diagramming.
    - Importance/Difficulty matrix.
    - Feature Voting.
    - Creative matrixes.
    - Technical prototyping.
    - Storyboarding UI's
    - Stakeholder validation.
    - More??
- Introduce domain driven design concepts:
    - Ubiquitous language.
    - Context bounding.
    - Domain events.
- Outline effective tools for using design thinking to create ubiquitous language, bounded contexts and domain events.
- Outline rules for effective design thinking on agile teams.
- Discuss ideas for bringing these methods into teams that are not familiar with design thinking.
- Processes for rapid prototyping.
- Tools and processes for beta testing features.

## Audience:
This book is targeted at developers and architects seeking ways to work more closely with domain experts in order to understand complex problems and craft informed domain centric implementations.

## Why is your book different?

This book will offer a number of methods from design thinking, agile and domain driven design aimed at bridging the gap between domain knowledge and implementation. This marriage of skills will be separated from heavy handed implementation details and instead focus on methods for interacting with domain experts to extract information useful in crafting domain centric software and more creative solutions. Skills emphasized include:

Design Thinking:

- Communicating effectively with stakeholders.
- Identifying when to utilize design thinking methods and when not to.
- The discovery, ideate, prototype phases of design thinking.
- Individual design thinking methodologies and when to use them in the software development lifecycle. 
- Methods for prototyping.
- Hack weeks.

Agile:

- How to run better retros.
- Methods to prioritize tasks during sprints.
- How to evaluate what to build given competing priorities.
- Time boxing.
- Encouraging design spikes with guide rails.
- Fitting research into your sprints.
- Team switching for knowledge transfer.


Domain Driven Design:

- Capturing business details from domain experts in a way that transfers to software details.
- Identifying domain entities, domain events, context boundaries, and a ubiquitous language.
- Translating domain knowledge to code via testing, method naming and object naming.
- Understanding bounded contexts in software.
- Building long-lived communication tools that impact internal/external communication and code design.

## Competing Books
- [Domain Driven Design Distilled](https://www.amazon.com/Domain-Driven-Design-Distilled-Vaughn-Vernon/dp/0134434420/ref=sr_1_fkmrnull_1?crid=33UZDG9LM3BY0&keywords=domain+driven+design+distilled&qid=1550802381&s=gateway&sprefix=Domain+Driven+Design+D%2Caps%2C303&sr=8-1-fkmrnull)
- [Design It! From Programmer to Software Architect](https://www.amazon.com/Design-Programmer-Architect-Pragmatic-Programmers/dp/1680502093/ref=sr_1_1?keywords=Design+It%21&qid=1550802621&s=books&sr=1-1)
- [Lean Customer Development](https://www.amazon.com/Lean-Customer-Development-Hardcover-version/dp/1449356354/ref=sr_1_1?keywords=lean+cindy+a&qid=1550802543&s=gateway&sr=8-1)


## Why we should get excited about your topic:

In the Cathedral and the Bazaar a number of important ideas were set forth related to working more closely with our stakeholder:

1. Treating your users as co-developers is your least-hassle route to rapid code improvement and effective debugging.
1. Release early. Release often. And listen to your customers.
1. Given a large enough beta-tester and co-developer base, almost every problem will be characterized quickly and the fix obvious to someone.
1. If you treat your beta-testers as if they're your most valuable resource, they will respond by becoming your most valuable resource.
1. The next best thing to having good ideas is recognizing good ideas from your users. 
1. Often, the most striking and innovative solutions come from realizing that your concept of the problem was wrong.
1. Perfection (in design) is achieved not when there is nothing more to add, but rather when there is nothing more to take away. (Attributed to Antoine de Saint-Exupéry)
1. To solve an interesting problem, start by finding a problem that is interesting to you.
1. Provided the development coordinator has a communications medium at least as good as the Internet and knows how to lead without coercion, many heads are inevitably better than one.

Interestingly the book contradicts itself pointing out a major issue with the way we develop software:

> Every good work of software starts by scratching a developer's personal itch.

The implication here is that we do not know how to collaborate with our users in the same way as when we develop to solve our own problems. 

Domain Centric Software makes a case that in order to solve problems we need to move the solution architects closer to the domain space. I believe in order to replicate the success of the open source movement in a broader way, we need to find ways to bring domain experts together with solution architects to create a new way of interacting. If one is to believe "We are as gods and might as well get good at it" then we need to focus on creating tools for others in a manner we ourselves would accept.

I intend to present a set of tools to help developers take action on this premise, equipping developers to discuss complex problems with their domain experts in new and collaborative ways.

 