# GPSTopo — Quick Reference Cheat Sheet

**One-page reference for daily operations** 🚀

---

## 🎯 Services at a Glance

| Service | Price Range | Turnaround | Key Deliverable |
|---------|-------------|------------|-----------------|
| Boundary | $495–$795 | 3-5 days | PDF + DWG map |
| Topo | $795–$1,495 | 5-7 days | Contours + CSV |
| Layout/Staking | $395–$695 | 48-72 hrs | Staking report |
| As-Built | $695–$995 | 3-5 days | As-built + cert |
| ALTA | $1,995–$4,995 | 10-15 days | Signed survey |

---

## ⚡ Automation Flow (Quick View)

```
Payment → Create Card → Assign Partner → Field Work → QC → Deliver → Feedback
   ↓           ↓              ↓             ↓        ↓       ↓         ↓
Stripe      Airtable      WhatsApp      Upload    Review  Email    Survey
<30sec       <5min         <5min        Varies    <2hrs   <5min    +24hrs
```

---

## 📊 Target Response Times

| Action | Target Time |
|--------|-------------|
| Payment to assignment | <2 hours |
| Partner to accept | <2 hours |
| Client support response | <2 hours |
| QC review | <2 hours |
| Field work to QC | 24-48 hours |
| QC to delivery | <1 hour |

---

## ✅ QC Pass/Fail Checklist (Ultra-Quick)

**Boundary:**
- ✓ Lines match GIS  
- ✓ Dimensions labeled  
- ✓ Disclaimer present

**Topo:**
- ✓ Contours consistent  
- ✓ Elevations accurate  
- ✓ CSV matches drawing

**ALTA:**
- ✓ Table A complete  
- ✓ PLS signature  
- ✓ State compliance

---

## 💳 Payment Methods

| Method | Use Case |
|--------|----------|
| Stripe Card | Default (instant) |
| Stripe ACH | Save fees (3-5 days) |
| Invoice Net-15 | Repeat clients |
| Invoice Net-30 | Commercial |

---

## 🚨 Emergency Contacts

| Issue | Contact |
|-------|---------|
| Urgent field issue | Fernando: [WhatsApp] |
| Payment problem | Enrique: [Email/Phone] |
| Client escalation | Leo: [Email/Phone] |
| Tech/automation down | Enrique: [WhatsApp] |

---

## 📞 Support Templates (Copy/Paste)

### "Where's my order?"
```
Hi [Name], your project is [Status]. Expected delivery: [Date]. 
You'll get an auto-email when ready. Questions? Reply here!
```

### "Free revision approved"
```
Thanks for flagging this. We'll issue a corrected version within 
24-48 hours at no charge. Apologies for the oversight!
```

### "Out-of-scope change"
```
That falls outside the original scope. We can provide those 
details as a revision for $[Amount]. Proceed?
```

---

## 🧮 Profitability Quick Math

**Target Net Margin:** 50-60%

Example (Topo Survey):
- Client pays: $995
- Partner cost: $450
- **GPSTopo net: $545** (55%)

---

## 🔧 Tech Stack URLs

| Tool | Login/Dashboard |
|------|-----------------|
| Stripe | dashboard.stripe.com |
| Airtable | airtable.com/[workspace] |
| Zapier | zapier.com/app/dashboard |
| Website | hostinger.com |

---

## 📅 Daily Ops Checklist

**Every Morning:**
- [ ] Check Airtable for stuck projects (>24hrs no update)
- [ ] Review partner assignments (any no-response?)
- [ ] Check support email inbox
- [ ] Verify Zapier automations running (no failed zaps)

**Every Afternoon:**
- [ ] Follow up on pending QC reviews
- [ ] Check client feedback responses
- [ ] Update any custom quotes
- [ ] Archive completed projects

---

## 🎯 KPI Dashboard (Weekly Review)

| Metric | This Week | Target | Status |
|--------|-----------|--------|--------|
| Orders | ___ | 10+ | 🟢/🟡/🔴 |
| Avg. Turnaround | ___ | <5 days | 🟢/🟡/🔴 |
| QC Pass Rate | ___% | >95% | 🟢/🟡/🔴 |
| Revenue | $____ | $10k+ | 🟢/🟡/🔴 |
| NPS Score | ___ | >50 | 🟢/🟡/🔴 |

---

## 🛠️ Troubleshooting Common Issues

**Zapier not firing:**
1. Check Stripe webhook settings
2. Verify Airtable API key
3. Test trigger manually in Zapier

**Partner not responding:**
1. Check WhatsApp delivery status
2. Try backup contact method
3. Reassign after 2 hours

**Client download link broken:**
1. Regenerate OneDrive/Drive link
2. Check link expiration settings
3. Send via alternate method (email attachment)

**Payment failed:**
1. Send retry link from Stripe
2. Check if card expired
3. Offer ACH or manual payment

---

## 💡 Founder Decisions (When to Escalate)

| Scenario | Decision |
|----------|----------|
| Refund request >$500 | Enrique approval |
| Partner dispute | Fernando review |
| Legal/compliance question | Consult PLS/attorney |
| Custom service request | Quote with all 3 founders |
| Pricing exception | Enrique approval |

---

## 🚀 Growth Hacks

1. **Upsell rush fees** at checkout (+30% AOV)
2. **Bundle services** (topo + boundary = 15% off)
3. **Referral program** ($100 off for both parties)
4. **Monthly retainer** (3 surveys = 20% off)
5. **Seasonal promotions** (winter slow season discount)

---

## 📖 Where to Find More Info

- **Full process docs:** `/backup/` folder
- **Business spec:** `gpstopo_business_spec.md`
- **Automation details:** `automation_trigger_map.md`
- **Pricing guide:** `service_pricing_guide.md`
- **Glossary:** `glossary_and_faq.md`

---

*Print this and keep it handy for quick reference!*

**Last Updated:** November 10, 2025

