# SSL Expiry Alert System

## 🧑‍💻 Who is this for?
This workflow is ideal for administrators or IT professionals responsible for monitoring SSL certificates of multiple websites to ensure they do not expire unexpectedly.

## ❗ Problem
SSL certificates play a crucial role in ensuring secure communication over the internet. However, if not monitored closely, they can expire, leading to potential security risks and service disruption. This workflow helps in proactively monitoring SSL certificate expiry dates.

## ⚙️ Functionality
- Pulls URLs to monitor from a Google Sheet.
- Checks SSL certificates using [SSL-Checker.io](https://www.ssl-checker.io/).
- Updates Google Sheet with SSL details such as expiry date and certificate status.
- Sends email alerts for SSL certificates nearing expiry (<30 days) or invalid certificates.

## 🛠️ Setup
1. Clone the provided Google Sheet and update the Google Sheet URL in the "URLs to Monitor" node.
2. Set up Google Sheets and Gmail credentials in **n8n**.
3. Configure the **Discourse Trigger** for weekly monitoring.
4. Customize email/Telegram/Ntfy alert settings as needed.

## 🔧 Customization
- Modify the frequency of monitoring by adjusting the trigger interval in the **Weekly Trigger** node.
- Customize email content and recipients in the **Send Alert Email** node.
- Extend functionality by adding additional checks or actions based on SSL certificate status.

## 🔐 Note
Ensure proper authentication and authorization for accessing **Google Sheets**, **SSL-Checker.io**, and **Gmail accounts** within the workflow.