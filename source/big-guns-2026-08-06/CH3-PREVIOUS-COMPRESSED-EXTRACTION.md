# Caccetta–Häggkvist Directed-Triangle Campaign
## Full Asset Extraction — Entire Session

**Date:** 2026-08-06  
**Flagship:** Caccetta–Häggkvist conjecture, directed-triangle case  
**Target:** For every finite simple digraph/oriented graph \(D\) on \(n\) vertices,
\[
\delta^+(D)\ge \frac n3 \quad\Longrightarrow\quad D\text{ contains a directed }3\text{-cycle}.
\]

This document is a complete extraction of the mathematical assets produced during the session: valid reductions, named theorems, identities, proof attempts, retractions, failed kill shots, machine-checkable targets, exact surviving obstructions, and the strongest terminal theorem presently supported.

It deliberately distinguishes:

- **SUPPORTED** — proved in the session from stated hypotheses and suitable for machine checking;
- **CONDITIONAL** — correct under an explicitly stated reduction/hypothesis;
- **PROPOSAL / OBLIGATION** — a target that would close or materially advance the campaign but is not proved;
- **RETRACTED** — a statement whose derivation was found invalid;
- **FAILED ROUTE** — an attempted close whose precise failure was identified.

The flagship was **not proved** in this session. The strongest terminal audited result is the cubic directed-\(C_4\) lower bound for a hypothetical exact-boundary regular counterexample.

---

# 1. Flagship and Exact-Boundary Kernel

The campaign attacks the \(k=3\) case:
\[
\delta^+(D)\ge n/3 \implies C_3^\to\subseteq D.
\]

The working contradiction setup repeatedly used the exact-boundary form
\[
n=3d.
\]

After arc-minimization, the intended kernel is:
\[
d^+(v)=d\qquad\forall v.
\]

For the audited terminal theorem, the hypotheses can simply be taken directly as:

> \(D\) is an oriented graph on \(3d\) vertices, every vertex has outdegree exactly \(d\), and \(D\) has no directed triangle.

Let \(A\) be its adjacency matrix and
\[
Q:=A^2.
\]
Then
\[
Q_{xy}=|\{u:x\to u\to y\}|
\]
counts directed two-paths from \(x\) to \(y\).

The basic matrix kernel is:
\[
A\mathbf 1=d\mathbf 1,
\]
\[
A\circ A^{\mathsf T}=0,
\]
\[
A^2\circ A^{\mathsf T}=0.
\]

The last identity is the entrywise form of directed-triangle-freeness: if \(y\to x\), there can be no two-path \(x\to u\to y\).

---

# 2. Rooted Chamber Geometry

Fix \(x\in V(D)\) and define
\[
A_x=N^+(x),\qquad B_x=N^-(x),
\]
and
\[
M_x=V(D)\setminus(A_x\cup B_x\cup\{x\}).
\]

When no confusion arises:
\[
A=N^+(x),\quad B=N^-(x),\quad M=V\setminus(A\cup B\cup\{x\}).
\]

Write
\[
|A|=d,\qquad |B|=r=d^-(x),\qquad |M|=m=2d-r-1.
\]

## SUPPORTED — Outneighborhood wall
There are no arcs
\[
A\to B.
\]
Indeed, \(x\to a\to b\to x\) would be a directed triangle.

Thus:
\[
\boxed{E(A,B)=\varnothing.}
\]

This was variously named **\(A\to B\) Zero Theorem** and **Outneighborhood Wall Theorem**.

## SUPPORTED — Exact escape identity
All \(d^2\) outgoing arcs from the \(d\) vertices of \(A\) land in \(A\cup M\). Hence
\[
\boxed{d^2=e(A)+e(A,M).}
\]

Since an oriented graph on \(d\) vertices has at most \(\binom d2\) arcs,
\[
e(A,M)\ge d^2-\binom d2
=\frac{d(d+1)}2.
\]

Thus:
\[
\boxed{e(A,M)\ge\frac{d(d+1)}2.}
\]

## SUPPORTED — Local defect identity
Define
\[
\sigma(x):=\binom d2-e(A).
\]
Then
\[
\boxed{
e(A,M)=\frac{d(d+1)}2+\sigma(x).
}
\]

Every missing adjacency inside \(N^+(x)\) creates one additional unit of escape-arc mass into \(M\).

## SUPPORTED — Universal indegree ceiling
Since
\[
e(A,M)\le d|M|=dm,
\]
we obtain
\[
m\ge\frac{d+1}{2}.
\]
Since
\[
r=2d-1-m,
\]
\[
\boxed{
d^-(x)=r\le\frac{3d-3}{2}.
}
\]

This is the valid universal \(3/2\)-scale indegree barrier.

---

# 3. Minimal-Counterexample Hereditary Property

Under a smallest-counterexample reduction, every proper nonempty induced subgraph \(D[S]\) must fail the same threshold:
\[
\boxed{
\delta^+(D[S])<\frac{|S|}{3}
\qquad
(\varnothing\ne S\subsetneq V).
}
\]

Equivalently, every proper nonempty \(S\) contains some \(v\in S\) with
\[
d_S^+(v)<|S|/3.
\]

This one-sided peeling property is valid.

## Critical warning
It does **not** imply a bound on the total number of arcs \(e(D[S])\).

A dense acyclic/transitive orientation can have very low residual outdegree in an elimination ordering while containing \(\binom{|S|}{2}\) arcs, because arcs pointing backward in the elimination order are not counted by the residual outdegree sum.

This distinction caused the most important retraction in the campaign.

---

# 4. Major Retraction: False Hereditary Edge Bound

An earlier branch defined a function \(F(s)\) and claimed
\[
e(D[S])\le F(s)
\]
by summing low residual outdegrees along a peeling order.

That argument is invalid.

## Exact fault
For an elimination order \(v_1,\dots,v_s\),
\[
\sum_i d^+_{\{v_i,\dots,v_s\}}(v_i)
\]
counts only arcs pointing forward in that order.

An arc
\[
v_j\to v_i,\qquad j>i,
\]
is never counted in that sum.

