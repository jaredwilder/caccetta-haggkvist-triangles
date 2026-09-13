# Caccetta–Häggkvist Triangle Case — Terminal Audit Packet

## Court verdict

This packet contains a complete, machine-checkable proof of a strong structural theorem about any hypothetical extremal counterexample.

It does **not** contain a proof of the full Caccetta–Häggkvist directed-triangle case.

The proved theorem is:

> **Cubic Directed-\(C_4\) Theorem.**  
> Let \(D\) be an oriented graph on \(n=3d\) vertices such that every vertex has outdegree exactly \(d\), and suppose \(D\) contains no directed triangle. Then
> \[
> C_4(D)\ge \frac{3d^3}{2},
> \]
> where \(C_4(D)\) denotes the number of directed \(4\)-cycles counted up to cyclic rotation.

Equivalently,
\[
\operatorname{tr}(A^4)\ge 6d^3,
\]
where \(A\) is the adjacency matrix of \(D\).

This theorem is the strongest fully audited result produced by the current encirclement.

---

## 1. Definitions

Let \(D=(V,E)\) be an oriented graph:

- no loops;
- no pair of opposite arcs;
- \(|V|=3d\);
- \(d^+(x)=d\) for every \(x\in V\);
- no directed triangle.

Let \(A\) be its adjacency matrix:
\[
A_{xy}=
\begin{cases}
1,&x\to y,\\
0,&\text{otherwise}.
\end{cases}
\]

Put
\[
Q=A^2.
\]

Thus
\[
Q_{xy}=|\{u:x\to u\to y\}|.
\]

For each unordered nonadjacent pair \(\{x,y\}\), define
\[
a_{xy}:=Q_{xy},\qquad b_{xy}:=Q_{yx}.
\]

Because \(x\) has exactly \(d\) outneighbors,
\[
0\le a_{xy},b_{xy}\le d.
\]

---

## 2. Exact number of nonedges

The oriented graph has
\[
|E|=\sum_x d^+(x)=3d^2
\]
arcs.

Because there are no digons, each arc occupies one unordered adjacent pair.

Hence the number \(N_0\) of unordered nonadjacent pairs is
\[
N_0=\binom{3d}{2}-3d^2
=\frac{3d(d-1)}2.
\]

---

## 3. Escape two-path mass

Fix \(x\in V\) and let
\[
A_x=N^+(x).
\]

There are exactly \(d^2\) arcs whose tail lies in \(A_x\), because \(|A_x|=d\) and every vertex has outdegree \(d\).

No arc can run from \(A_x\) into \(N^-(x)\): if
\[
x\to u,\qquad u\to y,\qquad y\to x,
\]
then \(x,u,y\) form a directed triangle.

Therefore every arc leaving \(A_x\) either:

1. remains inside \(A_x\); or
2. ends at a vertex nonadjacent to \(x\).

The number of internal arcs satisfies
\[
e(D[A_x])\le \binom d2,
\]
because \(D[A_x]\) is oriented.

Consequently,
\[
\sum_{y\not\sim x}Q_{xy}
=d^2-e(D[A_x])
\ge d^2-\binom d2
=\frac{d(d+1)}2.
\]

Summing over all \(x\),
\[
E_2:=
\sum_{\substack{(x,y)\\x\not\sim y}}Q_{xy}
\ge
3d\cdot\frac{d(d+1)}2
=
\frac{3d^2(d+1)}2.
\]

Equivalently, summing over unordered nonedges,
\[
\sum_{\{x,y\}\text{ nonedge}}(a_{xy}+b_{xy})
\ge
\frac{3d^2(d+1)}2.
\]

---

## 4. Opposite-path product inequality

For every unordered nonedge \(\{x,y\}\),
\[
(d-a_{xy})(d-b_{xy})\ge0.
\]

Expanding,
\[
a_{xy}b_{xy}
\ge
d(a_{xy}+b_{xy}-d).
\]

Summing over all unordered nonedges gives
\[
\sum_{\{x,y\}\text{ nonedge}}a_{xy}b_{xy}
\ge
d\left(
\sum_{\{x,y\}\text{ nonedge}}(a_{xy}+b_{xy})
-dN_0
\right).
\]

Insert the established bounds:
\[
\sum(a_{xy}+b_{xy})
\ge
\frac{3d^2(d+1)}2,
\]
and
\[
dN_0=\frac{3d^2(d-1)}2.
\]

Their difference is
\[
\frac{3d^2((d+1)-(d-1))}{2}
=3d^2.
\]

