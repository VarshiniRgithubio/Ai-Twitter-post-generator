🧠 AI-Powered News Tweet Generator (n8n Workflow)

This project is an automated AI workflow built in n8n that generates insightful and educational news-style tweets using the Google Gemini model and posts them automatically to Twitter (X).

It is designed for creators, journalists, and marketers who want to post factual, professional, and concise tweet updates — powered by AI and real-time search.

🚀 Features

💬 Chat Trigger: Starts when a chat message or topic is received.

🧠 AI Agent (LangChain): Uses Gemini to generate tweet-style content based on a given title or topic.

🔎 SerpAPI Integration: Enhances AI responses with live search results for factual accuracy.

🗂️ Memory: Keeps short-term context across multiple chat sessions.

🐦 Twitter Integration: Automatically posts the generated tweet to your connected X (Twitter) account.

⚙️ Fully Automated: End-to-end automation — from topic input to publishing.

🧩 Workflow Overview
Nodes Used:
Node Name	Type	Description
When chat message received	@n8n/n8n-nodes-langchain.chatTrigger	Starts the workflow when a chat input is received.
AI Agent	@n8n/n8n-nodes-langchain.agent	Core logic that interprets the topic and creates an educational tweet.
Google Gemini Chat Model	@n8n/n8n-nodes-langchain.lmChatGoogleGemini	Provides the AI language model used to generate tweets.
Simple Memory	@n8n/n8n-nodes-langchain.memoryBufferWindow	Stores temporary context during workflow execution.
SerpAPI	@n8n/n8n-nodes-langchain.toolSerpApi	Retrieves factual web data to enrich tweets.
Create Tweet	n8n-nodes-base.twitter	Publishes the AI-generated tweet on Twitter (X).
🧠 AI Prompt Logic

The AI agent is instructed with a system message that ensures all generated tweets are:

Professional and factual

Written in the tone of breaking news or key announcements

Short, clear, and educational

Include 1–2 relevant hashtags for reach

Avoid personal opinions or clickbait

Example system message:

You are a helpful assistant. I will give you a title or topic. 
Your job is to write a tweet that sounds like a news update but is insightful and educational.

Keep it short, clear, and professional.
Make it sound like breaking news or a key announcement.
Make sure it is educational and factual, not clickbait.
Use simple language, 1–2 short sentences.
Add 1–2 relevant hashtags to improve reach.
Do not include personal opinions, just facts or insights.

⚙️ Setup Instructions
1️⃣ Prerequisites

An n8n instance (self-hosted or cloud)

Active credentials for:

Google Gemini (PaLM) API

SerpAPI

Twitter (X) API

2️⃣ Import the Workflow

Open your n8n dashboard.

Click “Import from file” or “Import from clipboard.”

Paste this workflow JSON and click Import.

3️⃣ Add Credentials

In n8n, open Credentials and add:

Google Gemini(PaLM) Api account

SerpAPI account

Twitter OAuth2 Api

4️⃣ Trigger the Workflow

Send a chat message with a topic or title.

The workflow will:

Generate an insightful tweet via Gemini

Optionally gather supporting facts via SerpAPI

Automatically post to your Twitter (X) account

🧾 Example

Input:

“AI regulation updates”

AI Output Tweet:

Breaking: Global regulators tighten AI safety frameworks to ensure transparency and accountability. #AI #TechNews

🛠️ Tech Stack

n8n – Workflow automation platform

LangChain – AI orchestration layer

Google Gemini (PaLM) – Language model for tweet generation

SerpAPI – Search API for real-time facts

Twitter API – Tweet publishing

📜 License

This project is open-source and available under the MIT License
.

👩‍💻 Author

Varshini Ramesh
💬 AI Automation & Workflow Developer
🌐 Connect on LinkedIn
 | Twitter
