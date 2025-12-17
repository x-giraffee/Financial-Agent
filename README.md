# A-Share Global Earnings Monitor

A static single-page application (SPA) to track high-quality A-share sectors driven by global demand.

## 1. Implementation Highlights
- **Architecture:** Zero-build React (via Babel Standalone). Runs directly in the browser.
- **Styling:** Tailwind CSS (via CDN) for a dark, mobile-responsive UI.
- **Data Source:** Fetches `data.json` by default. Can be easily swapped for an API.
- **Logic:**
  - **Scoring:** Built-in scoring engine for Leaders (Supply Chain, Scale, Margin) and Growth (CAGR, Orders, Potential).
  - **Signals:** Automatic `Green/Yellow/Red` profit signal calculation based on metrics.
  - **Export:** Client-side CSV generation for the current view.

## 2. How to Deploy (GitHub Pages)
1. Create a new GitHub repository (e.g., `global-earnings-monitor`).
2. Upload `index.html` and `data.json` to the `main` branch (or `gh-pages` branch).
3. Go to **Settings > Pages**.
4. Select the branch where you uploaded the files as the source.
5. Save. Your site will be live at `https://<your-username>.github.io/global-earnings-monitor/`.

## 3. Maintenance
- **Update Data:** Simply edit the `data.json` file. The app reads it on every refresh.
- **Real API:** Search for `// DATA FETCHING` in `index.html` to swap the `fetch('./data.json')` call with your API endpoint (e.g., Python/TuShare backend).
- **Config:** Scoring weights and Signal thresholds are defined as `CONSTANTS` at the top of the script in `index.html`.
