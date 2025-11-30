# Sports Interest Histogram

Interactive histogram visualizing global weekly search interest for several major sports leagues, built with HTML, CSS, and D3.js. The chart reads data directly from `sportsdata.csv` and can be deployed automatically to GitHub Pages via the included GitHub Actions workflow.


## Features

- Responsive, glassmorphism-inspired layout with accessible color contrast.
- D3-powered histogram with tooltips, keyboard focus, and adaptive bin counts.
- League selector to switch between Formula 1, NBA, NFL, and Premier League trends.
- Summary statistics panel (count, mean, median, IQR, 90th percentile) updating per selection.
- GitHub Actions workflow configured for automatic Pages deployment.

## Getting Started

1. Clone the repository and open the folder in your editor.
2. Launch a static file server (for example, VS Code Live Server) or open `index.html` in your browser. Local hosting is recommended so the browser can fetch `sportsdata.csv` without CORS issues.
3. Interact with the histogram by selecting different leagues.

## Customizing

- Update or replace `sportsdata.csv` with the same column names to visualize new data.
- Adjust styling within the `<style>` block of `index.html` or extract it into a separate stylesheet if preferred.
- Modify the `seriesMeta` array in the script to rename leagues or add new descriptions.

## Deployment

The workflow in `.github/workflows/deploy.yml` publishes the site to GitHub Pages whenever changes are pushed to the `main` branch.

1. In your repository settings, enable GitHub Pages and choose **Deploy from a branch** with source **GitHub Actions** if prompted.
2. Push to `main` (or trigger the workflow manually via **Actions → Deploy static site → Run workflow**).
3. After the workflow completes, the published URL appears in the workflow summary and under **Deployments**.

## Troubleshooting

- If the page shows "Failed to load sportsdata.csv", confirm the file exists in the repository root and retains the expected header names (`Week`, `f1: (Worldwide)`, etc.).
- Resize your browser window to force the histogram to recompute its binning.
- Use browser dev tools (Network tab) to ensure the CSV is served correctly when testing locally.
