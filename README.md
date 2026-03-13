# Koperbaarkopen – volledige multi-page HTML-bestanden

Gebruik onderstaande bestanden als losse projectstructuur.

## Bestandsstructuur

```text
koperbaarkopen/
├─ index.html
├─ producten.html
├─ certificaten.html
├─ contact.html
├─ winkelwagen.html
├─ betalen.html
├─ product-250g.html
├─ product-500g.html
├─ product-1kg.html
├─ style.css
└─ script.js
```

---

## `style.css`

```css
:root {
  --bg: #0a0d12;
  --panel: #10151d;
  --panel-2: #11161f;
  --panel-3: #171a22;
  --text: #ffffff;
  --muted: #94a3b8;
  --copper: #d29a5a;
  --copper-dark: #a86430;
  --line: rgba(255, 255, 255, 0.1);
  --shadow: 0 28px 90px rgba(0, 0, 0, 0.35);
}

* {
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  min-height: 100vh;
  font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
  color: var(--text);
  background:
    radial-gradient(circle at top, rgba(186, 116, 51, 0.18), transparent 30%),
    radial-gradient(circle at right, rgba(255, 255, 255, 0.05), transparent 18%),
    var(--bg);
}

button,
input,
select,
textarea {
  font: inherit;
}

a {
  color: inherit;
  text-decoration: none;
}

.container {
  width: min(1120px, calc(100% - 32px));
  margin: 0 auto;
}

.header {
  position: sticky;
  top: 0;
  z-index: 50;
  border-bottom: 1px solid var(--line);
  background: rgba(10, 13, 18, 0.82);
  backdrop-filter: blur(14px);
}

.header-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 24px;
  padding: 20px 0;
}

.brand {
  display: inline-block;
  color: inherit;
}

.brand-title {
  font-size: 30px;
  font-weight: 600;
  letter-spacing: 0.12em;
}

.brand-subtitle,
.eyebrow {
  margin-top: 6px;
  font-size: 12px;
  font-weight: 600;
  letter-spacing: 0.28em;
  text-transform: uppercase;
  color: var(--copper);
}

.nav {
  display: flex;
  align-items: center;
  gap: 28px;
  flex-wrap: wrap;
}

.nav-btn,
.primary-btn,
.secondary-btn,
.danger-btn,
.qty-btn {
  border: 0;
  cursor: pointer;
  transition: 0.2s ease;
}

.nav-btn {
  background: none;
  color: #cbd5e1;
  padding: 0;
  font-size: 14px;
}

.nav-btn:hover {
  color: var(--copper);
}

.page {
  padding: 64px 0 80px;
}

.hero {
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  gap: 56px;
  align-items: center;
  padding: 44px 0 96px;
}

.hero-pill {
  display: inline-flex;
  width: fit-content;
  padding: 8px 16px;
  border: 1px solid rgba(210, 154, 90, 0.3);
  border-radius: 999px;
  background: rgba(210, 154, 90, 0.1);
  font-size: 12px;
  font-weight: 600;
  letter-spacing: 0.28em;
  text-transform: uppercase;
  color: #e1b07a;
}

.hero h1,
.page-title,
.section-title {
  margin: 18px 0 0;
  line-height: 1.05;
  letter-spacing: -0.03em;
}

.hero h1 {
  font-size: clamp(44px, 6vw, 72px);
}

.page-title {
  font-size: clamp(34px, 4.5vw, 52px);
}

.section-title {
  font-size: clamp(30px, 4vw, 42px);
}

.gradient-text {
  background: linear-gradient(90deg, #f4d2a7, #d29a5a, #9f5f2a);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}

.lead,
.body-text {
  color: var(--muted);
  line-height: 1.8;
}

.lead {
  margin-top: 24px;
  font-size: 19px;
}

.button-row,
.product-actions,
.inline-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
  margin-top: 32px;
}

.primary-btn,
.secondary-btn,
.danger-btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 14px 24px;
  border-radius: 18px;
  font-size: 14px;
  font-weight: 700;
}

.primary-btn {
  color: white;
  background: linear-gradient(90deg, var(--copper), var(--copper-dark));
  box-shadow: 0 10px 30px rgba(210, 154, 90, 0.35);
}

.primary-btn:hover,
.secondary-btn:hover {
  transform: translateY(-1px);
}

.secondary-btn {
  color: white;
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.12);
}

.danger-btn {
  color: #d1d5db;
  background: rgba(0, 0, 0, 0.2);
  border: 1px solid rgba(255, 255, 255, 0.1);
}

.danger-btn:hover {
  border-color: rgba(248, 113, 113, 0.45);
  color: #fca5a5;
}

.hero-card-wrap {
  position: relative;
}

.hero-glow {
  position: absolute;
  inset: -24px;
  border-radius: 36px;
  background: linear-gradient(135deg, rgba(210, 154, 90, 0.3), transparent);
  filter: blur(24px);
}

.hero-card {
  position: relative;
  border-radius: 32px;
  border: 1px solid var(--line);
  background: rgba(255, 255, 255, 0.05);
  padding: 24px;
  box-shadow: 0 20px 80px rgba(0, 0, 0, 0.45);
  backdrop-filter: blur(10px);
}

.hero-card-frame {
  border-radius: 28px;
  padding: 1px;
  background: linear-gradient(135deg, #2b160b, #a86430, #f0c99c);
}

.hero-card-inner {
  border-radius: 27px;
  background: #120f0d;
  padding: 32px;
}

.metal-block,
.product-visual {
  border-radius: 24px;
  background: linear-gradient(135deg, #6f3d1d 0%, #d9a76f 35%, #fff1da 50%, #b96d34 70%, #6d3d1d 100%);
  box-shadow: inset 0 12px 28px rgba(255, 255, 255, 0.08), inset 0 -18px 30px rgba(0, 0, 0, 0.28);
}

.metal-block {
  height: 224px;
  margin-top: 20px;
}

.panel {
  border-radius: 34px;
  border: 1px solid var(--line);
  background: var(--panel);
  padding: 40px;
  box-shadow: var(--shadow);
}

.panel-dark {
  background: var(--panel-2);
}

.panel-highlight {
  background: linear-gradient(135deg, var(--panel-3), #0d0f14);
  border-color: rgba(210, 154, 90, 0.2);
}

.section-gap {
  margin-top: 32px;
}

.grid-3,
.grid-2,
.grid-hero-meta,
.cart-layout,
.payment-layout,
.split {
  display: grid;
  gap: 24px;
}

.grid-3 {
  grid-template-columns: repeat(3, minmax(0, 1fr));
}

.grid-2 {
  grid-template-columns: repeat(2, minmax(0, 1fr));
}

.grid-hero-meta {
  grid-template-columns: repeat(3, minmax(0, 1fr));
  margin-top: 40px;
}

.cart-layout,
.payment-layout {
  grid-template-columns: 1.1fr 0.9fr;
}

.split {
  grid-template-columns: 1fr 1fr;
}

.meta-card,
.feature-card {
  border-radius: 22px;
  border: 1px solid var(--line);
  background: rgba(255, 255, 255, 0.05);
  padding: 18px;
}

.meta-label {
  font-size: 12px;
  text-transform: uppercase;
  letter-spacing: 0.24em;
  color: var(--muted);
}

.meta-value {
  margin-top: 10px;
  font-size: 20px;
  font-weight: 700;
}

.product-card {
  border-radius: 30px;
  border: 1px solid var(--line);
  background: linear-gradient(180deg, rgba(255, 255, 255, 0.08), rgba(255, 255, 255, 0.03));
  padding: 32px;
  box-shadow: 0 12px 50px rgba(0, 0, 0, 0.28);
}

.product-card:hover {
  transform: translateY(-2px);
  border-color: rgba(210, 154, 90, 0.4);
  box-shadow: 0 18px 70px rgba(0, 0, 0, 0.4);
}

.badge {
  display: inline-flex;
  padding: 6px 12px;
  border-radius: 999px;
  border: 1px solid rgba(210, 154, 90, 0.25);
  background: rgba(210, 154, 90, 0.1);
  color: #e1b07a;
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.2em;
  text-transform: uppercase;
}

.price {
  margin-top: 16px;
  font-size: 42px;
  font-weight: 700;
  background: linear-gradient(90deg, #f4d2a7, #b56c35);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}

.divider {
  height: 1px;
  width: 100%;
  background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.12), transparent);
  margin: 0 auto;
}

label {
  display: grid;
  gap: 8px;
}

.field-label {
  font-size: 14px;
  font-weight: 700;
  color: white;
}

.optional {
  color: #64748b;
}

input,
select,
textarea {
  width: 100%;
  border-radius: 18px;
  border: 1px solid rgba(255, 255, 255, 0.1);
  background: rgba(0, 0, 0, 0.2);
  color: white;
  padding: 14px 16px;
  outline: none;
}

input::placeholder,
textarea::placeholder {
  color: #64748b;
}

input:focus,
select:focus,
textarea:focus {
  border-color: var(--copper);
}

textarea {
  min-height: 180px;
  resize: vertical;
}

.contact-strip {
  border-radius: 34px;
  padding: 32px;
  color: white;
  background: linear-gradient(90deg, var(--copper), var(--copper-dark));
  box-shadow: 0 18px 60px rgba(210, 154, 90, 0.28);
}

.contact-strip-grid {
  display: grid;
  gap: 24px;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  margin-top: 24px;
}

.contact-strip-label {
  color: rgba(255, 255, 255, 0.82);
  font-size: 14px;
  font-weight: 700;
}

.contact-strip-value {
  margin-top: 8px;
  font-size: 20px;
  font-weight: 700;
}

.cart-item {
  border-radius: 22px;
  border: 1px solid var(--line);
  background: rgba(255, 255, 255, 0.05);
  padding: 20px;
}

.cart-item-row {
  display: flex;
  justify-content: space-between;
  gap: 20px;
  align-items: center;
  flex-wrap: wrap;
}

.qty-wrap {
  display: flex;
  align-items: center;
  border-radius: 18px;
  border: 1px solid var(--line);
  background: rgba(0, 0, 0, 0.2);
}

.qty-btn {
  padding: 10px 16px;
  color: white;
  background: transparent;
  font-size: 20px;
  font-weight: 700;
}

.qty-btn:hover {
  color: var(--copper);
}

.qty-value {
  min-width: 52px;
  text-align: center;
  font-size: 14px;
  font-weight: 700;
}

.empty-state {
  border-radius: 22px;
  border: 1px dashed var(--line);
  background: rgba(255, 255, 255, 0.03);
  padding: 24px;
  color: var(--muted);
}

.summary-row {
  display: flex;
  justify-content: space-between;
  gap: 20px;
  padding-bottom: 12px;
  border-bottom: 1px solid var(--line);
  color: #cbd5e1;
}

.summary-row + .summary-row {
  margin-top: 16px;
}

.summary-total {
  display: flex;
  justify-content: space-between;
  margin-top: 16px;
  font-size: 20px;
  font-weight: 700;
}

.disabled {
  opacity: 0.4;
  cursor: not-allowed;
  pointer-events: none;
}

.footer {
  border-top: 1px solid rgba(255, 255, 255, 0.05);
  background: #090b10;
  color: #64748b;
}

.footer-inner {
  display: flex;
  justify-content: space-between;
  gap: 12px;
  padding: 32px 0;
  font-size: 14px;
  flex-wrap: wrap;
}

@media (max-width: 1024px) {
  .hero,
  .split,
  .cart-layout,
  .payment-layout,
  .grid-3,
  .grid-2,
  .grid-hero-meta,
  .contact-strip-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 768px) {
  .header-inner {
    align-items: flex-start;
    flex-direction: column;
  }

  .nav {
    gap: 16px;
  }

  .brand-title {
    font-size: 24px;
  }

  .panel,
  .contact-strip,
  .hero-card-inner,
  .product-card {
    padding: 24px;
  }

  .price {
    font-size: 34px;
  }
}
```

