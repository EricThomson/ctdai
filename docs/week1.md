# Week 1: Introduction to LLMs
Week 1 will introduce students to AI, with a focus on large language models (LLMs). We will cover foundational concepts in modern NLP, how transformer-based models work, and how to use commercially available APIs such as OpenAI's. Students will build their own chatbot, and we will introduce them to LangChain and Ollama for local models. 

## Learning Outcomes
By the end of this week, students should be able to:

1. Explain what LLMs are and how they differ from earlier NLP models, and why language models have become so much more powerful recently. 
2.  Use OpenAI’s API to send prompts and get responses
3.  Apply basic prompt engineering principles to improve model output
4.  Understand and visualize vector embeddings of text to understand semantic relations
5.  Build a basic chatbot interface using the OpenAI API
6.  Understand what LangChain is and how it interfaces with LLMs
7.  Run an LLM locally using Ollama
  
## Lesson outline
1. General background
    - How do LLMs fit into the wider ML/AI landscape.
    - What happened? Why was there an LLM explosion?
    - Basic architecture of LLM models
      - Conceptual overview of GPT models (including measures of semantic similarity)
      - Pretrained models vs fine-tuning
2.  Working with OpenAI API
    - Understanding roles (system/user/assistant roles)
    - Parameters (temperature, max tokens, etc) 
3.  Prompt engineering
    - Zero-shot, few-shot, chain-of-thought prompting.
    - Prompt templates  
4. How to build a chatbot
5.  Ollama: running models locally (installation and usage)
6.  LangChain intro
    - What is it, why is it useful.
    - How to use it to interface with different APIs
    - LCEL (langchain expression language)
    - Interfacing Ollama with LangChain
  
## Hands-On Activities
1.  Learn the basics of the OpenAI API
  - Build ChatBots with different personalities and aims
2.  Run a model locally using Ollama 
3. Use LangChain to build a prompt chain
4.  Compare using plain OpenAI/Ollama API call vs. LangChain wrapper


## Resources
- [OpenAI API documentation](https://platform.openai.com/docs/)
- [LangChain quickstart](https://docs.langchain.com/docs/get-started/)
- [Ollama setup guide](https://ollama.com/)
- [DeepLearning.ai prompt engineering class](https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/)

## Instructor Notes
While all of our students have used AI, this is going to be their first exposure to LLMs from a technical perspective. They will have had some ML background in Python 200 (and some neural networks), so this will dovetail with that nicely. 
