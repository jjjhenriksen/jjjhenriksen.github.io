# Transition to OpenClaw

This is sort of an offshoot of [my post about AI Agents](AI-Agents.md). 

## Table of Contents
1. [Why OpenClaw?](#why-openclaw)
2. [Setup](#setup)
3. [Introducing the Fleet](#introducing-the-fleet)

# Why OpenClaw?
From my blog post about [AI agents in general](AI-Agents.md): 
> OpenClaw has **native local provider support** as long as the 'API' in question supports either OpenAI or Anthropic specs, specifically including [documentation on how to use Ollama](https://docs.openclaw.ai/providers/ollama) with its documentation on how to access other providers. I already have used and experimented with Ollama in the past, which made me inclined to use it as my model provider for OpenClaw. OpenClaw is also **open source**, so I don't have to worry about a company taking my data (highly likely, look at the Discord ID verification data breach), or simply refusing to provide the product anymore if they find it unprofitable (highly unlikely). I can simply copy the repository and run it locally without any connection to the internet for sensitive information. I also wanted to experiment with using skills and tools with frontier LLMs, and OpenClaw conforms to the [AgentSkills spec](https://agentskills.io/home), which gives me a lot of references to build off of for custom skills. 

There are other reasons beyond these for my transition from Shortcuts-based automation to OpenClaw:
1. [The availability on-demand of new and revised information from internet search](#new-information-on-demand)
2. [Being able to re-run the matrix with a single command, calculating information 'in-real-time' compared to relying on completely deterministic systems](#real-time-telemetry)
3. [Agent specialization: Distinct agents handle routing, execution, research, communication, etc.](#agent-specialization)
4. [Direct conversational control instead of indirect trigger or automation-based workflows.](#direct-control)
5. [Using tools and skills to execute on my behalf, instead of waiting for me to have the cognitive effort required to execute](#tools-and-skills)

## New Information, On-Demand

## Real-Time Telemetry

## Agent Specialization

## Direct Control

## Tools and Skills
What really brought me to wanting to use OpenClaw was the availability of being able to use **tools and skills.** Claude Code/Claude Cowork really revolutionized agentic AI with the introduction of skills. Now that the AgentSkills spec itself is open-source and model agnostic, I can do anything at the touch of a button with OpenClaw without paying insane amounts of money for a Claude subscription. This enables direct execution of complex tasks through reusable capabilities, allowing actions to be performed immediately and programmatically while maintaining flexibility, portability, and cost control.

# Setup
The setup process is fairly simple:
1. [Implementing Tailscale](#implementing-tailscale)
2. [Download and setup OpenClaw](#download-and-setup-openclaw)
3. [Add the rest of the agents](#add-the-other-agents)
4. [Implement local models and model routing](#implement-local-models--model-routing)

## Implementing Tailscale
Since the computer I'm using to run OpenClaw is not my primary machine, I used [Tailscale](https://docs.openclaw.ai/gateway/tailscale) to SSH to the secondary machine for setup. I have physical access to the computer itself so I'm able to use it to double-check configs and otherwise manage my agents, but the advantage of this setup is that my computer doesn't have to be online 24/7 for my agents to be online 24/7. I can access their tools and capabilities from everywhere.

It's also a lot easier to set everything up using SSH if you're able to access your files and documentation on one machine without having to copy it to the other. 

## Download and setup OpenClaw

## Add the other agents
Setting up my agents was the easy part after I got the first one online. 

## Implement local models / model routing

# Introducing the Fleet