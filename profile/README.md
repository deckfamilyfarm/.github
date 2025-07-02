# 🐄 Deck Family Farm — Technical Overview & Sustainability Plan

Welcome to the **Deck Family Farm** GitHub organization. This repository exists to document and preserve all code, integrations, and infrastructure essential to the ongoing digital operations of the farm.

---

## 📦 Purpose

This GitHub organization contains:
- Automations for managing **product inventory**, **pricing**, and **CSA orders**
- Code for **Square POS integrations** for Farmers Markets
- **Full Farm CSA** software integrations (via Local Line)
- Product marketing tools and auto-generated **PDF price lists**
- Backend and frontend code for:
  - **herdlist** animal tracking
  - **killdeer** API for product/inventory sync
  - **reports** and analytics

---

## ☁️ Hosting & Deployment

All servers and databases are hosted on **[DigitalOcean](https://www.digitalocean.com/)** under the account:
> 📧 `jdeck88@gmail.com`

### Infrastructure:
- **Droplets** host backend Node.js applications and NGINX reverse proxies.
- **Mysql** databases are also hosted on DigitalOcean.
- PM2 is used to manage long-running services.
- NGINX is configured to serve all API endpoints under `api.deckfamilyfarm.com`.

---

## 🧭 Key Repositories

| Repo | Purpose |
|------|---------|
| [`killdeer`](https://github.com/deckfamilyfarm/killdeer) | API server and reports for products, pricing, inventory |
| [`herdlist`](https://github.com/deckfamilyfarm/herdlist) | Animal management and data import/export |
| [`entities`](https://github.com/deckfamilyfarm/entities) | Visualize entity relationships/Diagram |
| `.github` | Org-wide documentation (you are here) |

---

## 🌐 External Systems

### 🔹 [Wix Website](https://www.deckfamilyfarm.com)
Public homepage for general visitors and customers. Managed outside GitHub.

### 🔹 [Local Line CSA Portal](https://www.localline.ca/deckfamilyfarm)
Used to host the Full Farm CSA online store.

---

## 🧭 Orientation for New Developers

If you're stepping in to manage or support this system:
- Start by reading through each repo’s individual `README.md`.
- Connect to the DigitalOcean dashboard (contact `jdeck88@gmail.com` for credentials or shared access).
- Review NGINX config in `/etc/nginx/sites-available/` on the production droplet.
- `killdeer` is the canonical API for inventory, prices, and products.
- All scheduled scripts and services are managed via PM2 on the droplet (`pm2 list`).
- APIs are deployed under `https://api.deckfamilyfarm.com`.
- Reports are deployed under `https://reports.deckfamilyfarm.com`.

---

## 📘 Documentation Goals

This page serves as a sustainability and transition guide.
- If something breaks, check here first.
- If John Deck is unavailable, this page and linked repos will help you regain control and understanding of the system.

> This is a living document — feel free to update it with new systems, credentials, or integrations as they are added.

---

🛠 Built and maintained by Deck Family Farm  
📫 Contact: `jdeck88@gmail.com`

