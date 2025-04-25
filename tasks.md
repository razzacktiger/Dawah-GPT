# DawahGPT Prototype Tasks

## Data Collection

- [ ] **T1**: Scrape Sapience Institute articles (HTML → text).
- [ ] **T2**: Download IERA Dawah PDFs and convert to text.
- [ ] **T3**: Extract YouTube transcripts via `youtube_transcript_api`.

## Data Preprocessing

- [ ] **T4**: Clean and dedupe raw text; remove boilerplate.
- [ ] **T5**: Chunk text into ~500-token segments with metadata.

## Embedding & Indexing

- [ ] **T6**: Generate embeddings for all chunks using OpenAI API.
- [ ] **T7**: Ingest embeddings into Pinecone vector store.

## Backend & RAG Pipeline

- [ ] **T8**: Prototype retrieval + prompt template in Jupyter.
- [ ] **T9**: Implement FastAPI endpoint `/chat` invoking LangChain RAG.

## Frontend

- [ ] **T10**: Build Streamlit chat UI (input box + history pane).
- [ ] **T11**: Connect UI to FastAPI `/chat` endpoint.

## Testing & Evaluation

- [ ] **T12**: Write unit tests for retrieval accuracy (recall@k).
- [ ] **T13**: Draft 20 sample Dawah Q&A pairs for human eval.
- [ ] **T14**: Conduct human rating sessions; collect scores.

## DevOps & Logging

- [ ] **T15**: Dockerize backend and vector store.
- [ ] **T16**: Set up basic Prometheus/Grafana for latency & usage.

## Demo & Documentation

- [ ] **T17**: Prepare demo script and slide deck.
- [ ] **T18**: Write README with setup & usage instructions.

## Future Backlog (Phase 2)

- [ ] **T19**: Design memory store for multi-turn context.
- [ ] **T20**: Research speech-to-text + TTS integration.
- [ ] **T21**: Plan multi-language translation pipeline.
