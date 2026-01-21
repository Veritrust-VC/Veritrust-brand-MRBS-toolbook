# VeriTrust MRBS SSOT (Machine-Readable Brand System)

This repository is the **Single Source of Truth (SSOT)** for the **VeriTrust** brand in **MRBS** format.

VeriTrust provides **identity, trust, and governance** infrastructure for **AI agents**, **MCP servers**, and other digital entities, including:
- Agent Name Service (ANS)
- MCP Trust Registry / MCP Trust Framework (MCPF)
- A2A Delegation Registry
- DID/VC issuance and verification APIs

This SSOT enables:
- AI agents to generate brand-consistent copy/design
- Automated validation of brand compliance
- Design systems and apps to consume tokens directly
- Version-controlled evolution of the brand

---

## How to Use

### For AI Agents
1. Read `brand.manifest.json` first.
2. Load identity rules from `identity/*`.
3. Load design tokens from `visual/*` (or root tokens).
4. Validate outputs using `rules/*`.
5. Compare against `examples/correct` and avoid `examples/incorrect`.

### For Designers / Developers
- Use `visual/*.tokens.json` for UI tokens.
- Use `assets/*` for approved SVG assets.
- Use `templates/*` manifests to drive generation of slides/docs/web blocks.

---

## Key Principles (VeriTrust-specific)
- Trust is **verifiable** (DIDs/VCs), not “claimed”.
- Governance is **enforced** (policy + registry + revocation), not “suggested”.
- Messaging must be **precise**, **audit-friendly**, and **enterprise-safe**.
- Avoid hype; prefer concrete mechanisms (verify, issue, resolve, revoke).

---

## Versioning
- SSOT version: see `brand.manifest.json` -> `version`
- Follow SemVer:
  - MAJOR: breaking schema changes
  - MINOR: new tokens/templates/rules
  - PATCH: copy fixes, clarifications

---

## License
Content is provided for VeriTrust brand operations. See `rules/legal.yaml` for trademark usage and required notices.
