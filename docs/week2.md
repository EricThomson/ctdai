# Week 2: Retrieval-Augmented Generation (RAG)
Retrieval-Augmented Generation (RAG) systems are large language models (LLMs) that are augmented with external knowledge sources such as file systems or databases. For example, if you ask an LLM, “Who won the World Cup?” it might reply based on 2021 or earlier knowledge. A RAG system can search a structured data source and provide current information. 

## Learning Outcomes
By the end of this week, students will be able to:

1.  Define retrieval-augmented generation (RAG) and when it is useful (e.g., cost savings compared to simply increasing the context window).
2.  Differentiate between retrieval and generation
3.  Retrieve relevant documents and integrate them into LLM prompots. 
4.  Create vector stores for storing document embeddings and performing similarity searches. 
5. Evaluate responses of RAG systems, determining whether responses are based on retrieved sources or hallucinations.
6. Integrate custom documents into a RAG workflow. 
 
## Lesson outline
While RAG systems can get extremely complex, our plan is to start very simple, and iteratively build toward more a more production-ready pipeline in three steps.

### Step 1: Minimal Naive RAG Implementation 
Very short (~100 lines) implementation of naive RAG:

- Load one or two PDFs  
- Perform basic keyword matching
- Pass matched content into the LLM via a simple prompt

This will be a *very* short demo (100 lines) to illustrate the central concept: retrieving information from an external data store and injecting it into the model’s prompt to generate better answers. This is to demonstrate the simplicity of the minimal RAG concept. This approach has several well-known limitations (to name two: the retrieval step is brittle, and it won't scale to larger datasets). Therefore, we will quickly pivot away. 

### Step 2: Basic Semantic RAG
Our plan is to adapt [Nir Diamant’s minimal RAG example](https://github.com/NirDiamant/RAG_TECHNIQUES/blob/main/all_rag_techniques/simple_rag.ipynb) to demonstrate semantic RAG. This step includes:

- Document chunking with embedding. 
- Storing and querying chunks in a vector store (FAISS)
- Retrieving top-k relevant chunks using semantic similarity and vector indexes. 
- Evaluation of the RAG system

This is the simplest example with all the basic features that overcome the limitations of the naive RAG from Step 1. 

### Step 3: Scalable RAG with pgvector
We will next build a more scalable example suitable for enterprise applications. We will build a vector database using LangChain and PostgreSQL with pgvector. we will work with a vector store using LangChain and Postgres/pgvector. 

For this, step we plan to adapt and build on the [excellent tutorial from Timescale](https://www.timescale.com/blog/how-to-build-llm-applications-with-pgvector-vector-store-in-langchain), customizing it for our educational context. This step includes:

- Using pgvector and LangChain to perform semantic similarity search over embedded documents.
- Store vector embeddings and document metadata in a PostgreSQL database. 
- Work with multi-document libraries 
- Meta-data filtering
- Further discussion of evaluating RAG workflows.

This step will attempt to connect the previous concepts to production-level implementation, showing how retrieval works in ways that can scale (and reinforce some of the RDB concepts they learned in Python 100). 

## Hands-On Activities
1. Build a naive RAG example from scratch (no embeddings, no DB)
2. Build a semantic RAG pipeline from scratch.
3. Set up a local or hosted Postgres database with `pgvector` support
4. Store embeddings and metadata in the vector database
5. Display retrieved sources alongside the generated answer to evaluate accuracy
6. Explore different ways to evaluate RAG systems

## Resources
- [AWS: What is RAG?](https://aws.amazon.com/what-is/retrieval-augmented-generation/)
- [Nir Diamant RAG page](https://github.com/NirDiamant/RAG_Techniques)
- [Timescale RAG Tutorial](https://www.timescale.com/blog/how-to-build-llm-applications-with-pgvector-vector-store-in-langchain)
- [Supabase Blog: OpenAI Embeddings + pgvector](https://supabase.com/blog/openai-embeddings-postgres-vector)
- [LlamaIndex: Understanding RAG](https://docs.llamaindex.ai/en/stable/understanding/rag/)
- [Building RAG with Ollama (YouTube)](https://www.youtube.com/watch?v=GWB9ApTPTv4)
- [Vector indices](https://www.youtube.com/watch?v=N7TQgp18kA4)
  
## Instructor Notes
We still need to figure out what docs to use. For the lesson, we will need to provide a very small, curated library of documents for demos and assignments. Consider:

- Public scientific papers or abstracts (e.g., arXiv)
- Policy documents or public tutorials (e.g., bias in AI or ML, how to learn to code). 
- Code the Dream curriculum materials (e.g., course descriptions or content) — this allows students to build domain-specific assistants that can answer questions about CTD itself.
- tbd

Regarding the vector store setup:
- Supabase is a friendly on-ramp.
- Alternatively, setting up a local Postgres server would reinforce DB knowledge from Python 100 and provide useful struggles and hands-on practice. Students used SQLite in P100 and could use some practice with db servers.

