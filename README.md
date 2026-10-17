# Hi, I'm Aryan 👋 [![Profile Views](https://komarev.com/ghpvc/?username=kharyan14&color=blue&style=flat-square)](https://github.com/kharyan14/kharyan14)

I lead rollouts and product enhancements for **DocVu**, a mortgage document-AI product. I handle production triage, edge-case management, and feature prioritization. With around 4 years in enterprise tech—including data consulting at Informatica prior to this—I am now focusing on AI product management and forward-deployed engineering roles.

---

## 🚀 What I'm Building

* **[docchase](https://github.com/kharyan14/docchase)** — An intelligent multi-agent system designed to automate document tracking, follow-ups, and exception escalation across enterprise workflows.
* **[mortgage-exception-workbench](https://github.com/kharyan14/mortgage-exception-workbench)** — Flags missing documents, conflicting values, and low-confidence extractions in loan files. It answers with cited policy and routes low-confidence cases to a human reviewer before any database write occurs.
* **[rag-knowledge-base](https://github.com/kharyan14/rag-knowledge-base)** — Document Q&A built with LangChain, OpenAI embeddings, and FAISS. It answers exclusively from retrieved passages, cites its sources, and includes a built-in evaluation set.
* **[ai-research-digest](https://github.com/kharyan14/ai-research-digest)** — Automatically pulls new AI papers from arXiv, summarizes them using Gemini, and tracks category and author trends via pandas.
* **[tax-saathi](https://github.com/kharyan14/tax-saathi)** — A browser-based prototype helping Indian taxpayers track ITR deadlines, late fees, and required filing documents. 
  * 🌐 Check out the [Live Demo](https://kharyan14.github.io/tax-saathi)

---

## 🏗️ System Architecture & Workflow Sequences

### `docchase` — Multi-Agent Tracking Pipeline
```text
[Input Trigger] 
       │
       ▼
[Orchestrator Agent] ──(Task Decomposition)──► [Document Tracker Agent]
       │                                              │
       ▼                                              ▼
[Escalation Engine] ◄──(Confidence Threshold Check)── [Extraction Worker]

```

### `mortgage-exception-workbench` — Exception Triage Workflow

```text
Incoming Loan File 
       │
       ▼
[Encoder-Decoder Extraction] ──► [Policy Compliance Engine]
                                        │
                                        ├─► High Confidence (≥ 0.90) ──► [Automated DB Write]
                                        │
                                        └─► Low Confidence (< 0.90)  ──► [Human Reviewer Queue]

```

---

## 📊 Evaluation Metrics & Rigor

To ensure enterprise reliability, my document processing and RAG repositories track targeted quantitative benchmarks:

* **Retrieval Precision & Recall (`rag-knowledge-base`):** Measured via precision@k and recall@k to ensure relevant policy sections are fetched without injecting noise.
* **Faithfulness & Answer Relevance:** Verified using automated evaluation sets to confirm LLM answers are strictly grounded in retrieved document context, maintaining a **>92% faithfulness score**.
* **Extraction Confidence Scoring (`mortgage-exception-workbench`):** Utilizes token-level confidence thresholds from encoder-decoder models to prevent hallucinated data writes and streamline human-in-the-loop audit trails.

---

## 🛠️ How I Work

> Production support shows you where AI products actually break: messy inputs, edge-case failures, and unclear data ownership. I turn those real-world failure modes into structured specs, rigorous eval sets, and robust working prototypes.

---

## 💻 Tech Stack & Tools

* **Languages & Core:** `Python` `SQL` `PySpark`
* **AI, LLM & RAG Stack:** `LangChain` `RAG Architectures` `Antigravity` `OpenAI API` `Gemini API`
* **Document Processing & MLOps:** `Encoder-Decoder Models` `Model Evaluation & Evals` `Vector DBs (FAISS)`
