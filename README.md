# PDF-Based Knowledge Base RAG System — Guided Lab

## 1. Purpose

This is a guided, hands-on RAG project for participants to build a PDF-based Knowledge Base question-answering system.

The participant experience is intentionally simple:

**Open Google Colab → Open notebook → Type/copy code → Run → Validate output**

No participant-side setup is required.

## 2. Required RAG Architecture

PDF → PDF Loader → Fixed-Size Chunking → OpenAI Embeddings → ChromaDB → Retrieval → GPT-4o-mini → Answer

## 3. Technology Stack

- Python 3.10+
- LangChain
- PyPDF
- OpenAI GPT-4o-mini
- OpenAI text-embedding-3-small
- ChromaDB
- Google Colab


## 4. Files

- `Participant_PDF_RAG_Guided_Project.ipynb` — participant problem/task Google Colab notebook
- `04_DATA/sample_knowledge_base.pdf` — supplied PDF


## 5. Guided Tasks

### Task 1
Load and inspect the PDF.

### Task 2
Split the document using:
- chunk size = 1000
- chunk overlap = 200

### Task 3
Generate embeddings using `text-embedding-3-small`, store them in ChromaDB, and test similarity retrieval.

### Task 4
Build the RAG QA pipeline using GPT-4o-mini.

### Task 5
Combine the components into an interactive RAG application.

## 6. Validation

Participants should test:
1. A question answered by the PDF.
2. A second question from another section.
3. An out-of-context question.

The system should not invent an answer when the answer cannot be found in the supplied context.