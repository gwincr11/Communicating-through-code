# Interviewing and Job Shadowing

What better way to learn about a topic then spend time with an expert? 

In our stakeholder mapping exercise, we began to identify different types of users we should communicate with to gain a better understanding of their working context and challenges. We will now explore some methods for engaging these users, or domain experts, to increase our awareness of their language, workflows, entities, and problems.

In this chapter, we will introduce interviewing and job shadowingas methods of digging deeper into the warranty workflow that exists today to better understand the domain we are working within. We will be looking to gain as many key insights as we can to aid our implementation choices in the future. 

We will explore how to conduct better interviews, get stakeholder buy-in, avoid common pitfalls that could bias your implementation and how to collect common language, domain events, and identify entities and processes.

# Identifying an interviewing topic

Our warranty process has been flagged for replacement because it is built in a legacy system that we believe is leading to tracking issues and slowing down communications. We have been implementing a new customer support portal in sales and management wants to tie the two systems together for a variety of reasons. The top-down pressure is revolving around tracking costs in warranty, but the warranty is expressing concerns about customer interactions and fearing a changing process. 

Our interview could go in a number of directions based on what we know. It would be easy to focus on what management wants out of the transition as hierarchies lead to this kind of approach. In our case, we choose to seek the topic which is the most domain centric. What does that mean? Glad you asked, we want to get at the most common workflows, entities, processes in the central workflows. In our case, what is the common lifecycle of a warranty? This will ensure our solution first focuses on the primary work that needs to be completed, primary domain. We want to avoid getting into the weeds of how cost is being tracked at this point, although it is a motivating force in the org, once we have a solid core domain modeled we can move to cost tracking as a separate subdomain and explore that problem independently. It may be a driver for why we are making the switch, but the important thing to tackle first is the core domain.

# Determining who to interview

Different domain experts will work with our system in different ways and have different needs of the system. If we refer to our bounded contexts we can gain some insight into different entities that may need to access this system, we can also do a separate stakeholder mapping exercise just for this project, it may show new bounded contexts to account for. 

We want to ensure we interview a few people from each context to get some different perspectives, when possible these people should have very different backgrounds. For our warranty system we have identified the following domain experts to discuss this system with:

- The warranty dept.
- Inventory and purchasing.
- Internal sales reps.
- Outside sale reps.
- Small bike shop mechanic.
- Large outdoor sporting goods store shop manager.
- Product management.

This represents the core group of domain experts that touch the warranty system on a daily basis today. Each of them may have very different roles in the company and need very different things out of the system. This should give us a broad view of the domain space and how the different contexts view things.

We have a pretty long list here, generally speaking, it may be hard to talk to so many stakeholders. However, talking to 2-3 is always better than talking to none. 

# Getting permission from stakeholders

We need to reach out to each of our domain experts and get their permission to do the interviews. The way we speak to each group may be different in tone based on who they are, our relationship with them, and their relationship to the project.

Warranty should hopefully be aware of the project, getting permission from the core domain experts who you are directly affecting their workflow should be easy. Sometimes you need to deal with push back about changing processes, but this is an opportunity to ease tensions and express your ambitions to improve their day to day work. Try building enthusiasm in the project by showing a willingness to work together and project often go from dreaded to exciting as the domain experts see the ability to change their day to day workflows in a positive way.

Outside collaborators such as bike shops are often trickier, in this case, I will often leverage the relationship a sales rep has with a shop or find a shop warranty particularly enjoys. Often times your domain experts can grease the wheels and even get outside collaborators excited about contributing back toward improving systems they dislike.

Internal collaborators like sales may often state they don't have time to do an interview. These interviews can sometimes be the trickiest in some ways, however, I have had success with drop-in conversation or offering to take someone out to lunch.

# Writing questions

Now it is time to write interview questions. Interviewing people is a bit like hanging out at the bar with a friend asking them about their last great adventure. We want to go into it curious and with a beginners mindset. It is tempting to approach interview questions in a similar way to writing survey questions, by this I mean questions with yes/no multiple choice answers, try to avoid this. 

We will be using some question starters to help us create good interviewing starters, thinking about interview questions as conversation starters is a good approach. Our starters are:

- Tell me about the last time you did x.
- Have you done x differently in the past? Maybe at a different company.
- What do you tell new co-workers on their first day?
- What does a typical x process look like?

Filling in our topic `common warranty lifecycle` we end up with the following questions:

- Tell me about the last warranty you processed.
- Have you processed warranties differently in the past?
- What do you tell new warranty employees on their first day about the process?
- What is the process for a typical warranty?

These question will spark conversation and have plenty of room to breath. The goal is to remove yourself from the conversation as much as possible and let the domain expert explain their process. It is common to interject bias into questions and we want to avoid that as much as possible.

