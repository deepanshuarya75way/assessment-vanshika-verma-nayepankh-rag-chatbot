# 🤖 NayePankh AI — RAG Chatbot

An AI-powered **Retrieval-Augmented Generation (RAG) chatbot** built for **NayePankh Foundation**, a UP Government registered NGO working to support underprivileged communities across India.

The chatbot allows users to ask questions about **donations, volunteering, internships, NGO initiatives, and social-impact activities** and receive contextual answers grounded in the organization's knowledge base.

---

## 🌐 Live Demo

🚀 **Try the chatbot live:**

👉 https://vanshika-nayepankh-bot.streamlit.app/

---

## 📌 About the Project

Visitors to an NGO website may have practical questions such as:

- How can I donate?
- Is my donation tax-exempt?
- How can I volunteer?
- Are internships available?
- What kind of initiatives does the NGO conduct?
- How does NayePankh Foundation support underprivileged communities?

Finding answers to these questions can sometimes require navigating through multiple pages or contacting the organization directly.

This project solves that problem by providing an **AI-powered conversational interface** using **Retrieval-Augmented Generation (RAG)**.

Instead of relying only on the language model's general knowledge, the chatbot first retrieves relevant information from a curated NayePankh Foundation knowledge base and then provides that context to the LLM.

This helps generate responses that are **relevant, contextual, and grounded in the available source material**.

The project demonstrates a practical implementation of RAG using a real-world social-impact use case.

---

# 🧠 How RAG Works

The chatbot follows a retrieval-first architecture:

```text
                 User Question
                       │
                       ▼
              HuggingFace Embeddings
                       │
                       ▼
                 Vector Search
                       │
                       ▼
                    ChromaDB
                       │
              Top 4 Relevant Chunks
                       │
                       ▼
            Retrieved Context + Query
                       │
                       ▼
                Prompt Template
                       │
                       ▼
              Groq API → LLaMA 3
                       │
                       ▼
             Grounded AI Response
                       │
                       ▼
                Streamlit UI
                       │
                       ▼
              Response + Sources
