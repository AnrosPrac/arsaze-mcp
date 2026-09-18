# Arsaze MCP Server

Arsaze is an AI-native video editing platform — a real timeline, not a chat box.
This repo is the **public connector listing** for Arsaze's remote MCP server: it
documents how to connect, not the platform's source code (which is closed-source).

Connect an MCP-capable client to an Arsaze project and every tool call the agent
makes plays back live in the editor — timeline edits, color grades, generation,
renders — as it happens. Full manual editing (timeline, trim modes, color wheels,
keyframes) is always available too; the agent is an operator you can hand the
controls to, not a requirement.

## Connect

- **Endpoint:** `https://api.arsaze.com/mcp`
- **Transport:** Streamable HTTP
- **Auth:** OAuth 2.1 with PKCE — you'll be prompted to sign in to your Arsaze
  account and authorize the connecting client on first use. No API keys to copy
  around.
- **Docs:** https://arsaze.com/docs/mcp

### Supported clients today

Claude, ChatGPT, and Grok are supported as MCP clients:

- **Claude:** Settings → Connectors → Add custom connector
- **ChatGPT:** add as a custom MCP plugin using the server URL
- **Grok:** grok.com/connectors → New Connector → Custom

Any other client that supports remote MCP servers over Streamable HTTP with
OAuth 2.1 can connect using the endpoint above — the server advertises its
OAuth metadata per the standard MCP discovery flow.

## What you can do with it

- **Projects & assets** — list/create projects, search the asset library, upload
- **Timeline editing** — add/trim/split/ripple-delete clips, transitions, render
- **Color & effects** — LUTs, color wheels, RGB curves, HSL secondary, cinematic looks
- **Audio** — voiceover generation, auto-ducking, loudness normalization, SFX
- **Generation** — video, avatar video, voice cloning, thumbnails, image/music/SFX
- **Captions** — auto-generate and manage caption sets
- **Review** — shareable review links, comment threads, director briefs

Full tool list is discoverable via the MCP `tools/list` method once connected.

## Support

Issues connecting or using the Arsaze MCP server: https://arsaze.com/contact

## License / Access

Arsaze is a commercial product. This repository contains connection
documentation only; the Arsaze platform itself is closed-source.