---

## `script.js`

```js
const products = [
  {
    slug: "koperbaar-250g",
    file: "product-250g.html",
    weight: "250 g",
    price: "€21,25",
    shortDescription:
      "Compacte koperbaar voor instapkopers die een luxe presentatie willen combineren met een toegankelijk formaat.",
    description:
      "De 250 gram koperbaar is ideaal voor klanten die op een toegankelijke manier willen starten met een representatieve koperbaar. Het formaat is compact, stijlvol en wordt geleverd met certificaat van echtheid.",
    badge: "Instapformaat",
  },
  {
    slug: "koperbaar-500g",
    file: "product-500g.html",
    weight: "500 g",
    price: "€42,50",
    shortDescription:
      "Een gebalanceerd formaat met dezelfde verfijnde afwerking, certificering en representatieve uitstraling.",
    description:
      "De 500 gram koperbaar biedt een mooie balans tussen formaat en prijs. Geschikt voor klanten die net iets meer volume zoeken, zonder in te leveren op uitstraling, afwerking en certificering.",
    badge: "Populair",
  },
  {
    slug: "koperbaar-1kg",
    file: "product-1kg.html",
    weight: "1 kg",
    price: "€85,00",
    shortDescription:
      "Massieve koperbaar met premium afwerking, certificaat van echtheid en een krachtige, exclusieve presentatie.",
    description:
      "De 1 kg koperbaar is het meest gekozen formaat binnen de collectie. Een krachtige, massieve koperbaar met luxe uitstraling, duidelijke certificering en een professionele presentatie voor verzamelaars en representatief bezit.",
    badge: "Meest gekozen",
  },
];

const features = [
  "Individueel certificaat van echtheid",
  "Verfijnd afgewerkt en visueel gecontroleerd",
  "Beschermend verpakt voor veilige levering",
  "Beschikbaar voor zakelijke en particuliere afname",
];

const euroFormatter = new Intl.NumberFormat("nl-NL", {
  style: "currency",
  currency: "EUR",
});

function parsePrice(price) {
  const normalized = price.replace(/€/g, "").replace(/\./g, "").replace(/,/g, ".").trim();
  const parsed = Number(normalized);
  return Number.isFinite(parsed) ? parsed : 0;
}

function formatLineTotal(price, qty) {
  return euroFormatter.format(parsePrice(price) * qty);
}

function getCartItems() {
  return JSON.parse(localStorage.getItem("kbk-cart") || "[]");
}

function setCartItems(items) {
  localStorage.setItem("kbk-cart", JSON.stringify(items));
}

function getCartCount() {
  return getCartItems().reduce((sum, item) => sum + item.qty, 0);
}

function getCartSubtotal() {
  return getCartItems().reduce((total, item) => total + parsePrice(item.price) * item.qty, 0);
}

function updateCartCount() {
  const cartBtn = document.querySelector("[data-cart-count]");
  if (!cartBtn) return;
  const count = getCartCount();
  cartBtn.textContent = count > 0 ? `Winkelwagen (${count})` : "Winkelwagen";
}

function addToCart(slug) {
  const product = products.find((item) => item.slug === slug);
  if (!product) return;

  const items = getCartItems();
  const existing = items.find((item) => item.slug === slug);

  if (existing) {
    existing.qty += 1;
  } else {
    items.push({
      slug: product.slug,
      name: `Koperbaar ${product.weight}`,
      price: product.price,
      qty: 1,
    });
  }

  setCartItems(items);
  updateCartCount();
}

function updateCartItemQty(slug, nextQty) {
  const items = getCartItems();

  if (nextQty <= 0) {
    setCartItems(items.filter((item) => item.slug !== slug));
    return;
  }

  setCartItems(
    items.map((item) => (item.slug === slug ? { ...item, qty: nextQty } : item))
  );
}

function removeFromCart(slug) {
  setCartItems(getCartItems().filter((item) => item.slug !== slug));
}

function bindAddToCartButtons() {
  document.querySelectorAll("[data-add-to-cart]").forEach((button) => {
    button.addEventListener("click", () => {
      const slug = button.getAttribute("data-add-to-cart");
      addToCart(slug);
    });
  });
}

function renderProductCard(product) {
  return `
    <div class="product-card">
      <div class="badge">${product.badge}</div>
      <h3 style="font-size:32px; margin:18px 0 0;">Koperbaar ${product.weight}</h3>
      <div class="price">${product.price}</div>
      <p class="body-text" style="margin-top:16px;">${product.shortDescription}</p>
      <div class="product-actions">
        <a class="primary-btn" href="${product.file}">Bekijk product</a>
        <button class="secondary-btn" data-add-to-cart="${product.slug}">Voeg toe aan winkelmand</button>
      </div>
    </div>
  `;
}

function renderProductGrids() {
  const homeGrid = document.getElementById("home-product-grid");
  const productsGrid = document.getElementById("products-grid");

  if (homeGrid) {
    homeGrid.innerHTML = products.map(renderProductCard).join("");
  }

  if (productsGrid) {
    productsGrid.innerHTML = products.map(renderProductCard).join("");
  }
}

function renderCertificatesFeatures() {
  const certificatesFeatures = document.getElementById("certificates-features");
  if (!certificatesFeatures) return;
  certificatesFeatures.innerHTML = features
    .map((feature) => `<div class="feature-card">${feature}</div>`)
    .join("");
}

function renderProductPage() {
  const detailRoot = document.querySelector("[data-product-slug]");
  if (!detailRoot) return;

  const slug = detailRoot.getAttribute("data-product-slug");
  const product = products.find((item) => item.slug === slug);
  if (!product) return;

  const title = document.getElementById("detail-title");
  const badge = document.getElementById("detail-badge");
  const price = document.getElementById("detail-price");
  const description = document.getElementById("detail-description");
  const featuresContainer = document.getElementById("detail-features");
  const addBtn = document.getElementById("detail-add-btn");

  if (title) title.textContent = `Koperbaar ${product.weight}`;
  if (badge) badge.textContent = product.badge;
  if (price) price.textContent = product.price;
  if (description) description.textContent = product.description;
  if (featuresContainer) {
    featuresContainer.innerHTML = features
      .map((feature) => `<div class="feature-card">${feature}</div>`)
      .join("");
  }
  if (addBtn) {
    addBtn.addEventListener("click", () => {
      addToCart(product.slug);
      window.location.href = "winkelwagen.html";
    });
  }
}

function renderCartPage() {
  const list = document.getElementById("cart-items");
  const subtotalEl = document.getElementById("cart-subtotal");
  const totalEl = document.getElementById("cart-total");
  const payBtn = document.getElementById("go-payment-btn");
  if (!list || !subtotalEl || !totalEl) return;

  const items = getCartItems();
  const subtotal = euroFormatter.format(getCartSubtotal());
  subtotalEl.textContent = subtotal;
  totalEl.textContent = subtotal;
  list.innerHTML = "";

  if (items.length === 0) {
    list.innerHTML = `<div class="empty-state">Je winkelmand is nog leeg. Voeg eerst een product toe.</div>`;
    if (payBtn) payBtn.classList.add("disabled");
    return;
  }

  if (payBtn) payBtn.classList.remove("disabled");

  items.forEach((item) => {
    const row = document.createElement("div");
    row.className = "cart-item";
    row.innerHTML = `
      <div class="cart-item-row">
        <div>
          <div style="font-size: 20px; font-weight: 700;">${item.name}</div>
          <div class="body-text" style="margin-top: 6px;">Prijs per stuk: ${item.price}</div>
        </div>
        <div style="display:flex; align-items:center; gap:12px; flex-wrap:wrap;">
          <div class="qty-wrap">
            <button class="qty-btn js-minus">-</button>
            <div class="qty-value">${item.qty}</div>
            <button class="qty-btn js-plus">+</button>
          </div>
          <button class="danger-btn js-remove">Verwijderen</button>
          <div style="font-size: 24px; font-weight: 700; color: #f4d2a7;">${formatLineTotal(item.price, item.qty)}</div>
        </div>
      </div>
    `;

    row.querySelector(".js-minus").addEventListener("click", () => {
      updateCartItemQty(item.slug, item.qty - 1);
      location.reload();
    });
    row.querySelector(".js-plus").addEventListener("click", () => {
      updateCartItemQty(item.slug, item.qty + 1);
      location.reload();
    });
    row.querySelector(".js-remove").addEventListener("click", () => {
      removeFromCart(item.slug);
      location.reload();
    });
    list.appendChild(row);
  });

  if (payBtn) {
    payBtn.addEventListener("click", () => {
      if (getCartItems().length === 0) return;
      window.location.href = "betalen.html";
    });
  }
}

function renderPaymentPage() {
  const paymentSummary = document.getElementById("payment-summary");
  const completeBtn = document.getElementById("complete-order-btn");
  if (!paymentSummary) return;

  const items = getCartItems();
  const subtotal = euroFormatter.format(getCartSubtotal());
  paymentSummary.innerHTML = "";

  if (items.length === 0) {
    paymentSummary.innerHTML = `<div class="empty-state">Er zitten nog geen producten in je winkelmand.</div>`;
    if (completeBtn) completeBtn.classList.add("disabled");
    return;
  }

  if (completeBtn) completeBtn.classList.remove("disabled");

  items.forEach((item) => {
    const row = document.createElement("div");
    row.className = "summary-row";
    row.innerHTML = `<span>${item.name} x${item.qty}</span><span>${formatLineTotal(item.price, item.qty)}</span>`;
    paymentSummary.appendChild(row);
  });

  const shipping = document.createElement("div");
  shipping.className = "summary-row";
  shipping.innerHTML = `<span>Verzending</span><span>€0,00</span>`;
  paymentSummary.appendChild(shipping);

  const total = document.createElement("div");
  total.className = "summary-total";
  total.innerHTML = `<span>Totaal</span><span>${subtotal}</span>`;
  paymentSummary.appendChild(total);
}

document.addEventListener("DOMContentLoaded", () => {
  updateCartCount();
  renderProductGrids();
  renderCertificatesFeatures();
  renderProductPage();
  renderCartPage();
  renderPaymentPage();
  bindAddToCartButtons();
});
```

