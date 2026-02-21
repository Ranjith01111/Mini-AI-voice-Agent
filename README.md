# Mini AI Voice Agent

A bilingual (Tamil & English) AI voice agent powered by [LiveKit Agents](https://docs.livekit.io/agents/) and Google Gemini (`gemini-2.0-flash-exp`). The agent speaks in a natural Tamil–English mix, addresses the user by name, and includes real-time noise cancellation.

---

## Features

- Real-time voice conversation via LiveKit
- Bilingual responses (Tamil + English)
- Google Gemini 2.0 Flash real-time model
- LiveKit built-in noise cancellation (BVC)
- Configurable personality through `prompt.py`

---

## Prerequisites

- Python 3.9+
- A [LiveKit Cloud](https://cloud.livekit.io/) account (or self-hosted LiveKit server)
- A Google AI API key with access to Gemini

---

## Setup

1. **Clone the repository**

   ```bash
   git clone https://github.com/Ranjith01111/Mini-AI-voice-Agent.git
   cd Mini-AI-voice-Agent
   ```

2. **Create and activate a virtual environment**

   ```bash
   python -m venv venv
   source venv/bin/activate   # Windows: venv\Scripts\activate
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment variables**

   Create a `.env` file in the project root:

   ```env
   LIVEKIT_URL=wss://<your-livekit-project>.livekit.cloud
   LIVEKIT_API_KEY=<your-api-key>
   LIVEKIT_API_SECRET=<your-api-secret>
   GOOGLE_API_KEY=<your-google-api-key>
   ```

5. **Run the agent**

   ```bash
   python agent.py dev
   ```

---

## Project Structure

```
Mini-AI-voice-Agent/
├── agent.py          # Main agent entry point
├── prompt.py         # Agent instructions and response style
├── requirements.txt  # Python dependencies
└── .env              # Environment variables (not committed)
```

---

## Customization

Edit `prompt.py` to change the agent's personality, language style, or the name it uses to address the user.

---

## How to Exclude This Repository from GitHub Copilot

By default, when GitHub Copilot is enabled for your account or organisation, it may have access to all repositories. Follow these steps to **uncheck (exclude) this repository** so that Copilot no longer uses its code as context.

### For personal accounts

1. Go to **GitHub.com** and sign in.
2. Click your profile picture → **Settings**.
3. In the left sidebar, select **Copilot**.
4. Under **"GitHub Copilot"**, find the **Repository access** section.
5. Locate **Mini-AI-voice-Agent** in the list and **uncheck** (deselect) it.
6. Click **Save** to apply the change.

### For organisations

1. Go to your **Organisation settings** on GitHub.
2. In the left sidebar, select **Copilot** → **Policies**.
3. Under **Repository access**, find **Mini-AI-voice-Agent** and **uncheck** it.
4. Click **Save**.

### Using a `.copilotignore` file (content-level exclusion)

You can also prevent specific files in this repository from being used as Copilot context by creating a `.copilotignore` file in the project root. It follows the same syntax as `.gitignore`:

```
# Exclude environment and secret files
.env
venv/
__pycache__/
```

> **Note:** The repository-level toggle controls whether Copilot indexes the repository at all. The `.copilotignore` file controls which *files within* the repository are excluded from Copilot suggestions.

---

## License

This project is provided as-is for educational purposes.
