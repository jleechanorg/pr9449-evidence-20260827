# PR #9449 evidence

Exact-head evidence for private `worldarchitect.ai` PR #9449 at
`d51c9127f82b1a9f650aec9a833db19fc9ee57c9`.

The two complementary bundles prove distinct boundaries:

- [Real-server disconnect bundle](artifacts/pr9449-d51c9127-disconnect-evidence.zip):
  the production local server and SSE route use a real AGY-backed LLM response;
  the client closes after exactly one narrative chunk; the canonical raw LLM
  response is present; and full Firestore story plus game state remain unchanged
  across 20 post-disconnect observations.
- [Gemini SDK deadline bundle](artifacts/pr9449-d51c9127-provider-evidence.zip):
  a direct real Gemini SDK stream reaches the application deadline in 0.465s,
  within the 0.600s bound, with correlated authoritative BigQuery
  payload/event/latency rows. It proves bounded application termination and
  truthful cancellation telemetry. It does not claim provider cleanup or raw
  model-output capture when `cancellation_acknowledged=false`.

The fresh disconnect run passed 2/2 scenarios with one canonical narrative
chunk, no terminal `done`, and unchanged full Firestore story plus game state
across all 20 observations. The fresh provider verifier passed every required
claim and all bundle checksums at the same exact HEAD.

- [Inline GIF](media/pr9449_d51c9127_PASS_disconnect_persistence.gif)
- [Direct MP4](media/pr9449_d51c9127_PASS_disconnect_persistence.mp4)
- [Asciinema cast](media/pr9449_d51c9127_PASS_disconnect_persistence.cast)
- [VTT captions](media/pr9449_d51c9127_PASS_disconnect_persistence.vtt)

The older `5de277d3`, `f0e614a`, and `04a08dd9` files remain archived for
historical comparison and are not the current acceptance evidence.
