# 🤖 AI Gmail Agent

An AI-powered n8n workflow that combines a locally running Large Language Model with memory and Gmail capabilities.

The workflow allows a user to interact with an AI agent through chat while giving the agent access to Gmail as a tool when required.

## 🔄 Workflow

```text
                 ┌── Ollama Chat Model
                 │
Chat Trigger → AI Agent ── Simple Memory
                 │
                 └── Gmail Tool
```

### How It Works

1. **Chat Trigger**
   - Receives messages from the user through n8n's chat interface.
   - Passes the user's message to the AI Agent.

2. **AI Agent**
   - Processes the user's request.
   - Determines how to respond and whether an available tool needs to be used.
   - Coordinates the language model, memory, and Gmail tool.

3. **Ollama Chat Model**
   - Provides the Large Language Model used by the AI Agent.
   - Runs locally using Ollama instead of relying entirely on a cloud-hosted LLM.

4. **Simple Memory**
   - Maintains conversation context between messages.
   - Allows the agent to remember information from the current conversation.

5. **Gmail Tool**
   - Gives the AI Agent the ability to send emails when required.
   - Uses Gmail OAuth 2.0 authentication through Google Cloud.

## 🧠 What I Learned

Building this workflow helped me understand:

- AI Agents in n8n
- Connecting tools to an AI Agent
- Tool calling
- Running LLMs locally with Ollama
- Adding conversational memory to an agent
- Connecting Gmail as an AI tool
- Gmail API integration
- Google OAuth 2.0
- OAuth Client IDs and redirect URIs
- OAuth consent screens
- Test users and Google Auth Platform
- Debugging OAuth errors such as `redirect_uri_mismatch` and `access_denied`
- Self-hosting AI automation with Docker and n8n

## 🛠️ Tech Stack

- n8n (Self-hosted)
- Ollama
- Large Language Model (Local)
- Gmail API
- Google OAuth 2.0
- Docker

## 📁 Workflow File

The complete n8n workflow is available in [`workflow.json`](workflow.json).

To use the workflow yourself, import the JSON file into n8n and configure your own:

- Ollama model
- Gmail OAuth credentials
- Google Cloud OAuth application

> No passwords, OAuth tokens, client secrets, API keys, or other sensitive credentials are included in this repository.

## 🔐 OAuth Setup

The Gmail integration uses Google OAuth 2.0.

For a local n8n installation, the OAuth redirect URI follows the format:

```text
http://localhost:5678/rest/oauth2-credential/callback
```

The Google Cloud OAuth application must be configured with the appropriate redirect URI and Gmail API access.

## 📸 Workflow Preview

![AI Gmail Agent](screenshots/workflow.png)

## 🚀 Future Improvements

Possible improvements to this workflow include:

- Additional Gmail operations
- More AI tools
- Improved long-term memory
- Calendar integration
- Web search capabilities
- Multiple specialized AI agents
- RAG and knowledge-base integration
- Deployment beyond the local environment