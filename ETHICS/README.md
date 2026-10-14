# Ethics — POWERTOP

**Project:** POWERTOP  
**Category:** LAPTOPS  
**Upstream:** see BENCH.json  
**Pinned commit:** `fc38769ba42c3fa3b397dcd1b7116d2aa2f68424`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `acf995bf8030b5320a1ad9701b0b0a6735c822664d4eba62384e81d6e1467f80`  
**Date:** October 2026

## Position

POWERTOP is packaged for offline deployment with a verifiable audit trail. The
ethical questions this raises are answered by making the system's behaviour
checkable rather than by policy statements.

## The four commitments

1. **No hidden egress.** The deployment has no external API dependency; this is
   testable by running it with the network disconnected.
2. **Attributable output.** Every artifact is recorded in a hash chain, so what
   the system produced can be reconstructed.
3. **Operator control.** The institution owns the hardware and the keys.
4. **Refusal to overclaim.** Where a certification is not held, the project says
   so rather than implying it.

## Dual use

This project is packaged for civilian and public-sector deployment. Where an
upstream has dual-use characteristics, the licence gate and the reference-only
marking in `BENCH.json` record that.
