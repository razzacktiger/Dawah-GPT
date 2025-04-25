# DawahGPT Prototype Plan

## 1. Project Overview

We will build a “DawahGPT” prototype: a Retrieval-Augmented Generation (RAG) chatbot answering polemical and theological questions about Islam and other religions, trained on Sapience Institute, IERA, and related Dawah materials. :contentReference[oaicite:0]{index=0}

## 2. Objectives

- **Core Functionality**: Retrieve relevant Dawah content and generate faithful, context-aware answers. :contentReference[oaicite:1]{index=1}
- **Time-to-Prototype**: Deliver a working chat UI and backend within 1–2 weeks. :contentReference[oaicite:2]{index=2}
- **Quality Metrics**: Achieve ≥4/5 human ratings on faithfulness and clarity in initial tests. :contentReference[oaicite:3]{index=3}

## 3. Data Requirements

- **Sources**:
  - Sapience Institute articles (HTML/PDF). :contentReference[oaicite:4]{index=4}
  - IERA Dawah pamphlets and web-posts.
  - Transcripts from Dawah videos (YouTube). :contentReference[oaicite:5]{index=5}
- **Preprocessing**: Clean boilerplate, split into ~500-token chunks, attach metadata (source, date, URL). :contentReference[oaicite:6]{index=6}

## 4. Architecture

- **Vector Store**: Pinecone or Chroma for embedding index.
- **Embedding Model**: OpenAI Ada-style embeddings (or open-source equivalent).
- **LLM**: GPT-4 via OpenAI API (or Llama 2 fine-tuned).
- **Orchestration**: LangChain to chain retrieval → prompt templating → generation. :contentReference[oaicite:7]{index=7}
- **API Layer**: FastAPI endpoints for chat queries. :contentReference[oaicite:8]{index=8}
- **Frontend**: Streamlit or Next.js for minimal chat interface. :contentReference[oaicite:9]{index=9}

## 5. Non-Functional Requirements

- **Latency**: ≤1 s retrieval + ≤2 s LLM response per query. :contentReference[oaicite:10]{index=10}
- **Scalability**: Containerized via Docker for horizontal scaling. :contentReference[oaicite:11]{index=11}
- **Logging & Analytics**: Record queries, sources used, user feedback. :contentReference[oaicite:12]{index=12}

## 6. Evaluation Strategy

- **Automated**:
  - Retrieval recall@k for ground-truth Q&A pairs.
  - Hallucination rate via known-answer tests.
- **Human**:
  - Blind rating on faithfulness, clarity (1–5 scale). :contentReference[oaicite:13]{index=13}
  - Safety review to catch off-topic or inappropriate answers.

## 7. Success Criteria

- Prototype chat UI answering 20 sample Dawah questions with ≥4/5 average human score.
- System logs, metrics dashboard, and feedback loop in place.

## 8. Phase 2 Feature Roadmap

1. Conversation memory for follow-ups.
2. Voice I/O (speech-to-text + TTS).
3. Multi-language support (Arabic, Urdu, English).
4. Admin dashboard for source management.
5. In-app user feedback (thumbs up/down).
6. Quran API integration for auto-citing verses. :contentReference[oaicite:14]{index=14}
