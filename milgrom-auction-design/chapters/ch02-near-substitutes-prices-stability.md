# Chapter 2: (Near-)Substitutes, Prices, and Stability

## Core Idea

Substitutes are the structure that lets prices discover stable outcomes. Milgrom extends the logic from continuous competitive equilibrium to discrete matching, knapsack allocation, greedy algorithms, and pseudo-equilibrium prices when exact market clearing is impossible.

## Frameworks Introduced

- **Gross substitutes**
  - When to use: when evaluating whether monotone price adjustment can find stable prices.
  - How: check whether increasing one good's price weakly increases demand for other goods whose prices are unchanged.
- **Stable augmented matching**
  - When to use: when matching involves wages or contract terms.
  - How: pair a matching with wages for all worker-firm pairs; stability requires firms and workers to choose optimally at those wages and no blocking contract to exist.
- **Kelso-Crawford auction logic**
  - When to use: for labor-like matching with substitute demand.
  - How: firms raise offers to workers; workers reject worse offers; under substitutes the process approaches stable outcomes.
- **Greedy threshold auction**
  - When to use: when exact optimization is hard but a monotone greedy rule gives a good allocation.
  - How: run a monotone winner-selection rule; charge each winner the threshold bid at which it would just continue to win.
- **Pseudo-equilibrium**
  - When to use: when indivisibility prevents exact market clearing.
  - How: define the price where demand switches from exceeding capacity to not exceeding capacity, then evaluate efficiency loss by the value of unused capacity.

## Key Concepts

- **Tatonnement**: price adjustment process in which prices rise with excess demand and fall with excess supply.
- **Competitive equilibrium**: prices and allocations where agents optimize and markets clear.
- **Stable matching**: matching without unacceptable contracts or blocking worker-firm pairs.
- **Knapsack problem**: choose valuable items subject to a capacity constraint.
- **Relaxed knapsack**: divisible version of knapsack, useful as a benchmark.
- **Greedy algorithm**: process items by value/size or priority and accept each item if feasible.
- **Threshold price**: bid level at which a bidder changes from losing to winning.
- **Monotone winner selection**: if a bidder wins at one bid, improving the bid cannot make it lose.
- **Pseudo-equilibrium price**: approximate clearing price for an indivisible or hard allocation problem.

## Mental Models

- Use **substitutes as monotonicity**: price increases should move demand toward alternatives, not destabilize the whole system.
- Think of **greedy algorithms as price-compatible approximations** when exact optimization is infeasible.
- Use **empty capacity value** as a practical bound on what approximate prices may fail to capture.

## Anti-patterns

- **Assuming exact clearing prices exist**: indivisibilities can make exact supply-demand equality impossible.
- **Using greedy rules without monotonicity**: strategy-proof threshold pricing depends on monotone winner selection.
- **Confusing near-substitutes with substitutes**: approximate substitutability can support useful approximations but not all exact-equilibrium conclusions.

## Worked Example

In the knapsack example, each owner has an item with value and size, and the auctioneer wants to fit items into limited capacity. The relaxed divisible problem is solved by ordering items by value per unit of size. The discrete problem uses a greedy approximation: process items in that order and pack any item that fits. This may miss the optimum, but it is monotone: if a winning item raises its bid, it appears no later in the ordering and remains a winner. That monotonicity permits threshold payments and strategy-proof bidding. The same price-like logic can then be used to guide investments that shrink items, though pseudo-equilibrium may still be inefficient when individual investment incentives do not align with the global optimum.

## Key Takeaways

1. Gross substitutes make monotone price adjustment stable and meaningful.
2. Stable matching can be reinterpreted as equilibrium with suitable wages.
3. Greedy algorithms can support strategy-proof threshold auctions when winner selection is monotone.
4. Pseudo-equilibrium is a useful substitute for exact clearing when indivisibility blocks exact prices.
5. Approximate price signals can guide investment, but the residual inefficiency must be bounded and tested.

## Connects To

- **Ch 1**: supplies the price-discovery tools promised for complex markets.
- **Ch 3**: contrasts threshold auctions and Vickrey mechanisms as strategy-proof designs.
- **Ch 4**: uses greedy algorithms and near-substitutes for deferred-acceptance clock auctions.
