# Interviewing and Job Shadowing

What better way to learn about a topic then spend time with an expert. In our stakeholder mapping exercise we began to identify different types of users we should communicate with to better understand their working context and challenges. 

By working with these experts we can continue to develop our domain knowledge documents  and better frame the experience of the work environment. The intuitive knowledge we learn from this experience can inform the decisions we make in the future about the product but also inform architecture choices and aid in low level implementation choices like variable naming via our context bounds and associated ubiquitous language.

The first step in interviewing or job shadowing is to pick a topic. Picking a topic will often steer us toward job shadowing or interviewing. I finding interviewing to be a good method for getting insights into general experiences or broad stroke conversations. I often find job shadowing to be a better tool for augmenting and optimizing existing processes. 

## Biases

Creating interviewing questions or preparing for a job shadowing exercise can be a bit of a trap. As developers we have strong thoughts and opinions about our users and our products direction. These thoughts and opinions will impact the people we choose to talk to, the topics we lean towards, the questions we ask and how we listen. Acknowledging our biases before starting any sort of interviewing process is a good first step.

There are a number of common biases to examine prior to entering any period of interviewing. Identifying these biases in ourselves and our team are not just useful for interviewing and job shadowing but can also help us to understand our team dynamics, inter-team communications and product decision influencers.

The three main biases I have seen include confirmation bias, survivorship bias, availability bias and social desirability.

#### Confirmation biases
Confirmation bias is the tendency to interpret new evidence as a confirmation of one's exiting beliefs. An example of confirmation bias is someone who holds the belief that left handed people are more creative than right handed people. In confirmation bias this individual would place greater importance on this correlation confirming their bias in their mind every time they met a left handed person who was creative, they would ignore the right handed people who are creative. 

If you start to see questions that can be thought of as confirming an idea or seeking evidence of a belief you are probably in the middle of confirmation bias. Also be cognizant of the tendency humans have to ignore disconfirming information, this is how stereotypes perpetuate.

#### Survivorship biases
During WW2 the US Military was attempting to strengthen the armor on planes. In order to do this they took stock of where the bullet holes on the planes where located and placed more armor in those locations. The problem with this approach was text book survivorship bias. 

The planes hit in the spot where the engineers where putting more armor was pointless because a plane could survive a hit in that location. They later realized they needed to put armor where they were not seeing holes because those planes where not surviving.

We often see similar scenarios in our own interviews, we tend to interview our best customers or heaviest users. This may be helpful from a relationship perspective, but those users needs are mostly being met. Instead we should try to interview the users that abandon our product for another product.

#### Availability Biases

As we go through our day we are bombarded with the current events of our work. Support needs, issues you have been working on, parts of the codebase you wrote etc... Anything that is top of mind can influence how you see or think about a situation. 

For example if your company just released a shiny new feature you are more likely to suggest it as a possible solution over something that maybe more appropriate that came out 5 years ago simply because it is top of mind.

#### Social Desirability biases
Anyone being interviewed will be bias toward answering questions in a way that is socially acceptable. When was the last time someone asked you if you test all your code, how did you answer? If you are like most people you don't test all your code, but you said yes regardless because you want them to think of you in certain way. 

This is social desirability bias it is a bit like peer pressure, we have a reason to lie or color the truth because we are trying to align our practices with what we perceive as the socially accepted values. 

### How do we interview people without these biases?

Interviewing people is hard, we have to navigate both our biases and the interviewees. Really great interviewers are hard to come by, but not everyone needs to be Terry Gross to get value out of an interview. 

You can learn to follow a pretty formulaic interview process and get good at it. I often am reminded of a statement a friend of mine told me about interviewing, you have 2 ears and 1 mouth try to use them in that proportion. It really is all about listening. 

Most people love to tell stories, if you can get a person into a story telling mode they will usually become fairly honest and straightforward as opposed to people answering questions survey style. 

So how do we conduct such an interview?

## Asking for permission.

The first thing we need to do in conducting an interview is to seek permission from the participant. Seeking permission often takes setup, this is a good time to set expectations. Why are you interviewing people, how will the interviewee be compensated, how many people are you interviewing, where will the interview take place, what will you talk about with them, will you be recoding, who else will be at the interview and any other relevant information is nice. When setting expectations you want to be clear about what you are doing, but don't get to specific. You can start to color response even before you have an interview.

Expectations are also dependent on whom you are talking to. Internal users may have insight into what you are working on, while external users may not. Be sure to consider what is appropriate to share or expose in an interviewing process before releasing your companies hot new feature months before it comes out.

## Interviewing
Now the fun part, the interview. I like to make sure a few things are in place before I conduct an interview. 

