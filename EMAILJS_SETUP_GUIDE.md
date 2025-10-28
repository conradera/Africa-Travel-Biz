# EmailJS Setup Guide - Direct Email Sending

## Overview
EmailJS allows your static website to send emails directly to `admin@africa-travel.info` without requiring a backend server. Messages are sent instantly when users submit the contact form.

---

## 📧 Setup Instructions

### Step 1: Create EmailJS Account

1. Go to **https://www.emailjs.com/**
2. Click "Sign Up" (free account)
3. Create an account with your email
4. Verify your email address

### Step 2: Add Email Service

1. In EmailJS dashboard, go to **"Email Services"**
2. Click **"Add New Service"**
3. Choose your email provider:
   - **Gmail** (recommended for personal/professional emails)
   - **Outlook**
   - **Custom SMTP**
4. Follow the connection steps for your email provider

### Step 3: Create Email Template

1. Go to **"Email Templates"** in dashboard
2. Click **"Create New Template"**
3. Use these settings:

**Template Settings:**
- **Template Name:** `Africa Travel Biz Contact Form`
- **Subject:** `{{subject}}`
- **To Email:** `admin@africa-travel.info`
- **From Email:** `{{from_email}}`
- **Reply To:** `{{from_email}}`

**Template Content:**
```
New Contact Form Submission from Africa Travel Biz Website

Name: {{from_name}}
Company: {{company}}
Email: {{from_email}}
Phone: {{phone}}

Message:
{{message}}

Submitted on: {{submission_date}}

---
This email was sent from the contact form on africatravelbiz.com
```

4. Click **"Save"**

### Step 4: Get Your Credentials

After creating the template, you'll need these values:

1. **Public Key**
   - Dashboard → **Account** → **Security**
   - Copy your **Public Key**

2. **Service ID**
   - Dashboard → **Email Services**
   - Copy the **Service ID** of your email service

3. **Template ID**
   - Dashboard → **Email Templates**
   - Copy the **Template ID** of your template

### Step 5: Update Your Website Code

Open `script.js` and replace the placeholder values on lines 159 and 174:

**Line 159** - Replace:
```javascript
window.emailjs.init("YOUR_PUBLIC_KEY");
```
With:
```javascript
window.emailjs.init("your-actual-public-key-here");
```

**Line 174** - Replace:
```javascript
window.emailjs.send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', templateParams)
```
With:
```javascript
window.emailjs.send('your-service-id', 'your-template-id', templateParams)
```

### Step 6: Test the Form

1. Open your website
2. Navigate to the contact form
3. Fill out all fields:
   - Name: Test User
   - Company: Test Company
   - Email: your-test@email.com
   - Phone: +1234567890
   - Message: This is a test message
4. Click "Send Message"
5. Check `admin@africa-travel.info` inbox for the email

---

## 📋 Email Format

When someone submits the form, you'll receive an email to `admin@africa-travel.info` with:

**Subject:** `New Inquiry from Africa Travel Biz - [Company Name]`

**Body:**
```
New Contact Form Submission from Africa Travel Biz Website

Name: John Doe
Company: ABC Corporation
Email: john@example.com
Phone: +81-90-xxxx-xxxx

Message:
I'm interested in your services for our upcoming business trip to Kenya.

Submitted on: 1/15/2024, 3:45:23 PM

---
This email was sent from the contact form on africatravelbiz.com
```

---

## ⚙️ Advanced Configuration

### Limit Email Volume (Free Tier)

- Free tier: 200 emails/month
- If you expect more volume, upgrade to Paid plan
- Check usage at Dashboard → Usage

### Customize Email Template

You can modify the email template in EmailJS dashboard:
- Add company branding
- Include unsubscribe links
- Add styling (HTML emails)
- Include attachments

### Security Settings

In EmailJS dashboard, enable:
- ✅ Rate limiting
- ✅ CAPTCHA (optional)
- ✅ Email validation

---

## 🔧 Troubleshooting

### Issue: "Email not sending"

**Solution:**
1. Check browser console for errors
2. Verify Public Key is correct
3. Verify Service ID is correct
4. Verify Template ID is correct
5. Ensure email service is connected properly

### Issue: "Email goes to spam"

**Solution:**
1. Add `africatravelbiz.com` as authorized domain
2. Configure SPF records for your email provider
3. Add DKIM authentication
4. Use professional sender address

### Issue: "Rate limit exceeded"

**Solution:**
1. Free tier: 200 emails/month
2. Upgrade to paid plan for more volume
3. Implement rate limiting in code
4. Add CAPTCHA to prevent spam

---

## 📊 Usage Monitoring

Monitor email usage:
1. Login to EmailJS dashboard
2. Go to **"Usage"**
3. See:
   - Emails sent this month
   - Email delivery status
   - Failed emails
   - Success rate

---

## 🎯 Next Steps

Once setup is complete:

1. ✅ Test form with real submission
2. ✅ Verify emails arrive at admin@africa-travel.info
3. ✅ Set up auto-reply (optional)
4. ✅ Configure email filters to organize incoming emails
5. ✅ Add form to database backup (optional)

---

## 📞 Support

- **EmailJS Documentation:** https://www.emailjs.com/docs/
- **EmailJS Support:** support@emailjs.com
- **EmailJS Community:** https://github.com/emailjs-com/emailjs-sdk

---

## 🔒 Privacy & Security

✅ **Data Protection:**
- EmailJS is GDPR compliant
- Data encrypted in transit
- No data stored on EmailJS servers (only forwarded)

✅ **Best Practices:**
- Don't share Public Key publicly (it's okay in client-side code)
- Keep Service ID and Template ID private
- Regularly review sent emails for spam
- Monitor usage to prevent abuse

---

**Setup Status:** Ready for configuration
**Estimated Setup Time:** 10-15 minutes
**Difficulty Level:** Easy

