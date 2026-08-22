# John Gilligan

Chief engineer at an ISP/MSP. Twenty years of production networking (BGP,
carrier voice, three datacenters), now spent building AI systems that run on
that infrastructure and answering the question the demos skip: how do you know
it works, and what happens when it is wrong?

## What I build

- **A fleet of ~20 production MCP servers** over the systems an MSP actually
  runs: the carrier voice switch, RMM, O365 audit logs, virtualization,
  documentation. Entra-authenticated, containerized, telemetry on every tool.
- **[mcp-telemetry-kit](https://github.com/JohnGilligan2/mcp-telemetry-kit)**:
  two copy-in files that give any MCP server a Grafana presence, including the
  context-window cost each tool's schema imposes on every connected client.
  Deliberately not a package; the README explains why.
- **Scored decision pipelines**: an outage detector where statistical detectors
  surface candidates, an LLM judge scores them against semantic prior art, and
  a golden set built from operational outcomes (not model opinion) measures
  recall and precision separately, because a missed outage and a noisy alert
  do not cost the same.
- **[snapshot-drift](https://github.com/JohnGilligan2/snapshot-drift)** and
  **[selfhosted-claude-code](https://github.com/JohnGilligan2/selfhosted-claude-code)**:
  a deterministic config-drift differ whose alert set was tuned by measurement
  (1,247 real snapshot pairs, 4 findings), and a self-hosted runner fleet that
  executes cloud agent sessions on our own infrastructure, outbound-only.
- **Tenancy boundaries as code**: the customer-facing connector pattern where
  every read passes through one scope module with its own leak-test suite.
  Written up [on the blog](https://johngilligan2.github.io/).

## Writing

- [Securing a customer-facing MCP server](https://johngilligan2.github.io/) —
  what changed when the threat model inverted from internal to customer-facing,
  and the part I am least comfortable with.

More at [johngilligan2.github.io](https://johngilligan2.github.io/).
