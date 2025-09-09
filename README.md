# BrandGuard — M-Gas Impersonation Scanner

🚨 **Problem:**  
M-Gas Kenya faces impersonation on Facebook — fake pages and groups that scam customers, tarnish the brand, and cause financial loss.

💡 **Solution (MVP):**  
I built **BrandGuard**, a Python + Gradio web app that:
- Auto-discovers Facebook Pages/Groups via DuckDuckGo Search.
- Scores each entity using M-Gas’ brand fingerprint:
  - Must match tagline: *"M-Gas is changing lives by providing pay-as-you-go cooking gas to all Kenyans."*
  - Must not be a Group (M-Gas has no groups).
  - Must link to official domain: **mgas.ke**
- Flags impersonators vs suspicious vs low-risk.
- Generates:
  - 📑 Threat Intelligence Summary
  - 📨 Complaint Pack (ready for Meta takedown)
  - 📊 CSV/Markdown exports

⚙️ **Tech Stack**
- Python
- Gradio (UI)
- Pandas
- DuckDuckGo Search (free-tier discovery)

🔐 **Security Guardrails (added later)**
- Auth login (username/password)
- Input validation
- Rate limiting
- Purge outputs button

📌 **Next Steps**
- Connect to Meta Graph API for enriched data (followers, about).
- Extend to monitor any consumer-facing enterprise brand.
- Integrate customer alert notifications.

---

## 🚀 Demo
1. Clone repo:
   ```bash
   git clone https://github.com/YOURUSERNAME/BrandGuard-MGas.git
   cd BrandGuard-MGas
   pip install -r requirements.txt
   python main.py

   Open in browser → run scan.

⚠️ Uses only public web data + official APIs. Fully ToS compliant.
