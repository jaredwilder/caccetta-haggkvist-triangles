# Computational Attack Plan

## Campaign A — Verify the principal theorem

For bounded \(d\):

1. generate every feasible candidate or use SAT/CP-SAT;
2. enforce:
   - \(n=3d\);
   - zero diagonal;
   - no digons;
   - every row sum \(d\);
   - no directed triangle;
3. compute \(Q=A^2\);
4. verify:
   \[
   \sum_{\{x,y\}\text{ nonedge}}Q_{xy}Q_{yx}\ge3d^3;
   \]
5. verify:
   \[
   \operatorname{tr}(A^4)\ge6d^3.
   \]

Any violation refutes the session theorem immediately.

## Campaign B — Optimize skew energy

Optimize:
\[
K(D)=\|A^2-(A^{\mathsf T})^2\|_F^2.
\]

Record:

- maximum \(K(D)\);
- ratio \(K(D)/\|A^2\|_F^2\);
- distribution of \((Q_{xy},Q_{yx})\);
- maximum product and maximum asymmetry;
- indegree variance;
- common-in/common-out rectangle statistics.

## Campaign C — Search for strengthening candidates

Candidate families:

1. a universal upper bound on skew energy;
2. a lower bound on the number of nonedges with both \(Q_{xy},Q_{yx}\ge c d\);
3. a variance penalty for highly asymmetric products;
4. a relation between indegree variance and skew energy;
5. a fifth/sixth moment inequality using \(A^2\circ A^{\mathsf T}=0\);
6. flag inequalities retaining a directed \(4\)-cycle and one extra vertex.

Every candidate must be falsified on bounded instances before being admitted.

## Campaign D — Novelty

Only after verification, search for the exact statements:

- `trace(A^4) >= 6 d^3` under CH3 exact-boundary kernel;
- `C4 >= 3 d^3 / 2`;
- opposite two-path product lower bound;
- skew decomposition in CH literature;
- heavy vertex and heavy opposite-pair corollaries.
