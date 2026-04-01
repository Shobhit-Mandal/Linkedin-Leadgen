# LinkedIn Lead Generation & Outreach System

An end-to-end automation system that converts job signals into qualified leads and personalized outreach using n8n, APIs, and LLMs.

---

## 🚀 Problem

Agencies and service businesses spend hours manually:

- finding companies that are actively hiring (high-intent signal)
- identifying relevant decision-makers
- writing personalized cold emails

This process is repetitive, time-consuming, and inconsistent.

---

## ⚙️ Solution

Designed an automated workflow that:

1. Captures user intent via a simple Google Form
2. Identifies high-intent companies from LinkedIn job listings
3. Enriches company and contact data using APIs
4. Prioritizes relevant decision-makers (HR, founders, managers)
5. Generates personalized cold emails using LLMs
6. Sends outreach automatically and tracks execution

---

## 🧠 System Flow

Input → Processing → Output

- **Input:** LinkedIn job search URL + business context (services, positioning)
- **Processing:**
  - scrape job & company data (Apify)
  - enrich contacts (Hunter / APIs)
  - filter & prioritize leads
  - generate personalized messaging (LLMs)
- **Output:** Automated email outreach pipeline with logging and retry handling

---

## 🔧 Tech Stack

- n8n (workflow orchestration)
- Apify (data scraping)
- Hunter.io (email enrichment)
- Gmail SMTP (OAuth2)
- LLMs (Llama / DeepSeek)
- Google Sheets (trigger + logging)

---

## 📌 Key Features

- End-to-end automation from lead discovery → outreach
- High-intent targeting using hiring signals
- Personalized messaging at scale using LLMs
- Retry and error-handling built into workflow
- No frontend required (form + sheet based system)

---

## ⚠️ Note

Some third-party integrations may require fresh API keys or configuration updates, but the core workflow design and logic remain intact.

---

## 👤 Author

Shobhit Mandal  
Contact: shobhitmandal0209@gmail.com