## Refutation model
A transitive tournament can have all removed vertices of residual outdegree \(0\) under a suitable removal order while still containing
\[
\binom s2
\]
arcs.

## RETRACTED consequences
Every result relying essentially on the false hereditary edge estimate was withdrawn, including:

- **Exact Hereditary Edge Bound**;
- **Hereditarily Sharpened Fan Capacity Theorem**;
- **Five-Sixths Escape Theorem**;
- **Five-Sixths Bridge Theorem**;
- **Hereditary Bridge Export Theorem**;
- **Seven-Sixths Indegree Barrier**;
- the Round 9 **Three-Layer Density Ledger** in its \(F(s)\)-dependent form;
- all later \(5/6\)-density conclusions derived from that edge estimate;
- the apparent near-Mantel closure derived from those densities.

The valid replacement is the weaker but rigorous
\[
e(A,M)\ge d(d+1)/2
\]
and the universal
\[
d^-(x)\le(3d-3)/2.
\]

---

# 5. Matrix and Two-Path Assets

Let
\[
Q=A^2.
\]

## SUPPORTED — Reverse-arc annihilation
\[
\boxed{
Q_{xy}=0\quad\text{whenever }y\to x.
}
\]
Equivalently:
\[
\boxed{
A^2\circ A^{\mathsf T}=0.
}
\]

## SUPPORTED — Two-path conservation
Every row of \(Q\) sums to
\[
d^2,
\]
because each of the \(d\) outneighbors of \(x\) has outdegree \(d\):
\[
\boxed{
\sum_yQ_{xy}=d^2.
}
\]

Globally:
\[
\boxed{
\sum_{x,y}Q_{xy}=3d^3.
}
\]

## SUPPORTED — Nonadjacent endpoint escape mass
For fixed \(x\),
\[
\sum_{y\not\sim x}Q_{xy}
=d^2-e(D[N^+(x)])
\ge\frac{d(d+1)}2.
\]

Globally:
\[
\boxed{
E_2:=
\sum_{\substack{(x,y)\\x\not\sim y}}Q_{xy}
\ge
\frac{3d^2(d+1)}2.
}
\]

This identity is one of the main durable assets of the campaign.

---

# 6. Exact Number of Nonedges

Because \(D\) has \(3d^2\) arcs and no digons, it occupies exactly \(3d^2\) unordered adjacent pairs.

The total number of unordered pairs is
\[
\binom{3d}{2}.
\]

Therefore the number \(N_0\) of unordered nonadjacent pairs is:
\[
\boxed{
N_0=
\binom{3d}{2}-3d^2
=
\frac{3d(d-1)}2.
}
\]

This exact count is a key ingredient in the terminal \(C_4\) theorem.

---

# 7. Energy Assets

For each row \(x\), \(Q_{xy}=0\) on the diagonal and on every reverse-arc position \(y\to x\). Thus row \(x\) has at most
\[
k_x=3d-1-d^-(x)
\]
possible support positions.

Since its row sum is \(d^2\), Cauchy-Schwarz gives:
\[
\boxed{
\sum_yQ_{xy}^2
\ge
\frac{d^4}{3d-1-d^-(x)}.
}
\]

Summing:
\[
\boxed{
\|A^2\|_F^2
\ge
\sum_x\frac{d^4}{3d-1-d^-(x)}.
}
\]

Using convexity and average indegree \(d\):
\[
\boxed{
\|A^2\|_F^2
\ge
\frac{3d^5}{2d-1}.
}
\]

## SUPPORTED — Equality rigidity
Equality in the continuous row-energy floor would require:

1. all indegrees equal \(d\);
2. each row of \(A^2\) uniform on all legal support positions.

That uniform value would be
\[
\frac{d^2}{2d-1}.
\]

Because \(A^2\) is integral, exact equality would require
\[
2d-1\mid d^2.
\]
But
\[
\gcd(d,2d-1)=1,
\]
so \(2d-1\mid1\), forcing \(d=1\).

Hence for \(d>1\),
\[
\boxed{
\|A^2\|_F^2>
\frac{3d^5}{2d-1}.
}
\]

This is strict but does not by itself provide a proportional gap.

## SUPPORTED — Exact integer row-energy floor
For
\[
k_x=3d-1-d^-(x),
\]
write
\[
d^2=k_xq_x+t_x,\qquad 0\le t_x<k_x.
\]
Then the exact minimum squared norm of an integer row with sum \(d^2\) and support at most \(k_x\) is
\[
\boxed{
\sum_yQ_{xy}^2
\ge
(k_x-t_x)q_x^2+t_x(q_x+1)^2.
}
\]

This is a useful exact machine optimization primitive.

---

# 8. Spectral Assets

Because \(D\) is loopless, oriented, and directed-triangle-free:
\[
\boxed{\operatorname{tr}(A)=0,}
\]
\[
\boxed{\operatorname{tr}(A^2)=0,}
\]
\[
\boxed{\operatorname{tr}(A^3)=0.}
\]

Since
\[
A\mathbf1=d\mathbf1,
\]
\(d\) is an eigenvalue.

Let the remaining eigenvalues be
\[
\lambda_2,\dots,\lambda_{3d}.
\]
Then:
\[
\boxed{\sum_{i\ge2}\lambda_i=-d,}
\]
\[
\boxed{\sum_{i\ge2}\lambda_i^2=-d^2,}
\]
\[
\boxed{\sum_{i\ge2}\lambda_i^3=-d^3.}
\]

With
\[
\mu_i=\lambda_i/d,
\]
\[
\boxed{
\sum_{i\ge2}\mu_i
=
\sum_{i\ge2}\mu_i^2
=
\sum_{i\ge2}\mu_i^3
=-1.
}
\]

## SUPPORTED — Frobenius/singular-energy budget
Because \(A\) has exactly \(3d^2\) ones:
\[
\boxed{\|A\|_F^2=3d^2.}
\]

Since the Perron direction already contributes singular value at least \(d\):
\[
\sum_{i\ge2}s_i^2\le2d^2.
\]

