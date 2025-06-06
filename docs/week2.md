# Week 2: Retrieval-Augmented Generation (RAG)

RAG systems are large language models (LLMs) that are augmented with external knowledge sources such as documents or databases. These systems allow models to access up-to-date or domain-specific information *at runtime*, without needing to retrain the underlying model. 

For example, if you ask a standard LLM, “Who won the World Cup?” it might reply based on 2021 or earlier knowledge. A RAG system, by contrast, can search a structured data source and provide current information. This makes RAG useful for question-answering systems, technical assistants, customer support tools, and more.

## Focus
This week, we will focus on building a minimal working RAG pipeline that connects an LLM with a document-based knowledge store. While RAG systems can get very complex, we’ll focus on understanding and implementing the core components of such pipelines:

- Embedding real documents into vector representations
- Storing those vectors in a searchable vector database (Postgres + pgvector)
- Retrieving relevant chunks of documents at query time
- Passing those chunks into an LLM to generate an answer
- Returning source-aware answers that reference the input documents

## Hands-On Activities
> Note we plan to adapt and tweak the excellent hands-on tutorial at 
[timescale](https://www.timescale.com/blog/how-to-build-llm-applications-with-pgvector-vector-store-in-langchain), using all open source tools.

- Set up a local or hosted Postgres database with `pgvector` support 
  - Potentially Supabase for ease of use
- Ingest and chunk a small document library (e.g., scientific papers, policy documents, or public tutorials (TBD)
- Embed chunks using the OpenAI API or a Hugging Face model
- Store embeddings and metadata in the vector database
- Implement a retrieval function using cosine similarity
- Prompt an LLM with retrieved content to answer user questions
- Display retrieved sources alongside the generated answer to evaluate accuracy. 

## Learning Outcomes
By the end of this week, students will be able to:

- Explain what retrieval-augmented generation is and why it's useful
- Build a basic document ingestion and chunking pipeline
- Compute vector embeddings of text using a transformer-based model
- Store and query embeddings using Postgres (maybe w/Supabase) + pgvector 
- Retrieve relevant documents and use them to prompt an LLM
- Distinguish grounded responses from hallucinations based on citation
- Explain the difference between retrieval (finding relevant chunks) and generation (answering questions based on them).
- Be sure students understand the difference between *retrieval* and *generation*. Retrieval handles finding relevant chunks, generation handles answering the question based on them.
- Swap in their own documents and fine-tune retrieval behavior (this would be a great HW assignment for Week 2, maybe coupled with gradio or streamlit app).


## Resources
- [AWS: What is RAG?](https://aws.amazon.com/what-is/retrieval-augmented-generation/)
- [Timescale RAG Tutorial](https://www.timescale.com/blog/how-to-build-llm-applications-with-pgvector-vector-store-in-langchain)
- [Supabase Blog: OpenAI Embeddings + pgvector](https://supabase.com/blog/openai-embeddings-postgres-vector)
- [LlamaIndex: Understanding RAG](https://docs.llamaindex.ai/en/stable/understanding/rag/)
- [Building RAG with Ollama](https://www.youtube.com/watch?v=GWB9ApTPTv4)

## Instructor Notes
Beware overcomplication and premature optimization: it's tempting to add additional bells and whistles with RAG pipelines, but let's try to really focus on the essentials (the why and the how). 

We’ll want to provide a small curated library of documents, we'll need to think about this (which for lesson, which to recommend for assignment). E.g., public scientific papers or abstracts (e.g., from arXiv). But maybe something more aligned with CTD values, or even CTD curriculum content (maybe CTD course curricula so we could ask questions about specific courses how the curriculum works, etc). This allows students to build a domain-specific assistant that can answer questions about real material they care about.

On the RDS. Supabase setup is the simplest on-ramp to vector storage, but we can think about whether to go with directly setting up a postgres server. It would reinforce DB ideas from Python 100, but mroe real-world (they used sqlite in P100 but that's not an industry standard).  




