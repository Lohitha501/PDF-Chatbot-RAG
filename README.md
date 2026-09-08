# PDF Chatbot RAG

A Retrieval-Augmented Generation (RAG) based chatbot that allows users to ask questions about the content of PDF documents and receive relevant answers using an AI language model.

## Overview

PDF Chatbot RAG processes a PDF document, extracts its content, divides the text into smaller chunks, generates semantic embeddings, and stores them in a vector database.

When a user asks a question, the system retrieves the most relevant information from the document and provides it to the language model to generate a contextual answer.

## Key Features

- PDF document processing
- Text extraction and chunking
- Semantic text embeddings
- Vector storage using ChromaDB
- Semantic similarity search
- Context-aware question answering
- OpenRouter LLM integration
- Secure API key management using environment variables

## Technologies Used

| Technology | Purpose |
|------------|---------|
| Python | Application development |
| PyPDF2 | PDF text extraction |
| Sentence Transformers | Text embeddings |
| ChromaDB | Vector database |
| OpenRouter | Language model integration |
| Python-dotenv | Environment variable management |

## System Workflow

PDF Document  
→ Text Extraction  
→ Text Chunking  
→ Embedding Generation  
→ ChromaDB Storage  
→ Semantic Search  
→ Context Retrieval  
→ LLM Response

## Project Structure

```text
PDF-Chatbot-RAG/
│
├── data/
│   └── sample.pdf
│
├── utils/
│   ├── chunking.py
│   ├── embeddings.py
│   ├── openrouter_llm.py
│   ├── pdf_reader.py
│   ├── prompt_builder.py
│   ├── retriever.py
│   └── vector_db.py
│
├── app.py
├── config.py
├── requirements.txt
├── .gitignore
└── README.md

Installation

Create a virtual environment:

python -m venv venv

Activate the virtual environment:

venv\Scripts\activate

Install the required dependencies:

pip install -r requirements.txt
Configuration

Create a .env file in the project directory and add your OpenRouter API key:

OPENROUTER_API_KEY=your_api_key_here

Do not upload the .env file to GitHub.

Running the Application

Run the application using:

python app.py

The chatbot will process the PDF and allow you to enter questions based on its content.

Project Objective

The objective of this project is to demonstrate how Retrieval-Augmented Generation can be used to build a document-based question-answering system by combining semantic search, vector databases, and large language models.
