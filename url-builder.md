---
layout: default
title: "The Gelato & Icecream Factory - URL Builder"
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
    width: 100%;
    max-width: 1400px;
    margin: 0 auto;
  }
  
  .page-title {
    text-align: center;
    font-size: 3.5em;
    color: #C85A7A;
    margin: 30px 0 20px 0;
    font-style: italic;
    text-shadow: 2px 2px 0px #D4A574;
  }
  
  .subtitle {
    text-align: center;
    font-size: 1.6em;
    color: #4A1F1F;
    margin-bottom: 40px;
    line-height: 1.6;
  }
  
  .builder-section {
    background: white;
    border: 5px solid #C85A7A;
    border-radius: 20px;
    padding: 35px;
    margin: 30px 0;
    box-shadow: 8px 8px 0px #D4A574;
  }
  
  .section-header {
    font-size: 2.2em;
    color: #4A1F1F;
    margin-bottom: 25px;
    font-weight: bold;
    border-bottom: 3px solid #D4A574;
    padding-bottom: 12px;
  }
  
  .form-group {
    margin-bottom: 30px;
  }
  
  .form-label {
    display: block;
    font-size: 1.4em;
    color: #4A1F1F;
    margin-bottom: 12px;
    font-weight: bold;
  }
  
  .checkbox-group {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 15px;
    margin-top: 12px;
  }
  
  .checkbox-item {
    display: flex;
    align-items: center;
    background: #FFF5E6;
    padding: 15px;
    border: 3px solid #D4A574;
    border-radius: 10px;
    cursor: pointer;
    transition: all 0.3s ease;
  }
  
  .checkbox-item:hover {
    background: #FFE8E8;
    transform: scale(1.02);
  }
  
  .checkbox-item input[type="checkbox"] {
    width: 24px;
    height: 24px;
    margin-right: 12px;
    cursor: pointer;
    accent-color: #C85A7A;
  }
  
  .checkbox-item input[type="radio"] {
    width: 24px;
    height: 24px;
    margin-right: 12px;
    cursor: pointer;
    accent-color: #C85A7A;
  }
  
  .checkbox-item label {
    font-size: 1.3em;
    cursor: pointer;
    flex: 1;
  }
  
  .timing-controls {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 20px;
    margin-top: 15px;
  }
  
  .timing-item {
    background: #FFF5E6;
    padding: 20px;
    border: 3px solid #D4A574;
    border-radius: 12px;
    transition: all 0.3s ease;
  }
  
  .timing-item.disabled {
    opacity: 0.4;
    pointer-events: none;
    background: #f0f0f0;
  }
  
  .timing-header {
    font-size: 1.4em;
    font-weight: bold;
    color: #4A1F1F;
    margin-bottom: 12px;
  }
  
  .slider-container {
    margin-top: 10px;
  }
  
  input[type="range"] {
    width: 100%;
    height: 8px;
    border-radius: 5px;
    background: #D4A574;
    outline: none;
    -webkit-appearance: none;
    margin: 10px 0;
  }
  
  input[type="range"]::-webkit-slider-thumb {
    -webkit-appearance: none;
    appearance: none;
    width: 24px;
    height: 24px;
    border-radius: 50%;
    background: #C85A7A;
    cursor: pointer;
    border: 3px solid #4A1F1F;
  }
  
  input[type="range"]::-moz-range-thumb {
    width: 24px;
    height: 24px;
    border-radius: 50%;
    background: #C85A7A;
    cursor: pointer;
    border: 3px solid #4A1F1F;
  }
  
  .slider-value {
    font-size: 1.6em;
    color: #C85A7A;
    font-weight: bold;
    text-align: center;
    margin-top: 8px;
  }
  
  .toggle-switch {
    display: flex;
    align-items: center;
    gap: 15px;
  }
  
  .switch {
    position: relative;
    display: inline-block;
    width: 70px;
    height: 36px;
  }
  
  .switch input {
    opacity: 0;
    width: 0;
    height: 0;
  }
  
  .slider {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: #D4A574;
    transition: .4s;
    border-radius: 34px;
    border: 3px solid #4A1F1F;
  }
  
  .slider:before {
    position: absolute;
    content: "";
    height: 22px;
    width: 22px;
    left: 4px;
    bottom: 4px;
    background-color: white;
    transition: .4s;
    border-radius: 50%;
  }
  
  input:checked + .slider {
    background-color: #C85A7A;
  }
  
  input:checked + .slider:before {
    transform: translateX(34px);
  }
  
  .url-preview {
    background: #4A1F1F;
    color: #FFE8E8;
    padding: 25px;
    border-radius: 12px;
    font-family: 'Courier New', monospace;
    font-size: 1.2em;
    word-break: break-all;
    line-height: 1.8;
    margin-top: 20px;
    border: 4px solid #D4A574;
  }
  
  .action-buttons {
    display: flex;
    gap: 20px;
    margin-top: 30px;
    flex-wrap: wrap;
    justify-content: center;
  }
  
  .action-btn {
    background: linear-gradient(45deg, #C85A7A, #D4A574);
    color: white;
    font-size: 1.6em;
    font-weight: bold;
    padding: 20px 40px;
    border-radius: 15px;
    border: 4px solid #4A1F1F;
    cursor: pointer;
    transition: all 0.3s ease;
    text-decoration: none;
    display: inline-block;
    box-shadow: 5px 5px 0px #4A1F1F;
  }
  
  .action-btn:hover {
    transform: scale(1.05) rotate(-1deg);
    box-shadow: 7px 7px 0px #4A1F1F;
  }
  
  .action-btn:active {
    transform: scale(0.98);
  }
  
  .action-btn.secondary {
    background: #D4A574;
  }
  
  .nav-links {
    text-align: center;
    margin: 40px 0;
    padding: 30px 0;
    border-top: 5px solid #C85A7A;
  }
  
  .nav-links a {
    color: white;
    text-decoration: none;
    margin: 8px;
    font-weight: bold;
    padding: 18px 30px;
    background: #C85A7A;
    border-radius: 12px;
    display: inline-block;
    border: 4px solid #4A1F1F;
    font-size: 1.4em;
  }
  
  .nav-links a:hover {
    background: #D4A574;
    color: #4A1F1F;
  }
  
  .help-text {
    font-size: 1.2em;
    color: #666;
    margin-top: 10px;
    font-style: italic;
  }
  
  .copy-feedback {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) scale(0);
    background: #C85A7A;
    color: white;
    padding: 30px 50px;
    border-radius: 20px;
    font-size: 2em;
    font-weight: bold;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
    z-index: 1000;
    transition: transform 0.3s ease;
    border: 5px solid #4A1F1F;
  }
  
  .copy-feedback.show {
    transform: translate(-50%, -50%) scale(1);
  }
