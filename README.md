# Police Web App

This is a Blazor WebAssembly application for police operations management.

## Deployment

This application is automatically deployed to GitHub Pages using GitHub Actions.

### How It Works

1. When changes are pushed to the `main` branch, the GitHub Actions workflow automatically deploys the static site to GitHub Pages.
2. The workflow can also be triggered manually from the Actions tab.
3. The site is available at: `https://kapambwe.github.io/PoliceWebApp/`

### Setup Requirements

To enable GitHub Pages deployment for this repository:

1. Go to repository Settings → Pages
2. Under "Build and deployment":
   - Source: Select "GitHub Actions"
3. The workflow will automatically deploy the site on the next push to `main`

### Manual Deployment

You can manually trigger a deployment:
1. Go to the "Actions" tab in the repository
2. Select "Deploy static content to Pages" workflow
3. Click "Run workflow" button

### Local Development

This repository contains the built output of a Blazor WebAssembly application. The application uses:
- Blazor WebAssembly
- Bootstrap for styling
- Leaflet for mapping features
- Radzen Blazor components

The base path is configured as `/PoliceWebApp/` to match the GitHub Pages URL structure.

## Files

- `index.html` - Main entry point
- `service-worker.js` - Service worker for offline support
- `.nojekyll` - Prevents Jekyll processing on GitHub Pages
- `_framework/` - Blazor framework files
- `_content/` - Static content from Blazor components
