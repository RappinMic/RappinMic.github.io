visions-in-paint/
├── _config.yml
├── Gemfile
├── index.html
├── gallery.html
├── shop.html
├── success.html
├── assets/
│   └── images/
│       ├── art1.jpg
│       ├── art2.jpg
│       └── art3.jpg
└── README.md

assets/images/

title: Visions in Paint LLC
description: Online Art Gallery & Shop
baseurl: ""
url: ""

theme: minima
markdown: kramdown

source "https://rubygems.org"

gem "jekyll", "~> 4.3"
gem "minima"

source "https://rubygems.org"

gem "jekyll", "~> 4.3"
gem "minima"

<!DOCTYPE html>
<html>
<head>
  <title>Visions in Paint LLC</title>
  <style>
    body { font-family: Arial; text-align: center; background: #f4f4f4; }
    header { background: black; color: white; padding: 20px; }
    nav a { margin: 15px; color: white; text-decoration: none; }
    img { width: 300px; margin: 10px; border-radius: 10px; }
    .btn { background: black; color: white; padding: 10px 20px; text-decoration: none; border-radius: 5px; }
  </style>
</head>
<body>

<header>
  <h1>🎨 Visions in Paint LLC</h1>
  <nav>
    <a href="gallery.html">Gallery</a>
    <a href="shop.html">Shop</a>
  </nav>
</header>

<h2>Welcome to Visions in Paint LLC</h2>
<p>Explore original artwork and purchase directly online.</p>

<img src="assets/images/art1.jpg">
<img src="assets/images/art2.jpg">
<img src="assets/images/art3.jpg">

<br><br>
<a class="btn" href="shop.html">Visit Shop</a>

</body>
</html>

<!DOCTYPE html>
<html>
<head>
  <title>Gallery - Visions in Paint LLC</title>
  <style>
    body { font-family: Arial; text-align: center; }
    img { width: 300px; margin: 15px; border-radius: 10px; }
  </style>
</head>
<body>

<h1>🖼️ Art Gallery</h1>

<img src="assets/images/art1.jpg">
<img src="assets/images/art2.jpg">
<img src="assets/images/art3.jpg">

<br><br>
<a href="index.html">Back Home</a>

</body>
</html>

<!DOCTYPE html>
<html>
<head>
  <title>Shop - Visions in Paint LLC</title>
  <style>
    body { font-family: Arial; text-align: center; }
    .product { margin: 20px; padding: 20px; border: 1px solid #ccc; }
    .btn { background: black; color: white; padding: 10px 20px; text-decoration: none; border-radius: 5px; }
  </style>
</head>
<body>

<!DOCTYPE html>
<html>
<head>
  <title>Shop - Visions in Paint LLC</title>
  <style>
    body { font-family: Arial; text-align: center; }
    .product { margin: 20px; padding: 20px; border: 1px solid #ccc; }
    .btn { background: black; color: white; padding: 10px 20px; text-decoration: none; border-radius: 5px; }
  </style>
</head>
<body>

<h1>🛒 Shop Art</h1>

<div class="product">
  <h2>Painting #1</h2>
  <img src="assets/images/art1.jpg" width="200">
  <p>$50.00</p>
  <a class="btn" href="https://buy.stripe.com/YOUR_STRIPE_LINK">Buy Now</a>
</div>

<div class="product">
  <h2>Painting #2</h2>
  <img src="assets/images/art2.jpg" width="200">
  <p>$75.00</p>
  <a class="btn" href="https://buy.stripe.com/YOUR_STRIPE_LINK">Buy Now</a>
</div>

<div class="product">
  <h2>Painting #3</h2>
  <img src="assets/images/art3.jpg" width="200">
  <p>$100.00</p>
  <a class="btn" href="https://buy.stripe.com/YOUR_STRIPE_LINK">Buy Now</a>
</div>

<br>
<a href="index.html">Back Home</a>

</body>
</html>

<!DOCTYPE html>
<html>
<head>
  <title>Payment Success</title>
</head>
<body>
  <h1>✅ Payment Successful</h1>
  <p>Thank you for supporting Visions in Paint LLC.</p>
  <a href="index.html">Return Home</a>
</body>
</html>

# 🎨 Visions in Paint LLC

A Jekyll-powered art gallery website with Stripe payments.

## 🚀 Features
- Art gallery
- Stripe payments
- Static website
- Mobile friendly
- Hosted on GitHub Pages

## ⚙️ Setup

```bash
git clone https://github.com/yourusername/visions-in-paint.git
cd visions-in-paint
bundle install
bundle exec jekyll serve