Therefore
\[
\boxed{
\sum_{\{x,y\}\text{ nonedge}}Q_{xy}Q_{yx}
\ge 3d^3.
}
\]

---

## 5. Conversion to directed four-cycles

For a nonadjacent unordered pair \(\{x,y\}\), the product
\[
Q_{xy}Q_{yx}
\]
counts choices of vertices \(u,v\) satisfying
\[
x\to u\to y
\quad\text{and}\quad
y\to v\to x.
\]

These choices form a directed closed walk
\[
x\to u\to y\to v\to x.
\]

The four vertices are distinct:

- \(x\ne y\) by definition;
- \(u\ne x,y\) and \(v\ne x,y\) because the graph has no loops;
- \(u\ne v\), because otherwise both \(u\to y\) and \(y\to u\) would hold, forming a digon.

Hence each choice gives a genuine directed \(4\)-cycle.

Conversely, every directed \(4\)-cycle
\[
x\to u\to y\to v\to x
\]
is counted once for the opposite pair \(\{x,y\}\) and once for the opposite pair \(\{u,v\}\).

Thus
\[
\sum_{\{x,y\}\text{ nonedge}}Q_{xy}Q_{yx}
=
2C_4(D).
\]

Combining with the previous section:
\[
2C_4(D)\ge3d^3.
\]

Therefore
\[
\boxed{
C_4(D)\ge\frac{3d^3}{2}.
}
\]

Since
\[
\operatorname{tr}(A^4)=4C_4(D),
\]
we also obtain
\[
\boxed{
\operatorname{tr}(A^4)\ge6d^3.
}
\]

---

## 6. Integrality note

The integer-valued conclusion may be written as
\[
C_4(D)\ge\left\lceil\frac{3d^3}{2}\right\rceil.
\]

When \(d\) is odd, \(3d^3/2\) is a half-integer, so the ceiling form is the exact integer statement.

---

## 7. Minimal machine checker

A checker needs only:

1. verify that \(A\) is a \(0\)-\(1\) square matrix;
2. verify zero diagonal;
3. verify \(A_{ij}A_{ji}=0\);
4. verify every row sum equals \(d\);
5. verify \(n=3d\);
6. verify \(\operatorname{tr}(A^3)=0\);
7. compute \(Q=A^2\);
8. enumerate unordered nonedges;
9. verify:
   \[
   \sum_{\{x,y\}}Q_{xy}Q_{yx}\ge3d^3;
   \]
10. verify:
   \[
   \operatorname{tr}(A^4)
   =
   2\sum_{\{x,y\}\text{ nonedge}}Q_{xy}Q_{yx}
   \ge6d^3.
   \]

The symbolic proof requires no floating-point arithmetic, optimization, or external theorem beyond finite integer counting.

---

## 8. Lean formalization targets

A clean Lean development can separate the result into these lemmas:

1. `no_arc_outNbr_to_inNbr`
2. `escape_two_path_mass_vertex`
3. `unordered_nonedge_count`
4. `opposite_path_product_lower_bound`
5. `opposite_two_paths_distinct`
6. `opposite_two_paths_to_directed_four_cycle`
7. `directed_four_cycle_count_double`
8. `cubic_directed_C4_lower_bound`

The only delicate formalization step is the precise finite-set convention for counting directed \(4\)-cycles modulo cyclic rotation.

The trace statement
\[
\operatorname{tr}(A^4)\ge6d^3
\]
is likely the easier initial kernel theorem.

---

## 9. Exact CH closure boundary

This theorem does not contradict the existence of a hypothetical counterexample.

A full proof of the directed-triangle case still needs a valid implication of the form
\[
C_4(D)\ge\frac{3d^3}{2}
\quad\Longrightarrow\quad
D\text{ contains a directed triangle},
\]
or another contradiction derived from the same kernel.

No such implication has been proved in this packet.

The current exact missing obligation is:

> **Fourth-Moment Closure Obligation.**  
> Prove that no oriented \(d\)-out-regular graph on \(3d\) vertices can be directed-triangle-free while satisfying
> \[
> \operatorname{tr}(A^4)\ge6d^3.
> \]

At present this obligation is unsupported and may itself be false without additional hypotheses.

---

## 10. Final authority statement

**Proved here:** the cubic directed-\(C_4\) lower bound, conditional only on the stated extremal-counterexample kernel.

**Not proved here:** the Caccetta–Häggkvist directed-triangle conjecture.

**Recommended machine disposition:**

- submit the cubic \(C_4\) theorem to exact checking;
- run a novelty check only after the theorem survives;
- do not mark the flagship closed unless a separately checked contradiction from the fourth-moment condition is supplied.
