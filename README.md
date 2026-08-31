# PR #9449 evidence

Exact-head evidence for private `worldarchitect.ai` PR #9449 at
`2d7adea1300c21eed06b1915589ed3fd8c192adb`.

The two current bundles prove complementary boundaries:

- [Real AGY recovery bundle](artifacts/pr9449-2d7adea130-agy-recovery-evidence.zip):
  the mandatory-policy `testing_mcp` real-server route passes 3/3 scenarios.
  The client force-closes its SSE connection after one consumer-visible prose
  fragment (no terminal `done`); recovery transitions `404` to `200` as a typed
  `interrupted_draft`, with no forbidden gameplay fields. Continue and Retry
  each run through a fresh streaming turn and do not duplicate state. Raw
  provider records identify `agy_request` and `agy_response`; this is real AGY
  provider evidence, not a direct Gemini SDK claim.
- [Headed browser recovery bundle](artifacts/pr9449-2d7adea130-ui-recovery-evidence.zip):
  `testing_ui` passes 3/3 browser scenarios for reload/Continue, reload/Retry,
  and completed-receipt refresh. Its checksum-verified captioned MP4 visibly
  shows the recovered prose, non-authoritative warning, and both controls.
  The browser uses real local application assets but intercepts recovery/SSE
  network responses, so provider and Firestore claims belong only to the MCP
  bundle.

Both bundles contain exact Git provenance, verification reports, and complete
SHA-256 manifests. The MCP bundle also contains raw SSE/provider captures and
campaign snapshots. `/wa` and a direct Gemini-SDK/BQ claim are intentionally
not made by this evidence.

- [Inline UI GIF](media/pr9449_2d7adea130_PASS_recovery_ui.gif)
- [Direct UI MP4](media/pr9449_2d7adea130_PASS_recovery_ui.mp4)
- [VTT captions](media/pr9449_2d7adea130_PASS_recovery_ui.vtt)
- [Terminal capture](media/pr9449_2d7adea130_PASS_disconnect_persistence.cast)

Older evidence remains archived for historical comparison and is not the
current acceptance evidence.
