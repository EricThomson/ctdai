# Week 3: Agents
Instead of just responding to user input, an agent can receive a goal, break it down into steps, select tools to accomplish those steps, and iteratively observe the outcomes. This process is known as the *agent loop*, often implemented using the *ReAct* pattern (Reasoning + Acting). It enables LLMs to alternate between *thinking* (deciding what to do next) and *doing* (calling a tool, reading output, updating the plan).

We’ll begin by exploring what agents are, when and why they’re useful, and what distinguishes them from more static workflows like standard prompting or RAG. From there, we’ll build up a minimal agent in Python. Then we'll introduce agent frameworks like [smolagent](https://github.com/smol-ai/smol-agent) and [LlamaIndex](https://docs.llamaindex.ai/en/stable/examples/agent/react_agent/) to show how these abstractions can make designing agents easier.

The centerpiece project for the week is a *Data Analysis Research Assistant*: an agent that can answer questions about a dataset by planning multi-step actions such as loading a file, calling pandas or matplotlib functions, and reporting results back to the user.

## Learning Outcomes
By the end of this week, students should be able to:

1. Explain what AI agents are, and nature of the ReAct agent loop
2. Describe when agents are preferable to simple LLM or RAG workflows
3. Build a minimal working agent from scratch in Python (a data analysis research assistant)
4. Demonstrate how third-party frameworks can aid in the creation of AI agents:
     - Demonstrate this using both smolagent and Llamaindex frameworks to help with the analysis research assistant.

## Lesson outline
1. Intro to AI Agents. 
    - What is an Agent? 
    - What is the ReAct (Reasoning + Acting) agent loop?
    - Why use agents instead of plain LLM calls or RAG?
    - How do agents use tools to solve problems step by step?
2. Build an analysis research assistance agent from scratch using Python.
   - Adapt lesson from workshop at Triangle AI Summit (Reifschneider):
   - Limit the number of tools available just to keep it simple:
      - E.g., Matplotlib, pandas, numpy, filesystem access.
3. Build a similar agent using smolagent/Llamanindex to show frameworks in action.
   - Adapt lesson from huggingface agent tutorial. 

## Hands-On Activities
1. Build a minimal agent from scratch (LLM wrapper, tool registry, loop engine): something adapted from the [Agents Workshop](https://ai.duke.edu/triangle-ai-summit/) at Triangle AI Summit (lead by Jon Reifschneider).
2. Use smolagent to replicate and enhance the same logic with lightweight framework support.
3. Use LlamaIndex's ReActAgent to illustrate a more advanced framework
4.  Potential assignment: Agentic RAG, or add additional tools (plotly, scipy, scikit-learn, pytorch for a challenge). 

For 2-4, we will adapt materials from the excellent [hugging face agents course](https://huggingface.co/learn/agents-course/).



## Resources
- [ReAct (Reasoning/Acting)](https://react-lm.github.io/)
- NB from [Triangle AI Summit Agents](https://ai.duke.edu/triangle-ai-summit/) workshop. 
- [Hugging Face Agents Course](https://huggingface.co/learn/agents-course/)
- [smolagents GitHub](https://github.com/huggingface/smolagents)
- [LlamaIndex ReAct agent example](https://docs.llamaindex.ai/en/stable/examples/agent/react_agent/)

## Instructor Notes
Err on the side of simplicity: less is more. If students walk away with a working mental model of the agent loop, and can build a minimal example, that’s a success! *Resist the temptation to add complex features to this lesson.*

We should equip agents with a small number of tools to avoid overwhelming students (and agents). Stick to tools with more easily debuggable outputs (math, filesystem, basic pandas/matplotlib) to aid our debugging of tools and agent logic. We want to spend our time debugging agents, not the tools.  

When building practical lessons, it will be good add in brainstorming questions -- let students think about agentic tools they would like to build: students love thinking about the possibilities with agentic ai. 
  
Some additional considerations (e.g., things to add in a longer course, or practicum, or for assignments): 

- Monitoring and evaluation:  -- not included in core lesson but worth discussing somewhere. 
- Multi-agent workflows: we should discuss this cutting-edge case in lesson, even if we don't have practical code example.
- MCP (Anthropic Model context protocol): we can mention briefly as potentially useful API
- LangGraph: powerfuly but likely too complex a framework for a single introductory  week. Probably worth mentioning.



