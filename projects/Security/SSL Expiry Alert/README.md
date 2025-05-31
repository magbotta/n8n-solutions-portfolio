# 🔐 SSL Certificate Monitor Workflow

This **n8n** workflow automates the process of monitoring SSL certificate expiration dates to help prevent service disruptions due to expired certificates. It utilizes [SSL-Checker.io](https://ssl-checker.io/) to validate certificate status and sends alerts via Gmail when certificates approach expiration.

---

## 📌 Use Case

Managing SSL certificates manually can be **time-consuming** and **error-prone**, potentially leading to **downtime** or **security vulnerabilities** from expired certificates.

This workflow provides **automated visibility** into the SSL status of your web assets.

---

## ⚙️ What This Workflow Does

- **Reads URLs** from a Google Sheet.
- **Checks SSL certificate status** for each domain using **SSL-Checker.io**.
- **Sends notification emails** via Gmail if a certificate is close to expiry (e.g., within 7 days).
- Runs **weekly** for continuous coverage.

---

## 🚀 Setup Instructions

1. **Add Credentials:**
   - Google Sheets
   - Gmail
   - SSL-Checker.io API

2. **Prepare Your Data Source:**
   - Create a Google Sheet with a list of website URLs to monitor.

3. **Configure the Workflow:**
   - Set the schedule to run **weekly** using a Cron node.
   - Set notification threshold (e.g., certificates expiring in less than 7 days).

4. **Activate Workflow:**
   - Enable the workflow in n8n to begin automated monitoring and alerting.

---

## 🛠 How to Customize

| Area | Customization Option |
|------|----------------------|
| 🔄 URL Source | Replace Google Sheets with **Airtable**, **MySQL**, or **CSV** import |
| ⏰ Notification Threshold | Adjust alert window (e.g., notify for **14 days** instead of 7) |
| 🔔 Notification Channel | Add Slack, Microsoft Teams, or SMS integrations |
| 📝 Renewal Automation | Send email/API request to SSL provider for renewal |

---

## 📧 Example Notification

> **Subject:** SSL Certificate Expiring Soon for `example.com`  
> **Body:** The SSL certificate for `example.com` is set to expire in **6 days**.  
> Please renew the certificate to avoid service interruptions.

---

## 🧩 Requirements

- A running instance of **n8n**
- API key for **SSL-Checker.io**
- Access to a Gmail account with SMTP enabled
- Google Sheet with domains to monitor

---

## 📄 License

MIT License. Feel free to fork and adapt this workflow for your organization’s needs.
