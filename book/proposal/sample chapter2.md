# Interviewing and Job Shadowing

What better way to learn about a topic then spend time with an expert. In our stakeholder mapping exercise we began to identify different types of users we should communicate with to better understand their working context and challenges. Now we will explore some methods for engaging these domain experts to increase our awareness of their language, workflows, entities and problems. Our goals are to reduce friction in future communications with stakeholders and code changes. We achieve this by better understand the language, processes and tools of the working environment, ultimately resulting in code that fluidly evolves with its environment by utilizing the common language of the environment, enhancing the ability of the tools already in place and seeking to co-exist in harmony with the processes important to the problem space.

In this chapter we will introduce interviewing and job shadowing. We will use these methods to dig deep into the warranty workflow that exists today in order to understand the domain we are working within. We will be looking to gain as many key insights as we can to aid our implementation choices in the future. 

We will explore how to conduct better interviews, get stakeholder buy in, common pitfalls that could bias you implementation and how to collect common language, domain events, identify entities and processes.

# Identifying an interviewing topic

Our warranty process has been flagged for replacement because it is built in a legacy system that we believe is leading to tracking issues and slowing down communications. We have been implementing a new customer support portal in sales and management wants to tie the two systems together for a variety of reasons. The top down pressure is revolving around tracking costs in warranty, but warranty is expressing concerns about customer interactions and fearing a changing process. 

Our interview could go in a number of directions based on what we know. For example we could focus on:
	- Tracking issue that management is prioritizing.
	- The speed of communications for warranties.
	- The sales/warranty overlap.
	- The common warranty lifecycle.

Often times hierarchies lead to this kind of approach. We are focusing solely on x problem. This sort of approach assumes that we are certain of the issue itself. It also assumes we are comfortable enough with the domain to not spend time exploring the warranty domain at all and instead focus on a single problem in the domain. In our scenario the original warranty system was implemented over 10 years ago, none of the knowledge accumulated during that implementation is relevant or available any more as the implementation tooling is changing and the work itself is ready to be re-examined because the new development team is in no way familiar with the tools, processes and language of the warranty dept or processes between departments.

As is often the case we need to choose to seek the topic which is the most domain centric. We want to get at the most common workflows, entities, processes in the central workflows. The team needs to understand what is the common lifecycle of a warranty. This will ensure our solution first focuses on the primary work that needs to be completed, primary domain. We want to avoid getting into the weeds of how are cost being tracked at this point, although it is a motivating force in the org, once we have a solid core domain modeled we can move to cost tracking as a separate subdomain and explore that problem independently. It maybe a driver for why we are making the switch, but the important thing to tackle first is the core domain.

Once we have a well defined knowledge of the environment, functioning ubiquitous language among different stakeholders and suitable basic implementation of the warranty system we can narrow down our areas of interviewing to more specific features, such as the tracking needs. Prior to defining these context boundaries and ubiquitous language you increase the risk of speaking different languages and increasing code friction by encoding these mis-understandings into you implementation.

# Determining who to interview

Different domain experts will work with our system in different ways and have differing needs of the system. If we refer to our bounded contexts we can gain some insight into different entities that may need to access this system, we can also do a separate stakeholder mapping exercise just for this project, it may show new bounded contexts to account for. 

We should interview a few people from each context to get some different perspectives, when possible these people should have very different backgrounds. For our warranty system we have identified the following domain experts to discuss this system with:

- The warranty dept.
- Inventory and purchasing.
- Internal sales reps.
- Outside sale reps.
- Small bike shop mechanic.
- Large outdoor sporting goods store shop manager.
- Product management.


This represents the core group of domain experts that touch the warranty system on a daily basis today. Each of them have very different roles in the company and need very different things out of the system. This should give us a broad view of the domain space and how the different context view things.

We have a pretty long list here, generally speaking it maybe hard to talk to this many stakeholders. Trying to talk to 2-3 is better then talking to none.

Every interview cycle will have different interviewee needs. In our example we are seeking a broad audience as we are starting fresh. Once you have captured these perspectives for this broad sweeping project, future more focused projects can be limited to just the parts of the organization who's processes we are affecting. When limiting to less groups it is still a good idea to get some diversity in skillsets and application usage. I like to record interviews when possible so that I can reference them in the future should I need to.

# Getting buy in from stakeholders

We need to reach out to each of our domain experts and get their permission to do the interviews. The way we speak to each group will be different in tone based on who they are, our relationship with them, and their relationship to the project.