It is important to mostly let the interviewee talk, we want to be an active listener. From time to time something will come up in the interview that you think it would be nice to expand upon. Having some potential lines in your questions to help you frame a question in a way that qualifies the statement or expands upon it is helpful.

- If you had x how frequently would you have used it in the past 6 months?
- Just to be sure I am clear if you had x, what would it allow you to do that you cannot do now?
- Tell me more about why you prefer the competitors feature over ours.
- If you had to choose between x and y which would you choose?

At some point in the interview, the conversation will wind down. I like to offer the domain expert the ability to create a solution at this point. Often they have stewed over a potential solution or better workflow but don't possess the skills required to implement it. Have some questions ready for this time:

- How would you solve x?
- If you could change one thing today what would it be?
- If you had a magic wand what would you change?

I will add all these questions to a question outline so they are ready for the interview day.

## Identifying bias

Creating interviewing questions or preparing for a job shadowing exercise can be a bit of a trap. As developers, we have strong thoughts and opinions about our users and our products direction. These thoughts and opinions will impact the people we choose to talk to, the topics we lean towards, the questions we ask and how we listen. Acknowledging our biases before starting any sort of interviewing process is a good first step.

There are a number of common biases to examine prior to entering any period of interviewing. Identifying these biases in ourselves and our team are not just useful for interviewing and job shadowing but can also help us to understand our team dynamics, inter-team communications and product decision influencers.

The main biases I have seen include confirmation bias, survivorship bias, availability bias, and social desirability.

#### Confirmation biases
Confirmation bias is the tendency to interpret new evidence as a confirmation of one's existing beliefs. An example of confirmation bias is someone who holds the belief that left-handed people are more creative than right-handed people. In confirmation bias this individual would place greater importance on this correlation confirming their bias in their mind every time they met a left-handed person who was creative, they would ignore the right-handed people who are creative. 

If you start to see questions that can be thought of as confirming an idea or seeking evidence of a belief you are probably in the middle of confirmation bias. Also, be cognizant of the tendency humans have to ignore disconfirming information, this is how stereotypes perpetuate.

#### Survivorship biases
During WW2 the US Military was attempting to strengthen the armor on planes. In order to do this, they took stock of where the bullet holes on the planes were located and placed more armor in those locations. This is a great example of the problem with survivorship bias. 

The planes hit in the spot where the engineers where putting more armor were far safer because a plane could survive a hit in that location. They later realized they needed to put armor where they were not seeing holes because those planes were not surviving.

We oftentimes see similar scenarios in our own interviews, our tendency is to interview our best customers or heaviest users. This is helpful from a relationship perspective, but those users needs are mostly being met. Instead, we should try to interview the users that abandon our product for another product.

#### Availability Biases

As we go through our day we are bombarded with the current events of our work; support's needs, issues you have been working on, parts of the codebase you wrote etc... Anything that is top of mind can influence how you see or think about a situation. 

This is why if your company just released a shiny new feature you are more likely to suggest it as a possible solution over something that may be more appropriate that came out 5 years ago simply because it is top of mind. 

#### Social Desirability biases
Anyone being interviewed will be biased toward answering questions in a way that is socially acceptable. When was the last time someone asked you if you test all your code, how did you answer? If you are like most people you don't test all your code, but you said yes, or shaped some story to make it sound like you do most of the time, because you want them to think of you in a desirable way. 

This is social desirability bias it is a bit like peer pressure, we have a reason to lie or color the truth because we are trying to align our practices with what we perceive as the socially desired values. 


### How do we interview people without these biases?

Interviewing people is hard, we have to navigate both our biases and the interviewees. Really great interviewers are hard to come by, but not everyone needs to be Terry Gross to get value out of an interview. 

You can learn to follow a mostly formulaic interview process and get good at it. I am often reminded of a statement a friend of mine told me about interviewing, you have 2 ears and 1 mouth try to use them in that proportion. It really is all about listening. 

Most people love to tell stories and if you can get a person into a storytelling mode they will usually become fairly honest and straightforward as opposed answering questions in a survey style. 

So how do we conduct such an interview?


# Interviewing

## Location

I tend to prefer comfortable informal interviews, I feel people can be more authentic. You may also choose to simply meet people where they are, sometimes other people in the room can be good as it becomes a case of interviewing a group as people often chime in, other times social pressures can keep people from saying what they really think. In our case, the warranty system is ok to interview in an open context as there are not really pressing feelings involved or social pressure.

To prepare our interviewing space I go through this checklist:

- [ ] At least one note taker.
- [ ] Question we are going to ask.
- [ ] Post-it notes and pens.
- [ ] If desired a recording device, make sure this is ok with the interviewee.

## Conducting the interview

