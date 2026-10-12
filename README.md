🌿 Gratitude & Wellness Tracker
A privacy-first, client-side web application designed to cultivate daily gratitude while helping you stay on top of your medication schedule. Built with HTML5, Tailwind CSS, JavaScript, and Transformers.js for intelligent semantic duplicate detection.

❤️Made with love for my brother.

✨ Features
🙏 30-Day Anti-Repeat Gratitude Journal
Daily Reflections: Record three things you are grateful for each day.

🧠 AI-Powered Semantic Checking (Transformers.js): Uses a lightweight client-side embedding model (Xenova/all-MiniLM-L6-v2) running entirely in your browser. It checks new gratitude entries against your previous 30 days of entries to prevent accidental repetition of the same concepts (even with different wording).

Calendar & History View: Review your past gratitude entries and track your consistency over time.

💊 Medication Manager & Reminders
Schedule Management: Add medications with custom dosages, frequencies (Daily, Specific Days, Interval), and reminder times.

Browser Notifications: Receive timely browser notifications when it's time to take your medication.

Adherence Tracking: Check off medications as taken each day and review your adherence streak.

🔒 100% Privacy & Local Storage
No Server Required: All data (journal entries, medications, history) is stored securely in your browser's localStorage.

Complete Privacy: Your personal health data and reflections never leave your device or get sent to any external server.

🚀 Getting Started & Installation
Because this is a static single-page application, you can run it instantly without setting up a backend server or build pipeline.

Option 1: Run Locally
Clone or download this repository to your computer:

Bash
git clone https://github.com/zachncurry/mygratitude.git
Open the folder and double-click index.html to open it directly in your web browser. (Note: For full Transformers.js model downloading in some browsers, running a local static server like npx serve or the VS Code Live Server extension is recommended).

Option 2: Deploy to GitHub Pages (Free Hosting)
Upload your index.html file to your GitHub repository (e.g., in the main branch).
Go to your repository on GitHub and click on Settings.
In the left sidebar, click on Pages.
Under Build and deployment, select Deploy from a branch.
Choose your main branch (or root directory) and click Save.
Within a minute, GitHub will provide a live URL where your app is hosted!

🛠️ Tech Stack
Frontend UI: HTML5, Tailwind CSS (via CDN), FontAwesome icons.
AI / NLP: Transformers.js running Xenova/all-MiniLM-L6-v2 locally in WebAssembly / Web Workers.
Data Persistence: HTML5 localStorage.
Notifications: Browser Notification API & Web Audio API (for optional alert sounds).

💡 How the AI Duplicate Check Works
When you enter a gratitude item, Transformers.js generates a numerical vector embedding of your sentence in your browser. The app compares the cosine similarity of your new entry against all active entries from the past 30 days. If a similarity threshold is crossed (indicating you're repeating a very similar thought or blessing), the app gently prompts you to think of something new to expand your mindfulness practice!

📄 License
This project is open-source and available under the MIT License.
