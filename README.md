# RAG in Legal Document

## Masalah
Legal document has many format

## Solusi
This application can take many format of legal documents (i.e. .docx, .pdf, .tiff)

## Diagram

```mermaid
flowchart TD
    A[Question] -->|Check Validity| B(Guardrail - llama-guard)
    B --> |Yes| C{RAG Type}
    C -->|Agentic| D[LangGraph-based flow]
    C -->|HyDE| E[LLM Hypothetical Answer]
    C -->|Retrieve-and-rerank| F[faiss]
    F --> G[Local Huggingface Model]
```

## Metrik

## Cara Menjalankan
