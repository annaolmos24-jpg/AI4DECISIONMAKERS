# AI4DECISIONMAKERS

AI advisory material for senior leadership: expert roles, decision frameworks and ready-to-use AI agents that support executive decisions.

## Projects

### GES M&A Advisory

An AI advisory team to support GES (Global Experience Specialists) leadership on mergers and acquisitions in the trade show and live events industry.

| File | What it is |
| --- | --- |
| [GES-MA-Agent-Blueprint.md](ges-ma/GES-MA-Agent-Blueprint.md) | The 28 expert roles a GES acquisition program needs, in six tiers, with a recommended 8-agent first version |
| [agents/](ges-ma/agents/README.md) | Full system prompts for all 28 agents, one file each, with an index |

**The six tiers:**

1. **Deal leadership and strategy:** Orchestrator, Corporate Strategist, PE Operating Partner, Industry Expert, Target Sourcing
2. **Financial:** Valuation, Quality of Earnings, Contracts and Revenue, Tax, Debt and Financing
3. **Legal, risk and regulatory:** M&A Counsel, Antitrust, Labor and Union, Risk and Safety, Venue and Exclusivity
4. **Operational and commercial diligence:** Operations and Logistics, Customer, Event Tech, Creative Agency, Cybersecurity, ESG
5. **Integration and people:** Integration Lead, Synergy, HR and Talent, IT Systems
6. **Governance:** Investment Committee Challenger, Board Briefing Writer, Deal Process Manager

**Quick start**

1. Read the [blueprint](ges-ma/GES-MA-Agent-Blueprint.md) and confirm the assumptions listed at its end with GES leadership.
2. Start with the 8-agent first version: #1 Orchestrator, #2 Strategist, #4 Industry Expert, #5 Sourcing, #6 Valuation, #8 Contracts, #13 Labor and Union, #26 Challenger.
3. To run them as Claude Code subagents, copy the files from `ges-ma/agents/` into a project's `.claude/agents/` folder. On other platforms, use each file's text below the front matter as the agent's system prompt.
4. Give every request to the M&A Orchestrator (#1); it assigns work to the other agents and returns a combined go/no-go recommendation.

**Important:** the agents advise and the human deal team decides. Industry and ownership facts in the prompts come from general knowledge and must be confirmed before use on real deals. Keep all target and deal information confidential.

## Repository layout

```
README.md                       this file
ges-ma/
  GES-MA-Agent-Blueprint.md     roles, tiers, first version, assumptions
  agents/
    README.md                   index of all 28 agents
    01-ma-orchestrator.md
    ...
    28-deal-process-manager.md
```
