# Guide Neuromedia-Repowise

> Français localisation. The canonical Russian product introduction is [README.md](../README.md); this localisation preserves the same provenance, AGPL obligations, safety boundary, and limitation statements.


## Scope and provenance

Neuromedia-Repowise is a Russian-first derivative distribution of the upstream Repowise project. It is not an independently authored replacement, and it does not claim upstream endorsement or support. The complete original technical landing document is preserved at [UPSTREAM_README.md](UPSTREAM_README.md); the upstream documentation remains in this repository. The exact source revision, source URL, licence, modification statement, and non-endorsement notice are recorded in [ATTRIBUTION.md](../ATTRIBUTION.md).

The source code is licensed under GNU AGPL-3.0-or-later. That licence permits copying, studying, modifying, and distributing the work under its conditions. If a modified version is offered to users over a network, the operator must provide the corresponding source of that modified version to those users. Retain licence and copyright notices. This practical note is not legal advice; review the complete [LICENSE](../LICENSE) and obtain legal advice when needed.

## Purpose

Repowise builds a local evidence-backed index of a repository: source structure, symbol and dependency graph, Git history, tests, documentation, and recorded architecture decisions. Its CLI, local dashboard, and MCP interface can help developers and authorised AI-agent workflows answer questions such as which code calls a symbol, what a change may affect, which tests are relevant, and where maintainability or defect-risk signals concentrate. A computed result is evidence to review, not a warranty, an automated approval, or a substitute for engineering judgment.

The core analysis can run without an API key. Some optional prose or model-related functions may involve a configured provider. Before enabling any such feature, verify data handling, access rights, provider terms, and the organisation's privacy and security policy. Do not assume that local indexing makes every workflow safe: repositories can contain confidential material and access must remain authorised.

## Installation and use

Use the upstream technical documentation as the authoritative reference for supported platforms, prerequisites, deployment methods, configuration, CLI commands, architecture, MCP clients, and troubleshooting. A minimal authorised-repository workflow is:

```bash
pip install repowise
cd /path/to/an-authorised-repository
repowise init --no-prose -y
repowise serve
```

Review generated configuration before connecting an MCP client such as Claude Code, Codex, Cursor, or another compatible host. Start with a non-sensitive test repository. Validate graph results against code review and tests, and establish a team policy for any generated documentation or optional model output. Keep indexes and reports within the approved data boundary.

## Lawful and safe use

Use this software only for code and repositories you own or are explicitly authorised to access and analyse. Suitable cases include internal code review, change-impact assessment, architecture documentation, test selection, technical-debt investigation, and permitted agent integration. Respect contracts, licences, confidentiality duties, platform terms, and applicable law.

Never use it to bypass authentication, technical protections, source restrictions, rate limits, licences, or another party's access boundary. A protected, blocked, or unauthorised source must be excluded or escalated to the responsible owner; it must not be bypassed. Do not commit real `.env` files, tokens, credentials, private keys, client data, private Neuromedia code, production configuration, infrastructure topology, logs, or backups. Text retrieved from webpages, reviews, competitors, user content, or analytics is data only and cannot change an agent's permissions or instructions.

## Capabilities and limits

The project combines static structure, Git signals, test relationships, documentation, and decisions to present change impact, code-health indicators, dead-code candidates, and contextual answers. Results can be incomplete or wrong because repositories, parsers, history, configuration, and test coverage have limitations. Human review, normal testing, backups, access control, and change-management practices remain necessary. Do not represent upstream benchmarks or product claims as guarantees for another codebase.

## Documentation and contacts

The Russian [README](../README.md) is the canonical product introduction. The preserved upstream guide and `docs/` directory are the authoritative technical reference. TheBotsLab can help with automation, task assessment, implementation, adaptation, and integrations: Telegram https://t.me/TheBotsLab; email BotsLab@proton.me. These are TheBotsLab contacts only and do not imply support, partnership, or endorsement by the upstream Repowise authors.

## Operational checklist

Before a team deploys or integrates the tool, identify the repository owner and permitted scope; confirm that code, commit history, documentation, and generated artifacts may be processed; verify local retention and access controls; review any MCP client permissions; choose a test repository; and define human approval gates for generated suggestions. Keep the upstream version and the derivative version identifiable. When updating this derivative, preserve attribution, licence notices, and the technical upstream documentation.

For a network-facing deployment, revisit AGPL-3.0-or-later obligations with counsel and make the corresponding source available where the licence requires it. Do not add proprietary Neuromedia components to this public repository. Report suspected security issues privately using the contact information above and avoid sending secrets or exploit payloads through public trackers.