Hence:
\[
\boxed{
\sum_{i\ge2}|\lambda_i|^2\le2d^2
}
\]
and
\[
\boxed{
\sum_{i\ge2}|\mu_i|^2\le2.
}
\]

## SUPPORTED — Cubic defect identities
Subtracting moment equations:
\[
\boxed{
\sum_{i\ge2}\mu_i(1-\mu_i)=0,
}
\]
\[
\boxed{
\sum_{i\ge2}\mu_i^2(1-\mu_i)=0,
}
\]
and therefore
\[
\boxed{
\sum_{i\ge2}\mu_i(1-\mu_i)^2=0.
}
\]

## FAILED ROUTE — spectrum-only closure
The complex unit disk has enough phase freedom that these finitely many moment constraints do not obviously contradict one another. Pointwise half-plane separation fails.

Conclusion: abstract eigenvalue moments alone do not close the kernel; entrywise support/eigenvector information is required.

---

# 9. Strong Connectivity and Periodicity

## SUPPORTED — Strong connectivity under minimality
In a smallest counterexample, choose a sink strongly connected component \(S\).

No arc leaves \(S\), so every \(v\in S\) retains all \(d\) outneighbors inside \(S\):
\[
\delta^+(D[S])\ge d.
\]

Since \(|S|\le3d\),
\[
d\ge |S|/3.
\]

If \(S\subsetneq V\), this contradicts minimality. Hence:
\[
\boxed{D\text{ is strongly connected}.}
\]

## SUPPORTED — Periodic cases eliminated
For a strongly connected \(d\)-out-regular digraph of period \(h\), cyclic classes must each have size at least \(d\). Since total size is \(3d\),
\[
h\le3.
\]

### \(h=3\)
All three classes have size exactly \(d\), and every vertex must hit all \(d\) vertices in the next class. This produces complete cyclic bipartite links and hence directed triangles. Impossible.

### \(h=2\)
The graph is bipartite. An oriented bipartite graph on \(3d\) vertices has at most
\[
\frac{(3d)^2}{4}=\frac94d^2
\]
arcs, but \(D\) has
\[
3d^2
\]
arcs. Impossible.

Therefore:
\[
\boxed{
D\text{ is primitive/aperiodic}.
}
\]

Consequently all non-Perron eigenvalues satisfy
\[
|\lambda_i|<d.
\]

## FAILED ROUTE — quantitative primitivity
Strict inequality alone is insufficient. A uniform spectral gap
\[
|\lambda_2|\le(1-\varepsilon)d
\]
was not proved.

---

# 10. Four-Flag / Chamber Assets

For a root \(x\), define cyclic chamber indicators:
\[
X_{ba}=1_{b\to a},\qquad
Y_{am}=1_{a\to m},\qquad
Z_{mb}=1_{m\to b}.
\]

Directed-triangle-freeness gives:
\[
\boxed{
\sum_{b,a,m}X_{ba}Y_{am}Z_{mb}=0.
}
\]

Using
\[
XYZ\ge X+Y+Z-2
\]
for \(0\)-\(1\) variables:
\[
\boxed{
m\,e(B,A)+r\,e(A,M)+d\,e(M,B)\le2drm.
}
\]

This is an exact necessary rooted four-flag inequality.

## SUPPORTED — Valid \(M\to B\) floor
Degree accounting gives:
\[
e(M,B)\ge e(A,M)-e(M).
\]
Using only
\[
e(M)\le\binom m2,
\]
\[
\boxed{
e(M,B)\ge
\max\left\{
0,\,
\frac{d(d+1)}2-\binom m2
\right\}.
}
\]

## SUPPORTED — Exact \(B\to A\) ledger
Every \(b\in B\) sends an arc to \(x\):
\[
rd=r+e(B)+e(B,A)+e(B,M).
\]
Thus
\[
\boxed{
e(B,A)=rd-r-e(B)-e(B,M).
}
\]

With
\[
e(B,M)+e(M,B)\le rm,
\]
\[
e(B,A)\ge rd-r-e(B)-rm+e(M,B).
\]

Using only \(e(B)\le\binom r2\) does not force a quadratic \(B\to A\) layer throughout the allowed range.

## Structural obstruction: backward reservoir
If \(e(B,A)\) is small, then
\[
e(B)+e(B,M)
\]
must be large.

Thus the missing degree can hide:

1. internally inside a nearly transitive/backward hierarchy on \(B\); or
2. in the wrong-direction bipartite reservoir \(B\to M\).

This was called the **Two-Reservoir Classification**.

## FAILED ROUTE
Pairwise chamber densities do not force the cyclic product positive. The counterexample can survive through anticorrelation and directional reservoirs.

---

# 11. Forbidden Rectangle Assets

For \(a\in A\), define
\[
M_a=N_M^+(a),\qquad
B_a=N_B^-(a).
\]

If
\[
b\to a\to m,
\]
then \(m\to b\) is forbidden, or else
\[
b\to a\to m\to b
\]
is a directed triangle.

Hence:
\[
\boxed{
e(M,B)
+
\left|
\bigcup_{a\in A}(M_a\times B_a)
\right|
\le mr.
}
\]

This is the **Forbidden-Rectangle Union Theorem**.

The route failed because:

- the large \(M_a\) can correlate negatively with large \(B_a\);
- even if the sum of rectangle areas is large, the rectangles can overlap heavily.

Thus a surviving counterexample can require simultaneous:

1. strong negative degree correlation;
2. strong rectangle overlap.

This is a precise obstruction, not a proof.

---

# 12. Maximum-Fan and Weighted-Fan Assets

For ordered pairs \((x,y)\), define:
\[
P_{xy}=N^+(x)\cap N^-(y),
\]
so
\[
|P_{xy}|=Q_{xy}.
\]

## Valid trivial/high-indegree fan floor
Choosing \(x\) with \(d^-(x)\ge d\), row-energy/support averaging yields:
\[
\max_yQ_{xy}\ge\frac{d^2}{2d-1}>\frac d2.
\]

