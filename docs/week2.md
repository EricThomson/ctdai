# Week 2: Retrieval-Augmented Generation (RAG)
Retrieval-Augmented Generation (RAG) systems are large language models (LLMs) that are augmented with external knowledge sources such as documents or databases. These systems allow models to access up-to-date or domain-specific information *at runtime*, without needing to retrain the underlying model.

For example, if you ask a standard LLM, “Who won the World Cup?” it might reply based on 2021 or earlier knowledge. A RAG system, by contrast, can search a structured data source and provide current information. This makes RAG useful for question-answering systems, technical assistants, customer support tools, and more.

## Focus
This week, we will focus on building a minimal working RAG pipeline that connects an LLM with a document-based knowledge store. While RAG systems can get very complex, we’ll focus on starting simple and understanding and implementing the core components of such pipelines. Our plan is to build up in complexity in three steps:

### Step 1: Minimal Naive RAG Implementation 

Start with the absolute basics, implementing RAG from scratch:
- Load 1–2 PDFs using `pypdf`
- Extract full text
- Perform basic keyword matching (e.g., `if query in doc`)
- Pass matched content into the LLM via a simple prompt

Here we will emphasize:
- The core concept of RAG: retrieving information from an external data store and injecting it into the model’s prompt to generate better answers. This works, but has limitations.
- The limitations of naïve RAG include the retrieval step’s inability to handle synonyms, lack of scalability with larger datasets, and absence of filtering or ranking by relevance.

### Step 2: Basic Semantic RAG
Address the limitations of the minimal RAG implementation by introducing:
- Document chunking (e.g., with `RecursiveCharacterTextSplitter`)
- Embedding chunks using OpenAI or Hugging Face models
- Storing and querying chunks in a vector store (e.g., FAISS)
- Retrieving top-k relevant chunks using semantic similarity

We’ll use resources such as [Nir Diamant’s minimal RAG example](https://github.com/NirDiamant/RAG_Techniques) to demonstrate this workflow.

### Step 3: Scalable RAG with pgvector
Build a full pipeline using Langchain that includes:
- Postgres vector storage (either local Postgres or Supabase)
- Metadata storage and retrieval
- Multi-document libraries
- Scalable, production-aligned workflows

We will adapt and tweak the [excellent tutorial from Timescale](https://www.timescale.com/blog/how-to-build-llm-applications-with-pgvector-vector-store-in-langchain), which uses all open-source tools.

## Hands-On Activities
- Run the minimal RAG example from scratch (no embeddings, no DB)
- Discuss its limitations and transition to Nir Diamant's semantic RAG notebook
- Set up a local or hosted Postgres database with `pgvector` support (Supabase recommended for ease of use)
- Ingest and chunk a small document library (e.g., scientific papers, course materials, etc.)
- Embed chunks using the OpenAI API or a Hugging Face model
- Store embeddings and metadata in the vector database
- Prompt an LLM with retrieved content to answer user questions
- Display retrieved sources alongside the generated answer to evaluate accuracy

## Learning Outcomes
By the end of this week, students will be able to:
- Explain what retrieval-augmented generation is and why it's useful (cost savings comopared to increasing context window).
- Build a basic document ingestion and chunking pipeline
- Compute vector embeddings of text using a transformer-based model
- Store and query embeddings using Postgres (or Supabase) + pgvector
- Retrieve relevant documents and use them to prompt an LLM
- Distinguish grounded responses from hallucinations based on source reference
- Explain the difference between retrieval (finding relevant chunks) and generation (answering questions based on them)
- Swap in their own documents and fine-tune retrieval behavior

Note: the distinction between *retrieval* and *generation* is foundational. Retrieval locates relevant pieces of text; generation creates a coherent answer based on those pieces.

## Resources
- [AWS: What is RAG?](https://aws.amazon.com/what-is/retrieval-augmented-generation/)
- [Nir Diamant RAG page](https://github.com/NirDiamant/RAG_Techniques)
- [Timescale RAG Tutorial](https://www.timescale.com/blog/how-to-build-llm-applications-with-pgvector-vector-store-in-langchain)
- [Supabase Blog: OpenAI Embeddings + pgvector](https://supabase.com/blog/openai-embeddings-postgres-vector)
- [LlamaIndex: Understanding RAG](https://docs.llamaindex.ai/en/stable/understanding/rag/)
- [Building RAG with Ollama (YouTube)](https://www.youtube.com/watch?v=GWB9ApTPTv4)

## Instructor Notes
Provide a small, curated library of documents for demos and assignments. Consider:
- Public scientific papers or abstracts (e.g., arXiv)
- Policy documents or public tutorials (e.g., bias in AI or ML, how to learn to code, best way to learn a new skill, tbd). 
- Code the Dream curriculum materials (e.g., course descriptions or content) — this allows students to build domain-specific assistants that can answer questions about CTD itself.
- tbd

Regarding the vector store setup:
- Supabase is a friendly on-ramp.
- Alternatively, setting up a local Postgres server would reinforce DB knowledge from Python 100 and provide useful struggles and hands-on practice. Students used SQLite in P100 and could use some practice with db servers.

