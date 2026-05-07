# ☀️ SunCart – Summer Essentials Store

A modern summer eCommerce platform where users can explore and purchase seasonal products like sunglasses, summer outfits, skincare, beach accessories, and more.

## 🌐 Live URL

## 📌 Project Purpose

SunCart is a full-featured summer shopping platform built with Next.js App Router. Users can browse summer products, view detailed product pages (protected by authentication), register/login with email or Google, and manage their profile.

## ✨ Key Features

- 🏠 **Home Page** – Animated hero slider with summer sale banners, popular products section, summer care tips, and top brands showcase
- 🛍️ **Products Page** – Browse all 8+ summer essentials with category filters
- 🔒 **Protected Product Details** – Full product details page accessible only to logged-in users; redirects to login otherwise
- 🔐 **Authentication (BetterAuth)** – Email/password registration & login, Google OAuth social login
- 👤 **My Profile** – View logged-in user's name, email, photo, and member since date
- ✏️ **Update Profile** – Update name and profile photo URL via BetterAuth's `updateUser`
- 📱 **Fully Responsive** – Mobile, tablet, and desktop layouts
- 🎨 **Animate.css** – Smooth entrance animations on hero and auth pages
- 🔔 **Toast Notifications** – Success/error feedback via react-hot-toast

## 🛠️ Tech Stack

- **Framework**: Next.js 16 (App Router)
- **Styling**: Tailwind CSS v4
- **Authentication**: BetterAuth
- **Database**: better-sqlite3 (local SQLite)
- **Animations**: animate.css
- **Notifications**: react-hot-toast

## 📦 NPM Packages Used

| Package | Purpose |
|---|---|
| `next` | React framework with App Router |
| `react` / `react-dom` | UI library |
| `tailwindcss` | Utility-first CSS framework |
| `better-auth` | Authentication (email + Google OAuth) |
| `better-sqlite3` | SQLite database adapter for BetterAuth |
| `animate.css` | CSS animation library |
| `react-hot-toast` | Toast notification system |

## 🚀 Getting Started

```bash
# Install dependencies
npm install

# Set up environment variables
cp .env.local.example .env.local
# Fill in BETTER_AUTH_SECRET, GOOGLE_CLIENT_ID, GOOGLE_CLIENT_SECRET

# Run development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## 🔑 Environment Variables

```env
BETTER_AUTH_SECRET=your-secret-key
BETTER_AUTH_URL=http://localhost:3000
NEXT_PUBLIC_APP_URL=http://localhost:3000
GOOGLE_CLIENT_ID=your-google-client-id
GOOGLE_CLIENT_SECRET=your-google-client-secret
```

## 📁 Project Structure

```
app/
├── components/
│   ├── Navbar.jsx          # Sticky navbar with auth state
│   ├── Footer.jsx          # Footer with links & social
│   ├── HeroSlider.jsx      # Auto-rotating hero banner
│   └── ProductCard.jsx     # Reusable product card
├── products/
│   ├── page.js             # All products listing
│   └── [id]/page.js        # Protected product detail
├── login/page.js           # Login with email + Google
├── register/page.js        # Register with email + Google
├── my-profile/
│   ├── page.js             # Profile view (protected)
│   └── update/page.js      # Update name & photo
├── api/auth/[...all]/      # BetterAuth API handler
├── layout.js               # Root layout
└── page.js                 # Home page
data/
└── products.json           # 8 summer products
lib/
├── auth.js                 # BetterAuth server config
└── auth-client.js          # BetterAuth client config
```
