# 🛒VISIONS IN PAINT LLC

A modern web application that allows users to browse images, leave comments, and purchase products seamlessly.

## 🚀 Features

- 🖼️ Image gallery with responsive layouts  
- 💬 User comments and reviews  
- 🛍️ Product purchasing & checkout flow  
- 🔐 User authentication (login / signup)  
- 📱 Mobile-friendly design  

---

## 🧰 Tech Stack

**Frontend**
- HTML / CSS / JavaScript
- Framework: React / Next.js / Vue *(update as needed)*

**Backend**
- Node.js / Express / Django / etc.
- REST or GraphQL API

**Database**
- PostgreSQL / MongoDB / Firebase

**Payments**
- Stripe / PayPal *(or placeholder for now)*

---

## 📸 Screenshots

![Homepage](screenshots/homepage.png)
![Product Page](screenshots/product.png)
![Checkout](screenshots/checkout.png)

> Add images to a `/screenshots` folder in your repo.

---

##Project Structure

visions-in-paint/
├── jekyll-site/
│   └── _config.yml
├── server/
│   ├── index.js
│   └── routes/
│       ├── payments.js
│       └── users.js
└── .env

const express = require("express");
const Stripe = require("stripe");
require("dotenv").config();

const app = express();
const stripe = Stripe(process.env.STRIPE_SECRET_KEY);

app.use(express.json());

app.post("/create-checkout-session", async (req, res) => {
  const session = await stripe.checkout.sessions.create({
    payment_method_types: ["card"],
    line_items: [{
      price_data: {
        currency: "usd",
        product_data: { name: "Artwork" },
        unit_amount: 5000,
      },
      quantity: 1,
    }],
    mode: "payment",
    success_url: "http://localhost:4000/success",
    cancel_url: "http://localhost:4000/cancel",
  });

  res.json({ url: session.url });
});

app.listen(4242, () => console.log("Server running on 4242"));

---

BASH

npm install express stripe dotenv
node index.js

---

<button onclick="checkout()">Buy</button>

<script>
async function checkout() {
  const res = await fetch("http://localhost:4242/create-checkout-session", {
    method: "POST"
  });
  const data = await res.json();
  window.location = data.url;
}
</script>

-
