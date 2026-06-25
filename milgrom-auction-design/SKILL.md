---
name: milgrom-auction-design
description: "Knowledge base from \"Discovering Prices: Auction Design in Markets with Complex Constraints\" by Paul Milgrom. Use when applying Milgrom's frameworks for auction design, price discovery, substitutes and complements, Vickrey mechanisms, deferred-acceptance clock auctions, and markets with complex constraints."
---

<!-- argument-hint: [topic, framework name, or chapter number] -->

# Discovering Prices: Auction Design in Markets with Complex Constraints
**Author**: Paul Milgrom | **Pages**: ebook source | **Chapters**: 5 + appendix | **Generated**: 2026-06-25

## How to Use This Skill

- **Without arguments** - load the core frameworks for market and auction design.
- **With a topic** - ask about `gross substitutes`, `Vickrey`, `deferred acceptance`, `FCC incentive auction`, `pseudo-equilibrium`, or another indexed concept.
- **With chapter** - ask for `ch02`, `ch04`, etc.; I load the relevant chapter file.
- **For design work** - ask whether a market should use prices alone, a Vickrey-style mechanism, a clock auction, or an approximation algorithm.

When a question depends on chapter detail, I will read the relevant chapter file before answering.

---

## Core Frameworks & Mental Models

### Complexity as the reason markets need design

Use market design when the problem is not merely "how much of a homogeneous good should be supplied," but "which exact units can be assigned to whom under constraints." Prices alone work best for simple resource constraints; they need mechanism support when temporary imbalance is unsafe, infeasible, legally impossible, or computationally hard.

Design test:

1. Are units meaningfully heterogeneous by place, time, quality, adjacency, or compatibility?
2. Do feasibility constraints involve combinations rather than totals?
3. Would a temporary excess-demand state create a serious harm, not just rationing?
4. Are property rights incomplete, unclear, or politically constrained?
5. Is finding the optimal allocation computationally hard?

If several answers are yes, the designer should not rely on decentralized bargaining or a single posted price.

### Substitutes are the friendly case

Use the substitutes lens when raising the price of one item makes other items weakly more attractive. In Milgrom's account, substitutes are not just an economic intuition; they are the condition under which monotone price adjustment and monotone algorithms behave well.

When goods are gross substitutes, ascending auctions can move prices upward toward market-clearing outcomes. In discrete matching models, substitute demand supports stable matchings and auction-like wage adjustments. In Vickrey settings, substitutes help ensure that Vickrey payoffs lie in the core, so payments look competitive rather than excessive.

### Complements are the danger case

Use the complements warning when value depends on acquiring items together: paired inputs, adjacent spectrum blocks, matched takeoff and landing slots, national clearing of local stations, or multi-party land assemblies. Complements make decentralized bargaining slow, Vickrey payoffs fragile, and price-only guidance unreliable.

Practical smell: if one participant's item has little value unless several others also participate, expect coordination failure, holdup, unstable prices, or collusion opportunities.

### Prices as guides, not as complete allocations

Milgrom's central move is to keep prices even when prices cannot do the whole job. In complex systems, prices may guide substitution, investment, and participation while a centralized algorithm enforces feasibility details. This is the bridge between economic markets and engineering dispatch systems.

Use coarse prices when fine-grained products would explode in number. Then use rules, algorithms, or system operators to fill in the operational details that prices cannot express.

### Pseudo-equilibrium for approximate clearing

Use pseudo-equilibrium when exact market-clearing prices do not exist because goods are indivisible or constraints are complex. A pseudo-equilibrium price is the threshold-like price at which demand changes from exceeding feasible capacity to not exceeding it. It can guide investment and short-run allocation, but the value of unused capacity becomes the bound on efficiency loss.

Decision rule: if exact clearing is impossible, ask whether the price still gives decision makers approximately correct marginal signals for investment and participation.

### Vickrey auction as benchmark, not default

Use the Vickrey auction as a theoretical benchmark for efficiency and strategy-proofness. It selects the value-maximizing allocation and charges each participant for the externality imposed on others. Truth-telling is dominant because the payment rule makes each bidder internalize total surplus.

Do not default to Vickrey when:

- bidders must report too many package values;
- optimization is NP-hard or only approximate;
- computing each winner's price requires many additional hard optimizations;
- bidders face budget or credit constraints;
- participants will not understand or trust the payment logic;
- value privacy matters;
- losing bidders can collude profitably without transfers;
- complements make Vickrey payoffs fall outside the core.

### The core as the competitive-payoff standard

Use the core to ask whether auction payoffs are competitively defensible. A payoff vector is in the core when no coalition can improve on it by forming a different feasible arrangement. If a Vickrey outcome is outside the core, the usual symptom is that the auctioneer pays too much or receives too little relative to competitive alternatives.

Rule of thumb: when complements are important, check core risk before trusting Vickrey payments.

### Greedy algorithms as market mechanisms