Warranty should be aware of the project, getting permission from the core domain experts who's workflow you are affecting should be easy. When you need to deal with push back about changing processes use this as an opportunity to ease tensions and express your ambitions to improve their day to day work. You can build enthusiasm in a project by showing a willingness to work together. Doing so projects often go from dreaded to exciting as the domain experts start to feel empowered to change their day to day workflows in a positive way.

Outside collaborators such as bike shops are often tricky, in this case try leveraging an internal relationship, in our case a sales rep has a relationship with a shop, or find a shop warranty particularly enjoys working with. Your domain experts can grease the wheels and even get outside collaborators excited about contributing back toward improving systems they dislike.

Internal collaborators like sales may often state they don't have time to do an interview. In this scenario I have had success with drop in conversation or offering to take some one out to lunch, beers may also help.

# Writing questions

Now it is time to write interview questions. Interviewing people is a bit like hanging out at the bar with a friend asking them about their last great adventure. We want to go into it curious and with a beginners mindset. It is tempting to approach interview questions in a similar way to writing survey questions, by this I mean questions with yes/no, multiple choice answers, try to avoid this. 

We will be using some question starters to help create good interviewing starters. I think about interview questions as conversation starters. Our question starters are:

- Tell me about the last time you did x.
- Have you done x differently in the past? Maybe at a different company.
- What do you tell new co-workers on their first day?
- What does a typical x process look like?

Filling in our topic `common warranty lifecycle` we end up with the following questions:

- Tell me about the last warranty you processed.
- Have you processed warranties differently in the past?
- What do you tell new warranty employees on their first day about the process?
- What is the process for a typical warranty?

With these questions we are seeking real world stories. Ideally the interviewee will walk you through an experience they recall from recent work. In our warranty example, we want the warranty dept to tell us about a warranty claim starting at the place where they learn about a new claim, how they interact with the person who submitted the claim, how they decide what action to take and how they take said action. There is a lot to dig into with a story that tells the lifecycle of a whole process such as this.

These question will spark a story and have plenty of room to breath. The goal is to remove yourself from the conversation as much as possible and let the domain expert explain their process start to finish. It is common to interject bias into questions and we want to avoid that as much as possible.

Your number one priority is to listen, not to talk. From time to time something will come up in the interview that you think it would be nice to expand upon. Having some potential questions to help you expand a statement in a way that qualifies the statement or expands upon will improve the quality of your interviews.

- If you had x how frequently would you have used it in the past 6 months?
- Just be be sure I am clear if you had x, what would it allow you to do that you cannot do now?
- Tell me more about why you prefer the competitors feature over ours.
- If you had to choose between x and y which would you choose?

Each of these questions is designed to dig into the specifics of a task. The 5 why's is another good practice, if you ask why 5 times you will generally get to the end of someone's knowledge on a topic. We want to get as deep into their processes so we can understand what they are doing, why and how they talk about it. During this we are extracting as much language, process, domain entities, events, collaborators and tools as possible.

At some point in the interview the conversation will wind down. I like to offer the domain expert the ability to solution at this point. Often they have stewed over a potential solution or better workflow but don't posses the skills required to implement it. Have some questions ready for this time:

- How would you solve x?
- If you could change one thing today what would it be?
- If you had a magic wand what would you change?

Often times this will not lead to a implementable solution, however it may spark an idea down the road of how you could approach the problem. It could also hand you the solution you need, don't dismiss any ideas at this point.

I will add all these questions to a question outline so they are ready for interview day.

## Identifying bias

Creating interviewing questions or preparing for a job shadowing exercise can be a bit of a trap. As developers we have strong thoughts and opinions about our users and our products direction. These thoughts and opinions will impact the people we choose to talk to, the topics we lean towards, the questions we ask and how we listen. Acknowledging our biases before starting any sort of interviewing process is a good first step.

There are a number of common biases to examine prior to entering any period of interviewing. Identifying these biases in ourselves and our team are not just useful for interviewing and job shadowing but can also help us to understand our team dynamics, inter-team communications and product decision influencers.

The main biases I have seen include confirmation bias, survivorship bias, availability bias and social desirability.

#### Confirmation biases
Confirmation bias is the tendency to interpret new evidence as a confirmation of one's exiting beliefs. An example of confirmation bias is someone who holds the belief that left handed people are more creative than right handed people. In confirmation bias this individual would place greater importance on this correlation confirming their bias in their mind every time they met a left handed person who was creative, they would ignore the right handed people who are creative. 

