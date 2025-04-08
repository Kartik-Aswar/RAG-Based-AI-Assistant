# RAG Pipeline with Dynamic Routing and Quality Control

A robust Retrieval-Augmented Generation (RAG) system with automatic routing between vector store and web search, featuring quality control checks for document relevance and answer grounding.

## Features

- **URL Ingestion**: Process multiple URLs for document retrieval
- **Hybrid Search Routing**: Automatically chooses between vector store and web search
- **Document Relevance Grading**: Filters irrelevant retrieved documents
- **Hallucination Check**: Verifies answer grounding in source materials
- **Query Transformation**: Improves search queries through iterative rewriting
- **Retry Mechanism**: Automatic query rephrasing for failed retrievals

## Prerequisites

- Python 3.10+
- API keys for:
  - Groq (https://console.groq.com/)
  - LangChain (https://smith.langchain.com/)
  - Tavily (hardcoded trial key if required then change it)
  
