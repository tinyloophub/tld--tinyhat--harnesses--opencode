---
name: tinyhat-opencode
description: Pinned mirror of OpenCode, a provider-agnostic terminal agent harness.
license: MIT
metadata:
  tinyhat:
    harness:
      upstream_url: https://github.com/anomalyco/opencode
      upstream_ref: v1.14.28
      upstream_sha: acd8783a36d8642ade7038f34ca4f2f2ac3cc824
      system_repo_url: https://github.com/tinyloophub/tld--sys--tinyhat-harness-opencode
      sbom: ./sbom.spdx.json
      slsa_level: 1
      sandbox_tiers: [0, 1, 2]
      agent_skills_features:
        - progressive_disclosure
        - scripts
        - references
        - assets
      mcp_support: true
      otel_support: false
      owns_sandbox: false
      headless_driver: opencode CLI/API
      supported_providers:
        - anthropic
        - openai
        - google
        - openrouter
        - azure
        - bedrock
        - ollama
        - local
---

# tinyhat-opencode

Pinned mirror metadata for
[`anomalyco/opencode`](https://github.com/anomalyco/opencode), kept as
Tinyhat's multi-provider terminal-agent harness candidate.

OpenCode is a complete harness, not just an SDK: it provides a CLI,
client/server runtime shape, provider adapters, Agent Skills discovery,
subagent support, and MCP integration. Tinyhat owns the sandbox wrapper
around this harness, so `owns_sandbox` is false even though the harness
can run inside Tinyhat's sandbox tiers.

## What This Directory Is

This directory is the first-commit payload for
`github.com/tinyloophub/tld--sys--tinyhat-harness-opencode`. The admin
seed action creates/registers that repository and seeds it from this
directory. The upstream source tree is fetched into the system repo at
the pinned `v1.14.28` snapshot during vendoring.

## Vendor Compliance

Upstream is licensed MIT. Tinyhat-side modifications belong under
`patches/` as numbered patch files; the v1 mirror payload starts with
an empty patches directory.
