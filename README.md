# Financial Document Query Chatbot

> Explore similar LLM projects at [gowrish28gog](https://github.com/gowrish28gog/).

A chatbot that uses **Retrieval-Augmented Generation (RAG)** to query and summarize financial documents (10-Q, 10-K). Users can ask questions and get accurate, concise financial insights.

![RAG Chatbot](./assets/rag_chatbot_10q.png)

---

## Key Features

- Query PDFs of financial reports and extract key information.
- Summarize key financial metrics in **two-sentence answers**.
- Compare outputs from multiple models: **GPT-3.5-turbo, LLaMA 2, Gemma 1.1, Flan-T5**.
- Reduces hallucinations often seen in standard LLM responses.
- User-friendly chatbot interface.

---

## How It Works

1. **Problem:** Given a PDF and a question, retrieve relevant information and generate accurate answers.
2. **Data Processing:** PDFs are split into chunks for faster and more accurate retrieval.
3. **RAG:** Combines document retrieval with language model generation.
4. **Prompt Design:** Prompts crafted for concise and relevant financial summaries.
5. **UI:** Simple chatbot interface for interactive queries.

<figure>
    <img src="./assets/llm_hallucination.png" width="300">
    <figcaption>GPT-4 without RAG can hallucinate; RAG reduces this issue.</figcaption>
</figure>

---

## System Architecture

![System Architecture](./assets/rag_architecture.png)

Modified from [blog.goopenai](https://blog.gopenai.com/retrieval-augmented-generation-rag-using-llama-2-chromadb-together-ai-for-retrieval-qa-80e7045a6c79)

---

## Models & Experiments

- GPT-3.5-turbo  
- LLaMA 2  
- Gemma 1.1  
- Flan-T5  

![Models Experiment](./assets/models_experiment.png)

---

## Evaluation Metrics

**Generation Metrics:**  
- **Faithfulness:** Is the answer factually correct based on the document?  
- **Answer Relevancy:** Does the answer directly address the question?  

**Retrieval Metrics:**  
- **Context Recall:** How well the retrieved content matches the ground-truth answer.  
- **Context Precision:** Are the most relevant parts ranked at the top?  

![GPT-3.5 Evaluation](./assets/gpt35_eval.png)

---

## Installation

```bash
pip install -r requirements.txt
