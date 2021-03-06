# On the table excercise
Everyone meets the people at their table, exchange 

- Your name
- Why you are here
- Where you work

# Motivation 5 min
I put this workshop together to try to introduce more developers to design thinking processes. It has been my experience while implementing these techniques in multiple teams, including with my team at GitHub, that the ideas, methodologies and approaches presenting in design thinking help developers to:

- Better understand the domain they are developing solutions within.
- Communicate better with stakeholders.
- Create better modeled implementations.
- Create more interesting solutions.
- Create more sustainable solutions that change easier.

I spoke with @risukun about her experience implementing design thinking on a team inside of Home Depot. It was her experience that the team she worked on not only accelerated its development cycle, but it also developed products that more concisely solved the users problem and found that the language her development team used in code more closely resembled that of the teams stakeholders.

Design Management Institute’s ten year study that shows design-centric companies outperforming the S&P 500 by 211%

> "Good design is good business", Tom Watson IBM

# What is design thinking? 5 min
Design thinking is often summed up in steps that allow you to Learn, Understand, Ideate, Prototype and validate solutions. Different approachs or schools of thought will have slightly different terminology for this process but generally people dip their toe in the water by learning a process similar to what we will go through today. 

Todays example will emphasis some aspects that I have found helpful from a programmers perspective that are typically not discussed in these sorts of workshops mainly around shared language and capturing the domain of the user in language and process.

One important thing to emphasis is that todays workshop will show you a very clear process, however any of the pieces of todays overall process can be administered in isolation to improve outcomes, the process is not perscriptive it is more like cooking, different ingredients can be used in different combinations to create different scenarios. 

This will not immediately be a skill that is easy to learn, it is learned over time and honed like a great chef learns how to properly use salt, fat and acid and can identify how much and when to use these features. It all comes with practice and experimentation.

Today we will examine a recipe I have used repeatably with great success I will try to show you how to follow it and then give you direction of where you can go from here if you find this practice useful.

It is important to see that design thinking on it's own is not a useful tool, it is a tool that can greatly increase an existing area of expertise by helping you understand how to better apply your practice to a problem. I often think of it like measuring before cutting, I want to measure the problem space as much as possible and review all the possible cuts I could make before I actually touch the materials I have to work with.

>"The lessons taught at the d.school offer people permission to think differently about problems and solutions. They teach people how to form connections among people of different disciplines that break down silos of knowledge and that lead to unexpected and useful outcomes. This way of work offers many people a new way to see the world — a way that feels much more natural and that dissolves the barriers formed by traditional power dynamics and ineffective workflows." 

> Emi Kolawole
> 
> https://medium.com/stanford-d-school/how-design-thinking-helped-me-learn-to-love-my-discipline-and-the-pursuit-of-mastery-cb172a003eb3

- Double Diamond
https://medium.com/digital-experience-design/how-to-apply-a-design-thinking-hcd-ux-or-any-creative-process-from-scratch-b8786efbf812
- “If I had an hour to solve a problem I'd spend 55 minutes thinking about the problem and 5 minutes thinking about solutions.” - Einstein

# What is Domain Driven Design?
Domain-driven design (DDD) is an approach to software development for complex needs by connecting the implementation to an evolving model.[1] The premise of domain-driven design is the following:

- placing the project's primary focus on the core domain and domain logic;
- basing complex designs on a model of the domain;
- initiating a creative collaboration between technical and domain experts to iteratively refine a conceptual model that addresses particular domain problems.

# Problem introduction 2 min
We are all attending CodeMash so lets explore the space of hosting and running this large conference. We will avoid selecting a particular problem to work on and instead leave that as an excercise of prioritization in the groups. 

# Learn
We will start the day at the begining of our first diamond in the learning or discover phase. We will be interviewing CodeMash volunteers to discuss their work at the conference. 

## How to interview

- What does interviewing mean to you?
- Have someone tell about an interview.
- Remember we have 2 ears and 1 mouth, use them in that proportion.
 

## Quick Guide

- Identify a topic for investigation.
- Prepare your questions and recording equipment.
- Determine your criteria for selecting interviewees.
- Identify the people you will interview.
- Set a time and place to meet them.
- Introduce yourself and the purpose. Obtain consent.
- Start with easy questions, then draw out specifics.
- Resist the urge to fill space with your own context.
- Listen carefully and take good notes.
- Thank each participant.

