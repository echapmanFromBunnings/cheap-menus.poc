---
layout: default
title: "The Gelato & Icecream Factory - Welcome"
---

<style>
  html, body {
    width: 100%;
    overflow-x: hidden;
    box-sizing: border-box;
  }
  
  *, *::before, *::after {
    box-sizing: inherit;
  }
  
  body {
    background: repeating-linear-gradient(
      0deg,
      #FFE8E8,
      #FFE8E8 20px,
      #FFD5D5 20px,
      #FFD5D5 40px
    );
    font-family: 'Courier New', monospace;
    color: #4A1F1F;
    margin: 0;
    padding: 0;
    min-height: 100vh;
    font-size: 20px;
  }
  
  .logo-header {
    text-align: center;
    padding: 40px 50px 30px 50px;
    border-bottom: 5px solid #4A1F1F;
    background: #FFF5E6;
    width: 100%;
  }
  
  .logo-header img {
    display: block;
    margin: 0 auto;
    max-width: 250px;
    width: 90%;
    height: auto;
    mix-blend-mode: multiply;
  }
  
  .container {
    background: #FFF5E6;
    padding: 50px;
    text-align: center;
    width: 100%;
  }
  
  .tagline {
    font-size: 3em;
    color: #C85A7A;
    margin: 30px 0 40px 0;
    font-style: italic;
    text-shadow: 2px 2px 0px #D4A574;
  }
  
  .welcome-text {
    font-size: 1.8em;
    line-height: 1.6;
    margin: 40px auto;
    max-width: 1200px;
    color: #4A1F1F;
    padding: 30px;
    background: rgba(255, 255, 255, 0.7);
    border-radius: 20px;
    border: 5px solid #C85A7A;
  }
  
  .features {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 25px;
    margin: 40px 0;
  }
  
  .feature-box {
    background: white;
    border: 5px solid #D4A574;
    border-radius: 15px;
    padding: 25px;
    box-shadow: 5px 5px 0px #C85A7A;
    transition: transform 0.3s ease;
  }
  
  .feature-box:hover {
    transform: scale(1.05) rotate(1deg);
  }
  
  .feature-icon {
    font-size: 4em;
    margin-bottom: 15px;
  }
  
  .feature-text {
    font-size: 1.6em;
    color: #4A1F1F;
    font-weight: bold;
  }
  
  .menu-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 35px;
    margin: 50px 0;
  }
  
  .menu-card {
    background: white;
    border: 6px solid #C85A7A;
    border-radius: 20px;
    padding: 40px 25px;
    box-shadow: 8px 8px 0px #D4A574;
    transition: all 0.3s ease;
    cursor: pointer;
    text-decoration: none;
    display: block;
  }
  
  .menu-card:hover {
    transform: scale(1.05) rotate(-1deg);
    box-shadow: 12px 12px 0px #4A1F1F;
  }
  
  .menu-number {
    font-size: 5em;
    color: #D4A574;
    font-weight: bold;
    text-shadow: 3px 3px 0px #C85A7A;
    margin-bottom: 15px;
  }
  
  .menu-title {
    font-size: 2em;
    color: #4A1F1F;
    font-weight: bold;
    margin-bottom: 15px;
  }
  
  .menu-description {
    font-size: 1.4em;
    color: #4A1F1F;
    line-height: 1.5;
  }
  
  .cta-button {
    display: inline-block;
    background: linear-gradient(45deg, #C85A7A, #D4A574);
    color: white;
    font-size: 2em;
    font-weight: bold;
    padding: 25px 50px;
    border-radius: 60px;
    text-decoration: none;
    margin: 35px 15px;
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
    transition: all 0.3s ease;
    border: 5px solid #4A1F1F;
  }
  
  .cta-button:hover {
    transform: scale(1.05) rotate(-1deg);
    box-shadow: 0 15px 35px rgba(0, 0, 0, 0.4);
  }
  
  .footer {
    margin-top: 50px;
    padding-top: 35px;
    border-top: 5px solid #C85A7A;
    font-size: 1.4em;
    color: #4A1F1F;
    font-style: italic;
  }
</style>

<div class="logo-header">
  <img src="{{ site.baseurl }}/logo.png" alt="The Gelato & Icecream Factory">
</div>

<div class="container">
  <p class="tagline">The Far-Out Ice Cream Experience!</p>
  
  <div class="welcome-text">
    <strong>Welcome to The Gelato & Icecream Factory!</strong><br>
    Step into our nostalgic parlor where every scoop is a journey back in time and every flavor is crafted with vintage charm! We're serving up the finest ice cream creations with that classic retro touch. ✨
  </div>
  
  <div class="features">
    <div class="feature-box">
      <div class="feature-icon">🍦</div>
      <div class="feature-text">20 Classic Flavors</div>
    </div>
    <div class="feature-box">
      <div class="feature-icon">🎨</div>
      <div class="feature-text">Retro Charm</div>
    </div>
    <div class="feature-box">
      <div class="feature-icon">💎</div>
      <div class="feature-text">Premium Quality</div>
    </div>
    <div class="feature-box">
      <div class="feature-icon">🎪</div>
      <div class="feature-text">Vintage Experience</div>
    </div>
  </div>
  
  <h2 style="font-size: 3.5em; color: #4A1F1F; margin: 40px 0 35px 0; text-shadow: 2px 2px 0px #D4A574;">
    📸 FULL MENU IMAGES 📸
  </h2>
  
  <div style="margin: 30px 0; text-align: center;">
    <a href="{{ site.baseurl }}/url-builder.html" class="cta-button" style="font-size: 1.6em; padding: 20px 35px;">
      🔗 BUILD CUSTOM SLIDESHOW URL 🔗
    </a>
    <p style="font-size: 1.3em; color: #4A1F1F; margin-top: 15px; font-style: italic;">
      Create custom URLs for digital signage with timing controls!
    </p>
  </div>
  
  <div class="menu-grid">
    <a href="{{ site.baseurl }}/5.html" class="menu-card">
      <div class="menu-number">5</div>
      <div class="menu-title">Menu Image 1</div>
      <div class="menu-description">
        View our full menu in high resolution!
      </div>
    </a>
    
    <a href="{{ site.baseurl }}/6.html" class="menu-card">
      <div class="menu-number">6</div>
      <div class="menu-title">Menu Image 2</div>
      <div class="menu-description">
        Browse our complete offerings!
      </div>
    </a>
    
    <a href="{{ site.baseurl }}/7.html" class="menu-card">
      <div class="menu-number">7</div>
      <div class="menu-title">Menu Image 3</div>
      <div class="menu-description">
        Explore all our delicious options!
      </div>
    </a>
    
    <a href="{{ site.baseurl }}/8.html" class="menu-card">
      <div class="menu-number">8</div>
      <div class="menu-title">Menu Image 4</div>
      <div class="menu-description">
        See everything we have to offer!
      </div>
    </a>
  </div>
  
  <div class="footer">
    <p>
      <strong>Hours:</strong> Open every day for your sweet tooth! 🌅<br>
      <strong>Location:</strong> Where memories are made! 📍<br>
      <strong>Motto:</strong> "Scooping happiness since forever!" 🍦
    </p>
  </div>
</div>
