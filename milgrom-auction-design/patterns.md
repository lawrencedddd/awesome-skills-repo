# Patterns

## Complex-Constraint Market Diagnosis

**When to use**: before designing a market for spectrum, transport, power, matching, land assembly, or cloud capacity.

**How**: identify whether the core problem is aggregate scarcity or exact assignment. List feasibility rules, heterogeneity dimensions, property-right constraints, and computational hardness. If violations cause more than ordinary rationing, add centralized feasibility enforcement.

**Trade-offs**: more design can improve feasibility and participation, but it adds administrative, legal, and software complexity.

## Substitutes-First Auction Design

**When to use**: when deciding whether prices can guide allocation.

**How**: test whether items are substitutes, complements, or mixed. If substitutes dominate, use monotone price adjustment or ascending/descending clock mechanisms. If complements dominate, expect package bidding, coordination, or central planning needs.

**Trade-offs**: substitute structure is powerful but fragile; forcing complements into a substitutes design can create bad incentives.

## Greedy Threshold Auction

**When to use**: when exact optimization is hard but a monotone greedy allocation is acceptable.

**How**: define a priority rule, run greedy selection, prove winner monotonicity, and charge winners their threshold prices.

**Trade-offs**: strategy-proof and tractable, but generally not exactly efficient.

## Pseudo-Equilibrium Pricing

**When to use**: when indivisibility prevents exact market clearing.

**How**: compute the lowest price at which demand does not exceed feasible capacity. Use that price to guide allocation and investment decisions; estimate inefficiency using unused capacity valued at the pseudo-equilibrium price.

**Trade-offs**: gives a useful price signal without exact clearing, but can still misguide investments in some cases.

## Vickrey Benchmark Check

**When to use**: when evaluating whether an ideal strategy-proof efficient auction is feasible.

**How**: ask whether bidders can report all needed values, the auctioneer can optimize exactly, counterfactual prices can be computed accurately, budgets do not bind, and bidders can understand/trust the rule.

**Trade-offs**: excellent benchmark; often poor operational default in large complex settings.

## Core Robustness Test

**When to use**: when payments from a mechanism look too generous to winners or too poor for the auctioneer.

**How**: check whether a coalition can form an alternative feasible arrangement that gives all members more. Pay special attention to complements.

**Trade-offs**: core constraints improve competitive plausibility but may conflict with dominant-strategy efficiency.

## Deferred-Acceptance Clock Auction

**When to use**: procurement with single-minded sellers and feasibility constraints, especially when bidder understanding matters.

**How**: start with high prices; lower one or more inessential bidders' prices; let bidders exit when price falls below value; freeze essential bidders; accept remaining active bidders at the end.

**Trade-offs**: obvious, feasible, private, and group-strategy-proof, but it may sacrifice exact optimality.

## Approximate-Matroid Greedy Design

**When to use**: when constraints are hard but seem close to a matroid-like substitutes structure.

**How**: build a matroid inner approximation focused on likely binding constraints. Run greedy selection on that approximation, then optionally extend greedily under the true constraints.

**Trade-offs**: tractable with performance intuition; bound quality depends on approximation relevance.

## FCC-Style Staged Reallocation

**When to use**: when a resource must be bought from incumbents and resold or repurposed for new users.

**How**: invite incumbents with high opening prices, set an ambitious clearing target, run reverse procurement, run forward sale, test revenue sufficiency, lower the target if needed, and run assignment rounds for exact details.

**Trade-offs**: handles endogenous supply and demand, but requires strong legal authority, careful software, and stakeholder education.
