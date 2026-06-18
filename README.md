


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
