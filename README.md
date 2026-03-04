# 📚 Contextual Document Retrieval System

## 🌟 Overview

A sophisticated Retrieval-Augmented Generation (RAG) system for intelligent document processing and semantic search, leveraging  advanced NLP techniques.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Build Status](https://img.shields.io/badge/build-passing-brightgreen)

## ✨ Features

- 📄 Multi-format document processing (PDF, TXT)
- 🔍 Semantic search capabilities
- 🧠 Intelligent text chunking
- 📊 Vector-based document retrieval
- 🤖 Context-aware response generation

## 🚀 Quick Start

### Prerequisites

- Python 3.8+
- Pinecone Account
- Pinecone API Key

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/document-retrieval-system.git
cd document-retrieval-system
```

2. Create virtual environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

3. Install dependencies
```bash
pip install -r requirements.txt
```

4. Set up environment variables
```bash
# Create .env file
PINECONE_API_KEY=your_pinecone_api_key
```

## 💡 Basic Usage

```python
from document_processor import DocumentProcessor
from vector_store import VectorStore
from mock_llm import MockLLM

# Initialize components
doc_processor = DocumentProcessor()
vector_store = VectorStore(api_key)
mock_llm = MockLLM()

# Load and process document
doc_processor.load_document('sample.pdf')
chunks = doc_processor.chunk_text()
embeddings = doc_processor.generate_embeddings(chunks)

# Index document
vector_store.add_documents(embeddings, chunks, 'sample.pdf')

# Perform query
query_embedding = doc_processor.process_query("Your search query")
search_results = vector_store.search(query_embedding)
response = mock_llm.generate_response(query, search_results[0])
```

## 🛠 Project Structure

```
document-retrieval-system/
│
├── document_processor.py    # Document loading and processing
├── vector_store.py          # Vector database management
├── mock_llm.py              # Response generation
├── main.py                  # Main application script
├── requirements.txt         # Project dependencies
└── README.md                # Project documentation
```

## 🔬 Core Components

1. **Document Processor**
   - Handles multi-format document extraction
   - Implements intelligent text chunking
   - Generates semantic embeddings

2. **Vector Store**
   - Manages document embeddings
   - Performs semantic similarity search
   - Supports Pinecone vector database

3. **Mock LLM**
   - Generates context-aware responses
   - Ranks search results
   - Provides flexible query handling


## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## 📋 Roadmap

- [ ] Support more document formats
- [ ] Enhance embedding techniques
- [ ] Implement advanced caching
- [ ] Add more sophisticated LLM integration

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🛎️ Support

For issues, questions, or suggestions, please [open a GitHub issue](https://github.com/shubhamlodha21/document-retrieval-system/issues).

## 🌐 Connect

- Author: Adinath More 
- LinkedIn: (https://www.linkedin.com/in/adi-more-1a5b34210/)
- Email: moreadinath412@gmail.com
