# GPT-2 Membership Inference Attack Demo

This repository contains the code, synthetic dataset, and instructions to reproduce the experiment described in the paper:

**"Privacy Risks in Local LLMs: A Practical Demonstration"**

## 📄 Summary

This project demonstrates how a local GPT-2 model can replicate sensitive data (e.g., Brazilian CPF numbers) inserted via prompts, even without fine-tuning or persistent memory. It simulates a Membership Inference Attack in a controlled development environment using a synthetic dataset.

---

## 📁 Repository Structure

```
.
├── main.py               # Script to run the experiment
├── clientes.db           # SQLite database with synthetic client data
├── requirements.txt      # Required Python packages
├── results/              # Folder for output logs and observations
└── README.md             # Project documentation
```

---

## ⚙️ Setup Instructions

1. **Clone the repository**
```bash
git clone https://github.com/your-user/gpt2-membership-inference.git
cd gpt2-membership-inference
```

2. **Create virtual environment (recommended)**
```bash
python3 -m venv venv
source venv/bin/activate  # or .\venv\Scripts\activate on Windows
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Experiment

```bash
python main.py
```

The script will:
- Load synthetic client data from `clientes.db`
- Generate prompts with CPFs
- Query the local GPT-2 model
- Print and save the model's response to assess memorization

---

## 🧪 Dataset

The database `clientes.db` contains synthetic records generated using the [Faker](https://faker.readthedocs.io/) library. Each record includes:
- Full name
- Email address
- Valid-format CPF number

No real personal data is used in this project.

---

## 🔒 Privacy and Ethics

This project is for **educational and research purposes only**. It uses fully synthetic data and does not involve any real personal information. The goal is to promote awareness of privacy risks when using LLMs in software development environments.

---

## ✅ Artifact Badges (Expected)

- ✔️ **Availability**: Code and data are fully public
- ✔️ **Functionality**: Scripts run and generate expected outputs
- ✔️ **Reproducibility**: Clear instructions provided
- ✔️ **Sustainability**: Structured repository with documentation

---

## 📅 Last updated

May 10, 2025
