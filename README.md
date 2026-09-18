# Arsaze MCP Server

Arsaze is an AI-native video editing platform. This repo is the **public connector
listing** for Arsaze's remote MCP server — it documents how to connect, not the
platform's source code (which is closed-source).

Connect an MCP-capable client (Claude, ChatGPT, Cursor, etc.) to Arsaze to let an
AI agent drive real timeline editing, generation, and review workflows on your
Arsaze projects: cutting and arranging clips, color grading, captions, b-roll and
image/video/voice generation, transitions, exports, and review/share links — the
same editing surface available in the Arsaze app itself, exposed as MCP tools.

## Connect

- **Endpoint:** `https://api.arsaze.com/mcp`
- **Transport:** Streamable HTTP
- **Auth:** OAuth 2.1 with PKCE — you'll be prompted to sign in to your Arsaze
  account and authorize the connecting client on first use. No API keys to copy
  around.

### Claude Desktop / Claude Code

Add a remote MCP connector pointing at the endpoint above. See
[Claude's MCP connector docs](https://code.claude.com/docs/en/mcp-quickstart) for
the exact steps for your client.

### Other MCP clients

Any client that supports remote MCP servers over Streamable HTTP with OAuth 2.1
can connect using the endpoint above — the server advertises its OAuth metadata
per the standard MCP discovery flow.

## What you can do with it

- Timeline editing: add/move/trim/split/ripple-delete clips, transitions, gaps,
  speed ramps, keyframes
- Color: LUTs, color wheels, RGB curves, HSL secondary, color-grade matching
- Audio: track loudness/compression/EQ/noise reduction, ducking, auto-cut-silence
- Captions: auto-generate, edit, and manage caption sets
- Generation: image, video, voice, music, and SFX generation, plus b-roll
- Review: shareable review links, comment threads, director briefs
- Export: render and export finished timelines

Full tool list is discoverable via the MCP `tools/list` method once connected.

## Support

Issues connecting or using the Arsaze MCP server: <!-- TODO: support email/link -->

## License / Access

Arsaze is a commercial product. This repository contains connection
documentation only; the Arsaze platform itself is closed-source.
