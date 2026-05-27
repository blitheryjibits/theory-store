# 🛍️ Theory 418 Solutions — Storefront

A modern, high‑performance e‑commerce storefront built with **Next.js**, powered by a **Medusa** backend.  
This frontend communicates with the Medusa server via REST APIs and provides a fast, responsive shopping experience.

---

## 🚀 Features

- ⚡ **Next.js 15** with Turbopack for ultra‑fast dev experience
- 🛒 **Medusa Commerce** integration (products, carts, checkout, regions)
- 🎨 Fully customizable UI
- 🌍 Region & currency handling via middleware
- 🔐 Secure API communication with backend
- 📦 Dynamic product pages
- 🧩 Modular architecture for easy extension
- 📱 Responsive design for mobile & desktop

---

## 📁 Project Structure

```
storefront/
  ├── app/                 # Next.js App Router pages
  ├── components/          # UI components
  ├── lib/                 # API helpers, utils
  ├── middleware.ts        # Region detection + Medusa API middleware
  ├── public/              # Static assets
  ├── styles/              # Global styles
  ├── .env.local           # Environment variables
  └── package.json
```

---

## 🔧 Requirements

Before running the storefront, ensure you have:

- Node.js 18+
- A running **Medusa backend** (local or remote)
- A valid `NEXT_PUBLIC_MEDUSA_BACKEND_URL` in your `.env.local`

---

## ⚙️ Environment Variables

Create a `.env.local` file in the storefront root:

```env
NEXT_PUBLIC_MEDUSA_BACKEND_URL=http://localhost:9000
```

If your backend is deployed (Render, Fly.io, etc.):

```env
NEXT_PUBLIC_MEDUSA_BACKEND_URL=https://your-medusa-backend.com
```

---

## 🏃 Running the Storefront

### Development

```bash
npm install
npm run dev
```

The app will start at:

```
http://localhost:8000
```

---

## 🧪 Testing the Connection

Make sure your Medusa backend is running:

```bash
cd ../backend
npm run dev
```

Then visit:

```
http://localhost:8000
```

If the backend is offline, the storefront middleware will fail to fetch regions.

---

## 🧱 Building for Production

```bash
npm run build
npm start
```

---

## 🚀 Deployment

You can deploy the storefront to:

- **Vercel** (recommended)
- Netlify
- AWS Amplify
- Any Node.js hosting provider

Just ensure your environment variable is set:

```
NEXT_PUBLIC_MEDUSA_BACKEND_URL=https://your-production-backend.com
```

---

## 🧩 Customization

You can customize:

- Product listing pages
- Product detail pages
- Cart & checkout flow
- UI components
- Middleware logic
- API helpers

The storefront is intentionally modular to support rapid iteration.

---

## 🤝 Contributing

Pull requests are welcome.  
For major changes, please open an issue first to discuss what you’d like to modify.

---

## 📄 License

MIT License.  
You are free to use, modify, and distribute this storefront.

---
