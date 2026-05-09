# TrendStore - Next.js E-Commerce Demo

A modern, responsive frontend for an apparel storefront built entirely inside the `client/` folder. This demo uses temporary example product data and focuses on shopping, cart, and checkout UI.

---

## 🌟 Features

- Responsive product browsing
- Category filtering and search UI
- Product detail pages with size/color variants
- Shopping cart with quantity management
- Persistent cart stored in the browser
- Checkout flow with shipping and payment forms
- Form validation using Zod and React Hook Form

---

## 🧩 Sections

- **Home**: Featured hero and product list
- **Products**: Catalog browsing
- **Product Detail**: Item details and variant selection
- **Cart**: Checkout process with shipping/payment forms

---

## 🛠 Tech Stack

- Next.js 16
- React 19
- TypeScript
- Tailwind CSS 4
- Zustand
- React Hook Form
- Zod
- Lucide React
- React Toastify

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

## 📌 Notes

- Repository contains only the `client/` frontend app.
- Product data is temporary/example data used for demonstration.
- Backend integration and production persistence are not included.


⚠️ Project Status: Under Construction / Work in Progress**

# TrendStore - Full Stack E-Commerce Application

A modern, full-stack e-commerce platform built with **Next.js 16** for the frontend and **Express.js** for the backend. TrendStore provides a seamless shopping experience with product browsing, filtering, cart management, and checkout functionality.

---

## 🎯 Overview

TrendStore is a frontend e-commerce demo built entirely inside the `client/` folder. The repository contains only the client application, and backend integration / production data persistence are not included here. The current implementation uses temporary example product data for demo purposes and showcases product browsing, cart management, and checkout flow.

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

### **Product Management**
- Multiple product variants (sizes, colors)
- Product images for each color variant
- Detailed product descriptions
- Price information
- Stock availability

### **Cart Management**
- Add products with selected size and color
- Track quantity per item
- Remove items from cart
- Clear entire cart
- Real-time cart updates
- Cart total calculation

---

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

### **Prerequisites**
- Node.js 18+ and npm/yarn
- Git

### **Installation**

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd next_e-commerce
   ```

2. **Install Frontend Dependencies**
   ```bash
   cd client
   npm install
   ```

3. **Install Backend Dependencies**
   ```bash
   cd ../server
   npm install
   ```

---

## ▶️ Running the Application

### **Development Mode**

**Terminal 1 - Frontend (Port 3000)**
```bash
cd client
npm run dev
```
Access at: `http://localhost:3000`

**Terminal 2 - Backend (Port varies)**
```bash
cd server
node src/index.ts
```

### **Production Build**

**Frontend Build**
```bash
cd client
npm run build
npm start
```

**Lint Code**
```bash
cd client
npm run lint
```

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

## 📦 Dependencies Overview

### **Frontend Key Dependencies**
| Package | Version | Purpose |
|---------|---------|---------|
| Next.js | 16.2.4 | React framework with SSR |
| React | 19.2.4 | UI library |
| Zustand | 5.0.12 | State management |
| React Hook Form | 7.75.0 | Form management |
| Zod | 4.4.2 | Schema validation |
| Tailwind CSS | 4 | Styling |
| Lucide React | 1.14.0 | Icons |

### **Backend Key Dependencies**
| Package | Version | Purpose |
|---------|---------|---------|
| Express.js | 5.2.1 | Web server framework |

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the ISC License - see the LICENSE file for details.

---

## 👨‍💻 Author

Full Stack E-Commerce Application

---

## 📞 Support & Contact

For issues, questions, or suggestions, please open an issue in the repository.

---

## 🗺️ Roadmap

### Phase 1: MVP ✅
- Product listing and details
- Shopping cart
- Checkout flow

### Phase 2: Backend Integration
- User authentication
- Database setup
- API endpoints

### Phase 3: Enhanced Features
- Payment gateway integration
- Order management
- Admin dashboard

### Phase 4: Optimization
- Performance optimization
- Analytics
- SEO improvements

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
