AGILE EXECUTION WORK PACKAGE

**Project:** OpenEMR Patient Scheduling & Clinical Workflow Modernization  
**Version:** Hybrid (BA + Technical Ops)  
**Author:** Brenda Garza  

---

## 1. Sprint Planning

**Sprint Goal:**  
Enable full digital check-in and vitals workflow.

**Step-by-Step Sprint Planning:**

1. Product Owner brings the goal.  
2. Business Analyst clarifies requirements:  
   - Review FRD/SRS  
   - Review workflow diagrams  
   - Confirm acceptance criteria  
   - Validate dependencies (label printers, RFID readers, API access)  
3. Development team breaks work into actionable user stories.  
4. Story point estimation using Fibonacci series: 1, 2, 3, 5, 8, 13  
   - Example:  
     - "Create check-in screen" → 3  
     - "Integrate RFID endpoint" → 8  
5. Capacity check: Team commits only to what they can realistically complete.  
6. Business Analyst updates the sprint backlog in JIRA.

---

## 2. Sprint Backlog

**Sprint Goal:**  
Enable patient check-in → vitals → physician routing with working labels.

| ID    | User Story                       | Points | Notes                |
|-------|---------------------------------|--------|--------------------|
| US-01 | Create digital check-in screen   | 3      | UI + validation     |
| US-02 | Generate barcode wristband label | 5      | Zebra / NiceLabel   |
| US-03 | Create vitals entry module       | 3      | Nurse workflow      |
| US-04 | Notify physician after vitals    | 2      | Trigger event       |
| US-05 | RFID tag assignment to lab samples | 8    | Integrate hardware  |
| US-06 | Update status dashboard          | 5      | Real-time routing   |

**Total:** 26 points (within capacity)

---

## 3. Sprint Burndown Chart

**Definition:**  
A burndown chart shows how many story points remain in the sprint.

**X-axis:** Days of Sprint  
**Y-axis:** Work Remaining  

**Purpose:** Track progress, identify bottlenecks early, adjust scope if needed.

---

## 4. Daily Stand-Up

**Questions Answered Daily:**

1. What I completed  
2. What I will do next  
3. Any blockers  

**Example for this project:**

- Yesterday: Finalized workflow for vitals module and validated label printing requirements.  
- Today: Writing acceptance criteria for RFID tracking.  
- Blockers: Need confirmation on number of RFID readers.

---

## 5. Sprint Review

**Purpose:**  
Demo completed work and gather feedback.

**Completed Features:**

- Digital check-in  
- Vitals module  
- Status dashboard  
- Label printing  
- RFID tagging for lab workflow  

---

## 6. Sprint Retrospective

**Purpose:**  
Identify what went well, what didn’t, and actions for improvement.

**Example Retrospective:**

**Went Well:**  
- Check-in feature delivered with zero bugs  
- RFID integration completed ahead of schedule  
- Clear acceptance criteria prevented rework  

**Didn’t Go Well:**  
- Label printer setup delayed due to missing device drivers  
- Vitals screen needed redesign after UX review  

**Improvements:**  
- Add hardware requirements checklist  
- Involve UX earlier  
- Use Figma for quick UI prototypes  

---

## 7. System Integration Testing (SIT) & User Acceptance Testing (UAT)

**SIT (System Integration Testing):**  
Testing how modules and hardware integrate.

- Does check-in trigger label printing?  
- Does RFID tag update the lab queue?  
- Does vitals submission alert the doctor?  

**UAT (User Acceptance Testing):**  
Testing by actual end-users (nurses, receptionists, lab techs).

- Can receptionist check in patients easily?  
- Can nurses enter vitals without confusion?  
- Can lab techs track samples with RFID?  

**Purpose:** Validate that the system meets real-world workflow needs.

---

## 8. Sample JIRA Board

**Columns:**

- To Do  
- In Progress  
- Review  
- Testing  
- Done  

**Usage:**  
User stories, acceptance criteria, and BPMN diagrams flow through the board to track progress and ensure visibility for all stakeholders.
