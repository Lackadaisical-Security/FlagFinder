# FlagFinder

FlagFinder is a modular, privacy-first desktop tool for detecting social “flags” in conversations. It supports text, audio, image, and API feeds, and features a plugin-based architecture, hybrid rule/ML pipeline, semantic search, RAG (retrieval-augmented generation), and full local encryption and audit logging.

## Features
- **Transcript Import**: Paste or upload chat logs (text, JSON, audio, image)
- **Rule & ML Analysis**: Detects sentiment, question rate, and flag keywords
- **Visual Timeline**: Color-coded chat history (🟢 go, 🟡 caution, 🔴 stop)
- **Contextual Advice**: Per-message flag, reason, and suggested reply
- **Semantic Search & RAG**: Vector search and retrieval-augmented LLM answers
- **Custom LLM Training**: Build and export datasets for Ollama/LLM fine-tuning
- **Cluster Visualization**: 2D embedding/flag cluster view
- **Encrypted Storage**: AES-GCM + HMAC, with audit logging (better-sqlite3)
- **Local-Only Privacy**: All processing and storage is on-device

## Tech Stack
- **Frontend**: Electron + React (UI in `/ui/`)
- **Backend**: Node.js (analysis, plugins, crypto, storage)
- **ML/NLP**: ONNX Runtime, Hugging Face Transformers, Ollama LLM integration
- **Storage**: better-sqlite3 (sessions, audit log), encrypted vault

## Quick Start
1. `npm install`
2. `pip install -r ml/requirements.txt` (for training/ONNX export)
3. `npm start` (launch Electron app)
4. (Optional) Train and export your own ONNX model, place in `/models/`

## Usage
- Import chat logs, analyze, and view flags in the timeline
- Use semantic search and RAG to generate LLM answers
- Visualize clusters and build custom LLM datasets
- All data is encrypted and auditable

## Documentation
- See `DOCUMENTATION.md` for full setup, plugin authoring, and API reference
- See `ML_PIPELINE.md` for ML training and ONNX export
- See `TESTING_QA.md` for testing and QA

## License
See [LICENSE](LICENSE).

## Changelog
See [CHANGELOG.md](CHANGELOG.md).
