# 🔍 Terminal-Based Digital Forensics Lab (AWS + Linux + Bash)

This project is a custom-built, cloud-based digital forensics lab designed to streamline and automate the intake, organization, hashing, and secure storage of digital evidence — all from the Linux terminal. No GUI. No mouse clicks. 100% terminal-driven.

Built to simulate real-world forensic workflows in environments that demand reliability, auditability, and scale.

---

## 🚀 Key Features

- ✅ Bash-based case intake & directory generation
- ✅ SHA256 hashing of all evidence files for integrity verification
- ✅ Timestamped chain-of-custody logs
- ✅ Secure uploads to Amazon S3 from the EC2 CLI
- ✅ Cloud-hosted on AWS EC2 (Amazon Linux 2023)
- ✅ IAM integration for permissioned, auditable AWS CLI usage
- ✅ Project structured and operated from the terminal — no GUI involved

---

## 🛠 Tools & Technologies

- **AWS EC2** – Linux instance for the terminal-based lab
- **Amazon S3** – Cloud storage for digital evidence files
- **AWS CLI** – Command line interface to interact with AWS from the server
- **IAM** – Secured access credentials for AWS automation
- **Bash** – Scripting language for automating forensic tasks
- **Linux file system** – For organizing case evidence and metadata
- **SHA256** – Used to hash and verify the integrity of all digital evidence

---

## 📁 Project Structure

Example case directory:

Each case folder is auto-generated via terminal prompts and includes:
- Evidence folder
- Hashes for each file (SHA256)
- Investigator info log (date, case number, crime type)
- Chain-of-custody records

---

## 🧪 Example Commands

```bash
# Create a new case from a script
./create_case.sh

# Hash a file
sha256sum ~/forensics/case_004/evidence/iphone_dump.txt > ~/forensics/case_004/hashes/iphone_dump.sha256

# Upload to S3
aws s3 cp ~/forensics/case_004/evidence/iphone_dump.txt s3://your-bucket-name/case_004/evidence/