---

## `index.html`

```html
<!doctype html>
<html lang="nl">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Home - koperbaarkopen</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <header class="header">
      <div class="container header-inner">
        <a class="brand" href="index.html">
          <div class="brand-title">koperbaarkopen</div>
          <div class="brand-subtitle">Premium koperbaren met certificaat</div>
        </a>
        <nav class="nav">
          <a class="nav-btn" href="index.html">Home</a>
          <a class="nav-btn" href="producten.html">Producten</a>
          <a class="nav-btn" href="certificaten.html">Certificaten</a>
          <a class="nav-btn" href="contact.html">Contact</a>
          <a class="nav-btn" href="winkelwagen.html" data-cart-count>Winkelwagen</a>
        </nav>
      </div>
    </header>

    <main class="page">
      <div class="container hero">
        <div>
          <div class="hero-pill">Exclusieve presentatie van koperbaren</div>
          <h1>Koperbaren in <span class="gradient-text">250 g, 500 g en 1 kg</span>.</h1>
          <p class="lead">Bestel direct luxe koperbaren met certificaat van echtheid. Geschikt voor verzamelaars, presentatie en representatieve opslag.</p>
          <div class="button-row">
            <a class="primary-btn" href="producten.html">Bekijk collectie</a>
            <a class="secondary-btn" href="winkelwagen.html">Bekijk winkelmand</a>
          </div>
          <div class="grid-hero-meta">
            <div class="meta-card"><div class="meta-label">Zuiverheid</div><div class="meta-value">999+ Cu</div></div>
            <div class="meta-card"><div class="meta-label">Beschikbaar</div><div class="meta-value">250 g / 500 g / 1 kg</div></div>
            <div class="meta-card"><div class="meta-label">Inclusief</div><div class="meta-value">Certificaat</div></div>
          </div>
        </div>
        <div class="hero-card-wrap">
          <div class="hero-glow"></div>
          <div class="hero-card">
            <div class="hero-card-frame">
              <div class="hero-card-inner">
                <div class="eyebrow">Signature Copper Bar</div>
                <div class="metal-block"></div>
                <div class="section-gap cart-item-row">
                  <div>
                    <div class="body-text">Direct bestelbaar</div>
                    <div class="section-title" style="font-size: 32px; margin-top: 8px;">Premium koperbaar</div>
                  </div>
                  <div class="meta-card" style="min-width: 120px; text-align: right;">
                    <div class="meta-label">Vanaf</div>
                    <div class="meta-value" style="color: #f4d2a7;">€21,25</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="container"><div class="divider"></div></div>

      <section class="section-gap">
        <div class="container">
          <div class="panel">
            <div class="eyebrow">Collectie</div>
            <h2 class="section-title">Onze koperbaren</h2>
            <div class="grid-3 section-gap" id="home-product-grid"></div>
          </div>
        </div>
      </section>

      <section class="section-gap">
        <div class="container">
          <div class="panel panel-highlight" style="display:flex; justify-content:space-between; align-items:center; gap:32px; flex-wrap:wrap;">
            <div style="max-width: 720px;">
              <div class="eyebrow">Grotere levering</div>
              <h2 class="section-title">Grotere levering? Neem contact op.</h2>
              <p class="lead" style="margin-top:16px;">Heb je interesse in grotere volumes, zakelijke levering of specifieke wensen rondom verzending en planning? Neem dan direct contact met ons op.</p>
            </div>
            <a class="primary-btn" href="contact.html">Neem contact op</a>
          </div>
        </div>
      </section>

      <section class="section-gap">
        <div class="container">
          <div class="contact-strip">
            <div class="eyebrow" style="color: rgba(255,255,255,0.82);">Contactgegevens</div>
            <div class="contact-strip-grid">
              <div><div class="contact-strip-label">E-mailadres</div><div class="contact-strip-value">info@koperbaarkopen.nl</div></div>
              <div><div class="contact-strip-label">Adres</div><div class="contact-strip-value">Straatnaam 1, 1234 AB Amsterdam</div></div>
              <div><div class="contact-strip-label">Telefoonnummer</div><div class="contact-strip-value">+31 6 12 34 56 78</div></div>
            </div>
          </div>
        </div>
      </section>
    </main>

    <footer class="footer"><div class="container footer-inner"><div>© 2026 koperbaarkopen</div><div>Premium verkoop van koperbaren met certificaat</div></div></footer>
    <script src="script.js"></script>
  </body>
</html>
```

