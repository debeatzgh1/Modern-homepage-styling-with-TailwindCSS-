<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        :root {
            --gh-bg: #0d1117;
            --gh-border: #30363d;
            --hustle-accent: #238636;
            --text-gray: #8b949e;
        }

        /* 1. Slim Top Overlay Banner */
        .mini-hustle-card {
            position: fixed;
            top: 10px; /* Positioned at the top */
            left: 50%;
            transform: translateX(-50%);
            width: 90%;
            max-width: 450px; /* Narrower for a cleaner look */
            background: var(--gh-bg);
            border: 1px solid var(--gh-border);
            border-radius: 8px; /* Slightly sharper professional corners */
            padding: 10px 15px;
            cursor: pointer;
            box-shadow: 0 4px 20px rgba(0,0,0,0.6);
            z-index: 1000;
            overflow: hidden;
            display: flex;
            align-items: center;
            gap: 12px;
            animation: borderPulse 4s infinite;
        }

        @keyframes borderPulse {
            0% { border-color: var(--gh-border); }
            50% { border-color: var(--hustle-accent); box-shadow: 0 0 10px rgba(35, 134, 54, 0.2); }
            100% { border-color: var(--gh-border); }
        }

        /* 2. Compact Auto-Slide Content */
        .slide-container {
            flex-grow: 1;
        }

        .slide-text {
            display: none;
            font-size: 0.8rem; /* Smaller font for top overlay */
            line-height: 1.2;
            color: white;
            animation: fadeSlide 0.5s ease;
        }

        .slide-text.active { display: block; }

        @keyframes fadeSlide {
            from { opacity: 0; transform: translateY(-5px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .hustle-tag {
            background: var(--hustle-accent);
            color: white;
            font-size: 0.65rem;
            font-weight: bold;
            padding: 2px 6px;
            border-radius: 4px;
            text-transform: uppercase;
            white-space: nowrap;
        }

        /* 3. Full-Screen Iframe Overlay */
        #iframe-overlay {
            position: fixed;
            top: 0; left: 0; 
            width: 100%; height: 100%;
            background: rgba(0,0,0,0.9);
            display: none;
            justify-content: center;
            align-items: center;
            z-index: 9999;
            backdrop-filter: blur(8px);
        }

        .iframe-container {
            width: 95%; /* Wider for GitHub Page tools */
            max-width: 1200px;
            height: 90vh;
            background: #ffffff;
            border-radius: 12px;
            position: relative;
            overflow: hidden;
            box-shadow: 0 0 50px rgba(0,0,0,0.5);
        }

        .close-iframe {
            position: absolute;
            top: 10px;
            right: 15px;
            background: #f85149;
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 5px;
            cursor: pointer;
            z-index: 10001;
            font-weight: bold;
            font-size: 0.8rem;
        }

        iframe {
            width: 100%;
            height: 100%;
            border: none;
        }
    </style>
</head>
<body>

    <div class="mini-hustle-card" onclick="openHustleKit()">
        <span class="hustle-tag">NEW</span>
        
        <div class="slide-container">
            <div class="slide-text active">
                <strong>Side Hustle Tools:</strong> Launch your digital business today.
            </div>
            
            <div class="slide-text">
                <strong>Entrepreneur Ideas:</strong> Thrive in the digital economy.
            </div>

            <div class="slide-text">
                <strong>One-Stop Place:</strong> Everything you need online.
            </div>
        </div>

        <span style="color: var(--text-gray); font-size: 1rem;">›</span>
    </div>

    <div id="iframe-overlay" onclick="closeHustleKit(event)">
        <div class="iframe-container" onclick="event.stopPropagation()">
            <button class="close-iframe" onclick="closeHustleKit(event)">CLOSE [X]</button>
            <iframe src="https://msha.ke/debeatzgh" title="Side Hustle Starter Kit"></iframe>
        </div>
    </div>

    <script>
        // Auto-Slide Logic
        let currentSlide = 0;
        const slides = document.querySelectorAll('.slide-text');
        
        function rotateSlides() {
            slides[currentSlide].classList.remove('active');
            currentSlide = (currentSlide + 1) % slides.length;
            slides[currentSlide].classList.add('active');
        }

        setInterval(rotateSlides, 3500); 

        // Iframe Open/Close Logic
        function openHustleKit() {
            document.getElementById('iframe-overlay').style.display = 'flex';
            document.body.style.overflow = 'hidden'; // Prevent background scroll
        }

        function closeHustleKit(event) {
            document.getElementById('iframe-overlay').style.display = 'none';
            document.body.style.overflow = 'auto'; // Restore scroll
        }
    </script>








<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DeBeatzGH - Dynamic Workspace Hub</title>
    <style>
        /* Modern Base Variables matching DeBeatzGH UI Ecosystem */
        :root {
            --bg-main: #060913;
            --bg-surface: rgba(15, 23, 42, 0.4);
            --border-glow: rgba(217, 70, 239, 0.15);
            --text-primary: #ffffff;
            --text-secondary: #94a3b8;
            --neon-pink: #d946ef;
            --neon-blue: #3b82f6;
            --font-stack: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
        }

        /* Smooth Reset and Global Rules */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            background-color: var(--bg-main);
            color: var(--text-primary);
            font-family: var(--font-stack);
            min-height: 100vh;
            overflow-x: hidden;
            line-height: 1.5;
            /* Subdued futuristic layout ambient background pattern */
            background-image: 
                radial-gradient(circle at 80% 20%, rgba(217, 70, 239, 0.08) 0%, transparent 40%),
                radial-gradient(circle at 10% 70%, rgba(59, 130, 246, 0.06) 0%, transparent 45%);
        }

        /* Container Layout */
        .page-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        /* Branding & Navigation Header */
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding-bottom: 60px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
        }

        .logo {
            font-size: 1.4rem;
            font-weight: 800;
            letter-spacing: -0.5px;
            background: linear-gradient(45deg, var(--neon-pink), var(--neon-blue));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .status-pill {
            background: rgba(59, 130, 246, 0.1);
            border: 1px solid rgba(59, 130, 246, 0.2);
            padding: 6px 14px;
            border-radius: 99px;
            font-size: 0.8rem;
            font-weight: 600;
            color: #60a5fa;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .status-dot {
            width: 8px;
            height: 8px;
            background-color: #3b82f6;
            border-radius: 50%;
            box-shadow: 0 0 8px #3b82f6;
        }

        /* Hero Content Structure */
        .hero {
            text-align: center;
            padding: 80px 0 60px 0;
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 3rem;
            font-weight: 900;
            letter-spacing: -1px;
            line-height: 1.15;
            margin-bottom: 20px;
            background: linear-gradient(to right, #ffffff, #94a3b8);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        @media (max-width: 768px) {
            .hero h1 { font-size: 2.25rem; }
        }

        .hero p {
            font-size: 1.1rem;
            color: var(--text-secondary);
            margin-bottom: 35px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        /* Call To Action Interaction Triggers */
        .cta-group {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--neon-pink) 0%, var(--neon-blue) 100%);
            color: white;
            border: none;
            padding: 14px 28px;
            font-size: 0.95rem;
            font-weight: 700;
            border-radius: 12px;
            cursor: pointer;
            text-decoration: none;
            box-shadow: 0 4px 20px rgba(217, 70, 239, 0.2);
            transition: all 0.25s ease;
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 24px rgba(217, 70, 239, 0.35);
            filter: brightness(1.05);
        }

        /* Features/Highlights Grid Layout */
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1xl));
            gap: 20px;
            margin-bottom: 80px;
            margin-top: 20px;
        }

        .feature-card {
            background: var(--bg-surface);
            border: 1px solid rgba(255, 255, 255, 0.04);
            border-radius: 18px;
            padding: 30px;
            backdrop-filter: blur(8px);
            transition: all 0.25s ease;
        }

        .feature-card:hover {
            border-color: var(--border-glow);
            transform: translateY(-2px);
            background: rgba(15, 23, 42, 0.6);
        }

        .feature-card h3 {
            font-size: 1.15rem;
            margin-bottom: 10px;
            font-weight: 700;
        }

        .feature-card p {
            color: var(--text-secondary);
            font-size: 0.9rem;
            line-height: 1.5;
        }

        /* Divider Segment Line */
        .section-divider {
            height: 1px;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.05) 50%, transparent);
            margin: 40px 0 80px 0;
        }

        /* Layout modifications to keep native styles safe within the host structure */
        #dbz-faq-hub {
            margin-top: 20px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
            border: 1px solid rgba(255, 255, 255, 0.02);
        }

        footer {
            text-align: center;
            color: rgba(148, 163, 184, 0.4);
            font-size: 0.8rem;
            margin-top: 100px;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.03);
        }
    </style>


    <div class="page-container">
        <!-- Site Header Navigation Context -->
        <header>
            <div class="logo">DEBEATZGH</div>
            <div class="status-pill">
                <span class="status-dot"></span>
                Ehub Hub Active
            </div>
        </header>

        <!-- Main Identity Showcase (Hero Section) -->
        <main class="hero">
            <h1>Next-Generation Creative & Digital Workspace Portals</h1>
            <p>Deploying lightweight automation blocks, production widgets, streaming modules, and asset kits tailored for active developers and digital web managers.</p>
            <div class="cta-group">
                <!-- Direct hook execution mimicking action parameters -->
                <button class="btn-primary" onclick="document.getElementById('dbz-btn').click();">
                    Launch Interactive App Hub
                </button>
            </div>
        </main>

        <!-- Spatial Feature Indexing Matrix Section -->
        <section class="features-grid">
            <div class="feature-card">
                <h3>Floating Workspace</h3>
                <p>Access your primary digital environments securely via our dedicated corner window interface system without shifting away from your running tab.</p>
            </div>
            <div class="feature-card">
                <h3>Lazy Architecture</h3>
                <p>Saves visual processing resources by compiling system memory structures exclusively when interaction parameters occur on screen.</p>
            </div>
            <div class="feature-card">
                <h3>Mobile Fluidity</h3>
                <p>Fully decoupled native multi-touch swipe mechanics handle item sorting gracefully across narrow physical panel layouts.</p>
            </div>
        </section>

        <div class="section-divider"></div>

        <!-- SCRIPT CONTAINER 2: Embed Object FAQ Interface Frame Insertion -->
        <div id="dbz-faq-hub">
            <style>
                #dbz-faq-hub {
                    --dbz-space-bg: #090d16;
                    --dbz-panel-bg: rgba(15, 23, 42, 0.65);
                    --dbz-card-border: rgba(255, 255, 255, 0.06);
                    --dbz-text-main: #f8fafc;
                    --dbz-text-muted: #94a3b8;
                    --dbz-accent-neon: #d946ef; /* Ehub / DeBeatzGH Accent Magenta */
                    --dbz-accent-blue: #3b82f6;
                    
                    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, sans-serif;
                    background: var(--dbz-space-bg);
                    color: var(--dbz-text-main);
                    padding: 40px 16px;
                    max-width: 768px;
                    margin: 0 auto;
                    border-radius: 24px;
                }

                #dbz-faq-hub h2 {
                    text-align: center;
                    font-size: 1.75rem;
                    font-weight: 900;
                    margin-bottom: 24px;
                    background: linear-gradient(45deg, var(--dbz-text-main), var(--dbz-text-muted));
                    -webkit-background-clip: text;
                    -webkit-text-fill-color: transparent;
                    letter-spacing: -0.5px;
                }

                /* Swipeable Mobile Category Bar */
                #dbz-faq-hub .category-slider {
                    display: flex;
                    gap: 10px;
                    overflow-x: auto;
                    scroll-snap-type: x mandatory;
                    scrollbar-width: none; /* Hide scrollbar for Firefox */
                    -webkit-overflow-scrolling: touch;
                    padding-bottom: 16px;
                    margin-bottom: 20px;
                    border-bottom: 1px solid var(--dbz-card-border);
                }

                #dbz-faq-hub .category-slider::-webkit-scrollbar {
                    display: none; /* Hide scrollbar for Chrome/Safari */
                }

                #dbz-faq-hub .cat-btn {
                    flex: 0 0 auto;
                    scroll-snap-align: start;
                    background: rgba(255, 255, 255, 0.03);
                    border: 1px solid var(--dbz-card-border);
                    color: var(--dbz-text-muted);
                    padding: 8px 18px;
                    border-radius: 20px;
                    font-size: 0.85rem;
                    font-weight: 600;
                    cursor: pointer;
                    transition: all 0.25s cubic-bezier(0.4, 0, 0.2, 1);
                }

                #dbz-faq-hub .cat-btn.active {
                    background: linear-gradient(135deg, var(--dbz-accent-neon) 0%, var(--dbz-accent-blue) 100%);
                    color: #ffffff;
                    border-color: transparent;
                    box-shadow: 0 4px 15px rgba(217, 70, 239, 0.25);
                }

                /* Lazy Load Accordion Layout */
                #dbz-faq-hub .faq-wrapper {
                    display: none;
                    flex-direction: column;
                    gap: 12px;
                }

                #dbz-faq-hub .faq-wrapper.active {
                    display: flex;
                    animation: dbzFadeIn 0.35s ease;
                }

                #dbz-faq-hub .faq-item {
                    background: var(--dbz-panel-bg);
                    border: 1px solid var(--dbz-card-border);
                    border-radius: 14px;
                    overflow: hidden;
                    transition: border-color 0.2s ease;
                }

                #dbz-faq-hub .faq-trigger {
                    width: 100%;
                    padding: 16px 20px;
                    text-align: left;
                    background: transparent;
                    border: none;
                    color: var(--dbz-text-main);
                    font-size: 0.95rem;
                    font-weight: 700;
                    cursor: pointer;
                    display: flex;
                    justify-content: space-between;
                    align-items: center;
                    gap: 15px;
                }

                #dbz-faq-hub .faq-icon {
                    font-size: 0.75rem;
                    color: var(--dbz-text-muted);
                    transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1);
                    flex-shrink: 0;
                }

                #dbz-faq-hub .faq-item.open {
                    border-color: rgba(217, 70, 239, 0.25);
                }

                #dbz-faq-hub .faq-item.open .faq-icon {
                    transform: rotate(180deg);
                    color: var(--dbz-accent-neon);
                }

                #dbz-faq-hub .faq-content {
                    max-height: 0;
                    overflow: hidden;
                    transition: max-height 0.3s cubic-bezier(0.4, 0, 0.2, 1);
                    background: rgba(0, 0, 0, 0.15);
                }

                #dbz-faq-hub .faq-content-inner {
                    padding: 16px 20px;
                    font-size: 0.88rem;
                    line-height: 1.5;
                    color: var(--dbz-text-muted);
                    border-top: 1px solid rgba(255, 255, 255, 0.02);
                }

                @keyframes dbzFadeIn {
                    from { opacity: 0; transform: translateY(6px); }
                    to { opacity: 1; transform: translateY(0); }
                }
            </style>

            <h2>Frequently Asked Questions</h2>

            <div class="category-slider" id="dbz-faq-cats">
                <button class="cat-btn active" onclick="switchFaqCategory('general')">General Portal</button>
                <button class="cat-btn" onclick="switchFaqCategory('ehub')">Ehub Streaming</button>
                <button class="cat-btn" onclick="switchFaqCategory('resources')">Creative Assets</button>
            </div>

            <div class="faq-wrapper active" id="faq-general">
                <div class="faq-item">
                    <button class="faq-trigger" onclick="toggleFaqAccordion(this, 'What is the DeBeatzGH workspace hub?')">
                        <span>What is the DeBeatzGH workspace hub?</span>
                        <span class="faq-icon">▼</span>
                    </button>
                    <div class="faq-content"><div class="faq-content-inner"></div></div>
                </div>
                <div class="faq-item">
                    <button class="faq-trigger" onclick="toggleFaqAccordion(this, 'How do I submit forms via GitHub pages safely?')">
                        <span>How do I submit forms via GitHub pages safely?</span>
                        <span class="faq-icon">▼</span>
                    </button>
                    <div class="faq-content"><div class="faq-content-inner"></div></div>
                </div>
            </div>

            <div class="faq-wrapper" id="faq-ehub">
                <div class="faq-item">
                    <button class="faq-trigger" onclick="toggleFaqAccordion(this, 'Where can I find the official music countdown charts?')">
                        <span>Where can I find the official music countdown charts?</span>
                        <span class="faq-icon">▼</span>
                    </button>
                    <div class="faq-content"><div class="faq-content-inner"></div></div>
                </div>
                <div class="faq-item">
                    <button class="faq-trigger" onclick="toggleFaqAccordion(this, 'Can I integrate the floating Ehub widget into my blog?')">
                        <span>Can I integrate the floating Ehub widget into my blog?</span>
                        <span class="faq-icon">▼</span>
                    </button>
                    <div class="faq-content"><div class="faq-content-inner"></div></div>
                </div>
            </div>

            <div class="faq-wrapper" id="faq-resources">
                <div class="faq-item">
                    <button class="faq-trigger" onclick="toggleFaqAccordion(this, 'Are the blogger templates free to modify?')">
                        <span>Are the blogger templates free to modify?</span>
                        <span class="faq-icon">▼</span>
                    </button>
                    <div class="faq-content"><div class="faq-content-inner"></div></div>
                </div>
            </div>

            <script>
                // Tab Switch Engine
                function switchFaqCategory(catId) {
                    document.querySelectorAll('#dbz-faq-hub .faq-wrapper').forEach(wrapper => {
                        wrapper.classList.remove('active');
                    });
                    document.querySelectorAll('#dbz-faq-hub .cat-btn').forEach(btn => {
                        btn.classList.remove('active');
                    });

                    document.getElementById(`faq-${catId}`).classList.add('active');
                    
                    const activeBtn = Array.from(document.querySelectorAll('#dbz-faq-hub .cat-btn')).find(btn => {
                        return btn.getAttribute('onclick').includes(catId);
                    });
                    if (activeBtn) {
                        activeBtn.classList.add('active');
                        activeBtn.scrollIntoView({ behavior: 'smooth', block: 'nearest', inline: 'center' });
                    }
                }

                // Lazy-Loading Accordion Logic Engine
                function toggleFaqAccordion(triggerElement, questionText) {
                    const faqItem = triggerElement.parentElement;
                    const contentPane = faqItem.querySelector('.faq-content');
                    const innerTextNode = faqItem.querySelector('.faq-content-inner');

                    if (!innerTextNode.innerHTML || innerTextNode.innerHTML.trim() === "") {
                        innerTextNode.innerHTML = fetchLazyFaqData(questionText);
                    }

                    const currentWrapper = faqItem.parentElement;
                    currentWrapper.querySelectorAll('.faq-item').forEach(item => {
                        if (item !== faqItem) {
                            item.classList.remove('open');
                            item.querySelector('.faq-content').style.maxHeight = null;
                        }
                    });

                    if (faqItem.classList.contains('open')) {
                        faqItem.classList.remove('open');
                        contentPane.style.maxHeight = null;
                    } else {
                        faqItem.classList.add('open');
                        contentPane.style.maxHeight = contentPane.scrollHeight + "px";
                    }
                }

                function fetchLazyFaqData(question) {
                    const dictionary = {
                        "What is the workspace hub?": "The DeBeatzGH workspace hub is a unified dashboard designed to catalog tools, widgets, entertainment pipelines, and custom API interfaces for creators, developers, and platform managers.",
                        "How do I submit forms via GitHub pages safely?": "Our system integrates lightweight sandboxed oembed environments. Your form fields render lazily inside designated sandboxes, bypassing raw infrastructure processing for maximum data compliance.",
                        "Where can I find the official music countdown charts?": "All digital entertainment updates are broadcast live inside the Ehub portal stream. Simply deploy the layout toggle widget or launch our system carousel overlays to view updated ranks.",
                        "Can I integrate the floating Ehub widget into my 






<!-- Floating Form Launcher and Modal -->

<style>

  /* Floating Launcher Button */

  #form-launcher {

    position: fixed;

    right: 10px;

    top: 10%;

    transform: translateY(-50%);

    z-index: 9999;

    background: #24292e;

    color: #fff;

    border: none;

    border-radius: 50%;

    width: 40px;

    height: 40px;

    box-shadow: 0 4px 16px rgba(36,41,46,0.16);

    display: flex;

    align-items: center;

    justify-content: center;

    cursor: pointer;

    font-size: 28px;

    transition: background 0.2s, box-shadow 0.2s;

  }

  #form-launcher:hover {

    background: #0366d6;

    box-shadow: 0 8px 32px rgba(36,41,46,0.24);

  }

  /* Modal Overlay */

  #form-modal-overlay {

    display: none;

    position: fixed;

    z-index: 10000;

    left: 0;

    top: 0;

    width: 80vw;

    height: 80vh;

    background: rgba(20, 20, 20, 0.68);

    align-items: center;

    justify-content: center;

  }

  /* Modal Content */

  #form-modal-content {

    background: #fff;

    border-radius: 12px;

    max-width: 78vw;

    width: 560px;

    max-height: 90vh;

    box-shadow: 0 8px 40px rgba(0,0,0,0.22);

    padding: 0;

    overflow: hidden;

    display: flex;

    flex-direction: column;

    position: relative;

    animation: modalShow 0.3s;

  }

  @keyframes modalShow {

    from { transform: scale(0.9); opacity: 0; }

    to   { transform: scale(1); opacity: 1; }

  }

  #form-modal-close {

    position: absolute;

    top: 6px;

    right: 16px;

    background: none;

    border: none;

    color: #222;

    font-size: 2rem;

    cursor: pointer;

    z-index: 10001;

    line-height: 1;

  }

  /* Responsive iframe */

  #form-modal-content iframe {

    width: 100%;

    min-height: 720px;

    border: none;

  }

  @media(max-width:700px){

    #form-modal-content { width: 98vw; border-radius: 4px; }

    #form-modal-content iframe { min-height: 90vh; }

  }