There is a common pattern to an interview you can follow to make things more natural, I even put this into a template to remind myself of the steps to take.

The first step in the process is an introduction. In this portion of the interview we need to cover the following three items:

1. Introduce yourself.
2. State your purpose.
3. Obtain consent to continue with the interview.

Once we have done the introduction, I like to ask the interviewee something personal, to ease any tension. Ask them about their day, comment on a unique article of clothing or any personal question that is friendly and easy to discuss. I try to avoid cliche question or topics like the weather as they have grown to lack any depth and don't let the person talk about themselves. If you let the person talk about themselves they will be much more at ease.

On to the questions! At this point, we ask the pre-planned questions. I usually have 3-4 ready and ideally, these questions should be open-ended. When getting answers don't feel like you need to stay on script and make sure to let the silence hang a little longer than normal. Often the best interview veers in an unexpected direction naturally as you explore reasons and ideas that are unique to the interviewee and potentially introduce topics or ideas you had not considered.

Once the conversation starts to dwindle I often will ask the users a straightforward question that prompts them to solve their own problem. Questions like how would you fix the situation or how have you dealt with this in another role often prompt the user to offer a solution. This may have value or not, but often is insightful in a different way.

The time has come to conclude our interview, at this point you can thank the participant and exchange pleasantries. Before the interviewee leaves, I always like to ask for permission to collaborate in the future. This helps build a pool of domain experts to tap when the time comes to test prototypes, validate ideas or collect extra information.

## The warranty domain expert interview

It is time to interview our warranty domain expert, Nevin, we walk through our introductions and purpose statement, obtain consent one last time then jump into our questions.

> You: Can you tell me about the last warranty you processed?

> Nevin: This xl Vision mountain bike has a broken frame, Harrie's bike shop contacted me via email to notify me about the issue. We sent out a new frame once we identified it was a manufacturing defect. I found the frame in a warehouse close to the shop and placed a shipping order with the distribution center. 

There is a lot to unpack in that brief overview. From a note takers perspective we can identify: 

- A high level process: notification of issue -> assessment -> decision of action to take -> shipping arrangement
    - Domain events in this process
      - Warranty issue received.
      - Warranty issue acknowledged by the employee.
      - Warranty issue assessed.
      - Warranty issue resolution proposed
      - Warranty issue resolution in progress
      - Warranty issue resolved.
      - Replacement product shipment received at the warehouse
      - Replacement product shipped
      - Replacement product delivered
- A number of potential bounded contexts:
  - Bike shop.
  - Manufacturer.
  - External Warehouse.
  - Shipping
- Domain entities
  - Bike, 
      - Size: Xl 
      - Category: Mountain Bike
      - Product Name: Vision
  - Bike Shop:
      - Name: Harrie's
      - Shipping address?
  - Warranty notification:

These things could feed our ubiquitous language, expand our bounded contexts, add to our domain events and ultimately inform our implementation. 

From the interviewer perspective, we can now take this interview in a lot of directions. Since we are looking to rebuild the warranty system from the ground up, the first thing we want to focus on is the warranty notification data.

> You: Can you tell me more about how you were notified of the issue and what information you needed to assess this incident?

> Nevin: Sure, Harries emailed us about the issue. We require pictures of the bike, pictures of the broken part, the serial number, and a bit of info about how the break occurred. We have an email template we send them to fill in and ask any follow-up questions over email. We also ask for a single point of contact with whom to work through the issue with on the shop end to simplify communications. Based on the type of break we assign a category to the issue.

> You: This is great would you mind emailing us that template? Can you forward us a few customer interaction examples?

Once again we have information that we can use to fill out our domain knowledge even more. It is great to try to collect any assets that may already exist to assist a process, often these organically grown processes built in a low fidelity way our early prototypes of what is really desired. We can also further develop our domain knowledge assets with this small question and answer cycle.

- Domain entities
  - Bike, 
      - size: xl 
      - category: Mountain Bike
      - Product name: Vision
      - Serial number
  - Bike Shop:
      - Name: Harrie's
      - Shipping address?
      - Email address
      - Employees
  - Warranty notification:
      - Image of the bike
      - serial number
      - Image of the break
      - How the break occurred
      - Point of contact for warranty submitor
      - Break type category

      
 This process could go on to investigate shipping workflows, warehouse interactions, manufacturer needs etc...
 
> You: Thanks for all this information Nevin this is amazing. Would you mind if I reach out to you in the future for follow-up information or to share ideas with you and get your feedback?
 
> Nevin: That would be great I am really excited to fix this.
 
> You: I am also wondering if you would let me shadow you for an hour or so while you work on some warranties to see what your workflow looks like?
 
## Note taking
 
