---
name: Corti ambient documentation (stream)
description: Stream a clinical encounter to Corti over WebSocket to receive live transcripts and extracted facts for ambient documentation.
api: asyncapi/corti-stream-asyncapi.json
operations: [sendConfiguration, sendAudio, sendEnd, receiveConfigStatus, receiveTranscript, receiveFacts, receiveUsage, receiveEnded, receiveError]
---

# Corti ambient documentation (stream)

Use the **Real-Time Ambient Documentation** WebSocket API to capture an encounter and receive both transcripts and structured clinical facts in real time.

## Auth
1. Get an OAuth token via `client_credentials`; for browser streaming request `scope="openid streams"`.
2. Open a `wss` connection to the `stream` channel on `api.{env}.corti.app` (env = `eu`, `us`, or `beta-eu`) with `Authorization: Bearer <token>`.

## Flow (verified operationIds)
1. **sendConfiguration** — send config after open. For fact extraction use `mode.type: "facts"` and supply a valid `mode.outputLocale` (BCP-47).
2. **receiveConfigStatus** — confirm the handshake succeeded (else inspect the `CONFIG_*` `reason`).
3. **sendAudio** — stream encounter audio.
4. **receiveTranscript** — consume live transcript segments.
5. **receiveFacts** — consume structured facts as they are extracted.
6. **sendEnd** — end the stream.
7. **receiveUsage** / **receiveEnded** — read usage and the final message, then close.

## Error rules
- Config problems: `CONFIG_DENIED` / `CONFIG_MISSING` / `CONFIG_TIMEOUT` with a `reason`.
- Runtime failures arrive via **receiveError**.
- See `errors/corti-error-codes.yml` and `conventions/corti-conventions.yml`.
