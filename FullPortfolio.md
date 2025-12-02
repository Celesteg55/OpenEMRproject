FULL END-TO-END PORTFOLIO PROJECT DELIVERABLES

**Project:** OpenEMR Workflow Modernization  
**Version:** Hybrid (BA + Technical Ops)  
**Author:** Brenda Garza  

---

## 1. Business Requirements Document (BRD)

- Full document covering:  
  - Executive Summary  
  - Business Objectives  
  - Current State Analysis (As-Is)  
  - Future State Recommendations (To-Be)  
  - Business Requirements Table (BR-01 → BR-10)  
  - Assumptions & Constraints  
  - Risks & Mitigation  
  - Success Criteria  

*Stored as:* `BRD.md` or `BRD.pdf`

---

## 2. Functional Requirements Document (FRD)

- Covers functional behaviors and user interactions  
- Includes all modules: Scheduling, Digital Check-In, Vitals, Clinical Routing, Label Printing, RFID, Lab Workflow, Patient Portal  
- User Stories linked to functional requirements  

*Stored as:* `FRD_SRS.md`

---

## 3. System Requirements Specification (SRS)

- Non-functional requirements (Security, Performance, Availability, Scalability, Usability, Hardware Integration)  
- System Architecture Overview  
- Data sources & APIs  
- Integration points  
- Stored as part of FRD: `FRD_SRS.md`

---

## 4. BPMN & Flowchart Set

**BPMN Diagrams (Text + Diagram Instructions)**

1. **Check-In & Vitals Flow:**  
   - Start → Check-In → Vitals → Doctor Consultation → Lab Order Decision → Lab Processing → Results Uploaded → End  

2. **Lab Workflow:**  
   - Physician creates lab order → Lab Queue → RFID scan → Processing → Results synced  

3. **Patient Portal Updates:**  
   - Lab results ready → System pushes updates → Notification → Patient views results  

---

## 5. JIRA User Stories

| ID    | User Story                       | Points | Module / Notes |
|-------|---------------------------------|--------|----------------|
| US-01 | Create digital check-in screen   | 3      | UI + validation |
| US-02 | Generate barcode wristband label | 5      | Zebra / NiceLabel |
| US-03 | Create vitals entry module       | 3      | Nurse workflow |
| US-04 | Notify physician after vitals    | 2      | Trigger event |
| US-05 | RFID tag assignment to lab samples | 8    | Integrate hardware |
| US-06 | Update status dashboard          | 5      | Real-time routing |

*Stored as:* `JIRA_UserStories.md`

---

## 6. Test Plan + UAT Scripts

**SIT & UAT Test Scenarios:**

- **SIT:** Module integration & hardware verification  
  - Check-in triggers label printing  
  - RFID updates lab queue  
  - Vitals submission alerts physician  

- **UAT:** End-user workflow validation  
  - Receptionist: patient check-in process  
  - Nurse: vitals entry & alerts  
  - Lab Tech: sample tracking via RFID  

*Stored as:* `TestPlan.md`

---

## 7. Change Control Document

- Versioning and approval process for requirement changes  
- Example columns: Request ID, Description, Impact, Status, Approval  

*Stored as:* `ChangeControl.md`

---

## 8. Status Report Examples

- Weekly progress tracking  
- Columns: Task, Owner, Status, Risks, Next Steps  
- Optional charts: Burndown chart, sprint progress, completed vs. planned  

*Stored as:* `StatusReports.md`

---

## 9. Charts & Metrics

- **Burndown Chart:** Story points remaining per sprint  
- **Velocity Chart:** Points completed per sprint  
- **Gantt/Timeline:** Sprint dates, milestones, dependencies  


---

## 10. How to Explain This Project

- **Project Overview:** 1–2 sentence description  
- **Workflow Summary:** High-level patient flow  
- **Deliverables Summary:** BRD, FRD, SRS, BPMN, User Stories, Test Plan  
- **Outcome / Impact:** Reduced wait times, improved lab tracking, streamlined communication  

*Stored as:* `Project_Summary.md`
