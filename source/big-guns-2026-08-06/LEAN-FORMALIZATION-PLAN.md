# Lean / Kernel Formalization Plan

## Phase 1 — Finite digraph primitives

Define:

- finite vertex type;
- adjacency predicate `E : V → V → Prop`;
- loopless;
- oriented/no digons;
- outdegree and indegree;
- directed triangle;
- directed 4-cycle;
- two-path count;
- adjacency matrix over `Nat` or `Int`.

## Phase 2 — Local kernel

1. `no_arc_outNbr_to_inNbr`
2. `escape_mass_root`
3. `indegree_ceiling`
4. `reverse_arc_two_path_zero`
5. `two_path_row_sum`

## Phase 3 — Cubic C4 theorem

6. `unordered_nonedge_count`
7. `two_path_nonedge_mass`
8. `opposite_product_pointwise`
9. `opposite_product_sum`
10. `opposite_two_paths_distinct`
11. `opposite_two_paths_form_C4`
12. `C4_counted_by_two_opposite_pairs`
13. `cubic_directed_C4_lower_bound`
14. `trace_four_lower_bound`

Recommended first endpoint:
\[
\operatorname{tr}(A^4)\ge6d^3.
\]
This avoids quotienting cycles by cyclic rotation until after the matrix theorem is closed.

## Phase 4 — Energy identities

15. `row_energy_cauchy`
16. `global_two_path_energy_floor`
17. `integer_row_energy_floor`
18. `fourth_moment_skew_decomposition`

## Phase 5 — Minimality reductions

19. `arc_minimal_regularization`
20. `minimal_counterexample_strongly_connected`
21. `period_two_impossible`
22. `period_three_impossible`
23. `minimal_counterexample_primitive`

## Axiom audit target

- no custom axioms;
- finite counting only;
- algebraic identities via `ring`;
- inequalities via `omega`, `nlinarith`, or explicit sum lemmas;
- cycle counting convention explicitly documented.
