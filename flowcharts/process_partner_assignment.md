# GPSTopo — Field Partner / PLS Assignment Workflow

```mermaid
%% GPSTopo: Partner Assignment Logic
graph TD
    A[New Project Created] --> B[Extract Project Metadata]
    B --> C[Service Type]
    B --> D[Project Location]
    B --> E[Urgency Level]
    
    C --> F{Assignment Rules Engine}
    D --> F
    E --> F
    
    F --> G{Service Type}
    
    G -->|Boundary/Topo| H[Query: GPS/Drone Partners]
    G -->|ALTA/Legal| I[Query: Licensed PLS Network]
    G -->|Layout/Staking| J[Query: Field Tech + PLS]
    
    H --> K{Location Match}
    I --> K
    J --> K
    
    K -->|Local Partner Available| L[Check Partner Workload]
    K -->|No Local Match| M[Expand Radius + Check Availability]
    
    M --> L
    
    L --> N{Workload OK?}
    
    N -->|Partner Available| O[Auto-Assign + Notify via WhatsApp]
    N -->|Partner Busy| P[Offer to Next Available]
    
    P --> O
    
    O --> Q[Partner Accepts/Declines]
    Q --> R{Accepted?}
    
    R -->|Yes| S[Lock Assignment + Send Project Details]
    R -->|No Response 2hrs| T[Re-route to Backup Partner]
    R -->|Declined| T
    
    T --> P
    S --> U[Partner Receives Full Scope + Access Link]

%% Assignment Priority Logic:
%% 1. Location proximity (prefer within 30-mile radius)
%% 2. Service type expertise (ALTA must go to licensed PLS)
%% 3. Current workload (max 3 active projects per partner)
%% 4. Historical performance (QC pass rate, turnaround time)
%% 5. Client urgency (rush jobs go to fastest responders)
```

---

## Partner Assignment Rules

### Rule 1: Service Type Matching

| Service | Required Partner Type |
|---------|----------------------|
| Boundary Mapping | GPS tech or PLS (depends on state) |
| Topographic | Drone operator or GPS tech |
| Construction Layout | Field tech + PLS verification |
| As-Built | Field tech + PE/PLS certification |
| ALTA/NSPS | Licensed PLS only |

### Rule 2: Location Proximity

- **Preferred:** Within 30-mile radius of project site
- **Acceptable:** Within 60-mile radius (may incur travel fee)
- **Remote:** Beyond 60 miles (requires special approval or higher rate)

### Rule 3: Workload Balancing

- **Max Active Projects per Partner:** 3 concurrent
- **Rush Projects:** Only assign to partners with <2 active projects
- **ALTA Projects:** Reserve for partners with proven track record (>90% QC pass rate)

### Rule 4: Response Time SLA

- **Partner Response Time:** 2 hours to accept or decline
- **No Response Action:** Auto-route to backup partner
- **Partner Cancellation:** Must notify >24 hours in advance (except emergencies)

---

## Partner Communication Flow

### Step 1: Initial Assignment Notification (WhatsApp + Email)

```
📍 New Project Assigned: [Project ID]
Service: [Boundary / Topo / ALTA]
Location: [Address]
Deadline: [Date]
Pay: $[Amount]

🔗 View Details: [Link]
✅ Accept | ❌ Decline
```

### Step 2: Acceptance Confirmation

```
✅ Project [Project ID] confirmed!
📂 Access project files: [Link]
📞 Client contact: [If needed]
📅 Expected completion: [Date]

Questions? Reply here or call our ops line.
```

### Step 3: Reminder (24 hours before deadline)

```
⏰ Reminder: Project [Project ID] due tomorrow
Status: [In Progress / Not Started]

Need extension? Let us know ASAP.
```

---

## Partner Performance Metrics

Track these metrics per partner for assignment optimization:

| Metric | Target |
|--------|--------|
| **Acceptance Rate** | >80% |
| **On-Time Delivery Rate** | >95% |
| **QC First-Pass Rate** | >90% |
| **Average Response Time** | <1 hour |
| **Client Feedback Score** | >4.5/5 |

---

## Automation Tools

- **Zapier/Make:** Trigger assignment on project card creation
- **Airtable Formula:** Auto-calculate partner availability based on active project count
- **WhatsApp Business API:** Send instant notifications
- **Google Maps API:** Calculate proximity and travel time

---

*Partner network management is key to scalability and consistent quality.*

