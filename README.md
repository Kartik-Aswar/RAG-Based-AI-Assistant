# RAG Pipeline with Dynamic Routing and Quality Control

Open-source implementation of a robust Retrieval-Augmented Generation (RAG) system with automatic routing between vector store and web search. Features quality control checks for document relevance, answer grounding, and safety mechanisms to prevent infinite looping through:
- Retry limit enforcement (max 3 attempts)
- Fallback to graceful exit after failed retrievals
- Systematic query transformation safeguards

## Features

- **URL Ingestion**: Process multiple URLs for document retrieval
- **Hybrid Search Routing**: Automatically chooses between vector store and web search
- **Document Relevance Grading**: Filters irrelevant retrieved documents
- **Hallucination Check**: Verifies answer grounding in source materials
- **Query Transformation**: Improves search queries through iterative rewriting
- **Retry Mechanism**: Automatic query rephrasing for failed retrievals
- **Safety-Limited Retries**: Automatic query rephrasing with built-in fail-safe (max 3 attempts) to prevent infinite loops  

## Prerequisites

- Python 3.10+
- API keys for:
  - Groq (https://console.groq.com/)
  - LangChain (https://smith.langchain.com/)
  - Tavily (hardcoded trial key if required then change it)
    
  