If you start to see questions that can be thought of as confirming an idea or seeking evidence of a belief you are probably in the middle of confirmation bias. Also be cognizant of the tendency humans have to ignore disconfirming information, this is how stereotypes perpetuate.

#### Survivorship biases
During WW2 the US Military was attempting to strengthen the armor on planes. In order to do this they took stock of where the bullet holes on the planes where located and placed more armor in those locations. This is a great example of the problem with survivorship bias. 

The planes hit in the spot where the engineers where putting more armor was pointless because a plane could survive a hit in that location. They later realized they needed to put armor where they were not seeing holes because those planes where not surviving.

We often see similar scenarios in our own interviews, we tend to interview our best customers or heaviest users. This may be helpful from a relationship perspective, but those users needs are mostly being met. Instead we should try to interview the users that abandon our product for another product.

#### Availability Biases

As we go through our day we are bombarded with the current events of our work; support's needs, issues you have been working on, parts of the codebase you wrote etc... Anything that is top of mind can influence how you see or think about a situation. 

This is why if your company just released a shiny new feature you are more likely to suggest it as a possible solution over something that maybe more appropriate that came out 5 years ago simply because it is top of mind. 

#### Social Desirability biases
Anyone being interviewed will be bias toward answering questions in a way that is socially acceptable. When was the last time someone asked you if you test all your code, how did you answer? If you are like most people you don't test all your code, but you said yes, or shaped some story to make it sound like you do most of the time, because you want them to think of you in desirable way. 

This is social desirability bias it is a bit like peer pressure, we have a reason to lie or color the truth because we are trying to align our practices with what we perceive as the socially desired values. 


### How do we interview people without these biases?

Interviewing people is hard, we have to navigate both our biases and the interviewees. Really great interviewers are hard to come by, but not everyone needs to be Terry Gross to get value out of an interview. 

You can learn to follow a mostly formulaic interview process and get good at it. I am often reminded of a statement a friend of mine told me about interviewing, you have 2 ears and 1 mouth try to use them in that proportion. It really is all about listening. 

Most people love to tell stories, if you can get a person into a story telling mode they will usually become fairly honest and straightforward as opposed to people answering questions survey style. 

So how do we conduct such an interview?


# Interviewing

## Location

I tend to prefer comfortable informal interviews, I feel people can be more authentic. You may also choose to simply meet people where they are, sometimes other people in the room can be good as it becomes a case of interviewing a group as people often chime in, other times social pressures can keep people from saying what they really think. In our case, the warranty system is ok to interview in an open context as there are not really pressing feelings involved or social pressure.

To prepare our interviewing space I go through this checklist:

- [ ] At least one note taker.
- [ ] Question we are going to ask.
- [ ] Post it notes and pens.
- [ ] If desired a recording device, make sure this is ok with the interviewee.

## Conducting the interview

There is a common pattern to an interview you can follow to make things more natural, I even put this into a template to remind myself of the steps to take.

The first step in the process is an introduction. In this portion of the interview we need to cover the following three items:

1. Introduce yourself.
2. State your purpose.
3. Obtain consent to continue with the interview.

Once we have done the introduction, I like to ask the interviewee something personal, to ease any tension. Ask them about their day, comment on a unique article of clothing or any personal question that is friendly and easy to discuss. I try to avoid cliche question or topics like the weather as they have grown to lack any depth and don't let the person talk about themselves. If you let the person talk about themselves they will be much more at ease.

On to the questions, at this point we ask the pre-planned questions. I usually have 3-4, ideally these questions should be open ended. When getting answers don't feel like you need to stay on script and make sure to let silence hang a little longer then normal. Often the best interview veers in an unexpected direction naturally as you explore reasons and ideas that are unique to the interviewee and potentially introduce topics or ideas you had not considered.

Once the conversation starts to dwindle I often will ask the users a straightforward question that prompts them to solve their own problem. Questions like how would you fix the situation or how have you dealt with this in another role often prompt the user to offer a solution. This may have value or not, but often is insightful in a different way.

The time has come to conclude our interview, at this point you can thank the participant and exchange pleasantries. Before the interviewee leaves I always like to ask for permission to collaborate in the future. This helps build a pool of domain experts to tap when it come time to test prototypes, validate ideas or collect more information.

## The warranty domain expert interview

It is time to interview our warranty domain expert, Nevin, we walk through our introductions and purpose statement, obtain consent one last time then jump into our questions.

You: Can you tell me about the last warranty you processed?

