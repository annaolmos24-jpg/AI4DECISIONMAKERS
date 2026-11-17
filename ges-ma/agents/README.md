# GES M&A Advisory Agents

28 agent definitions for GES's M&A advisory team, built from the [blueprint](../GES-MA-Agent-Blueprint.md). Each file is a complete, standalone system prompt: it includes GES context, the agent's method, GES-specific checks, red flags, standard data requests, shared rules and a fixed output format.

## How to use them

- **Claude Code subagents:** copy the files into `.claude/agents/` in a project. The front matter (`name`, `description`) is already in Claude Code's subagent format.
- **Any other platform** (Claude Projects, the API, other agent frameworks): use everything below the front matter as the agent's system prompt.
- **Start with the 8-agent first version:** #1, #2, #4, #5, #6, #8, #13, #26. The M&A Orchestrator (#1) is the entry point and assigns work to the rest.

## All agents

| # | Agent | Tier | Mission |
| --- | --- | --- | --- |
| 1 | [M&A Orchestrator](01-ma-orchestrator.md) | Tier 1 | Move each target through the deal process, send the right questions to the right agents, and turn their reports into one clear recommendation for the human deal team. |
| 2 | [Corporate Strategist](02-corporate-strategist.md) | Tier 1 | Answer "why this target?" Score how well the target fills a gap in GES's strategy, and say plainly when it does not. |
| 3 | [PE Operating Partner](03-pe-operating-partner.md) | Tier 1 | Decide whether the deal makes GES worth more at exit, and what has to go right for that to happen. |
| 4 | [Live Events Industry Expert](04-live-events-industry-expert.md) | Tier 1 | Give accurate, current market context so other agents judge each target against how this industry really works. |
| 5 | [Target Sourcing Analyst](05-target-sourcing-analyst.md) | Tier 1 | Find every credible target in the segments GES cares about, and rank them so leadership spends time on the best few. |
| 6 | [Valuation Analyst](06-valuation-analyst.md) | Tier 2 | Give leadership a price range they can defend to the investment committee, and show which assumptions move it most. |
| 7 | [Quality of Earnings Reviewer](07-quality-of-earnings-reviewer.md) | Tier 2 | Find the true, repeatable EBITDA and the normal level of working capital, so GES does not pay for earnings that are not there. |
| 8 | [Contract and Revenue Analyst](08-contract-revenue-analyst.md) | Tier 2 | Find out how much of the target's revenue would survive a change of ownership, and which contracts put the deal at risk. |
| 9 | [Tax Structuring Advisor](09-tax-structuring-advisor.md) | Tier 2 | Pick the structure that keeps the most after-tax value for GES, and find tax liabilities GES would inherit. |
| 10 | [Debt and Financing Advisor](10-debt-financing-advisor.md) | Tier 2 | Show how the deal will be paid for, and confirm GES stays within its debt covenants after closing. |
| 11 | [M&A Counsel](11-ma-counsel.md) | Tier 3 | Make sure the deal documents protect GES against the risks the other agents found. |
| 12 | [Antitrust Advisor](12-antitrust-advisor.md) | Tier 3 | Tell leadership early whether a deal could be blocked or delayed on competition grounds, and what filings it needs. |
| 13 | [Labor and Union Specialist](13-labor-union-specialist.md) | Tier 3 | Find and size every labor obligation GES would inherit, starting with multi-employer pension withdrawal liability. |
| 14 | [Risk, Insurance and Safety Advisor](14-risk-insurance-safety-advisor.md) | Tier 3 | Measure the target's safety record and insurance coverage, and the cost to bring both up to GES standards. |
| 15 | [Venue and Exclusivity Specialist](15-venue-exclusivity-specialist.md) | Tier 3 | Confirm that the target's venue access, often its real competitive advantage, survives the sale. |
| 16 | [Operations and Logistics Expert](16-operations-logistics-expert.md) | Tier 4 | Judge the condition, capacity and real cost of the target's operating assets, and how well they fit GES's network. |
| 17 | [Customer and Commercial Analyst](17-customer-commercial-analyst.md) | Tier 4 | Find out whether customers will stay, pay more and buy more from the combined company. |
| 18 | [Event-Tech Diligence Expert](18-event-tech-diligence-expert.md) | Tier 4 | Judge whether the target's technology is sound, scalable and worth buying instead of building. |
| 19 | [Creative and Agency Evaluator](19-creative-agency-evaluator.md) | Tier 4 | Decide whether the target's creative value will survive the deal, given that it lives in a few people. |
| 20 | [Cybersecurity and Privacy Reviewer](20-cybersecurity-privacy-reviewer.md) | Tier 4 | Find the security and privacy risks GES would inherit, and the cost to fix them. |
| 21 | [ESG and Sustainability Analyst](21-esg-sustainability-analyst.md) | Tier 4 | Find out whether the target helps or hurts GES with organizers and investors that require sustainable events. |
| 22 | [Integration Lead (IMO)](22-integration-lead.md) | Tier 5 | Make the integration work on Day 1 and deliver the deal's planned outcomes, without disrupting a single show. |
| 23 | [Synergy Analyst](23-synergy-analyst.md) | Tier 5 | Put a realistic number and timeline on every synergy, and track it until it is delivered. |
| 24 | [HR, Talent and Culture Advisor](24-hr-talent-culture-advisor.md) | Tier 5 | Keep the people the deal depends on, and bring the two teams together without losing performance. |
| 25 | [IT Systems Integration Lead](25-it-systems-integration-lead.md) | Tier 5 | Combine the systems on a timeline that never breaks exhibitor ordering or show operations. |
| 26 | [Investment Committee Challenger](26-investment-committee-challenger.md) | Tier 6 | Find the strongest reasons not to do this deal, so leadership decides with the downside in full view. |
| 27 | [Board Briefing Writer](27-board-briefing-writer.md) | Tier 6 | Give busy executives the decision, the reasons and the risks on one page they can read in three minutes. |
| 28 | [Deal Process Manager](28-deal-process-manager.md) | Tier 6 | Keep every deal on schedule and make sure no diligence request falls through the cracks. |

## Before you use them with real deals

The GES ownership and industry facts in each prompt come from general knowledge and should be confirmed with GES leadership. See "Assumptions to confirm" in the blueprint. Agents advise; the human deal team decides.
