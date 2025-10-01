# Twilio Toll-Free Verification Guide for YardHawk

**Status**: Ready for submission
**Date Prepared**: October 1, 2025
**Purpose**: Complete guide for submitting Twilio toll-free number verification

---

## 📋 Quick Checklist

Before starting Twilio verification, ensure you have:

- [x] Created static HTML pages for betaranch.com
- [x] Business information (legal name, EIN, address)
- [x] Website with SMS terms and privacy policy
- [x] Sample messages prepared
- [x] Use case descriptions written
- [x] Opt-in workflow documented

---

## 🌐 Required Web Pages

### Pages to Upload to betaranch.com

Upload these three HTML pages to your GitHub Pages repository:

1. **SMS Terms of Service**
   - File: `sms-terms.html`
   - URL: `https://betaranch.com/sms-terms.html`
   - Purpose: Documents SMS service terms, opt-in/opt-out, message types

2. **Privacy Policy**
   - File: `privacy.html`
   - URL: `https://betaranch.com/privacy.html`
   - Purpose: Data handling, privacy rights, SMS data protection

3. **SMS Opt-In Information**
   - File: `sms-opt-in.html`
   - URL: `https://betaranch.com/sms-opt-in.html`
   - Purpose: Shows how users sign up for SMS notifications

**Important**: All files are located in `docs/twilio-verification/static-pages/`

---

## 📝 Twilio Verification Form Submission

### Step 1: Business Information

Navigate to Twilio Console → Active Numbers → Select your toll-free number → Regulatory Information

#### Required Fields:

| Field | Your Response |
|-------|---------------|
| **Legal Business Name** | Beta Ranch, LLC |
| **Business Registration Number (EIN)** | [Your EIN - required by early 2026] |
| **Business Type** | Software/Technology Services (B2B SaaS) |
| **Business Address** | [Your registered business address] |
| **Business Phone** | [Your business phone number] |
| **Business Email** | support@betaranch.com |
| **Website URL** | https://betaranch.com |

---

### Step 2: Use Case Description

Twilio requires a clear explanation of how you'll use the toll-free number.

#### Primary Use Case: **Equipment Rental Operations Management**

**Detailed Description to Submit:**

```
YardHawk is a B2B software platform for construction equipment rental companies.
We send transactional SMS notifications to rental yard staff and rental customers
for operational purposes:

1. PullTag: Equipment gathering notifications sent to yard staff when customer
   orders require equipment to be pulled from the rental yard. Messages include
   pull tag ID, customer name, and link to equipment details.

2. ReturnPing: Rental return reminders sent to rental customers 24 hours before
   equipment is due back, helping ensure timely returns and reduce late fees.

All messages are transactional and operational in nature. We do NOT send marketing
or promotional messages. Message frequency: Yard staff receive 5-20 messages per
day during peak operations; customers receive 1-2 messages per rental contract.

Recipients are either employees of rental companies using our software or customers
renting equipment from those companies. All recipients provide explicit consent
through onboarding or rental contract signup.
```

**Character Count**: ~800 characters (well within Twilio limits)

---

### Step 3: Opt-In Process Documentation

Twilio requires proof that users consent to receive messages.

#### Opt-In Method: **WEB_FORM** (Primary) + **VERBAL** (Secondary)

**Primary Opt-In Workflow Description:**

```
YardHawk has two distinct opt-in workflows:

YARD STAFF OPT-IN:
1. Organization administrator adds employee to YardHawk system via web console
2. Administrator enters employee's mobile number in the roster management form
3. Web form includes checkbox: "I confirm this employee consents to receive
   operational SMS notifications from YardHawk for equipment pull requests"
4. Employee receives welcome SMS: "Welcome to YardHawk! You'll receive equipment
   pull notifications. Reply STOP to opt out. Reply HELP for support."
5. Employee can opt out anytime by replying STOP

RENTAL CUSTOMER OPT-IN:
1. During equipment rental contract setup, rental company asks customer:
   "Would you like to receive SMS reminders before your equipment is due back?"
2. Customer verbally agrees and provides mobile number
3. Rental staff enters number in YardHawk contract form with opt-in confirmation
4. Customer receives: "ABC Rentals will send you return reminders via YardHawk.
   Reply STOP to opt out."

Both workflows use branded YardHawk messaging, are specific to described use cases,
and allow immediate opt-out via STOP command.
```

#### Opt-In Page URL to Submit:

**URL**: `https://betaranch.com/sms-opt-in.html`

This page clearly shows:
- How users sign up (onboarding for staff, rental contract for customers)
- Example messages they'll receive
- Opt-out instructions (reply STOP)
- Message frequency expectations
- Privacy information

