# FUNCTIONAL REQUIREMENTS DOCUMENT (FRD) + SYSTEMS REQUIREMENTS SPECIFICATION (SRS)

**Project:** OpenEMR Patient Scheduling & Clinical Workflow Modernization 
**Version:** Hybrid (BA + Technical Ops)  
**Author:** Brenda Garza  

---

## 1. Introduction

This FRD/SRS defines the functional behaviors, system interactions, and workflow rules for the new OpenEMR scheduling and clinical workflow system, including:

- Scheduling  
- Check-in  
- Vitals routing  
- Physician documentation  
- Lab workflow  
- Label printing  
- RFID tracking  

**Purpose:** Demonstrates requirements writing, systems analysis, configuration thinking, and hardware/software understanding

---

## 2. Scope

**Covered System Requirements:**

- Scheduling Module  
- Digital Check-in  
- Vitals Module  
- Clinical Routing / Status Tracking  
- Label Printing  
- RFID Tag Integration  
- Lab Workflow  
- Patient Portal Sync  
- Reporting / Dashboards  

**Not Covered:**

- Insurance billing  
- Pharmacy systems  
- Radiology systems

---

## 3. Functional Requirements

### 3.1 Scheduling Module

| ID    | Requirement |
|-------|------------|
| FR-01 | The system shall allow staff to create, edit, cancel, and reschedule appointments. |
| FR-02 | The system shall support appointment types (Consult, Follow-Up, Lab Only, Emergency). |
| FR-03 | The system shall display appointment availability in a shared calendar view. |
| FR-04 | The system shall send automated reminders (SMS/email). |

---

### 3.2 Digital Check-In

| ID    | Requirement |
|-------|------------|
| FR-05 | Patients shall check in via kiosk, receptionist tablet, or QR scan from phone. |
| FR-06 | Upon check-in, system shall create a visit ID, generate a barcoded wristband label, and log timestamp. |
| FR-07 | Kiosk shall support multilingual options. |

---

### 3.3 Vitals Module

| ID    | Requirement |
|-------|------------|
| FR-08 | Nurses shall record vitals digitally (height, weight, BP, pulse, temp). |
| FR-09 | Vitals shall automatically notify the physician that the patient is ready. |
| FR-10 | Vitals must be timestamped and attributed to the nurse who entered them. |

---

### 3.4 Clinical Routing / Status Tracking

| ID    | Requirement |
|-------|------------|
| FR-11 | System shall update patient status automatically: Checked-In → Vitals → With Doctor → Sent to Lab → Complete. |
| FR-12 | Staff shall see patient status in real time on a dashboard. |
| FR-13 | System shall alert staff when a patient has been waiting too long. |

---

### 3.5 Label Printing

| ID    | Requirement |
|-------|------------|
| FR-14 | System shall generate standardized labels using Zebra Designer or NiceLabel templates. |
| FR-15 | Labels shall include Patient name, Visit ID, Lab order ID, Barcode + human-readable text, and optional RFID tag number. |
| FR-16 | System shall detect printer availability and send jobs to backup printer if needed. |

---

### 3.6 RFID Tracking

| ID    | Requirement |
|-------|------------|
| FR-17 | System shall encode RFID tags for lab samples. |
| FR-18 | RFID readers shall track sample movement at checkpoints. |
| FR-19 | System shall log timestamp, location, user/technician, and sample ID. |
| FR-20 | If a sample has not moved within X minutes, system shall flag it as “Stalled.” |

---

### 3.7 Lab Workflow

| ID    | Requirement |
|-------|------------|
| FR-21 | Physician shall create lab orders within EMR. |
| FR-22 | System shall route lab orders to appropriate lab queues (Blood, Urine, Imaging). |
| FR-23 | Lab technicians shall scan barcode/RFID to begin workflow. |
| FR-24 | Results shall sync automatically to EMR chart and Patient Portal. |
| FR-25 | System shall track turnaround time for each test. |

---

### 3.8 Patient Portal

| ID    | Requirement |
|-------|------------|
| FR-26 | Patients shall view visit summaries, lab results, and doctor notes. |
| FR-27 | Portal shall send email notification when results are ready. |

---

## 4. Non-Functional Requirements (NFRs)

| Category             | Requirement |
|---------------------|-------------|
| Security             | System must be HIPAA compliant; data encrypted in transit and at rest. |
| Performance          | System must load dashboard in under 3 seconds. |
| Availability         | 99.9% uptime; planned maintenance after hours. |
| Scalability          | Must support increase to 5,000 users. |
| Usability            | UI must be accessible (WCAG standards). |
| Hardware Integration | Must support Zebra printers, RFID scanners. |

---

## 5. System Architecture Overview

**Systems Involved:**

- OpenEMR  
- Scheduling API  
- Label Printer Server  
- RFID Reader System  
- Patient Portal API  

**Data Sources:**

- Patient demographics  
- Visit records  
- Lab orders  
- RFID logs

---

## 6. Data Flow Diagrams (DFD)

**(To be built later in Lucidchart or Gliffy)**

**DFD Level 0 (Context Diagram)**

- Patient → Check-In System  
- Nurse → Vitals System  
- Physician → EMR  
- Lab Tech → RFID & Lab System  
- System → Patient Portal  

**DFD Level 1 (Check-In Process)**

1. Patient enters info  
2. System validates or creates visit ID  
3. Label printer generates barcode  
4. Vitals queue updated

---

## 7. BPMN Flowcharts

**Workflow:**

Start
↓
Check-In Task
↓
Vitals Task
↓
Doctor Consultation
↓
Lab Order (Decision)
• If Yes → Send to Lab
• If No → Complete Visit
↓
Lab Processing
↓
Results Uploaded
↓
End

---

## 8. User Stories (Agile)

| ID    | As a | I want | So that |
|-------|------|--------|--------|
| US-01 | Receptionist | Schedule patient appointments | I can manage daily clinic flow |
| US-02 | Patient     | Check in digitally            | My wait time is reduced |
| US-03 | Nurse       | Record vitals electronically | Doctor receives them instantly |
| US-04 | Lab Tech    | RFID tracking of samples     | No specimens are lost |
| US-05 | Physician   | Enter notes digitally        | They immediately update the patient chart |

---

## 9. Acceptance Criteria (BDD Format)

**Check-In**

Given I am a patient
When I scan my ID at kiosk
Then my visit should be created
And a wristband label should print

**RFID**

Given a lab sample is tagged
When it passes a checkpoint
Then the system should log its timestamp and location

**Vitals**

Given vitals are entered
When the nurse clicks submit
Then the doctor should be notified

---
