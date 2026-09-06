---
name: init-auto4pi.agent
description: Automated workflow guide based on session work — web access, browser automation, YouTube transcripts, GitHub auth, and skill setup.
---

# Auto Workflow Skill

This skill covers the full setup and automation workflow completed in the session.

## What Was Done

### 1. Web Access Extension
- Installed: `npm install npm:pi-web-access`
- Provides web search, fetch, source-check capabilities

### 2. Skills Collection (`badlogic/pi-skills`)
- Cloned to `~/.pi/agent/skills/pi-skills/`
- Includes: brave-search, browser-tools, youtube-transcript, vscode, gccli, gdcli, gmcli, transcribe

### 3. Browser Tools Setup
- Key: Chrome needs `--remote-debugging-port=9222` + `--user-data-dir=C:\Users\admin\chrome-debug-profile`
- Created `Downloads/ai.agent/wakeup.bat`
- Commands tested:
  - `browser-nav.js <url>`
  - `browser-eval.js '<js>'`
  - `browser-screenshot.js`
  - `browser-content.js <url>`
  - `browser-cookies.js`

### 4. YouTube Transcript
- Installed in `youtube-transcript/`
- Tested with `node transcript.js dQw4w9WgXcQ`

### 5. GitHub Auth (`gh`)
- Completed device auth flow (`gh auth login`)
- Saved permanently; verified with `gh repo list --limit 5`

### 6. Real Automation Example
- Navigated to `github.com/search?q=pi-coding-agent`
- Extracted repo data via JavaScript evaluation
- Captured screenshot to `Downloads/ai.agent/`
- Clicked "Sign in" using `document.querySelector('...').click()`

## Quick Commands

Launch Chrome for automation:
```bash
C:\Users\admin\Downloads\ai.agent\wakeup.bat
```

Navigate:
```bash
node browser-nav.js https://github.com/subirdkimo
```

Evaluate JS:
```bash
node browser-eval.js "document.title"
```

YouTube transcript:
```bash
node youtube-transcript/transcript.js <video-id>
```

GitHub repos:
```bash
gh repo list --limit 5
```

Screenshot saves to `Downloads/ai.agent/` (configured).
