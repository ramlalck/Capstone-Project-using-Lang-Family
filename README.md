# 🚀 Agentic AI Capstone — OTT Incident Triage System (LangChain Ecosystem)

## 📌 Project Overview

This capstone project implements a **production-style Agentic AI system** for **OTT incident triage and diagnostics**, built end-to-end using the **LangChain family of frameworks**:

- **LangChain** – core LLM orchestration, prompts, tools, and RAG  
- **LangGraph** – explicit stateful control flow, retries, and escalation logic  
- **LangSmith** – observability, tracing, debugging, and run analysis  

The system demonstrates how to design **reliable, explainable, and observable LLM-powered workflows**, avoiding common pitfalls such as hallucinations, opaque reasoning, and uncontrolled agent behavior.

---

## 🎯 Problem Statement

In OTT platforms, incidents such as **CDN timeouts, DRM license failures, and packaging errors** require fast, accurate triage.

Traditional approaches:
- Are rule-heavy and brittle, or
- Use LLMs naively, leading to hallucinations and poor debuggability

This project solves the problem by building a **hybrid deterministic + LLM agent** that:
- Understands user-reported incidents
- Retrieves relevant knowledge
- Executes diagnostic tools
- Produces grounded, explainable responses
- Escalates gracefully when confidence is low

---

## 🧠 Key Capabilities Demonstrated

### ✅ Agentic AI Architecture
- Explicit **state machine** using LangGraph
- Clear separation of concerns: ingest → classify → retrieve → plan → act → synthesize → validate → escalate
- Deterministic control over retries and failure handling

### ✅ Hybrid Classification (Production-Grade)
- Deterministic-first classification using error signals
- LLM fallback only when rules cannot decide
- Prevents LLMs from overriding known facts

### ✅ RAG with Discipline
- Signal-aware knowledge base retrieval
- Clear distinction between retrieved documents and cited documents
- Validation ensures citations are grounded (hallucination guardrails)

### ✅ Tool-Oriented Reasoning
- Deterministic tools for error lookup and checklist generation
- Explicit tool planning and execution

### ✅ Robust Validation & Escalation
- Structured output validation
- Retry loop with bounded attempts
- Automatic escalation summary generation

### ✅ Full Observability with LangSmith
- End-to-end tracing of graph execution
- Visibility into LLM calls, tools, and routing decisions

---

## 🏗️ System Architecture (Conceptual Flow)

User Query  
→ Ingest (extract signals, error codes)  
→ Hybrid Intent Classification  
→ RAG Retrieval (KB)  
→ Tool Planning  
→ Tool Execution  
→ Synthesis (grounded explanation)  
→ Validation  
→ Retry / Escalate / End  

---

## 🧰 Tech Stack

- Python  
- LangChain  
- LangGraph  
- LangSmith  
- OpenAI Chat Models (pluggable with local LLMs)  
- Google Colab / Jupyter Notebook  

---

## 🧪 Example Use Cases

- Investigate CDN timeout on FireTV only  
- WV_LICENSE_403 observed on Android devices  
- Manifest 404 for one title only  

Each query produces:
- Classified intent
- Root-cause analysis
- Actionable next steps
- Evidence-backed citations
- Full execution trace in LangSmith

---

## 🔍 Observability & Debugging

All runs are traceable in **LangSmith**, including:
- Node-by-node execution
- Tool inputs and outputs
- LLM prompts and responses
- Retry and escalation paths

---

## 📂 Repository Structure

.
├── capstone_langgraph.ipynb  
├── README.md  

---

## 🏆 What This Capstone Proves

- Ability to design agentic AI systems
- Production-grade control and observability
- Practical use of the LangChain ecosystem
- Strong grounding, validation, and debugging discipline

---

## 🚧 Future Enhancements

- Embedding-based semantic retrieval
- Human-in-the-loop approvals
- Confidence scoring
- Ticketing system integrations

---

## 📌 Final Note

This capstone reflects **real-world production constraints** and emphasizes **reliability, transparency, and debuggability**.
