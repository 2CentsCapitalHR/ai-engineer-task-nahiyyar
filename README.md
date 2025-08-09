# ADGM RAG Corporate Agent

An **AI-powered ADGM-compliant Corporate Agent** prototype that:

- Accepts **.docx** legal documents.
- Detects document type and legal process (e.g., Company Incorporation).
- Verifies uploaded documents against **mandatory ADGM checklist**.
- Uses **Retrieval-Augmented Generation (RAG)** with official ADGM rules to:
  - Detect legal red flags.
  - Insert contextual comments & highlights in the document.
- Outputs:
  - Reviewed `.docx` with highlights & inline comments.
  - Structured JSON report summarising findings, missing documents, and recommendations.

---

## 🚀 Features

- **Document Upload & Parsing**: Accepts one or multiple `.docx` files.
- **Document Type Detection**: Keyword-based classification into ADGM categories.
- **Checklist Verification**: Compares uploaded files against required ADGM checklist for the detected process.
- **RAG Compliance Check**:
  - Retrieves relevant ADGM legal clauses from provided reference docs.
  - Uses an LLM to analyse each paragraph for compliance issues.
- **Red Flag Detection**: Finds missing clauses, wrong jurisdiction, ambiguous wording, missing signatures, and ADGM template non-compliance.
- **Inline Commenting**:
  - Highlights flagged paragraphs in yellow.
  - Adds bracketed inline comments with reasons & recommendations.
- **JSON Output**:
  - Includes process name, document counts, missing documents, and detailed issue list.

---

## 📂 Folder Structure

project/
│── adgm_rag_agent.py # Main script
│── adgm_refs/ # ADGM reference documents (PDF, DOCX, TXT)
│── requirements.txt # Python dependencies
│── README.md # This file


---

## ⚙️ Installation

### 1 Clone the Repository

```bash
git clone https://github.com/your-username/adgm-rag-agent.git
cd adgm-rag-agent
```
### 2 Install dependencies

```bash
pip install -r requirements.txt
```

### 3 Add ADGM Reference Documents

```bash
./adgm_refs/
```

### 4 Run the app

```bash
python adgm_rag_agent.py
```


