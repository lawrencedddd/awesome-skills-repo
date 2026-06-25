# Chapter 4: Deferred-Acceptance Auctions and Near-Substitutes

## Core Idea

When Vickrey optimization and pricing are infeasible, a deferred-acceptance clock auction can trade exact optimality for feasibility, transparency, strategy-proofness, group resistance, and privacy. The mechanism works especially well when hard constraints are close to matroid-like substitute structure.

## Frameworks Introduced

- **Obvious strategy-proofness**
  - When to use: when participant trust and comprehension are central.
  - How: at every decision node, compare the worst payoff from the truthful action with the best payoff from deviating. If truth is visibly safe, the mechanism avoids contingent reasoning.
- **Deferred-acceptance clock auction**
  - When to use: procurement-like settings with single-minded sellers and complex feasibility constraints.
  - How: prices descend; bidders exit when price falls below value; acceptance is deferred; winners are active bidders at termination.
- **Essential bidder test**
  - When to use: to preserve feasibility during a descending reverse auction.
  - How: before reducing a bidder's price, check whether losing that bidder would make the target infeasible. If yes, freeze that bidder as essential.
- **Greedy rejection algorithm**
  - When to use: when rejecting high-cost or low-priority bidders while maintaining feasibility.
  - How: process candidates in priority order; reject if feasible; otherwise keep them.
- **Substitutability index**
  - When to use: to evaluate how close a hard constraint system is to a matroid.
  - How: find a matroid inner approximation and measure the worst-case quality of feasible-set approximation; this also bounds greedy performance.

## Key Concepts

- **Single-minded bidder**: bidder with one main sell/not-sell decision.
- **Clock price**: displayed price that changes over auction rounds.
- **Active bidder**: bidder that has not exited.
- **Essential bidder**: bidder whose exit would make the allocation infeasible.
- **Group strategy-proofness**: no group can jointly deviate so all members strictly gain, within the mechanism.
- **Unconditional privacy**: winners reveal only enough information to prove they should win.
- **Matroid**: feasibility structure for which greedy algorithms solve weighted selection exactly.
- **Approximate matroid**: inner approximation of a hard feasible set by a matroid-like structure.

## Mental Models

- Use **dynamic simplicity over sealed-bid elegance** when participants cannot verify complex direct-mechanism logic.
- Think of **deferred acceptance as "do not commit until feasibility is known"**.
- Use **matroid closeness** as a reason a greedy auction may be good enough even when exact optimization is impossible.

## Anti-patterns

- **Using Vickrey with approximate optimizers**: a 1 percent allocation-value error can imply massive individual price errors in large markets.
- **Accepting bidders too early**: premature commitment can make later feasibility impossible.
- **Reducing prices for essential bidders**: risks losing the participants needed to satisfy the clearing target.
- **Treating all constraints as equally relevant**: approximation should focus on constraints likely to bind.

## Worked Example

In the FCC reverse auction, the auctioneer wanted to buy enough broadcast rights to clear spectrum while ensuring remaining stations could still be assigned channels. A descending clock auction offered each station a price. A station stayed active while the price was acceptable and exited when it was not. The system checked feasibility before allowing a station to exit: if losing that station would make the clearing target impossible, its price stopped falling and it became a winner. This made truthful exit behavior easy to understand, preserved feasibility by construction, and avoided the impossible task of computing exact Vickrey prices across millions of interference constraints.

## Key Takeaways

1. Vickrey pricing can be unusable when exact optimization cannot be verified.
2. Obvious strategy-proofness matters because real bidders must trust and understand the rule.
3. Deferred-acceptance clock auctions give bidders a simple stay/exit decision.
4. One-bidder-at-a-time price decrements plus essential-bidder checks preserve feasibility.
5. Approximate matroids explain why greedy designs can perform well under near-substitutes.

## Connects To

- **Ch 1**: applies the complex-constraint diagnosis to the FCC auction.
- **Ch 2**: relies on monotone greedy algorithms and near-substitute reasoning.
- **Ch 3**: responds to Vickrey's computational, privacy, and comprehension failures.
