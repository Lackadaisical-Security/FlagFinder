# FlagFinder Security Considerations

## Local-Only Processing
- All chat analysis, ML inference, and storage are performed on-device.
- No data is sent to the cloud or third parties unless explicitly configured.

## Encryption
- All session and vault data is encrypted at rest using AES-GCM with random salt and HMAC for integrity (see `crypto/crypto.ts`).
- Passphrase-based encryption: user provides a passphrase for vault operations.

## Audit Logging
- All analysis, session, and vault operations are logged to a local SQLite database (`storage/sqlite.ts`).
- Audit logs include timestamp, event type, and details.

## Model & Plugin Security
- Only ONNX models in the `/models/` directory are loaded.
- Plugins must implement the `Plugin` interface and are loaded from trusted local code.

## LLM/RAG Security
- RAG/LLM completions are performed via a local Ollama service if available.
- No chat data is sent to external LLMs unless the user configures a remote endpoint.

## Recommendations
- Use strong, unique passphrases for vault encryption.
- Regularly review audit logs for suspicious activity.
- Only install plugins and models from trusted sources.

## Compliance
- FlagFinder is designed for privacy and local compliance, but users are responsible for their own data handling and legal requirements.

---

For more, see `DOCUMENTATION.md` and `crypto/crypto.ts`.
