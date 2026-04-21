# Finance ChatBot 

## Overview
Finance ChatBot is an AI-powered personal finance assistant built using LangGraph, ChromaDB, and LLMs. It provides intelligent, context-aware responses for financial queries such as budgeting, SIP, loans, tax planning, insurance, and investment strategies.

The system supports retrieval-augmented generation (RAG), tool-based EMI calculation, multi-turn memory, and language-aware responses.

---

## Project Files

- Finance_ChatBot_clean.ipynb  
  Contains the complete implementation of the LangGraph-based Finance ChatBot with structured pipeline and clean code.

- Finance_ChatBot_demo.ipynb  
  Contains executed outputs showing real working examples of the chatbot including RAG responses, EMI calculations, and multi-language outputs.

- README.md  
  Project documentation and overview.
---

## Features

- Retrieval-Augmented Generation (RAG) using ChromaDB
- Finance knowledge base covering:
  - Budgeting
  - SIP and Mutual Funds
  - Loans and EMI
  - Tax saving instruments
  - Insurance
  - Stock market basics
  - Retirement planning
- EMI Calculator tool integration
- Multi-turn conversation memory
- Language-aware responses (English, Hindi, Bengali)
- LangGraph-based modular agent pipeline
- Router-based decision system (retrieve / tool / chitchat)

---

## Architecture

User Query → Memory Node → Router Node → (Retrieval / Tool / Skip) → Answer Node → Evaluation Node → Save Node

---

## Tech Stack

- Python
- LangGraph
- LangChain
- ChromaDB
- HuggingFace Embeddings
- Groq / Google Gemini LLM
- Streamlit 
- Jupyter Notebook (Colab)

---

## How It Works

1. User inputs a finance-related question
2. Router classifies the query:
   - Retrieval for finance knowledge
   - Tool for EMI calculation
   - Chitchat for casual queries
3. Relevant context is retrieved from vector database
4. LLM generates a response based on context and memory
5. Evaluation node checks faithfulness
6. Response is returned to user

---

## Example Queries

- What is SIP and how does it work?
- Calculate EMI for 500000 at 8.5% for 240 months
- What is an emergency fund?
- Best way to save tax in India?

---

## Setup (for running notebook)

Install dependencies:

```bash
pip install langgraph langchain chromadb sentence-transformers streamlit
