# Slide 1

Good Afternoon, everyone, I am Lyon coming from ESDD department. First of all, I want to thank Zhe for having me here today. During this session, I will not share any fundamental knowledge about Skills or something else about AI or Agent because I believe you are all experts in this field. Instead, I want to share my practical experience and thoughts on how to use Skills more efficiently in my daily work.

# Slide 2

I want to start with a question: How do you use Skills in your daily work? Have you ever encountered the following problems?

1. Too many Skills in the community, so you can't find the right one
2. The Skill you found doesn't work out of the box
3. You are afraid to write your own Skill because you don't know how to start
4. The trial-and-error cost is too high(especially when you are using opus)

If you have encountered these problems, I believe you will find this session helpful.

# Slide 3

But to be honest, I think there is no mystery about Skills. A Skill is just a structured prompt. If you can write a prompt, you can write a Skill. If you know how to conduct proper prompt, you can use Skills properly.

The major advantage of Skill is we can share and reuse them because its convention and standard. And I also suggest you to write your own Skill from the simplest thing as long as it can solve your problems.

# Slide 4
Let's talk about the core of this session: Functional Thinking.

The point here is no matter which skills you are using or you are trying to create something new, it is a good idea to apply functional thinking to your work.

The major two principles of functional thinking are single responsibility and composition.

The first one is straightforward: a function does one thing, and does it well. So in skill world, one skill should cover one domain and do it well.

The second principle is more complex in functional programming, but the core idea is complex behavior emerges from composing simple functions. So in skill world, two or more simple skills composed together can be a more powerful skill.

# Slide 5
Here is a case study, let's say you are a developer and you want to review a PR. You can use the following skills to review the PR:

The left one will couple all things together in one skill, it works but not efficient and not easy to maintain.

The right one is a more functional design, it splits the skill into three parts:

1. Where the data source come from and how to fetch it
2. What kind of review criteria should be applied
3. How to process review workflow

Because we are all engineers here or have some technology background, so we can easily understand the difference between the two designs. The right one is more flexible and easy to maintain.

On the other hand, we can make use of the "inference" ability of AI as much as possible to understand our intent and load the appropriate skills automatically.

That's all, it is really simple and practical.

Then I want to share the Skills I used every day in my daily work.

# Slide 6

First, for token efficiency, I use the "caveman" skill to compress the output of the AI. Please note that the skill is focusing on compress on output rather than input. Because the cost of input is much lower than the cost of output.

For coding, basically I used "superpowers" skill pack everyday and it is a really powerful skill pack. It covers the whole development cycle from requirement analysis to code review.

I also recommand you to use "simplify" skill to refactor the code after you write it. Its author is same as oh-my-opencode-slim plugin in OpenCode. And I have already used OpenCode for a while and give up Cursor due to OpenCode is open-source and cheaper with Rakuten In-House LLM.

# Slide 7
For context, I suggest everyone to find or write the appropriate skills to connect your AI Agent with the internal systems you work with. 

Why? Once you do this, you don't need to copy and paste text from here to there anymore and AI Agent can resolve problem on behalf of you.

Here are the skills I used everyday.

For harness, I use "creating-agents-md" skill to update and create the AGENTS.md file. It is the first skill I worte several months ago and I have iterated it several times based on community articles and discussions.

# Slide 8
For knowledge base and memory management, I use these three skills for different purposes:

* "understand-anything" is used to generate knowledge graphs from codebases and documents.
* "using-memvid-cli" is used to save knowledge related to one specific project.
* "using-light-rag" is a skill used together with lightweight RAG framework called LightRAG and retrieve knowledge related to multiple projects and business domains.

Sometimes, I heard people say RAG is dead due to model context window is long enough to store everything. But in reality, we still need RAG to provide the truthfulness of the information by semantic search and vector storage.

# Slide 9

At last, I usually use "Kami" and "html-ppt" skills to create the documents and presentation materials(like this one).

And use the meta skills "skill-creator" and "reviewing-skill" for skill creation tasks.

# Slide 10

Don't forget to follow the functional thinking to design your skills and workflows.

Here are some examples. You can find we can compose these skills to finish a complex task like we have a more powerful skill.

# Slide 11
One takeaway, use your skills like pure functions.

Start from your smallest pain point, write a skill that does one thing well, then compose it and iterate it. And don't forget to share it.

# Slide 12
I will also share some practical tips about how to use AI Agent more efficiently. I will not go deep into the details of these tips because we don't have enough time. But I think the motivation here is really easy to understand.

The first one is you should actively manage the context of your AI Agent rather than keep it as black box. At least, you should know how your context is used for different information:
* are there any duplicate or outdated ones?
* are there any disposable ones?
* whether the prompt is too long and contains too many unnecessary parts?
* whether Agent spend too much time on a single task due to lack of context or tools?

You cannot improve the performance of your AI Agent if you don't know how it works.

The second one is you should use AI as a lever rather than a brain replacement. AI should help you think better and gather information, compare options, execute. You still need to think and make decisions, do not rely on AI to do everything for you and send a prompt then let it go.

The third one is about how to save your budget. Maybe as you know, the Cursor have changed its pricing model from request limit to token usage limit. And I also heard some colleagues run out 500$ budget in one week even 2 days.(It doesn't make sense to me)

AI is awesome, but it is not free. You should use it wisely and save your budget.

The most practical tip is you should use the appropriate model for the appropriate task. Don't nuke every task with the most expensive model, for example, the anthropic opus. In most cases, I believe sonnet is enough even haiku as long as you use them properly.

# Slide 13

That's all, I hope you enjoy this session.

Thank you for your time and feel free to ask any questions you have. 

Thank you!