# My Medical Catalogue – setup
1. **Supabase**: create a project → SQL Editor → run `schema.sql`.
2. Authentication → Providers → enable **Google** (add Google OAuth client ID/secret). Authentication → URL Configuration → set Site URL and Redirect URLs to your Netlify URL.
3. Project Settings → API: copy **Project URL** and **anon key** into the top of `index.html` (`SB_URL`, `SB_KEY`). The anon key is safe in the browser; security comes from the row-level-security rules.
4. Replace `YOUR-DOMAIN.netlify.app` in `index.html`, `robots.txt`, `sitemap.xml`; replace the email in `privacy.html`.
5. Push to **GitHub** → Netlify → "Import from Git" (no build command, publish directory `/`).
6. Log in once with Google, then run: `update profiles set role='admin' where email='you@gmail.com';`
7. Admin panel (hidden): tap the logo 5 times, or open `yoursite/#admin`.
8. Share link + password (default `medical123`, change it in Admin → access). Install: browser menu → Add to Home screen.
