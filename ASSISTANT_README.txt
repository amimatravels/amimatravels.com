
AmimaTravels - Updated by assistant
=================================

What I changed:
- Added SEO meta tags and Organization schema (JSON-LD) to every HTML page.
- Injected a reusable header/navbar and a Login/Sign up modal on all pages.
- Created /scripts/auth.js which posts form data to Formspree (configure FORM_ENDPOINT inside that file) and falls back to localStorage if offline.
- Added a /blog/ folder with index.html and a sample post (sample-post.html). Use GitHub to add more posts or copy the template.
- Each page includes canonical link tags and basic meta descriptions. Edit per page as needed for better SEO.

Next steps (configure these after pulling updated site to GitHub):
1. Formspree: create a free form at https://formspree.io and replace the placeholder FORM_ENDPOINT in /scripts/auth.js with your form URL.
2. Email delivery: Formspree will send submissions to your email. Alternatively, configure Zapier or a webhook to write leads to Google Sheets.
3. Publishing posts: Add new HTML files to /blog or use a static site generator. If you want CMS-like editing, consider Netlify CMS or Forestry.io for Git-backed editing.
4. For user accounts (advanced): current modal is a lead capture. Implementing real auth requires a backend (e.g., Firebase Auth) and database; I can add that next if you'd like.

Deployment notes:
- The site is static (GitHub Pages). After replacing files in your repo, push to GitHub. Cloudflare will serve your domain via the CNAME file present in the repo.
- If you want posts to appear on the homepage, we can add a simple JavaScript script to read /blog/index.json or scan the /blog folder and list posts dynamically.

Files added/changed:
- /scripts/auth.js (new)
- /blog/index.html (new)
- /blog/sample-post.html (new)
- many .html files updated with meta and header injection
