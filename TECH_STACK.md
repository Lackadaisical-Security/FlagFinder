# FlagFinder Tech Stack & Dependencies

## Language
- Node.js (TypeScript)

## Core Libraries
- **ML & NLP**: Hugging Face Transformers (via Python, called from Node), ONNX Runtime (optional for local inference)
- **Audio Transcription**: Whisper (OpenAI, via Python bindings)
- **OCR**: Playwright (for screenshot automation), Tesseract.js (OCR in Node)
- **Web/API**: Express (REST), Apollo Server (GraphQL)
- **UI**: HTML/JS (vanilla or React), Electron (optional for desktop)
- **CLI**: Commander.js or yargs
- **Testing**: Jest, Playwright (E2E)
- **Security**: crypto (Node.js), custom Lackadaisical stack
- **Other**: dotenv, winston (logging), multer (file uploads)

## Python (ML/Transcription)
- transformers, torch, scikit-learn
- openai-whisper
- fastapi (optional for ML microservice)

## DevOps
- Docker (optional)
- GitHub Actions (CI)

## Install Instructions
- Node.js >= 18
- Python >= 3.9
- `npm install` in root
- `pip install -r ml/requirements.txt`

---

See README.md for full setup and dependency details.
