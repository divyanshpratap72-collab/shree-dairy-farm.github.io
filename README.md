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
