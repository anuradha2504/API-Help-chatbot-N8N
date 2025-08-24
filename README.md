# API-Help-chatbot-N8N

📖  API Help Chatbot

An intelligent chatbot designed to provide API help documentation instantly. This bot integrates with Google Drive, Pinecone, penAI, and Telegram using an n8n automation pipeline.

🚀 Features

📂 Fetches API help files stored in Google Drive

🔍 Converts documents into embeddings using OpenAI
📊 Stores and searches embeddings efficiently with Pinecone Vector DB
🤖 Uses OpenAI Chat Model to generate natural language answers
🔗 Automated workflows managed via n8n
💬 Seamless Telegram Bot integration for end-user interaction

🛠️ Tech Stack

n8n : Workflow automation for orchestrating tasks OpenAI : Embeddings & chat-based responses Pinecone : Vector database for semantic search Telegram Bot API : Messaging and triggers Google Drive API: Document storage and retrieval

Architecture Flow 🔹 Workflow Diagram (Mermaid) flowchart TD A[📂 Google Drive API] -->|Fetch Help Docs| Store API help documentation (PDF, DOCX, TXT, etc.) B[n8n Workflow] B -->|Convert to Embeddings| C[🔎 OpenAI Embeddings] C -->|Store & Search| D[📊 Pinecone Vector DB] D -->|Retrieve Relevant Context| E[🤖 OpenAI Chat Model] E -->|Answer Generated| F[💬 Telegram Bot]

🔹 ASCII Flow [Google Drive Docs] --> [n8n Workflow] --> [OpenAI Embeddings] --> [Pinecone Vector DB] | v [OpenAI Chat Model] --> [Telegram Bot]

📦 Setup Instructions

Clone Repository git clone https://github.com/anuradha2504/api-help-chatbot.git cd api-help-chatbot

Environment Variables

Create a .env file and configure the following:

OPENAI_API_KEY=your_openai_key PINECONE_API_KEY=your_pinecone_key PINECONE_ENVIRONMENT=your_pinecone_env GOOGLE_DRIVE_API_KEY=your_gdrive_key TELEGRAM_BOT_TOKEN=your_telegram_bot_token

Setup n8n
Install n8n

Import the provided workflow JSON (/workflows/api_help_chatbot.json)

Configure credentials for Google Drive, Pinecone, OpenAI, and Telegram

Deploy Pinecone Index Create an index (e.g., api-help-chatbot) Set dimension to match OpenAI embeddings (e.g., 1536 for text-embedding-ada-002)

Run the Bot Start n8n: n8n start

Now send a message to your Telegram bot, and it will reply with API help answers. 📌 Example Usage

User (Telegram): "How do I authenticate with the API?" Bot: Searches embeddings in Pinecone → Finds relevant docs → Generates response using OpenAI → Replies with explanation.

🔮 Future Enhancements ✅ Add multi-language support ✅ Support for Slack, Teams, or WhatsApp integration ✅ Caching for faster repeated queries ✅ Admin dashboard for monitoring usage and updating documents

👨‍💻 Author

Built by Anuradha Kumari using automation, AI, and messaging.
