# DawahGPT Requirements

| User Story (As a…) | Requirements (Acceptance Criteria) | Tasks (see task.md IDs) |
|---|---|---|
| **1. End User** asks a question in chat so that they get a contextual Dawah answer. | - Chat input field accepts free text<br>- Response time ≤3 s (retrieval + LLM)<br>- Answer displays source citations with each paragraph | T9: Implement `/chat` endpoint in FastAPI<br> T10: Build Streamlit chat UI<br> T11: Wire UI→API integration |
| **2. Content Manager** ingests new Dawah documents so that the knowledge base stays current. | - Support PDF, HTML, and transcript inputs<br>- Metadata tagging (source, date, author) attached<br>- Duplicate detection in ingestion pipeline | T1: Scrape Sapience Institute articles<br> T2: Convert IERA PDFs to text<br> T3: Extract YouTube transcripts<br> T4: Clean & dedupe raw text |
| **3. QA Evaluator** rates answer faithfulness so that we can track quality. | - UI to record 1–5 faithfulness & clarity scores<br>- Ratings stored with question/answer logs<br>- Generate weekly QA summary report | T12: Unit tests for rating UI<br> T13: Prepare 20 sample Q&A for human eval |
| **4. DevOps Engineer** monitors performance so that SLAs are met. | - Instrument retrieval & LLM latency metrics<br>- Dashboard shows P95 latency, error rates<br>- Alert if latency >3 s or error rate >1% | T15: Dockerize services<br> T16: Set up Prometheus/Grafana |
| **5. Admin** manages prompt templates so that answer style can be tuned. | - Admin UI to CRUD prompt templates<br>- Version history of template changes<br>- Access control for admin role | T19: Design prompt-management UI<br> T20: Implement versioning API |
| **6. Returning User** maintains context across turns so conversation feels coherent. | - Session store holds last k exchanges<br>- Context window appended to retrieval prompt<br>- Configurable session timeout | T19: Design memory store schema<br> T21: Integrate context in RAG chain |
