# Financial Fraud Detection & Live Automation Engine 💳🚨

An enterprise-grade financial intelligence workspace designed to ingest transaction pipelines, screen for anomalies against a robust fraud rule matrix, and initiate automated alerting infrastructure. This architecture pairs interactive visualization with a live automated operational command center.

---

## 🖥️ System Modules & Workspace Architecture

### 1. Executive Command Center
Consolidates real-time health metrics to provide immediate risk posture awareness for compliance officers and stakeholders.

<img width="1131" height="478" alt="executive-dashboard jpg" src="https://github.com/user-attachments/assets/0c6cc238-b6db-461e-8146-a6f3f7add735" />


* **Volume Processing Metrics:** Evaluates a total run of 55 transactions spanning a cumulative footprint of 1.78M INR.
* **Risk Tier Distribution:** Allocates system anomalies across 14 High Risk alerts, 15 Medium Risk alerts, and 11 Low Risk events.
* **Geographic & Merchant Concentrations:** Visualizes volume anomalies across key shipping locales (Foreign, Unknown, Mumbai, Delhi) alongside targeted transactional vectors (Wire Transfers and Electronics leading total exposures).

### 2. Fraud Deep Dive Workspace
Isolates anomalous actors and transaction identifiers to expedite active human-in-the-loop forensic assessments.

<img width="1189" height="475" alt="fraud-deep-dive jpg" src="https://github.com/user-attachments/assets/57a86c2b-f5fb-48a2-949b-855a4577ec37" />


* **Suspect Indexing:** Maps historical threat actions back to specific transactional identifiers (e.g., TXN001 to TXN015) alongside named profiles.
* **Financial Exposure Sorts:** Ranks individual threat actors dynamically based on cumulative capital outflows to capture high-velocity exploits immediately.

### 3. Rule Engine & Risk Analytics
Deconstructs raw inputs against explicit validation criteria to calculate multi-layered threat evaluation scores.

<img width="1171" height="475" alt="rule-engine jpg" src="https://github.com/user-attachments/assets/4ddd32d8-9fee-449e-9cec-f81e75f1caae" />


* **Average Risk Profile Weights:** Classifies calculated baseline indices where High Risk profiles heavily dictate anomalous activity clusters.
* **Core Risk Matrix Rules Catalog:**
  * `R11: UPI Abuse` & `R2: Round Amount` (High frequency anomalies)
  * `R1: High Value` & `R4: Velocity Breach` (Structural transaction constraints)
  * `R6: Off Hours` & `R7: Dormant Spike` (Temporal anomalies)

### 4. n8n Automation Engine Proof
Manages operational flow automation, directly converting rule validations into instantaneous system alerts.

<img width="1095" height="484" alt="automation-proof jpg" src="https://github.com/user-attachments/assets/bb1cabc1-dff9-48fc-b4de-3d3928e10e5c" />


* **Incident Automation Metrics:** Monitors live performance baselines showing an Average Risk Score of 2.04 across the pipeline.
* **Incident Alerting Integrations:** Validates communication logs showing 14 distinct Gmail alerts triggered and successfully transmitted to risk response queues.

---

## ⚙️ Technical Capabilities Architecture

* **Visual Ingestion Pipeline:** Streamlines multi-source banking spreadsheets directly into uniform presentation objects.
* **Automated Rule Evaluation:** Combines explicit heuristic logical statements (`Rules_Triggered`) with continuous numeric risk weighting variables.
* **n8n Orchestration Layer:** Creates instant notification pathways to keep information silos open between transaction layers and response teams.

---

## 🚀 Step-by-Step Deployment Guide

### Prerequisites
* BI visualization viewer or desktop container.
* An active instance of an **n8n orchestration workflow server** (Cloud or self-hosted Docker deployment).
* Connected email transfer relay service configuration (SMTP or native Google OAuth credentials).

### 1. Database & Dashboard Initialization
1. Import your raw financial ledger transactional arrays into your local workspace.
2. Link the file sources to establish clean relational connections across fields like `Transaction_ID`, `Fraud_Status`, and `Rules_Triggered`.

### 2. n8n Automation Setup
1. Open your native self-hosted n8n instance environment panel.
2. Select **Import from File** using the automation configuration file (`fraud_alert_workflow.json`) hosted in this repository root.
3. Configure your webhook parameters to trigger whenever a transaction row evaluates to `HIGH RISK` or logs a specific rule violation (such as `R11: UPI Abuse`).
4. Activate the workflow node to continuously monitor incoming traffic arrays.

---

## 📄 License
This architecture framework is shared openly under the terms of the MIT License. Review the enclosed `LICENSE` file for specific details.
