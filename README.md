# 🌟 Nova: Open-Source Contributor Assistant (Problem Statement 2B)

Nova is an intelligent, RAG-powered developer assistant designed to help first-time open-source contributors easily navigate complex repositories, understand setup instructions, and start contributing during Hacktoberfest.

---

## 🛠️ The Problems We Faced (Challenges & Pain Points)

1. **Scattered Documentation:** Essential project setup instructions and contributing guidelines are fragmented across multiple files (`README.md`, `CONTRIBUTING.md`), making it overwhelming for newcomers.
2. **Starter Kit Limitations:** Default starter kits only supported single PDFs and lacked concurrent multi-Markdown parsing.
3. **AI Hallucinations:** Standard LLMs often generated fake setup commands or inaccurate project details when asked questions outside their training scope.

---

## 💡 How We Solved Them (Technical Solutions)

* **Multi-File Ingestion & Dynamic Tagging:** Upgraded the pipeline to parse multiple `.md`, `.txt`, and `.pdf` files concurrently with source file-tagging (`[File: README.md]`).
* **Strict Hallucination Guardrails:** Enforced rigorous system prompts (`ANSWER_RULES`) restricting Google Gemma 4 to *strictly* use provided context.
* **Minimalist SaaS UI/UX:** Built a clean, modern interface using Gradio with a monochrome theme.
* **Automated Onboarding Checklist (Bonus 2B):** Implemented a specialized "Where do I start?" feature for instant contribution roadmaps.

---

## 🚀 Tech Stack
* **LLM Core:** Google Gemma 4
* **Embeddings:** `sentence-transformers` (`all-MiniLM-L6-v2`)
* **Interface:** Gradio (Python Web Framework)
* **Environment:** Google Colab
