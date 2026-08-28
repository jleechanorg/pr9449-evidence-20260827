# PR #9449 exact-head `/wa` review

Reviewed commit: `5de277d3eabbbcc08a031f35ad8408c6b3371f92`.

Both counted reviewers used real vendor browser UIs and received the same
lossless code packet plus both exact-head evidence ZIPs.

| Model | Final verdict | Confidence | Evidence |
|---|---|---|---|
| Grok | APPROVED with notes | high | [Vendor conversation](https://grok.com/c/0e497559-1dca-4545-a740-76b4a912aa1e?rid=028a8e37-05b5-4323-ac48-aed248544ed2) |
| Gemini | APPROVED with notes | high | [Response JSON](./pr9449-5de277d3-gemini-wa.json) · [browser screenshot](./pr9449-5de277d3-gemini-wa.png) |

Gemini initially invented paths, was challenged in the same attachment-backed
conversation, accepted the correction, and returned a grounded verdict citing
`mvp_site/main.py`, `mvp_site/llm_parser.py`,
`mvp_site/llm_providers/gemini_provider.py`, and `mvp_site/constants.py`.
The Workspace account does not expose Gemini's native Share action, so the
sanitized browser capture is published here instead.

Convergence: `2/4`, two different model families, both `APPROVED with notes`.
This satisfies the `/wa` decision rule. ChatGPT remained blocked at its
network/Cloudflare interstitial, and Perplexity's authenticated Free account
required an upgrade for document uploads; neither was counted.
