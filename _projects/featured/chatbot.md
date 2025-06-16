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
The analysis currently uses Python, Streamlit, Word embedding (all-MiniLM-L6-v2), language model (gpt-4o-mini), PDF extraction,  and web scrapping.

## Implementation
The chatbot is now in the testing phase
## Results
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chatbot Interface</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #EC5E1A 0%, #EC5E1A 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        .chatbot-wrapper {
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.1);
            overflow: hidden;
            width: 100%;
            max-width: 1200px;
            height: 90vh;
            display: flex;
            flex-direction: column;
        }
        .chatbot-header {
            background: linear-gradient(135deg, #5B0F1B 0%, #5B0F1B 100%);
            color: white;
            padding: 20px 30px;
            text-align: center;
            position: relative;
        }
        .chatbot-header h1 {
            margin: 0;
            font-size: 1.8rem;
            font-weight: 600;
        }
        .chatbot-header p {
            margin: 5px 0 0 0;
            opacity: 0.9;
            font-size: 0.95rem;
        }
        .chatbot-container {
            flex: 1;
            border: none;
            width: 100%;
            background: #f8f9fa;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1.1rem;
            color: #6c757d;
        }
        .features {
            background: #f8f9fa;
            padding: 15px 30px;
            border-top: 1px solid #e9ecef;
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            gap: 10px;
        }
        .feature {
            display: flex;
            align-items: center;
            color: #6c757d;
            font-size: 0.85rem;
        }
        .feature::before {
            content: "✓";
            color: #28a745;
            font-weight: bold;
            margin-right: 8px;
        }
        
        /* Floating chat button version */
        .chat-button {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 50%;
            border: none;
            color: white;
            font-size: 24px;
            cursor: pointer;
            box-shadow: 0 8px 25px rgba(0,0,0,0.15);
            transition: all 0.3s ease;
            z-index: 1000;
            display: none; /* Hidden by default, can be toggled with JavaScript */
        }
        .chat-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 12px 35px rgba(0,0,0,0.2);
        }
        .chat-modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.5);
            z-index: 1001;
            display: none;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        .chat-modal.active {
            display: flex;
        }
        .chat-modal-content {
            background: white;
            border-radius: 15px;
            width: 100%;
            max-width: 900px;
            height: 80vh;
            display: flex;
            flex-direction: column;
            overflow: hidden;
            position: relative;
        }
        .close-btn {
            position: absolute;
            top: 15px;
            right: 20px;
            background: none;
            border: none;
            font-size: 24px;
            color: white;
            cursor: pointer;
            z-index: 1002;
        }
        
        @media (max-width: 768px) {
            .chatbot-wrapper {
                height: 100vh;
                border-radius: 0;
                margin: 0;
            }
            
            .features {
                flex-direction: column;
                align-items: center;
            }
            
            .chat-button {
                bottom: 20px;
                right: 20px;
                width: 50px;
                height: 50px;
                font-size: 20px;
            }
        }
    </style>
</head>
<body>
    <!-- Main chatbot interface -->
    <div class="chatbot-wrapper">
        <div class="chatbot-header">
            <h1>AI Assistant</h1>
            <p>How can I help you today?</p>
        </div>
        
        <div class="chatbot-container">
            <!-- This is where you would embed your actual chatbot -->
            <p>Chatbot interface will be loaded here</p>
        </div>
        
        <div class="features">
            <div class="feature">24/7 Support</div>
            <div class="feature">Instant Responses</div>
            <div class="feature">Multi-language</div>
            <div class="feature">Secure & Private</div>
        </div>
    </div>

    <!-- Optional floating chat button (hidden by default) -->
    <button class="chat-button" onclick="toggleChat()">💬</button>
    
    <!-- Optional modal version -->
    <div class="chat-modal" id="chatModal">
        <div class="chat-modal-content">
            <div class="chatbot-header">
                <button class="close-btn" onclick="toggleChat()">&times;</button>
                <h1>AI Assistant</h1>
                <p>How can I help you today?</p>
            </div>
            <div class="chatbot-container">
                <p>Modal chatbot interface will be loaded here</p>
            </div>
            <div class="features">
                <div class="feature">24/7 Support</div>
                <div class="feature">Instant Responses</div>
                <div class="feature">Multi-language</div>
                <div class="feature">Secure & Private</div>
            </div>
        </div>
    </div>

    <script>
        function toggleChat() {
            const modal = document.getElementById('chatModal');
            const button = document.querySelector('.chat-button');
            
            if (modal.classList.contains('active')) {
                modal.classList.remove('active');
                button.style.display = 'block';
            } else {
                modal.classList.add('active');
                button.style.display = 'none';
            }
        }
        
        // Show floating button on scroll (optional)
        window.addEventListener('scroll', function() {
            const button = document.querySelector('.chat-button');
            if (window.scrollY > 300) {
                button.style.display = 'block';
            } else {
                button.style.display = 'none';
            }
        });
    </script>
</body>
</html>

## Future Improvements

We are currently in the process of testing the accuracy and usefulness of the chatbot
