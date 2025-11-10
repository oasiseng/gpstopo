# GPSTopo — Service Pricing Guide

**Internal Reference for Quoting & Stripe Product Setup**

---

## 💰 Base Pricing Structure

All prices include:
- Online ordering and payment
- Digital delivery
- One free revision (if within scope)
- Access to client portal
- Basic customer support

---

## Service Pricing Table

| Service | Base Price | Rush Fee | Typical Scope |
|---------|-----------|----------|---------------|
| **Boundary Mapping** | $495–$795 | +$250 (48hr) | Residential lot <0.5 acres |
| **Topographic Survey** | $795–$1,495 | +$500 (3-day) | 1-acre site with 2ft contours |
| **Construction Layout** | $395–$695 | +$200 (same-day) | Foundation corners + 4-6 points |
| **As-Built Verification** | $695–$995 | +$350 (48hr) | Post-construction elevation cert |
| **ALTA/NSPS Survey** | $1,995–$4,995 | By quote | Depends on Table A items |
| **Custom Drone Mapping** | $1,295+ | By quote | Site-specific (future service) |

---

## 📐 Pricing Variables

### Factor 1: Site Size

- **Residential (<1 acre):** Base price
- **Medium (1–5 acres):** +25–50%
- **Large (5+ acres):** Custom quote (typically +100%)

### Factor 2: Complexity

- **Simple/Flat Lot:** Base price
- **Wooded/Steep Terrain:** +$200–$400
- **Urban/Restricted Access:** +$150–$300

### Factor 3: Turnaround Time

| Option | Fee | Typical Use Case |
|--------|-----|------------------|
| Standard | Included | No deadline pressure |
| Rush (3-day) | +50% | Permit deadline approaching |
| Rush (48hr) | +75% | Urgent contractor need |
| Same-Day | +100%+ | Emergency staking |

### Factor 4: Additional Elements

- **Extra certifications:** +$150 (PE/PLS letter)
- **Multiple file formats:** +$50 per format
- **Site photos/drone imagery:** +$200–$500
- **3D terrain model:** +$300
- **Wetland delineation overlay:** +$250

---

## 🎯 Pricing by Market Segment

### Residential Homeowners

**Typical Service:** Boundary mapping for fence/pool permit

**Price Point:** $495–$695  
**Value Prop:** Fast, affordable, 100% online  
**Payment:** Stripe checkout (card or ACH)

---

### Contractors & Builders

**Typical Service:** Topo for design, as-builts for closeout

**Price Point:** $795–$1,495  
**Value Prop:** Quick turnaround, easy coordination  
**Payment:** Invoice + Stripe (Net-15 for repeat clients)

---

### Commercial / Title Companies

**Typical Service:** ALTA surveys for real estate transactions

**Price Point:** $1,995–$4,995  
**Value Prop:** Licensed PLS network, lender compliance  
**Payment:** Invoice (Net-30) or wire transfer

---

### Architects & Engineers

**Typical Service:** Topo + custom mapping for site design

**Price Point:** $1,295–$2,495  
**Value Prop:** Multiple formats (DWG, DXF, CSV), PE review  
**Payment:** Stripe or invoice (discount for repeat work)

---

## 💳 Payment Options

| Method | Use Case | Processing Time |
|--------|----------|-----------------|
| **Stripe Checkout (Card)** | One-time clients | Instant |
| **Stripe ACH** | Cost-conscious clients | 3-5 days |
| **Invoice (Net-15)** | Repeat contractors | Due in 15 days |
| **Invoice (Net-30)** | Commercial/gov clients | Due in 30 days |
| **Wire Transfer** | Large projects (>$5k) | 1-2 days |

---

## 🏷️ Stripe Product Setup

### Recommended Stripe Product Structure

**Option 1: Fixed Products** (Easiest to automate)

- Boundary Mapping — Small Lot: $495
- Boundary Mapping — Large Lot: $795
- Topographic Survey — 1 Acre: $995
- Topographic Survey — 3 Acres: $1,495
- ALTA Survey — Standard: $2,495
- ALTA Survey — Complex: $3,995

**Option 2: Variable Pricing** (More flexibility)

- Use Stripe's "Customer chooses amount" feature
- Set minimum price (e.g., $495)
- Require sales call or quote form first

---

## 📊 Pricing Strategy Notes

### Competitive Positioning

- **Traditional surveyors:** Often $1,500–$5,000+ for similar work (GPSTopo is 30–50% less)
- **Online GIS services:** $50–$200 (but lower quality, no field verification)
- **GPSTopo sweet spot:** Professional quality at tech-enabled prices

### Volume Discounts

- **5+ projects per year:** 10% discount
- **10+ projects per year:** 15% discount
- **Monthly retainer clients:** Custom pricing (typically 20–25% off)

### Seasonal Pricing (Optional)

- **Winter (slow season):** Promote with 10% off
- **Spring/Summer (busy):** Standard pricing
- **Rush fees:** Increase during peak season (+100% instead of +75%)

---

## 📝 Sample Quote Email Template

```
Hi [Client Name],

Thanks for your interest in GPSTopo mapping services!

Based on your project details:
📍 Location: [Address]
📐 Service: [Service Type]
🏞️ Site Size: [Acreage]

Estimated Price: $[Amount]
Turnaround: [Days] business days
Rush Option: Add $[Rush Fee] for [Rush Timeline]

This includes:
✅ Professional field data collection
✅ CAD-drafted deliverable (PDF + DWG)
✅ One free revision
✅ Digital delivery via secure portal

Ready to proceed? Place your order here: [Stripe Link]

Questions? Just reply to this email.

— GPSTopo Team
```

---

## 🧮 Profitability Breakdown (Internal)

**Target Margins per Service:**

| Service | Client Price | Partner Cost | GPSTopo Net | Margin % |
|---------|--------------|--------------|-------------|----------|
| Boundary | $595 | $250 | $345 | 58% |
| Topo | $995 | $450 | $545 | 55% |
| Layout | $495 | $200 | $295 | 60% |
| As-Built | $795 | $350 | $445 | 56% |
| ALTA | $2,995 | $1,800 | $1,195 | 40% |

*Partner costs include field work + drafting. Margins account for overhead, QC, support.*

---

## 🎯 Pricing Optimization Tips

1. **Bundle Services:** Offer "Topo + Boundary" package at 15% discount
2. **Upsell Rush Fees:** Present as option at checkout (increases AOV by 25%)
3. **Subscription Model (Future):** Monthly mapping plan for builders (e.g., 3 surveys/month for $2,495)
4. **Referral Discount:** $100 off for both referrer and new client

---

*Pricing should be transparent, competitive, and reflect the value of speed + convenience.*

