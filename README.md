# LlamaIndex RAG Q&A System

A Retrieval-Augmented Generation (RAG) system built with LlamaIndex that allows querying your own documents using state-of-the-art language models.

## Features

- 🧠 RAG-based question answering on your own documents
- 🔍 Vector search using FAISS 
- 🤖 Integration with OpenRouter API
- 📊 High-quality embeddings using HuggingFace local embeddings

## Installation

1. Clone this repository
2. Install dependencies:

```bash
pip install -r requirements.txt
```

## Setup

1. Copy `.env.example` to `.env`:

```bash
cp .env.example .env
```

2. Edit `.env` with your OpenRouter API key:

```
OPENROUTER_API_KEY=your_key_here
OPENROUTER_BASE_URL=https://openrouter.ai/api/v1
YOUR_SITE_URL=your_site_url  # Optional
YOUR_SITE_NAME=your_site_name  # Optional
```

3. Create a `data` directory and add your documents:

```bash
mkdir -p data
# Add your documents to the data directory
```

## Usage

Run the Jupyter notebook `RAG-QA.ipynb` to:

1. Load and process your documents
2. Create embeddings using HuggingFace's BAAI/bge-m3
3. Store the embeddings in a FAISS vector database
4. Query your documents using OpenRouter LLM

```bash
jupyter notebook RAG-QA.ipynb
```

## Project Structure

```
llamaindex-RAG/
├── .env                  # Environment variables (API keys)
├── RAG-QA.ipynb         # Main Jupyter notebook for RAG implementation
├── README.md            # This file
├── requirements.txt     # Required Python packages
├── data/                # Directory for your documents
└── storage/             # Directory for stored indexes (created during execution)
```

## Dependencies

- llama-index - Core indexing and retrieval framework
- FAISS - Vector similarity search
- HuggingFace - For embedding models
- OpenRouter - For LLM API access

## License

MIT