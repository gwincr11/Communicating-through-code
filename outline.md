## Motivation:
The act of programming is the translation of human problem to computer solution. There is a middle part of this process where the art, science and communication skills lie.

Over the years we have developed deep levels of abstractions to remove boiler plate code and noise that distract us from our goals. The open source movement has allowed for massive adoption of common solutions to common problems. This combination allows developers to move fast and focus more on domain problems. 

As our software development tools have progressed much discussion has occured about how we face programming problems. But linger in plain sight exists an entire spectrum of problems with the way we communicate. 

## Problem Description
Our code exists to solve human problems in well understood domains. As we program solutions to problems ideally we learn the domain we are working in well enough to communicate about it as experts. 

Our responsibility ultimately is to understand a human problem in a domain so well that we can translate the problem and solution into a intermediate language understood by humans and computers. 

This is the hardest problem in computer programming, some times thought of as naming things. This feels like a shallow definition of a much bigger problem in my opinion. I wish to expand upon that idea and claim that it is not just naming things but instead developing a programming language abstraction for our domain, a domain model or a domain specific language (DSL) if you will.

It is interesting to look at the difference between the definition of these two terms.

Domain Model
> A domain model is a system of abstractions that describes selected aspects of a sphere of knowledge, influence or activity (a domain[3]). The model can then be used to solve problems related to that domain. The domain model is a representation of meaningful real-world concepts pertinent to the domain that need to be modelled in software. The concepts include the data involved in the business and rules the business uses in relation to that data.
> A domain model generally uses the vocabulary of the domain, thus allowing a representation of the model to be communicated to non-technical stakeholders. It should not refer to any technical implementations such as databases or software components that are being designed.
> https://en.wikipedia.org/wiki/Domain_model

Domain Specific Language
>A domain-specific language (DSL) is a computer language specialized to a particular application domain. This is in contrast to a general-purpose language (GPL), which is broadly applicable across domains. There are a wide variety of DSLs, ranging from widely used languages for common domains, such as HTML for web pages, down to languages used by only one or a few pieces of software, such as MUSH softcode. DSLs can be further subdivided by the kind of language, and include domain-specific markup languages, domain-specific modeling languages (more generally, specification languages), and domain-specific programming languages. Special-purpose computer languages have always existed in the computer age, but the term "domain-specific language" has become more popular due to the rise of domain-specific modeling. Simpler DSLs, particularly ones used by a single application, are sometimes informally called mini-languages.
>https://en.wikipedia.org/wiki/Domain-specific_language


In many ways they seem to capture a similar idea but one carries around the baggage of language compilation or fancy programming tricks. This often leads to a misconception about the level of implementation needed to consider our implementation at this depth.

It feels vital that in order to better communicate through our code the idea of domain models become a stronger concept given the flexibility this much more generic concept carries. The introduction of the term language seems to make everything more computer sciency than is neccessary to improve our communication.

Regardless of how you think about implementation getting to the implementation is something we struggle to do. I have engaged in very few conversations with other developers about the language we are developing and the flow of the nouns, verbs, attributes et all languge we are introducing and how it capture the domain. Similarly, I have very infrequently seen a group of developers debating a workflow or process they were introducing into a system and how effiecient it is for the user. Often developers are much more caught up in implementation details and the new hot framework.

I think this is a problem with how we build software. Understanding the domain you are implementing tools for too often feels slippery and distant from our actual day to day jobs, but should it? Should I not be learning the hundreth hot new concept introduced by browser manufacturers this month to become a better software developer? How would I even start learning about my stakeholders domain? Wait is my stakeholders domain actually my domain?

We need tools, language and approaches to help us better understand our domain, users, and ultimately be able to build a suitable language for our tooling. 

### How to approach a new problem/feature
Often times we follow waterfall procedures through our organization even if we follow agile in our engineering groups. The user's identify some problem multiple times and it gets on a product person's road map. That product person works to understand the problem identifying scope, impact, talking to the user and hopefully working with a UX person to come up with a solution.