Use greedy algorithms when exact optimization is infeasible but the feasible set is substitutable or approximately substitutable. A monotone winner-selection rule supports threshold payments: if a bidder would win at one bid, it still wins after improving its bid. This monotonicity gives strategy-proofness.

Milgrom links three monotonicities:

- economic monotonicity: substitutes make demand move in the helpful direction;
- algorithmic monotonicity: greedy choices proceed without reversals;
- auction monotonicity: clock prices move one way, making incentives simple.

### Deferred-acceptance clock auctions

Use a deferred-acceptance clock auction for single-minded sellers under complex feasibility constraints, especially when the auctioneer must buy enough rights while preserving feasibility for those who remain. Prices descend. Bidders stay active while the offered price is at least their value and exit otherwise. Acceptance is deferred until the end.

This mechanism is attractive because it is:

- obviously strategy-proof: bidders can see that the simple stay/exit rule is best;
- group strategy-proof against transfer-free joint deviations;
- privacy preserving for winners;
- compatible with greedy rejection algorithms;
- feasible by construction when price reductions are allowed only for inessential bidders.

### Approximate matroids and the substitutability index

Use the approximate-matroid idea when a hard feasibility system behaves nearly like a matroid over the relevant region. Matroids are the clean case where greedy algorithms are optimal. The substitutability index measures how well a matroid inner approximation captures the feasible sets and also bounds the worst-case payoff ratio of the greedy solution.

Design implication: do not ask only "is this exactly a substitutes problem?" Ask whether the relevant constraints are close enough to a substitutable structure that a greedy, monotone auction can achieve high value with much better incentives and transparency.

### FCC incentive auction design logic

Use the FCC auction as a template for complex public-resource reallocation:

- clarify property rights without giving each owner a veto over system-wide reorganization;
- use a reverse auction to buy incumbent rights and a forward auction to sell repurposed rights;
- set a clearing target, then reduce it if revenue cannot cover costs;
- use feasibility checks for interference constraints;
- use descending prices for sellers and ascending clock prices for buyers;
- use assignment rounds after product winners are known to resolve detailed frequency preferences;
- let mechanism design, optimization, and policy constraints work together.

---

## Chapter Index

| # | Title | Key Frameworks |
|---|-------|----------------|
| [ch01](chapters/ch01-complex-market-design.md) | Introduction: Why Complex Markets Need Design | complex constraints, Coase limits, substitutes/complements, FCC problem |
| [ch02](chapters/ch02-near-substitutes-prices-stability.md) | (Near-)Substitutes, Prices, and Stability | gross substitutes, stable matching, greedy threshold auctions, pseudo-equilibrium |
| [ch03](chapters/ch03-vickrey-auctions-substitution.md) | Vickrey Auctions and Substitution | strategy-proofness, Vickrey payments, core, bidder submodularity, Vickrey limits |
| [ch04](chapters/ch04-deferred-acceptance-near-substitutes.md) | Deferred-Acceptance Auctions and Near-Substitutes | obvious strategy-proofness, clock auctions, greedy rejection, substitutability index |
| [ch05](chapters/ch05-conclusion.md) | Conclusion | prices plus engineering constraints, approximate substitutes, future applications |
| [ch06](chapters/ch06-fcc-incentive-auction-rules.md) | Appendix: FCC Incentive Auction Rules | opening prices, clearing targets, reverse/forward auctions, final-stage rule, assignment rounds |

## Topic Index

- **Activity rule** -> ch06
- **Approximate matroids** -> ch04
- **Assignment constraints** -> ch01, ch02, ch06
- **Assignment rounds** -> ch06
- **Clock auction** -> ch04, ch06
- **Coase theorem limits** -> ch01
- **Complements** -> ch01, ch03
- **Conditional reserve** -> ch06
- **Core** -> ch03
- **Deferred-acceptance clock auction** -> ch04
- **FCC broadcast incentive auction** -> ch01, ch04, ch06
- **Final-stage rule** -> ch06
- **Graph coloring / NP-completeness** -> ch01, ch04
- **Greedy algorithm** -> ch02, ch04
- **Gross substitutes** -> ch02, ch03
- **Intra-round bidding** -> ch06
- **Knapsack problem** -> ch02
- **Market-clearing prices** -> ch01, ch02, ch05
- **Obvious strategy-proofness** -> ch04
- **Pseudo-equilibrium** -> ch02
- **Substitutability index** -> ch04
- **Threshold auction** -> ch02
- **Vickrey auction** -> ch03, ch04
- **Winner-selection monotonicity** -> ch02, ch04

## Supporting Files

- [glossary.md](glossary.md) - key terms and definitions
- [patterns.md](patterns.md) - mechanisms, algorithms, and design patterns
- [cheatsheet.md](cheatsheet.md) - decision rules and quick comparisons

---

## Scope & Limits

This skill covers the book's concepts and mechanisms. It does not replace legal, regulatory, engineering, or auction-software expertise for live market design. For implementation in a specific codebase or policy setting, combine this skill with domain data, feasibility solvers, simulation, and stakeholder constraints.
