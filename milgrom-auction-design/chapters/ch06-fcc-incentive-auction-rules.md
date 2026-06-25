# Appendix: A Report on the FCC Incentive Auction

## Core Idea

The appendix describes the practical machinery of the FCC incentive auction: initial commitments, clearing targets, reverse-auction bidding, forward-auction bidding, final-stage rules, an extended round, and assignment rounds. It is the operational companion to the book's theory.

## Frameworks Introduced

- **Opening-price participation strategy**
  - When to use: when seller participation is uncertain and early participation is valuable.
  - How: set generous opening prices using value and difficulty indices, then let competition reduce prices.
- **Clearing-target staging**
  - When to use: when supply acquisition cost and buyer demand are jointly uncertain.
  - How: start with an ambitious target; if forward-auction revenue cannot cover reverse-auction cost, lower the target and run another stage.
- **Reverse auction for incumbents**
  - When to use: when the auctioneer buys rights from current holders.
  - How: prices descend while sellers are inessential; freeze prices when a seller is needed for feasibility.
- **Forward clock auction for new users**
  - When to use: when buyers compete for newly created licenses.
  - How: raise prices on products with excess demand while enforcing activity and demand-reduction rules.
- **Assignment rounds**
  - When to use: after generic product winners are known but exact frequencies or locations still matter.
  - How: let winners bid for preferred detailed assignments consistent with the main allocation.

## Key Concepts

- **Initial commitment**: binding broadcaster decision to participate under opening-price options.
- **UHF / VHF / HVHF / LVHF**: broadcast bands and options relevant to relinquishing or moving rights.
- **Clearing target**: amount of spectrum to repurpose from broadcast to mobile broadband.
- **Impairment**: reduction in broadband license usability due to remaining broadcast interference.
- **Partial Economic Area (PEA)**: geographic license unit in the forward auction.
- **Category 1 / Category 2 license**: license categories based on impairment level.
- **Activity rule**: restriction preventing bidders from increasing overall activity later.
- **Conditional reserve**: rule reserving some licenses for qualified bidders after revenue conditions are met.
- **Intra-round bidding**: allowing demand reductions at prices inside a round's price interval.
- **Final-stage rule**: test that forward-auction revenue covers reverse-auction costs and other thresholds.
- **Extended round**: additional clock round allowing limited price increases to close a revenue gap.

## Mental Models

- Use **staging** when market-clearing quantity is endogenous.
- Think of **generic products first, exact assignments later** when detailed preferences matter but would overload the main auction.
- Use **opening prices to invite participation** and later rounds to discipline cost.

## Anti-patterns

- **Setting the initial target too narrowly**: may leave valuable spectrum uncleared before discovering actual supply.
- **Treating all licenses as identical**: ignores impairment, geography, adjacency, and harmonics.
- **Skipping assignment rounds**: leaves value on the table when winners care about exact frequencies.
- **Letting revenue shortfalls linger**: the final-stage rule forces an explicit target reduction or closing path.

## Worked Example

The auction began with broadcasters making binding initial commitments. The FCC computed the maximum feasible clearing target from those commitments, initially 126 MHz of broadcast spectrum, corresponding to 100 MHz of mobile broadband after guard bands and other adjustments. The reverse auction then bought broadcast rights through descending prices. The forward auction sold broadband licenses through ascending clock prices. If buyer revenue was insufficient to cover seller costs, the clearing target was reduced and another stage began. Once the final-stage rule was satisfied, assignment rounds determined exact frequency assignments for wireless winners and post-auction channel assignments for remaining broadcasters.

## Key Takeaways

1. The FCC design separated participation, clearing quantity, reverse procurement, forward sale, and detailed assignment.
2. Opening prices were deliberately generous to attract sellers, while later competition reduced costs.
3. The clearing target was endogenous and adjusted when revenue did not cover costs.
4. Assignment rounds solved detailed preferences after the main market determined winners.

## Connects To

- **Ch 1**: supplies the policy and complexity context.
- **Ch 4**: explains the deferred-acceptance logic behind the reverse auction.
- **Spectrum auctions**: provides a concrete implementation pattern for other constrained reallocation markets.
