# Exact-boundary fourth-moment chain

**Author:** Jared Wilder  
**Source:** recovered fifteen-round Caccetta–Häggkvist packet  
**Human extraction:** 2026-09-14  
**Authority:** source-supported terminal assets; **not freshly independently replayed by this release**.  
**Flagship status:** the Caccetta–Häggkvist conjecture remains **OPEN**.

This note surfaces the strongest quantitative exact-boundary chain that is otherwise buried in the recovered theorem ledger.

## Setup

Assume an oriented graph `D` on

```text
n = 3d
```

vertices satisfies

```text
d⁺(v) = d   for every vertex v
```

and contains no directed triangle.

Let `A` be its adjacency matrix and put

```text
Q = A².
```

The conclusions below concern exactly this regular `n=3d` triangle-free kernel.

---

## 1. Rootwise escape-mass floor

Fix a vertex `x` and let

```text
P = N⁺(x).
```

Because the graph is directed-triangle-free, no arc from `P` can land in `N⁻(x)`.

The `d` vertices of `P` emit exactly `d²` arcs. Since `D[P]` is oriented,

```text
e(P) ≤ binom(d,2).
```

Therefore at least

```text
d² - binom(d,2) = d(d+1)/2
```

arcs run from `P` to vertices nonadjacent to `x`. Every such arc gives a two-path from `x` to a nonneighbor. Hence

```text
∑_{y not adjacent to x} Q_xy ≥ d(d+1)/2.
```

Summing over all `3d` roots gives

```text
∑_{ordered (x,y), x not adjacent to y} Q_xy
    ≥ 3d²(d+1)/2.
```

---

## 2. Exact nonedge count

The graph has

```text
|E(D)| = 3d²
```

arcs. There are no digons, so these occupy `3d²` unordered adjacent pairs. Thus the number `N₀` of unordered nonedges is

```text
N₀ = binom(3d,2) - 3d²
   = 3d(d-1)/2.
```

---

## 3. Opposite-path product inequality

For an unordered nonedge `{x,y}`, set

```text
a = Q_xy,
b = Q_yx.
```

Because each vertex has exactly `d` outneighbors,

```text
0 ≤ a,b ≤ d.
```

Thus

```text
(d-a)(d-b) ≥ 0,
```

which rearranges to

```text
ab ≥ d(a+b-d).
```

Summing over unordered nonedges and inserting the escape-mass floor and exact value of `N₀` yields

```text
∑_{ {x,y} nonedge } Q_xy Q_yx ≥ 3d³.
```

This is the packet's T147.

---

## 4. Directed four-cycle theorem

A term in

```text
Q_xy Q_yx
```

chooses two directed two-paths

```text
x → u → y,
y → v → x.
```

The intermediate vertices are distinct; otherwise a digon appears. Therefore each choice gives a directed 4-cycle

```text
x → u → y → v → x.
```

Conversely, every directed 4-cycle is counted once for each of its two opposite unordered pairs. Hence

```text
∑_{ {x,y} nonedge } Q_xy Q_yx = 2 C₄(D).
```

Combining with the product lower bound gives

```text
2 C₄(D) ≥ 3d³,
```

so

> **C₄(D) ≥ ceil(3d³/2).**

Equivalently,

```text
tr(A⁴) = 4 C₄(D) ≥ 6d³.
```

This is T148 in the source ledger and is the strongest quantitative theorem in this exact-boundary chain.

In particular, every such kernel contains at least one directed 4-cycle. That corollary is T149.

---

## 5. Exact fourth-moment skew decomposition

The same source records

```text
tr(A⁴) = ∑_{x,y} Q_xy Q_yx.
```

With `Q=A²`, the symmetric/skew decomposition gives

```text
tr(A⁴)
  = ||Q||_F² - (1/2)||Q-Qᵀ||_F².
```

Equivalently,

```text
C₄(D)
  = (1/4)||A²||_F²
    - (1/8)||A²-(Aᵀ)²||_F².
```

This is T153.

It identifies the surviving escape mechanism after the forced two-path energy:

> **skew two-path energy.**

Triangle-freeness and regularity force substantial two-path energy, while directional asymmetry can subtract from the symmetric opposite-path product that produces directed 4-cycles.

---

## 6. Concentration consequences

Averaging the 4-cycle lower bound over the `3d` vertices gives:

> **some vertex lies on at least `2d²` directed 4-cycles.**

A further averaging argument in the source gives an unordered nonedge `{x,y}` with

```text
Q_xy Q_yx ≥ ceil(2d²/(2d-1)).
```

These are the packet's T150/T151 concentration consequences.

---

## What this proves — and what it does not

The exact-boundary structural spine is

```text
escape two-path mass
    ↓
opposite-path product
    ↓
many directed C₄
    ↓
skew-energy obstruction.
```

The source extraction marks the central C4 theorem as a supported terminal asset. Its dependency chain is explicit, and the historical packet advertises an exact-integer checker / Lean trace route.

However, this September 14 human publication **does not claim a fresh independent replay of those artifacts**. The repository's recovered-source warning remains in force.

Most importantly:

- the theorem forces directed 4-cycles, not directed triangles;
- it does not close the `r=3` Caccetta–Häggkvist conjecture;
- historical novelty / priority is not asserted here.

Correct status:

> **exact source-supported boundary theorem chain; fresh independent checker/formal replay and literature-priority court remain separate work.**
