# PR #9449 evidence

Sanitized exact-head evidence for private `worldarchitect.ai` PR #9449 at
`f0e614a86144ef5fb8ba120c39d55b401ad62898`.

The two complementary bundles prove different boundaries:

- `artifacts/pr9449-f0e614a-disconnect-evidence.zip`: real local production
  server, real streaming LLM call, real SSE client disconnect, and unchanged
  persisted Firestore state across 20 post-disconnect observations.
- `artifacts/pr9449-f0e614a-provider-evidence.zip`: direct real Gemini SDK
  deadline plus correlated BigQuery payload/event/latency rows. It proves
  bounded consumer termination and truthful acknowledgement telemetry; it
  does not claim provider cleanup when `cancellation_acknowledged=false`.

The terminal recording shows exact Git provenance, PR HEAD, checksum
verification for both bundles, the real-server PID/cmdline, the passed
scenarios, unchanged state hashes, the server's skipped-persistence log line,
and matching pre/post SHAs.

- [Inline GIF](media/pr9449_f0e614a_PASS_disconnect_persistence.gif)
- [Direct MP4](media/pr9449_f0e614a_PASS_disconnect_persistence.mp4)
- [Asciinema cast](media/pr9449_f0e614a_PASS_disconnect_persistence.cast)
- [VTT captions](media/pr9449_f0e614a_PASS_disconnect_persistence.vtt)