## Map of an interview:

- May I interview you?
- You are? - Demographics easy questions, warms up things.
- Tell me.... Open ended questions about their experiences
- Digg... we dig for details here of what is good or bad. What, why, etc.
- Imagine a better world section... In a perfect world how would this work?
- Obtain consent to get further information about future work.
- Thank You!

## Helpful Hints

- Try to choose a location with minimal distractions.
- Don’t put words into the interviewee’s mouth.
- Resist the urge to conduct an analysis at this stage.
- Draw out silences, people often add more if you let silence linger

Template: 

https://assets.lumaworkplace.com/resources/files/97/LUMA_Interviewing_8.5x11.pdf?1492622577

# Language collection
Users often have language the use extensively in their field. We have many terms to discuss this jargon, industry speak, slang, etc... People sometimes go into fields and study something for years creating a shared context of language only applicable in their field. 

One of the trickiest things about being a software engineer is that we attempt to build solutions for such a diverse set of expertise that we are often largely unfamiliar with the domain we are operating in. This can lead to miscommunication between un-aligned parties. We play long games of telephone from users, to managers, to designer and maybe down to implementors.

In this process we want to keep an ear out for Nouns, verbs, processes or phrases the interviewee uses. We can often find nomenclature that is very specific to a domain, think industry specific, scientific, etc... Also keep an ear out for generic terms that maybe context loaded, things like user, account, organization are often overloaded terms that are highly contextual.

Identify these terms as you interview and try to capture the words, context they are used in and look for clarification when needed.

- Nouns often map to object or Database entities
- Can you map out any entity relationships?
- Verbs often signify process, how do verbs relate to nouns? Can you capture this?
- Can the verbs be mapped to function in the system?
- Is there a process hierarchy, can you map verbs and nouns into this process? Is it signifying anything important about how you model the domain?
- Is there any language ambiguity? Ask for clarification.
- Can any of this be used in documentation in the codebase?
- Did the interviewee presented a good test scenario?
- Has the interviewee brought up any edge cases?
- Are their verbs or nouns that we could use to help the user navigate any new tooling?
- Is the user presenting any sort of logical hierarchy to processes or entities we should reflect in the tools UI structure? Can these also be captured in code?

When capturing this information it is safe to use all kinds of diagrams, words, trees, tables whatever captures the idea well. 



# A Note on Process Flow
Often times when interviewing people will outline a process to you.
 
1. Found my keys
2. Got in the car
3. Drove to the store
4. Got milk
5. drove home

This is highly generic but hopefully you get the idea. Often when automating manual tasks or augmented common procedures users have a prefered way to complete the task. Understanding their existing workflow can help you better understand a process and how to describe it in code and augment it with tooling.

It is also a good idea to look for goods and bads in the current process, capturing a process is only as useful as the process is good. If we capture a process the user distastes or that has holes in it we maybe automating a bad process. 

This differentation is a tricky line to follow. Often stakeholders are keen to keep nomenclature, process and tools familiar. However, they may also have a distaste for the current. Keeping nomenclature the same while changing process may allow for an easy transition allowing the user to maintain language but changing order for example limits the amount of change being introduced.

# Go interview
Assign one person to be the interviewer, one person to be a note taker and one person to capture language and processes.

Try to capture as much information from the interview as you can. Each idea can be captured on a post it note to keep note small and concise. It is good to draw, write, sketch and journal. Use the method that helps you most effectively capture your ideas.

# Ubiqutious Language and Context Bounding

Often times language has meaning or process has meaning inside a context in particular parts of an organization. For example consumer facing sales may have a different idea of what an account is and what it can do then b2b sales. Another example of bounded context could be that accounting cares about payments in a different way then sales, one dealing with taxes the other commssions.

This is bounded context. Using tools to isolate and differentiate these bounded contexts can help prevent god objects and clarify duplicate language with different meaning.

# Rose Bud Thorn
Members of the Boy Scouts of America frequently use this method to identify one positive experience (Rose), one negative experience (Thorn), and one new goal or insight (Bud). We can employ this method to utilize this method to help focus a set of data and plan next steps.

- Rose = Pink (indicates things that are positive).
- Thorn = Blue (indicates things that are negative).
- Bud = Green (indicates things that have potential).