</style>

<!-- Floating Launcher Button -->

<button id="form-launcher" title="Request Design Service">

  <svg width="32" height="32" fill="none" viewbox="0 0 24 24"><rect width="24" height="24" rx="12" fill="#24292e"/><path d="M8 12h8M12 8v8" stroke="#fff" stroke-width="2" stroke-linecap="round"/></path></rect></svg>



<!-- Modal Overlay and Content -->

<div id="form-modal-overlay">

  <div id="form-modal-content">

    <button id="form-modal-close" title="Close">&times;</button>

    <iframe src="https://debeatzgh1.github.io/me-/" allowfullscreen></iframe>

  </div>

</div>

<script>

  // Floating Launcher Modal Logic

  var launcher = document.getElementById('form-launcher');

  var overlay  = document.getElementById('form-modal-overlay');

  var closeBtn = document.getElementById('form-modal-close');

  launcher.onclick = function() {

    overlay.style.display = 'flex';

    document.body.style.overflow = 'hidden'; // Prevent background scroll

  };

  closeBtn.onclick = function() {

    overlay.style.display = 'none';

    document.body.style.overflow = '';

  };

  // Close modal when clicking outside content

  overlay.onclick = function(e) {

    if (e.target === overlay) {

      overlay.style.display = 'none';

      document.body.style.overflow = '';

    }

  };

  // ESC key closes modal

  document.addEventListener('keydown', function(e){

    if(e.key === 'Escape'){

      overlay.style.display = 'none';

      document.body.style.overflow = '';

    }

  });

