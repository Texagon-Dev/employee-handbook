---
layout: default
title: "On Call Policy"
nav_order: 13
---
# **On-Call Policy**

**Purpose and Scope**
This policy defines how we handle urgent issues in **production** and **staging** (where staging may affect customers).
As a services-based startup, we must minimize downtime, communicate clearly, and protect team wellbeing.
This document sets the **people on call**, **response timelines**, **communication rules**, **severity handling**, **post-incident documentation**, and **actions for non-compliance**.

---

## **1) Coverage**

- Applies to **every live project** in **production** or **staging** where customer or client impact is possible.
- Coverage is **24×7** for customer-impacting incidents.

## **2) On-Call Composition (per shift)**

- **1× Frontend Engineer**
- **1× Backend Engineer**
- **1× Team Lead** (incident coordinator and decision maker)
- **Product Manager (PM)** available during incidents to manage client communication.
- **If no Team Lead exists, the PM acts as TL** as defined in this policy.

## **3) Scheduling**

- The **PM** prepares and maintains the weekly on-call schedule.
- Each discipline has one assigned engineer per week, rotating fairly.
- Swaps must be updated in the schedule and announced in Slack **before** the shift starts.

## **4) Alerts & Communication**

- **Initial alert:** via **Slack and WhatsApp** to on-call members.
- **All coordination** happens in the project’s Slack channel.
- **PM** drafts all customer messages, which are approved by the **Team Lead** (or acting TL).

## **5) Response Targets**

- **Acknowledge alert within 10 minutes.**
- **Start work within 15 minutes after acknowledgement.**
- Post **concise, time-stamped updates** in Slack until mitigation or resolution.

## **6) Severity Levels & Update Cadence**

- **P0 (Critical):** Full outage, data loss, payments down, or security issue.

  - Immediate all-hands by on-call trio + PM.
  - Updates every **10–20 min**; client updates as needed.

- **P1 (High):** Major degradation or partial outage.

  - Prompt engagement by on-call team.
  - Updates every **15–30 min**; client updates as needed.

- **P2 / P3 (Moderate / Low):** Minor impact or visual issues.

  - **Acknowledge and confirm now.**
  - **Fix next working day.**

## **7) Standard Incident Flow**

1. Alert received → **acknowledge ≤10 minutes.**
2. **Team Lead (or PM as TL)** sets severity and directs response.
3. Engineers implement fix, rollback, or feature-flag change; verify recovery.
4. **PM** manages external comms after TL approval.
5. **PM** documents the incident — timeline, impact, actions, root cause, and follow-ups.

## **8) Wellbeing & Compensation**

- If an incident requires after-hours work, the responder may **arrive late the next day** (coordinate with manager).
- **Exception:** when the issue was caused by **clear developer fault**, no compensation applies.

## **9) Roles at a Glance**

- **Team Lead (or PM as TL):** sets severity, leads decision-making, approves customer comms.
- **Frontend/Backend Engineers:** triage, mitigate, fix, verify, and update.
- **PM:** owns schedule, manages clients, and writes the incident doc.

---

## **10) Failure to Comply & Disciplinary Action**

Every on-call member is expected to meet the response standards and responsibilities in this policy.
Failure to comply — including missed acknowledgments, delayed response, lack of communication, or negligence that extends customer impact — will lead to the following actions:

### **First Instance**

- **Written warning** from the Team Lead and PM.
- **No wellbeing compensation** (late arrival, rest time, or any on-call benefit) applies for next coming incident.

### **Second Instance**

- **Salary deduction** calculated **per hour** for the time the problem remains unresolved **or** for the duration the client bears losses — whichever is longer.
- The delay and loss will be logged in the incident record.

### **Third Instance**

- The engineer will be placed on a **Performance Improvement Plan (PIP)** for **1 month**, during which:

  - **Salary deductions** may continue,
  - **Work will be under closer review**, and
  - **Employment status** will be formally reviewed after the PIP period.

### **Severe Negligence**

Ignoring P0/P1 alerts, refusing to respond, or falsifying updates may result in **immediate escalation to management and HR**, and **termination without prior warnings** depending on severity.

---

### **Summary**

- **Ack ≤10 min; start ≤15 min after ack.**
- On-call team: **1 FE + 1 BE + 1 TL (PM if no TL)** + **PM** for client comms.
- **Slack** for coordination; alerts via **Slack + WhatsApp.**
- **P0:** update every 10–20 min | **P1:** 15–30 min | **P2/P3:** fix next day.
- **After-hours work → late arrival** (unless fault).
- **Failure to comply → written warning → pay deduction → PIP + review.**