Nevin: This xl Vision mountain bike has a broken frame, Harrie's bike shop contacted me via email to notify me about the issue. We sent out a new frame once we identified it was a manufacturing defect. I found the frame in a warehouse close to the shop and placed a shipping order with the distribution center. 

There is a lot to unpack in that brief overview. From a note takers perspective we can identify: 

- A high level process: notification of issue -> assessment -> decision of action to take -> shipping arrangement
	- Domain events in this process
	  - Warranty issue received.
	  - Warranty issue acknowledged by employee.
	  - Warranty issue assessed.
	  - Warranty issue resolution proposed
	  - Warranty issue resolution in progress
	  - Warranty resolution offered
	  - Warranty resolution accepted
	  - Replacement product shipment received at warehouse
	  - Replacement product shipped
	  - Replacement product delivered
	  - Warranty issue resolved.
- A number of potential bounded contexts:
  - Bike shop.
  - Manufacturer.
  - External Warehouse.
  - Shipping
- Domain entities
  - Bike, 
      - size: xl 
      - category: Mountain Bike
      - Product name: Vision
  - Bike Shop:
      - Name: Harrie's
      - Shipping address?
  - Warranty notification:

These things could feed our ubiquitous language, expand our bounded contexts, add to our domain events and ultimately inform our implementation. 

### Sidbar: Fidelity in note taking
Depending on how well liked or defined your process is you may want to more fully capture the process. I tend to capture language in a higher fidelity if processes are well defined, liked or efficient. Lower fidelity is better when things are not as well defined, are inefficient or lack in some areas. As Henry Ford once said, if I asked the customer what they wanted they would say a faster horse. Allowing your team room to innovate is a matter often a matter of fidelity, at the point of capture you start to make value decisions of how much you want to replace, be aware of this during your note taking you are already making value judgments. 

In our example we know our system is gravely inefficient, so we want to capture notes that allow for room to improve. If we conducted the same interview in a well loved efficient process, or rigid environment driven by compliance our output should be higher fidelity for the process section. 

> Warranties are received via email then assigned to a warranty manager. The assigned manager then notifies the shop that they are starting work. Next follow up questions are sent to the shop. Once follow up questions are answered, the warranty manager asses the issue and offer a resolution. Given the resolution is accepted any needed parts are then shipped to the shop. Upon receiving the parts the warranty is marked as resolved.

This higher fidelity process outline captures more information about the process. If you are following BDD this could be dropped in as a spec. User stories such as this have their place, we can see the ubiquitous language, identify context boundaries and capture this directly in our code base. However, this level of fidelity offers a solution, which at times can prevent brainstorming pathways we will explore in future chapters. Feel free to use both approaches depending on your requirements.
### End side bar

From the interviewer perspective we can now take this interview in a lot of directions. Since we are looking to rebuild the warranty system from the ground up, the first thing we want to focus on is the warranty notification data.

You: Can you tell me more about how you were notified of the issue and what information you needed to assess this incident?

Nevin: Sure, Harries emailed us about the issue. We require pictures of the bike, pictures of the broken part, the serial number, and a bit of info about how the break occurred. We have an email template we send them to fill in and ask any follow up questions over email. We also ask for a single point of contact with whom to work through the issue with on the shop end to simplify communications. Based on the type of break we assign a category to the issue.

You: This is great would you mind emailing us that template? Can you forward us a few example customer interactions?

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
 
 You: Thanks for all this information Nevin this is amazing. Would you mind if I reach out to you in the future for follow up information or to share ideas with you and get your feedback?
 
 Nevin: That would be great I am really excited to fix this.
 
 You: I am also wondering if you would let me shadow you for an hour or so while you work on some warranties to see what you workflow looks like?
 
## Note taking
 
It is tempting to try to model our database or layout our objects in our notes. Ideally notes will quickly capture ideas and not model things for us. Ultimately we are trying to understand our domain, not figure out implementation details. 

Try to keep your notes short, using post it notes for note taking will encourage this as space is limited. We want to capture just enough information to understand the domain. Notes like:

- Bike, 
  - size: xl 
  - category: Mountain Bike
  - Product name: Vision
  - Serial number

Are preferred to: 

> A bike has a size, category, product name and serial number. Each warranty has a bike and the warranty belongs to a bike shop. 

This is the start of a db model, you will get there eventually but it is far to early in the process to know if what you are doing enforces the domain properly.


# Job Shadowing

Nevin has invited us back to do some job shadowing. In this process we are looking to gain on the ground experience to see all the parts of the process that are often not discussed in an interview because they are so ingrained in day to day activity they seem obvious to the domain expert. 

