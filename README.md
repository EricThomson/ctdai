# Code the Dream AI Workspace
A workspace to develop hands-on, accessible AI teaching materials for [Code the Dream](https://codethedream.org/). This informal space is for experimenting with lesson plans, identifying core skills, and creating learning paths for Python 200 and AI modules. Student facing-material will be hosted at Code the Dream. 

One goal is to create a modular “basis set” of AI tools and concepts — not to cover everything -- but to give students enough foundational knowledge and confidence to pick up new tools on their own.

This repo contains multiple notebooks to introduce core skills in a modular way. Early lessons focus on one core idea or tool at a time (the “toolkit”). We then pull these pieces together into more complex, project-driven workflows — such as RAG pipelines and AI agents.

The modular design ensures flexibility, allowing us to adapt, add, or remix content as tools evolve.

# Modular toolkit
These are the draft notebooks that introduce key tools, ideas, and mental models. The first few are intended to be taught in order. Others can be slotted in as needed. 

> Some of the following are just stubs, some are more developed but have significant TODO's

| Notebook Name         | Description |
|-----------------------|-------------|
| `01_hello_ai`         | Set up the OpenAI API, securely store your API key, and test it by generating a response using `gpt-4o-mini`. A friendly "hello world" for AI. |
| `02_prompts_to_chats` | Learn the basics of prompt engineering and role-based message formatting. Ends with building a simple chatbot using the OpenAI API. |
| `embeddings_intro`    | Visualize and explore text embeddings using PCA and cosine similarity. An intro to how LLMs represent meaning. |
| `ollama_intro`        | Install the Ollama server and run large language models locally on your machine without needing an external API. |
| `huggingface_intro`   | Get started with Hugging Face tools, models, and datasets. Learn how to use them locally or in the cloud. |
| `langchain_intro`     | Learn the basics of LangChain and how to use it to build more complex, modular LLM-powered applications. |

# Projects
These are more than just modular intros — they start to combine tools and ideas. These will ideally give students a taste of how real-world LLM applications work, and provide the basis for more practical applications.

> The following are just stubs with no content

| Notebook Name         | Description |
|-----------------------|-------------|
| `rag_intro`           | Introduction to Retrieval-Augmented Generation (RAG). Use when your AI needs access to external knowledge or documents. |
| `agents_intro`        | When your AI needs to *do* things, not just *say* things. Learn about agents that can act autonomously via tools and software. |

## Additional considerations
AI literacy is essential. Students should understand the basics of how LLMs work and what their limitations are, and the significant ethical dimensions of this work. We won’t have time to dive deeply into all these issues, but they should be acknowledged and incorporated into discussion, reflection, or light assignments. Some key points to cover: 

- LLMs are trained on vast internet data — this introduces *bias*, misinformation, and uneven quality.
- Ethical concerns include fairness, access, environmental impact, and explainability (there is a good overview of ethical considerations [here](https://libguides.amherst.edu/c.php?g=1350530&p=9969379)). 
- Many public discussions of AI are full of hype. Students should be equipped to think critically when people make outlandish claims (e.g., about AGI). This requires that they understand how the models work -- at least at a coarse level. 
  - Students should have a general grasp of concepts like transformers, attention mechanisms, and the strengths/limits of LLMs (e.g., text vs. visual reasoning).


## TO DO
- Think about how to integrate larger "capstone" projects.
- What notebooks are missing? Are there any we should cut? 
- Consider adding brief assignments or discussion prompts to each notebook
- Build simple project templates for student teams

## Installation
Built using uv. To install the dependences you can use `uv.lock` or `requirements.txt` (`pip install -r requirements.txt`). Please ask if help needed (expand on this more)...

> I have pytorch installed w/cuda 12.6, so you might need to mess with that on your system (see https://pytorch.org/get-started/locally/).
