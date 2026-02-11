# OpenClaw Chat ⚡

A simple, beautiful chat interface for OpenClaw. Supports real-time streaming responses.

**Live Site:** https://chadeth.github.io/chat-openclaw/

## Quick Setup

### Step 1: Access the Chat
Visit: **https://chadeth.github.io/chat-openclaw/**

### Step 2: Configure Your OpenClaw Connection

Click **Settings** and enter:

1. **Gateway URL**: Your OpenClaw gateway address
   - Local: `http://localhost:18789`
   - Remote: Your tunnel URL (e.g., `https://your-tunnel.example.com`)

2. **Gateway Token**: Your OpenClaw authentication token
   - Found in `~/.openclaw/openclaw.json` under `gateway.auth.token`
   - Or check your OpenClaw config

3. **Model** (optional): Leave default or specify your preferred model

### Step 3: Start Chatting!

Type a message and press Enter (or click Send).

---

## For OpenClaw Admins

### Exposing Your Gateway

To use this chat app remotely, you need to expose your OpenClaw gateway:

**Option 1: Cloudflare Tunnel (Recommended)**
```bash
cloudflared tunnel --url http://localhost:18789
```

**Option 2: Tailscale Funnel**
```bash
tailscale funnel 18789
```

**Option 3: ngrok**
```bash
ngrok http 18789
```

### CORS Configuration

If you're accessing from a different domain, ensure your OpenClaw gateway allows CORS.
The gateway typically handles this automatically.

---

## Features

- ⚡ Real-time streaming responses (SSE)
- 🎨 Beautiful dark theme
- 💾 Settings saved to browser localStorage
- 📱 Mobile-friendly responsive design
- 🔒 All data stays in your browser - no server-side storage

## Technical Details

- Pure HTML/CSS/JavaScript - no build step required
- Connects directly to OpenClaw's OpenAI-compatible API (`/v1/chat/completions`)
- Uses Server-Sent Events (SSE) for streaming
- Works on any static hosting (GitHub Pages, Cloudflare Pages, etc.)

---

Made with ⚡ by Chadeth
