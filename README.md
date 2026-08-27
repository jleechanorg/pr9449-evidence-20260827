# PR #9449 evidence

Exact-head evidence for private `worldarchitect.ai` PR #9449 at
`04a08dd928a0c6a8bc6316990a9c927b92c6e238`.

The two complementary bundles prove distinct boundaries:

- [Real-server disconnect bundle](artifacts/pr9449-04a08dd9-disconnect-evidence.zip):
  the production local server and SSE route use a real AGY-backed LLM response;
  the client closes after exactly one narrative chunk; the canonical raw LLM
  response is present; and full Firestore story plus game state remain unchanged
  across 20 post-disconnect observations.
- [Gemini SDK deadline bundle](artifacts/pr9449-04a08dd9-provider-evidence.zip):
  a direct real Gemini SDK stream reaches the application deadline in 0.465s,
  within the 0.600s bound, with correlated authoritative BigQuery
  payload/event/latency rows. It proves bounded application termination and
  truthful cancellation telemetry. It does not claim provider cleanup or raw
  model-output capture when `cancellation_acknowledged=false`.

The current terminal recording shows the exact local and remote PR SHA, both
verdicts, canonical raw-response provenance, the one-chunk disconnect boundary,
matching full-state/full-story hashes, the skipped-persistence server log, and
checksum verification.

- [Inline GIF](media/pr9449_04a08dd9_PASS_disconnect_persistence.gif)
- [Direct MP4](media/pr9449_04a08dd9_PASS_disconnect_persistence.mp4)
- [Asciinema cast](media/pr9449_04a08dd9_PASS_disconnect_persistence.cast)
- [VTT captions](media/pr9449_04a08dd9_PASS_disconnect_persistence.vtt)

The older `f0e614a` files remain archived for historical comparison and are not
the current acceptance evidence.
