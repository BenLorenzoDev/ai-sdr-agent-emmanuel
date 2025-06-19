# ai-sdr-agent-emmanuel
Prompt, logic, and test cases for Emmanuel King – AI Sales Development Rep built in n8n

# Emmanuel King — AI SDR Agent

This repository documents the behavior, prompts, logic, and test coverage for an AI Sales Development Rep named *Emmanuel King*, built to respond to email leads and book qualified meetings.

## 🛠 AI SDR Workflow — Version 1

![n8n-ai-sdr-workflow](https://github.com/user-attachments/assets/f3939046-71f9-451d-ab03-a891ee1b9db6)

**📌 Workflow Overview – Key Logic Points (v1):**

- **Trigger Node**: Activated when a new lead responds via email (e.g. webhook or polling inbox).
- **Context Builder**: Gathers lead name, email, message content, time zone, and campaign source.
- **Message Analyzer**: Classifies lead’s tone or intent (`Direct Interest`, `Skeptical`, etc.).
- **Prompt Composer**: Dynamically generates the OpenAI system and user prompts using structured templates.
- **OpenAI Node**: Responds in the voice of Emmanuel King, following SDR psychological frameworks and email format rules.
- **Formatter Node**: Converts OpenAI output into HTML email body with clean `<p>` and `<ul><li>` structure.
- **Delivery Node**: Sends the response via Instantly.ai or another email API (e.g. Gmail, Mailgun).
- **Optional: Calendar Checker**: (If needed) Queries availability or includes Calendly fallback link.
- **Logging & Alerts**: Logs response history and notifies internal Slack channel if booked.

---

🆕 *Future versions (v2, v3...) will include logic for lead scoring, intent tracking, and real-time CRM updates.*


## 🔍 Overview
Emmanuel is designed to:
- Respond like a confident, helpful SDR
- Book meetings without ever revealing he's AI
- Handle objections, vague replies, and off-topic questions smoothly

## 📁 Structure

- `prompt/system-prompt.md` — Short prompt version for OpenAI (n8n-ready)
- `tests/test-scenarios.xlsx` — Sample leads for QA
- `snippets/html-templates.md` — Email formatting examples
- `examples/sample-replies.md` — Realistic reply outputs by cue type

## 📅 Calendly Link

> [https://calendly.com/permasize/demo](https://calendly.com/permasize/demo)

## 🧪 Testing Strategy
Each test case in `test-scenarios.xlsx` maps to a cue type and expected tone/pattern. AI outputs are evaluated against:
- Staying in character
- Proper formatting
- CTA with 3 time slots or Calendly fallback


## 📄 License
MIT (or choose your preferred one)