**Screenshot Recommendation**: Take a screenshot of the opt-in page showing the complete workflow and submit as supporting documentation.

---

### Step 4: Sample Messages

Twilio wants to see actual message examples.

#### Sample Message 1: PullTag (Yard Staff)

```
🚛 PULL TAG: PT-A1B2C3
Customer: ABC Construction
Contract: 12345
Link: yardhawk.app/pt/xyz
Reply STOP to opt out
```

**Character Count**: 102 characters
**Message Type**: Transactional/Operational
**Purpose**: Notify yard staff of equipment pull request

---

#### Sample Message 2: ReturnPing Warning (Rental Customer)

```
⏰ RETURN REMINDER: Equipment Excavator 320 due back 2:00 PM today. Contract #12345. Reply STOP to opt out.
```

**Character Count**: 107 characters
**Message Type**: Transactional/Reminder
**Purpose**: Remind customer of upcoming equipment return

---

#### Sample Message 3: ReturnPing Overdue (Rental Customer)

```
🚨 OVERDUE: Equipment Excavator 320 was due 2:00 PM. Please return immediately. Late fees may apply. Contract #12345
```

**Character Count**: 117 characters
**Message Type**: Transactional/Alert
**Purpose**: Notify customer equipment is overdue

---

#### Sample Message 4: Welcome/Confirmation

```
Welcome to YardHawk! You'll receive equipment pull notifications. Reply STOP to opt out. Reply HELP for support.
```

**Character Count**: 111 characters
**Message Type**: Transactional/Confirmation
**Purpose**: Confirm opt-in and provide instructions

---

### Step 5: Additional URLs to Provide

| Purpose | URL | Description |
|---------|-----|-------------|
| SMS Terms of Service | https://betaranch.com/sms-terms.html | Complete SMS terms and conditions |
| Privacy Policy | https://betaranch.com/privacy.html | Data handling and privacy rights |
| Opt-In Information | https://betaranch.com/sms-opt-in.html | How users sign up for SMS |
| Main Website | https://betaranch.com | Company information and contact |

---

## 🎯 Best Practices for Approval

Based on Twilio's verification best practices:

### ✅ Do This:

1. **Match Everything**: Ensure business name on website matches legal name in Twilio
2. **Use Business Email**: Use @betaranch.com email, not personal Gmail/Yahoo
3. **Be Specific**: Provide detailed use case description (we did above)
4. **Show Branding**: All opt-in pages and messages mention "YardHawk"
5. **Separate Consent**: Opt-in is standalone, not buried in general terms
6. **Real Content**: Website has substantive content about YardHawk services

### ❌ Avoid This:

1. **Vague Descriptions**: Don't just say "operational messages" - be specific
2. **Shared Consent**: Don't share opt-in across multiple use cases
3. **Login Walls**: All verification URLs must be publicly accessible (no login required)
4. **Generic Emails**: Don't use gmail.com or other personal email domains
5. **Missing Pages**: Ensure all URLs resolve and show proper content

---

## 📸 Screenshots to Prepare

For best approval chances, prepare these screenshots:

1. **SMS Opt-In Page** (`/sms-opt-in.html`)
   - Shows complete workflow
   - Demonstrates branded opt-in process
   - Visible "Reply STOP to opt out" messaging

2. **Staff Roster Form** (from YardHawk app - optional)
   - Shows where administrator enters phone numbers
   - Demonstrates opt-in checkbox
   - Screenshot can be from staging/demo environment

3. **SMS Terms Page** (`/sms-terms.html`)
   - Shows comprehensive terms documentation
   - Demonstrates compliance focus

**Image Requirements**:
- Publicly accessible URLs (upload to GitHub Pages or host on Imgur)
- Format: PNG or JPG
- Must show actual branded content (not lorem ipsum)

---

## 🔄 Submission Process

### Step-by-Step in Twilio Console:

1. **Log in to Twilio Console**
   - Navigate to: Phone Numbers → Active Numbers

2. **Select Your Toll-Free Number**
   - Click on the toll-free number you want to verify

3. **Go to Regulatory Information Tab**
   - Click "Verify this toll free number"

4. **Choose Profile Option**
   - If you have existing Trust Hub profile: Select it
   - If new: Click "Create new Customer Profile"

5. **Fill Business Information**
   - Copy business info from table above
   - Use exact legal name: "Beta Ranch, LLC"

6. **Enter Use Case**
   - Copy the detailed use case description from above
   - Paste into "Use Case Description" field

7. **Document Opt-In Process**
   - Select primary method: "WEB_FORM"
   - Paste opt-in workflow description from above
   - Add URL: `https://betaranch.com/sms-opt-in.html`

