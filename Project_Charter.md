Project Charter: Vehicle Security Operations Center (VSOC) Platform

1. Project Information

Field	Details
Project Name	Vehicle Security Operations Center (VSOC) Platform
Project Sponsor	M.D (CEO)
Product Manager	Priya
Project Start Date	Q3 2026 (TBD)
Target Completion	~18 Months From Start Date 
Document Version	v1.0

2. Project Purpose
Connected and autonomous vehicles generate vast amounts of telemetry data and are increasingly vulnerable to remote cyber exploits. Fleet operators require a centralized platform to monitor, detect, analyze, and respond to security incidents in real time while meeting strict international regulations.
The purpose of this project is to develop a cloud-based Vehicle Security Operations Center (VSOC) that provides continuous automated threat detection and response, executive and technical reporting, and secure immutable data pipelines for connected vehicle fleets.

3. Business Need
Current vehicle fleet cybersecurity solutions often lack:
	Real-time threat visibility: Delays in processing batch telemetry leave zero-day exploits active for too long.
	Automated incident response: Manual interventions fail to prevent cascading vehicle safety failures while on the road.
	Centralized fleet monitoring: Fragmented vehicle logs prevent cross-fleet attack correlation.
	Compliance reporting: Inability to easily provide vehicle forensic data for UNECE R155/R156 and ISO/SAE 21434 auditing.

4. Project Objectives
	Platform Delivery: Build a cloud-native VSOC platform tailored to autonomous fleet architectures.
	High-Throughput Ingestion: Real-time ingestion and parsing of CAN bus, telematics, and V2X logs.
	Ultra-Low Latency: Detect cybersecurity threats and compute anomalies within sub-second thresholds.
	Fail-Safe Automation: Orchestrate real-time responses to isolate network nodes without overriding physical vehicle safety controls.
	Regulatory Assurance: Ensure 100% compliance with automotive cybersecurity standards and global driver data privacy laws (GDPR/CCPA).

5. Project Scope
In Scope
	Secure cloud data ingestion endpoints (TLS mutual authentication).
	Real-time monitoring dashboard with tiered role-based access control (RBAC).
	Automated incident response playbook execution engine.
	Immutable audit trail logs for forensic compliance.
	Automated generation of technical and executive compliance reports.

Out of Scope
	Vehicle hardware/sensor development or manufacturing.
	Vehicle firmware compilation (the VSOC detects and triggers, but does not compile software patches).
	Physical vehicle security (anti-theft hardware).
	Insurance claims or general fleet maintenance scheduling.

6. Project Deliverables
	Cloud-Native VSOC Platform Engine (Kafka/Stream processing cluster).
	Web-Based Fleet Monitoring Dashboard (Analyst Alert Triage Interface).
	Automated Response Playbook Orchestrator (Vehicle Cloud Commands API).
	Immutable Auditing Ledger Infrastructure (Compliant long-term storage).
	Automated Report Generation Module (Executive PDF / Technical JSON).

7. Success Criteria
	Detection Latency: Real-time threat detection alert triggered within ≤5 seconds of event ingestion.
	Pipeline Lag: Telemetry ingestion to cloud parsing completed in <50"ms" .
	Platform Availability: 99.99% uptime across multi-region cloud deployments.
	Regulatory Certification: Successful dry-run pass of an ISO/SAE 21434 compliance audit.

8. High-Level Requirements
Functional Requirements
	Data Isolation: Real-time collection and correlation of vehicle telemetry data.
	Dynamic Alerting: Severity scoring (Critical, High, Medium, Low) for detected threats.
	Isolation Playbooks: Automated trigger execution to safely quarantine compromised vehicle cloud nodes.

Non-Functional Requirements
	Scalability: Horizontally scale ingestion to handle up to 10,000 concurrent streaming vehicle payloads.
	Security: End-to-end data encryption (AES-256 at rest, TLS 1.3 in transit).
	Data Immutability: Audit trails must use write-once-read-many (WORM) storage properties to prevent tampering.

9. Assumptions & Constraints
	Assumptions:
     Vehicles possess an active telematics control unit (TCU) capable of sending streaming JSON/Protobuf outputs. Security analysts will be available to train the anomaly models during development.

    Constraints: 
    Fixed 7-month deadline to hit the pilot demonstration milestone; strict compliance boundaries where an automated response must never conflict with physical functional vehicle safety laws.