---

## `producten.html`

```html
<!doctype html>
<html lang="nl">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Producten - koperbaarkopen</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <header class="header"><div class="container header-inner"><a class="brand" href="index.html"><div class="brand-title">koperbaarkopen</div><div class="brand-subtitle">Premium koperbaren met certificaat</div></a><nav class="nav"><a class="nav-btn" href="index.html">Home</a><a class="nav-btn" href="producten.html">Producten</a><a class="nav-btn" href="certificaten.html">Certificaten</a><a class="nav-btn" href="contact.html">Contact</a><a class="nav-btn" href="winkelwagen.html" data-cart-count>Winkelwagen</a></nav></div></header>
    <main class="page">
      <div class="container">
        <div class="panel">
          <div class="eyebrow">Producten</div>
          <h1 class="page-title">Alle koperbaren</h1>
          <p class="lead">Kies hieronder een product om naar een aparte productpagina te gaan.</p>
          <div class="grid-3 section-gap" id="products-grid"></div>
        </div>
      </div>
    </main>
    <footer class="footer"><div class="container footer-inner"><div>© 2026 koperbaarkopen</div><div>Premium verkoop van koperbaren met certificaat</div></div></footer>
    <script src="script.js"></script>
  </body>
</html>
```

---

## `certificaten.html`

