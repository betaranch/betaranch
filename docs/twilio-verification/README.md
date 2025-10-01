# Twilio Toll-Free Verification Package

**Purpose**: Complete documentation and web pages for Twilio toll-free SMS verification
**Status**: Ready for deployment
**Date Created**: October 1, 2025

---

## 📦 What's Included

This directory contains everything needed to verify a Twilio toll-free number for YardHawk SMS services.

### 📄 Static HTML Pages (for betaranch.com)

Located in `static-pages/`:

1. **sms-terms.html** - SMS Terms of Service
   - Deploy to: `https://betaranch.com/sms-terms.html`
   - Purpose: Legal terms for SMS messaging

2. **privacy.html** - Privacy Policy
   - Deploy to: `https://betaranch.com/privacy.html`
   - Purpose: Data handling and privacy rights

3. **sms-opt-in.html** - SMS Opt-In Information
   - Deploy to: `https://betaranch.com/sms-opt-in.html`
   - Purpose: How users sign up for notifications

### 📋 Documentation

- **TWILIO_TOLL_FREE_VERIFICATION_GUIDE.md** - Complete verification guide
  - Business information to submit
  - Use case descriptions
  - Sample messages
  - Opt-in workflow documentation
  - Step-by-step Twilio Console instructions
  - Pre-submission checklist

- **DEPLOYMENT_STEPS.md** - Quick deployment instructions
  - How to upload pages to GitHub Pages
  - Verification steps
  - Testing checklist

---

## 🚀 Quick Start

### Step 1: Deploy HTML Pages to betaranch.com

```bash
# Copy the three HTML files to your betaranch.com GitHub Pages repository
cp static-pages/*.html /path/to/betaranch-website/

# Commit and push to GitHub
cd /path/to/betaranch-website
git add *.html
git commit -m "Add Twilio verification pages for YardHawk SMS"
git push origin main
```

### Step 2: Verify Pages are Live

Test in your browser (incognito mode recommended):
- https://betaranch.com/sms-terms.html
- https://betaranch.com/privacy.html
- https://betaranch.com/sms-opt-in.html

All pages should load without login and display properly formatted content.

### Step 3: Submit Twilio Verification

Open `TWILIO_TOLL_FREE_VERIFICATION_GUIDE.md` and follow the detailed instructions.

Key information you'll need:
- Business name: Beta Ranch, LLC
- Business email: support@betaranch.com
- Website: https://betaranch.com
- EIN: [Your Employer Identification Number]

---

## 📝 Files Overview

```
twilio-verification/
├── README.md                                  (this file)
├── TWILIO_TOLL_FREE_VERIFICATION_GUIDE.md    (complete verification guide)
├── DEPLOYMENT_STEPS.md                        (quick deployment guide)
└── static-pages/
    ├── sms-terms.html                         (SMS terms of service)
    ├── privacy.html                           (privacy policy)
    └── sms-opt-in.html                        (opt-in information)
```

---

## ✅ Pre-Deployment Checklist

Before deploying to betaranch.com:

- [ ] Review all HTML pages for accuracy
- [ ] Verify business name matches legal registration
- [ ] Confirm contact email is support@betaranch.com
- [ ] Update any placeholder text (e.g., toll-free number will be added after approval)
- [ ] Check all internal links work correctly

---

## 🔍 What Twilio Will Check

Twilio reviewers will verify:

1. **Business Legitimacy**
   - Real business with active website
   - Contact information matches business domain
   - Legal name consistent across all pages

2. **Opt-In Process**
   - Clear explanation of how users consent
   - Branded messaging (mentions YardHawk)
   - Specific to use case (not generic)

3. **Message Compliance**
   - Sample messages include opt-out instructions
   - Messages are transactional, not marketing
   - Reasonable message frequency disclosed

4. **Website Quality**
   - Publicly accessible (no login walls)
   - Real content (not under construction)
   - Professional presentation

---

## 📞 Support

- **Twilio Help**: https://www.twilio.com/docs/messaging/compliance/toll-free
- **Internal Questions**: Review TWILIO_TOLL_FREE_VERIFICATION_GUIDE.md
- **Technical Issues**: Contact development team

---

## 🗑️ After Approval

Once Twilio approves your toll-free number:

1. Update environment variables with toll-free number
2. Replace "[Number will be assigned]" text in HTML pages with actual number
3. Redeploy updated pages to betaranch.com
4. Test SMS delivery to US and Canadian numbers
5. Archive this documentation for future reference

---

## 📅 Timeline

- **Preparation**: ~1 hour (deploy pages, gather business info)
- **Twilio Review**: 3-5 business days
- **After Approval**: Update configs and test (1 hour)

---

## 🎯 Success Criteria

You'll know verification is complete when:

✅ Twilio Console shows "Approved" status
✅ Toll-free number can send SMS to US/Canada
✅ Test messages deliver successfully
✅ Environment variables updated with toll-free number

---

**Note**: This is a temporary directory. After successful verification and deployment, this can be moved to `docs/_archive/` for historical reference.
