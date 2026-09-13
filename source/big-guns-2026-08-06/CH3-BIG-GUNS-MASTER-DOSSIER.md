# Caccetta–Häggkvist Directed-Triangle Campaign
## BIG-GUNS Full Asset Extraction — Entire Session

**Date:** 2026-08-06  
**Campaign:** Caccetta–Häggkvist, directed-triangle case  
**Owner/Operator:** Jared Wilder  
**Extraction mode:** Court-separated theorem estate, full round chronology, machine-ingestible asset bank  
**Flagship status:** **OPEN — NOT CLOSED IN THIS SESSION**

---

# 0. What This Bundle Is

This is the complete mathematical estate of the thought exercise, not a short handoff.

It includes:

- every named theorem, lemma, candidate, obstruction, and protocol item from all fifteen rounds;
- theorem-number collisions preserved by round-qualified IDs;
- exact Court status for each item;
- the full retraction chain and every dependent result that must never be reused;
- detailed proofs of the strongest surviving results;
- all machine-checkable formulas;
- the exact missing closure obligation;
- Lean and finite-search plans;
- a publication-outline asset;
- JSON ledgers for deterministic ingestion.

The source session repeatedly attempted the flagship close. It did **not** establish the Caccetta–Häggkvist triangle case. The principal surviving theorem is:

\[
\boxed{C_4(D)\ge\left\lceil\frac{3d^3}2\right\rceil}
\]
for every triangle-free oriented \(d\)-out-regular graph on \(3d\) vertices, equivalently:
\[
\boxed{\operatorname{tr}(A^4)\ge6d^3.}
\]

This theorem remains subject to independent machine verification and historical novelty review.

---

# 1. Source-Bound Flagship

Let \(D\) be a finite oriented graph on \(n\) vertices. The flagship is:
\[
\delta^+(D)\ge\frac n3
\quad\Longrightarrow\quad
D\text{ contains a directed triangle}.
\]

The exact-boundary kernel used throughout the later campaign is:
\[
n=3d,\qquad d^+(v)=d\ \forall v,
\]
together with:
\[
A\circ A^{\mathsf T}=0,
\qquad
A^2\circ A^{\mathsf T}=0.
\]

The campaign's true closure cut is:

> Prove that no exact-boundary regular triangle-free oriented kernel exists.

No adjacent result, architecture, or theorem volume substitutes for this.

---

# 2. Executive Court Verdict

## Flagship
`NOT CLOSED`

## Principal supported mathematical asset
**Cubic Directed-\(C_4\) Theorem**
\[
C_4(D)\ge\left\lceil\frac{3d^3}2\right\rceil.
\]

## Equivalent trace form
\[
\operatorname{tr}(A^4)\ge6d^3.
\]

## Principal surviving identity
\[
\operatorname{tr}(A^4)
=
\|A^2\|_F^2
-\frac12
\|A^2-(A^{\mathsf T})^2\|_F^2.
\]

## Exact surviving mechanism
Large two-path mass is mandatory, but it may be stored directionally:
\[
(A^2)_{xy}\gg(A^2)_{yx}
\]
on many nonedges.

## Exact missing obligation
Control the skew two-path energy
\[
\|A^2-(A^{\mathsf T})^2\|_F^2
\]
strongly enough to make the full exact-boundary kernel infeasible.

---

# 3. Full Round-by-Round Chronicle

## Round 1

Established the first local geometry: outneighborhood-to-inneighborhood exclusion, escape mass, and the hereditary deficit of a smallest counterexample. The route became a pair-cell expansion attack.

- **R1-L1 — Neighborhood Acyclicity Pressure** — `SUPPORTED`: For every v, D[N+(v)] and D[N-(v)] are directed-triangle-free; for every arc v→x, N+(x)∩N-(v)=∅.
- **R1-L2 — Half-Degree Escape Lemma** — `SUPPORTED`: For a minimum-outdegree vertex v with d=δ+(D), some x∈N+(v) has at least (d+1)/2 outneighbors in M_v.
- **R1-L3 — Minimal-Counterexample Hereditary Deficit** — `SUPPORTED_CONDITIONAL`: In a vertex-minimal counterexample, every proper nonempty S has a vertex x with d_S^+(x)<|S|/3.
- **R1-ME — Minimal Escape Lemma** — `SUPPORTED_CONDITIONAL`: For every proper nonempty S, some x∈S has d^+_{V\S}(x)>d-|S|/3.

## Round 2

Arc-minimal regularization and exact escape were combined with two successive forbidden walls. The first precise obstruction was identified: later escape layers may fold into earlier forward layers.

- **T1 — Arc-Minimal Regularization Theorem** — `SUPPORTED_CONDITIONAL`: After choosing a counterexample with minimum order and then minimum arcs, every vertex has outdegree d=ceil(n/3).
- **T2 — Forbidden Residue Theorem** — `SUPPORTED_CONDITIONAL`: A vertex-minimal counterexample cannot have n≡1 mod 3.
- **T3 — Universal Minimum-Tail Theorem** — `SUPPORTED_CONDITIONAL`: Every vertex has an incoming tail of minimum outdegree; in the arc-minimal kernel this is automatic because all vertices have outdegree d.
- **T4 — Hereditary Deficit Theorem** — `SUPPORTED_CONDITIONAL`: Every proper nonempty induced subgraph has minimum outdegree below one third of its order.
- **T5 — Exact Escape Theorem** — `SUPPORTED_CONDITIONAL`: For every proper nonempty S, some x∈S has d^+_{V\S}(x)≥d-ceil(|S|/3)+1.
- **T6 — A-to-B Exclusion Theorem** — `SUPPORTED`: For A=N+(v), B=N-(v), E(A,B)=∅.
- **T7 — Quadratic Escape-Mass Theorem** — `SUPPORTED`: For |A|=d, e(A,M_v)≥d(d+1)/2 and hence |M_v|≥(d+1)/2.
- **T8 — Two-Thirds Escape Vertex Theorem** — `SUPPORTED_CONDITIONAL`: Some x∈A has |N_M^+(x)|≥d-ceil(d/3)+1>2d/3.
- **T9 — Second-Generation Forbidden-Indegree Theorem** — `SUPPORTED`: If X=N_M^+(x), then for z∈X, N+(z)∩N-(x)=∅.
- **T10 — Second-Escape Compression Theorem** — `SUPPORTED_CONDITIONAL`: Applying hereditary deficit to X yields z∈X with a large external outneighbor set W=N+(z)\X, disjoint from N-(x).
- **T11 — Pair-Cell Indegree Ceiling** — `SUPPORTED_CONDITIONAL`: For the selected x and X, d^-(x)≤n-d-|X|+ceil(|X|/3)-2.
- **T12 — Layer-Folding Obstruction Theorem** — `STRUCTURAL_DIAGNOSIS`: Naive recursive escape fails because later forward layers may overlap older forward layers; only immediate backward walls are forbidden.
- **CA — Candidate A — Fold-or-Triangle Lemma** — `PROPOSAL`: A large overlap of a new escape layer with earlier layers should either force a triangle or pay an explicit expansion penalty.
- **CB — Candidate B — Selected-Vertex Indegree Floor** — `PROPOSAL`: Select a low-internal-outdegree x with an unusually large indegree sufficient to contradict T11.
- **CC — Candidate C — Weighted Pair-Cell Inequality** — `PROPOSAL`: Sum pair-cell inequalities over many low-internal-degree vertices instead of selecting one vertex.

## Round 3

Global two-path accounting converted lost transitive closure into escape mass. A large nonedge bridge and a one-way H→P rectangle emerged, but the rectangle could serve as a degree reservoir.

- **T13 — Universal Three-Chamber Theorem** — `SUPPORTED`: For each x, V\{x} partitions into P_x=N+(x), I_x=N-(x), M_x, and E(P_x,I_x)=∅.
- **T14 — Exact Escape-Slack Identity** — `SUPPORTED`: If σ(x)=binom(d,2)-e(P_x), then e(P_x,M_x)=d(d+1)/2+σ(x).
- **T15 — Nonneighbor Capacity Theorem** — `SUPPORTED`: |M_x|≥(d+1)/2+σ(x)/d, hence an indegree upper bound follows.
- **T16 — Global Nonneighbor Conservation Theorem** — `SUPPORTED`: Σ_x |M_x|=n(n-1-2d); at n=3d the average is d-1.
- **T17 — Global Defect Budget Theorem** — `SUPPORTED`: Σ_xσ(x) is bounded by the global nonneighbor budget; at n=3d, Σσ(x)≤nd(d-3)/2.
- **T18 — Directed Two-Path Classification Theorem** — `SUPPORTED`: Every directed two-path x→p→y is either transitively closed by x→y or has nonadjacent endpoints; y→x is forbidden.
- **T19 — Global Escape-Path Theorem** — `SUPPORTED`: The total escape two-path count is nd(d+1)/2+Σσ(x).
- **T20 — Common-Inneighborhood Identity** — `SUPPORTED`: Σ_{p→y}|N-(p)∩N-(y)|=nd(d-1)/2-Σσ(x).
- **T21 — Folding Conservation Theorem** — `SUPPORTED`: Transitive two-path mass plus escape two-path mass equals nd²; lost transitive closure becomes escape mass one-for-one.
- **T22 — High-Multiplicity Escape Pair Theorem** — `SUPPORTED`: At n=3d some ordered nonadjacent pair has q(x,y)≥ceil(d(d+1)/(2(d-1)))>d/2+1.
- **T23 — Parallel-Bridge Chamber Theorem** — `SUPPORTED`: For P=N+(x)∩N-(y), E(P,N-(x))=∅ and E(N+(y),P)=∅.
- **T24 — Rectangle-to-C4 Theorem** — `SUPPORTED`: For H=N+(y)∩N-(x), every (p,h)∈P×H yields x→p→y→h→x; the pair lies in |P||H| directed 4-cycles.
- **T25 — Fold-or-Expansion Theorem** — `SUPPORTED_DICHOTOMY`: For any η, either |H|<ηd and L∪R expands, or |H|≥ηd and the pair supports at least ηd|P| directed 4-cycles.
- **T26 — Rectangle Orientation Theorem** — `SUPPORTED`: No arc points P→H; every adjacency between H and P is oriented H→P.
- **T27 — Four-Chamber Extremal Skeleton Theorem** — `STRUCTURAL_SYNTHESIS`: Surviving profiles resemble a cyclic four-chamber skeleton x→P→y→H→x with a one-way H→P reservoir.
- **T28 — One-Way Rectangle Saturation Lemma** — `SUPPORTED`: e(H,P)≥|H|(d-n+|P|+|H|) whenever the right side is positive.
- **CD — Candidate D — Rectangle Diversity Lemma** — `PROPOSAL`: A large one-way H→P rectangle cannot have nearly identical tail inneighborhoods.
- **CE — Candidate E — Common-Inneighborhood Compression Lemma** — `PROPOSAL`: If H-vertex inneighborhoods overlap too strongly, a large common core should violate hereditary subcriticality.

## Round 4

The bridge system was compressed into explicit inequalities. The half-bridge premise was recognized only as a sufficient contradiction device, not a plausible property of counterexamples.

- **T29 — Escape Multiplicity Identity** — `SUPPORTED`: Σ_{ordered nonedges}q(x,y)=Σ_x e(N+(x),M_x)≥nd(d+1)/2.
- **T30 — Ordered Nonadjacency Identity** — `SUPPORTED`: At n=3d the number of ordered nonadjacent pairs is n(d-1).
- **T31 — Super-Half Bridge Theorem** — `SUPPORTED`: Some ordered nonedge has q(x,y)≥ceil(d(d+1)/(2(d-1)))=ceil(d/2+1+1/(d-1)).
- **T32 — Bidirectional Bridge Exclusion Theorem** — `SUPPORTED`: For P=N+(x)∩N-(y), H=N+(y)∩N-(x), all P–H adjacencies point H→P.
- **T33 — Bridge Deficit Theorem** — `SUPPORTED_CONDITIONAL`: For bridge size s, d^-(x)≤n-d-s+ceil(s/3)-2.
- **T34 — Reverse-Bridge Capacity Theorem** — `SUPPORTED`: d^-(x)≤n-d-(s+1)/2; at n=3d, d^-(x)≤2d-(s+1)/2.
- **T35 — Total Bridge Energy Identity** — `SUPPORTED`: For fixed x, Q_x=Σ_{y∈M_x}q(x,y)=d²-e(N+(x))≥d(d+1)/2.
- **T36 — Indegree–Bridge Amplification Theorem** — `SUPPORTED`: Some nonneighbor y has q(x,y)≥ceil(d(d+1)/(2(2d-1-d^-(x)))) at n=3d.
- **T37 — Exact Closure Criterion** — `SUPPORTED_SUFFICIENT_CONDITIONS`: Any of several explicit bridge-amplification or deficit inequalities would close the kernel.
- **T38 — Half-Bridge Closure Theorem** — `SUPPORTED_IMPLICATION_ONLY`: If every nonedge had q(x,y)≤(d-1)/2, global escape mass would contradict the exact nonedge count.
- **T39 — Half-Bridge Failure Structure Theorem** — `SUPPORTED`: Failure of the half-bridge premise yields a large one-way rectangular certificate P,H around a nonedge.

## Round 5

The half-bridge route was hostile-audited. Common forward targets were shown to create transitive fans rather than triangles. The exact obstruction became simultaneous large common in/out neighborhoods with a one-way forbidden rectangle.