Thus some two-path fan has size \(>d/2\).

## RETRACTED — \(0.686d\) fan
An attempted combination of
\[
q\ge\frac{d^2}{3d-1-d^-(x)}
\]
with an upper bound on \(d^-(x)\) substituted in the wrong inequality direction and produced
\[
q\gtrsim0.68614d.
\]

This was explicitly retracted.

Do not use it.

## SUPPORTED — Weighted fan averaging
Consider
\[
\sum_{x,y}\sum_{p\in P_{xy}}d^-(p).
\]

A fixed \(p\) belongs to exactly
\[
d^-(p)d^+(p)=d\,d^-(p)
\]
ordered fans, so
\[
\boxed{
\sum_{x,y}\sum_{p\in P_{xy}}d^-(p)
=
d\sum_p d^-(p)^2.
}
\]

By Cauchy:
\[
\sum_pd^-(p)^2\ge3d^3.
\]
Therefore:
\[
\boxed{
\sum_{x,y}\sum_{p\in P_{xy}}d^-(p)\ge3d^4.
}
\]

Also:
\[
\sum_{x,y}|P_{xy}|=3d^3.
\]

Hence some nonempty fan \(P=P_{xy}\) has average indegree at least \(d\):
\[
\boxed{
\frac1{|P|}\sum_{p\in P}d^-(p)\ge d.
}
\]

This is the **Weighted Maximum-Fan Selection** result.

## SUPPORTED — Fan inneighborhood compression
For a fan \(P\subseteq N^-(y)\), if \(z\to p\) for some \(p\in P\), then \(y\nrightarrow z\), or else
\[
z\to p\to y\to z
\]
is a triangle.

Thus:
\[
\bigcup_{p\in P}N^-(p)
\]
is disjoint from \(N^+(y)\), so its size is at most \(2d\).

Combined with average indegree \(\ge d\), this forces a vertex \(z\) hitting at least \(|P|/2\) vertices of \(P\).

Hence there is a set
\[
C\subseteq N^+(x)\cap N^+(z)\cap N^-(y)
\]
with
\[
|C|\ge|P|/2.
\]

This was called the **Dual Fan Theorem**.

## FAILED ROUTE
Applying hereditary minimum-outdegree deficit inside \(C\) creates a common-in/common-out forbidden rectangle, but the resulting inequalities remain feasible. The route folds back to a previously encountered rectangle boundary.

---

# 13. Common-In/Common-Out Rectangle Energy

For vertices \(x,z\), define:
\[
C_{xz}=N^+(x)\cap N^+(z),
\]
\[
I_{xz}=N^-(x)\cap N^-(z).
\]

If \(c\in C_{xz}\) and \(i\in I_{xz}\), then \(c\to i\) is forbidden:
\[
x\to c\to i\to x
\]
would be a directed triangle.

Hence:
\[
\boxed{E(C_{xz},I_{xz})=\varnothing.}
\]

A global quantity introduced was:
\[
T=
\sum_{x,z}|C_{xz}|\,|I_{xz}|.
\]

This is related to two-path/common-neighborhood energy and was proposed as a route to a global contradiction.

No sufficiently strong upper bound from the empty rectangles was proved.

---

# 14. Terminal Fourth-Moment Theorem — Strongest Audited Asset

This is the main theorem to take to the machine.

## THEOREM — Cubic Directed-\(C_4\) Lower Bound

Let \(D\) be an oriented graph on \(3d\) vertices. Suppose:

- every vertex has outdegree exactly \(d\);
- \(D\) contains no directed triangle.

Then:
\[
\boxed{
C_4(D)\ge
\left\lceil\frac{3d^3}{2}\right\rceil,
}
\]
where \(C_4(D)\) is the number of directed \(4\)-cycles counted up to cyclic rotation.

Equivalently:
\[
\boxed{
\operatorname{tr}(A^4)\ge6d^3.
}
\]

### Proof asset A — opposite two-path variables
For each unordered nonedge \(\{x,y\}\), define:
\[
a_{xy}=Q_{xy},\qquad b_{xy}=Q_{yx}.
\]
Since every vertex has \(d\) outneighbors:
\[
0\le a_{xy},b_{xy}\le d.
\]

Therefore:
\[
(d-a_{xy})(d-b_{xy})\ge0,
\]
so:
\[
\boxed{
a_{xy}b_{xy}\ge d(a_{xy}+b_{xy}-d).
}
\]

### Proof asset B — sum over nonedges
From the escape-mass theorem:
\[
\sum_{\{x,y\}\text{ nonedge}}(a_{xy}+b_{xy})
\ge
\frac{3d^2(d+1)}2.
\]

The number of unordered nonedges is:
\[
N_0=\frac{3d(d-1)}2.
\]

Hence:
\[
\begin{aligned}
\sum_{\{x,y\}\text{ nonedge}}a_{xy}b_{xy}
&\ge
d\left(
\frac{3d^2(d+1)}2
-
d\frac{3d(d-1)}2
\right)\\
&=
3d^3.
\end{aligned}
\]

Thus:
\[
\boxed{
\sum_{\{x,y\}\text{ nonedge}}
Q_{xy}Q_{yx}
\ge3d^3.
}
\]

### Proof asset C — conversion to \(C_4\)
A choice counted by
\[
Q_{xy}Q_{yx}
\]
gives:
\[
x\to u\to y\to v\to x.
\]

The four vertices are distinct:

- \(x\ne y\);
- \(u,v\notin\{x,y\}\);
- \(u\ne v\), otherwise \(u\leftrightarrow y\) would be a digon.

Thus it is a genuine directed \(4\)-cycle.

Every directed \(4\)-cycle has exactly two unordered opposite pairs, so:
\[
\boxed{
\sum_{\{x,y\}\text{ nonedge}}Q_{xy}Q_{yx}
=
2C_4(D).
}
\]

Therefore:
\[
2C_4(D)\ge3d^3,
\]
and:
\[
\boxed{
C_4(D)\ge\frac{3d^3}{2}.
}
\]

