# GPSTopo Technologies - Online Order Workflow

## 100% Digital Survey Ordering Process

```mermaid
%% GPSTopo: Online Survey Order Workflow
graph TD
    A([Client visits gpstopo.com]) --> B{Select Service Type}
    B -->|Boundary| C[/Enter Project Info + Address/]
    B -->|Topo| C
    B -->|As-Built| C
    C --> D[Stripe Checkout]
    D --> E[✓ Payment Confirmed]
    E --> F[Auto-Create Project Card]
    F --> G[Notify Team + Assign PLS/Field Partner]
    G --> H[Field Data Collection]
    H --> I[Map Processing & Drafting]
    I --> J{QC Review}
    J -->|Revisions Needed| I
    J -->|Approved| K[Upload to Client Portal]
    K --> L[Auto-Send Delivery Email + Files]
    L --> M[/Client Downloads + Optional Feedback/]
    M --> N([Project Closed & Archived])

%% Lean Optimization Tips:
%% 1. Combine "Create Card" and "Notify Team" via one webhook → avoid extra integrations
%% 2. Use Stripe metadata to pass service type directly to project card
%% 3. Set up auto-assignment rules based on location/workload to eliminate manual dispatch
%% 4. Trigger QC checklist automatically when field partner marks "complete"
```

---

## Key Automation Points

| Step | Tool/Method | Automation Trigger |
|------|-------------|-------------------|
| Payment | Stripe Checkout | Form submission |
| Project Card | Trello/Airtable API | Stripe webhook |
| Team Notification | Email/Slack | Card creation event |
| Partner Assignment | Smart routing rules | Location + availability |
| QC Review | Checklist trigger | Status change to "Complete" |
| Delivery | Email + portal link | QC approval |
| Feedback | Survey link | Delivery confirmation |

---

## Process Metrics to Track

- **Order-to-Assignment Time**: Target < 2 hours
- **Field-to-Delivery Time**: Target < 48 hours
- **QC Pass Rate**: Target > 95% first-time
- **Client NPS**: Track via feedback link

---

*Last Updated: November 2025*

