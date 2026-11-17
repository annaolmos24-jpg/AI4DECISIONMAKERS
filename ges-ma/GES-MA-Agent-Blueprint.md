# GES M&A Advisory: Expert Roles & Agent Blueprint

Nov 17, 2026

Full agent definitions (system prompts) for all 28 roles are in [agents/](agents/README.md).

## Executive summary

A GES acquisition program needs 28 expert roles across six tiers. Eight of them are enough for a first working version. Each role is written so it can become an AI agent with one shared prompt template and one shared output format.

- **Who GES is:** Global Experience Specialists, a general services contractor for trade shows and live events. It runs exhibitor services, booth design and rental, material handling and freight, and corporate and experiential events.
- **Ownership:** Viad sold GES to the private equity firm Truelink Capital around late 2024 (confirm with GES). M&A is therefore likely a PE buy-and-build: add-ons that grow EBITDA before an exit.
- **Market:** Freeman leads, with GES, Shepard and regional decorators behind it. Revenue rests on multi-year show-organizer contracts, unionized show-floor labor and venue access.
- **The two risks most specific to this industry:** change-of-control clauses in organizer contracts, and multi-employer union pension withdrawal liability. Both have their own agent in the first version.

## How each agent is specified

Every agent uses the same prompt template. Its row in the tier tables below fills the template. That keeps outputs consistent enough for the Orchestrator and the Board Briefing Writer to combine.

**Prompt template (fill per agent):**

1. **Identity:** "You are the [Role] on GES's M&A advisory team. GES is a PE-backed trade show and live events services contractor."
2. **Mission:** the one question this agent answers about a target.
3. **Inputs:** what it reads (target profile, financials, contracts, data room files, market data).
4. **Checks:** the GES-specific items it must always test.
5. **Boundaries:** what it does not decide. Agents advise; the human deal team and investment committee decide.
6. **Output:** the shared format below.

**Shared output format (every agent, every target):**

| Field | Content |
| --- | --- |
| Rating | Green, Yellow or Red for this agent's area |
| Headline | One sentence with the key finding and its number |
| Findings | 3 to 7 bullets, each with its evidence and source |
| Value impact | Estimated effect on price or EBITDA, as a $ range |
| Deal-breakers | Anything that should stop the deal, or "None found" |
| Open questions | Data requests for the target or the data room |
| Confidence | High, Medium or Low, with the reason |

## Tier 1: Deal leadership and strategy

These five agents decide what to buy and run the process. The Orchestrator sends work to every other agent.

| # | Agent | Mission | Inputs → Outputs | GES-specific checks |
| --- | --- | --- | --- | --- |
| 1 | **M&A Orchestrator** (Head of Corp Dev) | Run each target from first look to close; route work to the other agents | Target list, agent reports → deal status, go/no-go recommendation | Keep a deal on track without disrupting the live show calendar |
| 2 | **Corporate Strategist** | Answer "why this target?" against the acquisition thesis | GES strategy, capability gaps → thesis fit score, strategic rationale | Gaps: AV and production, event tech, registration and lead retrieval, international expos, experiential agencies |
| 3 | **PE Operating Partner** | Test whether the deal raises GES's exit value | Sponsor goals, hold period, leverage → value creation plan, exit multiple impact | Fits Truelink's buy-and-build plan; add-on bought at a lower multiple than GES's expected exit multiple |
| 4 | **Live Events Industry Expert** | Give market context on any target or segment | Industry news, show calendars, trade associations → market brief, competitive position | Freeman, Shepard and regional rivals; organizers such as Informa, RX, Emerald, Clarion; IAEE, ESCA, UFI |
| 5 | **Target Sourcing Analyst** | Build and rank the universe of possible targets | Company databases, show directories, web → scored long list and short list | Regional decorators, exhibit builders, AV firms, event-tech SaaS, show logistics specialists |

## Tier 2: Financial

These five agents decide what a target is worth and how to pay for it. In events, the main traps are COVID-distorted history and revenue that moves with show rotation.

