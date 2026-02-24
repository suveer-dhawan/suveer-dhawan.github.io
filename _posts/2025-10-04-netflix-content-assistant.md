---
title: "Netflix Content Assistant: Architecting Local RAG Infrastructure"
date: 2025-10-04 21:40:00 +0530
categories: [Projects, Modern AI Infra]
tags: [rag, python, langchain, ollama, chromadb, semantic-search]
pin: true
---

**Role:** Personal AI Research Project  
**Location:** Melbourne, Australia  
**Timeline:** Sep 2025   

While many AI applications rely exclusively on paid cloud APIs, I wanted to architect and deploy modern AI infrastructure entirely locally. I built an intelligent movie recommendation system using a Retrieval-Augmented Generation (RAG) architecture to process and semantically search a comprehensive dataset of over 6,000 Netflix titles.

### The Architecture & Stack

To ensure privacy, eliminate API costs, and manage context windows effectively, the system was built using a fully local deployment strategy:

* **Orchestration:** LangChain (Managing the LLM application framework and RAG pipeline).
* **Local LLM Deployment:** Ollama (Running `llama3.2` for conversational reasoning and `mxbai-embed-large` for embeddings).
* **Vector Database:** ChromaDB (Storing vector embeddings and executing rapid similarity searches).
* **Data Processing:** Python and Pandas (Extracting and normalizing rich metadata from the raw Netflix catalog).

### Core Technical Achievements

**1. Local Semantic Search Infrastructure**

Instead of relying on basic keyword matching, I implemented advanced vector-based similarity search. The system ingests the dataset, processes rich metadata (genres, IMDB/TMDB scores, release years, and descriptions), and converts them into dense vector embeddings stored in ChromaDB. 

**2. Conversational RAG Pipeline**

The retrieval system uses cosine distance metrics to find the top optimal results based on natural language user queries (e.g., "I want something dark and psychological" or "Movies similar to Inception"). It combines this retrieved context with LangChain's generation pipeline, allowing the local model to provide highly personalized, context-aware recommendations.

**3. Hardware & Memory Optimization**

Running models locally requires careful resource management. The system operates efficiently within a ~2GB memory footprint, with query response times averaging 2-5 seconds. This demonstrates an advanced understanding of AI infrastructure constraints and the practicalities of deploying conversational AI systems on local hardware.

### The Takeaway

This project proves an understanding of what happens "under the hood" of modern generative AI. By managing a dedicated vector database, engineering custom prompts for entertainment discovery, and deploying open-source models locally, I demonstrated the ability to build scalable, private, and highly efficient semantic search systems from the ground up.