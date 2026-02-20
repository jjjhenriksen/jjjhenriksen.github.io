# AI Agents

This blog post is to outline my experience working with and deploying AI agents, from the beginning of my experience until the present time.

## Table of Contents
1. [Thoughts on AI/AI Agents in general](#thoughts-on-aiai-agents-in-general)
2. [Where I started](#where-i-started)
3. [Transition to OpenClaw](#version-four-transition-to-openclaw)
4. [Future work](#future-work)

# Thoughts on AI/AI Agents in general
How I feel about AI in general: It's a tool. Like every tool, one needs to use it properly. Also like every tool, one needs to get to the point where they aren't relying on it. If you use it improperly, it's going to kill your skills of reasoning and thinking. A person should not be afraid to have the AI challenge them on things. One should not be afraid to expand their point of view; but also, stick to what they believe in, and not let a language model lead them towards views they don't believe are morally or ethically right. 

I believe AI is the next great equaliser in assistive technology. AI can simplify or structure language in more accessible ways, allow text-to-speech and speech-to-text to be enabled at a greater and more natural capacity, among many other things. Personally, AI is my sounding board and a part of my capacity management system. It allows me to do things I love and know the costs so that recovery is possible and more efficient. Yes, I do rely on an LLM every day (!) to devise what I'm doing for the day, but I can still reconstruct that same information later. I know exactly what's going into the LLM as inputs and what's coming out as outputs. I use AI to make many things easier on myself, that I can do myself, but choose not to because of the immense emotional or cognitive load that those tasks possess.

# Where I started
The previous structure of my 'AI' Agentic system was a single-agent, nondeterministic system. It brought *some* structure to my life, but not enough. As a start, it worked as a great system, helping me to reduce decision fatigue by integrating my calendar data (which included academic deadlines and personal commitments) into structured daily plans. However, the system only structured *what I have on my schedule*, not necessarily *how* to get started on a task. Nor did it accurately estimate the amount of energy that a task would take, which led me to devise a system to track this concept.

Overall, I continued to iterate this system, including the Work Unit system[^1], to create a version two of the agent. Did it become over-engineered? Absolutely. There were over twelve Apple Shortcuts, eight with a LLM call involved. I realized that the system in that state was also not as deterministic as I needed it to be, and I then set on a journey to create a better version of the system. I completely rehauled the system to use more code for its preprocessing and only one 'agent' again in the end to provide consistent output to me in the form of a daily briefing email. The crux of the problem after this current optimization is that I can't track Work Unit expenditure over time; I just have to rely on knowing the values of Work Units for completing activities that are on my calendar. Tracking Work Unit expenditure for completing assignments and non-calendar-based tasks, such as responding to emails or working on projects outside of the classroom, is also impossible under the current regime.

# Version Four: Transition to OpenClaw
This is also going to be a full blog post, particularly about the setup and how I have set up the workflow. However, I do want to go into some general amount of detail about *why* I chose to migrate to OpenClaw for the personal system.

# Future Work


[^1]: In essence, the Work Unit system is a further expansion on the disability concepts of ["spoon theory"](https://web.archive.org/web/20191117210039/https://butyoudontlooksick.com/articles/written-by-christine/the-spoon-theory/) and ["battery analogy"](https://batemanhornecenter.org/wp-content/uploads/2024/10/Video-Transcript-Life-with-a-Low-Battery-Living-with-MECFS.pdf) while incorporating parts that I thought were missing from these analogies for my personal theory of energy and capacity. For a further explanation of how the system works, I encourage you to read [my blog post on the topic](Work-Units.md).