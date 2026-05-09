⚠️ Project Status: Under Construction / Work in Progress**

# TrendStore - Full Stack E-Commerce Application

A modern, responsive frontend for an apparel storefront built entirely inside the `client/` folder. This demo uses temporary example product data and focuses on shopping, cart, and checkout UI.

---

## ✨ Features

### **Frontend Features**
- 🏠 **Homepage** - Featured products and category showcase
- 🛍️ **Product Browsing** - View all products with detailed information
- 🔍 **Search & Filter** - Find products by name, category
- 📋 **Product Details** - View product images, descriptions, available sizes/colors
- 🛒 **Shopping Cart** - Add/remove items with quantity management
- 💾 **Persistent Cart** - LocalStorage-based cart persistence
- 📦 **Checkout Process**
  - Multi-step checkout (Cart → Shipping → Payment)
  - Shipping address form with validation
  - Payment form with card details
- 🎨 **Responsive Design** - Mobile-friendly interface
- 📱 **Modern UI** - Clean, intuitive user experience

---

## 🧩 Sections

- **Home**: Featured hero and product list
- **Products**: Catalog browsing
- **Product Detail**: Item details and variant selection
- **Cart**: Checkout process with shipping/payment forms

---

## 🛠 Tech Stack

### **Frontend (Client)**
- **Framework**: Next.js 16.2.4 (React 19.2.4)
- **Language**: TypeScript 5
- **Styling**: Tailwind CSS 4 + PostCSS
- **State Management**: Zustand 5.0.12
- **Form Management**: React Hook Form 7.75.0 + Zod 4.4.2 (validation)
- **UI Icons**: Lucide React 1.14.0
- **Notifications**: React Toastify 11.1.0
- **Linting**: ESLint 9

---

## 📁 Project Structure

```
next_e-commerce/
│
├── client/                          # Next.js Frontend Application
│   ├── src/
│   │   ├── app/                     # Next.js App Router Pages
│   │   │   ├── page.tsx             # Homepage with featured products
│   │   │   ├── cart/
│   │   │   │   └── page.tsx         # Shopping Cart & Checkout
│   │   │   ├── products/
│   │   │   │   ├── page.tsx         # Products Listing
│   │   │   │   └── [id]/
│   │   │   │       └── page.tsx     # Product Detail Page
│   │   │   ├── layout.tsx           # Root Layout Component
│   │   │   └── globals.css          # Global Styles
│   │   │
│   │   ├── components/              # Reusable React Components
│   │   │   ├── Navbar.tsx           # Navigation Bar
│   │   │   ├── SearchBar.tsx        # Product Search
│   │   │   ├── Categories.tsx       # Category Filter
│   │   │   ├── Filter.tsx           # Product Filters
│   │   │   ├── ProductList.tsx      # Product Grid Display
│   │   │   ├── ProductCard.tsx      # Individual Product Card
│   │   │   ├── ProductInteraction.tsx # Size/Color Selection
│   │   │   ├── ShoppingCartIcon.tsx # Cart Icon with Badge
│   │   │   ├── ShippingForm.tsx     # Shipping Address Form
│   │   │   ├── PaymentForm.tsx      # Payment Method Form
│   │   │   └── Footer.tsx           # Footer Component
│   │   │
│   │   ├── stores/                  # Zustand State Management
│   │   │   └── cartStore.ts         # Shopping Cart Store
│   │   │
│   │   ├── types.ts                 # TypeScript Type Definitions
│   │   └── public/                  # Static Assets
│   │       └── products/            # Product Images
│   │
│   ├── next.config.ts              # Next.js Configuration
│   ├── tsconfig.json               # TypeScript Configuration
│   ├── tailwind.config.ts          # Tailwind CSS Configuration
│   ├── postcss.config.mjs          # PostCSS Configuration
│   └── package.json                # Dependencies
```

## 📊 Data Models

### **Product Type**
```typescript
{
  id: string | number
  name: string
  shortDescription: string
  description: string
  price: number
  sizes: string[]
  colors: string[]
  images: Record<string, string>  // Key: color, Value: image URL
}
```

### **Cart Item Type**
```typescript
{
  ...ProductType
  quantity: number
  selectedSize: string
  selectedColor: string
}
```

### **Shipping Form Schema**
- Full Name (required)
- Email (required, valid email)
- Phone Number (7-10 digits)
- Address (required)
- City (required)

### **Payment Form Schema**
- Card Holder Name (required)
- Card Number (16 digits)
- Expiration Date (MM/YY format)
- CVV (3 digits)

---

## 🚀 Getting Started

```bash
git clone <repository-url>
cd next-e-commerce/client
npm install
npm run dev
```

Open `http://localhost:3000`.

---

## 📝 API Endpoints

*Backend API endpoints to be implemented.*

> Note: The current client uses temporary example product data and mock in-memory behavior. Backend data storage and API integration will be completed in future development.

---

## 🎯 Current Features Status

### ✅ Completed
- Frontend UI with all components
- Product browsing and filtering
- Shopping cart functionality with persistence
- Multi-step checkout flow
- Form validation (Shipping & Payment)
- Responsive design
- Type-safe development with TypeScript

### 🔄 In Development
- Backend API routes
- Database integration
- Payment processing
- Order management
- Admin dashboard

### 📋 Planned Features
- User authentication & profile management
- Order history
- Product reviews and ratings
- Wishlist functionality
- Email notifications
- Inventory management
- Analytics dashboard

---

## 🔒 Security Considerations

- Form validation using Zod for input sanitization
- Payment form data handling (currently for demo purposes)
- TypeScript for type safety and preventing runtime errors
- Environment variables for sensitive data (to be implemented)

**⚠️ Note**: Payment processing currently for demo purposes. Integrate with payment gateway (Stripe, PayPal) for production.

---

## 🎓 Learning Resources

- [Next.js Documentation](https://nextjs.org/docs)
- [React Documentation](https://react.dev)
- [Tailwind CSS](https://tailwindcss.com/docs)
- [Zustand](https://github.com/pmndrs/zustand)
- [Express.js](https://expressjs.com)

---

**Last Updated**: May 2026
**Current Version**: 0.1.0
