# n8n AI Agent Outbound - Restaurant Reservation Workflow

A streamlined, production-ready n8n workflow designed to handle automated restaurant reservations. It receives booking requests via a webhook, processes customer details, logs the data into Google Sheets, and sends an automated confirmation response.

## 🚀 Features

* **Webhook Trigger:** Receives incoming reservation payloads (Customer Name, Phone Number, Date, Time, Guests).
* **Google Sheets Integration:** Automatically appends and logs verified booking details into a Google Sheet database.
* **Webhook Response:** Sends a JSON success response back to the caller/AI agent once the reservation is successfully recorded.

---

## 📋 Workflow Structure

1. **Webhook Node:** Listens for incoming `POST` requests at `/restaurant-reservation`.
2. **Google Sheets Node:** Appends structured rows (`customer_name`, `phone_number`, `date`, `time`, `guests`, `status`) to your specified spreadsheet.
3. **Respond to Webhook Node:** Returns a confirmation JSON payload back to the client.

---

## ⚙️ Setup & Installation

1. Import the `workflow.json` file into your n8n instance.
2. **Google Sheets Node:** Reconnect your own Google Sheets OAuth2 credentials and select your target Spreadsheet and Sheet name.
3. **Webhook Node:** Activate the workflow to generate your production webhook URL.

---

## 🔒 Security Notice
This repository contains a sanitized version of the workflow. All personal credentials, instance IDs, webhook tokens, and specific Google Sheet IDs have been removed to ensure safe public sharing.