</style>

<div class="logo-header">
  <img src="{{ site.baseurl }}/logo.png" alt="The Gelato & Icecream Factory">
</div>

<div class="container">
  <h1 class="page-title">🔗 URL Builder 🔗</h1>
  <p class="subtitle">
    Build custom URLs for your menu slideshow! Configure timing, starting page, and display options!
  </p>
  
  <div class="builder-section">
    <h2 class="section-header">📋 Select Slides</h2>
    <div class="form-group">
      <label class="form-label">Which slides should be included in the slideshow?</label>
      <p class="help-text">Select one or more slides to include in your custom rotation</p>
      <div class="checkbox-group">
        <div class="checkbox-item">
          <input type="checkbox" id="include5" value="5" checked>
          <label for="include5">🖼️ Menu Image 1 (Page 5)</label>
        </div>
        <div class="checkbox-item">
          <input type="checkbox" id="include6" value="6" checked>
          <label for="include6">🖼️ Menu Image 2 (Page 6)</label>
        </div>
        <div class="checkbox-item">
          <input type="checkbox" id="include7" value="7" checked>
          <label for="include7">🖼️ Menu Image 3 (Page 7)</label>
        </div>
        <div class="checkbox-item">
          <input type="checkbox" id="include8" value="8" checked>
          <label for="include8">🖼️ Menu Image 4 (Page 8)</label>
        </div>
      </div>
    </div>
  </div>
  
  <div class="builder-section">
    <h2 class="section-header">⏱️ Timing Settings</h2>
    <div class="form-group">
      <label class="form-label">How long should each screen display? (in seconds)</label>
      <p class="help-text">Set individual timing for each selected slide</p>
      <div class="timing-controls">
        <div class="timing-item" id="timing5">
          <div class="timing-header">🖼️ Menu Image 1</div>
          <div class="slider-container">
            <input type="range" id="delay5" min="5" max="120" value="20" step="5">
            <div class="slider-value"><span id="value5">20</span> seconds</div>
          </div>
        </div>
        <div class="timing-item" id="timing6">
          <div class="timing-header">🖼️ Menu Image 2</div>
          <div class="slider-container">
            <input type="range" id="delay6" min="5" max="120" value="20" step="5">
            <div class="slider-value"><span id="value6">20</span> seconds</div>
          </div>
        </div>
        <div class="timing-item" id="timing7">
          <div class="timing-header">🖼️ Menu Image 3</div>
          <div class="slider-container">
            <input type="range" id="delay7" min="5" max="120" value="20" step="5">
            <div class="slider-value"><span id="value7">20</span> seconds</div>
          </div>
        </div>
        <div class="timing-item" id="timing8">
          <div class="timing-header">🖼️ Menu Image 4</div>
          <div class="slider-container">
            <input type="range" id="delay8" min="5" max="120" value="20" step="5">
            <div class="slider-value"><span id="value8">20</span> seconds</div>
          </div>
        </div>
      </div>
    </div>
  </div>
  
  <div class="builder-section">
    <h2 class="section-header">⚙️ Display Options</h2>
    
    <div class="form-group">
      <label class="form-label">Starting Screen</label>
      <p class="help-text">Choose which screen to show first</p>
      <div class="checkbox-group">
        <div class="checkbox-item">
          <input type="radio" name="startPage" id="start5" value="5" checked>
          <label for="start5">🖼️ Menu Image 1</label>
        </div>
        <div class="checkbox-item">
          <input type="radio" name="startPage" id="start6" value="6">
          <label for="start6">🖼️ Menu Image 2</label>
        </div>
        <div class="checkbox-item">
          <input type="radio" name="startPage" id="start7" value="7">
          <label for="start7">🖼️ Menu Image 3</label>
        </div>
        <div class="checkbox-item">
          <input type="radio" name="startPage" id="start8" value="8">
          <label for="start8">🖼️ Menu Image 4</label>
        </div>
      </div>
    </div>
    
    <div class="form-group">
      <label class="form-label">Image Rotation</label>
      <p class="help-text">Set the default rotation for all menu images</p>
      <div class="checkbox-group">
        <div class="checkbox-item">
          <input type="radio" name="rotation" id="rotate0" value="0" checked>
          <label for="rotate0">🔄 0° (Normal)</label>
        </div>
        <div class="checkbox-item">
          <input type="radio" name="rotation" id="rotate90" value="90">
          <label for="rotate90">🔄 90° (Clockwise)</label>
        </div>
        <div class="checkbox-item">
          <input type="radio" name="rotation" id="rotate180" value="180">
          <label for="rotate180">🔄 180° (Upside Down)</label>
        </div>
        <div class="checkbox-item">
          <input type="radio" name="rotation" id="rotate270" value="270">
          <label for="rotate270">🔄 270° (Counter-clockwise)</label>
        </div>
      </div>
    </div>
    
    <div class="form-group">
      <label class="form-label">Kiosk Mode</label>
      <p class="help-text">Hide all controls for a clean display (perfect for digital signage!)</p>
      <div class="toggle-switch">
        <label class="switch">
          <input type="checkbox" id="kioskMode">
          <span class="slider"></span>
        </label>
        <span id="kioskLabel" style="font-size: 1.4em; color: #4A1F1F;">Off</span>
      </div>
    </div>
  </div>
  
  <div class="builder-section">
    <h2 class="section-header">🔗 Your Custom URL</h2>
    <div class="url-preview" id="urlPreview">
      <!-- URL will be generated here -->
    </div>
    <div class="action-buttons">
      <button class="action-btn" id="copyBtn">📋 Copy URL</button>
      <a class="action-btn secondary" id="openBtn" href="#" target="_blank">🚀 Open URL</a>
    </div>
  </div>
  
  <div class="nav-links">
    <a href="{{ site.baseurl }}/index.html">🏠 Home</a>
    <a href="{{ site.baseurl }}/5.html">📺 Menu Images</a>
  </div>
