# Trackingo Pro — Live Bus Tracker (Vignesh TAT • ZK3M8T)

## Overview
A self-contained, responsive web application for tracking Bitla Software (`trkg.in` / `bus.trackingo.in`) live bus links, pre-configured with the live 33-stop route and telemetry for `http://trkg.in/BITLAA/ZK3M8T` (`https://bus.trackingo.in/customer/track_vehicle?ZK3M8T`).

## Files Included
- `index.html` — Complete, self-contained single-file web application (open directly in any browser).
- `app.js` — Extracted JavaScript telemetry engine, Leaflet map controller, and API parser.
- `styles.css` — Extracted custom CSS styles and Leaflet dark-theme overrides.

## Live API Endpoints Documented
1. **Short Link Redirect**: `http://trkg.in/BITLAA/ZK3M8T` -> `https://bus.trackingo.in/customer/track_vehicle?ZK3M8T`
2. **Journey & 33-Stop Schedule API**: `GET https://bus.trackingo.in/api/live/journey_details?key=ZK3M8T&zoom_position=12&platform=mobile`
3. **Real-Time GPS & Speed Polling API (20s interval)**: `GET https://bus.trackingo.in/api/live/eta_map?key=ZK3M8T&current_status=true`

## GitHub Pages CI/CD Deployment (`.github/workflows/deploy-pages.yml`)
1. Push this folder to a GitHub repository (`main` or `master` branch).
2. In your GitHub repository, navigate to **Settings → Pages**.
3. Under **Build and deployment → Source**, select **GitHub Actions**.
4. Every push to `main`/`master` (or manual run from the **Actions** tab) will automatically package `index.html` and deploy your live bus tracker to `https://<username>.github.io/<repo>/`.
