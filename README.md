# Azure AI Language Text Analysis Application

## Overview

This project demonstrates how to use **Azure AI Language Service** and the **Azure AI Foundry SDK** to perform advanced text analytics on hotel review documents.

The application processes text files containing customer reviews and performs the following Natural Language Processing (NLP) tasks:

* Language Detection
* Named Entity Recognition (NER)
* Personally Identifiable Information (PII) Detection
* PII Redaction

The project is built using Python and the Azure AI Text Analytics SDK.

---

## Features

### Language Detection

Automatically identifies the language used in each review document.

Example:

Input:

```text
Bonjour, cet hôtel était magnifique.
```

Output:

```text
Language: French
```

### Named Entity Recognition (NER)

Extracts important entities from text such as:

* People
* Locations
* Organizations
* Dates
* Events

Example:

Input:

```text
Satya Nadella visited London.
```

Output:

```text
Satya Nadella (Person)
London (Location)
```

### Personally Identifiable Information (PII) Detection

Detects sensitive information including:

* Names
* Phone Numbers
* Email Addresses
* Addresses
* Financial Information

### PII Redaction

Automatically masks sensitive information before publication or storage.

Example:

Input:

```text
John Smith lives at 123 Main Street.
```

Output:

```text
********** lives at *************
```

---

## Technologies Used

* Python 3.13
* Azure AI Language Service
* Azure AI Foundry
* Azure Identity SDK
* Azure Text Analytics SDK
* Visual Studio Code
* Azure CLI

---

## Project Structure

```text
text-analysis/
│
├── reviews/
│   ├── review1.txt
│   ├── review2.txt
│   └── review3.txt
│
├── text-analysis.py
├── requirements.txt
├── .env
└── README.md
```

---

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/azure-ai-text-analysis.git
cd azure-ai-text-analysis
```

### 2. Create Virtual Environment

```bash
python -m venv .venv
```

Activate the environment:

Windows

```bash
.venv\Scripts\activate
```

Mac/Linux

```bash
source .venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file:

```env
PROJECT_ENDPOINT=https://your-foundry-resource.services.ai.azure.com
```

---

## Azure Authentication

Login to Azure:

```bash
az login
```

The application uses:

```python
DefaultAzureCredential()
```

to securely authenticate with Azure AI services.

---

## Running the Application

```bash
python text-analysis.py
```

---

## Sample Output

```text
Review:
The hotel was amazing and located near London Bridge.

Language:
English

Entities:
London Bridge (Location)

PII Entities:
John Smith (Person)

Redacted Text:
********** stayed at the hotel.
```

---

## Learning Outcomes

Through this project, I gained hands-on experience with:

* Azure AI Language Service
* Azure AI Foundry
* NLP Pipelines
* Entity Recognition
* PII Detection and Redaction
* Azure SDK Authentication
* Cloud-based AI Development

---

## Future Improvements

* Sentiment Analysis
* Key Phrase Extraction
* Multi-document Processing
* Batch Inference
* REST API Deployment using FastAPI
* Integration with Azure OpenAI
* RAG-based Document Analysis

---

## Certification Alignment

This project supports preparation for:

**Microsoft Azure AI Engineer Associate (AI-102)**

Relevant skills covered:

* Analyze Text with Azure AI Language
* Build NLP Solutions
* Authenticate Azure Resources
* Process and Secure Text Data
* Develop AI Applications using Azure SDKs

---

## Author

**Shilpa Abbugari**

MSc Data Science | AI Engineer | Machine Learning Enthusiast

Currently building practical Azure AI, Generative AI, and Machine Learning projects to strengthen AI Engineering skills and prepare for industry roles.
