# 🎫 Salesforce Support Ticket Management System (Admin + QA Project)

## 📌 Project Overview
This Salesforce Admin + QA mini project is designed to manage customer support issues using a simple ticketing system.
It helps users create and track **Support Tickets**, assign them to **Agents**, and monitor ticket progress using reports and dashboards.

This project demonstrates Salesforce Admin skills such as:
- Custom Objects & Fields
- Lookup Relationships
- Validation Rules
- Record-Triggered Flow Automation
- Reports & Dashboard
- Manual Testing (Test Cases)

---

## 🎯 Objectives
✅ Create and manage support tickets efficiently  
✅ Link tickets with Customers and Agents  
✅ Automatically set ticket Priority based on Issue Type  
✅ Ensure data quality using validation rules  
✅ Track ticket status and performance with reports and dashboard  

---

## 🧱 Objects Created
### 1) Customer
Stores customer details.
- Email
- Phone
- Customer Type (New / Existing)
- Status (Active / Inactive)

### 2) Agent
Stores support agent details.
- Email
- Active (Checkbox)
- Level (L1 / L2 / L3)

### 3) Support Ticket
Stores customer issues and ticket tracking info.
- Ticket Number (Auto Number: `TKT-0001`)
- Customer (Lookup → Customer)
- Assigned Agent (Lookup → Agent)
- Issue Type (Login Issue / Payment Issue / Bug / Feature Request / Other)
- Priority (Low / Medium / High / Critical)
- Status (New / In Progress / Resolved / Closed)
- Description (Long Text)
- Resolution Notes (Long Text)
- SLA Due Date (Date)

---

## 🔗 Relationships Implemented
✅ **Support Ticket → Customer** (Lookup Relationship)  
✅ **Support Ticket → Agent** (Lookup Relationship)

This ensures each Support Ticket is linked to:
- one Customer
- one Assigned Agent

---

## ✅ Validation Rules Implemented
### 1) Customer Mandatory
Prevents ticket creation without selecting Customer.


## 🔗 Relationships Implemented
✅ **Support Ticket → Customer** (Lookup Relationship)  
✅ **Support Ticket → Agent** (Lookup Relationship)

This ensures each Support Ticket is linked to:
- one Customer
- one Assigned Agent

---

## ✅ Validation Rules Implemented
### 1) Customer Mandatory
Prevents ticket creation without selecting Customer.

2) Resolution Notes Mandatory for Resolved/Closed
Prevents saving ticket as Resolved/Closed without Resolution Notes.

⚡ Automation (Record Triggered Flow)
Auto Set Ticket Priority (Before Save)
A Record-Triggered Flow automatically assigns Priority based on Issue Type:

Issue Type	Priority Set Automatically
Payment Issue	High
Bug	High
Login Issue	Medium
Feature Request	Low
Other	Low

✅ Flow Name: Auto_Set_Ticket_Priority
✅ Trigger: Support Ticket created
✅ Type: Before Save (Fast Field Updates)

📊 Reports Created
✅ Tickets by Status
✅ Tickets by Priority
✅ Tickets by Issue Type
✅ Tickets by Agent

📈 Dashboard Created
✅ Support Ticket Dashboard
Includes charts for:

Tickets by Priority

Tickets by Status

Tickets by Issue Type

Tickets Assigned to Agents

🧪 QA Testing (Test Cases)
Manual test cases were created to validate:
✅ Customer & Agent creation
✅ Ticket creation workflow
✅ Lookup relationships (Customer & Agent)
✅ Validation rules behavior
✅ Flow automation accuracy
✅ Report and dashboard visibility

 (Google Sheet) [https://docs.google.com/spreadsheets/d/1KJiDnRVBdBkL8puulI-zm2gu3WXYQ0kQZpgP4JgV6Es/edit?usp=sharing]
 
📸 Screenshots
Add your screenshots inside a folder called:
screenshots/

Recommended screenshots:

Custom objects & fields [https://drive.google.com/file/d/1iSsKDeR0i4cO6eB0pQrmw_CRu2Bh5xHZ/view?usp=sharing] 

Record Triggered Flow : [https://drive.google.com/file/d/1-xboQRDI0rgtPrF3jXm2W_qnRW3QZkz1/view?usp=sharing]

Validation Rules : [https://drive.google.com/file/d/159Zf4Yc9e4yuZl9ZtyovFA43GPEOmwpr/view?usp=sharing]

Reports : [https://drive.google.com/file/d/1IXHZ0DdZL7pvjsaX83-wefTxRO4gtUZO/view?usp=sharing]

Dashboard :[https://drive.google.com/file/d/16xEod2OJevFLR2LgjPIKvwo2Pox1PmdA/view?usp=sharing]

👤 Author
Monika Sarkar
Salesforce QA | Manual Testing | Salesforce Admin | Jira | Test Case Writing | SOQL