Since \(C_4(D)\in\mathbb Z\):
\[
\boxed{
C_4(D)\ge
\left\lceil\frac{3d^3}{2}\right\rceil.
}
\]

Finally:
\[
\operatorname{tr}(A^4)=4C_4(D),
\]
so:
\[
\boxed{
\operatorname{tr}(A^4)\ge6d^3.
}
\]

---

# 15. Consequences of the Cubic \(C_4\) Theorem

## SUPPORTED — Every hypothetical kernel contains directed \(C_4\)s
For \(d\ge1\),
\[
C_4(D)>0.
\]

Thus every hypothetical exact-boundary regular triangle-free counterexample contains a directed \(4\)-cycle.

## SUPPORTED — Heavy four-cycle vertex
Let \(c_4(x)\) count directed \(4\)-cycles containing \(x\). Then:
\[
\sum_xc_4(x)=4C_4(D).
\]

Using \(n=3d\):
\[
\frac1{3d}\sum_xc_4(x)
\ge2d^2.
\]

Hence some vertex lies on at least:
\[
\boxed{2d^2}
\]
directed \(4\)-cycles.

Equivalently, for some \(x\):
\[
\boxed{
\sum_yQ_{xy}Q_{yx}\ge2d^2.
}
\]

## SUPPORTED — Heavy bidirectional bridge
A heavy vertex \(x\) has at most
\[
2d-1
\]
nonneighbors. Hence some nonneighbor \(y\) satisfies:
\[
\boxed{
Q_{xy}Q_{yx}
\ge
\frac{2d^2}{2d-1}.
}
\]

With integrality:
\[
\boxed{
Q_{xy}Q_{yx}
\ge
\left\lceil\frac{2d^2}{2d-1}\right\rceil.
}
\]

Define:
\[
P=N^+(x)\cap N^-(y),
\]
\[
R=N^+(y)\cap N^-(x).
\]

Then:
\[
|P||R|=Q_{xy}Q_{yx}.
\]

Every \((p,r)\in P\times R\) gives a directed \(4\)-cycle
\[
x\to p\to y\to r\to x.
\]

Triangle-freeness implies:
\[
\boxed{E(P,R)=\varnothing,}
\]
while arcs \(R\to P\) may exist.

## FAILED CLOSE
The product lower bound is only \(\Omega(d)\), not \(\Omega(d^2)\). It permits asymmetric profiles such as:
\[
Q_{xy}\approx d,\qquad Q_{yx}=O(1).
\]

Thus cubic total \(C_4\) mass does not automatically produce a pair with both opposite two-path counts linear in \(d\).

This is the **asymmetric four-cycle reservoir** obstruction.

---

# 16. Exact Symmetric/Skew Two-Path Decomposition

Let:
\[
S=Q+Q^{\mathsf T},
\qquad
K=Q-Q^{\mathsf T}.
\]

For each pair:
\[
4Q_{xy}Q_{yx}
=
S_{xy}^2-K_{xy}^2.
\]

Globally:
\[
\boxed{
\operatorname{tr}(A^4)
=
\|Q\|_F^2
-\frac12\|Q-Q^{\mathsf T}\|_F^2.
}
\]

Since \(Q=A^2\):
\[
\boxed{
\operatorname{tr}(A^4)
=
\|A^2\|_F^2
-
\frac12
\left\|
A^2-(A^{\mathsf T})^2
\right\|_F^2.
}
\]

Equivalently:
\[
\boxed{
C_4(D)
=
\frac14\|A^2\|_F^2
-
\frac18
\left\|
A^2-(A^{\mathsf T})^2
\right\|_F^2.
}
\]

This is a central exact identity from the terminal encirclement.

## Interpretation
The fourth-cycle mass is exactly:

> total two-path energy minus the penalty for directional asymmetry.

The remaining obstruction is therefore measurable:
\[
\boxed{
\left\|A^2-(A^{\mathsf T})^2\right\|_F^2.
}
\]

A hypothetical counterexample can survive the large two-path energy by storing enough of it asymmetrically.

---

# 17. Exact Flagship Closure Boundary

The session does **not** prove:
\[
\delta^+(D)\ge n/3\implies C_3^\to\subseteq D.
\]

The strongest audited theorem is conditional on the exact-boundary regular kernel.

A complete CH3 proof still needs a valid contradiction from that kernel.

One concrete terminal formulation is:

> **Fourth-Moment Closure Obligation.**  
> Show that no triangle-free oriented \(d\)-out-regular graph on \(3d\) vertices can satisfy the complete collection of kernel identities together with
> \[
> \operatorname{tr}(A^4)\ge6d^3.
> \]

The bare implication
\[
\operatorname{tr}(A^4)\ge6d^3
\implies C_3^\to
\]
has **not** been proved and should not be assumed.

A more structurally faithful formulation is:

> **Skew-Energy Closure Obligation.**  
> Derive, from orientation, out-regularity, triangle-freeness, minimality, and the entrywise support constraints, an upper/lower bound on
> \[
> \|A^2-(A^{\mathsf T})^2\|_F^2
> \]
> incompatible with the fourth-moment and two-path-energy identities.

This is an obligation, not a theorem.

---

# 18. Complete Named-Theorem Ledger from the Session

The following names appeared during the campaign. Statuses below are the authoritative extraction.

## Valid / supported or supported under explicit minimal-counterexample hypotheses

- **Corrected High-Root Barrier** — only the corrected limited-root logic survived conceptually; the \(7/6\) numerical barrier did not.
- **\(A\to B\) Zero Theorem / Outneighborhood Wall Theorem** — SUPPORTED.
- **Local Defect Identity** — SUPPORTED.
- **Reverse-Arc Annihilation Theorem** — SUPPORTED.
- **Two-Path Conservation Theorem** — SUPPORTED.
- **Valid Indegree Ceiling** — SUPPORTED:
  \[
  d^-(x)\le(3d-3)/2.
  \]
