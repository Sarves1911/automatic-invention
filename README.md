# automatic-invention
Automated invoice follow-up system using n8n and OpenAI to detect unpaid invoices, generate personalized reminders, and send follow-up emails — all without manual intervention.



# 🧠 Smart Invoice Follow-up System with n8n & OpenAI

This project is a **Smart Invoice Follow-up Automation System** built using [n8n](https://n8n.io/) and [OpenAI](https://platform.openai.com/). It automates email follow-ups for unpaid invoices by checking their status, generating personalized reminder messages using OpenAI, and sending those messages to clients.


---

## ✨ Features

- Automatically reads invoice data (from Google Sheets or a database you can use stripr if you want to)
- Detects unpaid invoices
- Uses OpenAI to generate human-like follow-up messages
- Sends personalized emails to clients via Gmail or SMTP
- Scheduled workflows using n8n's built-in cron

---

## 🛠️ Tech Stack

- [n8n](https://n8n.io/) – Workflow automation tool
- [OpenAI API](https://platform.openai.com/) – GPT-based content generation
- Google Sheets / PostgreSQL / Airtable (for invoice data)
- Email Node (Gmail/SMTP) – for sending reminders

---

## 📦 Setup Instructions

### 1. Clone this Repository


git clone https://github.com/Sarves1911/auromatic-invention.git


### 2. Setup n8n

You can run n8n:

* Locally with Docker:

docker run -it --rm \
  -p 5678:5678 \
  -v ~/.n8n:/home/node/.n8n \
  n8nio/n8n


* Or via [n8n.cloud](https://n8n.io/n8n-cloud/) (hosted version)

### 3. Configure the Workflow

* Open n8n editor at `http://localhost:5678`
* Import the provided workflow file from this repo (or recreate it)
* Connect:

  * Google Sheets / Airtable / DB node for invoice data
  * OpenAI API key in the OpenAI node
  * Gmail / SMTP node with your email credentials

### 4. Add API Keys

Ensure you set up the following credentials in n8n:

* **OpenAI API Key**
* **Gmail/SMTP Credentials**
* Optional: **Google Sheets API credentials**

### 5. Test the Workflow

Trigger the workflow manually or via the cron scheduler to run daily/weekly.
