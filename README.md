# Financial News Q&A with Local RAG Pipeline

A Retrieval-Augmented Generation (RAG) system for querying financial news using local LLMs (Ollama) and FAISS vector search.

![RAG Architecture Diagram](https://i.imgur.com/RVQHX7l.png) *(Example diagram - replace with your actual architecture)*

## Features

- **Web Scraping**: Automated extraction of financial articles from MoneyControl using LangChain's AsyncHtmlLoader
- **Chunk Processing**: Text splitting with RecursiveCharacterTextSplitter (1000 chars chunks, 200 overlap)
- **Local LLM Integration**: Ollama's phi model for offline question answering
- **Vector Search**: FAISS index with OllamaEmbeddings for efficient document retrieval
- **Source Attribution**: RetrievalQAWithSourcesChain provides verifiable answer sources

## Tech Stack

- **LangChain** (Document loaders, text splitters, chains)
- **Ollama** (Local LLM inference)
- **FAISS** (Vector similarity search)
- **Python** (Pandas, Pickle, Requests)

## Installation

1. Install Ollama and pull the phi model:
```bash
curl -fsSL https://ollama.com/install.sh | sh
ollama pull phi
