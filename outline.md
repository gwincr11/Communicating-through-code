## Motivation:
The act of programming is the translation of human problem to computer solution. This middle part of this process is where the art, science and communication skills lie.

Over the years we have developed deep levels of abstractions to remove boiler plate code and noise that distract us from our goals. The open source movement has allowed for massive adoption of common solutions to common problems. This combination allows developers to move fast and focus more on domain problems. 

As our software development tools have progressed much discussion has occured about how we face programming problems. But linger in plain sight exists an entire spectrum of problems with the way we communicate. 

## Problem Description
Our code exists to solve human problems in well understood domains. As we program solution to problems ideally we learn the domain we are working in well enough to communicate about it as experts. 

Our responsibility ultimately is to understand a human problem in a domain so well that we can translate the problem and solution into a intermediate language understood by humans and computers. 

This is the hardest problem in computer programming, some times thought of as naming things. But I wish to expand upon that idea and claim that it is not just naming things but instead developing a programming language abstraction for our domain, a domain model or a domain specific language (DSL) if you will.

It is interesting to look at the difference between the definition of these two terms.

In many ways they seem to capture a similar idea but one carries around the baggage of language compilation or fancy programming tricks. This often leads to a misconception about the level of implementation needed to consider our implementation at this depth.

It feels vital that in order to better communicate through our code the idea of domain models become a stronger concept given the flexibility this much more generic concept carries. The introduction of the term language seems to make everything more computer sciency than is neccessary to improve our communication.

Regardless of how you think about implementation getting to the implementation is something we struggle to do. I have engaged in very few conversations with other developers about the language we are developing and the flow of the nouns, verbs, attributes et all languge we are introducing and how it capture the domain.

But were does this problem lie? It feels slippery and abstract from our actual jobs. Should I not be learning the hundreth hot new concept introduced by browser manufacturers this month to become a better software developer? How would I even start learning about my stakeholders domain?

### Understanding the domain
At the highest level we have our understanding of our domain, that maybe programming lifecycles, banking, warranty proccesses, or some other human problem. This is often a after thought when we look for programmers, but the ability to understand the domain you are working in will help programmers conceptualize solutions that are more flexible and empathetic to the users.

- The idea or problem being explored
- The shared domain language
- The company/context specific domain language
- The contextual opinions about how to approach the domain

### Grappling with the language of the domain
Every proffession has its own set of vocabulary that is specific to its domain, this is sometime even specific to a very granular level, company, dept etc... Understanding the language of the domain is vital in understanding what is being asked of the solution being implemented. Capturing these concepts not just at the time of implementation but also for feature additions and refactors is critical to a well understood codebase.

Currently the output of our processes as we work through the language of the domain is not captured in any long lived format, it is scattered around the codebase, issues, requirements and other communications. But rarely if ever have I come across anything that resembles dictionary of terms at a company or in a program. This situation can often cause problems in future communications. 

One example that immediately comes to mind is the concept of a User, this has become an overloaded term in most codebases and can mean many things. We use this term so broadly that we capture requirements with stories that say things like as a user I wish to delete all the things. But what is a user in any context? I can think of lots of users in the app I work on.

- Vocabulary used by the industy/domain.
- Vocabulary used by the end user.
- Vocabulary used by the PM/Designer etc.
- Vocabulary captured in the code.
- Vocabulary used in a refactor.

### Understanding Individual perspective

Every person you discuss a project with brings their own perspectives, vocabulary and experiences to the table. The more people you talk to the more complete your picture of the problem becomes. You will discover similarities and differences that will help you determine the most appropriate solutions.

A good example of this is a sale moving from sales to fullfilment in any sort of sales system. Often times sales people will talk about sales as sales even when they are not yet closed deals. However if you talk to the fullfilment department they will not consider something a sale until it has an order attached and payment is recieved. This sort of language difference can be confusing when you look at how code is implemented and discussed vs when you discuss features with these different people. Understanding their is a process to sales and different language in different departments is vital in building a solution that assist this sort of process, but how often do we need to re-educate ourselves on this difference and is it getting captured in code in a way that is purveying this sort of nuance or is it showing up as a state machine with no explanation?

- Where are they coming from
- What problem are they facing
- What hacks are they using today
- Language barriers
- Context Context Context

### Context loss through the processes
Each step of the process involves people, their understanding of that problem an attempt to capture it in language and then the re-conceptualizing of that conceptualization in the next person/medium. Like the game telephone but translating the idea into different languages. 
 - Context loss in the requirements process
 - Context loss in the developers understanding
 - Context loss in the code
 - Context loss in refactoring

### Symptoms/Outcomes
- Developers and users talking past each other by using the same vocabulary that has different meanings.
- Developing solutions that don't solve the users issue
- Products losing site of the initial goal/solution over time
- Objects, functions or other programming concepts that do not clearly map to the domain
- Lots of comments in the codebase
- Test suites that do not explain the problem
- Code reviews that focus more on the code and less on the implementations ability to solve the problem.



## Story of my trial and error

## Some solutions

### Defining the problem

### Understanding the domain

### Mapping the key vocabulary/concepts

### `