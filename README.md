# ⚡️ AI Audio-to-Content Repurposing Engine

An end-to-end automated content processing pipeline built with **Activepieces**, **Deepgram AI**, **OpenRouter (Claude 3.5 Sonnet)**, **Notion**, and **Telegram Bot**.

This system monitors a Notion Database for incoming audio/video links, extracts speech via high-accuracy transcription, processes the transcript through Claude 3.5 Sonnet to generate platform-tailored scripts and posts, and instantly delivers the finalized content directly to a Telegram chat.

---

## 🎯 Features
* **Automated Triggering**: Continuously polls Notion for new audio/video entries without reprocessing duplicate items.
* **High-Accuracy Speech-to-Text**: Utilizes Deepgram's API for fast and precise audio transcription.
* **LLM Content Generation**: Leverages Claude 3.5 Sonnet via OpenRouter to generate:
  * 3x Short-Form Video Scripts (Hook, Body, CTA) optimized for high retention.
  * 1x Professional LinkedIn Post formatted with engaging structure & emojis.
* **Instant Delivery**: Pushes clean, ready-to-publish Markdown output straight to a Telegram channel/bot.

---

## 🏗️ Architecture & Workflow

```text
[ Notion Database ] 
        │ (New Video URL)
        ▼
[ Activepieces Orchestrator ]
        │
        ├─► 1. Deepgram API (Speech-to-Text Transcription)
        │
        ├─► 2. OpenRouter API / Claude 3.5 Sonnet (Script & Post Generation)
        │
        └─► 3. Telegram Bot API (Instant Notification & Output Delivery)