At this point hopefully the UX person validates the solution, but they probably don't. Then the mock ups get kicked over to a group of engineers to implement. Engineering then gets involved and maybe pushes back or just blindly tries to figure out what they are implementing without any context of what the conversation was. There is even a chance the engineer implementing the solution has never talked to the user about the problem or worse doesn't understand the domain at all.

This distance from the problem would quickly be apparent if anyone on the product side or the user would read through the code being written by the developer. Likely, given an understanding of programming, the language being developed by the engineer would not be recognized as being the the problem scope and possibly not even close to the language used to discuss the domain being developed with in.

Lets call this process smell :P

### A better approach
Why is it considered proper to approach understanding a problem with an intermediary? As a developer I cannot count the times I have felt disconnected from what I was implementing. For a long time I struggled to with the idea that I was to just build what I was told and expected to understand that it was the best approach because some one said so. I have far too much curiosity for this to be acceptable to me.

I had worn many hats, UX designer, Project manager, developer and integration coordinator. Some how the whole process felt disconnected to me. The role of each of these employees was clear to me. I knew why things moved threw a pipeline, assembly lines had influenced all of the standard processes for every industry since the world changing introduction of the model T. But applying similar handoffs between steps in the development of software some how felt flimsy to me.

Over time I have come to respect and consider a few different ideas about how to do this better. I wish to challenge some practices about how we write code, how we explore problems and the way we form solutions.

### When we try to build a solution and make a mess

> “When you’re a carpenter making a beautiful chest of drawers, you’re not going to use a piece of plywood on the back, even though it faces the wall and nobody will ever see it. You’ll know it’s there, so you’re going to use a beautiful piece of wood on the back. For you to sleep well at night, the aesthetic, the quality, has to be carried all the way through.” Steve Jobs

We talk about craftsmanship a lot in software. I think that we think about software craftsmanship in too much of a limited view point. I look instead to organic architecture as inspiration of what truly well built software should look like.

> "Form follows function - that has been misunderstood. Form and function should be one, joined in a spiritual union." Frank Lloyd Wright

Well written software should be one with its domain. If it is true that software is eating the world, then well software should be what it eats, not what it eats should become software.

The responsibility of the form "software" fitting in the function "domain" actually lies at the software engineer, although we seem to try to split this responsibility amond multiple parties and leave each with only a slice of the pie. I do not wish to be little these other roles but instead want to see them connect into a unified team seeking to understand and work with in the enviroment in which they are operating, this is how we build sustainable, eviroment aware software.

### Framing the domain
Over the years there have probably been tens or hundreds of people who have contributed knowledge, ideas, solutions to your business/domain. The degree to which the context of these touch points is recreatable is important.

We have all been in a code base trying to understand how a certain feature works only to find out that every line of code has been named after a video game character. All of a sudden you have gone from befuddled to where something is happening to bemoaning the developer who named the parsing library Koopa Troopa and expected you to be able to find that at 3 in the morning when it was not working.

Now you need to implement a new feature in the parsing library, but not only do you not have the understanding of how Koopa Troopa eating a mushroom works, but you have no context of why the functions were created the way they were and how the developer choose to use a linked list instead of an array. If this feels all too familar I am right there with you.

While this implementation technically exists on a project and has given me nightmares it is a worst case scenario. Alternatively I have worked on projects where classes in an application named say "order" mean something different in the application then what "order" means in the organization. Leading to really difficult confusing conversations.

All these problems are problems of language and context. 

### Survey the land
When an organic architect starts a project the first thing the do is study the environment, software engineers should do the same. Our environment is the problem and the domain, not the hills and the trees.

When we first start to explore problems, I believe it is vital to have at least one developer in the room. Asking questions early, exploring the users world, job shadowing and building empathy for how things are done today, what is good, what is bad, process, lessons learned etc... Often times automations fall directly out of experimentation with a manual process, conveying as much information from the user directly to the developer can cut out information loss and help the developer not lose lessons learned.

