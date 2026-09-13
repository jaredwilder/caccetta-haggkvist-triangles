# Caccetta–Häggkvist directed-triangle program

**Author:** Jared Wilder  
**Status:** research program / partial structural results; the Caccetta–Häggkvist conjecture is **not claimed solved**.

This repository is the canonical public home for the estate's directed-triangle campaign. It preserves the theorem ledger, terminal-defect package, recovered defect-budget work, correction history, and exact finite relation-table evidence in one subject-focused location.

## What is here

The source program develops exact-boundary structure for a hypothetical minimum counterexample at `r=3`, including regularity forced by arc-minimality, the `n in {3d-1,3d}` boundary, fourth-moment lower bounds, critical-edge common-outneighbor bounds, and the defect identity replacing a looser edge-potential route. It also preserves corrected/retracted statements rather than silently deleting them.

The exact historical source bytes are migrated under `source/` from `jaredwilder/unpublished-math-papers/caccetta-haggkvist/`.

## Reading rule

A theorem ledger entry is not automatically a closure of the conjecture. Conditional reductions, exact finite classifications, negative results, and open obligations remain status-separated.

Historical novelty is a separate literature question from mathematical correctness.

## Recovered original source packet — 2026-09-13

The original fifteen-round packet contains 166 theorem, candidate, diagnostic and retraction records. The source retraction register is essential reading. Its cubic directed-C4 result is explicitly awaiting independent verification; this release does not certify all ledger entries.

- [Original record table](source/big-guns-2026-08-06/THEOREM-LEDGER.json)
- [Source packet](source/big-guns-2026-08-06/)
- [Source hashes and observed status counts](verification/source-packet.json)

Read the [retraction register](source/big-guns-2026-08-06/RETRACTION-REGISTER.md) alongside the [master dossier](source/big-guns-2026-08-06/CH3-BIG-GUNS-MASTER-DOSSIER.md). Historical supported/proposal statuses are source assertions; this packet has no executable proof verification in this release.

Run `python verification/verify_source_packet.py` to verify all recovered source bytes, original JSON manifests when present, and record counts.
