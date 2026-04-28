# 🚀 Agentic API Orchestration & AI Automations

A repository of autonomous, multi-step n8n workflows integrating Large Language Models (LLMs) for data synthesis, multimodal generation, and seamless API orchestration. 

## 📂 Workflows Included

This collection contains several exported n8n JSON workflows designed to automate complex tasks with zero manual friction:

* **🎙️ AI Audio Summarization and Speech Generation**
    * *Flow:* Triggers via chat, processes audio using Groq's translation/transcription API, and utilizes Gemini for advanced LLM chain processing.
* **💼 AI Job Seeker**
    * *Flow:* Scheduled automation that reads job postings from RSS feeds, uses Gemini to extract structured technical skills, formats personalized cover letters, and logs the data into Google Sheets.
* **📰 AI News Summarizer**
    * *Flow:* Aggregates multiple tech and AI RSS feeds, merges the data payloads, and uses Gemini to generate a cohesive daily news summary.
* **🖼️ AI Thumbnail Generator (with Frontend)**
    * *Flow:* Webhook-driven architecture that receives a text prompt, interfaces with the Freepik API for image generation, checks processing status, and returns the generated binary image.
* **🎧 AI Podcast Generator (with Frontend)**
    * *Flow:* Accepts text via webhook, structures a conversational podcast script using Gemini, and generates high-quality voice audio using the Murf.ai API.
* **📝 LinkedIn Article Posting (with Frontend)**
    * *Flow:* Ingests raw article text via webhook, uses dual Gemini LLM chains to extract insights and actionable advice, and adapts it into a sub-200-word post optimized for social media.
* **🗣️ Podcast Generator (Chatbot)**
    * *Flow:* An interactive chat-triggered workflow that acts as an expert scriptwriter, converting user topics into engaging 2-minute podcast scripts and routing them to TTS endpoints.

## 🛠️ Tech Stack & Integrations

* **Core Orchestration:** [n8n](https://n8n.io/)
* **AI / LLMs:** Google Gemini (Chat Models), LangChain (n8n nodes)
* **APIs:** Groq API (Audio translation), Murf.ai API (TTS), Freepik API (Image Generation)
* **Data Handling:** Google Sheets API, RSS Feed Readers, Webhooks, HTTP Requests, Structured Output Parsers

## 🚀 How to Use (Installation)

1. Set up a local or cloud instance of [n8n](https://n8n.io/).
2. Open your n8n workspace and create a **New Workflow**.
3. Click on the **Options** menu (three dots) in the top right corner of the canvas.
4. Select **Import from File...** and choose any of the `.json` files in this repository.
5. **Configure Credentials:** You will need to update the authentication credentials in the respective nodes (e.g., entering your own Groq API keys, Murf.ai keys, Google Sheets OAuth, and Gemini API keys).
6. Click **Test Workflow** to run manually, or toggle the **Active** switch for schedule/webhook triggers.

---
*Maintained by Charan Sri Dev*