- **T40 — High-Indegree Root Theorem** — `SUPPORTED`: Some vertex has indegree at least d.
- **T41 — Root Escape-Energy Theorem** — `SUPPORTED`: For high-indegree root x, Σ_{y∈M}q_y=d²-e(A)≥d(d+1)/2.
- **T42 — Bridge Export Theorem** — `SUPPORTED`: For bridge P of size s, e(P,U)≥s(d-1)-binom(s,2), yielding 2r+s≤4d-3 at n=3d.
- **T43 — Reverse-Wall Theorem** — `SUPPORTED`: For R=N+(y), E(R,P)=∅.
- **T44 — Two-Block Degree Identity** — `SUPPORTED`: Exact outgoing-degree decomposition for P∪R with E(R,P)=∅.
- **T45 — Bridge Collision Identity** — `SUPPORTED`: Σ_{z∈M}binom(q(x,z),2)=Σ_{pairs {a,b}⊂A}|N+(a)∩N+(b)∩M|.
- **T46 — Double-Wall Escape Theorem** — `SUPPORTED_CONDITIONAL`: A large common forward target set C forces |N-(a)∪N-(b)|≤2d-|C|+ceil(|C|/3)-1.
- **T47 — Transitive-Fan Obstruction Theorem** — `STRUCTURAL_DIAGNOSIS`: Large common in- and out-neighborhoods can coexist as a transitive layered configuration without forming a directed triangle.
- **T48 — Fan-Reversal Closure Criterion** — `SUPPORTED`: For I=N-(a)∩N-(b), C=N+(a)∩N+(b), E(C,I)=∅; any forced C→I arc closes a triangle.
- **T49 — One-Way Fan Capacity Inequality** — `SUPPORTED`: |I|≤2d-(|C|+1)/2 at n=3d.

## Round 6

The campaign moved to A² energy. Row concentration, fan energy, and second-order common-target concentration were derived. The claimed recursive fan cascade was later audited as overclaimed.

- **T50 — Cubic-Zero Theorem** — `SUPPORTED`: tr(A³)=0.
- **T51 — Reverse-Arc Annihilation Theorem** — `SUPPORTED`: A²∘Aᵀ=0.
- **T52 — Two-Path Mass Theorem** — `SUPPORTED`: Σ_{x,y}(A²)_{xy}=nd².
- **T53 — Exact Support Partition Theorem** — `SUPPORTED`: Two-path mass partitions into transitive-arc endpoints and nonadjacent endpoints; reverse-arc entries vanish.
- **T54 — Escape-Mass Floor** — `SUPPORTED`: Σ_{ordered nonedges}(A²)_{xy}≥nd(d+1)/2.
- **T55 — Two-Path Collision Theorem** — `SUPPORTED`: ||A²||_F²=Σ_{u,v}|N-(u)∩N-(v)|·|N+(u)∩N+(v)|.
- **T56 — Global Fan-Energy Identity** — `SUPPORTED`: The common-in/common-out rectangle energy equals ||A²||_F².
- **T57 — Row Concentration Theorem** — `SUPPORTED`: Σ_yQ_{xy}²≥d⁴/(n-1-d^-(x)).
- **T58 — Fan-Energy Floor** — `SUPPORTED`: At n=3d, ||A²||_F²≥nd⁴/(2d-1)=3d⁵/(2d-1).
- **T59 — Multiplicity-Collapse Obstruction** — `STRUCTURAL_DIAGNOSIS`: A lower bound on ||A²||_F² can concentrate on few ordered pairs and does not force many distinct forbidden pairs.
- **T60 — Maximal-Bridge Matrix Theorem** — `SUPPORTED`: If μ=max Q_{xy}, then μ≥d²/(2d-1)>d/2 at n=3d.
- **T61 — Large Transitive-or-Escape Fan Theorem** — `SUPPORTED`: Some ordered pair has more than d/2 internally distinct two-paths; endpoints are either adjacent forward or nonadjacent.
- **T62 — Fan-Coherence Closure Theorem** — `PROPOSAL_UNVERIFIED`: A sufficiently large exact twin class inside a fan should admit quotient compression to a smaller counterexample.
- **T63 — Fan-Union Inequality** — `SUPPORTED`: |∪S_p|≥(Σ|S_p|)²/Σ|S_p∩S_q| and Σ|S_p|≥sd-binom(s,2).
- **T64 — Second-Order Concentration Theorem** — `SUPPORTED`: Some p,q in a fan have a common external outneighbor set at least the average lower bound from T63.
- **T65 — Fan Cascade Theorem** — `RETRACTED_OVERCLAIM`: The second-order concentration was described as recursively iterable; that iteration was not proved.

## Round 7

A global fan-capacity inequality and exact slack identity were produced. The crucial error entered here: a one-sided peeling order was incorrectly converted into total induced-edge sparsity.

- **T66 — Fan Rectangle Prohibition Theorem** — `SUPPORTED`: For I=N-(u)∩N-(v), C=N+(u)∩N+(v), E(C,I)=∅.
- **T67 — Universal Fan Capacity Theorem** — `SUPPORTED`: I(u,v)+(C(u,v)+1)/2≤2d at n=3d.
- **T68 — Universal Indegree Ceiling** — `SUPPORTED`: d^-(u)≤(3d-3)/2.
- **T69 — Common-Out Sum Identity** — `SUPPORTED`: Σ_{u,v}C(u,v)=Σ_w d^-(w)².
- **T70 — Fan Energy Identity** — `SUPPORTED`: ||A²||_F²=Σ_{u,v}I(u,v)C(u,v).
- **T71 — Common-Out Energy Floor** — `SUPPORTED`: ΣC(u,v)²≥(ΣC(u,v))²/n².
- **T72 — Two-Path Energy Floor** — `SUPPORTED`: ||A²||_F²≥nd⁴/(2d-1) at n=3d.
- **T73 — Fan-Capacity Saturation Theorem** — `SUPPORTED`: C·Λ equals missing internal adjacencies in C plus missing permitted outgoing arcs from C.
- **T74 — Global Slack Identity** — `SUPPORTED`: 2dS-||A²||_F²-(T+S)/2=Σ C(u,v)Λ(u,v).
- **T75 — Elimination-Ordering Theorem** — `SUPPORTED_CONDITIONAL`: Every proper S has an ordering with each removed vertex having residual outdegree below one third of the remaining order.
- **T76 — Exact Hereditary Edge Bound** — `RETRACTED`: Claimed e(D[S])≤Σ(ceil(t/3)-1); false because backward arcs are not counted.
- **T77 — Hereditarily Sharpened Fan Capacity Theorem** — `RETRACTED`: Used the false T76 to replace the coefficient 1/2 by 5/6.
- **T78 — Coefficient Required for Closure** — `CONDITIONAL_META`: Within a simplified pointwise fan-capacity/energy architecture, an unrealistically large coefficient would be needed for closure.
- **T79 — One-Pair Strategy Impossibility Theorem** — `STRUCTURAL_DIAGNOSIS`: Pairwise fan statistics plus first/second moments are quantitatively insufficient in the analyzed architecture.
- **T80 — Triple-Fan Prohibition Theorem** — `SUPPORTED`: For triple common-in I₃ and common-out C₃, E(C₃,I₃)=∅.

## Round 8

The false hereditary edge bound generated apparent 5/6 escape density and a 7/6 indegree barrier. These were later fully retracted.

- **T81 — Five-Sixths Escape Theorem** — `RETRACTED`: Claimed e(A,M)≥d²-F(d)≈5d²/6.
- **T82 — Five-Sixths Bridge Theorem** — `RETRACTED`: Claimed a bridge of size ≈5d/6 from a high-indegree root.
- **T83 — Hereditary Bridge Export Theorem** — `RETRACTED`: Used false edge bound inside a bridge.
- **T84 — Seven-Sixths Indegree Barrier** — `RETRACTED`: Claimed high roots or all vertices satisfy d^-(x)≤7d/6+O(1).
- **T85 — Low-Indegree Mass Bound** — `RETRACTED`: Derived distributional bounds from T84.
- **T86 — Near-Regular Core Theorem** — `RETRACTED`: Derived a large near-inregular core from T84.
- **T87 — Boundary Bridge Rigidity Theorem** — `RETRACTED`: Near 7d/6 was claimed to force almost-full bridges.
- **T88 — Full-Bridge Boundary Theorem** — `RETRACTED`: Used F(d) from the false hereditary edge bound.
- **T89 — Multi-Sink Rigidity Theorem** — `RETRACTED`: Near-boundary roots claimed to force many almost-full sinks.
- **T90 — Blow-Up Backflow Prohibition Theorem** — `PARTIAL_LOCAL_FACT`: The local fact a→y implies N+(y)∩N-(a)=∅ is valid; the global near-complete blow-up conclusion was not.
- **T91 — Inneighborhood-Union Closure Criterion** — `PROPOSAL`: A sufficiently large union of forbidden inneighborhoods would deprive a sink of d legal outtargets.
- **T92 — Three-Layer Product-Zero Theorem** — `SUPPORTED`: For B=N-(x), A=N+(x), M=M_x, tr(XYZ)=0 for cyclic matrices B→A, A→M, M→B.
- **T93 — Tripartite Closure Criterion** — `PROPOSAL_UNVERIFIED`: A sufficiently strong tripartite supersaturation inequality would make tr(XYZ)>0.

## Round 9

Those false densities generated a near-Mantel three-layer close. Terminal audit later showed the entire numerical close rested on the invalid edge estimate.

- **T94 — Corrected High-Root Barrier** — `RETRACTED`: The numerical barrier still depended on the false F(s) edge bound.
- **T95 — A-to-B Zero Theorem** — `SUPPORTED`: E(A,B)=∅.
- **T96 — First Cyclic-Layer Lower Bound** — `RETRACTED`: Used d²-F(d).
- **T97 — M-to-B Lower Bound** — `RETRACTED`: Used F(m).
- **T98 — B-to-A Lower Bound** — `RETRACTED`: Used F(r), F(m).
- **T99 — Three-Layer Density Ledger** — `RETRACTED`: All three cyclic layer bounds depended on T76.
- **T100 — Mantel Gap Theorem** — `RETRACTED_ROUTE`: The apparent near-Mantel contradiction was an artifact of the retracted density ledger.
- **T101 — Split-Chamber Obstruction Theorem** — `STRUCTURAL_DIAGNOSIS`: Whole-chamber bipartite cuts are constructions, not automatic upper bounds for triangle-free subgraphs of a tripartite host.
- **T102 — Forbidden-Rectangle Union Theorem** — `SUPPORTED`: e(M,B)+|∪_{a∈A}(N_M^+(a)×N_B^-(a))|≤mr.
- **T103 — Anticorrelation-or-Overlap Closure Theorem** — `PROPOSAL`: Closure follows if rectangle areas correlate positively and their overlap is controlled.

## Round 10

The hidden fault was found and the false branch was killed. The valid kernel was reset to regularity, wall exclusion, two-path identities, hereditary minimum-outdegree deficit, and matrix support.

- **T104 — One-Sided Peeling Does Not Count All Arcs** — `SUPPORTED`: Residual outdegree sums count only forward arcs in the peeling order.
- **T105 — Exact Refutation of the Hereditary Edge Bound** — `SUPPORTED`: A transitive tournament can have zero residual outdegree under a removal order while containing binom(s,2) arcs.
- **T106 — Outneighborhood Wall Theorem** — `SUPPORTED`: E(A,B)=∅.
- **T107 — Exact Local Defect Identity** — `SUPPORTED`: e(A,M)=d(d+1)/2+σ(x).
- **T108 — Reverse-Arc Annihilation Theorem** — `SUPPORTED`: A²∘Aᵀ=0.
- **T109 — Two-Path Conservation Theorem** — `SUPPORTED`: A²1=d²1 and ΣQ=nd².
- **T110 — Valid Indegree Ceiling** — `SUPPORTED`: d^-(x)≤(3d-3)/2.
- **T111 — Correct Terminal Obstruction Theorem** — `SUPPORTED_SUMMARY`: The audited elementary kernel forces escape mass but permits backward density, overlap, concentration, and long-range folding.
- **T112 — Machine Closure Contract** — `PROTOCOL`: A genuine close requires an exact rational certificate, a verified new structural lemma, or an exact bounded surviving model.

## Round 11

The first honest rooted four-flag system was completed. It exposed the backward reservoir: B can store degree internally or send it in the wrong B→M direction.

- **T113 — Rooted Chamber Equations** — `SUPPORTED`: Rooted sizes and E(A,B)=∅; d²=e(A)+e(A,M).
- **T114 — Rooted Cyclic Product-Zero Theorem** — `SUPPORTED`: Σ_{b,a,m}X_{ba}Y_{am}Z_{mb}=0.
- **T115 — Tripartite Union-Bound Theorem** — `SUPPORTED`: m e(B,A)+r e(A,M)+d e(M,B)≤2drm.
- **T116 — Valid M-to-B Floor** — `SUPPORTED`: e(M,B)≥max(0,d(d+1)/2-binom(m,2)).
- **T117 — Exact B-to-A Ledger** — `SUPPORTED`: e(B,A)=rd-r-e(B)-e(B,M), with a derived lower bound using M–B capacity.
- **T118 — Missing Cyclic Edge Theorem** — `SUPPORTED_DIAGNOSIS`: Current valid bounds force A→M strongly and sometimes M→B, but not B→A quadratically.
- **T119 — Backward Reservoir Theorem** — `SUPPORTED`: If e(B,A) is small, exact degree accounting forces e(B)+e(B,M) large.
- **T120 — Backward-Hierarchy Theorem** — `SUPPORTED_CONDITIONAL`: Hereditary deficit gives a peeling order on B; dense internal arcs may point backward across it.
- **T121 — Two-Reservoir Classification Theorem** — `STRUCTURAL_SYNTHESIS`: A surviving rooted profile stores B-degree internally or in the reverse B→M direction.
- **T122 — Pair-Marginal Phantom Theorem** — `PROPOSAL_MODEL`: Pairwise chamber marginals admit a zero-cyclic-product profile; no actual global graph was constructed.
- **T123 — Five-Flag Necessity Theorem** — `METHODOLOGICAL`: Rooted four-flags do not retain the correlation between internal B hierarchy, B→A degree, and A→M neighborhoods.