- **Rooted Chamber Equations** — SUPPORTED.
- **Rooted Cyclic Product-Zero Theorem** — SUPPORTED.
- **Tripartite Union-Bound Theorem** — SUPPORTED.
- **Valid \(M\to B\) Floor** — SUPPORTED.
- **Exact \(B\to A\) Ledger** — SUPPORTED.
- **Backward Reservoir Theorem** — structural equality/dichotomy, SUPPORTED.
- **Backward-Hierarchy Theorem** — the peeling-order interpretation is valid, but it does not bound total internal arcs.
- **Two-Reservoir Classification Theorem** — SUPPORTED as a structural classification from the ledger.
- **Forbidden-Rectangle Union Theorem** — SUPPORTED.
- **First Three Vanishing Trace Theorem** — SUPPORTED.
- **Perron Moment Cancellation Theorem** — SUPPORTED.
- **Singular-Energy Budget Theorem** — SUPPORTED.
- **Spectral Modulus Budget** — SUPPORTED.
- **Cubic Defect Identity** — SUPPORTED.
- **Peripheral Period Theorem** — standard Perron-Frobenius structure, used correctly under irreducibility.
- **Strong Connectivity Theorem** — SUPPORTED under minimal-counterexample setup.
- **Aperiodicity Theorem** — SUPPORTED under the same setup.
- **Strict Spectral Radius Gap** — SUPPORTED qualitatively for the primitive matrix.
- **Energy Equality Rigidity Theorem** — SUPPORTED.
- **Exact Integral Row-Energy Floor** — SUPPORTED.
- **Weighted Maximum-Fan Selection** — SUPPORTED.
- **Dual Fan Theorem** — SUPPORTED as derived from the weighted fan incidence argument.
- **Opposite Two-Path Product Theorem** — SUPPORTED.
- **Opposite Vertices Are Nonadjacent** — SUPPORTED.
- **Exact Nonedge Count** — SUPPORTED.
- **Escape-Mass Floor** — SUPPORTED.
- **Forced Opposite-Path Product Theorem** — SUPPORTED.
- **Cubic Directed-\(C_4\) Theorem** — SUPPORTED; flagship session theorem.
- **Every Counterexample Contains a Directed \(C_4\)** — SUPPORTED under kernel hypotheses.
- **Heavy Four-Cycle Vertex Theorem** — SUPPORTED.
- **Heavy Bidirectional Bridge Theorem** — SUPPORTED.
- **Exact Fourth-Moment Decomposition** — SUPPORTED.

## Retractions / invalidated claims

- **Exact Hereditary Edge Bound** — RETRACTED.
- **Hereditarily Sharpened Fan Capacity Theorem** — RETRACTED insofar as it used the false edge bound.
- **Five-Sixths Escape Theorem** — RETRACTED.
- **Five-Sixths Bridge Theorem** — RETRACTED.
- **Hereditary Bridge Export Theorem** — RETRACTED.
- **Seven-Sixths Indegree Barrier** — RETRACTED.
- **Three-Layer Density Ledger** using \(F(s)\) — RETRACTED.
- **Mantel near-close based on that ledger** — RETRACTED as a CH proof route.
- **\(0.68614d\) maximum-fan bound** — RETRACTED due to inequality-direction error.

## Proposals / non-theorems

- **Global Folding Exclusion Theorem** — closure target, NOT PROVED.
- **Five-Flag Necessity Theorem** — methodological claim, not a mathematical closure theorem.
- **Pair-Marginal Phantom Theorem** — should be treated as an obstruction model/heuristic, not a formal existence theorem unless separately constructed.
- **Abstract Spectral Phantom** — feasibility observation, not a CH theorem.
- **Asymmetric Four-Cycle Reservoir Theorem** — structural possibility/obstruction description; not an existence theorem for a full counterexample.
- **Machine Closure Contract** — protocol, not a mathematical theorem.
- **Fourth-Moment Closure Obligation** — OPEN obligation.
- **Skew-Energy Closure Obligation** — OPEN obligation.

---

# 19. Failed Kill Shots and What Each Taught Us

## A. Hereditary-density / peeling route
**Failure:** one-sided residual outdegree does not count backward arcs.

**Lesson:** never convert hereditary minimum-outdegree failure into total induced-edge sparsity without a genuinely two-sided argument.

## B. Three-chamber Mantel route
**Failure:** its strongest densities depended on the false hereditary edge bound.

**Lesson:** the apparent near-close was an artifact of an invalid density upgrade.

## C. Whole-chamber tripartite extremal route
**Failure:** triangle-free subgraphs of a complete tripartite host may split chambers; whole-chamber cuts are not automatically extremal upper bounds.

## D. Forbidden rectangle union
**Failure:** anticorrelation plus rectangle overlap can keep the union small.

## E. Peeling cascade
**Failure:** escape sets can fold back into previously exposed regions; the elimination order does not delete those vertices from the original graph.

## F. Maximum two-path fan
**Failure:** the attempted \(0.686d\) strengthening used an inequality in the wrong direction.

## G. Spectrum-only moments
**Failure:** complex phase freedom permits the first three power-sum identities abstractly.

## H. Periodicity
**Success:** period \(2\) and \(3\) are eliminated under strong connectivity. The kernel must be primitive.

## I. Energy equality
**Success:** exact uniform-support equality is arithmetically impossible for \(d>1\).

**Failure:** strictness alone is too small to close.

## J. Fourth moment
**Success:** forces
\[
C_4(D)\ge3d^3/2.
\]

**Failure:** total \(C_4\) mass can be distributed through highly asymmetric opposite two-path pairs.

---

# 20. Machine Verification Checklist

The highest-priority verification target is the cubic \(C_4\) theorem.

Given a \(0\)-\(1\) matrix \(A\):

1. Verify square dimension \(n\).
2. Verify zero diagonal.
3. Verify:
   \[
   A_{ij}A_{ji}=0
   \]
   for all \(i\ne j\).
4. Verify all row sums equal \(d\).
5. Verify:
   \[
   n=3d.
   \]
6. Verify directed-triangle-freeness, e.g.
   \[
   \operatorname{tr}(A^3)=0.
   \]
7. Compute:
   \[
   Q=A^2.
   \]