</div>

<div class="copy-feedback" id="copyFeedback">
  ✅ URL Copied!
</div>

<script>
  // Get base URL
  const baseUrl = window.location.origin + '{{ site.baseurl }}';
  
  // Constants
  const FIRST_SLIDE = 5;
  const LAST_SLIDE = 8;
  const NUM_SLIDES = 4;
  
  // Get all form elements
  const includeCheckboxes = [
    document.getElementById('include5'),
    document.getElementById('include6'),
    document.getElementById('include7'),
    document.getElementById('include8')
  ];
  
  const timingItems = [
    document.getElementById('timing5'),
    document.getElementById('timing6'),
    document.getElementById('timing7'),
    document.getElementById('timing8')
  ];
  
  const delaySliders = [
    document.getElementById('delay5'),
    document.getElementById('delay6'),
    document.getElementById('delay7'),
    document.getElementById('delay8')
  ];
  
  const delayValues = [
    document.getElementById('value5'),
    document.getElementById('value6'),
    document.getElementById('value7'),
    document.getElementById('value8')
  ];
  
  const startPageRadios = [
    document.getElementById('start5'),
    document.getElementById('start6'),
    document.getElementById('start7'),
    document.getElementById('start8')
  ];
  
  const rotationRadios = [
    document.getElementById('rotate0'),
    document.getElementById('rotate90'),
    document.getElementById('rotate180'),
    document.getElementById('rotate270')
  ];
  
  const kioskMode = document.getElementById('kioskMode');
  const kioskLabel = document.getElementById('kioskLabel');
  const urlPreview = document.getElementById('urlPreview');
  const copyBtn = document.getElementById('copyBtn');
  const openBtn = document.getElementById('openBtn');
  const copyFeedback = document.getElementById('copyFeedback');
  
  // Update timing controls and start page options based on selection
  function updateControls() {
    const selectedSlides = [];
    
    includeCheckboxes.forEach((checkbox, index) => {
      const slideNum = FIRST_SLIDE + index;
      const isChecked = checkbox.checked;
      
      if (isChecked) {
        selectedSlides.push(slideNum);
      }
      
      // Enable/disable timing control
      if (timingItems[index]) {
        if (isChecked) {
          timingItems[index].classList.remove('disabled');
        } else {
          timingItems[index].classList.add('disabled');
        }
      }
      
      // Enable/disable start page radio
      if (startPageRadios[index]) {
        startPageRadios[index].disabled = !isChecked;
        const parentItem = startPageRadios[index].closest('.checkbox-item');
        if (parentItem) {
          if (isChecked) {
            parentItem.style.opacity = '1';
            parentItem.style.pointerEvents = 'auto';
          } else {
            parentItem.style.opacity = '0.4';
            parentItem.style.pointerEvents = 'none';
          }
        }
      }
    });
    
    // Ensure at least one slide is selected
    if (selectedSlides.length === 0) {
      // Prevent recursion by checking directly instead of calling updateControls again
      includeCheckboxes[0].checked = true;
      selectedSlides.push(FIRST_SLIDE);
      if (timingItems[0]) {
        timingItems[0].classList.remove('disabled');
      }
      if (startPageRadios[0]) {
        startPageRadios[0].disabled = false;
        const parentItem = startPageRadios[0].closest('.checkbox-item');
        if (parentItem) {
          parentItem.style.opacity = '1';
          parentItem.style.pointerEvents = 'auto';
        }
      }
    }
    
    // Make sure a selected slide is chosen as start page
    const currentStart = document.querySelector('input[name="startPage"]:checked');
    if (currentStart && currentStart.disabled) {
      // Find first enabled start page option
      const firstEnabled = startPageRadios.find(radio => !radio.disabled);
      if (firstEnabled) {
        firstEnabled.checked = true;
      }
    }
    
    updateUrl();
  }
  
  // Update slider value displays
  delaySliders.forEach((slider, index) => {
    slider.addEventListener('input', function() {
      delayValues[index].textContent = this.value;
      updateUrl();
    });
  });
  
  // Update kiosk label
  kioskMode.addEventListener('change', function() {
    kioskLabel.textContent = this.checked ? 'On' : 'Off';
    updateUrl();
  });
  
  // Update start page when radio changes
  startPageRadios.forEach(radio => {
    radio.addEventListener('change', updateUrl);
  });
  
  // Update rotation when radio changes
  rotationRadios.forEach(radio => {
    radio.addEventListener('change', updateUrl);
  });
  
  // Update when slide selection changes
  includeCheckboxes.forEach(checkbox => {
    checkbox.addEventListener('change', updateControls);
  });
  
  // Function to generate URL
  function updateUrl() {
    // Get starting page
    const startPage = parseInt(document.querySelector('input[name="startPage"]:checked').value);
    
    // Get rotation value
    const rotation = parseInt(document.querySelector('input[name="rotation"]:checked').value);
    
    // Build list of selected slides and their transition times
    const selectedSlides = [];
    const transitionTimes = [];
    
    includeCheckboxes.forEach((checkbox, index) => {
      if (checkbox.checked) {
        const slideNum = FIRST_SLIDE + index;
        selectedSlides.push(slideNum);
        transitionTimes.push(delaySliders[index].value);
      }
    });
    
    // Build URL
    const url = new URL(baseUrl + '/' + startPage + '.html');
    url.searchParams.set('slides', selectedSlides.join(','));
    url.searchParams.set('transition', transitionTimes.join(','));
    
    // Add rotation parameter if not 0
    if (rotation !== 0) {
      url.searchParams.set('rotation', rotation.toString());
    }
    
    if (kioskMode.checked) {
      url.searchParams.set('kiosk', 'true');
    }
    
    // Display URL
    urlPreview.textContent = url.toString();
    openBtn.href = url.toString();
  }
  
  // Copy to clipboard
  copyBtn.addEventListener('click', function() {
    const url = urlPreview.textContent;
    
    // Copy to clipboard
    navigator.clipboard.writeText(url).then(function() {
      // Show feedback
      copyFeedback.classList.add('show');
      setTimeout(function() {
        copyFeedback.classList.remove('show');
      }, 2000);
    }).catch(function(err) {
      console.error('Failed to copy:', err);
      // Fallback: create a text area and copy from it
      const textArea = document.createElement('textarea');
      textArea.value = url;
      textArea.style.position = 'fixed';
      textArea.style.left = '-999999px';
      document.body.appendChild(textArea);
      textArea.select();
      try {
        document.execCommand('copy');
        copyFeedback.classList.add('show');
        setTimeout(function() {
          copyFeedback.classList.remove('show');
        }, 2000);
      } catch (err) {
        console.error('Fallback copy failed:', err);
      }
      document.body.removeChild(textArea);
    });
  });
  
  // Initialize
  updateControls();
</script>
