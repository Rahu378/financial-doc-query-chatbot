# Financial Document Query Chatbot

**Technologies:** Kendra, AWS (S3, Lambda, Amplify), RAG, LangChain, CUDA, PyTorch, GPT-3.5, LLaMA 2, Gemma 1.1  

**Timeline:** May 2024  

---

## Overview
A chatbot designed to query PDF financial documents (10-Q, 10-K) using Retrieval-Augmented Generation (RAG). Users can ask questions, retrieve relevant document sections, and calculate key financial metrics such as EV/EBITDA for M&A decisions. GPT-3.5-turbo improved retrieval accuracy by 25%, enhancing decision-making efficiency by 30%.

---

## Features
- Query financial PDFs and extract relevant information.
- Summarize key financial metrics in concise two-sentence responses.
- Compare outputs across GPT-3.5-turbo, LLaMA 2, and Gemma 1.1.
- Mitigate hallucinations with RAG for more faithful answers.
- User-friendly chatbot interface.

---

## Technical Problem Formulation
- **Problem Statement:** Given a PDF and a query, retrieve and synthesize relevant details accurately.
- **Data Ingestion:** Reading and splitting long financial documents for efficient chunking.
- **RAG:** Combines document retrieval with language model generation.
- **LLMs Evaluated:** GPT-3.5, LLaMA 2, Gemma 1.1, Flan-T5.
- **Prompt Design:** Two-sentence financial summaries.
- **User Interface:** Chatbot-like interface for interaction.

---

## System Architecture
Modified from [blog.goopenai](https://blog.goopenai.com)

![System Architecture](path/to/architecture_diagram.png)  <!-- Replace with your diagram path -->

---

## LLMs and Experiments
- GPT-3.5
- LLaMA 2
- Gemma 1.1
- Flan-T5

---

## Evaluation Metrics
- **Faithfulness:** Measures factual consistency of generated answers against the given context.
- **Answer Relevancy:** Scores relevancy of answers according to the given question. Incomplete, redundant, or unnecessary information is penalized.
- **Context Recall:** Measures the extent to which retrieved context aligns with the annotated answer (ground truth).
- **Context Precision:** Evaluates whether all ground-truth relevant items present in the contexts are ranked higher.

---

## Installation
```bash
pip install -r requirements.txt
