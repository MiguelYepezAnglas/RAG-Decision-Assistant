# 🧠 DecisionCoach AI – Advanced RAG System

An advanced Retrieval-Augmented Generation (RAG) system designed to support **professional decision-making and communication** by integrating technical, psychological, and business knowledge.


---

## 👨‍💻 Author

- Miguel Yepez
- Martin Rios
- Jose Valdivia


---

## 🚀 Overview

DecisionCoach AI is an intelligent assistant that:

- Retrieves relevant information from multiple sources
- Enhances responses using semantic search and reranking
- Generates structured and actionable answers using LLMs
- Reduces hallucinations through context validation
- Evaluates response quality using automatic metrics

---

## 🏗️ System Architecture
Documents 

→ Chunking → Embeddings → Vector DB (FAISS)

→ Hybrid Retrieval (FAISS + BM25)

→ Reranker (Cross-Encoder)

→ LLM (Qwen / Flan-T5)

→ Validation 

→ Evaluation 

→ Response


---

## 📚 Data Sources

The system integrates **real-world knowledge** from multiple domains:

- 🔹 AI / RAG (Wikipedia, LangChain Docs)
- 🧠 Psychology (Emotional Intelligence, Cognitive Bias)
- 💼 Business & Leadership (HBR, CCL)
- 💬 Communication (SkillsYouNeed, HubSpot)

Each document is enriched with metadata:
- `source_name`
- `url`
- `category`

---

## ⚙️ Key Components

### 1. 📄 Chunking
- Recursive splitting with overlap
- Balance between context and precision

### 2. 🔢 Embeddings
- Model: `sentence-transformers/all-MiniLM-L6-v2`
- Normalized vectors for semantic similarity

### 3. 🗂️ Vector Store
- FAISS (HNSW index)
- Efficient approximate nearest neighbor search

### 4. 🔍 Hybrid Retrieval
- FAISS → semantic search
- BM25 → lexical search
- Combined results for better recall

### 5. 📊 Reranking
- Cross-Encoder (`ms-marco-MiniLM`)
- Improves relevance of retrieved documents

### 6. 🤖 LLMs
- Qwen 1.5 (main generator)
- Flan-T5 (query rewriting)

### 7. 🧹 Validation Layer
- Hallucination detection
- Context enforcement
- Answer cleaning

### 8. 📈 Evaluation
- Grounding Score
- Hallucination Score
- ROUGE (ROUGE-1, ROUGE-L)

---

## 🧠 Pipeline

The system follows this flow:

1. Query rewriting (typo correction)
2. Query normalization
3. Hybrid retrieval
4. Reranking
5. Context construction
6. Answer generation
7. Post-processing
8. Evaluation

---

## 📊 Evaluation Metrics

### ✅ Grounding Score
Measures how much the answer is based on retrieved context.

### ⚠️ Hallucination Detection
Detects unsupported information in generated responses.

### 📏 ROUGE
Measures similarity between generated answers and reference answers.

Example:

ROUGE-1: 0.60
ROUGE-L: 0.49



---

## 📁 Repository Structure

├── notebook.ipynb

├── presentation.pdf

├── README.md



---

## 🎯 Key Features

- Hybrid retrieval (semantic + lexical)
- Multi-domain knowledge integration
- Structured professional responses
- Automatic evaluation pipeline
- Modular and extensible design

---

## 💡 Future Improvements

- Better reranking (ColBERT / LLM reranker)
- Retrieval evaluation (Recall@K, MRR)
- Streaming responses
- UI / Chat interface



---

## 📌 Summary

DecisionCoach AI demonstrates how RAG systems can go beyond simple QA by:

- Improving factual accuracy
- Enhancing reasoning quality
- Supporting real-world decision-making