</script>
> This project showcases a modern homepage layout built entirely with **Tailwind CSS**. It features a responsive design, sticky navigation, dark mode support, a floating home button, and smooth animations – all optimized for blogs, digital portfolios, and landing pages.

<p align="center">
  <img src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/08/generateamobile-firstresponsivebloggertemplatewithcustomizablecolorsfontsandsections1576324612066211977.jpg" alt="Firebase Front-End Components Preview" width="600"/>
</p>



>
> 🎯 Perfect for:
>
> * Developers and designers seeking clean UI components
> * Personal branding pages
> * Starter templates for Tailwind CSS beginners
>
> 💡 Key Features:
>
> * 🌙 Automatic dark mode detection
> * 🧭 Sticky & collapsible navigation
> * 🎯 Floating "Home" button
> * 📱 Mobile-friendly and responsive layout
> * ⚡ Fast loading, zero JavaScript frameworks
>
> 🔗 [Live Preview on GitHub Pages](https://digimartgh.blogspot.com/p/sign-in-for-more_19.html)



# 🚀 AI Tools & Side Hustle Hub  

![DeBeatzGH Thumbnail](https://debeatzgh.wordpress.com/wp-content/uploads/2025/08/designamodernminimalisticdesignfeaturinganai-themedicon28likeabraincircuitorrobot29overlaidwithdebeatzghoraitoolshustles6089986211026037047.jpg)  

## 🌟 About  
Welcome to **[DeBeatzGH](https://debeatzgh.wordpress.com/)** — your go-to hub for **AI tools, side hustle strategies, blogging resources, and digital growth guides**.  

This platform is built to help **students, creators, startups, and professionals** unlock the power of AI, monetize their skills, and thrive in today’s digital economy.  

### ✨ What You’ll Find  
- 💡 Explore **AI prompts, tools, and hacks**  
- 📈 Discover **side hustle strategies & online income ideas**  
- ✍️ Access **blogging & digital business guides**  
- 🚀 Stay ahead with **regular updates and fresh insights**  

---

## 👉 Get Started  
🔥 **Start your journey today → [Visit DeBeatzGH](https://debeatzgh.wordpress.com/)**  

---

<!-- README: DebeatzGH  (HTML-friendly for GitHub) -->
<div align="center">
  <a href="https://www.socialcreator.com/debeatzgh" target="_blank" rel="noopener">
    <img
      src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/08/designadigitalproductse-commerceonlinedeals3545265155247625100.jpg"
      alt="DebeatzGH Digital Store"
      style="max-width:100%; border-radius:16px;"
    />
  </a>

  <h1 style="margin-top: 14px;">DebeatzGH </h1>
  <p style="max-width:780px;">
    Your hub for AI insights, tech tutorials, side-hustle playbooks, and productivity tools.
    Learn, build, and launch digital projects faster.
  </p>

  <!-- CTAs -->
  <p>
    <a href="https://www.socialcreator.com/debeatzgh" target="_blank" rel="noopener"
       style="display:inline-block; padding:10px 16px; margin:4px; border-radius:999px; text-decoration:none; font-weight:600; border:1px solid #2563eb;">
      🚀 View Live App
    </a>
    <a href="https://github.com/debeatzgh1/Personal-Portfolio-site-" target="_blank" rel="noopener"
       style="display:inline-block; padding:10px 16px; margin:4px; border-radius:999px; text-decoration:none; font-weight:600; border:1px solid #111827;">
      ⭐ Star this Repo
    </a>
  </p>
</div>

<hr/>

<h2>Overview</h2>
<p>
  <strong>DebeatzGH</strong> helps beginners and creators build profitable digital assets:
  blogs, affiliate funnels, AI-assisted content, and more. Explore tutorials, tools, and
  ready-to-use components to speed up your workflow.
</p>

<h2>Features</h2>
<ul>
  <li><strong>AI & Tech Learning:</strong> Bite-sized guides for modern tools and workflows.</li>
  <li><strong>Side-Hustle Playbooks:</strong> Practical steps to validate and launch ideas.</li>
  <li><strong>Productivity Toolkit:</strong> Reusable widgets, templates, and scripts.</li>
  <li><strong>Beginner-Friendly:</strong> Clear explanations, curated resources, and examples.</li>
</ul>

<h2>Quick Start</h2>
<ol>
  <li>Clone:
    <pre><code>git clone https://github.com/debeatzgh1/Personal-Portfolio-site-</code></pre>
  </li>
  <li>Enter folder:
    <pre><code>cd debeatzgh</code></pre>
  </li>
  <li>Install deps (adjust to your stack):
    <pre><code># Node
npm install
npm run dev

# or Python
pip install -r requirements.txt
python app.py</code></pre>
  </li>
  <li>Open in browser:
    <pre><code>http://localhost:3000</code></pre>
  </li>
</ol>

<h2>Project Links</h2>
<ul>
  <li>🌐 Live App: <a href="https://www.socialcreator.com/debeatzgh" target="_blank" rel="noopener">socialcreator.com/debeatzgh</a></li>
  <li>🖼️ Thumbnail: <a href="https://debeatzgh.wordpress.com/wp-content/uploads/2025/08/designadigitalproductse-commerceonlinedeals3545265155247625100.jpg" target="_blank" rel="noopener">View image</a></li>
</ul>

<h2>Contributing</h2>
<p>
  Contributions are welcome! Open an issue for bugs or ideas. For changes, fork the repo,
  create a feature branch, and submit a pull request.
</p>

<h2>License</h2>
<p>
  Released under the <a href="./LICENSE">MIT License</a>.
</p>

<hr/>

<div align="center">
  <p><em>If this project helps you, consider giving it a star. It really helps! ⭐</em></p>
  <p>
    <a href="https://www.socialcreator.com/debeatzgh" target="_blank" rel="noopener"
       style="display:inline-block; padding:10px 16px; margin-top:6px; border-radius:10px; text-decoration:none; font-weight:600; border:1px solid #2563eb;">
      Open  Now →
    </a>
  </p>
</div>
