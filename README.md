# Auto_ticket_classification_using_Flow_Designer
A ServiceNow-based project that automatically classifies school IT support tickets using Flow Designer and sends automated email notifications.

# Auto Ticket Classification using Flow Designer

> A no-code ServiceNow solution that automatically classifies school IT helpdesk tickets (Category + Subcategory) and emails the caller as soon as a ticket is created.

| | |
|---|---|
| **Platform** | ServiceNow (Personal Developer Instance) – Flow Designer / Workflow Studio |
| **Custom Table** | Incident Workflow (`u_incident_workflow`) |
| **Flow Name** | Auto Classify School IT Tickets |
| **Update Set** | Project Update Set (Global scope) |
| **Team Members** | SAMRIN HASRAA S ,SALMA FARHANA M ,SAJITHA FATHIMA S K ,FATHIMA M |
| **Demo Video** | https://drive.google.com/file/d/1ToS4YSfd7P7Z9bMIzXCOWc1GtuFfXclN/view?usp=drive_link |

---

## Problem in one line
The school IT helpdesk gets many tickets daily (Wi-Fi, projector, password, slow computer) and staff manually pick the category for each one – slow, error-prone and not scalable.

## Solution in one line
A Flow Designer flow triggers on every new ticket, reads the **Short Description** for keywords, sets **Category** and **Subcategory** automatically, and sends a confirmation email to the **Caller**.

## Keyword → Classification map

| Short Description contains | Category | Subcategory |
|---|---|---|
| Wi-Fi / Network | Network | Wi-Fi |
| Projector | Hardware | Projector |
| Forgot password | Access | Forgot Password |
| Slow Computer | Performance | Slow Computer |

---

## Phase-wise Documents

| # | Phase | Document |
|---|---|---|
| 1 | Brainstorming & Ideation | [01_Brainstorming_and_Ideation_Phase.md](01_Brainstorming_and_Ideation_Phase.docx) |
| 2 | Requirement Analysis | [02_Requirement_Analysis_Phase.md](02_Requirement_Analysis_Phase.docx) |
| 3 | Project Design | [03_Project_Design_Phase.md](03_Project_Design_Phase.docx) |
| 4 | Project Planning | [04_Project_Planning_Phase.md](04_Project_Planning_Phase.docx) |
| 5 | Project Development | [05_Project_Development_Phase.md](05_Project_Development_Phase.docx) |
| 6 | Project Testing | [06_Project_Testing_Phase.md](06_Project_Testing_Phase.docx) |
| 7 | Project Documentation | [07_Project_Documentation_Phase.md](07_Project_Documentation_Phase.docx) |
| 8 | Project Demonstration | [08_Project_Demonstration_Phase.md](08_Project_Demonstration_Phase.docx) |

## Repository Structure

```
.
├── README.md
├── 01_Brainstorming_and_Ideation_Phase.docx
├── 02_Requirement_Analysis_Phase.docx
├── 03_Project_Design_Phase.docx
├── 04_Project_Planning_Phase.docx
├── 05_Project_Development_Phase.docx
├── 06_Project_Testing_Phase.docx
├── 07_Project_Documentation_Phase.docx
├── 08_Project_Demonstration_Phase.docx
├── images/                      # screenshots used in the documents
└── update_set/
    └── sys_remote_update_set_df12b071836fc310eb55f1e6feaad344.xml
```

## How to import the project into another ServiceNow instance
1. Go to **All → System Update Sets → Retrieve Update Sets** (or *Update Sets to Commit* → *Import Update Set from XML*).
2. Upload the XML file from the `update_set/` folder.
3. Open the loaded update set → **Preview Update Set** → resolve any issues → **Commit Update Set**.
4. Open **Flow Designer**, find *Auto Classify School IT Tickets* and **Activate** it.
