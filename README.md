# Email-Action-Intelligence-Agent

## Introduction
An AI-powered email intelligence agent that automatically retrieves emails from Gmail, aggregates the content, and analyzes it using OpenAI. The system generates structured daily digest reports containing key insights, priority issues, and actionable items, delivering them as professionally formatted HTML emails through an automated n8n workflow.

## Technologies Used
*   **Workflow Automation:** n8n
*   **AI & NLP:** OpenAI GPT-4
*   **APIs & Auth:** Gmail API, OAuth 2.0
*   **Web Technologies:** JavaScript, HTML, CSS, JSON
*   **Deployment:** Docker, Cloudflare Tunnel

## How It Works

<img width="1470" height="842" alt="Orchestration" src="https://github.com/user-attachments/assets/3d3b74b4-ab69-403f-9135-f635e0c91b84" />

1.  **Scheduled Trigger:** A chron-based trigger initiates the n8n workflow at a designated time each day.
2.  **Data Retrieval:** The Gmail node securely authenticates via OAuth 2.0 and fetches emails received over the past 24 hours.
3.  **Data Aggregation:** Key fields (sender, recipient, subject, labels, snippets) are extracted and combined into a structured dataset.
4.  **AI Analysis:** The aggregated dataset is routed to OpenAI GPT-4, which performs contextual cross-email analysis to extract key insights, critical issues, and specific action items.
5.  **Report Generation:** The structured JSON output from OpenAI is parsed and injected into a responsive HTML/CSS template.
6.  **Automated Delivery:** The final HTML digest report is automatically emailed back to the user for quick review.

## Features
*   **Automated Briefings:** Hands-free daily email summarization and inbox filtering based on Gmail categories.
*   **Deep Contextual Analysis:** AI-powered extraction of insights and action items across multiple related emails.
*   **Professional Output:** Clean, responsive HTML email reports generated from structured JSON data.
*   **Secure Integration:** Safe authentication via OAuth 2.0 and the Gmail API.
*   **Self-Hosted & Secure:** Containerized deployment via Docker with secure public webhook access via Cloudflare Tunnel.
*   **Highly Extensible:** Workflow can be easily adapted to push summaries to Slack, Telegram, or Notion.

## Output

<img width="1312" height="1276" alt="Mail_Response" src="https://github.com/user-attachments/assets/83cc1adf-5dd0-49e0-a0dc-fe3621ff4026" />


