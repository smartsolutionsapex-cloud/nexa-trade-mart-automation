# 🚀 NEXA TRADE MART - Complete E-Commerce Automation System

## 📋 Overview
NEXA TRADE MART is a complete, scalable, low-cost automation engine for online fashion, electronics, accessories, and combo businesses.

### Business Channels
- 🌐 Website (e-commerce)
- 📱 WhatsApp Integration
- 🎵 TikTok Shop
- 📘 Facebook Marketplace
- 📸 Instagram DM

---

## 🏗️ System Architecture

```
Frontend (Website) → Firebase (Database) → Automation Engine (n8n) → WhatsApp/Social APIs → Admin Dashboard
```

### Key Components
1. **Frontend** - Mobile-first e-commerce website
2. **Backend** - REST APIs for order processing
3. **Firebase** - Real-time database & authentication
4. **Automation Engine** - n8n workflows for automation
5. **Admin Dashboard** - Real-time analytics & control
6. **Communication** - WhatsApp, TikTok, Facebook integration

---

## 📦 Project Structure

```
nexa-trade-mart-automation/
├── frontend/                 # React e-commerce frontend
├── backend/                  # Node.js/Express API server
├── firebase/                 # Firebase configuration & rules
├── automation/               # n8n workflow configurations
├── dashboard/                # Admin dashboard (React)
├── docs/                     # Documentation
├── config/                   # Environment & configuration
└── deployment/               # Docker & deployment scripts
```

---

## 🚀 Quick Start

### Prerequisites
- Node.js 16+
- Firebase Account
- WhatsApp Business API Access
- n8n instance (self-hosted or cloud)
- Docker (optional)

### Installation Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/smartsolutionsapex-cloud/nexa-trade-mart-automation.git
   cd nexa-trade-mart-automation
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure environment variables**
   ```bash
   cp .env.example .env
   # Edit .env with your Firebase, WhatsApp, and API keys
   ```

4. **Start the system**
   ```bash
   npm start
   ```

---

## 💾 Database Schema

### Collections

#### PRODUCTS
```json
{
  "product_id": "PRD_001",
  "name": "Premium T-Shirt",
  "category": "Clothing",
  "buying_price": 150,
  "transport_cost": 20,
  "real_cost": 187,
  "selling_price": 374,
  "multiplier": 2,
  "profit_per_unit": 187,
  "stock_quantity": 50,
  "image_url": "https://...",
  "created_at": "2026-05-24T00:00:00Z"
}
```

#### ORDERS
```json
{
  "order_id": "ORD_001",
  "customer_name": "John Doe",
  "phone_number": "+27123456789",
  "product_id": "PRD_001",
  "quantity": 2,
  "total_price": 748,
  "profit": 374,
  "status": "pending",
  "timestamp": "2026-05-24T10:30:00Z"
}
```

#### CUSTOMERS
```json
{
  "customer_id": "CUST_001",
  "name": "John Doe",
  "phone": "+27123456789",
  "total_orders": 5,
  "total_spent": 3740
}
```

#### COMMISSIONS
```json
{
  "commission_id": "COM_001",
  "seller_id": "SEL_001",
  "order_id": "ORD_001",
  "commission_amount": 50,
  "status": "pending",
  "timestamp": "2026-05-24T10:30:00Z"
}
```

---

## ⚙️ Pricing Automation

### Formula

**Real Cost:**
```
real_cost = (buying_price × 1.10) + transport_share
```

**Selling Price:**
```
selling_price = real_cost × multiplier
```

**Category Multipliers:**
- Accessories: ×2.5
- Clothing: ×2
- Electronics: ×1.5–2
- Combos: ×2.2–3

**Profit:**
```
profit = selling_price - real_cost
```

---

## 📱 WhatsApp Automation

### Trigger Messages

1. **Order Confirmation**
   ```
   Hi [Name], your order at NEXA TRADE MART has been received.
   Order ID: [Order_ID]
   We will confirm stock and delivery shortly.
   ```

2. **Payment Instruction**
   ```
   Please complete payment of R[Amount] to confirm your order.
   Bank Details: [Details]
   Reference: [Order_ID]
   ```

3. **Order Status Updates**
   - ✅ Order Confirmed
   - 📦 Packed
   - 🚚 Out for Delivery
   - ✔️ Delivered

---

## 📊 Admin Dashboard Features

- 📈 Real-time sales analytics
- 💰 Total revenue & profit tracking
- 📦 Orders management
- 🚚 Delivery status tracking
- 📊 Stock inventory
- ⭐ Top-selling products
- 🤝 Commission management
- 📅 Daily/weekly reports

---

## 🔗 Integration Channels

### TikTok Shop
- Product listing sync
- Order import to Firebase
- Pixel tracking for ads

### Facebook Marketplace
- Product catalog sync
- Order capture workflow
- Customer messaging integration

### Instagram DM
- Auto-reply via WhatsApp
- Product inquiry handling
- Order initiation

---

## 🤝 Commission System

### Commission Rules
- Small products: R10–R20
- Medium products: 10% of profit
- Combos: R30–R50

### Tracking
- Seller dashboard
- Real-time commission updates
- Payout management

---

## 📚 Documentation

- [Setup Guide](./docs/SETUP.md)
- [API Documentation](./docs/API.md)
- [Firebase Configuration](./docs/FIREBASE.md)
- [n8n Workflows](./docs/WORKFLOWS.md)
- [Deployment Guide](./docs/DEPLOYMENT.md)

---

## 🚀 Deployment

### Docker
```bash
docker-compose up -d
```

### Cloud Hosting
- Frontend: Vercel / Netlify
- Backend: Heroku / Railway
- Firebase: Google Cloud
- n8n: Self-hosted or cloud

---

## 📞 Support

For issues or questions:
- 📧 Email: support@nexatrademart.com
- 💬 WhatsApp: +27123456789
- 🐛 GitHub Issues: [Create Issue](https://github.com/smartsolutionsapex-cloud/nexa-trade-mart-automation/issues)

---

## 📄 License

MIT License - See LICENSE file

---

## 👨‍💻 Created by

Smart Solutions Apex Cloud
- GitHub: [@smartsolutionsapex-cloud](https://github.com/smartsolutionsapex-cloud)