## Round 12

Expansion versus concentration was attacked directly. A numerical 0.686d fan claim was produced but later found to use an inequality in the wrong direction.

- **R12-T124 — Second-Neighborhood Deficit Theorem** — `SUPPORTED`: |N^{++}(v)\N+(v)|≥(d+1)/2.
- **R12-T125 — Folding Creates Codegree** — `SUPPORTED`: If two-step mass folds into a small support, row energy forces high multiplicity.
- **R12-T126 — Concentration Self-Bound** — `PARTIAL_RETRACTED`: The exact row-energy and indegree inequalities were valid; the derived numerical q≥0.68614d was invalid.
- **R12-T127 — Forced Double-Codegree Alternative** — `PROPOSAL_QUALITATIVE`: Insufficient expansion should create a large common-out set and forbidden rectangle.

## Round 13

The 0.686d claim was retracted. A valid weighted fan-selection theorem and a dual common-out fan were proved. The rectangle still remained feasible.

- **R13-T124 — Retraction of the 0.686d Fan Bound** — `SUPPORTED`: The denominator inequality was substituted in the wrong direction; q≥0.68614d is withdrawn.
- **R13-T125 — Maximum-Fan Kernel** — `SUPPORTED`: For a high-indegree root, some two-path fan has q≥d²/(2d-1)>d/2.
- **R13-T126 — Zero-Support Maximum-Fan Inequality** — `SUPPORTED`: d²≤q(3d-1-d^-(p)) for a fan vertex p.
- **R13-T127 — Fan-to-Inneighborhood Rectangle** — `SUPPORTED`: For P⊆N-(y), ∪_{p∈P}N-(p) is disjoint from N+(y), hence has size at most 2d.
- **R13-T128 — Weighted Maximum-Fan Selection** — `SUPPORTED`: Some nonempty P_{xy} has average indegree at least d.
- **R13-T129 — Dual Fan Theorem** — `SUPPORTED`: There are x,z,y and C⊆N+(x)∩N+(z)∩N-(y) with |C|≥|P|/2 for a weighted fan P.

## Round 14

The same kernel was attacked spectrally. Strong connectivity and aperiodicity were established under minimality; spectrum-only closure and equality cases were killed; exact integer row-energy remained.

- **T130 — First Three Vanishing Trace Theorem** — `SUPPORTED`: tr(A)=tr(A²)=tr(A³)=0.
- **T131 — Perron Moment Cancellation Theorem** — `SUPPORTED`: The non-Perron eigenvalues cancel d in the first three power sums.
- **T132 — Singular-Energy Budget Theorem** — `SUPPORTED`: ||A||_F²=3d² and residual singular-value squared mass is at most 2d².
- **T133 — Spectral Modulus Budget** — `SUPPORTED`: Σ_{i≥2}|λ_i/d|²≤2.
- **T134 — Cubic Defect Identity** — `SUPPORTED`: Σ μ_i(1-μ_i)=Σ μ_i²(1-μ_i)=Σ μ_i(1-μ_i)²=0.
- **T135 — Real-Part Defect Formula** — `SUPPORTED`: Re[z(1-z)²]=r cosθ-2r² cos2θ+r³ cos3θ.
- **T136 — Peripheral Period Theorem** — `SUPPORTED_STANDARD`: For irreducible d-regular A, peripheral eigenvalues are d times roots of unity determined by the period.
- **T137 — Aperiodicity Theorem** — `SUPPORTED_CONDITIONAL`: A minimal kernel is primitive after eliminating periods 2 and 3.
- **T138 — Strong Connectivity Theorem** — `SUPPORTED_CONDITIONAL`: A smallest counterexample is strongly connected.
- **T139 — Strict Spectral Radius Gap** — `SUPPORTED_CONDITIONAL`: All non-Perron eigenvalues satisfy |λ|<d.
- **T140 — Abstract Spectral Phantom** — `STRUCTURAL_DIAGNOSIS`: The abstract finite moment system may be feasible; moments alone do not encode entrywise support.
- **T141 — Energy Equality Rigidity Theorem** — `SUPPORTED`: Equality in the continuous row-energy floor forces d=1; for d>1 the inequality is strict.
- **T142 — Exact Integral Row-Energy Floor** — `SUPPORTED`: If d²=kq+t, the integer row energy is at least (k-t)q²+t(q+1)².

## Round 15

Fourth-moment RSI succeeded: escape mass plus the exact nonedge count forced cubic opposite-path product and hence at least ceil(3d³/2) directed 4-cycles. The remaining escape mechanism was isolated as skew two-path energy.

- **T143 — Opposite Two-Path Product Theorem** — `SUPPORTED`: For Q=A², tr(A⁴)=Σ_{x,y}Q_{xy}Q_{yx}=4C4(D).
- **T144 — Opposite Vertices Are Nonadjacent** — `SUPPORTED`: Opposite vertices of a directed 4-cycle are nonadjacent.
- **T145 — Exact Nonedge Count** — `SUPPORTED`: The number of unordered nonedges is 3d(d-1)/2.
- **T146 — Escape-Mass Floor** — `SUPPORTED`: The ordered nonedge two-path mass is at least 3d²(d+1)/2.
- **T147 — Forced Opposite-Path Product Theorem** — `SUPPORTED`: Σ_{unordered nonedges}Q_{xy}Q_{yx}≥3d³.
- **T148 — Cubic Directed-C4 Theorem** — `SUPPORTED_TERMINAL_ASSET`: C4(D)≥ceil(3d³/2), equivalently tr(A⁴)≥6d³.
- **T149 — Every Kernel Contains a Directed C4** — `SUPPORTED`: A triangle-free exact-boundary regular kernel necessarily contains a directed 4-cycle.
- **T150 — Heavy Four-Cycle Vertex Theorem** — `SUPPORTED`: Some vertex lies on at least 2d² directed 4-cycles.
- **T151 — Heavy Bidirectional Bridge Theorem** — `SUPPORTED`: Some nonedge {x,y} has Q_{xy}Q_{yx}≥ceil(2d²/(2d-1)).
- **T152 — Asymmetric Four-Cycle Reservoir Theorem** — `STRUCTURAL_DIAGNOSIS`: The C4 lower bound is compatible with Q_{xy}≈d and Q_{yx}=O(1) on significant pairs.
- **T153 — Exact Fourth-Moment Decomposition** — `SUPPORTED`: tr(A⁴)=||A²||_F²-(1/2)||A²-(Aᵀ)²||_F²; C4 is one quarter of this.


---

# 4. Complete Theorem Ledger

The statuses in this table are the authoritative extraction. A theorem name in the session does not imply that the statement was valid, novel, or load-bearing.

