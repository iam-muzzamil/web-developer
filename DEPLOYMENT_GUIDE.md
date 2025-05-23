# Netlify Deployment Guide for Portfolio Website

This guide will help you deploy your portfolio website to Netlify, making it publicly accessible on the web.

## Prerequisites

- A GitHub account (if you don't have one, sign up at [github.com](https://github.com))
- A Netlify account (sign up for free at [netlify.com](https://netlify.com))

## Step 1: Setup EmailJS (for contact form functionality)

1. Go to [EmailJS](https://www.emailjs.com/) and sign up for a free account
2. Create a new Email Service (Gmail, Outlook, or any other email provider)
3. Create a new Email Template for your contact form
4. Get your EmailJS User ID (Public Key) from Account Settings
5. Replace the placeholder values in your website files:
   - In `index.html`, replace `YOUR_PUBLIC_KEY` with your EmailJS public key
   - In `script.js`, replace `service_id` with your EmailJS service ID and `template_id` with your template ID

## Step 2: Push Your Code to GitHub

1. Create a new GitHub repository:
   - Go to [github.com/new](https://github.com/new)
   - Name your repository (e.g., "portfolio-website")
   - Choose "Public" visibility
   - Click "Create repository"

2. Initialize and push your code:
   ```bash
   # Navigate to your project folder
   cd "D:\dOWNLOADS\Portfolio Website"
   
   # Initialize a git repository
   git init
   
   # Add all files
   git add .
   
   # Commit your changes
   git commit -m "Initial commit"
   
   # Add the remote repository
   git remote add origin https://github.com/YOUR_USERNAME/portfolio-website.git
   
   # Push to GitHub
   git push -u origin master
   ```

## Step 3: Deploy to Netlify

1. Log in to Netlify
2. Click "New site from Git"
3. Select "GitHub" as your Git provider
4. Authorize Netlify to access your GitHub account
5. Select the repository you just created
6. Configure deployment settings:
   - Build command: (leave blank for a static site)
   - Publish directory: (leave blank to use the root directory)
7. Click "Deploy site"

## Step 4: Set Up a Custom Domain (Optional)

1. After deployment, go to your site settings in Netlify
2. Click on "Domain settings" or "Domain management"
3. You can either:
   - Purchase a domain through Netlify
   - Use a domain you already own by adding custom DNS records

## Step 5: Update Your Site

Whenever you want to make changes to your website:

1. Make changes to your local files
2. Commit your changes:
   ```bash
   git add .
   git commit -m "Description of changes"
   git push
   ```
3. Netlify will automatically detect the changes and redeploy your site

## Troubleshooting

If your contact form is not working:
1. Check browser console for any JavaScript errors
2. Verify that your EmailJS service ID, template ID, and public key are correct
3. Ensure your email template contains the fields: `from_name`, `from_email`, `message`, and `to_email`

## Additional Resources

- [Netlify Documentation](https://docs.netlify.com/)
- [EmailJS Documentation](https://www.emailjs.com/docs/)
- [GitHub Guides](https://guides.github.com/) 