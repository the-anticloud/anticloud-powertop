# Independent Insurance — POWERTOP

**Project:** POWERTOP  
**Category:** LAPTOPS  
**Upstream:** see BENCH.json  
**Pinned commit:** `fc38769ba42c3fa3b397dcd1b7116d2aa2f68424`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `acf995bf8030b5320a1ad9701b0b0a6735c822664d4eba62384e81d6e1467f80`  
**Date:** October 2026

## Why AI-specific cover matters

Deploying AI in a regulated sector creates liability surfaces that ordinary
technology cover does not reach: inference liability, audit-trail liability,
data-breach liability and IP-infringement liability.

## How this project's architecture reduces insurable risk

| Risk | Cloud AI | POWERTOP with AIOSS |
|---|---|---|
| Audit-trail loss | high — vendor-controlled logs | low — append-only chain, verifiable offline |
| Data breach in transit | high — data transits external servers | low — no external endpoint |
| Compliance violation | high — cannot satisfy air-gap requirements | low — structural |
| IP liability | moderate | low — pinned provenance chain |

## Evidence package for an insurer

- AIOSS chain verification for head `acf995bf8030b5320a1ad9701b0b0a6735c822664d4eba62384e81d6e1467f80`
- The 16-check register with per-check evidence hashes
- Framework control mapping in `BENCH.json`

## Contact

lois@0-1.gg
