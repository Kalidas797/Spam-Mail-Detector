# Email Spam Detector - Static Deployment Guide

This guide will help you deploy the Email Spam Detector application as a static website using GitHub Pages.

## Prerequisites

1. A GitHub account
2. Git installed on your computer

## Deployment Steps

1. Create a new repository on GitHub
   - Go to github.com and sign in
   - Click the '+' icon and select 'New repository'
   - Name your repository (e.g., 'email-spam-detector')
   - Make it public
   - Initialize with a README

2. Prepare your local files
   - Create a new branch called `gh-pages`
   - Convert the Flask application to a static site:
     - Keep `index.html` from the templates folder
     - Export the ML models to JSON format
     - Implement the prediction logic in JavaScript

3. Push your code to GitHub
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/email-spam-detector.git
   git push -u origin main
   ```

4. Enable GitHub Pages
   - Go to your repository settings
   - Navigate to 'Pages'
   - Select the `gh-pages` branch as the source
   - Save the changes

5. Access your deployed site
   - Your site will be available at: `https://YOUR_USERNAME.github.io/email-spam-detector`

## Important Notes

- The static version will require converting the Python ML models to a format usable in the browser (e.g., TensorFlow.js)
- All processing will happen client-side
- Consider the size of the converted models for optimal loading performance

## Alternative Deployment Options

1. Netlify
   - Sign up for a free account
   - Connect your GitHub repository
   - Deploy automatically from your main branch

2. Vercel
   - Similar to Netlify
   - Excellent for static site hosting
   - Automatic deployments from GitHub

3. Firebase Hosting
   - Free tier available
   - Good for static and dynamic content
   - Easy deployment process

Choose the platform that best suits your needs. All these options offer free tiers suitable for personal projects.