# Proposal for Design Think for Developers
### By: Cory Gwin

## Overview
Technology is simply a tool for solving a problem. Arguably the most valuable tool any developer has in their tool chest is the ability to understand, communicate about, break down a problem and provide a proven solution. Most organization find this incredibly difficult to do and often organization focus on how fast they can ship instead of how well their solutions are received. Oddly, as terrible as we are at this part of our jobs, our problem-solving tools get nowhere near the attention as our text editor skills, the scripting language of choice or deployment skills and other tools in our development war chest. Instead, we hand it off to other parts of the organization and later complain about them throwing requirements over the wall without asking if we should break down the wall.

It is time to break down these artificial boundaries and take responsibility for the solutions we build. The agile manifesto states we should prefer customer collaboration over contract negotiation. As developers we often leave the customer collaboration to others in our organization, leaving only short user stories or issues to gather context. This leads to a number of problems including:

- Downstream communication issues.
- Misunderstood requirements.
- Incorrect implementations.
- Developer frustration.
- Scope change or creep. 
- Lost context over time.
- Code that does not properly convey intent.
- Unintended consequences of poorly modeled data.
- Incorrect prioritization.

Our workflows and structures create communication barriers we must break down in order to move our implementations closer to their domains. As developers, our goals should include moving ourselves and our code closer to the domain. This requires understanding not only the problem being solved by a feature but also, more broadly an understanding of the field we are working in.

Design thinking offers a toolset for gathering insight into the domain that can help engineers understand a user's problem more fundamentally and offer a number of useful byproducts such as:

- Providing a better understanding of the entire domain.
- A clearer path to a domain language.
- Understanding problem nuance.
- Gaining lessons learned of the user.
- Clear prioritization of tasks.
- Identifying focused solutions.
- Providing insight into how an implementation may evolve.

Following the path of a team replacing a legacy application with a new application, this book will explore tools that can be utilized to break down a domain and better communicate with domain experts. The book will introduce a number of design thinking exercises and explain how they can be applied in different scenarios to help agile developers craft clearer implementations.

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

## Audience:
This book is suitable for developers, managers, product manager, project managers, designers and anyone looking for methods to bring implementation closer to a domain.

## Why is your book different?

This book will offer a design thinking tools set aimed at software development, with a minor focus on domain driven design. It will introduce software developers to all the phases of design thinking and teach them skills to help solve problems in more creative ways, skills emphasized include:

- Communicating effectively with stakeholders.
- Identifying when to utilize design thinking methods and when not to.
- The discovery, ideate, prototype phases of design thinking.
- Individual design thinking methodologies and when to use them in the software development lifecycle. 
- How to run better retros.
- How to evaluate what to build given competing priorities.
- Understanding the business domain they work in the day-to-day.
- Building long-lived communication tools that impact internal/external communication and code design.


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

Interestingly it contradicts itself pointing out a major issue with the way we develop software:

> Every good work of software starts by scratching a developer's personal itch.

The implication here is that we do not know how to collaborate with our users in the same way as when we develop to solve our own problems. 

This book makes a case that in order to solve problems we need to move the solution architects closer to the domain space. I believe in order to replicate the success of the open source movement in a broader way, we need to find ways to bring domain experts together with solution architects to create a new way of interacting. If one is to believe "We are as gods and might as well get good at it" then we need to focus on creating tools for others in a manner we ourselves would accept.

It then sets forward a set of tools to help developers take action on this premise equipping them to discuss complex problems with their user base in new and collaborative ways.

 