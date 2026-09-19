# 🌦️ Weather Email Automation

My first n8n automation workflow, built to automatically fetch current
weather data and send a daily weather update through Gmail.

## 🔄 Workflow

Schedule Trigger → OpenWeatherMap → Gmail

### How It Works

1. **Schedule Trigger**
   - Starts the workflow automatically at the configured time.

2. **OpenWeatherMap**
   - Fetches current weather information using the OpenWeatherMap API.
   - Returns data such as temperature, humidity and weather conditions.

3. **Gmail**
   - Uses the weather data received from OpenWeatherMap.
   - Sends the weather update automatically through Gmail.

## 🧠 What I Learned

Building this workflow helped me understand:

- Basic workflow automation with n8n
- Connecting and configuring nodes
- Working with APIs
- Reading JSON responses
- Passing data between nodes
- Using n8n expressions such as `{{ $json.main.temp }}`
- API authentication
- Gmail API integration
- Google OAuth 2.0
- OAuth redirect URIs and test users

## 🛠️ Tech Stack

- n8n (Self-hosted)
- Docker
- OpenWeatherMap API
- Gmail API
- Google OAuth 2.0

## 📁 Workflow File

The complete n8n workflow is available in [`workflow.json`](workflow.json).

You can import this JSON file into n8n and configure your own
OpenWeatherMap and Gmail credentials.

> No API keys, OAuth tokens, passwords, or other secrets are included.

## 📸 Workflow Preview

![Weather Email Automation](screenshots/workflow.png)