# Nexus Deploy Checklist — Super Agent Party

## Requirements
- Docker + Docker Compose (Linux)
- 8GB RAM minimum (16GB recommended)
- No GPU required — Ollama handles LLM locally
- Port 3456 open locally

## Step-by-Step (execute when Nexus is online)
```bash
# 1. Clone fork
git clone https://github.com/kevinleestites2-dev/super-agent-party
cd super-agent-party

# 2. Launch
docker-compose up -d

# 3. Access UI
open http://localhost:3456

# 4. Configure LLM
# Settings → LLM Provider → OpenAI Compatible
# Base URL: [Ollama bridge URL from TOOLS.md]
# Model: llama3 or mistral

# 5. Load Ghost Persona
# Companion → Upload VRM model
# Set name, personality, voice (ElevenLabs key in TOOLS.md)

# 6. Enable Live Stream
# Streaming → YouTube → add API key
# Streaming → Twitch → add stream key

# 7. Telegram reporting
# Messaging Bots → Telegram → token from TOOLS.md
```

## Status: QUEUED — activate when Nexus lands
