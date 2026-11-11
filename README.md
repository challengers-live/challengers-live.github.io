# Challenger Official Website

This repository contains the original Challenger HTML website prepared for GitHub Pages.

## Deploy
1. Upload all files and folders from this ZIP to the root of your GitHub repository.
2. Keep the repository's default branch as `main`.
3. Open **Settings → Pages** and set the build/deployment source to **GitHub Actions**.
4. The workflow in `.github/workflows/deploy-pages.yml` deploys the site on pushes to `main`.
5. Open the Pages URL shown in the repository's **Actions** deployment.

## Important
- The original website HTML is preserved; a favicon reference to `assets/challenger-logo.png` is added.
- The Supabase project/database is not included in this ZIP and is not recreated or reset.
- Keep the existing Netlify deployment active while testing the GitHub Pages copy.
- The existing Android Capacitor app currently points to `https://challengers-live.netlify.app`. It will continue using that URL until its Capacitor `server.url` is deliberately changed and a new APK is built.
- Before switching production traffic, test sign-in, signup, OTP/redirects, profiles, quizzes, uploads, and other app features on the GitHub Pages URL. Add the new Pages URL to Supabase Auth URL Configuration (Site URL/Redirect URLs as appropriate) while retaining the Netlify URLs during the transition.
- Never publish a Supabase `service_role` key. Frontend apps should use only the intended public/anon key with appropriate Row Level Security.
