# EmailJS Setup Guide for Portfolio Contact Form

This guide will help you set up EmailJS for your portfolio contact form to ensure messages are properly delivered to your email address.

## Step 1: Create an EmailJS Account

1. Go to [EmailJS.com](https://www.emailjs.com/) and sign up for an account
2. Verify your email address as required

## Step 2: Add an Email Service

1. In your EmailJS dashboard, go to "Email Services"
2. Click "Add New Service"
3. Select your preferred email provider (Gmail, Outlook, etc.)
4. Follow the authentication steps to connect your email account (anwaarmuzzamil@gmail.com)
5. Name your service (e.g., "portfolio_service")
6. Copy the **Service ID** (will look like "service_xxxxxxx")

## Step 3: Create an Email Template

1. Go to "Email Templates" in the dashboard
2. Click "Create New Template"
3. Design your template using these variables (already configured in your code):
   - `{{name}}`: Sender's name
   - `{{email}}`: Sender's email
   - `{{message}}`: The message content
   - `{{to_name}}`: Your name (Muzzamil Anwar)
   - `{{to_email}}`: Your email (anwaarmuzzamil@gmail.com)

4. Set up your template to look something like this:
```
From: {{name}} ({{email}})
To: {{to_name}} ({{to_email}})

Message:
{{message}}
```

5. Give your template a name (e.g., "contact_form")
6. Copy the **Template ID** (will look like "template_xxxxxxx")

## Step 4: Get Your Public Key

1. Go to "Account" > "API Keys" in the dashboard
2. Copy your **Public Key**

## Step 5: Update Your Website Code

1. Open `index.html` and replace the placeholder in this line:
```javascript
emailjs.init('YOUR_PUBLIC_KEY');
```
Replace 'YOUR_PUBLIC_KEY' with your actual public key.

2. Open `script.js` and replace the placeholders in this line:
```javascript
emailjs.send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', templateParams)
```
Replace 'YOUR_SERVICE_ID' with your actual service ID and 'YOUR_TEMPLATE_ID' with your actual template ID.

## Important Notes

- Make sure you're using a free or paid EmailJS plan with enough message quota for your needs
- Test the form after setup to ensure it works properly
- Check your spam folder if you don't receive test messages

## Troubleshooting

If you encounter issues:
1. Verify all IDs and keys are correctly copied
2. Check browser console for error messages
3. Ensure your email service is properly connected
4. Verify your EmailJS account is active and in good standing

For further assistance, visit [EmailJS Documentation](https://www.emailjs.com/docs/). 