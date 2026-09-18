# Caccetta–Häggkvist: the directed-triangle boundary case

For an oriented graph `D`, the `r=3` Caccetta–Häggkvist problem asks whether

\[
\delta^+(D)\ge \frac{|V(D)|}{3}
\]

forces a directed triangle.

This repository studies the exact boundary of a hypothetical minimum counterexample. The main surviving calculation is a cubic lower bound on directed 4-cycles in the regular boundary case, together with exact two-path identities that isolate the remaining obstruction.

## Directed 4-cycle lower bound

Let `D` be a triangle-free oriented graph on `3d` vertices in which every vertex has outdegree `d`. The source proof gives

\[
\boxed{C_4(D)\ge \left\lceil\frac{3d^3}{2}\right\rceil,}
\]

where `C_4(D)` counts directed 4-cycles. Equivalently, for the adjacency matrix `A`,

\[
\boxed{\operatorname{tr}(A^4)\ge 6d^3.}
\]

The accompanying exact identity is

\[
\operatorname{tr}(A^4)
=
\|A^2\|_F^2
-
\frac12\|A^2-(A^{\mathsf T})^2\|_F^2.
\]

This makes the difficulty concrete: a triangle-free boundary graph must carry large two-path mass, but that mass can be stored asymmetrically between `(x,y)` and `(y,x)`. The remaining problem is to control the skew two-path energy

\[
\|A^2-(A^{\mathsf T})^2\|_F^2
\]

strongly enough to make the boundary kernel impossible.

[`THEOREMS.md`](THEOREMS.md) is the recommended detailed mathematical note. The historical source dossier remains available for dependency tracing.

## Exact boundary structure

For a vertex `x`, write

\[
P_x=N^+(x),\qquad I_x=N^-(x),\qquad M_x=V(D)\setminus(P_x\cup I_x\cup\{x\}).
\]

Triangle-freeness gives

\[
E(P_x,I_x)=\varnothing.
\]

If

\[
\sigma(x)=\binom d2-e(P_x),
\]

then the exact escape identity is

\[
\boxed{e(P_x,M_x)=\frac{d(d+1)}2+\sigma(x).}
\]

Summing this identity converts missing transitive closure into directed two-path mass. At `n=3d`, the argument forces an ordered nonadjacent pair `(x,y)` with more than `d/2+1` common directed intermediates from `x` to `y`.

For such a pair, set

\[
P=N^+(x)\cap N^-(y),\qquad H=N^+(y)\cap N^-(x).
\]

Every adjacency between `H` and `P` points from `H` to `P`, and every pair `(p,h)\in P\times H` gives the directed 4-cycle

\[
x\to p\to y\to h\to x.
\]

This one-way rectangle is the local geometry behind the fourth-moment calculation.

## Verification and source material

The public mathematical entry points are:

- [`THEOREMS.md`](THEOREMS.md) — principal structural statements and the remaining cut;
- [`source/big-guns-2026-08-06/CH3-BIG-GUNS-MASTER-DOSSIER.md`](source/big-guns-2026-08-06/CH3-BIG-GUNS-MASTER-DOSSIER.md) — historical full derivation and chronology;
- [`source/big-guns-2026-08-06/THEOREM-LEDGER.json`](source/big-guns-2026-08-06/THEOREM-LEDGER.json) — structured historical records;
- [`source/big-guns-2026-08-06/RETRACTION-REGISTER.md`](source/big-guns-2026-08-06/RETRACTION-REGISTER.md) — corrections to superseded routes.

Run

```sh
python verification/verify_source_packet.py
```

to check source hashes and record counts. That script verifies archival integrity; it is not an independent proof checker for the directed-4-cycle inequality.

## Remaining mathematical question

The program reduces attention to an exact regular boundary kernel and identifies the skew two-path energy as the load-bearing obstruction. A proof that this asymmetry cannot be large enough would eliminate the kernel and complete this route to the directed-triangle case.

Historical priority of the directed-4-cycle inequality and some supporting identities should be assessed separately from the internal proof status.

Author: Jared Wilder.
