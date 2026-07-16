# GoGrab (GrabX)

GoGrab is a modern headless e-commerce application designed to provide a seamless and high-performance online shopping experience.

The project is structured as a decoupled monorepo:
- **`GrabX/`** — A fast, modern frontend built using React.js and Vite.
- **`Api/`** — A headless content manager and REST API server powered by Strapi (Node.js).

## 🚀 Features

- **Product Catalog** — Dynamic list of categories, search, and filtering options.
- **Shopping Cart** — Client-side cart management with persistence.
- **Admin Dashboard** — Content management dashboard for products, inventories, and categories (via Strapi Admin panel).
- **Modern Build Tooling** — Hot module reloading and optimized assets via Vite.

## 🛠️ Tech Stack

### Frontend (`GrabX`)
- **Library:** React.js
- **Build Tool:** Vite
- **Styles:** CSS / Tailwind
- **State Management:** React Context API

### Backend (`Api`)
- **Framework:** Strapi (Headless Node.js CMS)
- **Database:** SQLite (default for development) / PostgreSQL
- **Format:** REST API

---

## ⚙️ Getting Started

### Prerequisites
- Node.js (version 16.x or higher)
- npm or yarn

### 1. Backend Setup (`Api`)

```bash
cd Api
npm install
npm run build
npm run develop
```
The Strapi admin panel will be available at `http://localhost:1337/admin`. Create your administrator account and populate your products.

### 2. Frontend Setup (`GrabX`)

Create a `.env` file in the `GrabX` directory:
```env
VITE_API_URL=http://localhost:1337
```

Install and run:
```bash
cd ../GrabX
npm install
npm run dev
```
The application will launch at `http://localhost:5173`.

---

## 📂 Project Structure

```
grabx/
├── GrabX/                 # React Frontend
│   ├── src/
│   │   ├── components/    # Reusable UI elements
│   │   ├── pages/         # Page views (Home, Cart, Product)
│   │   ├── context/       # Global cart state
│   │   └── App.jsx
│   ├── package.json
│   └── vite.config.js
└── Api/                   # Strapi Backend API
    ├── config/            # Server & database configurations
    ├── src/               # Strapi content-type definitions
    └── package.json
```

## 📄 License

This project is licensed under the [MIT License](LICENSE).
