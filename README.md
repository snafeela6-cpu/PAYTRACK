# PayTrack - Business Credit & Payment Management System
> **Tagline:** *Simplifying Business Credit Management*  
> **Target Audience:** Indian small business owners, retail shops, textile stores, wholesalers, and distributors.

---

## 📌 Executive Overview

**PayTrack** is a production-quality commercial fintech SaaS platform designed to eliminate manual credit notebooks (*Bahi Khata* / *Udhar Khata*) and spreadsheets. It provides Indian MSMEs with an automated, reliable system for managing customer credit limits, outstanding balances, partial collections, payment commitments (Promise-to-Pay), Tamil & English WhatsApp payment reminders, and deterministic AI business intelligence.

---

## 🚀 Key Modules & Capabilities

### 1. Indian Localisation & Compliance
- **Strict Indian Rupees (₹):** Standard Indian grouping format (e.g. `₹1,00,000`, `₹12,450.50`).
- **Date & Time Standards:** Strict `DD-MM-YYYY` format with `Asia/Kolkata` (IST) clock.
- **Mobile Formatting:** `+91` 10-digit Indian mobile validation.
- **Payment Modes:** UPI (Google Pay, PhonePe, Paytm), Cash Counter, Bank Transfer (NEFT/IMPS/RTGS), Cheque, and Card.
- **GST Compliance:** Optional 15-digit GSTIN validation with 0%, 5%, 12%, 18%, and 28% tax slabs.

### 2. Core Modules (Navigation Structure)
1. **Dashboard:** Real-time KPIs (Total Outstanding, Total Collected, Overdue Dues, Active Accounts, 7-Day Forecast), 6-month turnover charts, recent activity, and upcoming due bills.
2. **Customers:** Directory with credit limits, purchases, payments, live balances, risk scores, search, filtering (Has Balance, Overdue, Settled, High Risk), and comprehensive customer ledger drawers.
3. **Credit Ledger:** Unified digital *Bahi Khata* displaying all debits (credit sales) and credits (payments) with automatic running balance.
4. **Transactions:** Invoices and payment receipts manager with quick filters, partial payment allocation, and GST computation.
5. **Payment Reminders:** Tamil (தமிழ்) and English reminder generation across Friendly, Professional, and Urgent tones with direct WhatsApp click-to-chat links (`wa.me/91...`).
6. **Promise-to-Pay (PTP) Tracker:** Commitment logging, tracking fulfilled commitments, marking missed/broken commitments, and historical logs.
7. **Business Insights (AI Engine):**
   - **Payment Behaviour Analysis:** Customer credit scoring (0–100) and risk profiling.
   - **Collection Forecasting:** 7, 15, and 30-day horizons with High, Moderate, and At-Risk recovery tiers.
   - **Cash Flow Insights:** Working capital tied in credit, Days Sales Outstanding (DSO), and healthy accounts ratio.
   - **Anomaly & Fraud Detection:** Duplicate invoice detection, unusual credit spikes, and broken commitment alerts.
   - **Deterministic Financial Assistant:** Natural language query processor answering business queries directly from live ledger records.
8. **Reports:** Daily, weekly, and monthly collection statements, aging buckets (0–15d, 16–30d, 30+d), CSV downloads, and printable PDF statements.
9. **Settings:** Business profile, banking details (Bank name, A/C, IFSC, UPI ID), default credit terms, Supabase PostgreSQL schema, and JSON backup/restore.

---

## 🛠️ Technology Stack

- **Frontend:** React 18, Vite, TypeScript, Tailwind CSS, Lucide React, Recharts
- **Database & Auth:** Supabase PostgreSQL, Row Level Security (RLS) policies, UUID v4 primary keys
- **Storage Mode:** Dual-mode architecture (Supabase PostgreSQL Cloud or Offline Standalone with realistic Indian demo data)

---

## 💻 Quick Start & Running Locally

### 1. Install Dependencies
```bash
npm install
```

### 2. Run Development Server
```bash
npm run dev
```

### 3. Build for Production
```bash
npm run build
```

---

## 🔐 Firebase Authentication Setup

PayTrack includes Firebase Authentication for commercial user and business credential management:
- **Sign In:** Email and Password authentication with validation and error code handling.
- **Sign Up:** Separate business registration with business name, proprietor name, industry category, +91 mobile number, and email.
- **Forgot Password:** Password recovery dispatch using Firebase `sendPasswordResetEmail`.
- **Firebase Configuration:** Set the following keys in your `.env` file or paste your Firebase config directly into the in-app **Firebase Config Modal**:
  ```env
  VITE_FIREBASE_API_KEY=your-api-key
  VITE_FIREBASE_AUTH_DOMAIN=your-project.firebaseapp.com
  VITE_FIREBASE_PROJECT_ID=your-project-id
  VITE_FIREBASE_STORAGE_BUCKET=your-project.appspot.com
  VITE_FIREBASE_MESSAGING_SENDER_ID=your-sender-id
  VITE_FIREBASE_APP_ID=your-app-id
  ```
- **Fallback Evaluation Mode:** If Firebase credentials are not yet configured, PayTrack operates in a standalone evaluation mode with working authentication and **One-Click Demo Access** so you can test all features immediately.

---

## 🗄️ Supabase PostgreSQL Setup (Optional Cloud Mode)

To connect PayTrack to your own Supabase project:
1. Create a project at [supabase.com](https://supabase.com).
2. Open the **SQL Editor** in your Supabase dashboard and run the script located at:
   ```
   supabase/schema.sql
   ```
3. Create a `.env` file in the project root:
   ```env
   VITE_SUPABASE_URL=https://your-project-id.supabase.co
   VITE_SUPABASE_ANON_KEY=your-anon-key
   ```
4. Restart the app. PayTrack will automatically switch to **Supabase Cloud Mode**. If no keys are provided, it smoothly operates in **Standalone Evaluation Mode** with preloaded Indian business data (*Sri Murugan Wholesalers & Distributors*).

---

## 🎓 Presentation Ready
Built to commercial fintech SaaS standards for high-stakes evaluations and Innovation & Design Thinking showcases.