It is tempting to try to model our database or layout our objects in our notes. Ideally, notes will quickly capture ideas and not model things for us. Ultimately we are trying to understand our domain, not figure out implementation details. 

Try to keep your notes short, using post-it notes for note taking will encourage this as space is limited. We want to capture just enough information to understand the domain. Notes like:

- Bike, 
  - size: xl 
  - category: Mountain Bike
  - Product Name: Vision
  - Serial number

Are preferred to: 

> A bike has a size, category, product name, and serial number. Each warranty has a bike and the warranty belongs to a bike shop. 

This is the start of a DB model, you will get there eventually but it is far too early in the process to know if what you are doing enforces the domain properly.


## Developing your ubiquitous language
At this point, we should think of things as developing an encyclopedia of institutional knowledge. In fact, I would recommend taking on this task at this point. Every interview you undertake should be approached as an opportunity to collect and share very useful domain knowledge that may currently exist in a silo.
 
If you can build a wiki or some other communication tool that can state what all the domain language is in different parts of your institution then you have a communication standard you can reference for new hires, naming things in the future and understanding what user means in the context of sales.

# Job Shadowing

Nevin has invited us back to do some job shadowing. In this process, we are looking to gain on the ground experience to see all the parts of the process that are often not discussed in an interview because they are so ingrained in the day-to-day activity that they seem obvious to the domain expert. 

As an outside party, we need to steep ourselves in the world of the domain expert a bit, as what they take for granted may be completely foreign to us. We may also see extremely inefficient practices that computers could automate, that the domain expert may never recognize as a problem.

## Setup
In a job shadowing exercise, we are entering into the workspace of the domain expert. We need to try to set ourselves up to be as unobtrusive as possible. Often times this means preparing ourselves as humans to be stealth. Have your pens and paper ready, get your coffee in hand or snack and prepare to sit back and be as quiet as a mouse, whatever that means for you.

You likely also want to arrange a time when the domain expert is actively undertaking the work you want to observe. Find a time that works well for this observation, ideally, they should be moderately busy, meaning not to overwhelmed to answer your questions but busy enough to show some variety.

When you come into their workspace expect there to be a bit of friendly interaction at the beginning and perhaps a bit of awkwardness as they start their day. Starting work is hard enough, doing it while being watched can definitely impact performance. You can try to ease tension by bringing donuts, telling jokes and then slowly receding back. 

## Observation

While observing try to ask a minimal amount of questions to the observant. I like to take notes of any questions I had and save them for the end. It is normal to have a follow up short interview after the shadowing session. It may also be helpful to have the domain expert explain out loud what they are doing as they undertake their work almost like a stream of consciousness. I tend to reserve this to the particularly complex tasks as it can influence their workflow.

There are a few key areas I tend to hone in on when observing a domain expert doing their work. The main 3 are tools, processes, and interactions. I find these are high-level categories I can hone in on and organize my thinking and notes around.

### Tools

Any tooling the domain expert interacts with is helpful to note. Often we are integrating with, replacing or augmenting tools. Having an understanding of what tools are in place, what they are used for, why they were chosen, where they fit in the process and what features are used is often handy to note for later use.

It can also help us to understand where our tooling fits in the broader picture, are these outside system interacting with ours, could they? Should they? Are their patterns or languages familiar to the domain expert from these tools that we can co-opt to simplify the environment of the domain expert? Tools in the environment are important to any domain expert, thus they should be important to us as augmenters of the environment.

### Processes

How are entities moving through the environments, what tools are taking inputs, creating outputs? What do these inputs and outputs look like? Are most of the processes happening on a computer? Is there physical workspace to consider? 

Most of the workflow we are examining is contained in the process, whether or not it is recognized as such or any good. Looking for patterns in the workflow and things that could potentially become patterns is a good thing to note.

This is a great time to outline domain entities, domain events and states that entities could exist in. You may want to actually draw timelines, comics, physical maps or process diagrams to show how things move through the process.

### Interactions

Interactions between different domain experts, processes or tools are all helpful to capture. Is there a point in time where a certain entity transfer to another group in your organization? Does the domain expert need to reach out to other places for information? Does information transfer from one system to another? How are the domain experts entering data into different places?

All these interactions likely point to some piece of tooling you will need to be aware of or consider implementing. Try to map out how entities are moving around in the context bounds and what action is required to move them in an out of these interactions.

### Looking for hacks

This is not one of my top 3 areas for focus, but hacks are really valuable for finding confusing or troublesome parts of a system. If a domain expert has taken the time to implement a hack to get around a situation it is likely that they understand something the implementors did not and got frustrated to a point that they fixed it themselves.

Hacks can take many forms, post-it notes with directions, macros in excel, browser plugins, copy and past patterns and more. Anything, where the user created a one-off custom solution to a problem, is worth exploring.