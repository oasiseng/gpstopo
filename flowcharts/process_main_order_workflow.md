# GPSTopo — Main Order Workflow (Service-Specific)

```mermaid
%% GPSTopo: Complete Online Order Workflow with Service Branching
graph TD
    A([Client visits gpstopo.com]) --> B[Browse Services + Pricing]
    B --> C{Select Service Type}
    
    C -->|Boundary Mapping| D1[/Enter: Address + Parcel Info/]
    C -->|Topographic| D2[/Enter: Site Info + Design Needs/]
    C -->|Construction Layout| D3[/Enter: Design Files + Specs/]
    C -->|As-Built| D4[/Enter: Original Plans + Scope/]
    C -->|ALTA/NSPS| D5[/Enter: Title Info + Table A Items/]
    
    D1 --> E[Review Quote + Add-ons]
    D2 --> E
    D3 --> E
    D4 --> E
    D5 --> E
    
    E --> F[Stripe Checkout]
    F --> G{Payment Status}
    
    G -->|Failed| H[Auto-Email: Payment Issue + Retry Link]
    G -->|Success| I[✓ Payment Confirmed]
    
    H --> F
    
    I --> J[Zapier: Create Project Card]
    J --> K[Auto-Assign Field Partner/PLS]
    K --> L[Send Partner Notification via WhatsApp/Email]
    L --> M[Partner Reviews Scope]
    
    M --> N{Scope Clear?}
    N -->|Needs Clarification| O[Auto-Request Client Info]
    N -->|Clear| P[Field Data Collection]
    
    O --> P
    
    P --> Q[Upload Raw Data to Shared Folder]
    Q --> R[Drafting + Map Processing]
    R --> S{QC Review}
    
    S -->|Revisions Needed| T[Flag Issues + Return to Drafter]
    S -->|Approved| U[Package Deliverables]
    
    T --> R
    
    U --> V[Upload to Client Portal/Drive]
    V --> W[Auto-Send Delivery Email]
    W --> X[/Client Downloads Files/]
    X --> Y[Auto-Send Feedback Survey]
    Y --> Z([Project Closed + Archived])

%% Lean Optimization Tips:
%% 1. Use Stripe metadata to auto-populate project card fields
%% 2. Set partner assignment rules based on: location, service type, workload
%% 3. QC checklist auto-triggers when partner marks "Data Uploaded"
%% 4. Delivery email includes direct download link (no portal login needed)
```

---

## Service-Specific Turnaround Times

| Service | Target Turnaround | Rush Option |
|---------|-------------------|-------------|
| Boundary Mapping | 3–5 business days | +50% fee for 24-48hr |
| Topographic | 5–7 business days | +75% fee for 3-day |
| Construction Layout | 48–72 hours | Same-day available |
| As-Built | 3–5 days | +50% for 48hr |
| ALTA/NSPS | 10–15 days | Jurisdiction-dependent |

---

## Automation Trigger Points

1. **Stripe Payment Success** → Create Trello/Airtable card
2. **Card Created** → Assign partner based on rules
3. **Partner Assigned** → Send WhatsApp notification
4. **Status = "Data Uploaded"** → Trigger QC checklist
5. **QC Approved** → Package files + send delivery email
6. **Delivery Confirmed** → Send feedback survey after 24 hours

---

*Last Updated: November 2025*

