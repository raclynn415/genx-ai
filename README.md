<!DOCTYPE html>
<html lang="en">
<head><!-- Updated with logo - version 2 -->
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>GenX AI - AI Video Generator</title>
  <style>
    body {
      font-family: system-ui, -apple-system, sans-serif;
      background: linear-gradient(135deg, #0a0a0a, #1a0033);
      color: white;
      text-align: center;
      padding: 20px;
      margin: 0;
      min-height: 100vh;
    }
    .logo-container img {
      max-width: 320px;
      height: auto;
      margin: 20px 0 10px;
      filter: drop-shadow(0 0 35px rgba(0, 255, 255, 0.9));
    }
    .tagline {
      font-size: 1.4rem;
      color: #ccc;
      margin-bottom: 40px;
    }
    input {
      width: 90%;
      max-width: 600px;
      padding: 18px;
      font-size: 1.1rem;
      background: #1f1f1f;
      border: 2px solid #00ffff;
      border-radius: 12px;
      color: white;
      margin-bottom: 20px;
    }
    button {
      background: linear-gradient(45deg, #00ffff, #ff00ff);
      color: black;
      border: none;
      padding: 16px 40px;
      font-size: 1.2rem;
      font-weight: bold;
      border-radius: 12px;
      cursor: pointer;
      margin: 10px;
      box-shadow: 0 0 25px rgba(0, 255, 255, 0.6);
    }
    .video-area {
      max-width: 620px;
      margin: 40px auto;
      background: #111;
      border-radius: 16px;
      padding: 25px;
      border: 2px dashed #00ffff;
    }
    .monetization {
      margin: 30px auto;
      max-width: 600px;
    }
    .demo-note {
      margin-top: 50px;
      color: #888;
      font-size: 0.95rem;
    }
  </style>
</head>
<body>
  <div class="logo-container">
    <img src="file_000000001e68722fb29f040fdd1afa52.png" alt="GenX AI Logo">
  </div>
  <p class="tagline">AI Video Generator</p>

  <input type="text" id="prompt" placeholder="Describe the video you want to create... (e.g. A cute robot dancing in neon city at night)">

  <br>
  <button onclick="generateDemo()">✨ Generate Video</button>

  <div class="video-area">
    <div id="loading" style="display:none; color:#00ffff; font-size:1.2rem; margin-bottom:15px;">Forging your video with neon energy...</div>
    <div id="result" style="color:#888;">
      <p>Your AI-generated video will appear here</p>
      <p style="font-size:0.95rem;">(Demo mode — real generation coming soon!)</p>
    </div>
  </div>

  <div class="monetization">
    <button onclick="alert('Credit packs coming soon! $4.99 for 10 videos')">Buy Credits</button>
    <button onclick="alert('Subscriptions coming soon! $4.99/mo Basic • $9.99/mo Pro')">Subscribe</button>
  </div>

  <div class="demo-note">
    GenX AI is in early development.<br>
    Made with ❤️ • Future Android app coming soon!<br>
    Follow for updates and more demo videos.
  </div>

  <script>
    function generateDemo() {
      const prompt = document.getElementById('prompt').value.trim() || "A futuristic neon scene";
      const loading = document.getElementById('loading');
      const result = document.getElementById('result');
      
      loading.style.display = 'block';
      result.style.display = 'none';

      setTimeout(() => {
        loading.style.display = 'none';
        result.innerHTML = `
          <p><strong>Prompt:</strong> ${prompt}</p>
          <p style="color:#00ffaa; font-size:1.2rem;">✅ Video forged successfully! (Demo)</p>
          <p>Imagine a beautiful AI-generated clip playing here 🔥</p>
          <p style="margin-top:20px; font-size:0.95rem;">Share this page and stay tuned for the full GenX AI app on Android!</p>
        `;
        result.style.display = 'block';
      }, 1800);
    }
  </script>
</body>
</html>