```html
<!doctype html>
<html lang="nl">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Certificaten - koperbaarkopen</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <header class="header"><div class="container header-inner"><a class="brand" href="index.html"><div class="brand-title">koperbaarkopen</div><div class="brand-subtitle">Premium koperbaren met certificaat</div></a><nav class="nav"><a class="nav-btn" href="index.html">Home</a><a class="nav-btn" href="producten.html">Producten</a><a class="nav-btn" href="certificaten.html">Certificaten</a><a class="nav-btn" href="contact.html">Contact</a><a class="nav-btn" href="winkelwagen.html" data-cart-count>Winkelwagen</a></nav></div></header>
    <main class="page">
      <div class="container" style="max-width: 960px;">
        <div class="panel">
          <div class="eyebrow">Certificaten</div>
          <h1 class="page-title">Officieel gecertificeerde koperbaren</h1>
          <p class="lead">Al onze koperbaren worden geleverd als officieel gecertificeerde producten. Iedere koperbaar wordt gecontroleerd, geregistreerd en gekoppeld aan een echtheidscertificaat met productspecificaties, gewicht en uniek certificaatnummer.</p>
          <p class="lead" style="margin-top: 18px;">Daarmee ontvang je niet alleen een representatief product, maar ook een duidelijke bevestiging van authenticiteit, herkomst en productcontrole. Dit geeft extra vertrouwen bij opslag, presentatie, doorverkoop en zakelijke afname.</p>
          <div class="grid-2 section-gap" id="certificates-features"></div>
        </div>
      </div>
    </main>
    <footer class="footer"><div class="container footer-inner"><div>© 2026 koperbaarkopen</div><div>Premium verkoop van koperbaren met certificaat</div></div></footer>
    <script src="script.js"></script>
  </body>
</html>
```