As an outside party we need to steep ourselves in the world of the domain expert a bit, as what they take for granted maybe completely foreign to us. We may also see extremely inefficient practices that computers could automate, that the domain expert may never recognize as a problem.

## Setup
In a job shadowing exercise we are entering into the workspace of the domain expert. We need to try to set ourselves up to be as un-obtrusive as possible. Often times this means preparing ourselves as humans to be stealth. Have you pens and paper ready, get your coffee in hand or snack and prepare to sit back and be as quite as a mouse, what ever that means for you.

You likely also want to arrange a time when the domain expert is actively undertaking the work you want to observe. Find a time that works well for this observation, ideally they should be moderately busy, meaning not to overwhelmed to answer your questions but busy enough to show some variety.

When you come into their workspace expect there to be a bit of friendly interaction at the beginning and perhaps a bit of awkwardness as they start their day. Starting work is hard enough, doing it while being watched can definitely impact performance. You can try to ease tension by bringing donuts, telling jokes and then slowly receding back. 

## Observation

While observing try to ask as few questions of the observant as possible. I like to take notes of any questions I had and save them for the end. It is normal to have a follow up short interview after the shadowing session. It may also be helpful to have the domain expert explain out loud what they are doing as they undertake their work almost like a stream of consciousness. I tend to reserve this to particularly complex tasks as it can influence their workflow.

There are a few key areas I tend to hone in on when observing a domain expert doing their work. The main 3 are tools, processes and interactions. I find these high level categories I can hone in on and organize my thinking and notes around.

### Tools

Any tooling the domain expert interacts with is helpful to note. Often we are integrating with, replacing or augmenting tools. Having an understanding of what tools are in place, what they are used for, why they where chosen, where they fit in the process and what features are used is often handy to note for later use.

It can also help us to understand were our tooling fits in the broader picture, are these outside system interacting with ours, could they? Should they? Are their patterns or language familiar to the domain expert from these tools that we can co-opt to simplify the environment of the domain expert? Tools in the environment are important to any domain expert, thus they should be important to us as augmenters of the environment.

### Processes

How are entities moving through the environments, what tools are taking inputs, creating outputs. What do these inputs and outputs look like? Is most of the process happening on a computer? Is there physical workspace to consider? 

Most of the workflow we are examining is process, whether or not it is recognized as such or any good. Looking for patterns in the workflow and things that could potentially become patterns is a good thing to note.

This is a great time to outline domain entities, domain events and states that entities could exist in. You may want to actually draw timelines, comics, physical maps or process diagrams to show how things move through the process.

### Interactions

Interactions between different domain experts, processes or tools are all helpful to capture. Is there a point in time where a certain entity transfer to another group in you organization? Does the domain expert need to reach out to other places for information? Does information transfer from one system to another? How are the domain experts entering data into different places?

All these interactions likely point to some piece of tooling you will need to be aware of or consider implementing. Try to map out how entities are moving around in the context bounds and what action is required to move them in an out of these interactions.

### Looking for hacks

This is not one of my top 3 areas for focus, but hacks are really valuable for finding confusing or troublesome parts of a system. If a domain expert has take the time to implement a hack to get around a situation it is likely that they understand something the implementors did not and got frustrated to a point that they fixed it themselves.

Hacks can take many forms, post it notes with directions, macros in excel, browser plugins, copy and past patterns and more. Any thing where the user created a one off custom solution to a problem is worth exploring.

## Observing our warranty process

You: Good morning Nevin, I brought coffee and bagels. How is your day going? 

Nevin: Great now that I have bagels.

You: Everyone loves a bagel, I am going to hang out back here and just observe your warranty routines. Mind if I look around at your space while you get your day started?

Nevin: No problem, if you have any questions just let me know.

You: Thanks

You walk around and note a few computers, a barcode scanner with internet browsing capabilities, label printers and some notes with email addresses for different warehouses holding our products.

Nevin: Hey Jim, I got a new warranty issue want to grab it?

Jim: On it.

You go over and watch Jim follow up on the warranty issue. He double checks that all the needed information is there in the issue, which it is. You take notes of all the items he is looking for in the email, it looks like there is an email template that they use to have shops submit warranties with, you take a note to get this template from them later.

Jim: This looks pretty straight forward, we have seen a lot of these bikes break at this junction. Nevin do we still have any x-large, huff and puff frames left in the west coast wharehouse? 

Nevin: No it will have to come from the east coast. Should take about a week to get to them.

Jim: Ok I will let the shop know and ship it out once they have given the go ahead.

