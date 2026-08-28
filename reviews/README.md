# PR #9449 exact-head `/wa` review

Current-head delta reviewed through commit:
`d51c9127f82b1a9f650aec9a833db19fc9ee57c9`.

Both counted reviewers used real vendor browser UIs and received the same
lossless code packet plus both exact-head evidence ZIPs.

| Model | Final verdict | Confidence | Evidence |
|---|---|---|---|
| Grok | PREVIOUS APPROVAL REMAINS | high | [Vendor conversation](https://grok.com/c/0e497559-1dca-4545-a740-76b4a912aa1e?rid=7ca83af9-5c02-4aab-a60e-71d0b4d37fd0) · [response JSON](./pr9449-d51c9127-grok-wa.json) |
| Gemini | PREVIOUS APPROVAL REMAINS | high | [Response JSON](./pr9449-d51c9127-gemini-wa.json) · [browser screenshot](./pr9449-d51c9127-gemini-wa.png) |

Gemini initially invented paths, was challenged in the same attachment-backed
conversation, accepted the correction, and returned a grounded verdict citing
`mvp_site/main.py`, `mvp_site/llm_parser.py`,
`mvp_site/llm_providers/gemini_provider.py`, and `mvp_site/constants.py`.
The Workspace account does not expose Gemini's native Share action, so the
sanitized browser capture is published here instead.

Convergence: `2/4`, two different model families, both preserving the prior
`APPROVED with notes` verdict after reading the exact full merge delta.
This satisfies the `/wa` decision rule. ChatGPT remained blocked at its
network/Cloudflare interstitial, and Perplexity's authenticated Free account
required an upgrade for document uploads; neither was counted.
