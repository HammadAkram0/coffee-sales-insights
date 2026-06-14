# ☕ Coffee Sales Insights

A production-ready business intelligence dashboard built on **Microsoft Fabric**, providing real-time sales analytics for a multi-location coffee shop chain.

---

## 🌐 Live App

**Fabric Portal:** [Open in Fabric](https://app.fabric.microsoft.com/groups/fc13921d-4f36-48e5-9d81-39fec78fc5ff/appbackends/e7778a9f-8aaa-47ff-a258-aa7d6f9e6719)

**Static Hosting URL:** https://sonic-glen-5f6f5c0351-westeurope.webapp.fabricapps.net

---

## 📊 Features

### Dashboard
- **Market Overview** — Aggregated KPIs across all four regional roasteries
- **Revenue Trajectory** — Weekly line chart showing revenue trends over time
- **Top Products** — Ranked list of best-performing products by revenue
- **Regional Impact** — Horizontal bar chart comparing store performance
- **Revenue by Category** — Breakdown across Beverage, Food, and Merchandise
- **Live Feed** — Real-time transaction ledger with store and amount

### Transactions
- Full transaction table with ID, Date, Time, Product, Category, Qty, Unit Price, Store, Payment Method, and Amount
- Filter by date range (From / To)
- Filter by store location
- Summary line showing total entries and revenue
- CSV download

### Locations
- Individual store cards for all locations
- Shows Transactions count and Revenue per store

### Promotions
- Promotional campaign cards with descriptions and estimated uplift

---

## 🏪 Store Locations

| Store | Revenue |
|-------|---------|
| West End Roastery | $429 |
| The Glasshouse | $320 |
| Harbor View | $238 |
| Old Town Depot | $180 |
| The Roastery Loft | $214 |
| Birch & Brew | $238 |

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Platform | Microsoft Fabric (Rayfin) |
| Frontend | Vanilla HTML, CSS, JavaScript |
| Charts | Custom Canvas API (hand-written) |
| Data | CSV (sales.csv) |
| Auth | Rayfin Auth with Fabric SSO |
| Hosting | Rayfin Static Hosting |
| Database | Microsoft Fabric SQL |

---

## 📁 Project Structure

```
Coffee-Sales-Insights/
├── dist/
│   ├── index.html          # Main app shell with all pages
│   ├── assets/
│   │   ├── app.js          # All JavaScript logic, chart rendering, data parsing
│   │   └── styles.css      # All styling and layout
│   └── data/
│       └── sales.csv       # Sales transaction data
├── rayfin/
│   ├── .deployments.json   # Fabric deployment config
│   ├── rayfin.yml          # Rayfin project configuration
│   └── tsconfig.json       # TypeScript config for Rayfin functions
├── package.json
└── README.md
```

---

## 🚀 Deployment

This project is deployed using the **Rayfin CLI** for Microsoft Fabric.

### Prerequisites
- Node.js installed
- Rayfin CLI: `npm install -g @microsoft/rayfin-cli`
- Microsoft Fabric workspace access

### Deploy to Fabric

```bash
# Navigate to project
cd Coffee-Sales-Insights

# Deploy to Fabric
npx @microsoft/rayfin-cli up
```

### Push to GitHub

```bash
git add .
git commit -m "your update message"
git push
```

---

## 📦 Fabric Configuration

| Setting | Value |
|---------|-------|
| Project Name | coffee-sales-insights |
| Fabric Workspace | Fabric App |
| Workspace ID | fc13921d-4f36-48e5-9d81-39fec78fc5ff |
| Rayfin Item ID | e7778a9f-8aaa-47ff-a258-aa7d6f9e6719 |
| Region | West Europe |
| Auth | Fabric SSO enabled |
| Database | MSSQL (Fabric SQL) |

---

## 📈 KPIs Tracked

- **Gross Revenue** — Total revenue across all stores (+12.4% vs previous period)
- **Total Transactions** — Number of sales transactions (+8.1% vs previous period)
- **Average Order Value** — Revenue per transaction (-2.3% vs previous period)

---

## 🗂️ Data Schema

The app reads from `dist/data/sales.csv` with the following columns:

| Column | Type | Description |
|--------|------|-------------|
| ID | Integer | Unique transaction ID |
| Date | Date (YYYY-MM-DD) | Transaction date |
| Product | String | Product name |
| Category | String | Beverage / Food / Merchandise |
| Quantity | Integer | Units sold |
| Unit Price | Float | Price per unit |
| Store Location | String | Store name |
| Payment Method | String | Cash / Card / Mobile |

---

## 👤 Author

**Hammad Akram**
GitHub: [@HammadAkram0](https://github.com/HammadAkram0)

---

## 📄 License

This project is private and proprietary. All rights reserved.
