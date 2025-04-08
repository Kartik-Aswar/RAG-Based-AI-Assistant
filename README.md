# RAG Pipeline with Dynamic Routing and Quality Control

Open-source implementation of a robust Retrieval-Augmented Generation (RAG) system with automatic routing between vector store and web search. Features quality control checks for document relevance, answer grounding, and safety mechanisms to prevent infinite looping through.
The output is consized with max output of 3 lines in sentence as it is defined in ChatPromptTemplate (if required can be changed by removing prompt = hub.pull("rlm/rag-prompt") and add custom PromptTemplate):
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

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/Kartik-Aswar/RAG-Based-AI-Assistant.git
cd RAG-Based-AI-Assistant
```

## Install dependencies:
```bash
pip install -r requirements.txt
```

## Configuration
Create .env file with your API keys:

- GROQ_API_KEY=your_groq_key
- LANGCHAIN_API_KEY=your_langchain_key
- groq_track=your_groq_track_key
- TAVILY_API_KEY=your_tavily_key
- HF_TOKEN=your hugging face token

## Usage

Run the assistant:

```bash
python Assistant_rag.py
```

1.Enter URLs separated by commas when prompted

2.Ask questions about the content

3.System will automatically:
- Retrieve relevant documents
- Verify answer quality
- Fallback to web search when needed
- Retry with improved queries






  
