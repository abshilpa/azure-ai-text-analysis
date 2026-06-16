# Azure AI Text Analytics — Hotel Review Analyzer 🏨🤖

A hands-on project built as part of the **Microsoft Learn: Develop AI Language and Speech Solutions on Azure** course. This application uses **Azure AI Language** to analyze hotel reviews — detecting language, extracting named entities, and redacting personally identifiable information (PII).

---

## 📌 Project Overview

Travel agencies receive hotel reviews in multiple languages from around the world. This application automates the process of:

- 🌍 **Detecting the language** each review is written in
- 🏷️ **Extracting named entities** such as people, places, dates, and addresses
- 🔒 **Redacting PII** (emails, names, addresses) before publishing reviews publicly

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python 3.13 | Programming language |
| Azure AI Language (Text Analytics) | NLP & text analysis |
| Azure AI Foundry | AI resource management |
| Azure CLI | Authentication & resource management |
| Git & GitHub | Version control |
| Visual Studio Code | Development environment |
| `azure-ai-textanalytics` SDK | Python SDK for Azure Language |
| `python-dotenv` | Environment variable management |

---

## 📂 Project Structure

```
text-analysis/
├── reviews/               # Sample hotel review text files
│   ├── review1.txt        # English review - London hotel
│   ├── review2.txt        # English review - London hotel
│   ├── review3.txt        # English review - San Francisco hotel
│   ├── review4.txt        # English review - San Francisco hotel
│   └── review5.txt        # French review - London hotel
├── .env                   # Azure credentials (not committed to GitHub)
├── requirements.txt       # Python dependencies
└── text-analysis.py       # Main application code
```

---

## ⚙️ Setup Instructions

### Prerequisites
Before running this project, make sure you have:

- ✅ An active **Azure subscription**
- ✅ **Python 3.13.x** installed
- ✅ **Git** installed and configured
- ✅ **Azure CLI** installed
- ✅ **Visual Studio Code** installed

---

### Step 1 — Clone the Repository
```bash
git clone https://github.com/microsoftlearning/mslearn-ai-language
cd mslearn-ai-language
```

### Step 2 — Navigate to the Exercise Folder
```bash
cd Labfiles/01-analyze-text/Python/text-analysis
```

### Step 3 — Create and Activate Virtual Environment
```bash
python -m venv .venv
.venv\Scripts\activate        # Windows
source .venv/bin/activate     # Mac/Linux
```

### Step 4 — Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 5 — Set Up Azure AI Language Resource
1. Go to [Azure Portal](https://portal.azure.com)
2. Create an **Azure AI Language** resource
3. Copy your **Endpoint** and **API Key**

### Step 6 — Configure Environment Variables
Create a `.env` file in the `text-analysis` folder:
```
FOUNDRY_ENDPOINT=https://your-resource.cognitiveservices.azure.com/
AI_SERVICE_KEY=your-api-key-here
```

### Step 7 — Login to Azure CLI
```bash
az login
```

### Step 8 — Run the Application
```bash
python text-analysis.py
```

---

## 📊 Sample Output

```
-------------
review1.txt

Good Hotel and staff
The Royal Hotel, London, UK ...

Language: English

Entities
    The Royal Hotel, London, UK (Address)
    Buckingham Palace (Location)
    Westminster Abbey (Location)
    alex@contoso.com (Email)

PII Entities
    alex@contoso.com (Email)

Redacted Text:
 Good Hotel and staff - Contact me at **************** for more details.

-------------
review5.txt

Un hôtel agréable
L'Hotel Buckingham, Londres, UK ...

Language: French
```
<img width="1357" height="891" alt="get language --french" src="https://github.com/user-attachments/assets/e5472e30-7015-472a-b565-6860bba68bc8" />

---
<img width="1336" height="936" alt="entites-1" src="https://github.com/user-attachments/assets/3e331ac4-8786-466d-8732-20e7656da6ef" />

---

<img width="1332" height="897" alt="reducted -pii output " src="https://github.com/user-attachments/assets/ebe1ac64-8aee-48e2-b926-83ff96382d99" />

---

<img width="1866" height="892" alt="lucky-ai --azure langunage " src="https://github.com/user-attachments/assets/8479c8dc-ea97-4ce2-a07c-c3be615896a2" />


---

## 🧠 What I Learned

- How to use the **Azure AI Language SDK** in Python
- Connecting to Azure services using **API Key authentication**
- **Language detection** across multiple languages (English, French, etc.)
- **Named Entity Recognition (NER)** — identifying locations, people, dates, emails
- **PII detection and redaction** for data privacy compliance
- Using **Azure CLI** for resource management and authentication
- Setting up Python **virtual environments** and managing dependencies
- Working with **Git** and **GitHub** for version control

---

## 🔐 Security Note

The `.env` file containing API keys is **not committed to GitHub**. It is listed in `.gitignore` to protect sensitive credentials.

---

## 📚 Reference

- [Microsoft Learn — Develop AI Language Solutions on Azure](https://learn.microsoft.com/en-us/training/)
- [Azure AI Language Documentation](https://learn.microsoft.com/en-us/azure/ai-services/language-service/)
- [Azure Text Analytics Python SDK](https://learn.microsoft.com/en-us/python/api/overview/azure/ai-textanalytics-readme)

---

## 👩‍💻 Author

**Shilpa** — Currently learning Azure AI Services and building hands-on projects to develop cloud AI skills.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://linkedin.com)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black)](https://github.com)

---

> 💡 *This project was completed as part of my Azure AI learning journey. I am actively building skills in cloud-based AI services, NLP, and Python development.*
