---
layout: default
title: "The Gelato & Icecream Factory - Welcome"
---

<style>
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
  }
  
  .logo-header img {
    display: block;
    margin: 0 auto;
    max-width: 250px;
    width: 90%;
    height: auto;
  }
  
  .container {
    background: #FFF5E6;
    padding: 50px;
    text-align: center;
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
  <img src="logo.png" alt="The Gelato & Icecream Factory">
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
    🍨 EXPLORE OUR MENU 🍨
  </h2>
  
  <div class="menu-grid">
    <a href="1.html" class="menu-card">
      <div class="menu-number">1</div>
      <div class="menu-title">Classic Flavors</div>
      <div class="menu-description">
        Traditional favorites and timeless treats!
      </div>
    </a>
    
    <a href="2.html" class="menu-card">
      <div class="menu-number">2</div>
      <div class="menu-title">Premium Selections</div>
      <div class="menu-description">
        Upscale flavors for discerning tastes!
      </div>
    </a>
    
    <a href="3.html" class="menu-card">
      <div class="menu-number">3</div>
      <div class="menu-title">Specialty Creations</div>
      <div class="menu-description">
        Unique and creative combinations!
      </div>
    </a>
    
    <a href="4.html" class="menu-card">
      <div class="menu-number">4</div>
      <div class="menu-title">Ultimate Indulgences</div>
      <div class="menu-description">
        Decadent and extraordinary flavors!
      </div>
    </a>
  </div>
  
  <div style="margin: 40px 0;">
    <a href="1.html" class="cta-button">🌟 START YOUR FLAVOR JOURNEY 🌟</a>
  </div>
  
  <div class="footer">
    <p>
      <strong>Hours:</strong> Open every day for your sweet tooth! 🌅<br>
      <strong>Location:</strong> Where memories are made! 📍<br>
      <strong>Motto:</strong> "Scooping happiness since forever!" 🍦
    </p>
  </div>
</div>
