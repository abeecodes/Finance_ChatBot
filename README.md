# FinAdvisor — Multilingual Personal Finance Advisory Chatbot

## Overview

FinAdvisor is an agentic AI chatbot designed to provide personalised financial guidance in English, Hindi, and Bengali. It uses LangGraph for multi-step orchestration, Retrieval-Augmented Generation (RAG) over a curated finance knowledge base, and persistent conversation memory to enable context-aware, multi-turn interactions.

---

## Problem Statement

Access to reliable and personalised financial advice remains limited for many individuals due to cost, language barriers, and the complexity of financial concepts. FinAdvisor offers an accessible, multilingual, AI-powered assistant that makes financial decisions easier and provides grounded responses based on trusted sources.

---

## Architecture

```
User Query
    ↓
Memory Node
(maintains conversation context and extracts user details)
    ↓
Router Node
(decides: retrieval/chit-chat/memory-only)
    ↓
Retrieval Node / Skip Node
(fetches relevant finance context if needed)
    ↓
Answer Node
(generates response using LLM + retrieved context + chat history)
    ↓
Evaluation Node
(validates response quality and faithfulness score)
    ↓
Save Node
(stores updated conversation state)
    ↓
Final Output
```

---

## Features

* Multi-turn conversational memory using state management
* Retrieval-Augmented Generation over curated finance documents
* Self-evaluation mechanism for response faithfulness
* Language support for English, Hindi, and Bengali
* Modular LangGraph-based agent architecture with multiple reasoning nodes
* Streamlit-based interactive user interface

---

## Setup Instructions

```bash
pip install -r requirements.txt
streamlit run app.py
```

Provide your Groq API key in the application sidebar to enable LLM functionality. API keys can be generated from the Groq console.

---

## Covered Financial Topics

Budgeting, systematic investment plans, mutual funds, taxation (80C, 80D), home loans, insurance, stock market basics, retirement planning, debt management, gold investment, real estate, and long-term financial goal planning.