8. **Provide Sample Messages**
   - Add all 4 sample messages from above
   - Include character counts if requested

9. **Submit Additional URLs**
   - SMS Terms: https://betaranch.com/sms-terms.html
   - Privacy Policy: https://betaranch.com/privacy.html
   - Main Website: https://betaranch.com

10. **Upload Screenshots (Optional but Recommended)**
    - Screenshot of opt-in page
    - Screenshot of roster form (if available)

11. **Review and Submit**
    - Double-check all URLs are accessible
    - Verify email matches domain (support@betaranch.com)
    - Submit for review

---

## ⏱️ After Submission

### Expected Timeline:
- **Review Period**: 3-5 business days
- **Status Updates**: Check Twilio Console → Messaging → Toll-Free Verification
- **Email Notifications**: Twilio will email updates to support@betaranch.com

### Possible Statuses:

1. **In Progress**: Under review (normal)
2. **Approved**: ✅ Ready to send SMS to US/Canada
3. **Rejected**: ❌ Review rejection reason and resubmit

### If Rejected:

Common rejection reasons and fixes:

| Rejection Reason | How to Fix |
|------------------|------------|
| Website not accessible | Verify all URLs load publicly (no login) |
| Opt-in not clear | Add more detail to opt-in workflow description |
| Use case vague | Add specific message examples and frequency |
| Business info mismatch | Ensure legal name matches across all pages |
| Missing EIN (2026+) | Provide Employer Identification Number |

---

## 🔐 Business Registration Number (EIN)

**Important Update (September 30, 2025):**

Twilio now collects Employer Identification Numbers (EINs) for toll-free verification.

- **Currently**: Optional but recommended
- **By Early 2026**: Required for all new verifications

**Where to Get Your EIN:**
- IRS Form SS-4 (if you already filed)
- IRS online EIN application
- Tax returns or business registration documents

**Format**: XX-XXXXXXX (e.g., 12-3456789)

---

## 📞 Help & Support

### Twilio Support:
- Console Help Center: Click "?" icon in Twilio Console
- Twilio Support: Create ticket in Console
- Verification Help: https://www.twilio.com/docs/messaging/compliance/toll-free

### YardHawk Internal:
- Verification Status: Track in Twilio Console
- Questions: Contact Claude for technical details
- Updates: Document any changes in this guide

---

## ✅ Pre-Submission Checklist

Before clicking Submit in Twilio Console:

- [ ] All 3 HTML pages uploaded to betaranch.com
- [ ] Verified all URLs load publicly (test in incognito browser)
- [ ] Business email uses @betaranch.com domain
- [ ] Legal business name matches across all pages
- [ ] Use case description is detailed and specific (not vague)
- [ ] Sample messages include "Reply STOP to opt out"
- [ ] Opt-in workflow clearly explains how users consent
- [ ] Screenshots prepared (optional but helpful)
- [ ] EIN ready (if available, required by 2026)

---

## 📊 Quick Reference Card

**Business Info:**
- Name: Beta Ranch, LLC
- Email: support@betaranch.com
- Website: https://betaranch.com

**Key URLs:**
- SMS Terms: https://betaranch.com/sms-terms.html
- Privacy: https://betaranch.com/privacy.html
- Opt-In: https://betaranch.com/sms-opt-in.html

**Use Cases:**
1. PullTag: Yard staff equipment pull notifications
2. ReturnPing: Customer rental return reminders

**Message Frequency:**
- Yard Staff: 5-20/day during operations
- Customers: 1-2 per rental contract

**Opt-In Methods:**
- Primary: Web form during onboarding/contract
- Secondary: Verbal consent for rental customers

---

## 🎉 After Approval

Once approved:

1. **Update toll-free number** in environment variables:
   ```
   TWILIO_PHONE_NUMBER=+1-8XX-XXX-XXXX
   ```

2. **Test SMS delivery**:
   - Send test PullTag message
   - Send test ReturnPing message
   - Verify delivery to US and Canadian numbers

3. **Update HTML pages** with actual toll-free number:
   - Replace "[Number will be assigned]" in all pages
   - Redeploy to betaranch.com

4. **Document in codebase**:
   - Update .env.example with toll-free number format
   - Add toll-free number to README if needed

---

## 📝 Notes

- Keep this guide updated if Twilio requirements change
- Save approval confirmation from Twilio
- Document any rejection reasons for future reference
- This guide prepared based on Twilio requirements as of October 2025

---

**Good luck with your verification!** 🚀

If you have questions during submission, refer to Twilio's official documentation:
- https://www.twilio.com/docs/messaging/compliance/toll-free/console-onboarding
- https://help.twilio.com/articles/13264118705051-Required-Information-for-Toll-Free-Verification
