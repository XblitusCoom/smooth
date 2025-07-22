<html lang="en">
 <head>
  <meta charset="utf-8"/>
  <meta content="width=device-width, initial-scale=1" name="viewport"/>
  <title>
   JavaScript Encrypt &amp; Decrypt Tool
  </title>
  <script src="https://cdn.tailwindcss.com">
  </script>
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" rel="stylesheet"/>
  <link href="https://fonts.googleapis.com/css2?family=Fira+Code&amp;family=Inter:wght@400;600&amp;display=swap" rel="stylesheet"/>
  <style>
   body {
      font-family: 'Inter', sans-serif;
      background-color: #0f172a;
      color: #e0e7ff;
    }
    textarea {
      font-family: 'Fira Code', monospace;
    }
    /* Modal backdrop */
    #about-modal {
      background-color: rgba(15, 23, 42, 0.85);
      backdrop-filter: blur(6px);
    }
  </style>
 </head>
 <body class="min-h-screen flex flex-col">
  <header class="bg-gradient-to-r from-indigo-900 via-purple-900 to-pink-900 shadow-lg">
   <div class="container mx-auto px-6 py-5 flex items-center justify-between">
    <div class="flex items-center space-x-3">
     <img alt="Purple square with white JS letters representing JavaScript logo" class="rounded-md" height="40" src="https://storage.googleapis.com/a1aa/image/36c1bc08-b305-4a73-3b8d-635875a330af.jpg" width="40"/>
     <h1 class="text-2xl font-semibold tracking-wide text-white select-none">
      JS Encrypt &amp; Decrypt
     </h1>
    </div>
    <nav class="hidden md:flex space-x-8 text-indigo-300 font-medium">
     <a class="hover:text-white transition" href="#encrypt">
      Encrypt
     </a>
     <a class="hover:text-white transition" href="#decrypt">
      Decrypt
     </a>
     <a class="hover:text-white transition" href="#about">
      About
     </a>
    </nav>
    <button aria-label="Toggle menu" class="md:hidden text-indigo-300 hover:text-white focus:outline-none" id="menu-btn">
     <i class="fas fa-bars fa-lg">
     </i>
    </button>
   </div>
   <nav class="hidden bg-indigo-900 text-indigo-300 px-6 py-4 space-y-3 md:hidden" id="mobile-menu">
    <a class="block hover:text-white transition" href="#encrypt">
     Encrypt
    </a>
    <a class="block hover:text-white transition" href="#decrypt">
     Decrypt
    </a>
    <a class="block hover:text-white transition" href="#about">
     About
    </a>
   </nav>
  </header>
  <main class="flex-grow container mx-auto px-6 py-10 max-w-5xl">
   <section class="mb-16" id="encrypt">
    <h2 class="text-3xl font-semibold mb-6 text-indigo-300 flex items-center space-x-3">
     <i class="fas fa-lock fa-lg">
     </i>
     <span>
      Encrypt JavaScript
     </span>
    </h2>
    <label class="block mb-2 font-semibold text-indigo-200" for="encrypt-input">
     Enter your JavaScript code:
    </label>
    <textarea class="w-full rounded-lg bg-indigo-800 text-indigo-100 p-4 resize-y border border-indigo-700 focus:outline-none focus:ring-2 focus:ring-purple-500" id="encrypt-input" placeholder="Paste your JavaScript code here..." rows="10"></textarea>
    <label class="block mt-6 mb-2 font-semibold text-indigo-200" for="encrypt-key">
     Encryption Key (any text):
    </label>
    <input class="w-full rounded-lg bg-indigo-800 text-indigo-100 p-3 border border-indigo-700 focus:outline-none focus:ring-2 focus:ring-purple-500" id="encrypt-key" placeholder="Enter encryption key" type="text"/>
    <button class="mt-6 bg-purple-600 hover:bg-purple-700 text-white font-semibold py-3 px-6 rounded-lg shadow-lg transition flex items-center space-x-2" id="encrypt-btn">
     <i class="fas fa-lock">
     </i>
     <span>
      Encrypt
     </span>
    </button>
    <label class="block mt-8 mb-2 font-semibold text-indigo-200" for="encrypt-output">
     Encrypted Output:
    </label>
    <textarea class="w-full rounded-lg bg-indigo-900 text-indigo-300 p-4 resize-y border border-indigo-700" id="encrypt-output" readonly="" rows="10"></textarea>
   </section>
   <section class="mb-16" id="decrypt">
    <h2 class="text-3xl font-semibold mb-6 text-indigo-300 flex items-center space-x-3">
     <i class="fas fa-unlock fa-lg">
     </i>
     <span>
      Decrypt JavaScript
     </span>
    </h2>
    <label class="block mb-2 font-semibold text-indigo-200" for="decrypt-input">
     Enter encrypted JavaScript code:
    </label>
    <textarea class="w-full rounded-lg bg-indigo-800 text-indigo-100 p-4 resize-y border border-indigo-700 focus:outline-none focus:ring-2 focus:ring-purple-500" id="decrypt-input" placeholder="Paste your encrypted JavaScript code here..." rows="10"></textarea>
    <label class="block mt-6 mb-2 font-semibold text-indigo-200" for="decrypt-key">
     Decryption Key (must match encryption key):
    </label>
    <input class="w-full rounded-lg bg-indigo-800 text-indigo-100 p-3 border border-indigo-700 focus:outline-none focus:ring-2 focus:ring-purple-500" id="decrypt-key" placeholder="Enter decryption key" type="text"/>
    <button class="mt-6 bg-purple-600 hover:bg-purple-700 text-white font-semibold py-3 px-6 rounded-lg shadow-lg transition flex items-center space-x-2" id="decrypt-btn">
     <i class="fas fa-unlock">
     </i>
     <span>
      Decrypt
     </span>
    </button>
    <label class="block mt-8 mb-2 font-semibold text-indigo-200" for="decrypt-output">
     Decrypted Output:
    </label>
    <textarea class="w-full rounded-lg bg-indigo-900 text-indigo-300 p-4 resize-y border border-indigo-700" id="decrypt-output" readonly="" rows="10"></textarea>
   </section>
   <section class="mb-16" id="about">
    <h2 class="text-3xl font-semibold mb-6 text-indigo-300 flex items-center space-x-3">
     <i class="fas fa-info-circle fa-lg">
     </i>
     <span>
      About Development
     </span>
    </h2>
    <p class="text-indigo-200 leading-relaxed max-w-3xl">
     This tool was created by 𝗦𝗺𝗼𝗼𝘁𝗵 𝗟𝗼𝗰𝗮𝘁𝗶𝗼𝗻 2025, with the 𝗨𝗦 𝗟𝗼𝗰𝗮𝘁𝗶𝗼𝗻 team, on telegram channel https://t.me/modapkstoapks, thank you to those of you who have supported me until now.
    </p>
    <img alt="Abstract digital illustration showing encryption and decryption concept with locks, keys, and JavaScript code snippets in purple and blue tones" class="mt-8 rounded-lg shadow-lg w-full max-w-3xl mx-auto" height="300" src="https://storage.googleapis.com/a1aa/image/23d0810f-2821-4aa1-f120-489c56835309.jpg" width="600"/>
   </section>
  </main>
  <footer class="bg-gradient-to-r from-indigo-900 via-purple-900 to-pink-900 text-indigo-300 py-6 text-center select-none">
   <p>
    © 2025 Copyright By Smooth Location
    <a class="hover:text-white underline" href="https://t.me/XBhigh" rel="noopener" target="_blank">
     Telegram
    </a>
   </p>
  </footer>

  <!-- About Modal -->
  <div aria-hidden="true" class="fixed inset-0 flex items-center justify-center z-50 hidden" id="about-modal" role="dialog" aria-modal="true" aria-labelledby="about-modal-title" aria-describedby="about-modal-desc">
   <div class="bg-indigo-900 rounded-lg shadow-xl max-w-md w-full mx-4 p-6 transform transition-transform duration-500 ease-in-out scale-90 opacity-0" id="about-modal-content" tabindex="-1">
    <h3 class="text-2xl font-semibold text-indigo-300 mb-4 text-center" id="about-modal-title">
     Smooth Location
    </h3>
    <p class="text-indigo-200 text-center mb-6" id="about-modal-desc">
     This tool was created by 𝗦𝗺𝗼𝗼𝘁𝗵 𝗟𝗼𝗰𝗮𝘁𝗶𝗼𝗻 2025, with the 𝗨𝗦 𝗟𝗼𝗰𝗮𝘁𝗶𝗼𝗻 team, on telegram channel https://t.me/modapkstoapks, thank you to those of you who have supported me until now.
    </p>
    <div class="flex justify-center">
     <button aria-label="Close about modal" class="bg-purple-600 hover:bg-purple-700 text-white font-semibold py-2 px-6 rounded-lg shadow-lg transition" id="about-modal-close">
      Close
     </button>
    </div>
   </div>
  </div>

  <script>
   // Mobile menu toggle
    const menuBtn = document.getElementById('menu-btn');
    const mobileMenu = document.getElementById('mobile-menu');
    menuBtn.addEventListener('click', () => {
      mobileMenu.classList.toggle('hidden');
    });

    // Simple XOR cipher for encryption/decryption
    function xorCipher(input, key) {
      const inputChars = Array.from(input);
      const keyChars = Array.from(key);
      let output = '';
      for (let i = 0; i < inputChars.length; i++) {
        const inputCode = inputChars[i].charCodeAt(0);
        const keyCode = keyChars[i % keyChars.length].charCodeAt(0);
        output += String.fromCharCode(inputCode ^ keyCode);
      }
      return output;
    }

    // Base64 encode/decode helpers for Unicode strings
    function base64Encode(str) {
      return btoa(unescape(encodeURIComponent(str)));
    }
    function base64Decode(str) {
      try {
        return decodeURIComponent(escape(atob(str)));
      } catch {
        return null;
      }
    }

    // Encrypt button handler
    const encryptBtn = document.getElementById('encrypt-btn');
    const encryptInput = document.getElementById('encrypt-input');
    const encryptKey = document.getElementById('encrypt-key');
    const encryptOutput = document.getElementById('encrypt-output');

    encryptBtn.addEventListener('click', () => {
      const code = encryptInput.value.trim();
      const key = encryptKey.value;
      if (!code) {
        alert('Please enter JavaScript code to encrypt.');
        return;
      }
      if (!key) {
        alert('Please enter an encryption key.');
        return;
      }
      const xored = xorCipher(code, key);
      const encoded = base64Encode(xored);
      encryptOutput.value = encoded;
    });

    // Decrypt button handler
    const decryptBtn = document.getElementById('decrypt-btn');
    const decryptInput = document.getElementById('decrypt-input');
    const decryptKey = document.getElementById('decrypt-key');
    const decryptOutput = document.getElementById('decrypt-output');

    decryptBtn.addEventListener('click', () => {
      const encrypted = decryptInput.value.trim();
      const key = decryptKey.value;
      if (!encrypted) {
        alert('Please enter encrypted JavaScript code to decrypt.');
        return;
      }
      if (!key) {
        alert('Please enter a decryption key.');
        return;
      }
      const decoded = base64Decode(encrypted);
      if (decoded === null) {
        alert('Invalid encrypted input. Please check your input.');
        return;
      }
      const decrypted = xorCipher(decoded, key);
      decryptOutput.value = decrypted;
    });

    // Modal logic
    const aboutModal = document.getElementById('about-modal');
    const aboutModalContent = document.getElementById('about-modal-content');
    const aboutModalClose = document.getElementById('about-modal-close');

    function openModal() {
      aboutModal.classList.remove('hidden');
      // Animate modal scale and opacity
      setTimeout(() => {
        aboutModalContent.style.transform = 'scale(1)';
        aboutModalContent.style.opacity = '1';
      }, 10);
      // Trap focus inside modal
      aboutModalContent.focus();
    }

    function closeModal() {
      aboutModalContent.style.transform = 'scale(0.9)';
      aboutModalContent.style.opacity = '0';
      setTimeout(() => {
        aboutModal.classList.add('hidden');
      }, 300);
    }

    aboutModalClose.addEventListener('click', closeModal);

    // Close modal on backdrop click
    aboutModal.addEventListener('click', (e) => {
      if (e.target === aboutModal) {
        closeModal();
      }
    });

    // Close modal on Escape key
    document.addEventListener('keydown', (e) => {
      if (e.key === 'Escape' && !aboutModal.classList.contains('hidden')) {
        closeModal();
      }
    });

    // Open modal on page load with smooth animation
    window.addEventListener('load', () => {
      openModal();
    });
  </script>
 </body>
</html>
