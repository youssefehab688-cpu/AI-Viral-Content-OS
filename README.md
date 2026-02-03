# 🚀 n8n Smart Content Engine (AI-Powered)

![n8n](https://img.shields.io/badge/n8n-Workflow-ff6d5a?style=for-the-badge&logo=n8n)
![Groq](https://img.shields.io/badge/AI-Groq%20(Llama3)-000000?style=for-the-badge)
![Airtable](https://img.shields.io/badge/CMS-Airtable-blue?style=for-the-badge&logo=airtable)
![Apify](https://img.shields.io/badge/Scraping-Apify-97ce5d?style=for-the-badge&logo=apify)

> **Turn a single link or topic into a full content ecosystem instantly.**

## 🌟 Overview

Content creation is exhausting. Researching, scripting, and repurposing content for multiple platforms takes hours.
I built **Smart Content Engine**, a fully automated pipeline that acts as your personal AI Content Agency. It takes a raw input (Article URL or Topic), analyzes it, and generates ready-to-publish assets for YouTube, Twitter/X, and LinkedIn—all organized in a custom Client Dashboard.

---

## 📸 The Workflow
*(The brain behind the automation)*

![Workflow Diagram](https://github.com/user-attachments/assets/b6c54867-a62d-46e2-837c-75432e9f5413)

## 📊 Client Dashboard (Airtable)
*(Where the magic happens - Rich Text formatted scripts & assets)*

![Airtable Dashboard](https://github.com/user-attachments/assets/a4bff779-62a9-4ab3-bb3f-cdb698300110)

---

## 🔥 Key Features

* **🧠 Intelligent Input Handling:** Automatically detects if the input is a URL (scrapes it via Apify) or a raw Topic (researches via LLM).
* **🕷️ Smart Scraping:** Uses Apify's official crawler to extract clean Markdown from any website.
* **✍️ Viral Scripting:** Generates engaging YouTube scripts with proper formatting (Hooks, Intros, Body, CTA) using Llama 3 (via Groq).
* **♻️ Viral Pack Generator:** Automatically repurposes the script into:
    * A 5-Posts **X Thread**.
    * A professional **LinkedIn Post**.
    * High-volume **SEO Tags**.
* **💾 Centralized CMS:** Saves everything to Airtable with Rich Text formatting for easy review and editing.

---

## 🛠️ Tech Stack

* **n8n:** The orchestration engine connecting all services.
* **Groq (Llama 3-70b):** Ultra-fast inference for high-quality writing.
* **Apify:** For reliable web scraping and content extraction.
* **Airtable:** As the database and client-facing dashboard (CMS).
* **Telegram:** The trigger interface (Input via chat).

---

## ⚙️ How It Works (Under the Hood)

1.  **Trigger:** User sends a link or topic to the Telegram Bot.
2.  **Routing:** The workflow checks the input type.
    * *If Link:* Triggers Apify to crawl the content.
    * *If Topic:* Passes directly to the AI for creative generation.
3.  **Generation:** Groq AI processes the data and writes a structured script (Markdown).
4.  **Repurposing:** A secondary AI step converts the script into a JSON object containing social media posts.
5.  **Storage:** Data is mapped and pushed to Airtable fields (Rich Text enabled).
6.  **Notification:** The bot replies with a confirmation and the generated script preview.

---

## 🚀 How to Use This Workflow

1.  **Clone the Repo:** Download the `workflow.json` file from this repository.
2.  **Import to n8n:** Open your n8n instance > Workflows > Import from File.
3.  **Setup Credentials:** You will need API keys for:
    * Telegram Bot
    * Groq Cloud
    * Apify
    * Airtable (Personal Access Token)
4.  **Configure Airtable:** Create a base with columns: `Topic`, `Source URL`, `Script` (Rich Text), `X Thread`, `LinkedIn Post`, `SEO Tags`.
5.  **Run:** Activate the workflow and start sending links!

---

## 👨‍💻 Author

Built with ❤️ by **[YoussefEhab]**
* **Automation Specialist & Full-Stack Developer**
* Open for Freelance work & Collaborations.

[Connect on LinkedIn](https://www.linkedin.com/in/youssef-ehab-086750146)!