8. Verify:
   \[
   Q_{xy}=0
   \]
   whenever \(y\to x\).
9. Enumerate unordered nonedges.
10. Verify:
    \[
    N_0=\frac{3d(d-1)}2.
    \]
11. For every \(x\), verify:
    \[
    \sum_{y\not\sim x}Q_{xy}
    =
    d^2-e(D[N^+(x)])
    \ge\frac{d(d+1)}2.
    \]
12. Verify:
    \[
    \sum_{\{x,y\}\text{ nonedge}}(Q_{xy}+Q_{yx})
    \ge\frac{3d^2(d+1)}2.
    \]
13. Verify pointwise:
    \[
    Q_{xy}Q_{yx}
    \ge
    d(Q_{xy}+Q_{yx}-d).
    \]
14. Sum to obtain:
    \[
    \sum_{\{x,y\}\text{ nonedge}}Q_{xy}Q_{yx}\ge3d^3.
    \]
15. Verify:
    \[
    \operatorname{tr}(A^4)
    =
    2\sum_{\{x,y\}\text{ nonedge}}Q_{xy}Q_{yx}.
    \]
16. Conclude:
    \[
    \operatorname{tr}(A^4)\ge6d^3.
    \]
17. Equivalently:
    \[
    C_4(D)\ge\left\lceil3d^3/2\right\rceil.
    \]

All of these steps are integer-exact.

---

# 21. Lean Formalization Queue

Recommended lemma decomposition:

1. `oriented_no_reverse_pair`
2. `triangle_free_no_outnbr_to_innbr`
3. `two_path_matrix_entry`
4. `two_path_row_sum`
5. `escape_two_path_mass_vertex`
6. `unordered_nonedge_count`
7. `opposite_path_product_pointwise`
8. `opposite_path_product_sum`
9. `opposite_two_paths_have_four_distinct_vertices`
10. `opposite_two_paths_form_directed_four_cycle`
11. `directed_four_cycle_has_two_opposite_pairs`
12. `trace_four_eq_four_mul_cycle_count`
13. `cubic_directed_C4_lower_bound`
14. `heavy_C4_vertex`
15. `heavy_bidirectional_bridge`
16. `two_path_symmetric_skew_decomposition`

For the first kernel formalization, the trace version may be simpler than quotienting cycles modulo cyclic rotation:
\[
\boxed{\operatorname{tr}(A^4)\ge6d^3.}
\]

---

# 22. Computational / Search Program Suggested by the Assets

This is not a route change; it is the direct machine interrogation of the surviving kernel.

## A. Exact finite feasibility
For small \(d\), enumerate or SAT/CP-SAT solve:
\[
n=3d,\quad d^+=d,\quad \text{oriented},\quad C_3^\to\text{-free}.
\]

Measure:

- indegree distribution;
- \(Q=A^2\);
- \(\|Q\|_F^2\);
- \(\operatorname{tr}(A^4)\);
- skew energy
  \[
  \|Q-Q^{\mathsf T}\|_F^2;
  \]
- distribution of
  \[
  (Q_{xy},Q_{yx})
  \]
  over nonedges;
- maximum/minimum products;
- common-in/common-out rectangle sizes;
- fan incidence statistics.

## B. Optimize the actual missing quantity
Optimize:
\[
\left\|A^2-(A^{\mathsf T})^2\right\|_F^2
\]
over the bounded kernel.

The goal is to infer a rational inequality strong enough to combine with:
\[
\operatorname{tr}(A^4)
=
\|A^2\|_F^2-\frac12\|Q-Q^{\mathsf T}\|_F^2
\]
and the exact lower bounds.

## C. Counterexample hunt for intermediate claims
Any proposed skew-energy, fan-symmetry, or rectangle inequality should first be attacked by SAT/ILP/random/local search before being admitted to the theorem bank.

## D. Flag certificate
If bounded data suggests a universal inequality, encode it as a rational flag/SDP certificate and then translate the final certificate to exact rational arithmetic.

---

# 23. Novelty / Literature-Check Queue

No historical novelty claim is made here.

After machine verification, check the following independently:

1. Is the exact bound
   \[
   C_4(D)\ge\lceil3d^3/2\rceil
   \]
   for triangle-free \(d\)-out-regular oriented graphs on \(3d\) vertices already known?
2. Is the equivalent trace inequality
   \[
   \operatorname{tr}(A^4)\ge6d^3
   \]
   present in the CH literature?
3. Is the nonedge opposite-path inequality
   \[
   \sum_{\{x,y\}\text{ nonedge}}Q_{xy}Q_{yx}\ge3d^3
   \]
   known in this exact form?
4. Are the heavy-vertex and heavy-bidirectional-bridge corollaries known?
5. Has the symmetric/skew decomposition been explicitly used in CH:
   \[
   \operatorname{tr}(A^4)
   =
   \|A^2\|_F^2-\frac12\|A^2-(A^{\mathsf T})^2\|_F^2?
   \]
6. Is there an existing extremal upper bound on skew two-path energy for triangle-free oriented graphs at density \(1/3\)?
7. Do known flag-algebra certificates implicitly contain the cubic \(C_4\) inequality?

Novelty should be recorded only after this check.

---

# 24. Highest-Value Theorem Bank

If only a compact bank is retained, keep these:

### TB-1 — Outneighborhood wall
\[
E(N^+(x),N^-(x))=\varnothing.
\]

### TB-2 — Escape identity
\[
e(N^+(x),M_x)
=
d^2-e(D[N^+(x)])
\ge\frac{d(d+1)}2.
\]

### TB-3 — Indegree ceiling
\[
d^-(x)\le\frac{3d-3}{2}.
\]

### TB-4 — Reverse-arc annihilation
\[
A^2\circ A^{\mathsf T}=0.
\]

### TB-5 — Two-path row conservation
\[
A^2\mathbf1=d^2\mathbf1.
\]

### TB-6 — Global escape two-path mass
\[
\sum_{x\not\sim y}(A^2)_{xy}
\ge\frac{3d^2(d+1)}2.
\]

