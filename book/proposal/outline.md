# Outline for Design Thinking for Developers

## Chapter 1: Introduction

Organic software:

- Seeks a natural progression of its environment.
- Flows and changes effortlessly with its domain.
- Satisfy social needs responsibly.
- Focuses on communicating consistently across the implementation and domain.
- Seek empowering solutions over narrowly targeted solutions.

Organic software is the modern ideal and quality needed if we seek to perpetuate the success and social responsibility of open source to a wider set of problems. We seek to serve the whole of life, seeking solutions which effortlessly enhance our environments in an informed, thoughtful and responsible manner.

Crafting organic software is challenging! Solving problems in an appropriate way without first exposing yourself to the situation is impossible! But this is consistently how we approach software development. A product manager tries to understand a feature someone thinks they need, the product manager then condenses this down into an issue that can fit into our software project management process of choice and a developer to implements.

This leads to a series of problems with the solution, a lack of domain knowledge throughout the organization, misleading code, poor data structures, un-maintainable codebase, insufficient or incorrect solutions and worse.

We will explore the intersection of the fields of design thinking, agile and domain-driven design as a better way to build products. Taking some of the best ideas from each while escaping some of the implementation details that can limit adoption.

In this first chapter, we will take a look at what design thinking is, outline the commonly referred to process and pick apart whether it needs to be done in totality. We will explore

- Discovery
- Ideation
- Prototyping
- Validation
- The Double D method

Design thinking process can offer an excellent way to engage domain experts in the creation of a product. Domain-driven design offers a set of tools for taking these findings and creating software implementations that more concisely capture the knowledge we have learned.

I will also introduce domain driven design ideas we will be covering in this book: 

- Ubiquitous languages
- Glossaries
- Context boundaries for primary and supporting domains
- Domain events
- Org personas

## Chapter 2: Discovery
We will outline the steps a development team is taking to implement a new warranty tool for a bike company. Working on any problem first requires learning everything you can about the problem. This critical phase is often one that software developers are left out of. We will explore why this is and why it should not be the case. 

In this chapter we will introduce the following tools:

- Stakeholder mapping
- Context Boundaries
- Bounded context diagrams

The first exercise introduced is a Stake Holder Mapping. This is a method for identifying potential domain experts to consult regarding the current process in place for warranty issues. The StakeHolder mapping also serves as a nice first pass at a bounded context diagram.


## Chapter 3: Interviewing and Job Shadowing

Now that we have identified all the stakeholders and processes we will impact, we can develop a picture of day to day operations. Job shadowing and interviewing are two valuable tools for exploring how the user does the task you are looking to augment every day. 

In this chapter, we will outline how to conduct a successful interview and how to do job shadowing. This includes 

- Using our stakeholder map and context bounding to identify interviewees.
- Getting permission.
- How to run a successful interview process.
- Finding inroads for future collaboration.
- Capturing ubiquitous language.
- Diagramming process flows and updating our experience diagrams with the new context.
- Identifying domain events.
- Looking for hacks and other contextual clues. 

## Chapter 4: Gaining Context

In this chapter, we introduce two methods for contextualizing information we gained in the prior exercises:

- Affinity clustering
- Rose, Bud, Thorn. 

Affinity clustering is a method which helps to sort our notes into contextually similar groups. Through this process, we sort the findings and observe groups that naturally start to emerge. Often we find numerous groupings inside a problem area that may map to or expand upon our contextual boundaries. We will use the output of this exercise in three ways, first to redefine our contextual boundaries. Next, we will seek related sets of problems we can later prioritize. Finally, we will introduce ways to utilize affinity mapping to organize our collected language, processes and domain events.

The second method introduced is Rose Bud Thorn. This is a tool used to categorize findings into positive (Rose), negative (Thorn) and items with potential for improvement (Bud). We will then use this as a way to discuss identifying potential areas for improvement.


## Chapter 5: Creating and Using our Ubiquitous Language Glossary
We now have a collection of language and bounded context that will allow us to create a glossary. We will explore what a glossary is and how to create one from your findings. 

- Breaking apart your domain by context boundaries
- Keeping language contextual
- Context Mapping
- Escaping implementation details
- Maintaining ubiquitous language and context boundaries long term.

The book will also show some pseudo code examples of how this language and context-bound idea can be implemented to lead to cleaner implementation and separation of concerns. We will explore techniques for name-spacing code, organizing files, naming methods vs. objects and separating concerns. One tricky thing in the world of domain driven design is the level of implementation detail, this can prevent adoption or cause friction with timelines or frameworks. We will explore how to accept some ideas but not others.

We will also explore how to keep these glossaries up to date and useful in your projects.

## Chapter 6: Defining a problem statement

