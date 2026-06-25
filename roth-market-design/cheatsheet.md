# Market Design Cheatsheet

## Core Diagnostic

| Question | If yes | Design move |
|---|---|---|
| Does price alone allocate the resource? | No | Treat it as a matching market |
| Are enough participants present together? | No | Build thickness with pooling, timing, or platform adoption |
| Are participants overwhelmed or delayed? | Yes | Reduce congestion with filters, speed, batching, or signals |
| Can people safely state true preferences? | No | Redesign incentives; consider deferred acceptance or clearer rules |
| Are transactions moving too early? | Yes | Add common start dates, coordinated deadlines, or a clearinghouse |
| Is tiny speed advantage dominating outcomes? | Yes | Consider batching or priority-rule changes |
| Is the transaction socially contested? | Yes | Run a repugnance audit before proposing a price market |

## Decision Rules

- When both sides must choose each other, model the problem as matching before pricing.
- When participants rush early, ask what makes waiting unsafe.
- When a market is thick but ineffective, look for congestion in attention, evaluation, response, or commitment.
- When ordinary participants must game the rules, treat that as a design failure.
- When communication becomes cheap, make meaningful signals scarce or costly.
- When cash is repugnant, separate the matching problem from the payment problem.
- When a market seems "free" but chaotic, inspect the missing rules.

## Mechanism Choices

| Situation | Prefer | Because |
|---|---|---|
| School choice with family rankings and public priorities | Student-proposing deferred acceptance | Families can rank more truthfully while priorities remain explicit |
| Residency-style labor market with early offers | Clearinghouse | Synchronizes timing and reduces unraveling |
| Organ exchange without cash sales | Compatibility exchange / chains | Respects legal and moral constraints while increasing transplants |
| Too many cheap applications | Limited signals | Helps receivers distinguish serious interest |
| Continuous electronic race for priority | Frequent batch clearing | Reduces wasteful latency competition |
| Heterogeneous goods that can be reliably graded | Commodity standards | Lets price and anonymous trading do more work |

## Failure Smells

| Smell | Likely failure |
|---|---|
| Participants accept before they know their options | Unraveling / exploding offers |
| Many participants but few transactions | Congestion |
| Users ask experts how to rank preferences strategically | Unsafe mechanism |
| The fastest participant wins without adding value | Wasteful speed race |
| Receivers ignore most messages | Cheap-talk overload |
| Legal design looks efficient but politically impossible | Repugnance ignored |
| Multiple acceptances coexist with unassigned participants | Poor coordination / missing clearinghouse |

## Roth-Style Design Sequence

1. Define what is scarce and who must choose whom.
2. Map existing rules, timing, information, and trust mechanisms.
3. Diagnose thickness, congestion, and safety.
4. Identify strategic behavior the current rules reward.
5. Choose the smallest rule change that makes honest, timely participation safer.
6. Test the design against logistics, law, legitimacy, and communication burden.
7. Monitor how participants adapt; redesign is often iterative.
