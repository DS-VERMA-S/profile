# EmailJS Setup Guide

This guide will help you set up EmailJS to make your contact form functional.

## Step-by-Step Setup

### 1. Create EmailJS Account
1. Visit [https://www.emailjs.com/](https://www.emailjs.com/)
2. Click "Sign Up" and create a free account
3. Verify your email address

### 2. Add Email Service
1. In your EmailJS dashboard, go to **Email Services**
2. Click **"Add New Service"**
3. Choose your email provider:
   - **Gmail**: Most popular choice
   - **Outlook**: Microsoft email
   - **Yahoo**: Yahoo Mail
   - **Custom SMTP**: For other providers

#### For Gmail Setup:
1. Select "Gmail"
2. Click "Connect Account"
3. Sign in with your Gmail account
4. Grant permissions
5. Note down the **Service ID** (e.g., `service_abc123`)

### 3. Create Email Template
1. Go to **Email Templates** in your dashboard
2. Click **"Create New Template"**
3. Use this template:

**Template Name**: `portfolio_contact`

**Subject**: `New Contact Form Message - {{subject}}`

**Content**:
```
Hello,

You have received a new message from your portfolio contact form:

Name: {{from_name}}
Email: {{from_email}}
Subject: {{subject}}

Message:
{{message}}

---
Sent from your portfolio website
```

4. Click **"Save"**
5. Note down the **Template ID** (e.g., `template_xyz789`)

### 4. Get Public Key
1. Go to **Account** > **General**
2. Find **Public Key** section
3. Copy your **Public Key** (e.g., `user_abcdef123456`)

### 5. Update Your Code

#### In `script.js`, replace these lines:
```javascript
// Replace these with your actual EmailJS credentials
const EMAILJS_SERVICE_ID = 'YOUR_SERVICE_ID';
const EMAILJS_TEMPLATE_ID = 'YOUR_TEMPLATE_ID';
const EMAILJS_PUBLIC_KEY = 'YOUR_PUBLIC_KEY';
```

#### With your actual values:
```javascript
const EMAILJS_SERVICE_ID = 'service_abc123';
const EMAILJS_TEMPLATE_ID = 'template_xyz789';
const EMAILJS_PUBLIC_KEY = 'user_abcdef123456';
```

#### Also update the recipient email:
```javascript
to_email: 'your.actual.email@gmail.com' // Replace with your email
```

### 6. Test Your Setup
1. Open your website in a browser
2. Scroll to the contact form
3. Fill out all fields:
   - Name: Test User
   - Email: test@example.com
   - Subject: Test Message
   - Message: This is a test message
4. Click "Send Message"
5. Check your email inbox for the message

## Troubleshooting

### Common Issues:

1. **"Email service not configured" error**:
   - Make sure you've replaced all placeholder values
   - Check that your Service ID, Template ID, and Public Key are correct

2. **Email not received**:
   - Check your spam/junk folder
   - Verify your email service is properly connected
   - Check EmailJS dashboard for error logs

3. **Form validation errors**:
   - Ensure all fields are filled
   - Check email format is valid
   - Make sure required attributes are present

### EmailJS Limits (Free Plan):
- 200 emails per month
- 2 email services
- 2 email templates
- Basic support

### Upgrade Options:
- **Pro Plan**: $15/month for 1,000 emails
- **Business Plan**: $25/month for 10,000 emails

## Alternative Solutions

If EmailJS doesn't work for you, consider these alternatives:

### 1. Formspree
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
    <input type="text" name="name" required>
    <input type="email" name="email" required>
    <textarea name="message" required></textarea>
    <button type="submit">Send</button>
</form>
```

### 2. Netlify Forms
If hosting on Netlify, add `netlify` attribute:
```html
<form name="contact" method="POST" data-netlify="true">
    <!-- form fields -->
</form>
```

### 3. Custom Backend
Use Node.js with Nodemailer for full control.

## Security Notes

- Never expose your EmailJS private keys
- Use environment variables in production
- Consider rate limiting for production use
- Validate all form inputs on the server side

## Support

- EmailJS Documentation: [https://www.emailjs.com/docs/](https://www.emailjs.com/docs/)
- EmailJS Support: [https://www.emailjs.com/support/](https://www.emailjs.com/support/)
- GitHub Issues: Create an issue in your repository
