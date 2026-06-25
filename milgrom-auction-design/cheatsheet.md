# Cheatsheet

## Mechanism Choice

| Situation | Prefer | Because |
|---|---|---|
| Homogeneous good, simple capacity | Posted prices or standard auction | Price can express scarcity well |
| Goods are gross substitutes | Ascending/descending price auction | Monotone price adjustment is stable |
| Indivisible capacity with near-substitutes | Greedy threshold auction or clock auction | Monotone approximation supports incentives |
| Strong complements | Package bidding, central coordination, or richer mechanism | Simple prices can fail badly |
| Exact optimization feasible and reports simple | Vickrey benchmark may be practical | Efficient and strategy-proof |
| Exact optimization infeasible | Greedy/deferred-acceptance mechanism | Approximate allocation with better transparency |
| Bidders must understand incentives easily | Obviously strategy-proof clock design | Avoids contingent reasoning |
| Winners need value privacy | Clock auction | Winners reveal less than full valuations |

## Fast Diagnostics

| Ask | If yes | Design implication |
|---|---|---|
| Does feasibility depend on combinations? | Complex constraint | Add feasibility algorithm |
| Are units heterogeneous by location/time/adjacency? | Product complexity | Avoid one aggregate price |
| Does raising one price increase demand for others? | Substitutes | Monotone prices likely useful |
| Does value require bundles? | Complements | Beware Vickrey/core failures |
| Is exact optimization NP-hard or unverifiable? | Computation barrier | Avoid exact Vickrey pricing |
| Can bidders state all package values? | If no | Avoid sealed direct mechanisms |
| Would participants distrust opaque payments? | Yes | Use dynamic clock rules |
| Is market quantity endogenous? | Yes | Use staged target adjustment |

## Vickrey Go / No-Go

Use Vickrey only when all are mostly true:

| Condition | Required confidence |
|---|---|
| Efficient allocation can be computed exactly | High |
| Counterfactual winner-omission prices can be computed accurately | High |
| Bidders can report values compactly | High |
| Budgets or credit limits do not distort bidding | High |
| Value disclosure is acceptable | Medium-high |
| Complements do not create core risk | Medium-high |

If any of the first three fail, treat Vickrey as a benchmark, not the mechanism.

## Deferred-Acceptance Clock Rule

| Step | Rule |
|---|---|
| Start | Quote high prices to all active sellers |
| Price move | Lower prices only for inessential active bidders |
| Bidder action | Stay active while price >= value; exit when price < value |
| Feasibility | If bidder exit would make target infeasible, freeze as essential |
| End | Winners are active bidders; pay final clock prices |

## FCC-Style Staging

| Stage | Decision |
|---|---|
| Initial commitments | Which incumbents are willing to participate at opening prices |
| Clearing target | Maximum feasible repurposing target from commitments |
| Reverse auction | Cost to acquire enough incumbent rights |
| Forward auction | Revenue from new users |
| Final-stage rule | Close if revenue covers costs and thresholds |
| Lower target | If not enough revenue, reduce spectrum target |
| Assignment rounds | Resolve exact frequency preferences |

## Design Smells

- If every unit needs its own price, product definition is too fine.
- If one owner can block a large reallocation, property rights may be over-specific.
- If a 1 percent optimization error can dominate individual prices, Vickrey pricing is unsafe.
- If bidders need to reason through many contingencies, obvious strategy-proofness may matter more than theoretical elegance.
- If exact market clearing fails, look for pseudo-equilibrium and bound the loss.
