# 🚀 N8N Automations
 
A collection of autonomous, multi-step [n8n](https://n8n.io/) workflows that combine LLMs (Google Gemini, Groq/Llama), speech & image generation APIs, and everyday productivity tools (Google Docs, Sheets, Calendar, Airtable, LinkedIn, Telegram, Gmail) into end-to-end automations — content generation, job hunting, media production, and daily assistants.
 
---
 
## 📂 Workflows Included
 
| Workflow | Trigger | What it does |
|---|---|---|
| 🎙️ **AI Podcast Generator (with Frontend)** | Webhook | Takes a topic via webhook, writes a ~2‑minute podcast script with Gemini, converts it to speech with Murf.ai, and downloads/returns the audio file. |
| 🗣️ **Podcast Generator (Chatbot)** | Chat | Conversational version — user gives a topic in chat, Gemini writes a friendly ~2-minute script, and the script is sent to Murf.ai for TTS. |
| 🔊 **AI Audio Summarization and Speech Generation** | Chat | Downloads an audio file, transcribes/translates it with Groq Whisper, summarizes it into clean bullet-point "minutes" with Gemini, then converts the summary back to speech via Murf.ai. |
| 📝 **Transcription Summarizer Agent** | Chat | Downloads a video/audio file, transcribes it with Groq Whisper, then an AI Agent creates a Google Doc, inserts the transcript, generates a structured summary, appends it, and returns the summary. |
| 🧾 **Voice to Invoice Agent** | Telegram | Listens for voice notes on Telegram, transcribes them with Gemini, extracts structured invoice data (customer, line items, totals) into JSON, renders an HTML invoice, converts it to PDF via PDFShift, and sends the PDF back on Telegram. |
| 🎵 **Song Generation** | Chat | Generates full song lyrics (verses/chorus/bridge) with Gemini from a user prompt, then submits them to the Suno API to produce an actual audio track. |
| 💼 **Automated LinkedIn Job Tracker with AI** | Scheduled | Reads job postings from an RSS/LinkedIn feed, uses Gemini with a structured output parser to extract skills and draft a tailored cover letter, and logs everything into an Airtable base. |
| 🔍 **AI Job Seeker** | Scheduled | Similar job-hunting flow — reads an RSS job feed, extracts skills + writes a cover letter with Gemini (structured output), and appends/updates the results in a Google Sheet. |
| 📰 **AI News Summarizer** | Scheduled | Aggregates multiple RSS/news sources, merges the payloads, and uses Gemini to compile a single daily AI/tech news digest emailed via Gmail. |
| 🌦️ **Weather Assistant** | Scheduled | Pulls current conditions from OpenWeatherMap, has Gemini turn them into a short, friendly daily plan (outfit, activity, reminder), and emails it via Gmail. |
| 📢 **Automated Social Media Content Generation with Image** | Google Sheets Trigger | Watches a Google Sheet for new article links, summarizes the article with Gemini, drafts a LinkedIn post, generates an AI image prompt, creates the image via the Freepik API, downloads it, and publishes the post + image directly to LinkedIn. |
| 📝 **LinkedIn Article Posting (with Frontend)** | Webhook | Accepts raw article text via webhook, summarizes key insights with one Gemini chain, reshapes it into an engaging LinkedIn post (with hooks/hashtags) with a second Gemini chain, and publishes it to LinkedIn. |
| 🖼️ **AI Thumbnail Generator (with Frontend)** | Webhook | Receives a text prompt via webhook, sends it to the Freepik Imagen3 API, polls for completion, retrieves the generated image, and returns it as a binary response. |
| 📚 **Learning Path Generator** | Chat | An AI Agent plans a day-by-day curriculum for any learning goal, researches real resources via SerpAPI, writes the full plan into a Google Doc, and schedules a calendar event for each day. |
 
---
 
## 🛠️ Tech Stack & Integrations
 
- **Orchestration:** [n8n](https://n8n.io/)
- **LLMs / AI Agents:** Google Gemini (Chat Models), Groq (Llama 3.3, Whisper), LangChain nodes (`@n8n/n8n-nodes-langchain`)
- **Speech:** Murf.ai (text-to-speech), Groq Whisper (speech-to-text / translation)
- **Image Generation:** Freepik API (Mystic, Imagen3)
- **Music Generation:** Suno API
- **Documents:** PDFShift (HTML → PDF)
- **Data & Productivity:** Google Docs, Google Sheets, Google Calendar, Airtable, Gmail
- **Feeds & Triggers:** RSS Feed Read, Schedule Trigger, Webhook, Chat Trigger, Telegram Trigger, Google Sheets Trigger
- **Structured Data:** LangChain Structured Output Parsers, custom Code (JavaScript) nodes
---
 
## 🚀 How to Use (Installation)
 
1. Set up a local or cloud instance of [n8n](https://n8n.io/).
2. Open your n8n workspace and create a **New Workflow**.
3. Click the **Options** menu (⋯) in the top-right corner of the canvas.
4. Select **Import from File...** and choose any `.json` file from this repository.
5. **Configure credentials.** Every workflow will need its own connections set up in n8n, for example:
   - Google Gemini (PaLM) API key
   - Groq API key
   - Murf.ai API key
   - Freepik API key
   - Suno API key
   - PDFShift API key
   - Google OAuth (Docs, Sheets, Calendar, Gmail)
   - Airtable OAuth / Personal Access Token
   - LinkedIn OAuth
   - Telegram Bot token
   - OpenWeatherMap API key
   - SerpAPI key
6. Click **Test Workflow** to run manually, or toggle **Active** for scheduled/webhook-based workflows.
> ⚠️ **Before importing or committing any workflow**, check the node parameters for hardcoded API keys and replace them with your own credentials or placeholder text (e.g. `YOUR_API_KEY_HERE`). Never commit real secrets to a public repository.
 
---
 
## 📁 Repository Structure
 
```
.
├── aipodcast_generator_with_frountend.json
├── podcast_ganerator.json
├── AI_Audio_Summarization_and_Speech_Generation.json
├── Transcription_Summarizer_Agent.json
├── voice_to_invoice_agent.json
├── song_generation.json
├── Automated_LinkedIn_Job_Tracker_with_AI.json
├── ai_job_seeker.json
├── AI_news_summarizer.json
├── weather.json
├── Automated_Social_Media_Content_Generation_with_Image.json
├── linkden_article_posting_workflow_with_frountend.json
├── ai_tumbnail_generating_workflow_with_frountend.json
├── Learning_path_generator.json
└── README.md
```
 
---
 
## 🤝 Contributing
 
Feel free to open a PR to add new workflows, fix node configurations, or improve documentation. Please scrub any personal credentials, webhook IDs, or API keys before submitting.
 
---
 
*Maintained by Charan Sri Dev*
 