| ID | Round | Name | Status | Authoritative extraction |
|---|---:|---|---|---|
| R1-L1 | 1 | Neighborhood Acyclicity Pressure | SUPPORTED | For every v, D[N+(v)] and D[N-(v)] are directed-triangle-free; for every arc v→x, N+(x)∩N-(v)=∅. |
| R1-L2 | 1 | Half-Degree Escape Lemma | SUPPORTED | For a minimum-outdegree vertex v with d=δ+(D), some x∈N+(v) has at least (d+1)/2 outneighbors in M_v. |
| R1-L3 | 1 | Minimal-Counterexample Hereditary Deficit | SUPPORTED_CONDITIONAL | In a vertex-minimal counterexample, every proper nonempty S has a vertex x with d_S^+(x)<\|S\|/3. |
| R1-ME | 1 | Minimal Escape Lemma | SUPPORTED_CONDITIONAL | For every proper nonempty S, some x∈S has d^+_{V\S}(x)>d-\|S\|/3. |
| T1 | 2 | Arc-Minimal Regularization Theorem | SUPPORTED_CONDITIONAL | After choosing a counterexample with minimum order and then minimum arcs, every vertex has outdegree d=ceil(n/3). |
| T2 | 2 | Forbidden Residue Theorem | SUPPORTED_CONDITIONAL | A vertex-minimal counterexample cannot have n≡1 mod 3. |
| T3 | 2 | Universal Minimum-Tail Theorem | SUPPORTED_CONDITIONAL | Every vertex has an incoming tail of minimum outdegree; in the arc-minimal kernel this is automatic because all vertices have outdegree d. |
| T4 | 2 | Hereditary Deficit Theorem | SUPPORTED_CONDITIONAL | Every proper nonempty induced subgraph has minimum outdegree below one third of its order. |
| T5 | 2 | Exact Escape Theorem | SUPPORTED_CONDITIONAL | For every proper nonempty S, some x∈S has d^+_{V\S}(x)≥d-ceil(\|S\|/3)+1. |
| T6 | 2 | A-to-B Exclusion Theorem | SUPPORTED | For A=N+(v), B=N-(v), E(A,B)=∅. |
| T7 | 2 | Quadratic Escape-Mass Theorem | SUPPORTED | For \|A\|=d, e(A,M_v)≥d(d+1)/2 and hence \|M_v\|≥(d+1)/2. |
| T8 | 2 | Two-Thirds Escape Vertex Theorem | SUPPORTED_CONDITIONAL | Some x∈A has \|N_M^+(x)\|≥d-ceil(d/3)+1>2d/3. |
| T9 | 2 | Second-Generation Forbidden-Indegree Theorem | SUPPORTED | If X=N_M^+(x), then for z∈X, N+(z)∩N-(x)=∅. |
| T10 | 2 | Second-Escape Compression Theorem | SUPPORTED_CONDITIONAL | Applying hereditary deficit to X yields z∈X with a large external outneighbor set W=N+(z)\X, disjoint from N-(x). |
| T11 | 2 | Pair-Cell Indegree Ceiling | SUPPORTED_CONDITIONAL | For the selected x and X, d^-(x)≤n-d-\|X\|+ceil(\|X\|/3)-2. |
| T12 | 2 | Layer-Folding Obstruction Theorem | STRUCTURAL_DIAGNOSIS | Naive recursive escape fails because later forward layers may overlap older forward layers; only immediate backward walls are forbidden. |
| CA | 2 | Candidate A — Fold-or-Triangle Lemma | PROPOSAL | A large overlap of a new escape layer with earlier layers should either force a triangle or pay an explicit expansion penalty. |
| CB | 2 | Candidate B — Selected-Vertex Indegree Floor | PROPOSAL | Select a low-internal-outdegree x with an unusually large indegree sufficient to contradict T11. |
| CC | 2 | Candidate C — Weighted Pair-Cell Inequality | PROPOSAL | Sum pair-cell inequalities over many low-internal-degree vertices instead of selecting one vertex. |
| T13 | 3 | Universal Three-Chamber Theorem | SUPPORTED | For each x, V\{x} partitions into P_x=N+(x), I_x=N-(x), M_x, and E(P_x,I_x)=∅. |
| T14 | 3 | Exact Escape-Slack Identity | SUPPORTED | If σ(x)=binom(d,2)-e(P_x), then e(P_x,M_x)=d(d+1)/2+σ(x). |
| T15 | 3 | Nonneighbor Capacity Theorem | SUPPORTED | \|M_x\|≥(d+1)/2+σ(x)/d, hence an indegree upper bound follows. |
| T16 | 3 | Global Nonneighbor Conservation Theorem | SUPPORTED | Σ_x \|M_x\|=n(n-1-2d); at n=3d the average is d-1. |
| T17 | 3 | Global Defect Budget Theorem | SUPPORTED | Σ_xσ(x) is bounded by the global nonneighbor budget; at n=3d, Σσ(x)≤nd(d-3)/2. |
| T18 | 3 | Directed Two-Path Classification Theorem | SUPPORTED | Every directed two-path x→p→y is either transitively closed by x→y or has nonadjacent endpoints; y→x is forbidden. |
| T19 | 3 | Global Escape-Path Theorem | SUPPORTED | The total escape two-path count is nd(d+1)/2+Σσ(x). |
| T20 | 3 | Common-Inneighborhood Identity | SUPPORTED | Σ_{p→y}\|N-(p)∩N-(y)\|=nd(d-1)/2-Σσ(x). |
| T21 | 3 | Folding Conservation Theorem | SUPPORTED | Transitive two-path mass plus escape two-path mass equals nd²; lost transitive closure becomes escape mass one-for-one. |
| T22 | 3 | High-Multiplicity Escape Pair Theorem | SUPPORTED | At n=3d some ordered nonadjacent pair has q(x,y)≥ceil(d(d+1)/(2(d-1)))>d/2+1. |
| T23 | 3 | Parallel-Bridge Chamber Theorem | SUPPORTED | For P=N+(x)∩N-(y), E(P,N-(x))=∅ and E(N+(y),P)=∅. |
| T24 | 3 | Rectangle-to-C4 Theorem | SUPPORTED | For H=N+(y)∩N-(x), every (p,h)∈P×H yields x→p→y→h→x; the pair lies in \|P\|\|H\| directed 4-cycles. |
| T25 | 3 | Fold-or-Expansion Theorem | SUPPORTED_DICHOTOMY | For any η, either \|H\|<ηd and L∪R expands, or \|H\|≥ηd and the pair supports at least ηd\|P\| directed 4-cycles. |
| T26 | 3 | Rectangle Orientation Theorem | SUPPORTED | No arc points P→H; every adjacency between H and P is oriented H→P. |
| T27 | 3 | Four-Chamber Extremal Skeleton Theorem | STRUCTURAL_SYNTHESIS | Surviving profiles resemble a cyclic four-chamber skeleton x→P→y→H→x with a one-way H→P reservoir. |
| T28 | 3 | One-Way Rectangle Saturation Lemma | SUPPORTED | e(H,P)≥\|H\|(d-n+\|P\|+\|H\|) whenever the right side is positive. |
| CD | 3 | Candidate D — Rectangle Diversity Lemma | PROPOSAL | A large one-way H→P rectangle cannot have nearly identical tail inneighborhoods. |
| CE | 3 | Candidate E — Common-Inneighborhood Compression Lemma | PROPOSAL | If H-vertex inneighborhoods overlap too strongly, a large common core should violate hereditary subcriticality. |
| T29 | 4 | Escape Multiplicity Identity | SUPPORTED | Σ_{ordered nonedges}q(x,y)=Σ_x e(N+(x),M_x)≥nd(d+1)/2. |
| T30 | 4 | Ordered Nonadjacency Identity | SUPPORTED | At n=3d the number of ordered nonadjacent pairs is n(d-1). |
| T31 | 4 | Super-Half Bridge Theorem | SUPPORTED | Some ordered nonedge has q(x,y)≥ceil(d(d+1)/(2(d-1)))=ceil(d/2+1+1/(d-1)). |
| T32 | 4 | Bidirectional Bridge Exclusion Theorem | SUPPORTED | For P=N+(x)∩N-(y), H=N+(y)∩N-(x), all P–H adjacencies point H→P. |
| T33 | 4 | Bridge Deficit Theorem | SUPPORTED_CONDITIONAL | For bridge size s, d^-(x)≤n-d-s+ceil(s/3)-2. |
| T34 | 4 | Reverse-Bridge Capacity Theorem | SUPPORTED | d^-(x)≤n-d-(s+1)/2; at n=3d, d^-(x)≤2d-(s+1)/2. |
| T35 | 4 | Total Bridge Energy Identity | SUPPORTED | For fixed x, Q_x=Σ_{y∈M_x}q(x,y)=d²-e(N+(x))≥d(d+1)/2. |
| T36 | 4 | Indegree–Bridge Amplification Theorem | SUPPORTED | Some nonneighbor y has q(x,y)≥ceil(d(d+1)/(2(2d-1-d^-(x)))) at n=3d. |
| T37 | 4 | Exact Closure Criterion | SUPPORTED_SUFFICIENT_CONDITIONS | Any of several explicit bridge-amplification or deficit inequalities would close the kernel. |
| T38 | 4 | Half-Bridge Closure Theorem | SUPPORTED_IMPLICATION_ONLY | If every nonedge had q(x,y)≤(d-1)/2, global escape mass would contradict the exact nonedge count. |
| T39 | 4 | Half-Bridge Failure Structure Theorem | SUPPORTED | Failure of the half-bridge premise yields a large one-way rectangular certificate P,H around a nonedge. |
| T40 | 5 | High-Indegree Root Theorem | SUPPORTED | Some vertex has indegree at least d. |
| T41 | 5 | Root Escape-Energy Theorem | SUPPORTED | For high-indegree root x, Σ_{y∈M}q_y=d²-e(A)≥d(d+1)/2. |
| T42 | 5 | Bridge Export Theorem | SUPPORTED | For bridge P of size s, e(P,U)≥s(d-1)-binom(s,2), yielding 2r+s≤4d-3 at n=3d. |
| T43 | 5 | Reverse-Wall Theorem | SUPPORTED | For R=N+(y), E(R,P)=∅. |
| T44 | 5 | Two-Block Degree Identity | SUPPORTED | Exact outgoing-degree decomposition for P∪R with E(R,P)=∅. |
| T45 | 5 | Bridge Collision Identity | SUPPORTED | Σ_{z∈M}binom(q(x,z),2)=Σ_{pairs {a,b}⊂A}\|N+(a)∩N+(b)∩M\|. |
| T46 | 5 | Double-Wall Escape Theorem | SUPPORTED_CONDITIONAL | A large common forward target set C forces \|N-(a)∪N-(b)\|≤2d-\|C\|+ceil(\|C\|/3)-1. |
| T47 | 5 | Transitive-Fan Obstruction Theorem | STRUCTURAL_DIAGNOSIS | Large common in- and out-neighborhoods can coexist as a transitive layered configuration without forming a directed triangle. |
| T48 | 5 | Fan-Reversal Closure Criterion | SUPPORTED | For I=N-(a)∩N-(b), C=N+(a)∩N+(b), E(C,I)=∅; any forced C→I arc closes a triangle. |
| T49 | 5 | One-Way Fan Capacity Inequality | SUPPORTED | \|I\|≤2d-(\|C\|+1)/2 at n=3d. |
| T50 | 6 | Cubic-Zero Theorem | SUPPORTED | tr(A³)=0. |
| T51 | 6 | Reverse-Arc Annihilation Theorem | SUPPORTED | A²∘Aᵀ=0. |
| T52 | 6 | Two-Path Mass Theorem | SUPPORTED | Σ_{x,y}(A²)_{xy}=nd². |
| T53 | 6 | Exact Support Partition Theorem | SUPPORTED | Two-path mass partitions into transitive-arc endpoints and nonadjacent endpoints; reverse-arc entries vanish. |
| T54 | 6 | Escape-Mass Floor | SUPPORTED | Σ_{ordered nonedges}(A²)_{xy}≥nd(d+1)/2. |
| T55 | 6 | Two-Path Collision Theorem | SUPPORTED | \|\|A²\|\|_F²=Σ_{u,v}\|N-(u)∩N-(v)\|·\|N+(u)∩N+(v)\|. |
| T56 | 6 | Global Fan-Energy Identity | SUPPORTED | The common-in/common-out rectangle energy equals \|\|A²\|\|_F². |
| T57 | 6 | Row Concentration Theorem | SUPPORTED | Σ_yQ_{xy}²≥d⁴/(n-1-d^-(x)). |
| T58 | 6 | Fan-Energy Floor | SUPPORTED | At n=3d, \|\|A²\|\|_F²≥nd⁴/(2d-1)=3d⁵/(2d-1). |
| T59 | 6 | Multiplicity-Collapse Obstruction | STRUCTURAL_DIAGNOSIS | A lower bound on \|\|A²\|\|_F² can concentrate on few ordered pairs and does not force many distinct forbidden pairs. |
| T60 | 6 | Maximal-Bridge Matrix Theorem | SUPPORTED | If μ=max Q_{xy}, then μ≥d²/(2d-1)>d/2 at n=3d. |
| T61 | 6 | Large Transitive-or-Escape Fan Theorem | SUPPORTED | Some ordered pair has more than d/2 internally distinct two-paths; endpoints are either adjacent forward or nonadjacent. |
| T62 | 6 | Fan-Coherence Closure Theorem | PROPOSAL_UNVERIFIED | A sufficiently large exact twin class inside a fan should admit quotient compression to a smaller counterexample. |
| T63 | 6 | Fan-Union Inequality | SUPPORTED | \|∪S_p\|≥(Σ\|S_p\|)²/Σ\|S_p∩S_q\| and Σ\|S_p\|≥sd-binom(s,2). |
| T64 | 6 | Second-Order Concentration Theorem | SUPPORTED | Some p,q in a fan have a common external outneighbor set at least the average lower bound from T63. |
| T65 | 6 | Fan Cascade Theorem | RETRACTED_OVERCLAIM | The second-order concentration was described as recursively iterable; that iteration was not proved. |
| T66 | 7 | Fan Rectangle Prohibition Theorem | SUPPORTED | For I=N-(u)∩N-(v), C=N+(u)∩N+(v), E(C,I)=∅. |
| T67 | 7 | Universal Fan Capacity Theorem | SUPPORTED | I(u,v)+(C(u,v)+1)/2≤2d at n=3d. |
| T68 | 7 | Universal Indegree Ceiling | SUPPORTED | d^-(u)≤(3d-3)/2. |
| T69 | 7 | Common-Out Sum Identity | SUPPORTED | Σ_{u,v}C(u,v)=Σ_w d^-(w)². |
| T70 | 7 | Fan Energy Identity | SUPPORTED | \|\|A²\|\|_F²=Σ_{u,v}I(u,v)C(u,v). |
| T71 | 7 | Common-Out Energy Floor | SUPPORTED | ΣC(u,v)²≥(ΣC(u,v))²/n². |
| T72 | 7 | Two-Path Energy Floor | SUPPORTED | \|\|A²\|\|_F²≥nd⁴/(2d-1) at n=3d. |
| T73 | 7 | Fan-Capacity Saturation Theorem | SUPPORTED | C·Λ equals missing internal adjacencies in C plus missing permitted outgoing arcs from C. |
| T74 | 7 | Global Slack Identity | SUPPORTED | 2dS-\|\|A²\|\|_F²-(T+S)/2=Σ C(u,v)Λ(u,v). |
| T75 | 7 | Elimination-Ordering Theorem | SUPPORTED_CONDITIONAL | Every proper S has an ordering with each removed vertex having residual outdegree below one third of the remaining order. |
| T76 | 7 | Exact Hereditary Edge Bound | RETRACTED | Claimed e(D[S])≤Σ(ceil(t/3)-1); false because backward arcs are not counted. |
| T77 | 7 | Hereditarily Sharpened Fan Capacity Theorem | RETRACTED | Used the false T76 to replace the coefficient 1/2 by 5/6. |
| T78 | 7 | Coefficient Required for Closure | CONDITIONAL_META | Within a simplified pointwise fan-capacity/energy architecture, an unrealistically large coefficient would be needed for closure. |
| T79 | 7 | One-Pair Strategy Impossibility Theorem | STRUCTURAL_DIAGNOSIS | Pairwise fan statistics plus first/second moments are quantitatively insufficient in the analyzed architecture. |
| T80 | 7 | Triple-Fan Prohibition Theorem | SUPPORTED | For triple common-in I₃ and common-out C₃, E(C₃,I₃)=∅. |
| T81 | 8 | Five-Sixths Escape Theorem | RETRACTED | Claimed e(A,M)≥d²-F(d)≈5d²/6. |
| T82 | 8 | Five-Sixths Bridge Theorem | RETRACTED | Claimed a bridge of size ≈5d/6 from a high-indegree root. |
| T83 | 8 | Hereditary Bridge Export Theorem | RETRACTED | Used false edge bound inside a bridge. |
| T84 | 8 | Seven-Sixths Indegree Barrier | RETRACTED | Claimed high roots or all vertices satisfy d^-(x)≤7d/6+O(1). |
| T85 | 8 | Low-Indegree Mass Bound | RETRACTED | Derived distributional bounds from T84. |
| T86 | 8 | Near-Regular Core Theorem | RETRACTED | Derived a large near-inregular core from T84. |
| T87 | 8 | Boundary Bridge Rigidity Theorem | RETRACTED | Near 7d/6 was claimed to force almost-full bridges. |
| T88 | 8 | Full-Bridge Boundary Theorem | RETRACTED | Used F(d) from the false hereditary edge bound. |
| T89 | 8 | Multi-Sink Rigidity Theorem | RETRACTED | Near-boundary roots claimed to force many almost-full sinks. |
| T90 | 8 | Blow-Up Backflow Prohibition Theorem | PARTIAL_LOCAL_FACT | The local fact a→y implies N+(y)∩N-(a)=∅ is valid; the global near-complete blow-up conclusion was not. |
| T91 | 8 | Inneighborhood-Union Closure Criterion | PROPOSAL | A sufficiently large union of forbidden inneighborhoods would deprive a sink of d legal outtargets. |
| T92 | 8 | Three-Layer Product-Zero Theorem | SUPPORTED | For B=N-(x), A=N+(x), M=M_x, tr(XYZ)=0 for cyclic matrices B→A, A→M, M→B. |
| T93 | 8 | Tripartite Closure Criterion | PROPOSAL_UNVERIFIED | A sufficiently strong tripartite supersaturation inequality would make tr(XYZ)>0. |
| T94 | 9 | Corrected High-Root Barrier | RETRACTED | The numerical barrier still depended on the false F(s) edge bound. |
| T95 | 9 | A-to-B Zero Theorem | SUPPORTED | E(A,B)=∅. |
| T96 | 9 | First Cyclic-Layer Lower Bound | RETRACTED | Used d²-F(d). |
| T97 | 9 | M-to-B Lower Bound | RETRACTED | Used F(m). |
| T98 | 9 | B-to-A Lower Bound | RETRACTED | Used F(r), F(m). |
| T99 | 9 | Three-Layer Density Ledger | RETRACTED | All three cyclic layer bounds depended on T76. |
| T100 | 9 | Mantel Gap Theorem | RETRACTED_ROUTE | The apparent near-Mantel contradiction was an artifact of the retracted density ledger. |
| T101 | 9 | Split-Chamber Obstruction Theorem | STRUCTURAL_DIAGNOSIS | Whole-chamber bipartite cuts are constructions, not automatic upper bounds for triangle-free subgraphs of a tripartite host. |
| T102 | 9 | Forbidden-Rectangle Union Theorem | SUPPORTED | e(M,B)+\|∪_{a∈A}(N_M^+(a)×N_B^-(a))\|≤mr. |
| T103 | 9 | Anticorrelation-or-Overlap Closure Theorem | PROPOSAL | Closure follows if rectangle areas correlate positively and their overlap is controlled. |
| T104 | 10 | One-Sided Peeling Does Not Count All Arcs | SUPPORTED | Residual outdegree sums count only forward arcs in the peeling order. |
| T105 | 10 | Exact Refutation of the Hereditary Edge Bound | SUPPORTED | A transitive tournament can have zero residual outdegree under a removal order while containing binom(s,2) arcs. |
| T106 | 10 | Outneighborhood Wall Theorem | SUPPORTED | E(A,B)=∅. |
| T107 | 10 | Exact Local Defect Identity | SUPPORTED | e(A,M)=d(d+1)/2+σ(x). |
| T108 | 10 | Reverse-Arc Annihilation Theorem | SUPPORTED | A²∘Aᵀ=0. |
| T109 | 10 | Two-Path Conservation Theorem | SUPPORTED | A²1=d²1 and ΣQ=nd². |
| T110 | 10 | Valid Indegree Ceiling | SUPPORTED | d^-(x)≤(3d-3)/2. |
| T111 | 10 | Correct Terminal Obstruction Theorem | SUPPORTED_SUMMARY | The audited elementary kernel forces escape mass but permits backward density, overlap, concentration, and long-range folding. |
| T112 | 10 | Machine Closure Contract | PROTOCOL | A genuine close requires an exact rational certificate, a verified new structural lemma, or an exact bounded surviving model. |
| T113 | 11 | Rooted Chamber Equations | SUPPORTED | Rooted sizes and E(A,B)=∅; d²=e(A)+e(A,M). |
| T114 | 11 | Rooted Cyclic Product-Zero Theorem | SUPPORTED | Σ_{b,a,m}X_{ba}Y_{am}Z_{mb}=0. |
| T115 | 11 | Tripartite Union-Bound Theorem | SUPPORTED | m e(B,A)+r e(A,M)+d e(M,B)≤2drm. |
| T116 | 11 | Valid M-to-B Floor | SUPPORTED | e(M,B)≥max(0,d(d+1)/2-binom(m,2)). |
| T117 | 11 | Exact B-to-A Ledger | SUPPORTED | e(B,A)=rd-r-e(B)-e(B,M), with a derived lower bound using M–B capacity. |
| T118 | 11 | Missing Cyclic Edge Theorem | SUPPORTED_DIAGNOSIS | Current valid bounds force A→M strongly and sometimes M→B, but not B→A quadratically. |
| T119 | 11 | Backward Reservoir Theorem | SUPPORTED | If e(B,A) is small, exact degree accounting forces e(B)+e(B,M) large. |
| T120 | 11 | Backward-Hierarchy Theorem | SUPPORTED_CONDITIONAL | Hereditary deficit gives a peeling order on B; dense internal arcs may point backward across it. |
| T121 | 11 | Two-Reservoir Classification Theorem | STRUCTURAL_SYNTHESIS | A surviving rooted profile stores B-degree internally or in the reverse B→M direction. |
| T122 | 11 | Pair-Marginal Phantom Theorem | PROPOSAL_MODEL | Pairwise chamber marginals admit a zero-cyclic-product profile; no actual global graph was constructed. |
| T123 | 11 | Five-Flag Necessity Theorem | METHODOLOGICAL | Rooted four-flags do not retain the correlation between internal B hierarchy, B→A degree, and A→M neighborhoods. |
| R12-T124 | 12 | Second-Neighborhood Deficit Theorem | SUPPORTED | \|N^{++}(v)\N+(v)\|≥(d+1)/2. |
| R12-T125 | 12 | Folding Creates Codegree | SUPPORTED | If two-step mass folds into a small support, row energy forces high multiplicity. |
| R12-T126 | 12 | Concentration Self-Bound | PARTIAL_RETRACTED | The exact row-energy and indegree inequalities were valid; the derived numerical q≥0.68614d was invalid. |
| R12-T127 | 12 | Forced Double-Codegree Alternative | PROPOSAL_QUALITATIVE | Insufficient expansion should create a large common-out set and forbidden rectangle. |
| R13-T124 | 13 | Retraction of the 0.686d Fan Bound | SUPPORTED | The denominator inequality was substituted in the wrong direction; q≥0.68614d is withdrawn. |
| R13-T125 | 13 | Maximum-Fan Kernel | SUPPORTED | For a high-indegree root, some two-path fan has q≥d²/(2d-1)>d/2. |
| R13-T126 | 13 | Zero-Support Maximum-Fan Inequality | SUPPORTED | d²≤q(3d-1-d^-(p)) for a fan vertex p. |
| R13-T127 | 13 | Fan-to-Inneighborhood Rectangle | SUPPORTED | For P⊆N-(y), ∪_{p∈P}N-(p) is disjoint from N+(y), hence has size at most 2d. |
| R13-T128 | 13 | Weighted Maximum-Fan Selection | SUPPORTED | Some nonempty P_{xy} has average indegree at least d. |
| R13-T129 | 13 | Dual Fan Theorem | SUPPORTED | There are x,z,y and C⊆N+(x)∩N+(z)∩N-(y) with \|C\|≥\|P\|/2 for a weighted fan P. |
| T130 | 14 | First Three Vanishing Trace Theorem | SUPPORTED | tr(A)=tr(A²)=tr(A³)=0. |
| T131 | 14 | Perron Moment Cancellation Theorem | SUPPORTED | The non-Perron eigenvalues cancel d in the first three power sums. |
| T132 | 14 | Singular-Energy Budget Theorem | SUPPORTED | \|\|A\|\|_F²=3d² and residual singular-value squared mass is at most 2d². |
| T133 | 14 | Spectral Modulus Budget | SUPPORTED | Σ_{i≥2}\|λ_i/d\|²≤2. |
| T134 | 14 | Cubic Defect Identity | SUPPORTED | Σ μ_i(1-μ_i)=Σ μ_i²(1-μ_i)=Σ μ_i(1-μ_i)²=0. |
| T135 | 14 | Real-Part Defect Formula | SUPPORTED | Re[z(1-z)²]=r cosθ-2r² cos2θ+r³ cos3θ. |
| T136 | 14 | Peripheral Period Theorem | SUPPORTED_STANDARD | For irreducible d-regular A, peripheral eigenvalues are d times roots of unity determined by the period. |
| T137 | 14 | Aperiodicity Theorem | SUPPORTED_CONDITIONAL | A minimal kernel is primitive after eliminating periods 2 and 3. |
| T138 | 14 | Strong Connectivity Theorem | SUPPORTED_CONDITIONAL | A smallest counterexample is strongly connected. |
| T139 | 14 | Strict Spectral Radius Gap | SUPPORTED_CONDITIONAL | All non-Perron eigenvalues satisfy \|λ\|<d. |
| T140 | 14 | Abstract Spectral Phantom | STRUCTURAL_DIAGNOSIS | The abstract finite moment system may be feasible; moments alone do not encode entrywise support. |
| T141 | 14 | Energy Equality Rigidity Theorem | SUPPORTED | Equality in the continuous row-energy floor forces d=1; for d>1 the inequality is strict. |
| T142 | 14 | Exact Integral Row-Energy Floor | SUPPORTED | If d²=kq+t, the integer row energy is at least (k-t)q²+t(q+1)². |
| T143 | 15 | Opposite Two-Path Product Theorem | SUPPORTED | For Q=A², tr(A⁴)=Σ_{x,y}Q_{xy}Q_{yx}=4C4(D). |
| T144 | 15 | Opposite Vertices Are Nonadjacent | SUPPORTED | Opposite vertices of a directed 4-cycle are nonadjacent. |
| T145 | 15 | Exact Nonedge Count | SUPPORTED | The number of unordered nonedges is 3d(d-1)/2. |
| T146 | 15 | Escape-Mass Floor | SUPPORTED | The ordered nonedge two-path mass is at least 3d²(d+1)/2. |
| T147 | 15 | Forced Opposite-Path Product Theorem | SUPPORTED | Σ_{unordered nonedges}Q_{xy}Q_{yx}≥3d³. |
| T148 | 15 | Cubic Directed-C4 Theorem | SUPPORTED_TERMINAL_ASSET | C4(D)≥ceil(3d³/2), equivalently tr(A⁴)≥6d³. |
| T149 | 15 | Every Kernel Contains a Directed C4 | SUPPORTED | A triangle-free exact-boundary regular kernel necessarily contains a directed 4-cycle. |
| T150 | 15 | Heavy Four-Cycle Vertex Theorem | SUPPORTED | Some vertex lies on at least 2d² directed 4-cycles. |
| T151 | 15 | Heavy Bidirectional Bridge Theorem | SUPPORTED | Some nonedge {x,y} has Q_{xy}Q_{yx}≥ceil(2d²/(2d-1)). |
| T152 | 15 | Asymmetric Four-Cycle Reservoir Theorem | STRUCTURAL_DIAGNOSIS | The C4 lower bound is compatible with Q_{xy}≈d and Q_{yx}=O(1) on significant pairs. |
| T153 | 15 | Exact Fourth-Moment Decomposition | SUPPORTED | tr(A⁴)=\|\|A²\|\|_F²-(1/2)\|\|A²-(Aᵀ)²\|\|_F²; C4 is one quarter of this. |

