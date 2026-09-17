# Caccetta–Häggkvist Directed Triangles

**Jared Wilder**

Structural work on the `r=3` case of the Caccetta–Häggkvist conjecture, with a focus on the exact boundary of a hypothetical minimum counterexample.

## Main structure

The program develops:

- regularity forced by arc-minimality;
- the boundary `n ∈ {3d-1, 3d}`;
- fourth-moment lower bounds;
- critical-edge common-outneighbor bounds;
- a defect identity replacing an earlier edge-potential route;
- exact finite relation-table evidence around the terminal defect configuration.

The source packet contains 166 theorem, candidate, diagnostic, and correction records from the fifteen-round campaign. Its useful mathematical content is preserved here by subject rather than buried in a session archive.

## Source packet

Historical source bytes live under `source/`, migrated from `jaredwilder/unpublished-math-papers/caccetta-haggkvist/`.

Key files:

- [theorem ledger](source/big-guns-2026-08-06/THEOREM-LEDGER.json)
- [master dossier](source/big-guns-2026-08-06/CH3-BIG-GUNS-MASTER-DOSSIER.md)
- [retraction register](source/big-guns-2026-08-06/RETRACTION-REGISTER.md)
- [source verification summary](verification/source-packet.json)

Run

```sh
python verification/verify_source_packet.py
```

to verify recovered source hashes, manifests, and record counts.

## Status

The repository contains partial structural results and exact finite evidence toward the directed-triangle problem. The full Caccetta–Häggkvist conjecture is not resolved here.