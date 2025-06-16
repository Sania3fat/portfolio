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

<div style="background: linear-gradient(135deg, #EC5E1A 0%, #EC5E1A 100%); padding: 40px 20px; border-radius: 10px; margin: 20px 0;">
  <div style="background: white; border-radius: 20px; box-shadow: 0 8px 32px rgba(0,0,0,0.1); overflow: hidden; max-width: 800px; margin: 0 auto;">
    
    <div style="background: linear-gradient(135deg, #5B0F1B 0%, #5B0F1B 100%); color: white; padding: 30px; text-align: center;">
      <h2 style="margin: 0; font-size: 2rem; font-weight: 600;">🤖 Institutional Assessment Assistant</h2>
      <p style="margin: 10px 0 0 0; opacity: 0.9; font-size: 1.1rem;">Ask me about Maryville College policies and procedures</p>
    </div>
    
    <div style="padding: 40px; background: #f8f9fa; text-align: center;">
      <div style="background: white; padding: 30px; border-radius: 15px; margin-bottom: 20px; box-shadow: 0 4px 15px rgba(0,0,0,0.05);">
        <h3 style="color: #5B0F1B; margin-bottom: 15px;">💬 Interactive Chat Interface</h3>
        <p style="color: #6c757d; margin-bottom: 20px;">The chatbot provides real-time responses to questions about institutional documents and policies.</p>
        <div style="background: #e9ecef; padding: 15px; border-radius: 10px; font-family: monospace; text-align: left;">
          <strong>User:</strong> What are the graduation requirements?<br>
          <strong style="color: #5B0F1B;">Assistant:</strong> Based on the institutional documents, graduation requirements include...
        </div>
      </div>
      
      <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; margin-top: 30px;">
        <div style="background: white; padding: 20px; border-radius: 10px; text-align: center; box-shadow: 0 2px 10px rgba(0,0,0,0.05);">
          <div style="font-size: 2rem; margin-bottom: 10px;">📚</div>
          <strong style="color: #5B0F1B;">Document Analysis</strong>
          <p style="font-size: 0.9rem; color: #6c757d; margin-top: 8px;">Processes academic catalogs and policy documents</p>
        </div>
        
        <div style="background: white; padding: 20px; border-radius: 10px; text-align: center; box-shadow: 0 2px 10px rgba(0,0,0,0.05);">
          <div style="font-size: 2rem; margin-bottom: 10px;">🔍</div>
          <strong style="color: #5B0F1B;">Smart Search</strong>
          <p style="font-size: 0.9rem; color: #6c757d; margin-top: 8px;">Uses semantic embeddings for accurate retrieval</p>
        </div>
        
        <div style="background: white; padding: 20px; border-radius: 10px; text-align: center; box-shadow: 0 2px 10px rgba(0,0,0,0.05);">
          <div style="font-size: 2rem; margin-bottom: 10px;">⚡</div>
          <strong style="color: #5B0F1B;">Real-time Response</strong>
          <p style="font-size: 0.9rem; color: #6c757d; margin-top: 8px;">Powered by GPT-4o-mini for instant answers</p>
        </div>
      </div>
    </div>
    
    <div style="background: #f8f9fa; padding: 20px; border-top: 1px solid #e9ecef;">
      <div style="display: flex; justify-content: space-around; flex-wrap: wrap; gap: 15px; align-items: center; font-size: 0.9rem; color: #6c757d;">
        <div>✅ <strong>RAG Architecture</strong></div>
        <div>✅ <strong>Semantic Search</strong></div>
        <div>✅ <strong>Policy Compliance</strong></div>
        <div>✅ <strong>Multi-format Support</strong></div>
      </div>
    </div>
    
  </div>
</div>

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