---

# 5. Supported Asset Cards

### R1-L1 — Neighborhood Acyclicity Pressure

**Status:** `SUPPORTED`  
**Statement:** For every v, D[N+(v)] and D[N-(v)] are directed-triangle-free; for every arc v→x, N+(x)∩N-(v)=∅.  
**Dependencies:** Triangle-free oriented graph.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### R1-L2 — Half-Degree Escape Lemma

**Status:** `SUPPORTED`  
**Statement:** For a minimum-outdegree vertex v with d=δ+(D), some x∈N+(v) has at least (d+1)/2 outneighbors in M_v.  
**Dependencies:** A→B exclusion; average internal outdegree in N+(v).  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### R1-L3 — Minimal-Counterexample Hereditary Deficit

**Status:** `SUPPORTED_CONDITIONAL`  
**Statement:** In a vertex-minimal counterexample, every proper nonempty S has a vertex x with d_S^+(x)<|S|/3.  
**Dependencies:** Vertex-minimal counterexample reduction.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### R1-ME — Minimal Escape Lemma

**Status:** `SUPPORTED_CONDITIONAL`  
**Statement:** For every proper nonempty S, some x∈S has d^+_{V\S}(x)>d-|S|/3.  
**Dependencies:** R1-L3 plus δ+(D)≥d.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T1 — Arc-Minimal Regularization Theorem

**Status:** `SUPPORTED_CONDITIONAL`  
**Statement:** After choosing a counterexample with minimum order and then minimum arcs, every vertex has outdegree d=ceil(n/3).  
**Dependencies:** Arc deletion cannot create triangles and preserves the threshold if a vertex had degree >d.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T2 — Forbidden Residue Theorem

**Status:** `SUPPORTED_CONDITIONAL`  
**Statement:** A vertex-minimal counterexample cannot have n≡1 mod 3.  
**Dependencies:** Delete any vertex from n=3m+1; remaining minimum outdegree is at least m on 3m vertices.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T3 — Universal Minimum-Tail Theorem

**Status:** `SUPPORTED_CONDITIONAL`  
**Statement:** Every vertex has an incoming tail of minimum outdegree; in the arc-minimal kernel this is automatic because all vertices have outdegree d.  
**Dependencies:** Vertex-deletion minimality; regularization.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T4 — Hereditary Deficit Theorem

**Status:** `SUPPORTED_CONDITIONAL`  
**Statement:** Every proper nonempty induced subgraph has minimum outdegree below one third of its order.  
**Dependencies:** Minimal counterexample.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T5 — Exact Escape Theorem

**Status:** `SUPPORTED_CONDITIONAL`  
**Statement:** For every proper nonempty S, some x∈S has d^+_{V\S}(x)≥d-ceil(|S|/3)+1.  
**Dependencies:** T4 and exact d-out-regularity.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T6 — A-to-B Exclusion Theorem

**Status:** `SUPPORTED`  
**Statement:** For A=N+(v), B=N-(v), E(A,B)=∅.  
**Dependencies:** Any a→b would create v→a→b→v.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T7 — Quadratic Escape-Mass Theorem

**Status:** `SUPPORTED`  
**Statement:** For |A|=d, e(A,M_v)≥d(d+1)/2 and hence |M_v|≥(d+1)/2.  
**Dependencies:** T6; e(A)≤binom(d,2).  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T8 — Two-Thirds Escape Vertex Theorem

**Status:** `SUPPORTED_CONDITIONAL`  
**Statement:** Some x∈A has |N_M^+(x)|≥d-ceil(d/3)+1>2d/3.  
**Dependencies:** T4 applied to A; exact d-out-regularity; T6.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T9 — Second-Generation Forbidden-Indegree Theorem

**Status:** `SUPPORTED`  
**Statement:** If X=N_M^+(x), then for z∈X, N+(z)∩N-(x)=∅.  
**Dependencies:** Otherwise y→x→z→y is a directed triangle.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T10 — Second-Escape Compression Theorem

**Status:** `SUPPORTED_CONDITIONAL`  
**Statement:** Applying hereditary deficit to X yields z∈X with a large external outneighbor set W=N+(z)\X, disjoint from N-(x).  
**Dependencies:** T4, exact regularity, T9.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T11 — Pair-Cell Indegree Ceiling

**Status:** `SUPPORTED_CONDITIONAL`  
**Statement:** For the selected x and X, d^-(x)≤n-d-|X|+ceil(|X|/3)-2.  
**Dependencies:** T10 and disjointness of X, W, N-(x), {x}.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T13 — Universal Three-Chamber Theorem

**Status:** `SUPPORTED`  
**Statement:** For each x, V\{x} partitions into P_x=N+(x), I_x=N-(x), M_x, and E(P_x,I_x)=∅.  
**Dependencies:** Triangle-free orientation.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T14 — Exact Escape-Slack Identity

**Status:** `SUPPORTED`  
**Statement:** If σ(x)=binom(d,2)-e(P_x), then e(P_x,M_x)=d(d+1)/2+σ(x).  
**Dependencies:** d-out-regularity and T13.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T15 — Nonneighbor Capacity Theorem

**Status:** `SUPPORTED`  
**Statement:** |M_x|≥(d+1)/2+σ(x)/d, hence an indegree upper bound follows.  
**Dependencies:** T14 and e(P_x,M_x)≤d|M_x|.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T16 — Global Nonneighbor Conservation Theorem

**Status:** `SUPPORTED`  
**Statement:** Σ_x |M_x|=n(n-1-2d); at n=3d the average is d-1.  
**Dependencies:** Outdegree sum equals indegree sum nd.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T17 — Global Defect Budget Theorem

**Status:** `SUPPORTED`  
**Statement:** Σ_xσ(x) is bounded by the global nonneighbor budget; at n=3d, Σσ(x)≤nd(d-3)/2.  
**Dependencies:** Sum T15 and use T16.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T18 — Directed Two-Path Classification Theorem