### TB-7 — Exact nonedge count
\[
N_0=\frac{3d(d-1)}2.
\]

### TB-8 — Cubic opposite-path product
\[
\sum_{\{x,y\}\text{ nonedge}}
(A^2)_{xy}(A^2)_{yx}
\ge3d^3.
\]

### TB-9 — Cubic directed-\(C_4\) theorem
\[
C_4(D)\ge\left\lceil\frac{3d^3}{2}\right\rceil.
\]

### TB-10 — Fourth trace bound
\[
\operatorname{tr}(A^4)\ge6d^3.
\]

### TB-11 — Two-path energy floor
\[
\|A^2\|_F^2
\ge\frac{3d^5}{2d-1},
\]
strict for \(d>1\).

### TB-12 — Exact skew decomposition
\[
\operatorname{tr}(A^4)
=
\|A^2\|_F^2
-\frac12
\|A^2-(A^{\mathsf T})^2\|_F^2.
\]

### TB-13 — Strong connectivity of a minimal counterexample
Under the minimality reduction:
\[
D\text{ is strongly connected}.
\]

### TB-14 — Aperiodicity of a minimal counterexample
Under the same reduction:
\[
D\text{ is primitive}.
\]

### TB-15 — Weighted fan selection
Some two-path fan \(P\) satisfies:
\[
\frac1{|P|}\sum_{p\in P}d^-(p)\ge d.
\]

---

# 25. Red-Team Warnings to Preserve Permanently

1. **Never reuse the false hereditary edge bound.**
2. **Never reuse the \(5/6\) escape density derived from it.**
3. **Never reuse the \(7/6\) indegree barrier.**
4. **Never reuse the \(0.68614d\) fan bound.**
5. A peeling order controls forward arcs, not total arcs.
6. Large total \(C_4\) mass does not imply a large-large opposite two-path pair.
7. Whole-chamber cuts are not automatically extremal in a tripartite triangle-free host.
8. Strict Perron spectral gap is not a quantitative spectral gap.
9. Pairwise densities do not capture correlation/overlap.
10. Do not label CH3 closed unless the exact final contradiction is independently machine checked.

---

# 26. Campaign Court Status

## Flagship
\[
\boxed{\text{Caccetta–Häggkvist directed-triangle case: NOT CLOSED.}}
\]

## Strongest audited theorem
\[
\boxed{
C_4(D)\ge
\left\lceil\frac{3d^3}{2}\right\rceil
}
\]
for every triangle-free oriented \(d\)-out-regular graph on \(3d\) vertices.

Equivalent:
\[
\boxed{
\operatorname{tr}(A^4)\ge6d^3.
}
\]

## Most important exact surviving obstruction
The two-path matrix can be strongly asymmetric:
\[
Q_{xy}\gg Q_{yx}
\]
on many nonedges while still producing the required total fourth-moment mass.

The asymmetry is measured exactly by:
\[
\boxed{
\|A^2-(A^{\mathsf T})^2\|_F^2.
}
\]

## Direct closure cut
Derive an inequality from the full kernel that makes:
\[
\operatorname{tr}(A^4)
=
\|A^2\|_F^2
-\frac12\|A^2-(A^{\mathsf T})^2\|_F^2
\]
incompatible with:
\[
\operatorname{tr}(A^4)\ge6d^3
\]
and the exact row/support/degree constraints.

---

# 27. One-Page Handoff to the Next Agent

**Problem:** Prove CH3:
\[
\delta^+(D)\ge n/3\Rightarrow C_3^\to.
\]

**Exact-boundary kernel:** work with a hypothetical triangle-free oriented graph on \(n=3d\) vertices with:
\[
d^+(v)=d.
\]

**Do not use:** hereditary total-edge sparsity, \(5/6\) escape, \(7/6\) indegree, or \(0.686d\) fan; all were retracted.

**Valid core:**
\[
E(N^+(x),N^-(x))=\varnothing,
\]
\[
e(N^+(x),M_x)\ge d(d+1)/2,
\]
\[
d^-(x)\le(3d-3)/2,
\]
\[
A^2\circ A^{\mathsf T}=0,
\]
\[
A^2\mathbf1=d^2\mathbf1.
\]

**Strongest new session theorem to verify first:**
\[
\boxed{
C_4(D)\ge\left\lceil3d^3/2\right\rceil
}
\]
or
\[
\boxed{\operatorname{tr}(A^4)\ge6d^3.}
\]

**Proof spine:**
\[
\sum_{x\not\sim y}Q_{xy}
\ge\frac{3d^2(d+1)}2,
\]
\[
N_0=\frac{3d(d-1)}2,
\]
\[
(d-Q_{xy})(d-Q_{yx})\ge0,
\]
hence
\[
\sum_{\{x,y\}\text{ nonedge}}Q_{xy}Q_{yx}\ge3d^3,
\]
and each directed \(C_4\) is counted by its two opposite pairs.

**Exact surviving identity:**
\[
\boxed{
\operatorname{tr}(A^4)
=
\|A^2\|_F^2
-\frac12\|A^2-(A^{\mathsf T})^2\|_F^2.
}
\]

**Mission:** control the skew two-path energy from the existing kernel strongly enough to force contradiction. Test every proposed inequality computationally before banking it.

**Court:** flagship open; cubic \(C_4\) theorem is the principal machine-verification asset.

---

# 28. Final Extraction Verdict

This session did not produce a proof of CH3.

It did produce a substantial audited theorem bank, a complete record of the false branches that must never be reused, and one especially clean machine-checkable structural theorem:

\[
\boxed{
\text{Triangle-free + }|V|=3d+\text{ outdegree }d
\quad\Longrightarrow\quad
C_4(D)\ge\left\lceil\frac{3d^3}{2}\right\rceil.
}
\]

The session's most important conceptual compression is:

\[
\boxed{
\text{CH3 survival requires large two-path mass AND large directional asymmetry.}
}
\]

The first is forced. The second is the surviving escape mechanism.

That is the estate to bank, verify, novelty-check, and feed back into the Oracle.