Often times developers are left out of the room when talking to users, if you work for a consultant you know the pain of sales saying everything will be great without even sharing the problem with you. Why are developers left out of the room? 

I have strove to be approachable to users my whole life and seen a number of user/developer interactions. I personally think there is some times a difficulty in being a developer in a room with a user, you cannot communicate, developers tend to sweat the implementation details way too soon and we have a tendency to jump to solutions way to early, my wife will tell you I am this way often. As a developer it is super important to build skills around information gathering and learn to deffer worries around implementation. The ability to see a user where they are at will help you learn what you need to know to make a better solution and help you possibly with forsight of where a application may go at a later time, helping you to avoid programming yourself into a corner.

Once we have talked to the user, it is a good idea to capture any vocabulary we may have learned and share it back for validation of accuracy, this can turn up holes in your understanding very quickly and can eventually turn into useful software documentation and training materials long term.

### Discuss ideas
After this process, you have likely come up with some ideas. Don't present ideas when discussing the problem with the user at first. It is better to spend time with where they are at the problem they are facing in the first round. 

I ussually like to go back with a small team and start throwing crazy ideas at the wall, un-incumbered creativity is helpful at this stage, so destroy it with a dinosaur is a valid solution, beside I want to build a dinosaur. A brainstorming session after a well informed user exploration can bring up powerful ideas and is lots of fun. It also helps you better capture your understanding of the domain by talking through the problem with some one else who was listening further solidifying your understanding of all the things you will be working on. 



### Understanding the domain
The highest level of communication in our industry is our domain. Your domain could be anything maybe programming lifecycles, banking, warranty proccesses, farming or some other human problem. This is often an after thought when we look for programmers, but the ability to understand the domain you are working in will help programmers conceptualize solutions that are more flexible and empathetic to the users.

The domain maybe any series of concepts that are important, the language used to discuss the involved entities, the processes required to fullfill your goals, the problems you are seeking to understand and solve, the things everyone in your domain does and the propreitary things that make your company different. The domain

- The idea or problem being explored
- The shared domain language
- The company/context specific domain language
- The contextual opinions about how to approach the domain

### Grappling with the language of the domain
Every proffession has its own set of vocabulary that is specific to its domain, this is sometime even specific to a very granular level, company, dept etc... Understanding the language of the domain is vital in understanding what is being asked of the solution being implemented. Capturing these concepts not just at the time of implementation but also for feature additions and refactors is critical to a well understood codebase. Often times bugs in our code are not actually implementation problems but mis-understood requirements. Understanding the language of the domain is vital in understanding what is being requested.

One of the main problems is the loss of context over time/process. Understanding of a problem is generally captured and passed on many times, we have all played telephone in the past. Many of our organizational tools enforce a telephone like context loss. During each hand off of information there is context loss, missed ideas and miss communications. Worst case scenarios include loving terms such as thrown over the fence.

Microservices, APIs, and other consumer models can further perpetuate the problem. Many times the consumers of these features have very little insight into the orginal understandings that helped to create the features they are consuming. This is further intesified by bad documenatation and no way to see what is actually happening under the hood.

Currently the output of our processes as we work through the language of the domain is not captured in any long lived centralized format, it is scattered around the codebase, issues, requirements and other communications. But rarely if ever have I come across anything that resembles dictionary of terms at a company or in a program. This situation can often cause problems in future communications. 

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


Poincare and the unconcious finding of harmony

Our language for this is muddied by implementation details, lets look for inspiration else where. Organic architecture and techinics for introducing un-natural structure in a natural way.

Design thinking's role.

Shared vocabulary and where is our dictionary

The code review as a tool to check yourself.

Comments in code should reflect definition in more context then just the code, it bridges a gap between the human problem and the implementation.

## Story of my trial and error

## Some solutions

### Defining the problem

### Understanding the domain

### Mapping the key vocabulary/concepts

### `