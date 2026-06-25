# Chapter 5: Conclusion

## Core Idea

Prices remain valuable in complex markets, but they must often be embedded inside mechanisms and engineering constraints. Milgrom's closing argument is that approximately substitutable structures allow auctions to deliver approximately efficient allocations with better incentive and privacy properties than exact but impractical mechanisms.

## Frameworks Introduced

- **Coarse market products plus centralized dispatch**
  - When to use: when pricing every time/location/state would create too many products.
  - How: define tradable products coarsely, then let a system operator or algorithm resolve detailed feasibility.
- **Short-run/long-run price linkage**
  - When to use: when short-run allocation prices should also guide long-run capacity or investment.
  - How: test whether the auction prices that guide dispatch also give plausible investment incentives.
- **Approximate substitutes program**
  - When to use: when exact substitutes fail but local replacement relations are strong.
  - How: design auctions around monotone approximations and measure the loss.

## Key Concepts

- **Engineering dispatch**: detailed operational assignment that ensures feasibility in real time.
- **Coarse product definition**: grouping many detailed states into manageable market products.
- **Approximately efficient allocation**: allocation close enough to optimum under a measured performance guarantee.
- **Long-run investment incentive**: signal that guides capacity or technology choices before the short-run market runs.

## Mental Models

- Use **prices for direction, algorithms for detail** in power, transportation, spectrum, and other complex systems.
- Think of **product granularity as a design variable**: too coarse loses information; too fine makes markets unusable.
- Use **approximately substitutes** as the bridge between clean economic theory and real operational constraints.

## Anti-patterns

- **Pricing every operational detail**: creates too many products and prices for participants to use.
- **Separating dispatch prices from investment incentives**: may solve today's allocation while distorting tomorrow's capacity.
- **Demanding exact optimality when approximation unlocks better incentives**: exact mechanisms can be slower, less trusted, and less private.

## Worked Example

Milgrom compares textbook airport pricing with actual flight control. Charging more during congested periods may guide long-run or scheduling decisions, but flight controllers still must assign runways, gates, and safe separation. Similarly, electricity markets cannot price power second by second at every location for ordinary users; they use coarser products and centralized operators. The lesson is not to abandon prices, but to combine them with operational mechanisms that enforce constraints.

## Key Takeaways

1. Complex systems often require both market prices and centralized feasibility enforcement.
2. Coarse product definitions are practical compromises, not theoretical failures.
3. Short-run auction prices should be evaluated partly by their long-run investment signals.
4. Approximate substitutes make high-quality auction outcomes possible even when exact clearing is unavailable.

## Connects To

- **Ch 2**: supplies pseudo-equilibrium and near-substitutes.
- **Ch 4**: shows one mechanism that implements the prices-plus-feasibility approach.
- **Power and transportation markets**: likely future applications of the same design logic.
