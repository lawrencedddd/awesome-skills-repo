# Chapter 1: Introduction

## Core Idea

Market design becomes necessary when decentralized bargaining and prices alone cannot resolve complex allocation constraints. Milgrom frames auction design as a way to discover prices and guide resource allocation when goods are heterogeneous, constraints are combinatorial, and feasibility itself may be computationally hard.

## Frameworks Introduced

- **Complex constraints**
  - When to use: use this label when feasibility depends on combinations, timing, adjacency, interference, compatibility, or assignment details.
  - How: identify the constraint that cannot be reduced to total quantity; ask whether violating it causes rationing, waste, legal conflict, or physical harm.
- **Coase theorem boundary test**
  - When to use: when someone argues that private bargaining should solve the allocation problem.
  - How: check secure property rights, transferability, low transaction costs, effective bargaining, and multi-party coordination. If these fail, design may create value.
- **Substitutes/complements diagnostic**
  - When to use: before choosing a pricing or auction format.
  - How: ask whether losing one item makes alternatives more attractive (substitutes) or makes other items less useful (complements).
- **Prices-plus-coordination**
  - When to use: when prices can guide choices but cannot guarantee feasibility.
  - How: use prices for participation and substitution, and use centralized rules or algorithms for feasibility details.

## Key Concepts

- **Market design**: deliberate construction of market rules so decentralized participants can reach useful outcomes.
- **Complex resource constraint**: a feasibility rule about combinations or assignments, not just total supply.
- **Heterogeneous goods**: goods that cannot be treated as identical because location, timing, adjacency, or quality matters.
- **Externality**: an effect of one participant's action on others that is not fully priced.
- **Imperfect competition**: a market condition in which some participants can influence prices or terms.
- **Graph coloring**: assigning colors to nodes so connected nodes differ; used as an analogy for TV channel assignment.
- **NP-completeness**: computational hardness class relevant to checking some feasible assignments.
- **Forward auction**: an auction in which the FCC sells spectrum licenses to new users.
- **Reverse auction**: an auction in which the FCC buys rights from existing users.

## Mental Models

- Use **complexity as a design trigger** when the market needs to decide which exact units go where, not just how many units trade.
- Think of **property rights as design inputs**, not natural givens. Good rights protect legitimate interests without giving each owner a veto over system-wide gains.
- Use **substitutes as price-friendly structure** and **complements as coordination-risk structure**.

## Anti-patterns

- **Treating all products as homogeneous**: hides the actual assignment problem and makes price recommendations too coarse.
- **Assuming Coasian bargaining scales**: multi-party assemblies can remain inefficient for decades even when gains from trade are large.
- **Letting each incumbent hold a veto**: creates holdout power and may prevent efficient reallocation.
- **Ignoring bidder comprehension**: complex rules can suppress participation even when the mechanism is theoretically attractive.

## Worked Example

The chapter uses the FCC broadcast incentive auction as the main design example. Broadcast rights had to be cleared so mobile broadband providers could use valuable spectrum, but remaining broadcasters still needed feasible channels with limited interference. A simple price per MHz could not determine which stations should move, because each station's feasibility depended on many other channel assignments. Congress shaped property rights so broadcasters were protected in coverage terms but not guaranteed their old channels. The auction then used prices and feasibility checks together: sellers faced a reverse auction, buyers faced a forward auction, and the system adjusted clearing targets when buyer revenue could not cover seller costs.

## Key Takeaways

1. Markets need design when the hard part is not price level but feasible coordination.
2. Substitutes make price guidance powerful; complements make coordination difficult.
3. Property-right design can preserve legitimate claims without creating holdouts.
4. Computational complexity is an economic design constraint, not just an engineering inconvenience.

## Connects To

- **Ch 2**: formalizes substitutes and near-substitutes as conditions under which prices and monotone auctions work.
- **Ch 4**: returns to FCC constraints and explains why deferred-acceptance clock auctions fit the problem.
- **Coase theorem**: supplies the baseline argument that Milgrom challenges for complex markets.