| # | Agent | Mission | Inputs → Outputs | GES-specific checks |
| --- | --- | --- | --- | --- |
| 6 | **Valuation Analyst** | Set a defensible price range | Financials, comparables, precedent deals → DCF, multiples, accretion analysis, price range | Normalize EBITDA across 2019 to 2025; use pre-COVID and post-recovery years, not 2020 to 2021 |
| 7 | **Quality of Earnings Reviewer** | Confirm the EBITDA and working capital are real | P&L, general ledger, adjustments → QoE report, adjusted EBITDA, working capital peg | Show rotation (a show changes city and size each year), customer deposits, timing of revenue recognition |
| 8 | **Contract and Revenue Analyst** | Find out how secure the revenue is | Organizer and venue contracts → contract register, renewal calendar, at-risk revenue | Change-of-control and termination clauses; exclusivity; renewal dates; revenue by top 10 shows |
| 9 | **Tax Structuring Advisor** | Pick the most tax-efficient deal structure | Entity charts, tax returns → asset vs. stock recommendation, step-up value | Cross-border structure for European, Middle East and APAC targets |
| 10 | **Debt and Financing Advisor** | Confirm the deal can be financed | GES credit agreement, sponsor terms → sources and uses, covenant headroom | Add-on limits and leverage covenants under the PE sponsor's debt |

## Tier 3: Legal, risk and regulatory

These five agents find liabilities a buyer would inherit. The Labor and Union Specialist covers this industry's largest hidden risk.

| # | Agent | Mission | Inputs → Outputs | GES-specific checks |
| --- | --- | --- | --- | --- |
| 11 | **M&A Counsel** | Protect GES in the deal documents | LOI, SPA or APA drafts, disclosure schedules → issues list, markup priorities, indemnity asks | Reps on contract assignability, labor and safety records |
| 12 | **Antitrust Advisor** | Flag competition and filing risk | Market shares by city and segment → concentration read, HSR filing need, timing risk | Few large contractors; a regional buy in a concentrated convention city may draw review |
| 13 | **Labor and Union Specialist** | Measure labor cost, labor risk and pension exposure | Collective bargaining agreements, pension fund notices → union map, withdrawal liability estimate, strike risk | Teamsters, Carpenters, IATSE locals by city; multi-employer pension withdrawal liability, which can be large and sits off the balance sheet |
| 14 | **Risk, Insurance and Safety Advisor** | Assess injury, liability and insurance exposure | Loss runs, OSHA logs, policies → risk score, insurance gaps, cost to fix | Rigging, forklifts, booth construction; workers' comp history |
| 15 | **Venue and Exclusivity Specialist** | Confirm the target can keep working where it works today | Venue agreements, permits, licenses → venue access map, at-risk venues | Convention center exclusives and approved-contractor lists; venue access is often the target's moat |

## Tier 4: Operational and commercial diligence

These six agents test whether the business works as the seller claims. Which of them a deal needs depends on the target type.

| # | Agent | Mission | Inputs → Outputs | GES-specific checks |
| --- | --- | --- | --- | --- |
| 16 | **Operations and Logistics Expert** | Assess warehouses, freight and rental assets | Site list, fleet, asset register → asset condition, utilization, capex needs | Carpet, furniture and booth inventory utilization; drayage and freight capacity; warehouse overlap with GES |
| 17 | **Customer and Commercial Analyst** | Measure customer concentration and loyalty | Customer revenue, win/loss, interviews → concentration, churn, pricing power | Two customer sets: organizers who award contracts, and exhibitors who buy services |
| 18 | **Event-Tech Diligence Expert** | Evaluate software targets | Code, architecture, product metrics → tech debt, scalability, build vs. buy view | Registration, lead retrieval, event apps, hybrid platforms; fit with GES ordering systems |
| 19 | **Creative and Agency Evaluator** | Judge creative quality and people dependence | Portfolio, awards, team roster → talent score, key-person risk, earn-out design | Experiential agency value sits in a few people; retention is the deal |
| 20 | **Cybersecurity and Privacy Reviewer** | Find data and security exposure | Security policies, breach history, data maps → risk rating, fix cost | Attendee personal data under GDPR and CCPA |
| 21 | **ESG and Sustainability Analyst** | Check sustainability claims and requirements | Waste, carbon and materials data → ESG score, organizer requirement fit | Organizers increasingly require sustainable builds; reusable booth systems are a selling point |

