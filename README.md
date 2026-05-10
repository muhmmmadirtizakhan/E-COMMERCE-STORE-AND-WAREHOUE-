# ✨ AETHERIC — Luxury E-Commerce Platform 🛍️

<p align="center">
  <img src="https://go.miva.com/hubfs/052022_BLOG_High-Bounce-Blog-Refresh_What%E2%80%99s%20the%20Difference%20Between%20an%20Ecommerce%20Platform%20and%20Shopping%20Cart@2x.png" />
</p>

<p align="center">
✨ Luxury Curation • 🔐 Encrypted Payments • 📧 Instant Confirmation
</p>

----
## 📋 Overview

**AETHERIC** is a production-grade full-stack luxury e-commerce platform built for high-end retail. It delivers a seamless shopping experience — from product discovery and cart management to secure checkout and branded order confirmation emails — all wrapped in an editorial luxury aesthetic.

## ✨ features
----------
## 🛍️ Customers
----
- 🔍 Browse and filter a curated product catalog
- 🛒 Manage a persistent cart across sessions
- 💳 Checkout securely via Stripe-powered payments
- 📧 Receive branded HTML order confirmation emails instantly
- ❤️ Save favourite products and revisit them anytime
- 📊 Access a personal dashboard to track orders and purchase history
- 💸 Monitor spending and analyse expenses over time
------
## 🏪 Store owner
-----
🏪 Store owners can:
- 📌 List, update, and manage product inventory
- 📦 Track and fulfill orders in real time
- 💰 Monitor revenue and analytics via a protected admin dashboard
- 👤 Look up customer order history and manage order statuses

-----
## 🛠️ Tech Stack

<p align="center">
  <img src="https://img.shields.io/badge/HTML%20·%20CSS%20·%20JS-Frontend-c4a47c?style=for-the-badge&logo=javascript&logoColor=0f0f1e&labelColor=0f0f1e" />
  <img src="https://img.shields.io/badge/Node.js%20·%20Express-Backend-c4a47c?style=for-the-badge&logo=nodedotjs&logoColor=339933&labelColor=0f0f1e" />
  <img src="https://img.shields.io/badge/Supabase-Database-3ECF8E?style=for-the-badge&logo=supabase&logoColor=3ECF8E&labelColor=0f0f1e" />
  <img src="https://img.shields.io/badge/Firebase-Auth%20%26%20Storage-FFCA28?style=for-the-badge&logo=firebase&logoColor=FFCA28&labelColor=0f0f1e" />
  <img src="https://img.shields.io/badge/Stripe-Payments-635BFF?style=for-the-badge&logo=stripe&logoColor=635BFF&labelColor=0f0f1e" />
  <img src="https://img.shields.io/badge/Resend-Email-c4a47c?style=for-the-badge&logo=maildotru&logoColor=c4a47c&labelColor=0f0f1e" />
  <img src="https://img.shields.io/badge/Formspree-Forms-E34F26?style=for-the-badge&logo=html5&logoColor=E34F26&labelColor=0f0f1e" />
</p>

-----
## 🏗️ Architecture

---

> 🧠 **3-Tier Design** — Client · Server · Services — every layer has one job.

🖥️ **Client** (HTML/CSS/JS) never touches any database or payment provider directly — every sensitive operation routes through the Express server first.

🛡️ **Express** acts as the central gatekeeper — every incoming request hits a Firebase Auth middleware that verifies the JWT token before any route logic executes.

🔀 **Once authenticated**, the server fans out to the right service — Supabase for database reads/writes, Stripe for payment intents and refunds, and Resend for branded order confirmation emails.

🔔 **Stripe webhooks** call back into the server to confirm payment server-side — order status is never trusted from the client alone.

⚡ **Formspree** is the only bypass — contact forms POST directly from the browser since no sensitive data is involved and no server overhead is needed.

------

<p align="center">
  <img src="./docs/architecture.svg" alt="AETHERIC System Architecture" width="100%"/>
</p>

------
