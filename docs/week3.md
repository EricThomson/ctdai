# Week 3: Agents
With agents we move beyond the case of LLMs simply responding to user inputs and doing what they are told. With agents, LLMs become capable of building plans, choosing from among a suite of tools to carry out those plans, and observing the results of those actions in a continuous feedback loop (the agent loop). This loop — often referred to as **ReAct** (Reasoning and Acting) — allows LLMs to alternate between *thinking* (e.g., choosing what to do) and *doing* (e.g., calling a tool, observing output, updating plan).

In Week 3 of the AI module, we'll start by asking why agents are useful, then explore the standard agent loop and how to implement a basic agent from scratch using Python classes. Students will then explore agent frameworks like [smolagent](https://github.com/smol-ai/smol-agent) and [LlamaIndex agents](https://docs.llamaindex.ai/en/stable/examples/agent/react_agent/) to understand how tools and abstractions can simplify agent development.

The main project this week is to build a *Data Analysis Research Assistant*. Students will create an agent that can answer questions about a dataset by planning multi-step actions such as loading a file, calling pandas or matplotlib functions, and explaining the results to the user.

## Focus
- Why use agents instead of plain LLM calls or RAG?
- What is the ReAct (Reasoning + Acting) agent loop?
- How do agents use tools to solve problems step by step?
- How can we build an agent from scratch using Python classes?
- What benefits do agent frameworks like smolagent and LlamaIndex offer?
- How can we build a small agent that assists with data analysis using tools like pandas, matplotlib, and filesystem access?

## Hands-On Activities
- Read and discuss the first two chapters of the Hugging Face [Agents Course](https://huggingface.co/learn/agents-course/intro)
- Step through a simplified ReAct agent loop on paper: given a question, brainstorm how the agent would reason, select a tool, observe output, and repeat
- Build a basic agent from scratch using Python classes (LLM wrapper, tool registry, loop engine)
- Integrate tool use into the scratch agent — for example, a calculator or text summarizer [use joe's as example]
- Use smolagent to rebuild the same logic with a lighter, framework-supported structure
- Optionally, try LlamaIndex's ReActAgent for a more advanced framework with memory and tool abstraction
- Project work: create a simple agent that loads a CSV file, explores data using pandas and matplotlib, and answers user questions by planning actions across multiple tools

## Learning Outcomes
By the end of this week, students will be able to:

- Explain the purpose and structure of the ReAct agent loop
- Describe when agents are preferable to simple LLM or RAG workflows
- Build a minimal working agent from scratch using Python classes
- Register and call tools dynamically from within an agent loop
- Use smolagent to simplify the creation of an agent with tool usage
- Optionally use LlamaIndex to explore more advanced agent capabilities
- Build a small research assistant that uses tools like pandas and matplotlib to analyze datasets and explain findings step-by-step

## Resources
- Hugging Face Agents Course (Modules 1–3): https://huggingface.co/learn/agents-course/
- smolagent GitHub: https://github.com/smol-ai/smol-agent
- LlamaIndex ReAct agent example: https://docs.llamaindex.ai/en/stable/examples/agent/react_agent/
- ReAct paper (optional/advanced): https://arxiv.org/abs/2210.03629

## Instructor Notes
Avoid overwhelming students with full framework complexity; start small with 2–3 tools max. We want to learn the basic pattern. The scratch agent should be minimalist — class-based but readable, focusing on chaining reasoning + action
We should be ready to troubleshoot pandas/matplotlib usage within tool calls — agent execution errors will often be tool-related, not LLM-related. Start with simple tool calls that we can debug. 

We should probably have students work in groups. Debugging agent behavior is easier with two brains. 