**Status:** `SUPPORTED`  
**Statement:** Every directed two-path x→p→y is either transitively closed by x→y or has nonadjacent endpoints; y→x is forbidden.  
**Dependencies:** Triangle-free orientation.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T19 — Global Escape-Path Theorem

**Status:** `SUPPORTED`  
**Statement:** The total escape two-path count is nd(d+1)/2+Σσ(x).  
**Dependencies:** T14 summed over roots.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T20 — Common-Inneighborhood Identity

**Status:** `SUPPORTED`  
**Statement:** Σ_{p→y}|N-(p)∩N-(y)|=nd(d-1)/2-Σσ(x).  
**Dependencies:** Classify two-paths by terminal arc.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T21 — Folding Conservation Theorem

**Status:** `SUPPORTED`  
**Statement:** Transitive two-path mass plus escape two-path mass equals nd²; lost transitive closure becomes escape mass one-for-one.  
**Dependencies:** T19 and T20.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T22 — High-Multiplicity Escape Pair Theorem

**Status:** `SUPPORTED`  
**Statement:** At n=3d some ordered nonadjacent pair has q(x,y)≥ceil(d(d+1)/(2(d-1)))>d/2+1.  
**Dependencies:** Average escape multiplicity using T19 and exact nonedge count.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T23 — Parallel-Bridge Chamber Theorem

**Status:** `SUPPORTED`  
**Statement:** For P=N+(x)∩N-(y), E(P,N-(x))=∅ and E(N+(y),P)=∅.  
**Dependencies:** Triangle-free orientation.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T24 — Rectangle-to-C4 Theorem

**Status:** `SUPPORTED`  
**Statement:** For H=N+(y)∩N-(x), every (p,h)∈P×H yields x→p→y→h→x; the pair lies in |P||H| directed 4-cycles.  
**Dependencies:** Definitions of P,H.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T25 — Fold-or-Expansion Theorem

**Status:** `SUPPORTED_DICHOTOMY`  
**Statement:** For any η, either |H|<ηd and L∪R expands, or |H|≥ηd and the pair supports at least ηd|P| directed 4-cycles.  
**Dependencies:** T24; elementary case split.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T26 — Rectangle Orientation Theorem

**Status:** `SUPPORTED`  
**Statement:** No arc points P→H; every adjacency between H and P is oriented H→P.  
**Dependencies:** h→x→p forbids p→h.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T28 — One-Way Rectangle Saturation Lemma

**Status:** `SUPPORTED`  
**Statement:** e(H,P)≥|H|(d-n+|P|+|H|) whenever the right side is positive.  
**Dependencies:** Outdegree capacity for vertices of H.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T29 — Escape Multiplicity Identity

**Status:** `SUPPORTED`  
**Statement:** Σ_{ordered nonedges}q(x,y)=Σ_x e(N+(x),M_x)≥nd(d+1)/2.  
**Dependencies:** T14/T19 with σ≥0.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T30 — Ordered Nonadjacency Identity

**Status:** `SUPPORTED`  
**Statement:** At n=3d the number of ordered nonadjacent pairs is n(d-1).  
**Dependencies:** Exact adjacent-pair count 2nd.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T31 — Super-Half Bridge Theorem

**Status:** `SUPPORTED`  
**Statement:** Some ordered nonedge has q(x,y)≥ceil(d(d+1)/(2(d-1)))=ceil(d/2+1+1/(d-1)).  
**Dependencies:** T29 and T30.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T32 — Bidirectional Bridge Exclusion Theorem

**Status:** `SUPPORTED`  
**Statement:** For P=N+(x)∩N-(y), H=N+(y)∩N-(x), all P–H adjacencies point H→P.  
**Dependencies:** Triangle-free orientation.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T33 — Bridge Deficit Theorem

**Status:** `SUPPORTED_CONDITIONAL`  
**Statement:** For bridge size s, d^-(x)≤n-d-s+ceil(s/3)-2.  
**Dependencies:** Hereditary deficit applied to P plus the wall N+(p)∩N-(x)=∅.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T34 — Reverse-Bridge Capacity Theorem

**Status:** `SUPPORTED`  
**Statement:** d^-(x)≤n-d-(s+1)/2; at n=3d, d^-(x)≤2d-(s+1)/2.  
**Dependencies:** Aggregate degree demand of P using only e(P)≤binom(s,2).  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T35 — Total Bridge Energy Identity

**Status:** `SUPPORTED`  
**Statement:** For fixed x, Q_x=Σ_{y∈M_x}q(x,y)=d²-e(N+(x))≥d(d+1)/2.  
**Dependencies:** Exact escape identity.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T36 — Indegree–Bridge Amplification Theorem

**Status:** `SUPPORTED`  
**Statement:** Some nonneighbor y has q(x,y)≥ceil(d(d+1)/(2(2d-1-d^-(x)))) at n=3d.  
**Dependencies:** Average T35 over M_x.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T37 — Exact Closure Criterion

**Status:** `SUPPORTED_SUFFICIENT_CONDITIONS`  
**Statement:** Any of several explicit bridge-amplification or deficit inequalities would close the kernel.  
**Dependencies:** Algebraic elimination of q and d^-(x); the listed premises were not proved.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T38 — Half-Bridge Closure Theorem

**Status:** `SUPPORTED_IMPLICATION_ONLY`  
**Statement:** If every nonedge had q(x,y)≤(d-1)/2, global escape mass would contradict the exact nonedge count.  
**Dependencies:** T29–T30.  
**Audit:** The premise is incompatible with the counterexample escape average and was never plausible as a counterexample property.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T39 — Half-Bridge Failure Structure Theorem

**Status:** `SUPPORTED`  
**Statement:** Failure of the half-bridge premise yields a large one-way rectangular certificate P,H around a nonedge.  
**Dependencies:** Definitions and T32.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T40 — High-Indegree Root Theorem

**Status:** `SUPPORTED`  
**Statement:** Some vertex has indegree at least d.  
**Dependencies:** Average indegree equals d.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T41 — Root Escape-Energy Theorem

**Status:** `SUPPORTED`  
**Statement:** For high-indegree root x, Σ_{y∈M}q_y=d²-e(A)≥d(d+1)/2.  
**Dependencies:** T6 and e(A)≤binom(d,2).  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T42 — Bridge Export Theorem

**Status:** `SUPPORTED`  
**Statement:** For bridge P of size s, e(P,U)≥s(d-1)-binom(s,2), yielding 2r+s≤4d-3 at n=3d.  
**Dependencies:** Degree accounting for P and oriented internal bound.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T43 — Reverse-Wall Theorem

**Status:** `SUPPORTED`  
**Statement:** For R=N+(y), E(R,P)=∅.  
**Dependencies:** p→y→r→p would be a triangle.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T44 — Two-Block Degree Identity

**Status:** `SUPPORTED`  
**Statement:** Exact outgoing-degree decomposition for P∪R with E(R,P)=∅.  
**Dependencies:** Finite edge partition.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T45 — Bridge Collision Identity

**Status:** `SUPPORTED`  
**Statement:** Σ_{z∈M}binom(q(x,z),2)=Σ_{pairs {a,b}⊂A}|N+(a)∩N+(b)∩M|.  
**Dependencies:** Double count common targets.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T46 — Double-Wall Escape Theorem

**Status:** `SUPPORTED_CONDITIONAL`  
**Statement:** A large common forward target set C forces |N-(a)∪N-(b)|≤2d-|C|+ceil(|C|/3)-1.  
**Dependencies:** Hereditary deficit inside C and two forbidden inneighborhood walls.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T48 — Fan-Reversal Closure Criterion

**Status:** `SUPPORTED`  
**Statement:** For I=N-(a)∩N-(b), C=N+(a)∩N+(b), E(C,I)=∅; any forced C→I arc closes a triangle.  
**Dependencies:** Triangle-free orientation.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T49 — One-Way Fan Capacity Inequality

**Status:** `SUPPORTED`  
**Statement:** |I|≤2d-(|C|+1)/2 at n=3d.  
**Dependencies:** Outdegree demand of C with E(C,I)=∅ and e(C)≤binom(|C|,2).  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T50 — Cubic-Zero Theorem

**Status:** `SUPPORTED`  
**Statement:** tr(A³)=0.  
**Dependencies:** Directed closed walks of length 3 are directed triangles.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T51 — Reverse-Arc Annihilation Theorem

**Status:** `SUPPORTED`  
**Statement:** A²∘Aᵀ=0.  
**Dependencies:** A reverse arc plus a two-path creates a triangle.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T52 — Two-Path Mass Theorem

**Status:** `SUPPORTED`  
**Statement:** Σ_{x,y}(A²)_{xy}=nd².  
**Dependencies:** A²1=d²1.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T53 — Exact Support Partition Theorem

**Status:** `SUPPORTED`  
**Statement:** Two-path mass partitions into transitive-arc endpoints and nonadjacent endpoints; reverse-arc entries vanish.  
**Dependencies:** T51 and orientation.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T54 — Escape-Mass Floor

**Status:** `SUPPORTED`  
**Statement:** Σ_{ordered nonedges}(A²)_{xy}≥nd(d+1)/2.  
**Dependencies:** T53 and e(N+(x))≤binom(d,2).  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T55 — Two-Path Collision Theorem

**Status:** `SUPPORTED`  
**Statement:** ||A²||_F²=Σ_{u,v}|N-(u)∩N-(v)|·|N+(u)∩N+(v)|.  
**Dependencies:** Expand the Frobenius norm.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T56 — Global Fan-Energy Identity

**Status:** `SUPPORTED`  
**Statement:** The common-in/common-out rectangle energy equals ||A²||_F².  
**Dependencies:** T55.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T57 — Row Concentration Theorem

**Status:** `SUPPORTED`  
**Statement:** Σ_yQ_{xy}²≥d⁴/(n-1-d^-(x)).  
**Dependencies:** Row sum d² and forced-zero support positions.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T58 — Fan-Energy Floor

**Status:** `SUPPORTED`  
**Statement:** At n=3d, ||A²||_F²≥nd⁴/(2d-1)=3d⁵/(2d-1).  
**Dependencies:** T57, convexity, average indegree d.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T60 — Maximal-Bridge Matrix Theorem

**Status:** `SUPPORTED`  
**Statement:** If μ=max Q_{xy}, then μ≥d²/(2d-1)>d/2 at n=3d.  
**Dependencies:** ||Q||_F²≤μΣQ=μnd² combined with T58.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T61 — Large Transitive-or-Escape Fan Theorem

**Status:** `SUPPORTED`  
**Statement:** Some ordered pair has more than d/2 internally distinct two-paths; endpoints are either adjacent forward or nonadjacent.  
**Dependencies:** T60 and T51.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T63 — Fan-Union Inequality

**Status:** `SUPPORTED`  
**Statement:** |∪S_p|≥(Σ|S_p|)²/Σ|S_p∩S_q| and Σ|S_p|≥sd-binom(s,2).  
**Dependencies:** Incidence Cauchy plus degree accounting.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T64 — Second-Order Concentration Theorem

**Status:** `SUPPORTED`  
**Statement:** Some p,q in a fan have a common external outneighbor set at least the average lower bound from T63.  
**Dependencies:** Averaging T63.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T66 — Fan Rectangle Prohibition Theorem

**Status:** `SUPPORTED`  
**Statement:** For I=N-(u)∩N-(v), C=N+(u)∩N+(v), E(C,I)=∅.  
**Dependencies:** Any c→i creates i→u→c→i.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T67 — Universal Fan Capacity Theorem

**Status:** `SUPPORTED`  
**Statement:** I(u,v)+(C(u,v)+1)/2≤2d at n=3d.  
**Dependencies:** Outdegree demand of C, T66, e(C)≤binom(C,2).  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T68 — Universal Indegree Ceiling

**Status:** `SUPPORTED`  
**Statement:** d^-(u)≤(3d-3)/2.  
**Dependencies:** Diagonal/rooted chamber escape calculation.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T69 — Common-Out Sum Identity

**Status:** `SUPPORTED`  
**Statement:** Σ_{u,v}C(u,v)=Σ_w d^-(w)².  
**Dependencies:** Count triples u→w←v.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T70 — Fan Energy Identity

**Status:** `SUPPORTED`  
**Statement:** ||A²||_F²=Σ_{u,v}I(u,v)C(u,v).  
**Dependencies:** T55.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T71 — Common-Out Energy Floor

**Status:** `SUPPORTED`  
**Statement:** ΣC(u,v)²≥(ΣC(u,v))²/n².  
**Dependencies:** Cauchy-Schwarz.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T72 — Two-Path Energy Floor

**Status:** `SUPPORTED`  
**Statement:** ||A²||_F²≥nd⁴/(2d-1) at n=3d.  
**Dependencies:** Same as T58.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T73 — Fan-Capacity Saturation Theorem

**Status:** `SUPPORTED`  
**Statement:** C·Λ equals missing internal adjacencies in C plus missing permitted outgoing arcs from C.  
**Dependencies:** Exact expansion of the fan-capacity slack.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T74 — Global Slack Identity

**Status:** `SUPPORTED`  
**Statement:** 2dS-||A²||_F²-(T+S)/2=Σ C(u,v)Λ(u,v).  
**Dependencies:** Sum T73.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T75 — Elimination-Ordering Theorem

**Status:** `SUPPORTED_CONDITIONAL`  
**Statement:** Every proper S has an ordering with each removed vertex having residual outdegree below one third of the remaining order.  
**Dependencies:** Hereditary deficit.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T80 — Triple-Fan Prohibition Theorem

**Status:** `SUPPORTED`  
**Statement:** For triple common-in I₃ and common-out C₃, E(C₃,I₃)=∅.  
**Dependencies:** Any common middle vertex closes a triangle.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T90 — Blow-Up Backflow Prohibition Theorem

