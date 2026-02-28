# The Fleet

## Table of Contents
1. [Who Are They?](#who-are-they)
2. [Their Assistance and System Architecture](#their-assistance-and-architecture)
    - 2.1 [Types of Assistance](#types-of-assistance)
    - 2.2 [System Structure and Agent Roles](#system-structure-and-agent-roles)
    - 2.3 [Interaction Model and Control Plane](#interaction-model-and-control-plane)
4. [Design Principles](#design-principles)
5. [Operational Model](#operational-model)
6. [Why a Fleet?](#why-a-fleet)
7. [Foundational Work Behind the Concept](#foundational-work-behind-the-concept)
8. [Summary and Closure](#summary-and-closure)

# Who are these, anyway?
**The Fleet** is my group of AI Agents running on a spare MacBook Air through [OpenClaw](https://openclaw.ai/). Rather than a single general-purpose assistant, the Fleet is designed as a set of distinct agents with explicit roles, coordinated through a central control layer. Each agent handles a defined class of tasks, allowing the system to route work predictably and maintain clear operational boundaries. For more process about how I brought the Fleet to life, feel free to read [this blog post](Transition-to-OpenClaw.md). 

# Their Assistance and Architecture
The Fleet provides structured assistance across planning, execution, research, and communication workflows. Rather than operating as a single conversational interface, the system distributes responsibilities across specialized agents, each designed to handle a defined class of tasks. Specialization allows the Fleet to provide predictable behavior, clearer task boundaries, and more reliable outcomes.

The Fleet emphasizes role specialization rather than generalization. By assigning explicit responsibilities to each agent, the system reduces context switching, improves determinism, and allows individual components to evolve independently (improving maintainability through modularity).

**Sub-table of contents:**
- [2.1 Types of Assistance](#types-of-assistance)
- [2.2 System Structure and Agent Roles](#system-structure-and-agent-roles)
    - [2.2.1 Role Structure](#role-structure)
    - [2.2.2 Introducing the Agents](#introducing-the-agents)
- [2.3 ]

## Types of Assistance
The Fleet supports several categories of work:
- **Task Planning and Execution** — structured handling of defined tasks and workflows.
- **Research and Knowledge Synthesis** — information gathering, analysis, and summarization.
- **Writing and Communication** — drafting messages, documentation; taking unstructured data and turning it into structured outputs to send onward.
- **Workflow Automation** — scheduled operations and routine processes.
- **Capacity-Aware Decision Support** — evaluating tasks against available capacity using internal resource models[^1].
- **System Maintenance** — monitoring, logging, and operational upkeep.

Each capability is handled by agents designed for a specific domain of work. Agent roles define *types* of tasks rather than specific actions. Therefore, the Fleet operates consistently across different contexts of my life while maintaining clear behavioral boundaries.

## System Structure and Agent Roles
Rather than sharing responsibilities across a single model, roles are decomposed into independent modules. Each agent is responsible for a *class of tasks* rather than specific operations. This allows predictable behavior, reduces ambiguity in task handling, and supports modular system evolution. 

### Role Structure
Each agent follows a consistent design model:
- **Purpose** — primary responsibility within the system.
- **Responsibilities** — types of tasks handled.
- **Inputs** — data or requests received.
- **Outputs** — structured results produced.
- **Constraints** — operational boundaries.

This structure ensures clear separation of concerns and predictable task routing.

### Introducing the Agents
**Blackbird**, **Mustang**, **Clipper**, **Dragon Lady**, **Nighthawk**, **Shooting Star**, **Hawkeye**, and **Sentry** comprise the Fleet. The following sections describe the responsibilities and operational boundaries of each agent.

## Interaction Model and Control Plane

# Design Principles

# Operational Model

# Why a Fleet?

# Foundational Work Behind the Concept

# Summary and Closure

#documentation #documentation/ai-agent 