1. A comfortable location with snacks is always nice to have.
2. At least one note taker.
3. An outline of the questions you want to ask.
4. Post it notes and pens. 
5. If desired and ok with the interviewee a recording device.

Next we need to write our questions, an easy way to do this is to use a question starter that encourages story telling. Story telling is the preferred method for interview responses as stories tend to be more organic. Survey style questions tend to impart an answer shaped by bias.

A great question starter is tell me about, this encourages dialog. Other good questions to ask can include:

- If you had to change one things what would it be? Why?
- Have you done x differently in the past?
- What do you tell new co-workers when they start?

Once you have a dialog going, clarifying questions can be used to shed light on the conversation and add priority. 

- If you had x how frequently would you have used it in the past 6 months?
- Just be be sure I am clear if you had x, what would it allow you to do that you cannot do now?
- Tell me more about why you prefer the competitors feature over ours.
- If a genie granted you 2 wishes about the current situation what 2 things would you fix?

### The shape of an interview

There is a common pattern to an interview you can follow to make things more natural, I even put this into a template to remind myself of the steps to take.

The first step in the process is an introduction. In this portion of the interview we need to cover the following three items:

1. Introduce yourself.
2. State your purpose.
3. Obtain consent to continue with the interview.

Once we have done the introduction, I like to ask the interviewee something personal sort of like an ice breaker to ease any tension. Ask them about their day, comment on a unique article of clothing or any personal question that is friendly and easy to discuss. I try to avoid cliche question or topics like the weather as they have grown to lack any depth and don't let the person talk about themselves. If you let the person talk about themselves they will be much more at ease.

On to the questions, at this point we ask the pre-planned questions. I usually have 3-4 these should be open ended, don't feel like you need to stay on script. Often the best interview veers in an unexpected direction naturally as you explore reasons and ideas that are unique to the interviewee and potentially introduce topics or ideas you had not considered.

Once the conversation starts to dwindle I often will ask the users a straightforward question that prompts them to solve their own problem. Questions like how would you fix the situation or how have you dealt with this in another role often prompt the user to offer a solution. This may have value or not, but often is insightful in a different way.

Finally we conclude our interview, at this point you can thank the participant and exchange pleasantries. Before the interviewee leaves I always like to ask permission to collaborate again in the future. This sets up the user for future interviews but also gives us a pool of domain experts to tap when it come time to test prototypes of validate ideas.


### Avoid yes no questions

It is always tempting to ask a question that the interviewee can answer yes or no to, however these are often the most bias answers and do not really offer any unique insight. If you are tempted to ask a yes/no question see if you can re-phrase the question in such a way that the answer ends up telling a story, explaining a process or exploring the reason a choice is made.


## Capturing language, process and events

Often times we think we need to define the domain language, however the domain language is currently being spoken everyday. Our job is rather to extract, contextualize and define it in such a way that it is easy to reference and share.

As we interview domain experts we have an opportune time to work on extracting their language and better understand it. When conducting an interview I recommend having the note taker write down any specific vocabulary that is discussed. Note any terms that are vague or overloaded and ask the interviewee to explain what they mean when they say x. Capture each of these terms so can later add them to our context boundaries and define them in the glossary.

## Job shadowing

Job shadowing is a tool to reach for when we are working on a very well defined process that we are looking to augment or change. I have approached this in two distinct ways with success. The first is silent observation, the second is engaging directly with the task and discussing it with the domain expert.

Silent observation of someone doing a task can show you how they do a task day to day in a pure way. In this scenario you want to limit your exposure to the participant as much as possible. Don't ask questions, don't get in there way, maybe even consider spying on them when they don't know you are watching. The purer the experience the less bias you impose on their performance.

When engaging in the activity, you get a different outcome. I like to approach this as if someone was training me to start a new job. Go through the actions of learning how to do the task. Ask questions, why do we do this, where does this go, how did this come to be? You are trying to clearly understand an entire workflow and get to know intimately why the decisions where made that lead to the current process.

In either of these approaches you need to take extensive notes on workflows, conversations that occur between stakeholders, the materials being passed around or used, tools available and flow of information between contexts.

### Look for the hacks
One thing to pay particular attention to are the hacks around the workspace. Sticky notes of keyboard shortcut, codes or steps are a good hint that a process is hard or confusing. Taking documents into and out of multiple programs can show formatting errors. I have even seen upc hacking to fix problems with upc numbers between factories. These are often low hanging fruit with a large impact.

### Capturing processes
There are a lot of ways to capture processes as you work through the job. Workflow process diagrams can show how different entities flow through the system and can capture language used to describe each step. We can also capture domain events that occur between each step of the workflow.


