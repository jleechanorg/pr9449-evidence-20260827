# PR #9449 evidence

Exact-head evidence for private `worldarchitect.ai` PR #9449 at
`72313a69e0c8938839e10d1c1b1966ef0206ed3c`.

The two current bundles prove complementary boundaries:

- [Real Gemini recovery bundle](artifacts/pr9449-72313a69-real-gemini-recovery-evidence.zip):
  `testing_mcp` exercises the production streaming route with
  `MOCK_SERVICES_MODE=false` and `gemini-3-flash-preview`. It passes 3/3
  scenarios and proves that an interrupted stream stores acknowledged prose as
  a typed draft without applying partial state, then resolves Continue and
  Retry exactly once. Replaying either resolution returns the persisted receipt
  without another state mutation.
- [Browser recovery bundle](artifacts/pr9449-72313a69-ui-recovery-evidence.zip):
  `testing_ui` passes 3/3 deterministic browser scenarios for reload followed by
  Continue, reload followed by Retry, and completed-receipt refresh. It proves
  the recovered-response UI and one-time canonical rendering. This browser
  layer uses intercepted backend responses; the real provider and Firestore
  claims come from the real Gemini bundle above.

Both bundles contain `verification_report.json` with `/er: PASS`, exact Git
provenance, and complete checksum manifests. The MCP bundle includes raw
SSE/provider request evidence and campaign snapshots. The UI bundle includes
the deterministic browser request ledger and captioned media. Independent
verification is recorded on PR #9449.

- [Inline UI GIF](media/pr9449_72313a69_PASS_recovery_ui.gif)
- [Direct UI MP4](media/pr9449_72313a69_PASS_recovery_ui.mp4)
- [VTT captions](media/pr9449_72313a69_PASS_recovery_ui.vtt)

Older evidence remains archived for historical comparison and is not the
current acceptance evidence.
