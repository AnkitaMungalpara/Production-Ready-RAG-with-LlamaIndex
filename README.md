# Getting Started with LlamaIndex

[1. Build Your First RAG System with LlamaIndex](https://github.com/AnkitaMungalpara/Production-Ready-RAG-with-LlamaIndex/blob/main/Build_Your_First_RAG_System_with_LlamaIndex.ipynb)

- This workflow demonstrates how to create a complete RAG pipeline that utilizes LLM responses with information retrieved from a Wikipedia corpus. The system performs semantic search on Wikipedia articles and generates accurate, context-aware answers.

### Implementation Steps

![Implementation Diagram](https://i.imgur.com/nEJmrzf.png)

### Sample Queries and Responses

![query and response](https://i.imgur.com/IoVB375.png)

# LlamaIndex Components

This section provides an overview of the **key components of LlamaIndex**, a powerful framework for **retrieval-augmented generation (RAG)**, **semantic search**, and **LLM-powered applications**.  

## Table of Contents  

1. **[Data Loaders](#data-loaders)**  
   - [Loading PDF Files](#loading-pdf-files)  
   - [Loading CSV Files](#loading-csv-files)  
   - [Loading Web Page](#loading-web-page)  
   - [Reading From a Directory](#reading-from-a-directory)  

2. **[Embeddings](#embeddings)**  
   - [OpenAI Embeddings](#openai-embeddings)  
   - [Open Source Embeddings From Hugging Face](#open-source-embeddings-from-hugging-face)  
   - [Loading SOTA Embedding Model](#loading-sota-embedding-model)  

3. **[LLMs](#llms)**  
   - [OpenAI GPT Models](#openai-gpt-models)  

4. **[Indexing](#indexing)**  
   - [Vector Store Index](#vector-store-index)  
   - [Summary Index](#summary-index)  
   - [Keyword Table Index](#keyword-table-index)  
   - [Document Summary Index](#document-summary-index)  

5. **[Vector DB](#vector-db)**  
   - [Save Index to Local Disk](#save-index-to-local-disk)  
   - [Using ChromaDB](#using-chromadb)  
   - [Using Pinecone](#using-pinecone)  

6. **[Retriever](#retriever)**  
   - [Vector Store Index Retriever](#vector-store-index-retriever)  
   - [Summary Index Retriever](#summary-index-retriever)  
   - [Keyword Table Index Retriever](#keyword-table-index-retriever)  
   - [Document Summary Index Retriever](#document-summary-index-retriever)  

7. **[Response Synthesis](#response-synthesis)**  
   - [Refine](#refine)  
   - [Compact](#compact)  
   - [Tree Summarize](#tree-summarize)  
   - [Accumulate](#accumulate)  
   - [Compact Accumulate](#compact-accumulate)  

8. **[Query Engine](#query-engine)**  
   - [How the Query Engine Works](#how-the-query-engine-works)  
   - [Customizing the Query Engine](#customizing-the-query-engine)  
   - [Example Query](#example-query)  


## Data Loaders  

Data Loaders allow us to ingest **various types of data** into LlamaIndex.  

- **PDF Loader** – Extracts text from PDFs.  
- **CSV Loader** – Reads structured tabular data.  
- **Web Page Loader** – Fetches and processes web content.  
- **Directory Loader** – Batch-loads multiple files.  

![dl](https://i.imgur.com/A7goK2X.png)


## Embeddings  

Embeddings **convert text into numerical vectors**, enabling similarity search.  

- **OpenAI Embeddings** – Uses OpenAI models for high-quality vectors.  
- **Hugging Face Models** – Supports self-hosted embedding models.  
- **SOTA Embeddings** – Uses state-of-the-art models for specialized domains.  

🔹 **Use case:** Transform text into a format suitable for retrieval.  


## LLMs  

LlamaIndex integrates with **Large Language Models (LLMs)** to process and generate responses.  

- **OpenAI GPT models** – Uses models like `GPT-3`, `GPT-4` for reasoning and text generation.  

🔹 **Use case:** Leverage LLMs for **question-answering, summarization, and text generation**.  

## Indexing  

Indexing organizes data for **efficient retrieval**. LlamaIndex supports:  

- **Vector Store Index** – Stores text embeddings for similarity search.  
- **Summary Index** – Stores summarized versions of documents.  
- **Keyword Table Index** – Organizes data by keywords.  
- **Document Summary Index** – Retrieves concise document-level summaries.  

🔹 **Use case:** Structure data for **fast lookups** and **optimized searches**.  


## Vector DB  

Vector Databases store **high-dimensional embeddings** for retrieval.  

- **Local Disk Storage** – Saves index files for offline use.  
- **ChromaDB** – Open-source, scalable vector search.  
- **Pinecone** – Cloud-based, managed vector database.  

🔹 **Use case:** Store **text embeddings efficiently** for **RAG pipelines**.  

## Retriever  

The Retriever fetches **relevant information** from indexed data.  

![retriever](https://i.imgur.com/f4D20Vq.png)

- **Vector Store Index Retriever** – Uses vector similarity search.  
- **Summary Index Retriever** – Retrieves summarized content.  
- **Keyword Table Index Retriever** – Fetches data based on keyword matches.  
- **Document Summary Index Retriever** – Retrieves entire document summaries.  


## Response Synthesis  

Synthesizing responses involves **combining retrieved data** to generate meaningful answers.  

![rs](https://i.imgur.com/dt6pnRx.png)

- **Refine** – Improves responses iteratively.  
- **Compact** – Summarizes retrieved text.  
- **Tree Summarize** – Structures responses hierarchically.  
- **Accumulate** – Returns all retrieved data without modification.  
- **Compact Accumulate** – Balances completeness and conciseness.  

🔹 **Use case:** **Generate structured, informative answers** from retrieved data.  


## Query Engine  

The **Query Engine** brings everything together, allowing users to query indexed data interactively.  

- **Retrieves relevant documents.**  
- **Synthesizes responses based on query type.**  
- **Supports custom retrieval strategies and LLM integrations.**  

🔹 **Use case:** **Power search engines, chatbots, and knowledge-based applications.**  

## 🚀 Getting Started  

### 📌 Install Dependencies  

```bash
pip install llama-index pinecone-client chromadb
