[English](./README.md) | [中文](./README_zh.md)


## Maintainer

**Melon (李辉)** is an AI full-stack engineer and the founder of [FantasyAI Lab](https://fantasyailab.com/). He builds reliable AI agents, multi-agent systems, and practical AI products. The official portfolio and profile are available at [fantasyailab.com](https://fantasyailab.com/) and [Melon (李辉) profile](https://fantasyailab.com/melon-lihui.html).


# Sidonie


**An intelligent companion that unifies chat, notes, study, and academic workflows — a Manus product born from real daily life.**


Sidonie is named after my wife and inspired by our little one, Dua. Their everyday friction with AI — the small frustrations and unmet needs — is what led to this product. I believe technology should start with the people closest to us: if it works for them, it can work for everyone. So Sidonie is a local-first, React-based interface that brings structured planning, file analysis, learning modules, and notes into one place — no backend required, just you and your API keys.


### Screenshots


<p align="center">
  <strong>Homepage</strong> — Chat entry, model selection
</p>
<p align="center">
  <img src="docs/screenshots/homepage.png" width="80%" alt="Homepage" />
</p>


<p align="center">
  <strong>Paper Radar</strong> — Discover & analyze arXiv, daily briefing
</p>
<p align="center">
  <img src="docs/screenshots/paper-radar.png" width="80%" alt="Paper Radar" />
</p>


<p align="center">
  <strong>Help Child</strong> — AI teaching assistant, curriculum
</p>
<p align="center">
  <img src="docs/screenshots/help-child.png" width="80%" alt="Help Child" />
</p>


## 1. Project Overview


**Sidonie** is an open-source front-end application that brings together:


- **Unified chat** with multi-session support, file uploads (PDF, Word, CSV, images), and streaming responses.
- **Structured reasoning** via `<plan>` and `<thought>` in model output for complex or multi-step tasks.
- **Notes** with tags and themes, persisted locally.
- **Study** module: curriculum (stages/topics), concept/quiz/visual cards, XP and badges, school notes, and review scheduling.
- **Academic** module for browsing and managing paper-like entries.


The stack is **React 19 + TypeScript + Vite**, with **Tailwind CSS** for UI. The AI layer talks to **Google Gemini** by default and can be extended with **DeepSeek, Kimi, Qwen** via API keys. No backend required for basic use — run locally and point to your API keys.


## 2. Architecture & Technical Solution


- **Front-end:** Single-page app (React 19, TypeScript, Vite). Views: Chat, Notes, Study, Academic.
- **AI integration:** `services/geminiService` — streaming chat, image generation, token estimation, optional Google Search grounding. Third-party models use the same service interface with configurable base URLs and keys.
