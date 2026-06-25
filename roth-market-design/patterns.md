# Patterns

## Thickness-Congestion-Safety Diagnosis
**When to use**: A marketplace produces poor matches, strategic behavior, or low participation.
**How**: Check whether enough participants gather together, whether they can process options, and whether honest participation is safe.
**Trade-offs**: Improving one dimension can strain another; more thickness can create congestion, and more speed can reduce safety.

## Standardize to Commodify
**When to use**: Participants spend too much effort inspecting heterogeneous goods or counterparties.
**How**: Define grades, quality categories, inspection standards, and settlement rules so more trades can clear by price.
**Trade-offs**: Standardization can erase valuable differences and create disputes over grading.

## Build a Clearinghouse
**When to use**: Decentralized offers unravel, explode, or produce unstable matches.
**How**: Collect preferences, synchronize timing, run a transparent matching mechanism, and make outcomes credible.
**Trade-offs**: Centralization requires trust, governance, and careful adaptation to special constraints.

## Use Deferred Acceptance
**When to use**: Two-sided matching has ranked preferences, capacities, and risk of strategic misrepresentation.
**How**: Let the protected side propose in preference order; receivers hold best current proposals; rejected proposers continue until the process stops.
**Trade-offs**: The proposing side is favored; priorities and constraints must be explicit.

## Pool to Create Compatibility
**When to use**: Useful matches are rare, as in kidney exchange or niche labor markets.
**How**: Combine local pools, share standardized data, and search for cycles or chains across a larger graph.
**Trade-offs**: Larger pools raise governance, privacy, logistics, and trust demands.

## Enforce a Common Market Start
**When to use**: Participants rush early and thin the market.
**How**: Establish shared dates, prohibit or discourage early offers, and make waiting safe.
**Trade-offs**: Rules require monitoring and must account for legitimate early information needs.

## Replace Exploding Offers with Coordinated Deadlines
**When to use**: Participants are pressured into premature commitments.
**How**: Set minimum response windows, common decision dates, or clearinghouse rules.
**Trade-offs**: Slower decisions can create uncertainty if the market lacks fallback mechanisms.

## Batch to Reduce Wasteful Speed Races
**When to use**: Tiny speed differences dominate allocation without improving social value.
**How**: Collect orders or claims over brief intervals and clear them together.
**Trade-offs**: Batching sacrifices some immediacy and must be tuned to the market's information flow.

## Add Trust Infrastructure
**When to use**: Participants fear fraud, non-delivery, low quality, no-shows, or exploitation.
**How**: Use reputation, escrow, verification, guarantees, deposits, dispute resolution, or licensing.
**Trade-offs**: Trust mechanisms can raise entry barriers and may be gamed.

## Reduce Strategy Burden
**When to use**: Sophisticated participants outperform because they understand the rules better.
**How**: Choose mechanisms where truthful preferences are safe; communicate rules plainly; audit outcomes for unequal strategic burden.
**Trade-offs**: Strategy-proofness for one side may not protect every side equally.

## Introduce Scarce Signals
**When to use**: Receivers face too many cheap messages or applications.
**How**: Give senders a limited number of signals and define what they mean.
**Trade-offs**: Signals can become a new game if too many, too few, or too ambiguous.

## Design Around Repugnance
**When to use**: A desired transaction is morally or legally blocked.
**How**: Identify the repugnant element, then explore exchange, queue, priority, reimbursement, or donation-compatible designs.
**Trade-offs**: Alternative designs may be less efficient than cash markets but more legitimate and feasible.

## Observe Markets as Field Sites
**When to use**: Applying Roth's ideas to a new domain.
**How**: Identify participants, scarcity, timing, information, rules, trust mechanisms, failure modes, and social constraints.
**Trade-offs**: Field observation gives practical insight but may miss formal incentive properties.