Often times our problem statement is handed to us due to business needs, however, the process by which we choose the problem to work on and state the problem are often difficult tasks that can be aided by the process. There are also situations in which we may be using design thinking to explore a new process inside our development processes.

Defining a problem statement can be political and difficult to write. Our Rose, Bud, Thorn and Affinity Clustering activities have exposed a number of areas which we can focus on but picking one to focus on is a matter of aligning people. When we do define it we need to ensure the language we use is open enough to encourage our creative process, yet bounded enough to keep us focused on our problem area.

We will utilize explore the proper language for phrasing problem statements and why language matters. Once we have identified the problem statements, we will look at two methods of choosing the problem to work on, bracketing and star voting.

- How to phrase a problem statement to encourage exploration.
- What is broad enough vs too broad in a statement.
- Choosing one problem statement among many potentials

## Chapter 7: Ideation

Now that we have a problem statement to work on we need to start thinking about how to approach our problem. Ideation is a process of generating as many ideas as possible. These techniques are useful in a number of scenarios where you need to generate potential solutions to a well-understood problem.

We will introduce a few exercises to help with the brainstorming process. 

- Creative matrix
- Story boarding
- Expanding statement starters

First, we will try redefining the opportunity by changing our statement starter by turning it into a question in the phrases of who, what, when, where, why and how. We will use each of these prompts to define as many answers as possible.

Next, we will look at creating a creative matrix.  In this process, we define 5 assets we have at our dispense to solve the problem and we align those with our domain areas to brainstorm how the statement starter could be solved, approached etc in different combinations of tools and subdomains.

## Chapter 8: Ranking competing ideas

At this point we have created a number of competing solutions, deciding which ones to pursue is often politically charged. We need tools to remove the personal attachment we hold to ideas and look at them subjectively. We will look at three exercises for doing this work. These tools are exceptionally valuable for going through backlogs, ranking company alignment goals like OKRs or getting stakeholders to express their needs accurately.

Method:
- Importance difficulty mapping
- Buy a feature
- Bracket voting 

First, we will look at Importance Difficulty Mapping. In this exercise, we create an (x,y) graph to visualize the importance and difficulty of every item we came up with during ideation in a quadrant. This visualization shows us the low hanging fruit, high-importance difficult items, low-importance low- difficulty items, and low-important high-difficulty items; assisting us in choosing what to work on.

Buy a Feature is a game in which each player is given a budget and can choose which features they would pay for. This show which features are most valuable to which stakeholders.

Brackets are a fun way to have features compete against each other for votes. As you work through the bracket people voting are allowed to change what they are rooting for so everyone's voice is heard to completion.

## Chapter 9: Prototyping

Now that we have the ranked ideas we wish to implement, it is time to validate our ideas and experiment with competing implementation details. 

There are two types of prototyping that make sense for software developers that I have experienced. 

The first is a user-facing prototype that shows off a feature that they will be working with, this is an invaluable alignment tool for working with stakeholder.

The second is a technology prototype, often when we set out to build a new feature, app, etc... much of our architecture decision is based on the strongest political position in the room or the most familiar tech. Technology prototypes allow us to break out of this and offer a space to experiment and validate different ideas. We will outline how to run a successful technical prototyping session.

Methods:

- User facing prototypes.
- Implementation prototypes.
- Setting up rails to encourage safe experimentation.
- Encouraging playful development.

## Chapter 10: Validating and learning from Prototypes

We prototype in order to ensure we are choosing the right direction, but learning from prototypes is an art. We need to separate our preference and bias and see what the prototype is really telling us. We will look at user testing our stakeholder facing prototypes and how to iterate. 

We will also look at tools for qualifying technical prototypes, setting criteria, validating new tech and outlining how to assess risk.

Methods:
- Inviting users to the testing table
- Paper prototype testing
- Validating technical prototypes by risk assessment
- Combining competing ideas.

## Chapter 11: Cooking with ingredients

Throughout this book, we have followed a very defined line of discovery, ideate, prototype and validate. This recipe is common in design thinking, however, the dogma of this process is misleading. Much like a great chef starts by following a recipe, they soon learn to break the ingredients apart and use them appropriately in different scenarios. We can utilize any one of these different methods in a number of scenarios and add a dash of ideation here and a prototyping session there without following the entire process.

In this chapter we will look at running better retros, aligning a backlog, blameless incident response, prototyping the competing implementation details, and how to run partial or full design thinking process in short periods of time.

Methods:

- Bridging the gap with agile
- Developing a design sense
- Slowly introducing teams to these methods.
- Retros.
- Scrum planning


## Chapter 12: Going remote

Many of the tools in this book are possible to do remotely as well. Let's take some of the common methods in this book and discuss how we can bring them to remote teams.

- Google docs
- Post it note applications
- Story telling sessions
- Sharing videos
- Code as documentation
- Test that represent intention