---

## `contact.html`

```html
<!doctype html>
<html lang="nl">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Contact - koperbaarkopen</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <header class="header"><div class="container header-inner"><a class="brand" href="index.html"><div class="brand-title">koperbaarkopen</div><div class="brand-subtitle">Premium koperbaren met certificaat</div></a><nav class="nav"><a class="nav-btn" href="index.html">Home</a><a class="nav-btn" href="producten.html">Producten</a><a class="nav-btn" href="certificaten.html">Certificaten</a><a class="nav-btn" href="contact.html">Contact</a><a class="nav-btn" href="winkelwagen.html" data-cart-count>Winkelwagen</a></nav></div></header>
    <main class="page">
      <div class="container" style="max-width: 960px;">
        <div class="panel">
          <div class="eyebrow">Contact</div>
          <h1 class="page-title">Neem contact met ons op</h1>
          <p class="lead">Heb je een vraag over producten, levering of een grotere aanvraag? Neem dan contact met ons op.</p>
          <form class="section-gap" style="display:grid; gap:20px;">
            <label><span class="field-label">Naam</span><input placeholder="Jouw naam" /></label>
            <label><span class="field-label">Bedrijf <span class="optional">(optioneel)</span></span><input placeholder="Bedrijfsnaam" /></label>
            <label><span class="field-label">E-mail</span><input type="email" placeholder="jouw@email.nl" /></label>
            <label><span class="field-label">Bericht</span><textarea placeholder="Typ hier je bericht of vraag."></textarea></label>
            <button type="button" class="primary-btn">Verstuur bericht</button>
          </form>
        </div>
      </div>
    </main>
    <footer class="footer"><div class="container footer-inner"><div>© 2026 koperbaarkopen</div><div>Premium verkoop van koperbaren met certificaat</div></div></footer>
    <script src="script.js"></script>
  </body>
</html>
```

