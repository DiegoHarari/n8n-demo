# n8n Simple Workflow: Webhook → Email + WhatsApp + Database

This is a minimal **n8n workflow** that shows how to connect multiple channels in a single automation.

## 🚀 Workflow overview
When a new request comes in via a **Webhook**, n8n:
1. Sends a **confirmation email** to the user.  
2. Sends a **WhatsApp message** (via Twilio or WhatsApp Cloud API).  
3. Stores the data into a **PostgreSQL (or MySQL) database**.  

This small workflow demonstrates how **communication + persistence** can be combined in just a couple of nodes.

## 📂 Files
- `workflow.json`: the workflow export (ready to import in n8n).
- `README.md`: project documentation.

## 🛠 How to use
1. Install [n8n](https://n8n.io).  
2. Go to your **n8n instance** → **Workflows** → **Import from File**.  
3. Select `workflow.json`.  
4. Configure your credentials for:
   - Email (SMTP or provider of your choice).
   - Twilio / WhatsApp Cloud API.
   - Database connection.

## 💡 Notes
- Replace `={{$json["email"]}}` and `={{$json["phone"]}}` with the fields coming from your Webhook payload.  
- Adapt the `Insert DB` node to match your database schema.  

