cloud-security-lab/

├─ terraform/                 # Infrastructure as Code

│  ├─ main.tf                 # AWS VPC, EC2, S3, IAM, CloudTrail

│  ├─ variables.tf            # Input variables (region, instance type, etc.)

│  └─ outputs.tf              # Useful outputs (EC2 IPs, bucket names)

│

├─ docs/                      

│  ├─ architecture.md         # Lab design + diagrams

│  ├─ attack-scenarios.md     # Step-by-step offensive exercises

│  ├─ detection-rules.md      # Queries (Splunk, Wazuh, Sigma)

│  └─ incident-playbook.md    # IR workflow + MITRE mapping

│

├─ detections/

│  ├─ splunk/                 # SPL queries \& dashboards

│  └─ wazuh/                  # Wazuh/Sigma rules

│

├─ scripts/                   # Helper scripts for attacks or setup

│  ├─ s3\_attack.sh            # Example: simulate misconfigured S3 access

│  └─ iam\_enum.py             # Example: privilege escalation checks

│

├─ images/                    # Diagrams + screenshots

│  ├─ architecture.png

│  ├─ attack-demo.png

│  └─ detection-dashboard.png

│

├─ .gitignore                 # Ignore Terraform state, AWS creds, etc.

├─ README.md                  # Main lab overview

└─ LICENSE                    # MIT or Apache license



