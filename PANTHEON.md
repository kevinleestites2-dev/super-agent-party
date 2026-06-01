# Super Agent Party — Pantheon Integration
**Forked for the Pantheon | 2026-05-31**  
**Source:** https://github.com/heshengtao/super-agent-party  
**Status:** FORKED ✅ | Deploy Target: The Nexus

---

## Pantheon Role: Ghost Streamer Command Center

Super Agent Party consolidates multiple Pantheon layers into a single platform:

| SAP Feature | Pantheon Layer Replaced |
|---|---|
| VRM/Live2D Desktop Companion | PersonaLive (Ghost Face Layer) |
| Live Streaming Bot (YouTube/Twitch) | ContentPrime Ghost Streamer |
| Task Center (computer vision + control) | EleftheriaPrime / ZeroTap |
| Instant Messaging Bot (Telegram/Discord) | Pantheon Reporting Channel |
| AI Browser (autonomous web control) | OpenSkynet / SkynetPrime |
| MCP + OpenAI API interface | ZapiaPrime ↔ SAP bridge |
| Long-term memory + character cards | Persona consistency layer |
| Extension system (self-bootstrapping) | Pantheon skill expansion |

---

## Deploy on The Nexus (when live)

### Docker (fastest path)
```bash
docker pull ailm32442/super-agent-party:latest
docker run -d -p 3456:3456 -v ./pantheon-sap-data:/app/data ailm32442/super-agent-party:latest
```
Access at: http://localhost:3456

### Docker Compose (recommended — includes gateway + login management)
```bash
git clone https://github.com/kevinleestites2-dev/super-agent-party
cd super-agent-party
docker-compose up -d
```

### Source Code (Termux/Linux)
```bash
git clone https://github.com/kevinleestites2-dev/super-agent-party
cd super-agent-party
pip install uv
uv sync
python server.py
```

---

## Ghost Streamer Integration

1. Launch SAP on The Nexus
2. Configure VRM/Live2D model as Ghost Persona face
3. Point LLM to Ollama bridge (existing config in `pantheon.env`)
4. Enable Live Streaming Bot → YouTube + Twitch
5. Wire Telegram reporting → existing Pantheon bot token
6. Connect MCP interface → ZapiaPrime can command SAP directly

---

## Integration Queue
- [ ] Wire Ollama bridge as SAP LLM backend (zero API cost)
- [ ] Load Ghost Persona VRM model
- [ ] Enable YouTube + Twitch live stream bot
- [ ] Connect Telegram bot for Pantheon status reports
- [ ] Expose MCP endpoint → ZapiaPrime control bridge
- [ ] Link ContentPrime scripts → SAP voice/text pipeline
- [ ] Fine-tune persona with GhostPrime stealth layer

---

## Notes
- No VRAM requirement — runs CPU-only via Ollama
- Docker is the cleanest deploy path on The Nexus
- MCP interface means ZapiaPrime can directly command SAP agents
- Extension system allows Pantheon-specific skills to be built inside SAP
- Long-term memory keeps Ghost Persona consistent across streams