Put one idea on each sticky note.
Capture as many data points as you can.
Avoid the urge to offer solutions at this point. Write them down and keep them in your pocket.

# Affinity Clustering

Now we have a lot of data points and it may feel like we have some potential areas to work on. But this information is still highly dishoveled and hard to reason about. We need a method to find some order in this chaos.

Affinity clustering is a great tool for finding order in a large set of data points. Gather up your Rose, Bud, Thorn post it notes and we will work through organizing them together.

- Have one person describe, then place, an item.
- Invite others to place similar items in proximity.
- Repeat the pattern until all items are included.
- Discuss and rearrange items as groupings emerge.
- Label the clusters that finally take shape.
- Don’t label the clusters too early. They may shift.
- Look for opportunities to create subgroupings.
- Consider using color to code different types of data.
- Avoid the urge to offer solutions at this point. Write them down and keep them in your pocket.


## A note on Rose Bud Thorn and Affinity clustering

I find these two steps to be incredibly useful in a number of situations. Try folding them into processes you may already have in place and time box them to 30 minutes each. A couple places you may find them incredibly useful are agile retrospectives and incident response meetings.


-- CUT?
# Statement Starters

Now you have a good amount of info, lets frame our problem. We want to use open language that encourages brain storming

- How might we ____
- In what ways might we _____
- How to _____

Compare the statements "How might we" and "How can we", how do they make you feel?


# Ideation
Ideation is the phase in which we come up with possible things to prototype. Lets vote on a few statements for everyone to work on. Put your statement starter on the board and cast a vote for what things we will prototype.


## Creative matrix
If you want to generate many wide-ranging ideas in a short amount of time, the structure of a Creative Matrix is useful because it stimulates cross-pollination by providing a template for generating new ideas where topics intersect. In a Creative Matrix grid, each cell represents the intersection of two disparate categories. It’s best to use the columns as categories related to people (e.g., personas, market segments, or problem statements) and the rows as categories for enabling solutions (e.g., technologies, environments, or policies). You can then use this “mash-up” of categories to help generate a wide range of concepts in each cell.

- Make a poster showing a large grid (max. 5 x 5 cells).
- Designate columns: Categories related to people.
- Designate rows: Categories for enabling solutions.
- Form teams. Hand out grids. Introduce the topic.
- Give each participant a pen and a sticky note pad.
- Ask them to ideate at the intersections of the grid.
- Instruct them to write one idea per sticky note.
- Start the clock. Limit the time to 15-20 minutes.


## Important/Difficulty mapping
Now we have some ideas, let figure out which option to work on. 

- Make a poster showing a large quad chart.
- Label horizontal axis Importance (or Impact).
- Label vertical axis Difficulty (or Cost to Execute).
- Form a team, and gather data for discussion.
- Plot items horizontally by relative importance.
- Plot items vertically by relative difficulty.
- Consider the quadrants where items get placed.
- Look for related groupings, and set priorities.


Switch up the teams, and select prototypes.

# Prototyping

Now it is time to prototype solutions, with your team vote on a possible solution to prototype and build a low fidelity model of your solution. 

What is the lowest cost possible thing you can build to show your idea off? How can you test UI flows and other parts of your solution?


- Assemble a small design team.
- Gather basic materials (e.g., pen, paper, tape, etc).
- Consider what you want to learn from the prototype.
- Select a scenario and a few key tasks to focus on.
- Build a rough approximation of the concept.
- Simulate as much functionality as possible.
- Include some realistic and readable content.
- Provide a signal for the areas that are incomplete.

One person for each team will volunteer to test another teams prototype. Then we will iterate and re-test. Run a basic UI test, discussing with the user what they are doing as they use your prototype. Have them talk through their thought process as they use the prototype. Avoid leading the user with language, setup a scenario and see what they do and why.
 
# Presentations
Everyone shows off their prototypes and talks a little about what they learned in the process.

# Next steps?

- D.School Bootleg for your team https://dschool.stanford.edu/resources/design-thinking-bootleg
- Luma Institute training. https://www.luma-institute.com/
- Luma Workplace https://www.luma-institute.com/products-and-services/luma-workplace/
- Books
	- Design Sprint
	- The Design Thinking Playbook


# Wrap up
Circle time.

- What did you learn today?
- What do you want to do differently after this?
- What was the most surprising thing about this excercise?