**Status:** `PARTIAL_LOCAL_FACT`  
**Statement:** The local fact a→y implies N+(y)∩N-(a)=∅ is valid; the global near-complete blow-up conclusion was not.  
**Dependencies:** Triangle-free orientation.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T92 — Three-Layer Product-Zero Theorem

**Status:** `SUPPORTED`  
**Statement:** For B=N-(x), A=N+(x), M=M_x, tr(XYZ)=0 for cyclic matrices B→A, A→M, M→B.  
**Dependencies:** Each positive term is a directed triangle.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T95 — A-to-B Zero Theorem

**Status:** `SUPPORTED`  
**Statement:** E(A,B)=∅.  
**Dependencies:** Same as T6.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T102 — Forbidden-Rectangle Union Theorem

**Status:** `SUPPORTED`  
**Statement:** e(M,B)+|∪_{a∈A}(N_M^+(a)×N_B^-(a))|≤mr.  
**Dependencies:** Each path b→a→m forbids m→b.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T104 — One-Sided Peeling Does Not Count All Arcs

**Status:** `SUPPORTED`  
**Statement:** Residual outdegree sums count only forward arcs in the peeling order.  
**Dependencies:** Direct audit of T75.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T105 — Exact Refutation of the Hereditary Edge Bound

**Status:** `SUPPORTED`  
**Statement:** A transitive tournament can have zero residual outdegree under a removal order while containing binom(s,2) arcs.  
**Dependencies:** Explicit construction.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T106 — Outneighborhood Wall Theorem

**Status:** `SUPPORTED`  
**Statement:** E(A,B)=∅.  
**Dependencies:** Triangle-free orientation.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T107 — Exact Local Defect Identity

**Status:** `SUPPORTED`  
**Statement:** e(A,M)=d(d+1)/2+σ(x).  
**Dependencies:** Regularity and T106.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T108 — Reverse-Arc Annihilation Theorem

**Status:** `SUPPORTED`  
**Statement:** A²∘Aᵀ=0.  
**Dependencies:** Triangle-free orientation.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T109 — Two-Path Conservation Theorem

**Status:** `SUPPORTED`  
**Statement:** A²1=d²1 and ΣQ=nd².  
**Dependencies:** Regularity.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T110 — Valid Indegree Ceiling

**Status:** `SUPPORTED`  
**Statement:** d^-(x)≤(3d-3)/2.  
**Dependencies:** T107 and capacity.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T111 — Correct Terminal Obstruction Theorem

**Status:** `SUPPORTED_SUMMARY`  
**Statement:** The audited elementary kernel forces escape mass but permits backward density, overlap, concentration, and long-range folding.  
**Dependencies:** Synthesis of valid assets.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T113 — Rooted Chamber Equations

**Status:** `SUPPORTED`  
**Statement:** Rooted sizes and E(A,B)=∅; d²=e(A)+e(A,M).  
**Dependencies:** Kernel.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T114 — Rooted Cyclic Product-Zero Theorem

**Status:** `SUPPORTED`  
**Statement:** Σ_{b,a,m}X_{ba}Y_{am}Z_{mb}=0.  
**Dependencies:** Each term is b→a→m→b.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T115 — Tripartite Union-Bound Theorem

**Status:** `SUPPORTED`  
**Statement:** m e(B,A)+r e(A,M)+d e(M,B)≤2drm.  
**Dependencies:** XYZ≥X+Y+Z-2 summed over triples.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T116 — Valid M-to-B Floor

**Status:** `SUPPORTED`  
**Statement:** e(M,B)≥max(0,d(d+1)/2-binom(m,2)).  
**Dependencies:** Degree accounting, orientedness, valid escape floor.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T117 — Exact B-to-A Ledger

**Status:** `SUPPORTED`  
**Statement:** e(B,A)=rd-r-e(B)-e(B,M), with a derived lower bound using M–B capacity.  
**Dependencies:** Degree partition for B.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T118 — Missing Cyclic Edge Theorem

**Status:** `SUPPORTED_DIAGNOSIS`  
**Statement:** Current valid bounds force A→M strongly and sometimes M→B, but not B→A quadratically.  
**Dependencies:** T113–T117.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T119 — Backward Reservoir Theorem

**Status:** `SUPPORTED`  
**Statement:** If e(B,A) is small, exact degree accounting forces e(B)+e(B,M) large.  
**Dependencies:** T117.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T120 — Backward-Hierarchy Theorem

**Status:** `SUPPORTED_CONDITIONAL`  
**Statement:** Hereditary deficit gives a peeling order on B; dense internal arcs may point backward across it.  
**Dependencies:** T75 plus T104 warning.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### R12-T124 — Second-Neighborhood Deficit Theorem

**Status:** `SUPPORTED`  
**Statement:** |N^{++}(v)\N+(v)|≥(d+1)/2.  
**Dependencies:** Same escape-capacity calculation as T7.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### R12-T125 — Folding Creates Codegree

**Status:** `SUPPORTED`  
**Statement:** If two-step mass folds into a small support, row energy forces high multiplicity.  
**Dependencies:** Row-sum Cauchy; equivalent to T57.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### R13-T124 — Retraction of the 0.686d Fan Bound

**Status:** `SUPPORTED`  
**Statement:** The denominator inequality was substituted in the wrong direction; q≥0.68614d is withdrawn.  
**Dependencies:** Direct inequality audit.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### R13-T125 — Maximum-Fan Kernel

**Status:** `SUPPORTED`  
**Statement:** For a high-indegree root, some two-path fan has q≥d²/(2d-1)>d/2.  
**Dependencies:** Row support and average.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### R13-T126 — Zero-Support Maximum-Fan Inequality

**Status:** `SUPPORTED`  
**Statement:** d²≤q(3d-1-d^-(p)) for a fan vertex p.  
**Dependencies:** Two-path sums supported outside N-(p) and bounded by global maximum q.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### R13-T127 — Fan-to-Inneighborhood Rectangle

**Status:** `SUPPORTED`  
**Statement:** For P⊆N-(y), ∪_{p∈P}N-(p) is disjoint from N+(y), hence has size at most 2d.  
**Dependencies:** z→p→y forbids y→z.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### R13-T128 — Weighted Maximum-Fan Selection

**Status:** `SUPPORTED`  
**Statement:** Some nonempty P_{xy} has average indegree at least d.  
**Dependencies:** Double count Σ_{x,y}Σ_{p∈Pxy}d^-(p)=dΣ_p d^-(p)².  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### R13-T129 — Dual Fan Theorem

**Status:** `SUPPORTED`  
**Statement:** There are x,z,y and C⊆N+(x)∩N+(z)∩N-(y) with |C|≥|P|/2 for a weighted fan P.  
**Dependencies:** T127, T128, incidence averaging.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T130 — First Three Vanishing Trace Theorem

**Status:** `SUPPORTED`  
**Statement:** tr(A)=tr(A²)=tr(A³)=0.  
**Dependencies:** No loops, digons, or directed triangles.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T131 — Perron Moment Cancellation Theorem

**Status:** `SUPPORTED`  
**Statement:** The non-Perron eigenvalues cancel d in the first three power sums.  
**Dependencies:** A1=d1 and T130.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T132 — Singular-Energy Budget Theorem

**Status:** `SUPPORTED`  
**Statement:** ||A||_F²=3d² and residual singular-value squared mass is at most 2d².  
**Dependencies:** A has 3d² ones and singular norm dominates Perron direction.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T133 — Spectral Modulus Budget

**Status:** `SUPPORTED`  
**Statement:** Σ_{i≥2}|λ_i/d|²≤2.  
**Dependencies:** Eigenvalue moduli are bounded by singular-value energy.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T134 — Cubic Defect Identity

**Status:** `SUPPORTED`  
**Statement:** Σ μ_i(1-μ_i)=Σ μ_i²(1-μ_i)=Σ μ_i(1-μ_i)²=0.  
**Dependencies:** Subtract normalized moment equations.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T135 — Real-Part Defect Formula

**Status:** `SUPPORTED`  
**Statement:** Re[z(1-z)²]=r cosθ-2r² cos2θ+r³ cos3θ.  
**Dependencies:** Direct algebra.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T136 — Peripheral Period Theorem

**Status:** `SUPPORTED_STANDARD`  
**Statement:** For irreducible d-regular A, peripheral eigenvalues are d times roots of unity determined by the period.  
**Dependencies:** Perron–Frobenius theory.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T137 — Aperiodicity Theorem

**Status:** `SUPPORTED_CONDITIONAL`  
**Statement:** A minimal kernel is primitive after eliminating periods 2 and 3.  
**Dependencies:** T138 plus class-size/arc-count arguments.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T138 — Strong Connectivity Theorem

**Status:** `SUPPORTED_CONDITIONAL`  
**Statement:** A smallest counterexample is strongly connected.  
**Dependencies:** A sink SCC would be a smaller induced counterexample.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T139 — Strict Spectral Radius Gap

**Status:** `SUPPORTED_CONDITIONAL`  
**Statement:** All non-Perron eigenvalues satisfy |λ|<d.  
**Dependencies:** T137.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T141 — Energy Equality Rigidity Theorem

**Status:** `SUPPORTED`  
**Statement:** Equality in the continuous row-energy floor forces d=1; for d>1 the inequality is strict.  
**Dependencies:** Uniform support plus integrality and gcd(d,2d-1)=1.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T142 — Exact Integral Row-Energy Floor

**Status:** `SUPPORTED`  
**Statement:** If d²=kq+t, the integer row energy is at least (k-t)q²+t(q+1)².  
**Dependencies:** Convexity over integer vectors.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T143 — Opposite Two-Path Product Theorem

**Status:** `SUPPORTED`  
**Statement:** For Q=A², tr(A⁴)=Σ_{x,y}Q_{xy}Q_{yx}=4C4(D).  
**Dependencies:** Closed length-4 walks in an oriented loopless graph are directed 4-cycles.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T144 — Opposite Vertices Are Nonadjacent

**Status:** `SUPPORTED`  
**Statement:** Opposite vertices of a directed 4-cycle are nonadjacent.  
**Dependencies:** Either diagonal orientation creates a directed triangle.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T145 — Exact Nonedge Count

**Status:** `SUPPORTED`  
**Statement:** The number of unordered nonedges is 3d(d-1)/2.  
**Dependencies:** Total pairs minus 3d² occupied adjacent pairs.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T146 — Escape-Mass Floor

**Status:** `SUPPORTED`  
**Statement:** The ordered nonedge two-path mass is at least 3d²(d+1)/2.  
**Dependencies:** Rootwise escape mass summed.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T147 — Forced Opposite-Path Product Theorem

**Status:** `SUPPORTED`  
**Statement:** Σ_{unordered nonedges}Q_{xy}Q_{yx}≥3d³.  
**Dependencies:** Pointwise (d-a)(d-b)≥0 plus T145–T146.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T148 — Cubic Directed-C4 Theorem

**Status:** `SUPPORTED_TERMINAL_ASSET`  
**Statement:** C4(D)≥ceil(3d³/2), equivalently tr(A⁴)≥6d³.  
**Dependencies:** T143 and T147.  
**Audit:** No additional caveat.  
**Certificate route:** Exact integer checker; Lean trace formalization.

### T149 — Every Kernel Contains a Directed C4

**Status:** `SUPPORTED`  
**Statement:** A triangle-free exact-boundary regular kernel necessarily contains a directed 4-cycle.  
**Dependencies:** T148.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T150 — Heavy Four-Cycle Vertex Theorem

**Status:** `SUPPORTED`  
**Statement:** Some vertex lies on at least 2d² directed 4-cycles.  
**Dependencies:** Average T148 over 3d vertices.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T151 — Heavy Bidirectional Bridge Theorem

**Status:** `SUPPORTED`  
**Statement:** Some nonedge {x,y} has Q_{xy}Q_{yx}≥ceil(2d²/(2d-1)).  
**Dependencies:** Average the heavy-vertex product over its nonneighbors.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification

### T153 — Exact Fourth-Moment Decomposition

**Status:** `SUPPORTED`  
**Statement:** tr(A⁴)=||A²||_F²-(1/2)||A²-(Aᵀ)²||_F²; C4 is one quarter of this.  
**Dependencies:** Symmetric/skew decomposition of Q.  
**Audit:** No additional caveat.  
**Certificate route:** Exact finite/integer proof or local combinatorial verification


---

# 6. Detailed Proof Estate


## A. Exact-boundary kernel

Assume an oriented graph \(D\) on \(3d\) vertices satisfies
\[
d^+(v)=d\quad\forall v
\]
and contains no directed triangle. Let \(A\) be its adjacency matrix and \(Q=A^2\).

The regular exact-boundary kernel is the mathematically clean object on which the strongest terminal theorem is stated. A smallest-counterexample reduction is needed only to justify why this kernel is the right CH3 boundary object; the cubic \(C_4\) theorem itself assumes the kernel directly.

## B. Outneighborhood wall and escape mass

Fix \(x\). Put
\[
P=N^+(x),\qquad I=N^-(x),\qquad M=V\setminus(P\cup I\cup\{x\}).
\]

If \(p\in P\), \(i\in I\), and \(p\to i\), then
\[
x\to p\to i\to x
\]
is a directed triangle. Therefore:
\[
E(P,I)=\varnothing.
\]

The \(d\) vertices of \(P\) emit exactly \(d^2\) arcs. All land in \(P\cup M\):
\[
d^2=e(P)+e(P,M).
\]

Because \(D[P]\) is oriented:
\[
e(P)\le\binom d2.
\]
Thus:
\[
e(P,M)\ge d^2-\binom d2=\frac{d(d+1)}2.
\]

