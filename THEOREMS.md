# Structural results for the directed-triangle boundary case

This note collects the principal mathematical statements used in the repository's study of a hypothetical triangle-free oriented graph at the exact Caccetta–Häggkvist boundary.

## Boundary setup

Let `D` be a triangle-free oriented graph on

\[
n=3d
\]

vertices with every vertex of outdegree `d`.

For a vertex `x`, write

\[
P_x=N^+(x),\qquad I_x=N^-(x),\qquad M_x=V(D)\setminus(P_x\cup I_x\cup\{x\}).
\]

Triangle-freeness immediately gives

\[
E(P_x,I_x)=\varnothing.
\]

## Exact escape identity

Define

\[
\sigma(x)=\binom d2-e(P_x).
\]

Then

\[
\boxed{e(P_x,M_x)=\frac{d(d+1)}2+\sigma(x).}
\]

Thus every edge missing from the transitive part of the outneighborhood reappears as one unit of escape mass into the nonneighbor set.

Equivalently, if directed two-paths from `x` are divided into transitively closed paths and paths ending at nonneighbors, the total is exactly `d^2` and the two classes trade mass one-for-one.

## Common two-path multiplicity

Let

\[
q(x,y)=|N^+(x)\cap N^-(y)|
\]

for an ordered nonadjacent pair `(x,y)`.

Summing the escape identity over all vertices forces at least one ordered nonedge with

\[
\boxed{q(x,y)\ge\left\lceil\frac{d(d+1)}{2(d-1)}\right\rceil>rac d2+1.}
\]

So every boundary counterexample contains a nonadjacent pair joined by many directed two-paths.

## One-way rectangle around a heavy nonedge

Fix such a pair `(x,y)` and put

\[
P=N^+(x)\cap N^-(y),
\qquad
H=N^+(y)\cap N^-(x).
\]

Then no edge points from `P` to `H`. Every adjacency between the two sets is oriented

\[
H\to P.
\]

Moreover every pair `(p,h)\in P\times H` gives a directed 4-cycle

\[
x\to p\to y\to h\to x.
\]

This is the basic local rectangle underlying the fourth-moment argument.

## Two-path / fourth-moment identity

Let `A` be the adjacency matrix of `D`. The source argument derives

\[
\boxed{
\operatorname{tr}(A^4)
=
\|A^2\|_F^2
-
\frac12\|A^2-(A^{\mathsf T})^2\|_F^2.
}
\]

The first term measures total two-path concentration. The second measures directional imbalance between the number of two-paths `x→*→y` and `y→*→x`.

This identity isolates the main obstruction to a direct energy proof: large two-path mass need not produce enough directed 4-cycles if it is stored too asymmetrically.

## Directed 4-cycle lower bound

Within the regular boundary framework, the source proof gives

\[
\boxed{C_4(D)\ge\left\lceil\frac{3d^3}{2}\right\rceil.}
\]

Equivalently,

\[
\boxed{\operatorname{tr}(A^4)\ge6d^3.}
\]

The repository currently preserves a written derivation and exact supporting identities. A separate independent machine verification of this headline inequality has not yet been completed.

## Supporting structural statements

The larger source archive also contains:

- minimum-counterexample and arc-minimal regularization reductions;
- hereditary deficit and exact escape inequalities;
- nonneighbor-capacity bounds;
- global conservation identities for nonneighbor and two-path mass;
- bridge-deficit and reverse-bridge inequalities;
- one-way fan and rectangle saturation bounds;
- fourth-moment and defect formulations developed after earlier potential-function routes failed.

These are best read as components of the boundary-kernel program rather than as a theorem-counting exercise.

## Remaining cut

The regular boundary case would be eliminated by a sufficiently strong upper control on the skew two-path energy

\[
\|A^2-(A^{\mathsf T})^2\|_F^2.
\]

That is the clean remaining obstruction identified by the current argument.

The historical source dossier and theorem ledger are retained under `source/big-guns-2026-08-06/` for provenance and detailed dependency tracing.

Author: Jared Wilder.