---

## `winkelwagen.html`

```html
<!doctype html>
<html lang="nl">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Winkelwagen - koperbaarkopen</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <header class="header"><div class="container header-inner"><a class="brand" href="index.html"><div class="brand-title">koperbaarkopen</div><div class="brand-subtitle">Premium koperbaren met certificaat</div></a><nav class="nav"><a class="nav-btn" href="index.html">Home</a><a class="nav-btn" href="producten.html">Producten</a><a class="nav-btn" href="certificaten.html">Certificaten</a><a class="nav-btn" href="contact.html">Contact</a><a class="nav-btn" href="winkelwagen.html" data-cart-count>Winkelwagen</a></nav></div></header>
    <main class="page">
      <div class="container" style="max-width: 1040px;">
        <div class="cart-layout">
          <div class="panel">
            <div class="eyebrow">Winkelwagen</div>
            <h1 class="page-title">Jouw geselecteerde producten</h1>
            <div class="section-gap" id="cart-items"></div>
          </div>
          <div class="panel panel-dark">
            <div class="eyebrow">Overzicht</div>
            <h2 class="section-title">Verder naar betalen</h2>
            <div class="section-gap">
              <div class="summary-row"><span>Subtotaal</span><span id="cart-subtotal">€0,00</span></div>
              <div class="summary-row"><span>Verzending</span><span>Berekenen bij afrekenen</span></div>
              <div class="summary-total"><span>Totaal</span><span id="cart-total">€0,00</span></div>
            </div>
            <button class="primary-btn section-gap" style="width:100%;" id="go-payment-btn">Ga naar betaalpagina</button>
          </div>
        </div>
      </div>
    </main>
    <footer class="footer"><div class="container footer-inner"><div>© 2026 koperbaarkopen</div><div>Premium verkoop van koperbaren met certificaat</div></div></footer>
    <script src="script.js"></script>
  </body>
</html>
```

---

## `betalen.html`

```html
<!doctype html>
<html lang="nl">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Betalen - koperbaarkopen</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <header class="header"><div class="container header-inner"><a class="brand" href="index.html"><div class="brand-title">koperbaarkopen</div><div class="brand-subtitle">Premium koperbaren met certificaat</div></a><nav class="nav"><a class="nav-btn" href="index.html">Home</a><a class="nav-btn" href="producten.html">Producten</a><a class="nav-btn" href="certificaten.html">Certificaten</a><a class="nav-btn" href="contact.html">Contact</a><a class="nav-btn" href="winkelwagen.html" data-cart-count>Winkelwagen</a></nav></div></header>
    <main class="page">
      <div class="container" style="max-width: 1040px;">
        <div class="payment-layout">
          <div class="panel">
            <div class="eyebrow">Betaalpagina</div>
            <h1 class="page-title">Vul je gegevens in</h1>
            <form class="section-gap" style="display:grid; gap:20px;">
              <input placeholder="Volledige naam" />
              <input placeholder="E-mailadres" />
              <input placeholder="Adres" />
              <div class="grid-2">
                <input placeholder="Postcode" />
                <input placeholder="Plaats" />
              </div>
              <select>
                <option>iDEAL</option>
                <option>Bancontact</option>
                <option>Creditcard</option>
                <option>Bankoverschrijving</option>
              </select>
            </form>
          </div>
          <div class="panel panel-dark">
            <div class="eyebrow">Besteloverzicht</div>
            <h2 class="section-title">Controleer en betaal</h2>
            <div class="section-gap" id="payment-summary"></div>
            <button class="primary-btn section-gap" style="width:100%;" id="complete-order-btn">Bestelling afronden</button>
          </div>
        </div>
      </div>
    </main>
    <footer class="footer"><div class="container footer-inner"><div>© 2026 koperbaarkopen</div><div>Premium verkoop van koperbaren met certificaat</div></div></footer>
    <script src="script.js"></script>
  </body>
</html>
```

---

## `product-250g.html`

