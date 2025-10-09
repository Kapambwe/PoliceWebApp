# GitHub Pages Deployment Guide

## What Was Done

This Pull Request sets up automatic deployment of the Police Web App to GitHub Pages.

### Files Added

1. **`.github/workflows/deploy.yml`** - GitHub Actions workflow that:
   - Automatically deploys to GitHub Pages when code is pushed to `main` branch
   - Can be manually triggered from the Actions tab
   - Uses official GitHub Actions for secure deployment
   - Handles all static content deployment

2. **`README.md`** - Documentation that explains:
   - How the deployment works
   - Setup instructions for GitHub Pages
   - Manual deployment process
   - Application overview

## How to Complete Deployment

After merging this PR to the `main` branch, follow these steps:

### Step 1: Enable GitHub Pages

1. Go to the repository on GitHub
2. Click on **Settings** tab
3. Click on **Pages** in the left sidebar
4. Under "Build and deployment":
   - **Source**: Select **"GitHub Actions"** from the dropdown
5. Save the settings (it may save automatically)

### Step 2: Trigger Deployment

The deployment will happen automatically in one of two ways:

**Option A: Automatic (Recommended)**
- Simply merge this PR to the `main` branch
- The workflow will run automatically
- The site will be deployed to `https://kapambwe.github.io/PoliceWebApp/`

**Option B: Manual**
- Go to the **Actions** tab
- Select "Deploy static content to Pages" workflow
- Click **"Run workflow"** button
- Select the `main` branch
- Click **"Run workflow"** to start

### Step 3: Verify Deployment

1. Wait for the workflow to complete (usually takes 1-2 minutes)
2. Visit `https://kapambwe.github.io/PoliceWebApp/`
3. The Police Web App should load successfully

## Technical Details

### Application Configuration

The app is already properly configured for GitHub Pages deployment:
- Base path is set to `/PoliceWebApp/` in `index.html`
- `.nojekyll` file prevents Jekyll processing
- Service worker is configured for offline support
- All static assets are pre-compressed (`.br` and `.gz` files)

### Workflow Features

- **Automatic deployment** on push to `main` branch
- **Manual deployment** available via Actions tab
- **Proper permissions** configured for Pages deployment
- **Concurrency control** to prevent conflicting deployments
- **Environment tracking** for deployment URLs

### Future Updates

Any time you push new changes to the `main` branch:
1. The workflow will automatically run
2. The updated site will be deployed to GitHub Pages
3. The deployment typically completes in 1-2 minutes

## Troubleshooting

### If the site doesn't load:

1. Check that GitHub Pages source is set to "GitHub Actions" in repository Settings
2. Verify the workflow ran successfully in the Actions tab
3. Check the browser console for any errors
4. Ensure the base path in `index.html` matches `/PoliceWebApp/`

### If you need to change the deployment:

- The workflow file is at `.github/workflows/deploy.yml`
- You can modify settings like the branch to deploy from
- Changes to the workflow require a push to take effect

## Questions?

If you encounter any issues with the deployment:
1. Check the Actions tab for workflow run logs
2. Review the deployment status in Settings → Pages
3. Verify the application works locally first
