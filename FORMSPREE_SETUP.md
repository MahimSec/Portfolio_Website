# Formspree Integration Setup Instructions

## Steps to Connect Your Form to Formspree:

### 1. Create a Formspree Account
- Go to https://formspree.io
- Sign up for a free account (or login if you already have one)

### 2. Create a New Form
- Click "New Form" or "Create Form"
- Give it a name like "Portfolio Contact Form" or "Hire Me Form"
- Formspree will generate a unique Form ID

### 3. Get Your Form ID
- After creating the form, you'll see a form ID like: `xpzkgdwq`
- Copy this ID

### 4. Update Your HTML File
- Open `/home/unknown/Portfolio Website/hire-me.html`
- Find line 80: `<form id="hire-form" class="space-y-6" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">`
- Replace `YOUR_FORM_ID` with your actual Form ID
- Example: `<form id="hire-form" class="space-y-6" action="https://formspree.io/f/xpzkgdwq" method="POST">`

### 5. Features Already Configured:

✅ **Hidden Subject Line**: Emails will have subject "New Job Inquiry from Portfolio"
✅ **Reply-to Email**: Uses `_replyto` so you can reply directly from your email
✅ **Success Message**: Green success banner appears after successful submission
✅ **Error Handling**: Red error banner appears if something goes wrong
✅ **Loading State**: Button shows "Sending..." while submitting
✅ **Form Reset**: Form clears automatically after successful submission
✅ **Smooth Scrolling**: Auto-scrolls to success/error message

### 6. Formspree Settings (Optional):
In your Formspree dashboard, you can configure:
- **Email notifications**: Where to send form submissions
- **Autoresponder**: Send automatic thank you emails
- **Spam filtering**: Enable reCAPTCHA or honeypot
- **Custom redirect**: Redirect to a thank you page (currently handled by JS)

### 7. Free Plan Limits:
- 50 submissions per month
- Unlimited forms
- Email notifications
- Spam filtering

### 8. Testing Your Form:
1. Open `hire-me.html` in your browser
2. Fill out all required fields
3. Click "Submit Application"
4. You should see the green success message
5. Check your Formspree dashboard for the submission
6. Check your email for the notification

## Form Fields Being Sent:

- **Full Name**: `full_name`
- **Email**: `_replyto` (special Formspree field for reply-to)
- **Target Role**: `target_role`
- **Years Experience**: `years_experience`
- **Expected Salary**: `salary`
- **Job Type**: `job_type`
- **Message/Cover Letter**: `message`
- **Subject** (hidden): `_subject` = "New Job Inquiry from Portfolio"

## Troubleshooting:

**If form doesn't submit:**
- Check browser console for errors (F12 → Console tab)
- Verify Form ID is correct
- Make sure you're using the correct Formspree URL format
- Check Formspree dashboard for any issues

**If submissions go to spam:**
- Configure Formspree's spam filtering
- Enable reCAPTCHA in Formspree settings

**Need more submissions?**
- Upgrade to Formspree's paid plan (starting at $10/month for 1000 submissions)

## Support:
- Formspree Docs: https://help.formspree.io/
- Formspree Status: https://status.formspree.io/
