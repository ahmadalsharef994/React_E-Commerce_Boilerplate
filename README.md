# React E-Commerce Boilerplate

<p align="center">
  <img src="https://img.shields.io/badge/React-18+-blue?logo=react" alt="React">
  <img src="https://img.shields.io/badge/Redux_Toolkit-2.x-purple?logo=redux" alt="Redux">
  <img src="https://img.shields.io/badge/Tailwind_CSS-3.x-teal?logo=tailwindcss" alt="Tailwind">
  <img src="https://img.shields.io/badge/Stripe-payments-blue?logo=stripe" alt="Stripe">
  <img src="https://img.shields.io/badge/license-MIT-blue" alt="License">
</p>

A feature-rich **React e-commerce boilerplate** with product catalog, shopping cart, checkout flow with Stripe, and user authentication. Ready to plug in your own backend.

---

## 🛍️ Features

- 🏪 Product catalog with search & category filters
- 🛒 Cart with quantity management (Redux Toolkit)
- 💳 Checkout with Stripe Elements
- 🔐 JWT authentication (login/register)
- 📦 Order history
- 📱 Fully responsive (Tailwind CSS)

---

## 🏗️ State & Flow

```mermaid
flowchart LR
    Catalog["🏪 Catalog"] -->|Add to Cart| Cart["🛒 Redux Cart\nStore"]
    Cart -->|Checkout| Stripe["💳 Stripe\nElements"]
    Stripe -->|Payment Intent| API["🚀 Backend API"]
    API -->|Order Confirmed| Orders["📦 Order History"]
```

---

## 🚀 Quick Start

```bash
npm install
cp .env.example .env      # add VITE_STRIPE_PUBLIC_KEY
npm run dev
```

---

## 📁 Structure

```
src/
├── components/
│   ├── ProductCard/
│   ├── Cart/
│   └── Checkout/
├── features/
│   ├── cart/cartSlice.ts
│   ├── auth/authSlice.ts
│   └── orders/ordersSlice.ts
├── pages/
│   ├── Home.tsx
│   ├── Product.tsx
│   ├── Checkout.tsx
│   └── Orders.tsx
└── services/
    └── api.ts
```

---

## ⚙️ Environment Variables

```env
VITE_API_URL=http://localhost:5000
VITE_STRIPE_PUBLIC_KEY=pk_test_...
```

---

## 📄 License

MIT
