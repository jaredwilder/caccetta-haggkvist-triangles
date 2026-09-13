# Retraction Register

## R-1 — Hereditary induced-edge sparsity

**Claim withdrawn**
\[
e(D[S])\le\sum_{t=1}^{|S|}\left(\left\lceil\frac t3\right\rceil-1\right).
\]

**Fault**
The peeling sum counts only arcs whose tails are removed before their heads. Backward arcs are omitted.

**Refutation**
A transitive tournament admits a removal order with residual outdegree \(0\) at every step while containing \(\binom{|S|}{2}\) arcs.

**Dependent assets withdrawn**
T76, T77, T81–T89, T94, T96–T100, all \(5/6\) escape and \(7/6\) indegree conclusions, and the apparent near-Mantel close.

## R-2 — \(0.68614d\) maximum fan

**Claim withdrawn**
\[
\max_{x,y}Q_{xy}\gtrsim0.68614d.
\]

**Fault**
An upper bound on \(d^-(x)\) produced a lower bound on the denominator of
\[
q\ge\frac{d^2}{3d-1-d^-(x)}.
\]
Substituting a lower denominator bound in that direction cannot strengthen the lower bound on \(q\).

**Valid replacement**
For a root with \(d^-(x)\ge d\):
\[
\max_yQ_{xy}\ge\frac{d^2}{2d-1}>\frac d2.
\]

## R-3 — Recursive fan cascade

A second-order common-target concentration was proved, but recursive applicability under identical hypotheses was not. T65 is withdrawn as an iteration theorem.

## R-4 — Universal promotion errors

Several statements initially derived for a specially selected high-indegree root were rhetorically promoted to every vertex. The universal promotion was removed. The only valid universal indegree ceiling retained is:
\[
d^-(x)\le\frac{3d-3}{2}.
\]
