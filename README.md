# Kirkup Consulting

GitHub Pages site for Kirkup Consulting, a digital pathology consulting group run by Christian Kirkup.

## Overview

This repository hosts the public website for Kirkup Consulting, providing information about digital pathology consulting services. The site is automatically deployed to GitHub Pages using GitHub Actions.

## Website Structure

- `index.html` - Main homepage with information about services, about section, and contact details
- Responsive design that works on desktop and mobile devices
- Clean, professional design appropriate for a consulting group

## Deployment

The site is automatically deployed to GitHub Pages using GitHub Actions. The deployment workflow:

- **Location**: `.github/workflows/deploy.yml`
- **Trigger**: Automatically runs on every push to the `main` branch
- **Manual Trigger**: Can also be manually triggered via the GitHub Actions UI

### Setup Instructions

1. **Enable GitHub Pages**:
   - Go to repository Settings → Pages
   - Under "Source", select "GitHub Actions" (not "Deploy from a branch")
   - The workflow will handle deployment automatically

2. **Workflow Permissions**:
   - The workflow requires `pages: write` and `id-token: write` permissions
   - These are configured in the workflow file and should work automatically

3. **Deployment Process**:
   - When code is pushed to `main`, the workflow automatically:
     - Checks out the repository
     - Configures GitHub Pages
     - Uploads the site files as an artifact
     - Deploys to GitHub Pages

## Local Development

To view the site locally:

1. Clone the repository
2. Open `index.html` in a web browser
3. Or use a local web server:
   ```bash
   python -m http.server 8000
   ```
   Then visit `http://localhost:8000`

## Making Updates

To update the website:

1. Edit `index.html` or other files as needed
2. Commit and push changes to the `main` branch
3. The GitHub Actions workflow will automatically deploy the updated site
4. Changes typically appear on the live site within a few minutes

## Site URL

Once deployed, the site will be available at:
`https://[username].github.io/kirkup-consulting/`

Or if using a custom domain, configure it in repository Settings → Pages.

## Technologies

- Pure HTML/CSS (no build step required)
- GitHub Actions for CI/CD
- GitHub Pages for hosting
