# ☁️ Cloud Security Lab

Hands-on **AWS Cloud Security Lab** to simulate attacks, detect malicious activity, and practice incident response.  
This project demonstrates **Cloud + SOC skills** by combining Terraform (IaC), attack simulations, Splunk/Wazuh detections, and playbooks mapped to **MITRE ATT&CK**.

---

## 🔹 Objectives
- Build a secure & reproducible AWS environment using **Terraform**
- Simulate common **cloud attacks** (misconfigured S3, IAM privilege escalation, metadata exfiltration)
- Collect and analyze logs with **CloudTrail + Splunk/Wazuh**
- Write custom **detection rules & dashboards**
- Practice **incident response playbooks**

---

## 🔹 Architecture
Components:
- AWS VPC + EC2 (victim + bastion)
- S3 bucket (misconfiguration target)
- IAM roles/policies (privilege escalation demo)
- CloudTrail + CloudWatch for logging
- Splunk/Wazuh integration for detection

📌 Detailed diagram: [docs/architecture.md](docs/architecture.md)

---

## 🔹 Attack Scenarios
1. Misconfigured S3 bucket → data exfiltration
2. IAM over-permission → privilege escalation
3. EC2 metadata exploitation via SSRF
4. Suspicious login attempts from unusual geolocations

Steps: [docs/attack-scenarios.md](docs/attack-scenarios.md)

---

## 🔹 Detection Rules
- Alerts for new IAM user creation
- S3 bucket public access
- CloudTrail console login from unusual IP
- Suspicious EC2 instance metadata access

Queries: [docs/detection-rules.md](docs/detection-rules.md)

---

## 🔹 Incident Playbook
Sample response workflow:
- Investigate CloudTrail alerts
- Contain → revoke IAM keys, lock role
- Remediate → fix bucket policy, rotate credentials
- Report → document timeline, attacker TTPs

Guide: [docs/incident-playbook.md](docs/incident-playbook.md)

---

## 🔹 Tools Used
- **Terraform** (infra as code)
- **AWS CloudTrail / CloudWatch**
- **Splunk / Wazuh**
- **Velociraptor** (endpoint hunting)
- **Pacu** (AWS exploitation framework)
- **MITRE ATT&CK** mapping

---

## 📸 Screenshots
(coming soon – attacks, detections, dashboards)

---

## 🚀 Getting Started
1. Clone this repo:
   ```bash
   git clone https://github.com/loksharan-soc/cloud-security-lab.git
   cd cloud-security-lab/terraform
   ```
2. Configure AWS credentials with an IAM user (lab-only).
3. Deploy infrastructure:
   ```bash
   terraform init
   terraform apply
   ```
4. Run attacks and monitor detections.

⚠️ **Warning**: Only use in isolated AWS accounts. Never in production.

---

