# ⚡️ AI Audio-to-Content Repurposing Engine

An end-to-end automated content processing pipeline built with **Activepieces**, **Deepgram AI**, **OpenRouter (Claude 3.5 Sonnet)**, **Notion**, and **Telegram Bot**.

This system monitors a Notion Database for incoming audio/video links, extracts speech via high-accuracy transcription, processes the transcript through Claude 3.5 Sonnet to generate platform-tailored scripts and posts, and instantly delivers the finalized content directly to a Telegram chat.

---

## 🛠️ Tech Stack & Architecture

* **Orchestration**: [Activepieces](https://www.activepieces.com/)
* **Database / Source Input**: [Notion API](https://developers.notion.com/)
* **Transcription Engine**: [Deepgram Speech AI](https://deepgram.com/)
* **LLM Provider**: [OpenRouter](https://openrouter.ai/) (Claude 3.5 Sonnet)
* **Output Channel**: [Telegram Bot API](https://core.telegram.org/bots/api)

### 🔄 Data Flow
* **Notion Database** ➔ *(New Video URL)*
* **Activepieces Orchestrator**:
  1. **Deepgram API** *(Speech-to-Text Transcription)*
  2. **OpenRouter / Claude 3.5 Sonnet** *(Script & Post Generation)*
  3. **Telegram Bot API** *(Instant Notification & Output Delivery)*

---

## 🎯 System Features & Capabilities

* **Automated Polling**: Continuously monitors Notion for new entries without reprocessing duplicate items.
* **High-Accuracy Speech-to-Text**: Transcribes audio and video files using Deepgram's API.
* **Smart Content Generation**: Generates 3x Short-Form Video Scripts (Hook, Body, CTA) and 1x LinkedIn Post using Claude 3.5 Sonnet.
* **Instant Delivery**: Formats the output with clean Markdown and pushes it to Telegram instantly.

---

## 📖 How to Use (طريقة الاستخدام)

1. **Add Media to Notion**:
   * Open your configured Notion database.
   * Create a new row, set the title, and paste the direct link of the audio/video file into the `Video URL` column.

2. **Automated Processing**:
   * The Activepieces workflow automatically detects the new item.
   * It sends the link to Deepgram for speech recognition, passes the transcription to Claude 3.5 Sonnet via OpenRouter, and formats the output.

3. **Receive Content**:
   * Open Telegram to receive a formatted message with 3 video scripts and a ready-to-publish LinkedIn post.

---

## 🚀 Setup & Installation (خطوات الإعداد)

1. **Notion Setup**:
   * Create a Notion Database with two properties: `Title` (Title) and `Video URL` (URL).

2. **Import Workflow**:
   * Download the `workflow.json` from this repository.
   * Import it into your Activepieces workspace.

3. **Configure API Keys**:
   * Connect your accounts/keys for Notion, Deepgram, OpenRouter, and Telegram Bot Token.

4. **Publish**:
   * Test the pipeline with a sample audio URL, then click **Publish**.

---

## ⚖️ Rights & License (حقوق الملكية والاستخدام)

* **Author**: Youssef Amr (جو)
* **Role**: Automation Specialist & Developer
* **License**: MIT License – Free to use, modify, and distribute with attribution to the original author.

---
© 2026 **Youssef Amr**. All rights reserved.
