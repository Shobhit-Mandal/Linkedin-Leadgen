# Linkedin-Leadgen
Linkedin lead generation and outreach automation using n8n and apify.

This repository contains a complete **n8n workflow** designed to automate B2B lead generation and cold outreach using data directly submitted through a Google Form. The system fetches job listings, enriches them with contact info, and sends out personalized cold emails.

---

## ✅ How It Works

1. **Google Form** collects input from the user:
   - LinkedIn job search URL (with filters like title, location, job type, etc.)
   - Agency/business name
   - Services offered
   - Contact details

2. **Google Sheet** stores the submitted responses.

3. **n8n Workflow** is triggered when a new row is added to the sheet:
   - Scrapes job and company data using Apify scrapers
   - Finds potential decision-makers using 3rd-party APIs
   - Prioritizes HR/Manager-level contacts
   - Generates highly tailored cold emails using llama & deepseek LLMs
   - Sends emails using **Gmail SMTP via OAuth**
   - Logs results + handles retries and errors

---

## 🛠️ Requirements

- n8n v1.82.3 or later
- Connected **Google Sheets (trigger node)** and **Google Form**
- Gmail SMTP (OAuth2-based)
- Apify account (for scraping actors)
- Email enrichment tool (Hunter.io)
- [Google Cloud Console App](https://console.cloud.google.com/) for OAuth setup

---

## 🧠 Features

- Zero frontend hosting needed — simply use Google Form
- Google Sheets Trigger to start workflow
- Scrapes job posts from LinkedIn search URL
- Prioritizes top leads (HR, Marketing, Recruiters)
- Personalizes cold emails with agency context
- Uses retry logic + error handling for resilience
- Gmail SMTP integration with OAuth2 for sending

## ⏱️ Running the Project

1. **Open n8n (locally or on server)**  
2. **Import the Workflow:**
   - Go to `Editor UI` → `Import` → upload `leadgen-workflow.json`

3. **Configure Credentials:**
   - Google Sheets OAuth
   - Gmail SMTP OAuth
   - Apify API key
   - Hunter.io API key 

4. **Test by Submitting a Google Form:**
   - Make sure it's connected to the sheet configured in n8n
   - Check executions tab for activity

---

## 📧 Contact

**Project Maintainer**  
`shobhitmandal0209@gmail.com`  


---

## 📄 License

This project is open-sourced under the [MIT License](LICENSE).
