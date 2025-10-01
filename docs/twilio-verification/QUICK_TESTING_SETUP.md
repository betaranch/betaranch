# Quick Testing Setup (Skip Toll-Free for Now)

**Goal**: Get SMS working TODAY for pilot testing while toll-free verification processes

---

## 🚀 Immediate Testing Path (5 Minutes)

### Step 1: Buy a Regular Local Number

1. Log into Twilio Console: https://console.twilio.com/
2. Navigate to: Phone Numbers → Manage → Buy a number
3. **Select "Local" (NOT toll-free)**
   - Choose your area code (e.g., your local area or WT Equipment's area)
   - Select any available number
   - Cost: ~$1-2/month
4. Click "Buy"

**No verification required** - ready immediately!

---

### Step 2: Update Environment Variables

```bash
# In your .env file:
TWILIO_PHONE_NUMBER=+15125551234  # Your new local number
TWILIO_ACCOUNT_SID=ACxxxxxxxxxxxxx # From Twilio Console
TWILIO_AUTH_TOKEN=your_auth_token   # From Twilio Console
```

---

### Step 3: Test SMS Immediately

```bash
# Test PullTag SMS
pnpm tsx scripts/test-pulltag-sms.sh

# Or use the API directly
curl -X POST http://localhost:3000/api/pull-tag/generate \
  -H "Content-Type: application/json" \
  -d '{
    "contractId": "test-contract-123",
    "phoneNumber": "+15125551111"  # Your test number
  }'
```

---

## ✅ For Production: Parallel Process

While you're testing with local number, submit toll-free verification:

### Week 1 (Now): Test with Local Number
- Deploy HTML pages to betaranch.com
- Submit toll-free verification
- Continue testing with local number

### Week 2: Switch to Toll-Free
- Toll-free verification approved (3-5 days)
- Update environment variable to toll-free number
- Continue using same code - just different number

---

## 📊 Comparison

| Feature | Local Number | Toll-Free | 10DLC |
|---------|--------------|-----------|-------|
| Setup Time | 5 minutes | 3-5 days | ~1 week |
| Verification | None | Required | Required |
| Cost | ~$1-2/month | ~$2-3/month | ~$2-3/month |
| Deliverability | Good | Excellent | Very Good |
| Professional | Moderate | High | High |
| **Good for Testing?** | ✅ YES | Overkill | Optional |

---

## 🎯 Recommended Approach

**For your pilot with WT Equipment:**

1. **This Week**:
   - Buy local number ($1)
   - Test PullTag workflow with WT staff
   - Verify SMS delivery and deep links work
   - Deploy HTML pages to betaranch.com

2. **Next Week**:
   - Submit toll-free verification (using byron@betaranch.com)
   - Continue testing while waiting for approval

3. **Week 2-3**:
   - Toll-free approved
   - Switch to toll-free number
   - Ready for broader pilot rollout

This way you're **not blocked** and can start validating the SMS workflow immediately.

---

## 🔍 Why This Works

- **Local numbers** work great for testing and small-scale use
- **Toll-free** is for professional production use
- Your code doesn't care - just swap the phone number in .env
- All the verification HTML pages still apply to toll-free (keep them)

---

## 💰 Cost Comparison

**Testing Phase (1 month):**
- Local number: $1-2
- SMS messages: ~$0.0079 per message
- 100 test messages: ~$2
- **Total: ~$3-4 for testing month**

**Production (after toll-free approved):**
- Toll-free number: $2-3/month
- SMS messages: same rate
- Switch when ready

---

## ⚠️ Important Notes

- Local numbers have **no verification requirement**
- Messages from local numbers may be filtered slightly more by carriers
- For **testing with known users** (WT Equipment staff), this is fine
- For **production at scale**, use toll-free

---

## 🚀 Get Started Right Now

1. Go buy a local number: https://console.twilio.com/us1/develop/phone-numbers/manage/search
2. Update TWILIO_PHONE_NUMBER in .env
3. Send test message to yourself
4. Test with WT Equipment staff

**You can be testing in 5 minutes.**

Then submit toll-free verification in parallel so it's ready when you need it.
