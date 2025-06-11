**Created by [Lackadaisical Security](https://lackadaisical-security.com)**

**✅ Project Status: FULLY FUNCTIONAL** - Ready for production use!

## FlagFinder

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
- **Frontend**: Electron + React + Nightmare.js (UI control and automation)
- **Backend**: Node.js (analysis, plugins, crypto, storage)
- **ML/NLP**: ONNX Runtime, Hugging Face Transformers, Ollama LLM integration
- **Storage**: better-sqlite3 (sessions, audit log), encrypted vault
- **Build System**: TypeScript, Webpack, Babel

## Quick Start
1. `npm install`
2. `pip install -r ml/requirements.txt` (for training/ONNX export)
3. Choose your preferred launch method:
   - `npm run panel` (Nightmare.js controlled Electron - **RECOMMENDED**)
   - `npm start` (Standard Electron app)
   - `npm run web` (Web interface at http://localhost:3000)
4. (Optional) Train and export your own ONNX model, place in `/models/`

## Available Commands
```bash
npm run panel    # Launch with Nightmare.js control (recommended)
npm start        # Standard Electron application
npm run web      # Web server interface 
npm run build    # Build TypeScript files
npm run demo     # Build everything + launch panel
npm test         # Run test suites
```

## Testing Backend Components
```bash
node test_analysis.js   # Test analysis engine
node test_storage.js    # Test storage & crypto systems
```

## Current Status

**🎉 FULLY OPERATIONAL** - All systems working correctly:

- ✅ **Analysis Engine**: Rule-based + ML sentiment detection
- ✅ **UI Interface**: Nightmare.js controlled Electron panel  
- ✅ **Storage System**: Encrypted vault + SQLite audit logging
- ✅ **Privacy Architecture**: 100% local processing, no external calls
- ✅ **Plugin System**: Extensible architecture for text, audio, image, API feeds
- ✅ **Build Pipeline**: Complete TypeScript + Webpack + Babel toolchain

## Usage
- Import chat logs, analyze, and view flags in the timeline
- Use semantic search and RAG to generate LLM answers
- Visualize clusters and build custom LLM datasets
- All data is encrypted and auditable

## Documentation
- See `DOCUMENTATION.md` for full setup, plugin authoring, and API reference
- See `ML_PIPELINE.md` for ML training and ONNX export
- See `TESTING_QA.md` for testing and QA

## Developed By

**[Lackadaisical Security](https://lackadaisical-security.com)** - Privacy-focused security tools and research.

## License
See [LICENSE](LICENSE).

## Changelog
See [CHANGELOG.md](CHANGELOG.md).