## Tier 5: Integration and people

These four agents protect value after signing. In events, a missed show date or a lost account manager costs more than any synergy gains.

| # | Agent | Mission | Inputs → Outputs | GES-specific checks |
| --- | --- | --- | --- | --- |
| 22 | **Integration Lead (IMO)** | Plan Day 1 and the first 100 days | Diligence findings, org charts → 100-day plan, Day-1 checklist, risk log | Integration milestones scheduled around the show calendar |
| 23 | **Synergy Analyst** | Size the synergies and track whether they are captured | Cost bases, customer overlap → synergy model, tracking dashboard | Warehouse consolidation, shared labor pools, cross-selling AV or creative into GES shows |
| 24 | **HR, Talent and Culture Advisor** | Keep the people who hold the relationships | Org chart, compensation, engagement → retention list, packages, culture gaps | Account managers own organizer relationships; when they leave, the contracts can follow |
| 25 | **IT Systems Integration Lead** | Merge systems without disrupting service | System inventory → integration roadmap, cost, cutover plan | ERP, estimating tools, and exhibitor ordering portals |

## Tier 6: Governance (meta-agents)

These three agents check and package the other agents' work. They analyze no target directly.

| # | Agent | Mission | Inputs → Outputs | GES-specific checks |
| --- | --- | --- | --- | --- |
| 26 | **Investment Committee Challenger** | Argue the case against every deal | All agent reports → counter-memo, top 5 reasons not to buy, unanswered questions | Cyclicality of events (COVID-style shocks); overpaying for one large organizer contract |
| 27 | **Board Briefing Writer** | Turn the analysis into decision documents for leadership | All reports, Challenger memo → one-page deal summary, board memo | Written for GES leadership and the PE sponsor's investment committee |
| 28 | **Deal Process Manager** | Keep the timeline and diligence requests moving | Deal plan, data room index → timeline, request tracker, overdue alerts | Diligence windows that avoid peak show season |

## Recommended first version and how it runs

Start with 8 agents: #1, #2, #4, #5, #6, #8, #13 and #26. Together they cover sourcing, strategic fit, valuation, the two risks most specific to this industry, and an independent challenge. Add the others as deals reach confirmatory diligence.

**How a target moves through the agents:**

1. **Source:** Target Sourcing Analyst (#5) builds a scored long list; Industry Expert (#4) adds market context.
2. **Screen:** Corporate Strategist (#2) scores thesis fit; low-fit targets drop out.
3. **Value:** Valuation Analyst (#6) sets a price range on the short list.
4. **Diligence:** Contract Analyst (#8) and Labor Specialist (#13) look for deal-breakers, with Tier 3 to 4 specialists added as needed.
5. **Challenge:** Investment Committee Challenger (#26) argues against the deal.
6. **Decide:** the Orchestrator (#1) combines the reports into a go/no-go for the human deal team.

**If you want fewer agents, these merge cleanly:**

| Merged agent | Combines |
| --- | --- |
| Financial Diligence | #7 Quality of Earnings + #10 Debt and Financing |
| Legal and Antitrust | #11 M&A Counsel + #12 Antitrust |
| Integration Office | #22 Integration Lead + #23 Synergy + #25 IT Integration |
| People and Talent | #19 Creative Evaluator + #24 HR and Culture |

## Assumptions to confirm with GES leadership

The industry and ownership facts above come from general knowledge, not checked sources. Confirm these before building the agents.

- [ ] Current ownership and sponsor (Truelink Capital?), hold period and exit plan
- [ ] Acquisition thesis: which capabilities, geographies or segments GES wants to add
- [ ] Deal size range and the leverage and add-on limits in GES's credit agreement
- [ ] Whether international targets are in scope
- [ ] Who sits on the investment committee, and what format it wants decisions in
- [ ] Which data sources the agents may use (CapIQ, PitchBook, internal CRM, data rooms)
