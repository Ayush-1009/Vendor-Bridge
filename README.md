# VendorBridge ERP 🌉

![VendorBridge Banner](https://img.shields.io/badge/Status-Live_Prototype-success) ![JavaScript](https://img.shields.io/badge/Frontend-Vanilla_JS-yellow) ![Python](https://img.shields.io/badge/Backend-Django_Python-blue) 

**VendorBridge** is a modern, AI-powered Procurement and Vendor Management System (VMS) built to streamline the B2B purchasing lifecycle. It bridges the gap between Procurement Officers, Workflow Managers, and Vendors through a secure, intelligent, and highly automated platform.

## ✨ Key Features (Hackathon Highlights)

* 🧠 **AI-Powered Quote Analyzer:** An intelligent algorithm that automatically scores and ranks competing vendor quotes based on a weighted matrix of Price (30%), Delivery Time (25%), Vendor Rating (20%), On-Time Delivery Rate (15%), and Warranty (10%)[cite: 2].
* 💡 **AI Pricing Insights:** A built-in market analysis tool that explains *why* a quote costs what it does (e.g., highlighting "Enterprise Silicon Premiums" or "Supply Chain Constraints" for hardware)[cite: 2].
* 🔒 **Immutable Audit Trail:** A legally compliant logging system that records every action (quote submissions, approvals, user creations)[cite: 2]. Logs are displayed in a filterable UI[cite: 1] and securely transmitted to a locked-down Django database[cite: 2].
* 👥 **Dynamic Role-Based Access (RBAC):** Secure, customized dashboards for 4 distinct user types: System Admin, Procurement Officer (PO), Workflow Manager, and Registered Vendor[cite: 2].
* 💾 **Hybrid Data Persistence:** Utilizes browser `localStorage` for seamless user registration and approval workflows during demos[cite: 2], while bridging to a Python/Django backend via REST APIs for secure data (Quotes and Audit Logs)[cite: 2].
* 📊 **Advanced Analytics & Reports:** Features a dedicated reports dashboard tracking total spend, monthly procurement trends, and individual vendor win-rate performance[cite: 2].
* 📄 **Automated Document Export:** One-click generation and downloading of Purchase Orders and Invoices[cite: 2].

## 🛠️ Tech Stack

**Frontend:**
* **HTML5:** Semantic structure with modular screens and modals[cite: 1].
* **CSS3:** Custom styling with CSS variables, responsive grids, and print-media optimization for PDF exports[cite: 3].
* **Vanilla JavaScript (ES6+):** State management, AI algorithm logic, DOM manipulation, and asynchronous API communication (`fetch`)[cite: 2].
* **FontAwesome:** Scalable vector icons for the UI[cite: 1].

**Backend (Integration Ready):**
* **Python / Django:** Designed to connect to a Django REST API for immutable audit logging and secure quote management (`http://127.0.0.1:8000/api/`)[cite: 2].

## 🚀 Quick Start Guide

### Running the Frontend (Client-Side Only)
You do not need a server to view the main UI and test the AI features!
1. Clone the repository.
2. Locate the `index.html` file[cite: 1].
3. Double-click to open it in any modern web browser.
4. *Note: Data such as new user registrations will persist locally in your browser[cite: 2].*

### Running the Full-Stack Application (With Django)
To enable the Immutable Audit Log and permanent database storage:
1. Navigate to your Django backend directory.
2. Run migrations: `python manage.py migrate`
3. Start the server: `python manage.py runserver`
4. Open the `index.html` frontend. It will automatically connect to `http://127.0.0.1:8000/`[cite: 2].

## 💡 The "Golden Path" Demo Workflow

To experience the full power of VendorBridge, follow this exact workflow:

1. **Vendor Registration:** Click *Sign up* on the login screen, fill out the form as a Vendor, and submit[cite: 1, 2].
2. **Admin Approval:** Log in as **Admin** (`admin@vendorbridge.com` / `Admin@123`)[cite: 2]. Navigate to *User Management*, open the *Pending Approvals* tab, and approve the new vendor[cite: 1, 2].
3. **Submit a Quote:** Log in with your new Vendor account. Go to *Open RFQs*, click **Submit Quote**, and enter your bid[cite: 2]. 
4. **AI Quote Analysis:** Log in as a **Procurement Officer** (`po@vendorbridge.com` / `PO@1234`)[cite: 2]. Go to *Compare Quotes*. Watch the AI automatically score the bids and recommend the best overall value. Click the **"Why does this cost X?"** button to view AI market insights[cite: 2].
5. **Manager Approval:** Click *Accept AI Recommendation*[cite: 2]. Log in as a **Manager** (`manager@vendorbridge.com` / `Manager@123`)[cite: 2], go to *Approvals*, and officially approve the PO[cite: 2].
6. **Audit & Analytics:** Log back in as **Admin**. Check the *Activity & Logs* tab to see the secure, immutable history of the entire process[cite: 1, 2]. Then, view the *Reports & Analytics* page to see how the vendor's win-rate updated in real-time[cite: 2].

---
*Built for the 2026 Hackathon*