```html
<!doctype html>
<html lang="nl">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Koperbaar 250 g - koperbaarkopen</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <header class="header"><div class="container header-inner"><a class="brand" href="index.html"><div class="brand-title">koperbaarkopen</div><div class="brand-subtitle">Premium koperbaren met certificaat</div></a><nav class="nav"><a class="nav-btn" href="index.html">Home</a><a class="nav-btn" href="producten.html">Producten</a><a class="nav-btn" href="certificaten.html">Certificaten</a><a class="nav-btn" href="contact.html">Contact</a><a class="nav-btn" href="winkelwagen.html" data-cart-count>Winkelwagen</a></nav></div></header>
    <main class="page" data-product-slug="koperbaar-250g">
      <div class="container">
        <div class="inline-actions"><a class="secondary-btn" href="producten.html">Terug naar producten</a><a class="secondary-btn" href="index.html">Home</a></div>
        <div class="split section-gap">
          <div class="panel"><div class="hero-card-frame"><div class="hero-card-inner"><div class="eyebrow">Aparte productpagina</div><div class="product-visual" style="height:288px; margin-top:20px;"></div></div></div></div>
          <div class="panel panel-dark">
            <div class="badge" id="detail-badge"></div>
            <h1 class="page-title" id="detail-title" style="margin-top:20px;"></h1>
            <div class="price" id="detail-price"></div>
            <p class="lead" id="detail-description"></p>
            <div class="grid-2 section-gap" id="detail-features"></div>
            <div class="product-actions"><button class="primary-btn" id="detail-add-btn">Voeg toe aan winkelmand</button><a class="secondary-btn" href="producten.html">Bekijk andere producten</a></div>
          </div>
        </div>
      </div>
    </main>
    <footer class="footer"><div class="container footer-inner"><div>© 2026 koperbaarkopen</div><div>Premium verkoop van koperbaren met certificaat</div></div></footer>
    <script src="script.js"></script>
  </body>
</html>
```

---

## `product-500g.html`

```html
<!doctype html>
<html lang="nl">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Koperbaar 500 g - koperbaarkopen</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <header class="header"><div class="container header-inner"><a class="brand" href="index.html"><div class="brand-title">koperbaarkopen</div><div class="brand-subtitle">Premium koperbaren met certificaat</div></a><nav class="nav"><a class="nav-btn" href="index.html">Home</a><a class="nav-btn" href="producten.html">Producten</a><a class="nav-btn" href="certificaten.html">Certificaten</a><a class="nav-btn" href="contact.html">Contact</a><a class="nav-btn" href="winkelwagen.html" data-cart-count>Winkelwagen</a></nav></div></header>
    <main class="page" data-product-slug="koperbaar-500g">
      <div class="container">
        <div class="inline-actions"><a class="secondary-btn" href="producten.html">Terug naar producten</a><a class="secondary-btn" href="index.html">Home</a></div>
        <div class="split section-gap">
          <div class="panel"><div class="hero-card-frame"><div class="hero-card-inner"><div class="eyebrow">Aparte productpagina</div><div class="product-visual" style="height:288px; margin-top:20px;"></div></div></div></div>
          <div class="panel panel-dark">
            <div class="badge" id="detail-badge"></div>
            <h1 class="page-title" id="detail-title" style="margin-top:20px;"></h1>
            <div class="price" id="detail-price"></div>
            <p class="lead" id="detail-description"></p>
            <div class="grid-2 section-gap" id="detail-features"></div>
            <div class="product-actions"><button class="primary-btn" id="detail-add-btn">Voeg toe aan winkelmand</button><a class="secondary-btn" href="producten.html">Bekijk andere producten</a></div>
          </div>
        </div>
      </div>
    </main>
    <footer class="footer"><div class="container footer-inner"><div>© 2026 koperbaarkopen</div><div>Premium verkoop van koperbaren met certificaat</div></div></footer>
    <script src="script.js"></script>
  </body>
</html>
```

---

## `product-1kg.html`

```html
<!doctype html>
<html lang="nl">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Koperbaar 1 kg - koperbaarkopen</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <header class="header"><div class="container header-inner"><a class="brand" href="index.html"><div class="brand-title">koperbaarkopen</div><div class="brand-subtitle">Premium koperbaren met certificaat</div></a><nav class="nav"><a class="nav-btn" href="index.html">Home</a><a class="nav-btn" href="producten.html">Producten</a><a class="nav-btn" href="certificaten.html">Certificaten</a><a class="nav-btn" href="contact.html">Contact</a><a class="nav-btn" href="winkelwagen.html" data-cart-count>Winkelwagen</a></nav></div></header>
    <main class="page" data-product-slug="koperbaar-1kg">
      <div class="container">
        <div class="inline-actions"><a class="secondary-btn" href="producten.html">Terug naar producten</a><a class="secondary-btn" href="index.html">Home</a></div>
        <div class="split section-gap">
          <div class="panel"><div class="hero-card-frame"><div class="hero-card-inner"><div class="eyebrow">Aparte productpagina</div><div class="product-visual" style="height:288px; margin-top:20px;"></div></div></div></div>
          <div class="panel panel-dark">
            <div class="badge" id="detail-badge"></div>
            <h1 class="page-title" id="detail-title" style="margin-top:20px;"></h1>
            <div class="price" id="detail-price"></div>
            <p class="lead" id="detail-description"></p>
            <div class="grid-2 section-gap" id="detail-features"></div>
            <div class="product-actions"><button class="primary-btn" id="detail-add-btn">Voeg toe aan winkelmand</button><a class="secondary-btn" href="producten.html">Bekijk andere producten</a></div>
          </div>
        </div>
      </div>
    </main>
    <footer class="footer"><div class="container footer-inner"><div>© 2026 koperbaarkopen</div><div>Premium verkoop van koperbaren met certificaat</div></div></footer>
    <script src="script.js"></script>
  </body>
</html>
```

Deze opzet is nu een echte multi-page HTML-site met losse pagina’s voor Home, Producten, Certificaten, Contact, Winkelwagen, Betalen en aparte productpagina’s.