10. High-Level Project Timeline
YEAR 1: Core Platform & Regulatory Hardening
 ├─ Q1 (PI-1): Ingestion Infrastructure & Telemetry Parsing
 ├─ Q2 (PI-2): Real-Time Analytics Engine & Analyst Triage UI
 ├─ Q3 (PI-3): Semi-Automated Playbooks & UNECE Audit Compliance
 └─ Q4 (PI-4): Scale Hardening, High-Throughput Fuzzing & Pilot Launch

 YEAR 2: Advanced Automation & Enterprise Multi-Tenancy
 ├─ Q1 (PI-5): Enterprise Multi-Tenancy & Fleet Segmentation
 ├─ Q2 (PI-6): Machine Learning Behavioral Anomaly Detection
 ├─ Q3 (PI-7): Closed-Loop Automated Safe-State Vehicle Mitigation
 └─ Q4 (PI-8): Global Edge-Cloud Synchronization & Full Commercial SOP


11. Project Budget (High-Level Rough Estimation)
 
The operational run-rate below covers the direct core engineering team, 24/7 Security Operations Center personnel (SOC Analysts), Legal/Compliance overhead, Product Management, and Sales Engineering to support client onboarding.

1. Total 2-Year Capital Expenditure Summary
Department / Cost Category	Year 1 Allocation	Year 2 Allocation	2-Year Total	% of Budget
1. Engineering & Architecture
$660,000	$710,000	$1,370,000	32.7%
2. Security Operations (SOC)
$320,000	$460,000	$780,000	18.6%
3. Cloud Infrastructure & DevOps
$189,000	$280,000	$469,000	11.2%
4. Product Management & UX
$218,000	$240,000	$458,000	10.9%
5. Legal, GRC, & Compliance
$165,000	$150,000	$315,000	7.5%
6. Sales Engineering & GTM Support
$110,000	$175,000	$285,000	6.8%
Operational Contingency (13%)	$233,000	$284,000	$517,000	12.3%
TOTAL ESTIMATED CAPEX	$1,895,000	$2,299,000	$4,194,000	100%
Departmental Cost Breakdowns
1. Engineering & Architecture Department
Responsible for designing the high-velocity streaming pipelines, data schema parsers, and API connections to the vehicles.
•	Note: Staffing increases in Year 2 to support AI/ML anomaly detection models.
Role	Yr 1 Count	Yr 2 Count	Fully Loaded Annual Rate	2-Year Total
Principal Cloud & Data Architect	1	1	$240,000	$480,000
Senior Data/Backend Engineers	2	2	$192,000	$768,000
Machine Learning Engineer	0	1	$195,000	$195,000
Total Department Cost	3	4	—	$1,370,000
2. Security Operations (SOC) Department
The primary user base. Analysts perform tiering, log forensics, and playbook management. Year 2 introduces a split shift for 24/7 global support.
Role	Yr 1 Count	Yr 2 Count	Fully Loaded Annual Rate	2-Year Total
Senior Security & Incident Engineer	1	1	$180,000	$360,000
SOC Security Analysts (T1 / T2)	1	3	$110,000	$420,000
Total Department Cost	2	4	—	$780,000
3. Cloud Infrastructure & IT Operations
Cloud consumption, third-party SIEM tooling, penetration testing software, and streaming storage accounts. Costs scale as real-time vehicle loads double in Year 2.
Item Description	Year 1 Cost	Year 2 Cost	2-Year Total
Cloud Ingestion & Compute (AWS/GCP Cluster)	$144,000	$220,000	$364,000
Security Tooling & Vulnerability Scanners	$45,000	$60,000	$105,000
Total Department Cost	$189,000	$280,000	$469,000
4. Product Management & UX Design
You (owning the vision, roadmap, and requirements mapping) along with front-end resources executing user-centered dashboard designs.
Role	Yr 1 Count	Yr 2 Count	Fully Loaded Annual Rate	2-Year Total
Product Manager (You)	1	1	$168,000	$336,000
UI/UX Frontend Contractor	1	1 (Part-Time)	$122,000	$122,000
Total Department Cost	2	2	—	$458,000
5. Legal, Governance, Risk, & Compliance (GRC)
Bakes in multi-region data auditing rules, privacy management frameworks (GDPR/CCPA), and official certification steps for international vehicle compliance. 
Item / Role Description	Year 1 Cost	Year 2 Cost	2-Year Total
Internal Compliance & Risk Analyst	$125,000	$130,000	$255,000
External Regulatory Auditing Fees (ISO 21434)	$40,000	$20,000	$60,000
Total Department Cost	$165,000	$150,000	$315,000
6. Sales Engineering & Go-To-Market (GTM) Support
Technical staff needed to interface directly with B2B clients, configure custom cloud telemetry endpoints, and run pilot presentations for prospective commercial vehicle fleets.
Role	Yr 1 Count	Yr 2 Count	Fully Loaded Annual Rate	2-Year Total
Senior Sales Engineer	1	1	$155,000	$245,000
Customer Training Support	0	1 (Part-Time)	$40,000	$40,000
Total Department Cost	1	2	—	$285,000

