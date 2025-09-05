import React from 'react';
import { WebView } from 'react-native-webview';

export default function App() {
  const htmlContent = `
  <!DOCTYPE html>
  <html lang="hi">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>श्री Dairy Farm</title>
      <style>
          body { font-family: Arial; background-color: #fffbe6; margin:0; padding:0;}
          header { background-color: #4CAF50; color:white; text-align:center; padding:20px 10px;}
          .container { padding:20px; }
          .product { background-color:#f0f8ff; margin:15px 0; padding:15px; border-radius:10px; box-shadow:1px 2px 5px rgba(0,0,0,0.2);}
          .product h3 { margin:0; }
          .product p { margin:5px 0; }
          .order-btn { background-color:#4CAF50; color:white; border:none; padding:10px 20px; margin-top:10px; border-radius:5px; cursor:pointer; font-size:16px;}
      </style>
  </head>
  <body>
      <header>
          <h1>श्री Dairy Farm</h1>
          <p>Contact: 8948090989</p>
      </header>
      <div class="container">
          <div class="product">
              <h3>Cow Milk</h3>
              <p>Price: ₹60 per litre</p>
              <button class="order-btn" onclick="order('Cow Milk',60)">Order via WhatsApp</button>
          </div>
          <div class="product">
              <h3>Buffalo Milk</h3>
              <p>Price: ₹80 per litre</p>
              <button class="order-btn" onclick="order('Buffalo Milk',80)">Order via WhatsApp</button>
          </div>
      </div>
      <script>
          function order(product, price) {
              var qty = prompt("कृपया कितनी quantity चाहिये (" + product + ") में (in litres):");
              if(qty && !isNaN(qty)) {
                  var msg = "नमस्ते, मैं " + qty + " litre " + product + " order करना चाहता हूँ। कुल ₹" + (qty*price) + "।";
                  window.location.href = "https://wa.me/918948090989?text=" + encodeURIComponent(msg);
              } else {
                  alert('कृपया valid quantity enter करें।');
              }
          }
      </script>
  </body>
  </html>import React from 'react';
import { Alert } from 'react-native';
import { WebView } from 'react-native-webview';

export default function App() {
  const htmlContent = `
  <!DOCTYPE html>
  <html lang="hi">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>श्री Dairy Farm</title>
      <style>
          body { font-family: Arial; background-color: #fffbe6; margin:0; padding:0;}
          header { background-color: #4CAF50; color:white; text-align:center; padding:20px 10px;}
          .container { padding:20px; }
          .product { background-color:#f0f8ff; margin:15px 0; padding:15px; border-radius:10px; box-shadow:1px 2px 5px rgba(0,0,0,0.2);}
          .product h3 { margin:0; }
          .product p { margin:5px 0; }
          .order-btn { background-color:#4CAF50; color:white; border:none; padding:10px 20px; margin-top:10px; border-radius:5px; cursor:pointer; font-size:16px;}
      </style>
  </head>
  <body>
      <header>
          <h1>श्री Dairy Farm</h1>
          <p>Contact: 8948090989</p>
      </header>
      <div class="container">
          <div class="product">
              <h3>Cow Milk</h3>
              <p>Price: ₹60 per litre</p>
              <button class="order-btn" onclick="order('Cow Milk',60)">Order via WhatsApp</button>
          </div>
          <div class="product">
              <h3>Buffalo Milk</h3>
              <p>Price: ₹80 per litre</p>
              <button class="order-btn" onclick="order('Buffalo Milk',80)">Order via WhatsApp</button>
          </div>
      </div>
      <script>
          function order(product, price) {
              var qty = prompt("कृपया कितनी quantity चाहिये (" + product + ") में (in litres):");
              if(qty && !isNaN(qty)) {
                  var msg = "नमस्ते, मैं " + qty + " litre " + product + " order करना चाहता हूँ। कुल ₹" + (qty*price) + "।";
                  window.location.href = "https://wa.me/918948090989?text=" + encodeURIComponent(msg);
              } else {
                  alert('कृपया valid quantity enter करें।');
              }
          }
      </script>
  </body>
  </html>
  `;

  return (
    <WebView
      originWhitelist={['*']}
      source={{ html: htmlContent }}
      javaScriptEnabled={true}
    />
  );
}
banner.jpg
cow1.jpg
buffalo1.jpg
milk.jpg
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Shree Dairy Farm</title>
<style>
/* --- General --- */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #fdf6e3;
    color: #333;
    line-height: 1.6;
}

/* --- Banner --- */
.banner {
    position: relative;
    text-align: center;
}
.banner img {
    width: 100%;
    height: 300px;
    object-fit: cover;
}
.banner-text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: white;
    text-shadow: 1px 1px 5px black;
}

/* --- Navigation --- */
nav {
    display: flex;
    justify-content: center;
    background: #2e7d32;
}
nav a {
    color: white;
    padding: 1rem 2rem;
    text-decoration: none;
}
nav a:hover {
    background-color: #1b5e20;
}

/* --- Sections --- */
section {
    padding: 2rem;
    text-align: center;
}

/* --- Products --- */
.product-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 2rem;
}
.product {
    border: 1px solid #ddd;
    padding: 1.5rem;
    width: 220px;
    border-radius: 10px;
    background: #fff;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}
.product h3 {
    margin-bottom: 0.5rem;
}
.order-btn {
    display: inline-block;
    margin-top: 1rem;
    padding: 0.5rem 1rem;
    background-color: #4caf50;
    color: white;
    text-decoration: none;
    border-radius: 5px;
}
.order-btn:hover {
    background-color: #388e3c;
}

/* --- Gallery --- */
.gallery-images {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 1rem;
}
.gallery-images img {
    width: 220px;
    height: 150px;
    object-fit: cover;
    border-radius: 10px;
}

/* --- Testimonials --- */
.testimonial-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 1.5rem;
}
.testimonial {
    background: #fff;
    padding: 1rem;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    width: 250px;
}
.testimonial p {
    font-style: italic;
}
.testimonial span {
    display: block;
    margin-top: 0.5rem;
    font-weight: bold;
}

/* --- Order Form --- */
#orderForm {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1rem;
}
#orderForm input,
#orderForm select,
#orderForm textarea,
#orderForm button {
    width: 300px;
    padding: 0.8rem;
    border-radius: 5px;
    border: 1px solid #ccc;
    font-size: 1rem;
}
#orderForm button {
    background-color: #4caf50;
    color: white;
    border: none;
    cursor: pointer;
}
#orderForm button:hover {
    background-color: #388e3c;
}
#orderForm textarea {
    height: 80px;
    resize: none;
}

/* --- Footer --- */
footer {
    background-color: #4caf50;
    color: white;
    text-align: center;
    padding: 1rem 0;
    margin-top: 2rem;
}

/* --- Responsive --- */
@media(max-width: 768px){
    .product-list, .gallery-images, .testimonial-list {
        flex-direction: column;
        align-items: center;
    }
    #orderForm input,
    #orderForm select,
    #orderForm textarea,
    #orderForm button {
        width: 90%;
    }
}
</style>
</head>
<body>

<!-- Banner -->
<div class="banner">
    <img src="images/banner.jpg" alt="Shree Dairy Farm Banner">
    <div class="banner-text">
        <h1>Shree Dairy Farm</h1>
        <p>Fresh Milk & Dairy Products Straight From Our Farm</p>
    </div>
</div>

<!-- Navigation -->
<nav>
    <a href="#home">Home</a>
    <a href="#products">Products</a>
    <a href="#gallery">Gallery</a>
    <a href="#testimonials">Testimonials</a>
    <a href="#order">Place Order</a>
    <a href="#contact">Contact</a>
</nav>

<!-- Home Section -->
<section id="home">
    <h2>Welcome to Shree Dairy Farm</h2>
    <p>Providing fresh and high-quality milk and dairy products directly from our farm to your home.</p>
</section>

<!-- Products Section -->
<section id="products">
    <h2>Our Products</h2>
    <div class="product-list">
        <div class="product">
            <h3>Cow Milk</h3>
            <p>₹60 / Litre</p>
            <a class="order-btn" href="https://wa.me/918948090989?text=I%20want%20to%20order%20Cow%20Milk">Order on WhatsApp</a>
        </div>
        <div class="product">
            <h3>Buffalo Milk</h3>
            <p>₹80 / Litre</p>
            <a class="order-btn" href="https://wa.me/918948090989?text=I%20want%20to%20order%20Buffalo%20Milk">Order on WhatsApp</a>
        </div>
        <div class="product">
            <h3>Paneer</h3>
            <p>Fresh & Homemade</p>
            <a class="order-btn" href="https://wa.me/918948090989?text=I%20want%20to%20order%20Paneer">Order on WhatsApp</a>
        </div>
        <div class="product">
            <h3>Ghee</h3>
            <p>Pure & Natural</p>
            <a class="order-btn" href="https://wa.me/918948090989?text=I%20want%20to%20order%20Ghee">Order on WhatsApp</a>
        </div>
    </div>
</section>

<!-- Gallery Section -->
<section id="gallery">
    <h2>Gallery</h2>
    <div class="gallery-images">
        <img src="images/cow1.jpg" alt="Cow">
        <img src="images/buffalo1.jpg" alt="Buffalo">
        <img src="images/milk.jpg" alt="Milk">
    </div>
</section>

<!-- Testimonials Section -->
<section id="testimonials">
    <h2>Customer Testimonials</h2>
    <div class="testimonial-list">
        <div class="testimonial">
            <p>"The milk is always fresh and delicious. Highly recommend Shree Dairy Farm!"</p>
            <span>- Ramesh Kumar</span>
        </div>
        <div class="testimonial">
            <p>"Great service and quality products. Love their paneer and ghee."</p>
            <span>- Sita Devi</span>
        </div>
        <div class="testimonial">
            <p>"Reliable and fresh dairy products delivered right to my home."</p>
            <span>- Ajay Singh</span>
        </div>
    </div>
</section>

<!-- Order Form Section -->
<section id="order">
    <h2>Place Your Order</h2>
    <form id="orderForm">
        <input type="text" id="name" placeholder="Your Name" required>
        <input type="tel" id="phone" placeholder="Phone Number" required>
        <input type="text" id="location" placeholder="Delivery Address / Location" required>
        <select id="product" required>
            <option value="">Select Product</option>
            <option value="Cow Milk">Cow Milk</option>
            <option value="Buffalo Milk">Buffalo Milk</option>
            <option value="Paneer">Paneer</option>
            <option value="Ghee">Ghee</option>
        </select>
        <input type="number" id="quantity" placeholder="Quantity" required>
        <textarea id="message" placeholder="Additional Message (Optional)"></textarea>
        <button type="submit">Submit Order</button>
    </form>
</section>

<!-- Contact Section -->
<section id="contact">
    <h2>Contact Us</h2>
    <p>Phone: 8948090989</p>
    <p>WhatsApp: <a href="https://wa.me/918948090989">Chat Now</a></p>
</section>

<footer>
    <p>© 2025 Shree Dairy Farm</p>
</footer>

<!-- Order Form Script -->
<script>
const form = document.getElementById('orderForm');
form.addEventListener('submit', function(e) {
    e.preventDefault();
    const name = document.getElementById('name').value;
    const phone = document.getElementById('phone').value;
    const location = document.getElementById('location').value;
    const product = document.getElementById('product').value;
    const quantity = document.getElementById('quantity').value;
    const message = document.getElementById('message').value;

    const text = `Hello, I want to order:
Name: ${name}
Phone: ${phone}
Location: ${location}
Product: ${product}
Quantity: ${quantity}
Message: ${message}`;

    const url = `https://wa.me/918948090989?text=${encodeURIComponent(text)}`;
    window.open(url, '_blank');
});
</script>

</body>
</html>
import React from 'react';
import { WebView } from 'react-native-webview';

export default function App() {
  const htmlContent = `
  <!DOCTYPE html>
  <html lang="hi">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>श्री Dairy Farm</title>
      <style>
          body { font-family: Arial; background-color: #fffbe6; margin:0; padding:0;}
          header { background-color: #4CAF50; color:white; text-align:center; padding:20px 10px;}
          .container { padding:20px; }
          .product { background-color:#f0f8ff; margin:15px 0; padding:15px; border-radius:10px; box-shadow:1px 2px 5px rgba(0,0,0,0.2);}
          .product h3 { margin:0; }
          .product p { margin:5px 0; }
          .order-btn { background-color:#4CAF50; color:white; border:none; padding:10px 20px; margin-top:10px; border-radius:5px; cursor:pointer; font-size:16px;}
      </style>
  </head>
  <body>
      <header>
          <h1>श्री Dairy Farm</h1>
          <p>Contact: 8948090989</p>
      </header>
      <div class="container">
          <div class="product">
              <h3>Cow Milk</h3>
              <p>Price: ₹60 per litre</p>
              <button class="order-btn" onclick="order('Cow Milk',60)">Order via WhatsApp</button>
          </div>
          <div class="product">
              <h3>Buffalo Milk</h3>
              <p>Price: ₹80 per litre</p>
              <button class="order-btn" onclick="order('Buffalo Milk',80)">Order via WhatsApp</button>
          </div>
      </div>
      <script>
          function order(product, price) {
              var qty = prompt("कृपया कितनी quantity चाहिये (" + product + ") में (in litres):");
              if(qty && !isNaN(qty)) {
                  var msg = "नमस्ते, मैं " + qty + " litre " + product + " order करना चाहता हूँ। कुल ₹" + (qty*price) + "।";
                  window.location.href = "https://wa.me/918948090989?text=" + encodeURIComponent(msg);
              } else {
                  alert('कृपया valid quantity enter करें।');
              }
          }
      </script>
  </body>
  </html>
  `;

  return (
    <WebView
      originWhitelist={['*']}
      source={{ html: htmlContent }}
      javaScriptEnabled={true}
    />
  );
}
import React from 'react';
import { Alert } from 'react-native';
import { WebView } from 'react-native-webview';

export default function App() {
  const htmlContent = `
  <!DOCTYPE html>
  <html lang="hi">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>श्री Dairy Farm</title>
      <style>
          body { font-family: Arial; background-color: #fffbe6; margin:0; padding:0;}
          header { background-color: #4CAF50; color:white; text-align:center; padding:20px 10px;}
          .container { padding:20px; }
          .product { background-color:#f0f8ff; margin:15px 0; padding:15px; border-radius:10px; box-shadow:1px 2px 5px rgba(0,0,0,0.2);}
          .product h3 { margin:0; }
          .product p { margin:5px 0; }
          .order-btn { background-color:#4CAF50; color:white; border:none; padding:10px 20px; margin-top:10px; border-radius:5px; cursor:pointer; font-size:16px;}
      </style>
  </head>
  <body>
      <header>
          <h1>श्री Dairy Farm</h1>
          <p>Contact: 8948090989</p>
      </header>
      <div class="container">
          <div class="product">
              <h3>Cow Milk</h3>
              <p>Price: ₹60 per litre</p>
              <button class="order-btn" onclick="order('Cow Milk',60)">Order via WhatsApp</button>
          </div>
          <div class="product">
              <h3>Buffalo Milk</h3>
              <p>Price: ₹80 per litre</p>
              <button class="order-btn" onclick="order('Buffalo Milk',80)">Order via WhatsApp</button>
          </div>
      </div>
      <script>
          function order(product, price) {
              var qty = prompt("कृपया कितनी quantity चाहिये (" + product + ") में (in litres):");
              if(qty && !isNaN(qty)) {
                  var msg = "नमस्ते, मैं " + qty + " litre " + product + " order करना चाहता हूँ। कुल ₹" + (qty*price) + "।";
                  window.location.href = "https://wa.me/918948090989?text=" + encodeURIComponent(msg);
              } else {
                  alert('कृपया valid quantity enter करें।');
              }
          }
      </script>
  </body>
  </html>
  `;

  return (
    <WebView
      originWhitelist={['*']}
      source={{ html: htmlContent }}
      javaScriptEnabled={true}
    />
  );
}
ShreeDairyFarmApp/
│
├─ App.js                # React Native WebView app with your HTML
├─ package.json          # Project dependencies
├─ app.json              # Expo app configuration
├─ assets/
│   └─ (images, logos optional)
├─ node_modules/
│   └─ (auto generated by npm install)
└─ babel.config.js       # Babel config for Expo
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Shree Dairy Farm</title>
<style>
body {font-family: Arial; margin:0; padding:0; background:#fdf6e3; color:#333; line-height:1.6;}
.banner {position: relative; text-align: center;}
.banner img {width:100%; height:300px; object-fit: cover;}
.banner-text {position:absolute; top:50%; left:50%; transform:translate(-50%, -50%); color:white; text-shadow:1px 1px 5px black;}
nav {display:flex; justify-content:center; background:#2e7d32;}
nav a {color:white; padding:1rem 2rem; text-decoration:none;}
nav a:hover {background:#1b5e20;}
section {padding:2rem; text-align:center;}
.product-list {display:flex; flex-wrap:wrap; justify-content:center; gap:2rem;}
.product {border:1px solid #ddd; padding:1.5rem; width:220px; border-radius:10px; background:#fff; box-shadow:0 4px 6px rgba(0,0,0,0.1);}
.product h3 {margin-bottom:0.5rem;}
.order-btn {display:inline-block; margin-top:1rem; padding:0.5rem 1rem; background:#4caf50; color:white; text-decoration:none; border-radius:5px;}
.order-btn:hover {background:#388e3c;}
.gallery-images {display:flex; flex-wrap:wrap; justify-content:center; gap:1rem;}
.gallery-images img {width:220px; height:150px; object-fit:cover; border-radius:10px;}
.testimonial-list {display:flex; flex-wrap:wrap; justify-content:center; gap:1.5rem;}
.testimonial {background:#fff; padding:1rem; border-radius:10px; box-shadow:0 4px 6px rgba(0,0,0,0.1); width:250px;}
.testimonial p {font-style:italic;}
.testimonial span {display:block; margin-top:0.5rem; font-weight:bold;}
#orderForm {display:flex; flex-direction:column; align-items:center; gap:1rem;}
#orderForm input, #orderForm select, #orderForm textarea, #orderForm button {width:300px; padding:0.8rem; border-radius:5px; border:1px solid #ccc; font-size:1rem;}
#orderForm button {background:#4caf50; color:white; border:none; cursor:pointer;}
#orderForm button:hover {background:#388e3c;}
#orderForm textarea {height:80px; resize:none;}
footer {background:#4caf50; color:white; text-align:center; padding:1rem 0; margin-top:2rem;}
@media(max-width:768px){.product-list,.gallery-images,.testimonial-list{flex-direction:column; align-items:center;}#orderForm input,#orderForm select,#orderForm textarea,#orderForm button{width:90%;}}
</style>
</head>
<body>

<div class="banner">
    <img src="images/banner.jpg" alt="Shree Dairy Farm Banner">
    <div class="banner-text">
        <h1>Shree Dairy Farm</h1>
        <p>Fresh Milk & Dairy Products Straight From Our Farm</p>
    </div>
</div>

<nav>
    <a href="#home">Home</a>
    <a href="#products">Products</a>
    <a href="#gallery">Gallery</a>
    <a href="#testimonials">Testimonials</a>
    <a href="#order">Place Order</a>
    <a href="#contact">Contact</a>
</nav>

<section id="home">
    <h2>Welcome to Shree Dairy Farm</h2>
    <p>Providing fresh and high-quality milk and dairy products directly from our farm to your home.</p>
</section>

<section id="products">
    <h2>Our Products</h2>
    <div class="product-list">
        <div class="product"><h3>Cow Milk</h3><p>₹60 / Litre</p><a class="order-btn" href="https://wa.me/918948090989?text=I%20want%20to%20order%20Cow%20Milk">Order on WhatsApp</a></div>
        <div class="product"><h3>Buffalo Milk</h3><p>₹80 / Litre</p><a class="order-btn" href="https://wa.me/918948090989?text=I%20want%20to%20order%20Buffalo%20Milk">Order on WhatsApp</a></div>
        <div class="product"><h3>Paneer</h3><p>Fresh & Homemade</p><a class="order-btn" href="https://wa.me/918948090989?text=I%20want%20to%20order%20Paneer">Order on WhatsApp</a></div>
        <div class="product"><h3>Ghee</h3><p>Pure & Natural</p><a class="order-btn" href="https://wa.me/918948090989?text=I%20want%20to%20order%20Ghee">Order on WhatsApp</a></div>
    </div>
</section>

<section id="gallery">
    <h2>Gallery</h2>
    <div class="gallery-images">
        <img src="images/cow1.jpg" alt="Cow">
        <img src="images/buffalo1.jpg" alt="Buffalo">
        <img src="images/milk.jpg" alt="Milk">
    </div>
</section>

<section id="testimonials">
    <h2>Customer Testimonials</h2>
    <div class="testimonial-list">
        <div class="testimonial"><p>"The milk is always fresh and delicious. Highly recommend Shree Dairy Farm!"</p><span>- Ramesh Kumar</span></div>
        <div class="testimonial"><p>"Great service and quality products. Love their paneer and ghee."</p><span>- Sita Devi</span></div>
        <div class="testimonial"><p>"Reliable and fresh dairy products delivered right to my home."</p><span>- Ajay Singh</span></div>
    </div>
</section>

<section id="order">
    <h2>Place Your Order</h2>
    <form id="orderForm">
        <input type="text" id="name" placeholder="Your Name" required>
        <input type="tel" id="phone" placeholder="Phone Number" required>
        <input type="text" id="location" placeholder="Delivery Address / Location" required>
        <select id="product" required>
            <option value="">Select Product</option>
            <option value="Cow Milk">Cow Milk</option>
            <option value="Buffalo Milk">Buffalo Milk</option>
            <option value="Paneer">Paneer</option>
            <option value="Ghee">Ghee</option>
        </select>
        <input type="number" id="quantity" placeholder="Quantity" required>
        <textarea id="message" placeholder="Additional Message (Optional)"></textarea>
        <button type="submit">Submit Order</button>
    </form>
</section>

<section id="contact">
    <h2>Contact Us</h2>
    <p>Phone: 8948090989</p>
    <p>WhatsApp: <a href="https://wa.me/918948090989">Chat Now</a></p>
</section>

<footer>
    <p>© 2025 Shree Dairy Farm</p>
</footer>

<script>
const form = document.getElementById('orderForm');
form.addEventListener('submit', function(e){
    e.preventDefault();
    const name = document.getElementById('name').value;
    const phone = document.getElementById('phone').value;
    const location = document.getElementById('location').value;
    const product = document.getElementById('product').value;
    const quantity = document.getElementById('quantity').value;
    const message = document.getElementById('message').value;

    const text = `Hello, I want to order:
Name: ${name}
Phone: ${phone}
Location: ${location}
Product: ${product}
Quantity: ${quantity}
Message: ${message}`;

    const url = `https://wa.me/918948090989?text=${encodeURIComponent(text)}`;
    window.open(url,'_blank');
});
</script>
</body>
</html>
<!-- Product Cards Section -->
<div class="container" id="products">
  <h2 style="text-align:center; margin-bottom:20px;">Our Products</h2>
  <div class="products">
    <div class="product-card">
      <img src="https://i.ibb.co/3mM8rXY/buffalo-milk.jpg" alt="Buffalo Milk">
      <h3>Milk (Buffalo)</h3>
      <p>₹80 per liter</p>
      <button onclick="orderProduct('Milk')">Order Now</button>
    </div>
    <div class="product-card">
      <img src="https://i.ibb.co/54Dp3ZQ/cow-milk.jpg" alt="Cow Milk">
      <h3>Milk (Cow)</h3>
      <p>₹60 per liter</p>
      <button onclick="orderProduct('Milk')">Order Now</button>
    </div>
    <div class="product-card">
      <img src="https://i.ibb.co/5LqLk0Y/paneer.jpg" alt="Paneer">
      <h3>Paneer</h3>
      <p>₹250 per kg</p>
      <button onclick="orderProduct('Paneer')">Order Now</button>
    </div>
    <div class="product-card">
      <img src="https://i.ibb.co/yg7K3Qv/ghee.jpg" alt="Ghee">
      <h3>Ghee</h3>
      <p>₹1200 per kg</p>
      <button onclick="orderProduct('Ghee')">Order Now</button>
    </div>
  </div>
</div>

  `;

  return (
    <WebView
      originWhitelist={['*']}
      source={{ html: htmlContent }}
      javaScriptEnabled={true}
    />
  );
}
