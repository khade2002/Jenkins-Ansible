# Flask CI/CD with Jenkins and Ansible (Single EC2 Server)

This project demonstrates a basic CI/CD pipeline using **Jenkins** and **Ansible** to deploy a simple **Flask** web application. The entire setup runs on a **single Ubuntu EC2 instance**.

## 🚀 Tech Stack

- Python 3 + Flask 2.3.2
- Jenkins (CI)
- Ansible (CD)
- Ubuntu EC2 (single server)

---

## 📁 Project Structure
```
.
├── app/                  # Flask application code
│   ├── app.py
│   └── templates/
├── inventory.ini         # Ansible inventory file (contains EC2 IP)
├── deploy.yml            # Ansible playbook for provisioning & deployment
├── requirements.txt      # Python dependencies
├── deploy.sh             # Shell script to run Ansible (if used)
└── Jenkinsfile           # Jenkins pipeline script (optional)
```



## ⚙️ How It Works

1. **GitHub:** You push new changes to the Flask app.
2. **Jenkins:** Pulls the code, sets up Python virtual environment, installs packages.
3. **Ansible:** Connects to the EC2 instance via SSH and deploys the app.
4. **EC2:** Flask app is hosted and accessible via public IP.

## 🔧 Prerequisites

- AWS EC2 instance with:
  - Python 3 installed
  - SSH access enabled
- Jenkins installed and configured
- Ansible installed on Jenkins host
- Python virtual environment support

## 📦 Commands

Run the Ansible playbook:
```bash
ansible-playbook -i inventory.ini deploy.yml
'''

## 🧠 What I Learned
CI/CD pipeline automation

Infrastructure as Code with Ansible

Real-world deployment practices on cloud

Integration of DevOps tools for seamless delivery



