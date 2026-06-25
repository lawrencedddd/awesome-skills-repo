# Chapter 3: Vickrey Auctions and Substitution

## Core Idea

The Vickrey auction is the benchmark mechanism for efficient, strategy-proof allocation, but its attractive properties depend on computation, bidder comprehension, budget feasibility, privacy, and substitute structure. Milgrom uses the core to identify when Vickrey payments look competitive and when they fail.

## Frameworks Introduced

- **Vickrey externality payment**
  - When to use: as a benchmark for truthful efficient allocation.
  - How: choose the allocation maximizing reported total value; charge each participant according to the loss it imposes on others.
- **Strategy-proof direct mechanism**
  - When to use: when bidders can report types or values directly.
  - How: verify that truthful reporting maximizes each bidder's payoff regardless of others' reports.
- **Uniqueness of strategy-proof payments**
  - When to use: when trying to modify payments while preserving the same allocation rule.
  - How: for broad connected type spaces and participation normalization, the payment rule is pinned down; there is little room to "tune" Vickrey-like payments.
- **Core as competitive standard**
  - When to use: to evaluate whether payoffs are vulnerable to coalition objections.
  - How: test whether any coalition could achieve more by excluding others or trading differently.
- **Bidder submodularity**
  - When to use: to know whether Vickrey payoffs are guaranteed to lie in the core.
  - How: ask whether a bidder's marginal contribution falls as the participant set grows; substitutes support this property.

## Key Concepts

- **Direct mechanism**: asks participants to report private information and computes outcomes from reports.
- **Vickrey auction**: efficient direct mechanism with externality payments and dominant truthful reporting.
- **Second-price auction**: single-item Vickrey auction where the winner pays the second-highest bid.
- **Core**: payoff set immune to blocking coalitions.
- **Bidder submodularity**: diminishing marginal contribution of a bidder as the set of other bidders grows.
- **Reporting complexity**: burden of expressing values for all relevant packages.
- **Computational complexity**: difficulty of solving the allocation and each winner's counterfactual price problem.
- **Value privacy**: bidders' desire not to reveal valuations useful in later negotiations.

## Mental Models

- Use **Vickrey as an idealized mirror**: it shows what truthful efficient allocation would require.
- Think of **core failure as overpayment risk** in procurement or under-revenue risk in sales.
- Use **complements as Vickrey stress tests**: complements can make losing bidders or coalitions able to offer better alternatives than the Vickrey payment outcome.

## Anti-patterns

- **Approximating Vickrey prices casually**: small percentage errors in large optimization values can produce huge individual price errors.
- **Ignoring package-reporting burden**: package values grow exponentially with item count unless preferences have compact structure.
- **Assuming dominant strategy survives budget constraints**: credit limits and financial constraints can destroy the clean truth-telling logic.
- **Requiring too much private value disclosure**: bidders may shade or avoid participation to protect future bargaining positions.
- **Overlooking transfer-free collusion**: losing bidders may coordinate to become profitable winners without side payments.

## Worked Example

Milgrom analyzes a procurement setting where a buyer needs items and sellers can supply them at different costs. In the Vickrey mechanism, each winning seller is paid enough that the payoff to everyone else is the same as it would be without that seller. This makes the seller internalize total surplus and report truthfully. But when two sellers provide complementary inputs, the Vickrey prices can leave the buyer with a payoff below what competitive coalition alternatives would imply. The payoff is outside the core: losing or alternative coalitions can point to a better deal. With substitutes, by contrast, bidder submodularity helps keep Vickrey payoffs in the core.

## Key Takeaways

1. Vickrey mechanisms are truthful because payments neutralize each bidder's effect on others.
2. For efficient allocation rules, strategy-proof payments are essentially unique under standard assumptions.
3. The core is the right competitive-payoff check for auction outcomes.
4. Substitutes are the condition under which Vickrey payoffs are reliably core-like.
5. Vickrey mechanisms can fail practically through reporting burden, computation, budgets, comprehension, collusion, and privacy.

## Connects To

- **Ch 2**: threshold auctions provide another strategy-proof route when allocation is monotone but not optimal.
- **Ch 4**: explains why the FCC auction could not rely on Vickrey pricing.
- **Core theory**: supplies the competitive benchmark for payoff division.
