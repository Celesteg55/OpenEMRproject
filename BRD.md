# 📄 Business Requirements Document (BRD)
**Project:** OpenEMR Patient Scheduling & Clinical Workflow Modernization  
**Version:** Hybrid (BA + Technical Workflow)  
**Author:** Brenda Garza  
**Date:** 2025

---

## 1. Executive Summary
The clinic’s current appointment and patient workflow system relies on manual check-ins, printed labels, inconsistent communication between staff, and outdated software tools.  
This causes long wait times, duplicated tasks, errors in routing patients, and lack of visibility into patient status.

This project aims to digitize and streamline patient scheduling, check-in, vitals routing, doctor consultations, lab orders, and patient portal updates.  
It also introduces barcoded labels, RFID tagging for tracking lab specimens, and standardized digital workflows.  

**Outcome:** Reduce process waste, improve accuracy, and increase staff productivity—aligning with modern healthcare operations and supporting Leidos’ mission-driven technical environments.

---

## 2. Business Objectives

### Primary Objectives
1. Reduce patient wait times and bottlenecks  
2. Provide real-time visibility into patient location/status  
3. Standardize scheduling and lab order workflows  
4. Reduce manual errors through digital labels and RFID  
5. Improve data accuracy and compliance  

### Secondary Objectives
6. Improve communication between reception, nurses, physicians, and lab staff  
7. Reduce rework caused by lost paperwork  
8. Create a foundation for future system integrations  

---

## 3. Current State Analysis (“As-Is”)

**Scheduling**
- Staff use spreadsheets and email  
- No unified calendar  
- Double-booking occurs  

**Check-in**
- Manual sign-in sheet  
- Patients wait long periods before being called  
- No real-time queue management  

**Vitals & Routing**
- Paper sheets physically carried between rooms  
- Nurses cannot see patient status at a glance  

**Doctor Notes**
- Some digital, some handwritten  
- No structured workflow  

**Lab Orders**
- Printed labels inconsistent  
- Lab samples sometimes misrouted  
- RFID not used to track movement  

**Communication**
- Staff rely on verbal updates, sticky notes, phone calls  

---

## 4. Future State (“To-Be”) Recommendations

**Digital Scheduling Platform**
- One shared system  
- Automated appointment reminders  
- Color-coded appointment types  

**Kiosk / Reception Check-in**
- Automated label printing  
- Barcoded patient wristbands  
- Queue system showing wait times  

**Vitals Module**
- Nurses enter vitals directly into system  
- Doctors notified automatically  

**Clinical Routing**
- Real-time patient status: Checked-In → Vitals → With Doctor → Lab → Complete  

**Lab Workflow Improvements**
- RFID-tagged lab samples  
- Zebra Designer / NiceLabel standard templates  
- Automated notifications when lab results complete  

**Patient Portal**
- Immediate access to notes and results  

---

## 5. Business Requirements

| ID     | Requirement |
|--------|-------------|
| BR-01  | The system shall allow patients to check in digitally or at reception. |
| BR-02  | The system shall automatically generate barcoded labels. |
| BR-03  | The scheduling module shall support appointment types and durations. |
| BR-04  | Nurses shall be able to enter vitals electronically. |
| BR-05  | Physicians shall view patient information in real time. |
| BR-06  | The system shall route patients between departments automatically. |
| BR-07  | Lab samples shall be tracked using RFID tags. |
| BR-08  | Staff shall receive system notifications for status changes. |
| BR-09  | Patient records shall sync to the portal after visit completion. |
| BR-10  | System shall support change logging for audit and compliance. |

---

## 6. Assumptions & Constraints

### Assumptions
- Staff can be trained on new tools  
- Wi-Fi and hardware support is available  
- EMR supports API integrations  

### Constraints
- HIPAA compliance  
- Budget limits for hardware (RFID scanners, label printers)  
- Limited on-site IT support  

---

## 7. Risks & Mitigation

| Risk                       | Impact | Mitigation |
|-----------------------------|--------|------------|
| Staff resistance to new tech| Medium | Training & pilot rollout |
| Hardware failure            | High   | Redundant label printers |
| Incorrect label templates   | Medium | QA testing using NiceLabel/Zebra |
| Workflow confusion          | High   | BPMN training |

---

## 8. Success Criteria
- 25% reduction in patient wait times  
- 40% reduction in manual scheduling errors  
- 100% adoption of digital routing  
- 90% accuracy in lab sample RFID tracking  
- Improved patient satisfaction scores
