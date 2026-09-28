---
name: game-theory
description: Analyze strategic choices whose outcomes depend on other actors' responses, incentives, information, and credible commitments.
version: 0.1.0
classes: ANALYST
metadata:
  hermes:
    tags: [analysis, strategy, game-theory]
    category: research
---

# Game theory

Use when outcomes depend on how other actors respond: negotiation, competition, cooperation, coordination, incentives, or institutional rules. Follow the scope and authority in `AGENTS.md`. Do not force a strategic model onto every interaction.

## Specify the game

1. Define the decision and boundary. Identify players, decision rights, feasible actions, objectives, constraints, status quo, outside options, and material payoffs, including risk and non-monetary stakes. Separate observed behavior from inferred preferences; never invent motives from labels.
2. Map timing, move order, deadlines, chance events, and what each player can observe. Distinguish public facts, private information or types, beliefs, and common knowledge. Use `research-and-fact-check` for decisive factual inputs, `business-analysis` for money flows, and `people-and-incentives` for behavioral context.
3. Use only the formalism needed. For a static complete-information game, examine Nash best responses and profitable deviations. For sequential decisions, use backward induction and test subgame credibility. With private types, make beliefs explicit and consider Bayesian best responses; examine off-path beliefs when they change the result. Do not claim an equilibrium without checking deviations or pretend missing payoffs have been measured.
4. When several equilibria are plausible, explain selection through expectations, focal points, history, installed base, or switching costs. Keep unresolved selection visible.

## Test strategic responses

Check whether a threat or promise remains worthwhile when it must be carried out. Identify what makes a commitment credible: verification, enforceability, collateral, reputation, delegation, or sunk investment. Distinguish signaling from screening and separating from pooling behavior. Look for adverse selection before agreement and moral hazard afterward.

For bargaining, map surplus, outside options, vetoes, agenda control, and deadlines. For designed rules, test incentive compatibility and willingness to participate. In repeated interaction, examine future stakes, observability, noisy signals, retaliation, forgiveness, and reset. Consider free-riding, coalition defection, entry, exit, network effects, and rule-makers when relevant.

State the proposed move and model the strongest plausible countermove. Reassess claims of a lasting advantage once others can observe, adapt, and respond. Analysis does not authorize making threats, contacting actors, executing trades, or implementing a strategy.

## Challenge and conclude

Construct at least one materially different interpretation of the game. Vary the assumptions about payoffs and beliefs that determine the conclusion. Consider bounded rationality, norms, identity, misperception, and organizational routines. Mark missing information rather than masking it with mathematical precision.

Give the decision-relevant mechanism, likely response, assumptions, and what observation would overturn the conclusion. For predictions, specify an observable indicator, checkpoint, and update condition. Use `forecast-and-options` for probabilities and timing. Game theory alone does not predict discoveries, external shocks, exact dates, or how preferences and institutions originate. A model constructed after the outcome is an explanation, not a prior forecast.

Keep the answer proportionate. Use a payoff table or game tree only when it clarifies the decision. Distinguish calculated results from qualitative judgments and give confidence grounded in inspected evidence.
