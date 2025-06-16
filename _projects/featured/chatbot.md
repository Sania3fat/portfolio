---
title: "Chatbot - Institutional Assessment"
description: "A chatbot that provides factual information from Institutional Documents and Policies"
category: featured
github_link: [Chatbot](https://github.com/Sania3fat/ChatBot/blob/main/chatbot_optimized_0615v3.py)
technologies:
  - Python
  - Streamlit
  - Database
  - Semantic (all-MiniLM-L6-v2)
  - LLM (gpt-4o-mini)
  - Web and PDF Scrapping and cleaning
image: /assets/images/chatbot.png
---

# Project Overview
The primary objective is to provide a chatbot that will summarize and give factual responses to questions from institutional documents and policies

## Features
- Data Sources: Primarily from [Maryville College](https://www.maryvillecollege.edu/academics/catalog/)
- Modeling: The core is a RAG (Retrieval-Augmented Generation) architecture. It combines document retrieval with language model generation to provide accurate, contextual responses.
- Analysis: Python, Streamlit

## Technologies Used
The analysis currently uses Python, Streamlit, Word embedding (all-MiniLM-L6-v2), language model (gpt-4o-mini), PDF extraction, and web scrapping.

## Implementation
The chatbot is now in the testing phase

## Results

### 🤖 Institutional Assessment Assistant
*Ask me about Maryville College policies and procedures*

---

#### 💬 Interactive Chat Interface
The chatbot provides real-time responses to questions about institutional documents and policies using advanced RAG (Retrieval-Augmented Generation) technology.

**Sample Conversation:**
```
User: What are the graduation requirements?
Assistant: Based on the institutional documents, graduation requirements include...
```

#### Key Features

| Feature | Technology | Description |
|---------|------------|-------------|
| 📚 **Document Analysis** | Python + PDF/Web Scraping | Processes academic catalogs and policy documents |
| 🔍 **Smart Search** | all-MiniLM-L6-v2 embeddings | Uses semantic embeddings for accurate retrieval |
| ⚡ **Real-time Response** | GPT-4o-mini | Powered by advanced language model for instant answers |
| 🔒 **Secure & Reliable** | Streamlit framework | Ensures data privacy and consistent performance |

#### Live Demo

**🚀 [Try the Chatbot Live](https://chatbot-zx3azdx793iudqjuf2eds9.streamlit.app){:target="_blank"}**

[![Chatbot Demo](https://img.shields.io/badge/🤖_Live_Demo-Try_Now-brightgreen?style=for-the-badge&logo=streamlit)](https://chatbot-zx3azdx793iudqjuf2eds9.streamlit.app)

> **Note:** Click the link above to interact with the live chatbot interface. The application opens in a new tab where you can ask questions about Maryville College policies and procedures.

#### Core Capabilities
✅ **RAG Architecture** - Combines retrieval and generation for accurate responses  
✅ **Semantic Search** - Understanding context and meaning, not just keywords  
✅ **Policy Compliance** - Trained specifically on institutional documents  
✅ **Multi-format Support** - Handles PDFs, web pages, and structured documents  

---

### Technical Architecture

The chatbot implements a **Retrieval-Augmented Generation (RAG)** system with the following components:

| Component | Technology | Purpose |
|-----------|------------|---------|
| **Frontend** | Streamlit | User interface and interaction |
| **Embeddings** | all-MiniLM-L6-v2 | Semantic document understanding |
| **LLM** | GPT-4o-mini | Natural language generation |
| **Data Processing** | Python + PDF/Web scraping | Document ingestion and cleaning |
| **Vector Database** | Custom implementation | Efficient similarity search |

### Sample Interactions

<div style="background: #f8f9fa; padding: 20px; border-radius: 10px; margin: 20px 0;">
<strong>🎓 Academic Policies:</strong>
<blockquote style="border-left: 4px solid #5B0F1B; padding-left: 15px; margin: 10px 0;">
"What is the minimum GPA requirement for graduation?"<br>
<em>→ Retrieves specific GPA requirements from the academic catalog</em>
</blockquote>

<strong>📋 Administrative Procedures:</strong>
<blockquote style="border-left: 4px solid #5B0F1B; padding-left: 15px; margin: 10px 0;">
"How do I apply for a leave of absence?"<br>
<em>→ Provides step-by-step procedures from policy documents</em>
</blockquote>

<strong>🏫 Campus Resources:</strong>
<blockquote style="border-left: 4px solid #5B0F1B; padding-left: 15px; margin: 10px 0;">
"What support services are available for students?"<br>
<em>→ Lists available resources with contact information</em>
</blockquote>
</div>

## Future Improvements

We are currently in the process of testing the accuracy and usefulness of the chatbot, with planned enhancements including:

- **Enhanced Context Understanding**: Improved handling of complex multi-part questions
- **Source Citation**: Direct links to relevant policy sections
- **Multi-modal Support**: Integration of images and diagrams from documents
- **Real-time Updates**: Automatic synchronization with policy changes
- **Analytics Dashboard**: Usage patterns and common queries analysis
