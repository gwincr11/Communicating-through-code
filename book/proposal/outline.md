# Outline for Design Thinking for Developers

## Chapter 1: What is Design Thinking

Solving hard problems is challenging, solving hard problems without first exposing yourself to the situation is impossible. But this is consistently how we approach software development. A product manager tries to understand a feature someone needs to solve their problem, they then condense this down into an issue that can fit into our software project management process of choice and hand it to a developer to implement.

This leads to a series of problems with the solution, a lack of domain knowledge throughout the organization, mis-leading code, poor data structures, un-maintainable codebases, in-sufficient or incorrect solutions and more.

We need a better toolset, I would never expect a doctor to attempt surgery on a patient without ever meeting the patient. Why do we accept this in our work? We lack a process, one interesting observation I have noticed is that software developers can create amazing solutions to software problems, this is because the domain is tightly coupled to the developers work. We intuitively understand how to write software for the problems we face every day because we are continuously exposed to them. The solution we build for other problems facing the world tend to not be as good. We need a process that exposes developers to the domains they are working in. This process needs to also improve upon out other processes that we have found to work well.

Design thinking is just such a process, it breaks down the process of learning about a domain and a problem into a series of methods we can reproduce. It does so by augmenting our domain learning and decision processes, many of which we currently do but in an informal way. In its simplest form solving a problem is going through a series of steps to identify the issue, understand the problem, come up with a solution and implement the solution. In reality there are millions of factors involved along the way from identifying to solving and all of these steps impact the quality of the solution.

In this first chapter we will take a look at what design thinking is, outline the commonly referred to process and pick apart whether it needs to be done in totality. 

## Chapter 2: A brief intro to Domain Driven Design

Design thinking process can offer an excellent way to engage domain experts in the creation of a product. This brief chapter will offer a overview of three domain driven design ideas, ubiquitous language, domain events and context bounding. 

These tools are helpful to programmers working within any organization regardless of wether a full fledged domain language is being used or not. In this chapter I will outline the final products we hope to gain through the book including a glossary, context boundaries for primary and supporting domains, domain events and org personas.

## Chapter 3: Discovery
In this book we will be outlining the steps a development team is taking to implement a new warranty tool for a bike company. The first step to working on any problem is learning everything you can about the problem. This phase is often one that software developers are left out of. We will explore why this is and why it should not be the case. 

The first exercise introduced is a Stake Holder Mapping. This is a method for identifying potential domain experts to consult regarding the current process in place for warranty issues. The StakeHolder mapping also serves as a nice first pass at a bounded context diagram.

Next we will introduce how to develop buy in from domain experts and bring them into the process. This includes setting expectations, motivating participation and introducing the problem. 

The final method introduced in this chapter is Experience Diagraming. This is a method for exploring the current process and visualizing it. Each of our identified stakeholders will be utilized to help outline all the steps a warranty takes from creation to completion from their perspective. This lifecycle exploration helps us to see potential areas of improvement. It also provides a collection point to work on our context boundaries and ubiquitous language.

## Chapter 4: Interviewing and Job Shadowing

Now that we have identified all the stakeholders and processes we will be impacting, we can develop a picture of day to day operations. Job shadowing and interviewing are two valuable tools for exploring how the user does the task you are looking to augment everyday. 

In this chapter we will outline how to conduct a successful interview and how to do job shadowing. This includes 

- Using our stakeholder map and context bounding to identify interviewees.
- Getting permission.
- How to run a successful interview process.
- Finding in roads for future collaboration.
- Capturing ubiquitous language.
- Diagramming process flows and updating our experience diagrams with new context.
- Identifying domain events.
- Looking for hacks and other contextual clues. 

## Chapter 5: Gaining Context

In this chapter we introduce two methods for contextualizing information we gained in the prior exercises affinity clustering and rose bud thorn. 

Affinity clustering is a method which helps to sort our notes into contextually similar groups. Through this process we sort the findings and observe groups that naturally start to emerge. Often we find numerous groupings inside a problem area that may map to or expand upon our contextual boundaries. We will use the output of this exercise in three ways, first to redefine our contextual boundaries. Next we will seek related sets of problems we can later prioritize. Finally we will introduce ways to utilize affinity mapping to organize our collected language, processes and domain events.

The second method introduced is Rose Bud Thorn this tool helps categorize findings into positive (Rose), negative (Thorn) and items with potential for improvement (Bud). We will then use this as a way to discuss identifying potential areas for improvement.


## Chapter 6: Creating our Ubiquitous Language Glossary
We now have a collection of language and bounded context that will allow us to create a glossary. We will explore what a glossary is and how to create one from your findings. 

The book will also show some pseudo code examples of how this language and context bound idea can be implemented to lead to cleaner implementation and separation of concerns. We will explore techniques for name-spacing code, organizing files, naming methods vs. objects and separating concerns.

We will also explore how to keep these glossaries up to date and useful in your projects.

## Chapter 7: Defining a problem statement

Often times our problem statement is handed to us due to business needs, however the process by which we choose the problem to work on and state the problem are often difficult tasks that can be aided by process. There are also situations in which we maybe using design thinking to explore a new process inside our development processes.

Defining a problem statement can be political and difficult to word. Our Rose, Bud, Thorn and Affinity Clustering activities have exposed a number of areas which we can focus on but picking one to hone in on is a matter of aligning people. When we do define it we need to ensure the language we use is open enough to encourage our creative process, yet bounded enough to keep us focused on our problem area.

We will utilize explore proper language for phrasing problem statements and why language matters. Once we have a identified problem statements we will look at two methods of choosing the problem to work on, bracketing and star voting.

## Chapter 8: Ideation

Now that we have a problem statement to work on we need to start thinking about how to approach our problem. Ideation is a process of generating as many ideas as possible. These techniques are useful in a number of scenarios where you need to generate potential solutions to a well understood problem.

We will introduce a few exercises to help with the brainstorming process

## Chapter 9: Ranking competing ideas

## Chapter 10: Prototyping

## Chapter 11: Validating Prototypes

## Chapter 12: Cooking with ingredients

## Chapter x: Going remote.x`