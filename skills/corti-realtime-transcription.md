---
name: Corti real-time speech-to-text (transcribe)
description: Open a real-time WebSocket to Corti and stream audio to receive live medical transcripts and detected commands using the stateless dictation API.
api: asyncapi/corti-transcribe-asyncapi.json
operations: [sendConfiguration, sendAudio, sendEnd, receiveConfigStatus, receiveTranscript, receiveCommand, receiveUsage, receiveEnded, receiveError]
---

# Corti real-time speech-to-text (transcribe)

Use the **Real-Time Stateless Dictation** WebSocket API to transcribe audio live. No interaction is created or stored; each connection is self-contained.

## Auth
1. Get an OAuth token via `client_credentials` at `https://auth.{env}.corti.app/realms/{tenant}/protocol/openid-connect/token`. For browser use, request a limited-scope token with `scope="openid transcribe"`.
2. Open a `wss` connection to the `transcribe` channel on `api.{env}.corti.app` (env = `eu`, `us`, or `beta-eu`). Send `Authorization: Bearer <token>`.

## Flow (verified operationIds)
1. **sendConfiguration** — immediately after the socket opens, send the config message (primary language as a BCP-47 tag, participant roles limited to `doctor`/`patient`/`multiple`, audio MIME type).
2. **receiveConfigStatus** — wait for the config acknowledgement. A `CONFIG_DENIED` / `CONFIG_MISSING` / `CONFIG_TIMEOUT` message means the handshake failed; read the `reason` field to fix it.
3. **sendAudio** — stream audio frames.
4. **receiveTranscript** — consume transcript messages as they arrive.
5. **receiveCommand** — consume any detected voice commands.
6. **sendEnd** — signal end of audio.
7. **receiveUsage** / **receiveEnded** — read usage and the final end message, then close.

## Error rules
- Handshake failures surface as `CONFIG_*` codes with a human-readable `reason`.
- Other failures arrive via **receiveError**.
- See `errors/corti-error-codes.yml` and `conventions/corti-conventions.yml`.
