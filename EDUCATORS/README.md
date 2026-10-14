# Educators — POWERTOP

**Project:** POWERTOP  
**Category:** LAPTOPS  
**Upstream:** see BENCH.json  
**Pinned commit:** `fc38769ba42c3fa3b397dcd1b7116d2aa2f68424`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `acf995bf8030b5320a1ad9701b0b0a6735c822664d4eba62384e81d6e1467f80`  
**Date:** October 2026

## Teaching with POWERTOP

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `acf995bf8030b5320a1ad9701b0b0a6735c822664d4eba62384e81d6e1467f80` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
