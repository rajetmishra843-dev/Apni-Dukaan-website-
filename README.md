# 🛍️ Apni Dukaan — Ecommerce Website

A full-featured, single-file ecommerce website for **Apni Dukaan** — a trending gadgets, jewellery, home & lifestyle online store based in Ajmer, Rajasthan, India.

**🔗 Live Site:** _add your GitHub Pages / Netlify link here after deploying_

---

## ✨ Features

- 🛒 **Shopping Cart** — add/remove items, quantity control, live totals
- ❤️ **Wishlist** — save products, move to cart anytime
- 🔍 **Search & Filters** — live search, category tabs, category tiles (10+ categories)
- 👁️ **Quick View** — large product detail popup with 3D tilt hover effect on photos
- 🔐 **Phone OTP Login** — Firebase Authentication, required before checkout
- 💳 **Payments** — Razorpay integration (COD + UPI/Card/Netbanking)
- 🏷️ **Promo Codes** — percentage/flat discounts, category-restricted codes supported
- 📦 **49+ Products** — real product photos, pricing, and descriptions
- 🪢 **Rakhi Festival Collection** — dedicated seasonal promo section
- 📍 **Store Location** — embedded Google Map + address
- 📱 **WhatsApp Integration** — click-to-chat, automatic order notifications, order tracking requests
- 📖 **Help Center** — Return & Refund, Shipping Info, Contact Us, Company info (About, Careers, Seller signup) — all as interactive modals
- 🎨 **Premium Black & Gold Theme** — custom logo, smooth scroll-reveal animations, shimmer image loading, polished micro-interactions
- 📱 **Fully Responsive** — mobile, tablet, and desktop

---

## 🚀 Deploy This Site

This is a **single HTML file** (`index.html`) — no build step, no server required.

### Option 1: GitHub Pages
1. Push this repo to GitHub (`index.html` must be in the root).
2. Go to **Settings → Pages**.
3. Under **Source**, select the `main` branch and `/ (root)` folder → **Save**.
4. Your site will be live at `https://<username>.github.io/<repo-name>/` within a minute or two.
5. Make sure a `.nojekyll` file exists in the root (already included) so GitHub Pages serves the file as-is.

### Option 2: Netlify
1. Go to [netlify.com](https://netlify.com) → **Add new site → Deploy manually**.
2. Drag and drop `index.html` (and `.nojekyll`) into the upload area.
3. Your site is live instantly on a `*.netlify.app` URL.
4. Or connect this GitHub repo under **Import an existing project** for automatic redeploys on every push.

> ⚠️ Razorpay and Firebase OTP **require a real `https://` domain** to work — they will not function when the file is opened locally (`file://`).

---

## ⚙️ Configuration

All configuration lives near the top of the `<script>` block in `index.html`.

| What | Where to find it | Notes |
|---|---|---|
| **Razorpay key** | `key: "rzp_live_..."` inside `placeOrder()` | Get from Razorpay Dashboard → Settings → API Keys |
| **Firebase config** | `const firebaseConfig = {...}` | Firebase Console → Project Settings → Your apps |
| **WhatsApp number** | `NOTIFY_CONFIG.OWNER_WHATSAPP` | Format: country code + number, no `+` or spaces (e.g. `916378690335`) |
| **Promo codes** | `const PROMO_CODES = {...}` | Add/edit codes — supports `percent` or `flat` discounts, `minOrder`, and `restrictCategory` |
| **Products** | `const PRODUCTS = [...]` | Each product is a JS object — see structure below |

### Product object structure
```js
{
  id: 1,
  name: "Product Name",
  category: "Home & Kitchen",   // must match an existing category, or creates a new one automatically
  price: 599,
  old: 999,                      // original price for discount display, or null
  rating: 4.3,
  reviews: 210,
  trust: 95,                     // trust score % shown on product card
  tag: "TRENDING",                // TRENDING / NEW / BESTSELLER / COMBO / "" for none
  image: "https://...",           // product photo URL, or null to use fallback icon
  deal: false,                    // true = shows in "Deal of the Day"
  desc: "Short product description"
}
```

---

## ✏️ Updating Products

**Adding, removing, or editing products doesn't require touching code manually if you don't want to:**

- Send an Excel/CSV with product details (name, price, category, description, photo) and it can be converted into the `PRODUCTS` array format above.
- Or edit `index.html` directly on GitHub: open the file → click the pencil (edit) icon → find the product inside the `PRODUCTS` array → edit the values → commit changes.

---

## 🧩 Tech Stack

- **Plain HTML, CSS, JavaScript** — no framework, no build tools, no dependencies to install
- **Firebase Authentication** (Phone/OTP) — via CDN
- **Razorpay Checkout.js** — via CDN
- **Google Fonts** — Space Grotesk, Manrope, IBM Plex Mono

---

## 📁 File Structure

```
/
├── index.html      ← the entire website (HTML + CSS + JS in one file)
└── .nojekyll        ← tells GitHub Pages to skip Jekyll processing
```

---

## 📞 Contact

- **WhatsApp:** [+91 63786 90335](https://wa.me/916378690335)
- **Instagram:** [@apnidukaan_ecommerce_india](https://www.instagram.com/apnidukaan_ecommerce_india)
- **Location:** Ajmer, Rajasthan, India — 305001

---

<p align="center">Made with ♥ in Rajasthan</p>
