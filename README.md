# Terminal-Based Digital Forensics Evidence Intake Tool

This project is a terminal-driven digital evidence intake system designed for digital forensics labs. Initially created using Bash on AWS EC2, it has since been rebuilt in Python for local execution, improving compatibility, maintainability, and cross-platform scalability. It uses the AWS SDK (`boto3`) to upload files securely to an S3 bucket.

---

## 🚀 Features

- Prompted case intake (case number, investigator, suspect, victim, crime type)
- Structured folder creation for digital evidence
- SHA256 hashing for evidence integrity
- Automatic upload of evidence and hash files to Amazon S3
- Runs entirely in the terminal using Python 3
- Cross-platform (Windows, macOS, Linux)

---

## 🛠️ Technologies Used

- Python 3.8+
- AWS S3 (for storage)
- `boto3` (AWS SDK for Python)
- `hashlib`, `os`, `getpass`, `boto3`

---

## 🧪 Sample Folder Structure

```
forensics/
└── case_001/
    ├── evidence/
    │   └── evidence.txt
    ├── hashes/
    │   └── evidence.sha256
    └── logs/
        └── case_info.txt
```

---

## 📦 Installation

1. **Clone this repo:**
   ```bash
   git clone https://github.com/yourusername/forensics-lab-intake.git
   cd forensics-lab-intake
   ```

2. **Install dependencies:**
   ```bash
   pip install boto3
   ```

3. **Set up your AWS credentials:**
   - Option 1 (recommended):
     ```bash
     aws configure
     ```
   - Option 2 (set env vars):
     ```bash
     set AWS_ACCESS_KEY_ID=your_access_key
     set AWS_SECRET_ACCESS_KEY=your_secret_key
     set AWS_DEFAULT_REGION=us-east-1
     ```

---

## ▶️ Usage

Run the script in the terminal:

```bash
python "PD Forensic Lab.py"
```

You will be prompted to enter:
- Case Number
- Investigator Name
- Victim Name
- Suspect Name
- Crime Type
- AWS Access Key & Secret (if not configured)

The script will:
- Create the folder structure
- Save the evidence file
- Create a SHA256 hash of the file
- Upload both files to the designated S3 bucket

---

## 🧠 Why Python Over Bash?

- **Cross-platform compatibility** (especially with Windows systems)
- **Easier to scale** into web apps or integrated forensic platforms
- **Cleaner, more readable code**
- Direct access to AWS services using `boto3`

---

## 🔐 Security & Best Practices

- Avoid hardcoding AWS credentials — use environment variables or IAM roles (if using EC2)
- SHA256 hashing ensures evidence integrity before upload
- Consider adding audit logging and logging to CloudTrail for production use

---

## 📈 Future Roadmap

- Build GUI using Flask or Tkinter
- Add database support (e.g. SQLite or DynamoDB) for indexing case metadata
- Chain-of-custody digital signing
- Full web dashboard for upload, search, and review

---

## 📷 Screenshots

> Insert screenshots here

- Terminal prompt for case input
- Folder structure after execution
- S3 bucket showing successful file upload

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

---

## 📄 License

MIT License

---

## 🙏 Acknowledgements

- Built as a proof-of-concept to modernize forensic evidence intake
- Guided by hands-on experimentation and mentorship from experienced engineers

---

## 🌐 Author

Jared Rollins — [LinkedIn Profile](https://www.linkedin.com/in/jared-r-71b71a233/)
