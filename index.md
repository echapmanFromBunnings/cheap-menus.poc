---
layout: default
title: "Groovy Scoops - Welcome to the Coolest Ice Cream Parlor"
---

<style>
  body {
    background: linear-gradient(135deg, #FF1493 0%, #00CED1 25%, #FFD700 50%, #9370DB 75%, #FF69B4 100%);
    background-size: 400% 400%;
    animation: groovyGradient 15s ease infinite;
    font-family: 'Courier New', monospace;
    color: #2C1810;
    margin: 0;
    padding: 20px;
    min-height: 100vh;
  }
  
  @keyframes groovyGradient {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
  }
  
  .container {
    max-width: 1000px;
    margin: 0 auto;
    background: #FFF5E6;
    border: 10px solid #FF1493;
    border-radius: 40px;
    padding: 50px;
    box-shadow: 0 30px 80px rgba(0, 0, 0, 0.4);
    text-align: center;
  }
  
  h1 {
    font-size: 4.5em;
    color: #FF1493;
    text-shadow: 4px 4px 0px #00CED1, 8px 8px 0px #FFD700, 12px 12px 0px #9370DB;
    margin-bottom: 20px;
    font-family: 'Impact', fantasy;
    letter-spacing: 5px;
    animation: float 3s ease-in-out infinite;
  }
  
  @keyframes float {
    0%, 100% { transform: translateY(0px); }
    50% { transform: translateY(-10px); }
  }
  
  .tagline {
    font-size: 2em;
    color: #00CED1;
    margin-bottom: 30px;
    font-style: italic;
    text-shadow: 2px 2px 0px #FFD700;
  }
  
  .welcome-text {
    font-size: 1.4em;
    line-height: 1.8;
    margin: 30px 0;
    color: #2C1810;
    padding: 20px;
    background: rgba(255, 255, 255, 0.7);
    border-radius: 15px;
    border: 3px dashed #00CED1;
  }
  
  .features {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    margin: 40px 0;
  }
  
  .feature-box {
    background: white;
    border: 4px solid #FFD700;
    border-radius: 15px;
    padding: 20px;
    box-shadow: 5px 5px 0px #FF69B4;
    transition: transform 0.3s ease;
  }
  
  .feature-box:hover {
    transform: scale(1.1) rotate(2deg);
  }
  
  .feature-icon {
    font-size: 3em;
    margin-bottom: 10px;
  }
  
  .feature-text {
    font-size: 1.2em;
    color: #9370DB;
    font-weight: bold;
  }
  
  .menu-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 30px;
    margin: 50px 0;
  }
  
  .menu-card {
    background: white;
    border: 5px solid #00CED1;
    border-radius: 20px;
    padding: 30px 20px;
    box-shadow: 10px 10px 0px #9370DB;
    transition: all 0.3s ease;
    cursor: pointer;
    text-decoration: none;
    display: block;
  }
  
  .menu-card:hover {
    transform: scale(1.15) rotate(-3deg);
    box-shadow: 15px 15px 0px #FF1493;
  }
  
  .menu-number {
    font-size: 4em;
    color: #FFD700;
    font-weight: bold;
    text-shadow: 3px 3px 0px #FF1493;
    margin-bottom: 10px;
  }
  
  .menu-title {
    font-size: 1.3em;
    color: #00CED1;
    font-weight: bold;
    margin-bottom: 10px;
  }
  
  .menu-description {
    font-size: 0.95em;
    color: #2C1810;
    line-height: 1.4;
  }
  
  .cta-button {
    display: inline-block;
    background: linear-gradient(45deg, #FF1493, #FFD700);
    color: white;
    font-size: 1.5em;
    font-weight: bold;
    padding: 20px 40px;
    border-radius: 50px;
    text-decoration: none;
    margin: 30px 10px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
    transition: all 0.3s ease;
    border: 4px solid #00CED1;
  }
  
  .cta-button:hover {
    transform: scale(1.1) rotate(-2deg);
    box-shadow: 0 15px 40px rgba(0, 0, 0, 0.5);
  }
  
  .disco-ball {
    font-size: 5em;
    animation: spin 4s linear infinite;
    display: inline-block;
    margin: 20px;
  }
  
  @keyframes spin {
    from { transform: rotate(0deg); }
    to { transform: rotate(360deg); }
  }
  
  .footer {
    margin-top: 50px;
    padding-top: 30px;
    border-top: 4px dashed #FF1493;
    font-size: 1.1em;
    color: #9370DB;
    font-style: italic;
  }
</style>

<div class="container">
  <div class="disco-ball">✨</div>
  
  <h1>🍦 GROOVY SCOOPS 🍦</h1>
  
  <p class="tagline">The Far-Out Ice Cream Experience!</p>
  
  <div class="welcome-text">
    <strong>Welcome, cool cats and groovy kittens!</strong><br>
    Step into our psychedelic parlor where every scoop is a trip down memory lane and every flavor is totally outta sight! We're serving up the wildest, most far-out ice cream creations this side of the Summer of Love. Peace, love, and ice cream, baby! ✌️
  </div>
  
  <div class="features">
    <div class="feature-box">
      <div class="feature-icon">🌈</div>
      <div class="feature-text">20 Wild Flavors</div>
    </div>
    <div class="feature-box">
      <div class="feature-icon">🎨</div>
      <div class="feature-text">Retro Vibes</div>
    </div>
    <div class="feature-box">
      <div class="feature-icon">💎</div>
      <div class="feature-text">Premium Quality</div>
    </div>
    <div class="feature-box">
      <div class="feature-icon">🎪</div>
      <div class="feature-text">Groovy Experience</div>
    </div>
  </div>
  
  <h2 style="font-size: 2.5em; color: #FF1493; margin: 40px 0 30px 0; text-shadow: 2px 2px 0px #00CED1;">
    🎯 EXPLORE OUR MENU 🎯
  </h2>
  
  <div class="menu-grid">
    <a href="1.html" class="menu-card">
      <div class="menu-number">1</div>
      <div class="menu-title">Classic Retro Flavors</div>
      <div class="menu-description">
        Cosmic Bubblegum, Disco Inferno, Purple Haze & more far-out creations!
      </div>
    </a>
    
    <a href="2.html" class="menu-card">
      <div class="menu-number">2</div>
      <div class="menu-title">Totally Radical Flavors</div>
      <div class="menu-description">
        Tiki Paradise, Cotton Candy Chaos, Groovy Matcha & other boss treats!
      </div>
    </a>
    
    <a href="3.html" class="menu-card">
      <div class="menu-number">3</div>
      <div class="menu-title">Outta Sight Flavors</div>
      <div class="menu-description">
        Rose Garden Romance, Tie-Dye Berry, Earl Grey Explosion & more!
      </div>
    </a>
    
    <a href="4.html" class="menu-card">
      <div class="menu-number">4</div>
      <div class="menu-title">Ultimate Far Out Flavors</div>
      <div class="menu-description">
        Pretzel Crunch, Midnight Velvet, Birthday Cake Spectacular & beyond!
      </div>
    </a>
  </div>
  
  <div style="margin: 50px 0;">
    <a href="1.html" class="cta-button">🌟 START YOUR FLAVOR JOURNEY 🌟</a>
  </div>
  
  <div class="footer">
    <p>
      <strong>Hours:</strong> Open every groovy day from dawn till disco! 🌅🕺<br>
      <strong>Location:</strong> Where the good vibes are, man! 🚐💫<br>
      <strong>Motto:</strong> "Keep on scooping in the free world!" ✌️🍦
    </p>
  </div>
  
  <div class="disco-ball">🪩</div>
</div>
