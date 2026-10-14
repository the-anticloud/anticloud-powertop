# Students — POWERTOP

**Project:** POWERTOP  
**Category:** LAPTOPS  
**Upstream:** see BENCH.json  
**Pinned commit:** `fc38769ba42c3fa3b397dcd1b7116d2aa2f68424`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `acf995bf8030b5320a1ad9701b0b0a6735c822664d4eba62384e81d6e1467f80`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `fc38769ba42c3fa3b397dcd1b7116d2aa2f68424`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `acf995bf8030b5320a1ad9701b0b0a6735c822664d4eba62384e81d6e1467f80`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