Every arc \(p\to y\) with \(p\in P\) and \(y\in M\) is a two-path
\[
x\to p\to y
\]
whose endpoints are nonadjacent. Hence:
\[
\sum_{y\not\sim x}Q_{xy}
=e(P,M)
\ge\frac{d(d+1)}2.
\]

Summing over all \(x\):
\[
\sum_{\substack{(x,y)\\x\not\sim y}Q_{xy}
\ge\frac{3d^2(d+1)}2.
\]

## C. Exact nonedge count

The graph has
\[
|E(D)|=\sum_xd^+(x)=3d^2
\]
arcs. There are no digons, so these occupy \(3d^2\) unordered adjacent pairs.

Therefore the number of unordered nonedges is:
\[
N_0=\binom{3d}{2}-3d^2=\frac{3d(d-1)}2.
\]

## D. Opposite-path product inequality

For an unordered nonedge \(\{x,y\}\), write:
\[
a=Q_{xy},\qquad b=Q_{yx}.
\]
Since \(x\) and \(y\) each have exactly \(d\) outneighbors:
\[
0\le a,b\le d.
\]

Therefore:
\[
(d-a)(d-b)\ge0.
\]
Expanding:
\[
ab\ge d(a+b-d).
\]

Sum over unordered nonedges:
\[
\sum_{\{x,y\}Q_{xy}Q_{yx}
\ge
d\left(
\sum_{\{x,y\}(Q_{xy}+Q_{yx})-dN_0
\right).
\]

The first sum is the ordered nonedge two-path mass:
\[
\sum_{\{x,y\}(Q_{xy}+Q_{yx})
\ge\frac{3d^2(d+1)}2.
\]
Also:
\[
dN_0=\frac{3d^2(d-1)}2.
\]
Subtract:
\[
\frac{3d^2((d+1)-(d-1))}{2}=3d^2.
\]
Multiply by \(d\):
\[
\boxed{
\sum_{\{x,y\}\text{ nonedge}Q_{xy}Q_{yx}\ge3d^3.
}
\]

## E. Conversion to directed \(4\)-cycles

A term in \(Q_{xy}Q_{yx}\) chooses vertices \(u,v\) with:
\[
x\to u\to y,\qquad y\to v\to x.
\]
The vertices are distinct. If \(u=v\), then both \(u\to y\) and \(y\to u\), a forbidden digon.

Thus every choice gives:
\[
x\to u\to y\to v\to x,
\]
a directed \(4\)-cycle.

Conversely each directed \(4\)-cycle is counted once for each of its two unordered opposite pairs. Therefore:
\[
\sum_{\{x,y\}\text{ nonedge}Q_{xy}Q_{yx}=2C_4(D).
\]

Hence:
\[
2C_4(D)\ge3d^3,
\]
so:
\[
\boxed{
C_4(D)\ge\left\lceil\frac{3d^3}{2}\right\rceil.
}
\]

Every directed \(4\)-cycle contributes four starting points to \(\operatorname{tr}(A^4)\):
\[
\boxed{
\operatorname{tr}(A^4)=4C_4(D)\ge6d^3.
}
\]

## F. Two-path energy and skew decomposition

Let:
\[
Q=A^2.
\]
Then:
\[
\operatorname{tr}(A^4)=\sum_{x,y}Q_{xy}Q_{yx}.
\]

Use:
\[
Q=\frac{Q+Q^{\mathsf T}2+\frac{Q-Q^{\mathsf T}2.
\]
A direct norm computation gives:
\[
\boxed{
\operatorname{tr}(A^4)
=
\|Q\|_F^2-\frac12\|Q-Q^{\mathsf T}\|_F^2.
}
\]

Equivalently:
\[
\boxed{
C_4(D)
=
\frac14\|A^2\|_F^2
-\frac18\|A^2-(A^{\mathsf T})^2\|_F^2.
}
\]

This is the cleanest exact expression of the surviving obstruction:

- triangle-freeness and regularity force large two-path energy;
- directional asymmetry subtracts from the symmetric opposite-path product that creates directed \(4\)-cycles.

## G. Row-energy floor

Every row of \(Q\) sums to \(d^2\).

If \(y\to x\), then \(Q_{xy}=0\). Also \(Q_{xx}=0\). Thus row \(x\) has support at most:
\[
k_x=3d-1-d^-(x).
\]

By Cauchy:
\[
\sum_yQ_{xy}^2\ge\frac{d^4}{k_x}.
\]
Summing and using average indegree \(d\):
\[
\boxed{
\|A^2\|_F^2\ge\frac{3d^5}{2d-1}.
}
\]

Exact equality for \(d>1\) is impossible because it would require the integral row values to equal \(d^2/(2d-1)\), forcing \(2d-1\mid d^2\) and hence \(d=1\).

## H. Strong connectivity and aperiodicity under minimality

For a smallest counterexample, a sink strongly connected component \(S\) has no outgoing arcs. Hence each vertex of \(S\) has all \(d\) outneighbors in \(S\), so:
\[
\delta^+(D[S])\ge d\ge|S|/3.
\]
If \(S\subsetneq V\), it is a smaller counterexample. Therefore \(D\) is strongly connected.

If its period were \(3\), all three cyclic classes would have size \(d\) and the links between consecutive classes would be complete, producing directed triangles.

If its period were \(2\), the oriented bipartite graph would have at most \(9d^2/4\) arcs, below the required \(3d^2\).

Hence a minimal kernel is primitive.


---


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


---


# Failed Kill-Shot Register

## 1. Pair-cell overflow
Large escape sets can overlap earlier forward layers. Triangle-freeness forbids only immediate returns into relevant inneighborhoods.

## 2. Single high-indegree contradiction
Pair-cell upper bounds on a selected indegree remained above the average indegree \(d\).

## 3. Half-bridge
The universal half-bridge premise would close by counting, but exact escape mass forces some counterexample bridge to violate it. It was only a sufficient contradiction condition.

## 4. Common-target concentration
Large common outneighborhoods form transitive fans, not necessarily directed triangles.

## 5. Fan rectangle
Large common in/out neighborhoods create a one-way rectangle \(I\to C\). The legal direction can absorb degree.

## 6. Fan cascade
Second-order concentration did not automatically reproduce the same hypotheses recursively.

## 7. Hereditary edge density
Killed by the backward-arc omission.

## 8. Three-layer Mantel
The near-close depended on the false induced-edge density upgrade.

## 9. Whole-chamber tripartite extremal
A triangle-free subgraph can split original chambers; the best whole-chamber cut is not automatically a universal upper bound.

## 10. Forbidden rectangle union
Large rectangle areas may anticorrelate and overlap heavily.

## 11. Four-flag product
Valid product-zero inequalities did not force the missing \(B\to A\) layer because \(B\) can store degree internally or in \(B\to M\).

## 12. Spectrum-only moments
Complex phase freedom survives the first three power sums and the residual energy budget.

## 13. Periodic kernel
This route succeeded: periods \(2\) and \(3\) are impossible. The primitive case remains.

## 14. Uniform row-energy equality
This route succeeded only in proving strictness; it did not yield a proportional gap.

## 15. Fourth-moment total mass
This route succeeded in forcing cubic directed-\(C_4\) mass. It does not force a linear–linear opposite pair because products can be highly asymmetric.


---

# 9. Exact Closure Program

A complete proof program from the surviving estate is:

\[
\begin{aligned}
S1:\;&\text{reduce a smallest counterexample to the exact-boundary regular kernel};\\
S2:\;&A^2\circ A^{\mathsf T}=0;\\
S3:\;&\sum_{x\not\sim y}(A^2)_{xy}\ge\frac{3d^2(d+1)}2;\\
S4:\;&C_4(D)\ge\left\lceil\frac{3d^3}2\right\rceil;\\
S5:\;&\operatorname{tr}(A^4)
=\|A^2\|_F^2-\frac12\|A^2-(A^{\mathsf T})^2\|_F^2;\\
S6:\;&\text{the kernel constraints force an incompatible skew-energy bound};\\
S7:\;&\bot.
\end{aligned}
\]

Steps \(S2\)–\(S5\) are supported in this estate.

Step \(S1\) is a standard minimality program whose exact handling of nonmultiples of three should be formalized carefully.

Step \(S6\) is the sole live mathematical closure obligation. It is unsupported.

---

# 10. Highest-Value Formula Bank

1. Root wall:
   \[
   E(N^+(x),N^-(x))=\varnothing.
   \]

2. Root escape:
   \[
   e(N^+(x),M_x)
   =
   d^2-e(D[N^+(x)])
   \ge\frac{d(d+1)}2.
   \]

3. Indegree ceiling:
   \[
   d^-(x)\le\frac{3d-3}2.
   \]

4. Reverse-arc annihilation:
   \[
   A^2\circ A^{\mathsf T}=0.
   \]

5. Two-path row sum:
   \[
   A^2\mathbf1=d^2\mathbf1.
   \]

6. Ordered nonedge two-path mass:
   \[
   \sum_{x\not\sim y}(A^2)_{xy}
   \ge\frac{3d^2(d+1)}2.
   \]

7. Unordered nonedges:
   \[
   N_0=\frac{3d(d-1)}2.
   \]

8. Opposite product:
   \[
   \sum_{\{x,y\}\text{ nonedge}}
   (A^2)_{xy}(A^2)_{yx}
   \ge3d^3.
   \]

9. Directed four-cycles:
   \[
   C_4(D)\ge\left\lceil\frac{3d^3}2\right\rceil.
   \]

10. Trace:
    \[
    \operatorname{tr}(A^4)\ge6d^3.
    \]

11. Two-path energy:
    \[
    \|A^2\|_F^2\ge\frac{3d^5}{2d-1},
    \]
    strict for \(d>1\).

12. Skew decomposition:
    \[
    \operatorname{tr}(A^4)
    =
    \|A^2\|_F^2
    -\frac12\|A^2-(A^{\mathsf T})^2\|_F^2.
    \]

13. Weighted fan:
    \[
    \exists P_{xy}\ne\varnothing:
    \frac1{|P_{xy}|}\sum_{p\in P_{xy}}d^-(p)\ge d.
    \]

14. Strong connectivity and primitivity hold for a smallest exact-boundary kernel.

---

# 11. Permanent Do-Not-Use List

- `Exact Hereditary Edge Bound`
- every \(F(s)\)-based induced-density estimate
- `Five-Sixths Escape Theorem`
- `Five-Sixths Bridge Theorem`
- `Seven-Sixths Indegree Barrier`
- \(0.68614d\) fan bound
- near-Mantel closure derived from the false density ledger
- recursive fan cascade without a separately proved invariance lemma
- any claim that the cubic \(C_4\) theorem closes CH3 by itself

---

# 12. Machine Verification Program

See `MACHINE-ATTACK-SPEC.json` and `COMPUTATIONAL-ATTACK-PLAN.md`.

Minimum symbolic checker for the principal theorem:

1. verify orientation, zero diagonal, and row sum \(d\);
2. verify \(n=3d\);
3. verify triangle-free;
4. compute \(Q=A^2\);
5. count unordered nonedges;
6. verify root escape mass;
7. verify pointwise
   \[
   (d-Q_{xy})(d-Q_{yx})\ge0;
   \]
8. sum to obtain opposite product \(\ge3d^3\);
9. verify its equality with twice the directed-\(C_4\) count;
10. conclude trace \(\ge6d^3\).

---

# 13. Novelty Boundary

No theorem in this bundle is asserted globally novel.

After exact verification, perform literature checks for:

- the exact cubic \(C_4\) lower bound;
- the trace form;
- the opposite two-path product inequality;
- the heavy \(C_4\)-vertex corollary;
- the heavy bidirectional bridge corollary;
- use of the skew decomposition in CH literature.

Truth and novelty remain orthogonal.

---

# 14. Publication-Ready Core

The cleanest potential note is not a claimed CH solution. It is the exact theorem:

> Every directed-triangle-free oriented \(d\)-out-regular graph on \(3d\) vertices contains at least \(\lceil3d^3/2\rceil\) directed \(4\)-cycles.

The proof is short, integer-exact, and independent of the invalid branches.

A publication attempt should proceed only after:

1. independent machine verification;
2. literature novelty review;
3. careful comparison of cycle-count conventions;
4. formal or certificate-backed proof release.

---

# 15. One-Page Agent Handoff

**Flagship:** CH3 remains open.

**Kernel:** triangle-free oriented graph on \(3d\) vertices, every outdegree \(d\).

**Never use:** hereditary induced-edge sparsity, \(5/6\), \(7/6\), or \(0.686d\) branches.

**Verify first:**
\[
C_4(D)\ge\left\lceil\frac{3d^3}2\right\rceil
\quad\Longleftrightarrow\quad
\operatorname{tr}(A^4)\ge6d^3.
\]

**Proof spine:**
\[
\sum_{x\not\sim y}Q_{xy}\ge\frac{3d^2(d+1)}2,
\]
\[
N_0=\frac{3d(d-1)}2,
\]
\[
(d-Q_{xy})(d-Q_{yx})\ge0,
\]
\[
\sum_{\{x,y\}}Q_{xy}Q_{yx}\ge3d^3,
\]
then divide by the two opposite pairs per \(C_4\).

**Live obstruction:**
\[
\|A^2-(A^{\mathsf T})^2\|_F^2.
\]

**Mission:** find and certify a universal skew-energy inequality incompatible with the full exact-boundary kernel.

---

# 16. Final Court Record

- `THEOREM_CLOSURE`: **NO**
- `STRICT_FRONTIER_THEOREM`: **POSSIBLE ONLY AFTER VERIFICATION + NOVELTY REVIEW**
- `SURVIVING_CAPABILITY`: **YES**
- `PRINCIPAL RESULT`: cubic directed-\(C_4\) lower bound
- `EXACT OPEN OBLIGATION`: skew two-path energy closure
- `RETRACTION AUDIT`: complete in this bundle
- `MACHINE READINESS`: theorem ledger, JSON state, verification plan, Lean plan, and search plan included