You capture notes about the location of the bike inventory driving delivery needs and dates. Also the process of notifying the shop. You also request that all the emails exchanged be forwarded to you for reference. 

From this exercise we have gained knowledge around a number of areas that didn't expose themselves during the interview. The warehouse inventory came up as did the tools that they use day to day. You could follow up and ask to see how any of these tools are used to try to drive insights into where you could further inject software into their process.

## Developing your ubiquitous language
At this point we should think of things as developing an encyclopedia of institutional knowledge. In fact I would recommend taking on this task at this point. Every interview you undertake should be approached as an opportunity to collect and share very useful domain knowledge that may currently exist in a silo.
 
Every group is different in how they like to communicate. Self describing software, document everything, automatically generated docs there are a lot of preferences in how we communicate amongst our teams. The method of communication is less important then the ability to capture the knowledge you have gained, so I am not going to weigh in on this religious war. If you can build a wiki or some other communication tool that can state what all the domain language is in different parts of your bounded context then you have a communication standard you can reference for new hires, naming things in the future and understanding what user means in the context of sales.

Taking our notes from our interview section we can extract our domain entities, domain events, process and new bounded contexts. We are not at a point were we are writing code yet but we can start to organize our domain further on a domain context map, grouping our entities, events and processes in their proper contexts. 

![](https://www.oreilly.com/library/view/domain-driven-design-distilled/9780134434964/graphics/04fig01.jpg)

Lets augment our previous context map from our stakeholder mapping exercise. Since we have spoken with warranty we identified some outside stakeholder we had not considered prior. The warehouse which houses our replacement parts is a group we will need to work with, the implementation for this group is an unknown at this time, could be an api could be an email workflow, which is what exists today. This is not part of our core domain and thus belongs in its own context. Similarly is the shipping agent, this will live outside our core domain as well. It is likely some other part of the organization, sales, also needs an shipping integration so it will serve us well to look at this as it's own sub-domain.

We can also fill in some information about the bike entities in our core domain and warranty processes inside our warranty sub-domain, warranty could potentially be the core domain from the teams perspective but is not from the business' perspective. Inside the core domain we can add the new bike and bike shop information we have collected:

- Core Domain entities
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

We can begin to fill in some process information in the warranty subdomain:

- A high level process: notification of issue -> assessment -> decision of action to take -> shipping arrangement
	- Domain events in this process
	  - Warranty issue received.
	  - Warranty issue acknowledged by employee.
	  - Warranty issue assessed.
	  - Warranty issue resolution proposed
	  - Warranty issue resolution in progress
	  - Warranty resolution offered
	  - Warranty resolution accepted
	  - Replacement product shipment received at warehouse
	  - Replacement product shipped
	  - Replacement product delivered
	  - Warranty issue resolved.
 
 We also have a warranty subdomain entities:
 
 - Warranty Notifications
 - Warranty Issue
      - Image of the bike
      - serial number
      - Image of the break
      - How the break occurred
      - Point of contact for warranty submitter
      - Break type category
 - Warranty Assigned Manager
 - Warranty Assigned shop 
 - Warranty Discussion

Along with this we have identified two more potential subdomains, shipping and warehousing/inventory. These could be built out in a similar fashion to what we have done with warranty.

This represents the core language, process and ideas in the warranty department as it exists today. I will also often add a list of tools available at this point so I have it for future brainstorming sessions. This may not be a part of what Domain Driven Design offers, but I prefer to look holistically at an environment as the problem space in order to better serve the problem.

- Handheld UPC Scanners, running android
- Cellphones
- Laptops with internet connection
- External Warehouse

There are clearly interconnections between our sub-domains we will explore mapping those out further in a future section.

# Conclusion

We have now collected a strong representation of the domain from the warranty managers perspective. Collecting ideas about how they communicate, work and their environment. This information allows us to think about the warranty environment in a much more informed way then we did prior to the exercise and gives us communication tools that can ease communication friction with stakeholders and also in the code itself. 

We also have a much better long term view of how the code itself may grow and change since we understand the working condition of the warranty lifecycle. This will help us make informed decisions as we build our solution that will keep us from setting up traps based on lack of foresight.

Finally we improved our relationships with key internal stakeholders. This social capital can help us champion our project and improves collaboration which can only improve our project. We have developed a toolset which helps us collaborate in an effective way instead of just complaining about things that are broken.

In the next chapter we will take these things we learned in this chapter and use some design thinkings methods to reflect on the knowledge we have gained.
