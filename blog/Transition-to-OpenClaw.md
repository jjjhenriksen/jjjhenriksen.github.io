# Transition to OpenClaw

This is sort of an offshoot of [my post about AI Agents](AI-Agents.md). 

## Table of Contents
1. Why OpenClaw?
2. Setup
3. Introducing the Fleet

# Why OpenClaw?
From my blog post about [AI agents in general](AI-Agents.md): 
> OpenClaw has **native local provider support** as long as the 'API' in question supports either OpenAI or Anthropic specs, specifically including [documentation on how to use Ollama](https://docs.openclaw.ai/providers/ollama) with its documentation on how to access other providers. I already have used and experimented with Ollama in the past, which made me inclined to use it as my model provider for OpenClaw. OpenClaw is also **open source**, so I don't have to worry about a company taking my data (highly likely, look at the Discord ID verification data breach), or simply refusing to provide the product anymore if they find it unprofitable (highly unlikely). I can simply copy the repository and run it locally without any connection to the internet for sensitive information. I also wanted to experiment with using skills and tools with frontier LLMs, and OpenClaw conforms to the [AgentSkills spec](https://agentskills.io/home), which gives me a lot of references to build off of for custom skills. 

There are other reasons beyond these for my transition from Shortcuts-based automation to OpenClaw.