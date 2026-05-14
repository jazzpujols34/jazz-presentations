# Sol Lee Round — Friday Speaker Notes (v2)

Round 1 (Frank + Kanwartej) is done. Friday is **Cheng-Han "Sol" Lee** — Architect at Microsoft, 9+ years tenure. This is the **technical peer-evaluation gate**. Frank already runs the management decision; Sol's job is to confirm you can hold up technically in a customer room.

If Sol gives thumbs up, you're in.

---

## What round 1 told us (read this first)

The conversation with Frank revealed the practice shape clearly. Internalize these:

**Practice structure:**
- It's the **Modern Work practice inside AIBS**
- Currently **zero people in Taiwan** for this practice (greenfield)
- Plan: expand to **5 people** — consultant + architect, Azure-focused
- You'd **report to Frank** directly
- **July timeframe** — real urgency, Q3 staffing
- Not isolated — there's a big support unit in TW you'd lean on

**Practice mission (Frank's framing):**
- Consulting, **not outsourcing**, **not support**
- Focus on **designing, architecting, project lifecycle**
- **Drive outcomes**, then **hand over to clients**

**The three success measures (Frank named them explicitly):**

1. **Utilization (the hard number):** 70% billable = **32 hrs / week chargeable** out of 40
2. **Pipeline (the soft number):** Bring in new work / new contracts ($500M was the regional aggregate)
3. **Performance review:** **ACR (Azure Consumption Revenue), MAU, Copilot seats** — how much consumption you help customers commit to, how many Copilot licenses you drive

**Data residency note (Frank flagged this):**

Taiwan customer data — especially **government, financial, sensitive verticals** — must stay outside China-region clouds. Reference: "GCR, before, customer info, gov, sensitive, keep it separate from china."

**Scenario interview format (they used it on you):**

The example: *"Design a document-sharing capability for scientist customers working on new medicine policy."* Pattern: design X for industry Y with constraint Z.

**Workflow reality (Frank described it):**
- **3–4 projects per day** juggle
- You **own your set of customers**
- AU comparison: 17 consultants in Australia, looking at +4
- **Individually operated** — high autonomy expected

---

## Sol Lee — refined profile

You already know his career path from round 1 notes. The refinement after meeting Frank:

**Sol is the peer-evaluation gate, NOT the management gate.** Frank decides whether to hire you. Sol decides whether you can hold up in a customer-facing room. That's a different angle than "do I want to work with this person." Sol's question is **"can this person solo a customer engagement at the depth our practice requires."**

**What Sol will probe:**

1. **Technical depth on real customer scenarios** — system design walkthroughs, not generic AI talk
2. **Engineering rigor** — DevOps, observability, state management, API design (his expertise)
3. **Industry awareness** — banking, healthcare, retail (his history). May test with a compliance scenario
4. **Operating mode** — can you juggle 3–4 projects, can you bill 70%, can you drive ACR
5. **Microsoft stack precision** — MAF vs Copilot Studio vs M365 Agents SDK vs Azure AI Foundry Agent Service. He'll know the difference; you need to also.

**What Sol will NOT focus on:**
- Cultural fit / values (that's Frank's lane, already passed)
- Strategic vision (Frank already heard this)
- Long career-trajectory stories (he wants engineering credibility)

**The trap to avoid with Sol:** answering at the strategic level when he asked at the architectural level. If he says "walk me through how you'd do X," that's a system design question, not a consulting-philosophy question. Get specific fast.

---

## What to adjust from round 1's deck (verbal only, no slide rewrites)

You already shipped the deck and it worked. Don't change slides. But adjust how you talk through them with Sol:

| Slide | Round 1 framing | Round 2 framing for Sol |
|---|---|---|
| **2** (60-sec story) | Three columns, narrate the path | **Compress to 60 sec.** Sol's not here for biography. |
| **3** (Gaming customer) | Set up the problem | **Skip the problem set-up.** Go straight to slide 4's diagram. Sol wants the architecture. |
| **4** (Architecture SVG) | Walk shape + bridge to Copilot Studio | **Go deep.** Component choices, state, failure modes, cost attribution. This is your strongest slide for Sol. |
| **5** (Cost framework) | Bottom-up + top-down | **Add ACR / MAU / Copilot seats** as the success metrics layer. "Cost framework is the design discipline; ACR + seats are the consulting outcome MS tracks." |
| **6, 7** (AOAI + Copilot rollouts) | Adoption playbook | **Lead with the deployment mechanics.** Sol respects shipping discipline. |
| **9** (Claude Code Workflow) | Systems thinking | **Frame as personal DevOps discipline.** Sol ran a DevOps Dojo. The CLAUDE.md + HANDOVER.md system speaks his language. |
| **11** (Why AIBS) | Three reinforcing capabilities | **Compress.** Sol's not evaluating fit — he wants to get to scenarios. |
| **12** (Gap + Ramp + KB receipt) | Honest gap | **Land the QR / knowledge base receipt** + **add the 70% utilization commitment** verbally. *"I know the practice runs at 70% utilization. The knowledge base proves I can ramp on my own time."* |

---

## Cadence for Friday

Assume 45 min — same as round 1.

- **First 5 min**: introduce yourself in 60 sec, ack round 1 went well, hand the floor to Sol to set direction
- **5–10 min**: probably scenario question — be ready to receive it before slide 1
- **10–25 min**: walk slides 4, 5, 9 in depth (the technical-heavy block)
- **25–35 min**: gap, ramp, knowledge base — drive toward operating-model conversation
- **35–45 min**: their questions + your questions back

**Be ready for Sol to lead with a scenario instead of letting you present.** Round 1 used scenarios; Sol is more technical, more likely to skip the deck walkthrough and go straight to design.

If he opens with a scenario: **welcome it**. Don't insist on walking the deck — pull up slide 4 or 5 only when relevant to your answer. The deck is a buffet, the scenario is the meal.

---

## Slide-by-slide narration — Sol-tuned (compressed)

### Slide 1 — Title
> "Jazz Lien. AI Business Solution Consultant. Round 2."

That's it. 10 seconds.

### Slide 2 — 60-second story (compress to 30 sec for Sol)
> "Tour-leader background, pivoted to tech in 2020. Azure cloud at Weblink, GCP at CloudMile for 2 years. 11 cloud certs — 5 Azure, 6 GCP Professional, plus Google Cloud Authorized Trainer. The technical column is what matters for our conversation."

Then move on. Don't dwell.

### Slide 3 — Gaming customer setup
**Skip or compress to 15 sec.**

> "Gaming client engagement last quarter — multi-agent customer service architecture. The slide has the business framing; let me show you the architecture instead."

Click forward to slide 4.

### Slide 4 — Architecture SVG (LEAD WITH THIS — 4-5 min)

This is your strongest slide for Sol. Go deep:

> "Reading left to right — User, API Gateway, Root Agent dispatching to two branches. RAG branch hits a vector DB fed by knowledge sources. Task branch hits internal APIs — CRM, payments, user DB. All LLM calls go through Model Armor for safety screening."

> "Underneath the diagram: **agents are stateless.** Conversation state lives in a session store keyed by user — for Vertex AI + ADK we used Firestore; on Microsoft side that's Dataverse or Cosmos DB depending on access pattern. Long-term memory in the vector DB. Identity-bound through user tokens — agent never sees raw credentials."

> "**Failure modes I designed for:** orchestrator timeout → fallback path. RAG retrieval miss → explicit 'I don't know' instead of hallucination. Model Armor block → user-visible error state with human-escalation path."

> "**Cost attribution:** every agent call tagged with session ID and agent ID. We can attribute spend to specific user journeys, not just monthly aggregate."

> "**Translation to Microsoft:** ADK doesn't map to Copilot Studio directly. ADK maps to **Microsoft Agent Framework — MAF** — the pro-code SDK that came out of AutoGen + Semantic Kernel. Azure AI Foundry Agent Service is the managed hosting layer. Copilot Studio sits above MAF as the low-code surface. M365 Agents SDK is for Teams + Copilot for M365 agents."

That last paragraph is the **single most important sentence you'll say to Sol.** The MAF distinction is your "I read the docs, not the brochure" signal.

### Slide 5 — Costing the solution (3-4 min, important for Sol)

Walk it normally, then **add this at the end:**

> "One thing I want to flag — the framework is bottom-up + top-down. But the success metric MS actually tracks is different. It's **ACR, MAU, and Copilot seat adoption.** So the cost framework is the design discipline; the consulting outcome is consumption growth post-deployment. 30-day leading indicators, 90-day business outcomes — defined in the SOW before deployment, then driven afterward."

Sol will recognize the language immediately. Round 1 confirmed this is how the practice measures success.

### Slide 6 — AOAI Evangelism (1-2 min if needed)

Sol won't dwell here. Quick:

> "First-wave AOAI work at 展碁國際 in 2023-2024. 23 tutorials, 50K reads, 85K views. The point is enablement at scale — same muscle that drives Copilot adoption."

### Slide 7 — GitHub Copilot rollout (1-2 min)

> "End-to-end Microsoft technology rollout. Seat assignment, IDE integration, bilingual deployment guides. Outcome: PM team launched a new AI-assisted-dev services product line. That's the loop — capability assessment, internal enablement, customer-facing docs, productized offering."

### Slide 8 — Builder practice (skip or 1 min)

Sol probably doesn't care about personal projects. If he asks:
> "Twelve-plus projects in two months. Three with paying customers. The discipline that makes that possible is the next slide."

### Slide 9 — Systems thinking / Claude Code Workflow (3-4 min, Sol's lane)

This is the slide that speaks Sol's DevOps Dojo language:

> "Claude Code Workflow — open-source AI development system. I treat AI not as a chat tool but as a development partner with persistent memory."

> "Six files, four protocols. CLAUDE.md and soul.md auto-load context — identity, conventions, voice. HANDOVER.md — cross-session relay. Skills/Knowledge — on-demand capability and reference. PM Handbook — decision frameworks."

> "**The point for our conversation:** this is engineering discipline applied to a non-deterministic workflow. Same instinct as DevOps applied to traditional code — make the implicit explicit, make the heroic repeatable. Result: 10× shipping velocity, ~10 colleagues at CloudMile adopted some version across engineering, sales, pre-sales."

### Slide 10 — Operating model (1-2 min — relevant to Sol's utilization concern)

This connects directly to Frank's round-1 reveal:

> "Solo, parallel, manager-unavailable — three modes. The relevant one for AIBS: parallel. 3-4 customer engagements concurrent, weekly one-pager up, clear escalation triggers. Decisions documented, not remembered. The HANDOVER.md protocol you just saw isn't just for AI — it's how I keep myself billable across multiple customers without dropping balls."

The "without dropping balls" framing addresses the 70% utilization question implicitly.

### Slide 11 — Why AIBS, why now (compress to 1 min)

Sol's already convinced. Compress:

> "Three capabilities converging at the role — customer translation, AI depth, learning velocity. The triangle visual makes the point; I'll skip the bullet expansion unless you want to dig in."

### Slide 12 — Gap + Ramp + Knowledge base receipt (LAND THIS, 3-4 min)

The receipt is your closer:

> "Three gaps for the Modern Workplace flavor — Intune at enterprise scale, Defender for Endpoint operations, Modern Desktop / M365 cert track."

> "Ramp: 60 days, Entra ID first because it's closest to my existing Azure security work, then Intune + Autopilot, then Defender for Endpoint."

> "But the receipt matters more than the plan. I built a **public knowledge base** specifically on Microsoft Modern Work — nine sections covering identity, endpoint, Copilot, Power Platform, security, business case, and interview prep itself. **Live at jazz-knowledge-management.pages.dev.** The QR's on the slide. The ramp started before I applied."

> "On the operating side — **I know the practice runs at 70% utilization. The knowledge base proves I can do the learning curve on my own time. I won't be a non-billable trainee for 90 days; I'll be a billable contributor faster than that.**"

That last sentence is the **directly Frank-confirmed-info acknowledgment** that signals you listened in round 1.

### Slide 13 — Closing (30 sec)

> "QR for the full archive at jazzlien.com. Happy to take questions on any slide — or pivot to a scenario if you'd rather."

The "or pivot to a scenario" offer is the **disarming move that respects Sol's time and his style.**

---

## Scenario interview prep — THE BIG ONE

Round 1 used scenarios. **Sol almost certainly will.** Practice these patterns tonight or tomorrow morning before the interview.

### The template — say this back to ANY scenario

When Sol gives you a scenario, **don't dive into the answer immediately.** First, demonstrate scoping discipline:

> *"Two clarifying questions before I design — first, who are the users (numbers, personas, primary apps they need)? Second, what's the compliance posture — regulated industry, data residency, sensitivity classification? With those I can be more concrete."*

This earns you 30 seconds to think AND demonstrates that you don't bluff scope.

**Then your answer follows this shape every time:**

1. **Discovery** — what's the current state, constraints, success criteria
2. **Layered design** — identity → device/access → workload → AI layer → governance
3. **Edge cases** — at least 3, ideally tied to compliance or scale
4. **Phased rollout** — pilot → expansion → operations
5. **Metrics** — leading indicator + business outcome, defined upfront

### Scenario 1 — Document sharing for scientists (the round-1 example, refined)

> *"Design a document-sharing capability for pharma scientists collaborating on new-medicine policy across multiple internal teams and external regulatory bodies."*

**Your answer:**

> *"Discovery first — pharma context means HIPAA-equivalent regulated data, multiple sensitivity tiers (clinical trial data, regulatory submissions, internal research notes), external collaborators with B2B identity. Mixed-device fleet, scientists on corporate Windows + some Mac, regulators on whatever they bring."*

> *"Layered design:*
> *Identity — Entra ID with B2B for external regulators, Conditional Access requiring MFA + compliant device for sensitive content tiers, sensitivity labels on documents to enforce policy at the document level.*
> *Collaboration — SharePoint sites segmented by sensitivity tier, Teams for synchronous, OneDrive for personal drafts. Information barriers between research and commercial teams to prevent regulatory issues.*
> *Information protection — Microsoft Purview for DLP, sensitivity labels with encryption, auto-classification using trainable classifiers for pharma-specific terminology.*
> *AI layer — Copilot for M365 to summarize regulatory submissions, BUT inherits all sensitivity labels and DLP — Copilot doesn't bypass the governance.*
> *Audit — every share, every Copilot query, logged for regulatory inspection."*

> *"Edge cases — external collaborator from a competitor (cross-tenant policies need to block), researcher leaves the org (access revocation cascades to all shared content), regulatory inspection requires 7-year audit retention.*

> *"Rollout — pilot with one research team for 6 weeks, measure: time-to-find-document, audit incident rate, helpdesk tickets. Then expansion by therapeutic area, then external collaborator onboarding last."*

> *"Success metric — operational: Copilot seat adoption + MAU on M365 apps. Strategic: time-to-regulatory-submission reduction. Defined in SOW."*

That's a 90-second answer that demonstrates Modern Workplace depth + compliance awareness + Microsoft stack precision + ACR/MAU framing.

### Scenario 2 — Copilot for M365 rollout (5,000 seats, financial services)

> *"How would you approach Copilot for M365 deployment for a 5,000-seat regional bank?"*

**Frame:**

> *"Banking adds tight regulatory posture. Discovery first — current M365 SKU (E3 vs E5 determines what tools you have), data governance posture (sensitivity labels in place?), DLP policies maturity, third-party data sources Copilot might need to query."*

> *"Design — Copilot for M365 is per-user license stack on top of M365. Three prerequisites: clean identity (everyone in Entra ID, no orphans), sensitivity labels deployed (Copilot inherits them — without labels, you risk customer data exposure in AI responses), DLP policies for financial regulated content."*

> *"Rollout: 3-phase. Phase 1 — IT pilot, 50 users, 4 weeks. Measure: prompt-to-useful-response rate, hallucination incidents on banking-specific content, helpdesk volume. Phase 2 — finance + ops, 500 users, focus on adoption metrics. Phase 3 — full rollout, 5,000 users, target 40% MAU within 90 days."*

> *"Edge cases — Copilot in Teams meetings recording client calls (consent + retention policy), Copilot in Word generating loan documents (review-and-approve workflow before send), Copilot accessing CRM data via Microsoft Graph (audit who-saw-what)."*

> *"Success metrics — ACR growth from Copilot consumption + adjacent Azure workloads (Purview, Defender), Copilot license seat utilization rate, helpdesk-tickets-per-1000-users as the operational health metric."*

### Scenario 3 — Defender for Endpoint deployment

> *"3,000-device enterprise wants to deploy Defender for Endpoint with Defender XDR. Walk me through your approach."*

**Frame:**

> *"Discovery — current EDR (replacing what?), device mix (Windows / Mac / mobile), Intune posture (devices already enrolled and compliant?), licensing tier (Defender for Endpoint Plan 1 vs Plan 2, or full Defender suite)."*

> *"Design layers — Defender for Endpoint as the EDR agent, ASR (attack surface reduction) rules tuned to environment, automated investigation enabled but starting in audit mode, integration with Defender XDR for cross-signal correlation (identity, email, cloud apps), Sentinel integration for SOC if they have one."*

> *"Rollout — phased by device fleet segment. IT pilot first (50 devices, ASR audit mode). Then standard knowledge workers, then frontline. Each phase: 2 weeks audit mode, measure false-positives + true-positives, then promote to block mode."*

> *"Edge cases — third-party security tools causing conflicts, BYOD endpoints (MAM-without-enrollment context), legacy apps triggering ASR false positives, the 'shadow IT' macOS devices that need separate handling."*

> *"Metrics — incident-detection time, false-positive rate week-over-week, ACR from Defender consumption."*

### Scenario 4 — Custom AI agent for a service-provider customer

> *"A service-provider customer wants a multi-tenant agent that answers customer queries about their products. They have 200 enterprise tenants. Design it."*

**Frame:**

> *"Multi-tenancy is the hard part — tenant isolation in identity, data, prompts, knowledge sources. Discovery: what's their auth model (B2B? federated identity per tenant?), data isolation requirements (some tenants regulated, some not), customization tier (do tenants get to customize prompts / knowledge?)."*

> *"Design — Copilot Studio per tenant for low-code, OR MAF on Azure AI Foundry for pro-code if customization is deep. Tenant-isolated Dataverse for tenant-specific knowledge, Azure AI Search with per-tenant indexes, Entra ID with multi-tenant app pattern for auth. Identity propagated through the agent call stack so the LLM never crosses tenant boundaries."*

> *"Edge cases — tenant onboarding (60 minutes to provision a new tenant), prompt injection from one tenant trying to extract another's data, billing attribution per tenant for ACR, tenant offboarding (data deletion compliance)."*

> *"Rollout — 5 pilot tenants for 6 weeks, measure cost-per-query and isolation incidents. Then onboarding ramp."*

> *"Metrics — ACR per tenant + adoption rate per tenant + revenue attribution back to the service provider."*

---

## Microsoft-stack Q&A — quick refresh

You've read this section before. Glance over it the night before. Key terms Sol will use:

- **MAF (Microsoft Agent Framework)** — pro-code SDK, AutoGen + Semantic Kernel successor (2026)
- **Azure AI Foundry Agent Service** — managed hosting layer, Vertex AI Agent Engine equivalent
- **Copilot Studio** — low-code conversational layer above MAF
- **M365 Agents SDK** — Teams + Copilot for M365 agent toolkit
- **Entra ID** — Azure AD's new name
- **Conditional Access** — policy engine (signals + controls)
- **Intune** — MDM + MAM platform
- **Autopilot** — zero-touch Windows provisioning
- **Defender for Endpoint** — EDR (P1 basic, P2 full + automated investigation)
- **Defender XDR** — cross-signal correlation across identity / email / endpoint / cloud apps
- **Purview** — data governance + DLP + sensitivity labels
- **Sentinel** — SIEM
- **Zero Trust** — verify explicitly + least privilege + assume breach
- **ACR** — Azure Consumption Revenue (the practice's metric)
- **MAU** — Monthly Active Users (on Copilot / M365)

---

## Direct Q&A from Sol (predicted)

These are tuned to Sol specifically. Each has **Frame**, **Say this**, **Watchpoint**.

### Sol Q1: "Walk me through a system design end-to-end."

**Frame:** Generic but Sol-specific — he wants the engineering layer, not the diagram surface.

**Say this:** see slide 4 walkthrough above. The full version with state, failure modes, cost attribution, and the MAF translation.

**Watchpoint:** Don't read the diagram. *Talk about what's underneath.* Specific tool choices (Firestore vs Cosmos DB, Entra ID, session-tagged costs) are the signal.

---

### Sol Q2: "How would you CI/CD a multi-agent system?"

**Frame:** Sol ran a DevOps Dojo. He cares about HOW you ship.

**Say this:**
> *"Five layers. Source-control everything — agent definitions, prompts, tool schemas, configuration. The Claude Code Workflow system is the personal version. CI runs unit tests on tools (deterministic, fast) plus prompt regression tests against a golden set. Integration tests run agent loops end-to-end against a sandbox — slow and expensive, so PR-merge only. Staging deployment with shadow traffic — production queries hit both prod and staging, staging output logged but not returned to user. Observability — every call instrumented for latency, tokens, tool invocations, quality signals like thumbs up/down or downstream task completion. Application Insights on the MS side."*

> *"Deployment: blue-green for the orchestrator, canary for prompt changes."*

**Watchpoint:** Be honest about what you've shipped vs designed. *"This is how I'd architect it; the closest production CI/CD I've run is my personal AI projects, simpler version of the pattern."*

---

### Sol Q3: "How do you handle state in distributed agents?"

**Frame:** Sol uses Dapr in banking. State management is his territory.

**Say this:**
> *"Three layers of state. Conversation state — short-term, in a fast key-value store. Session-scoped, expires after inactivity. On Microsoft side, Dapr state-management building block is the right fit. Memory state — long-term, what the agent remembers across sessions. Vector DB or graph DB depending on retrieval patterns. Configuration state — agent definitions, tool registrations, prompt templates. Source-controlled, deployed through CI/CD, not stored at runtime."*

> *"Critical pattern: agents are stateless processes. State lives in the platform, not the agent. That's what makes horizontal scaling work — you can lose any agent instance without losing user context."*

**Watchpoint:** Naming Dapr signals you researched him. Don't force it if the question doesn't fit, but if state distribution comes up — say it.

---

### Sol Q4: "How does your AI architecture translate to Microsoft's stack?"

**Frame:** The critical translation question. Get the MAF distinction right.

**Say this:**
> *"Three direct translations. ADK orchestration → Microsoft Agent Framework, MAF — pro-code, .NET and Python, came from AutoGen + Semantic Kernel merger. Vector DB + RAG → Azure AI Search + Microsoft Graph for tenant content. Custom agents → MAF for pro-code, Copilot Studio for low-code, Dataverse for the data layer. Managed hosting through Azure AI Foundry Agent Service."*

> *"Where Microsoft pulls ahead — identity unified through Entra ID, connectors to M365 Graph and Power Platform are first-class. Don't have to build the integration layer."*

**Watchpoint:** Lead with **MAF, not Copilot Studio.** If you say Copilot Studio is the ADK equivalent, you're wrong — Sol will register it.

---

### Sol Q5: "Tell me about a time you cost-optimized an AI workload."

**Frame:** Sol did this for FamilyMart. He'll relate.

**Say this:**
> *"Slide 5's framework. Biggest lever in practice is model selection — for a customer service bot at 10K queries a day, dropping from a flagship model to mid-tier is often 60-80% cost reduction with sub-10% accuracy drop on routine queries. The trick is query segmentation and routing — frontline queries to cheap model, edge cases to flagship."*

> *"Second lever — orchestration efficiency. Multi-agent stacks roughly 2-3× single LLM call. Consolidating two agent steps into one prompt sometimes halves the cost without quality loss. That's a refactoring exercise after a month of production data."*

> *"Third — caching, especially semantic caching for repeat intents. Even 20% hit rate is 20% inference savings."*

> *"The discipline I bring is doing this **at design time, not after the bill arrives.** Slide 5 codifies it."*

**Watchpoint:** Don't fabricate specific numbers. The framework is defensible without them.

---

### Sol Q6: "Compliance question — how do you handle regulated industry AI?"

**Frame:** Be honest about what you've done vs designed. Sol has built for SKMH and CDFH; he knows the real bar.

**Say this:**
> *"Three areas. Data flow controls — what data the agent can see and return. Sensitivity labels, DLP policies, output filtering through Model Armor or equivalent for PII redaction. For my gaming customer this was less critical; for banking or healthcare it's table-stakes from day one."*

> *"Audit trails — every agent decision logged with context. Compliance needs 'why did the system give this answer to this user at this time.' Session, agent, prompt version, model version — tagged on every LLM call."*

> *"Model governance — version pinning, change approval, output validation. The model the customer signed off on cannot change without process."*

> *"Honesty — I'd partner with someone who's done HIPAA or banking-specific work for the first project. Compliance is where consulting humility matters. Sol, you've done SKMH healthcare and CDFH banking — I'd want to learn that pattern from someone who's lived it."*

**Watchpoint:** The "I'd want to learn from you" close is genuine. Sol will respect it. Bluffing on compliance is a disqualifier.

---

### Sol Q7: "What's your API management story for agent endpoints?"

**Say this:**
> *"Gateway pattern — Azure API Management fronts agent endpoints. Three jobs. Auth and tenant isolation: Entra ID for identity, JWT validation at gateway, tenant context propagated downstream. Per-tenant rate limits prevent one customer from starving another. Observability: every request tagged, latency tracked, errors aggregated, Application Insights downstream. Versioning and rollback: agent capabilities evolve fast, gateway routes v1 of a tool to old agents while v2 rolls out, no downtime."*

> *"For tool exposure — agents call internal APIs through the same gateway as external traffic. Same security model, same observability. Tools don't get a backdoor."*

---

### Sol Q8: "Test automation for AI — what's your approach?"

**Say this:**
> *"Three layers. Deterministic tests on tools — does the SQL query return the right shape, does the API call succeed with auth. Prompt regression tests — golden set of inputs that should produce specific output shapes; LLM judges or string matching on key fields. End-to-end agent loops — slow, expensive, PR-merge only."*

> *"The hardest part is prompt regression. Quality drift is silent. Output slightly worse for two weeks before someone notices. I'd instrument production with quality signals — task completion, user thumbs-up, fall-back-to-human rate — and treat them as real-time test signals, not just observability."*

---

## The operating-model conversation (NEW — round 1 surfaced this)

Sol will likely ask about how you'd operate inside the practice. Three sub-questions, three answers ready.

### "How would you ramp to 70% billable utilization?"

> *"Treat customer engagements as repeatable patterns. Same architecture muscle, different customer. The Claude Code Workflow system I built — decision frameworks, handover protocols, knowledge base — exists precisely to keep me billable across concurrent engagements. I expect 1-2 months to learn the practice's rhythm; after that 70% is achievable through reusable patterns. The MS Modern Work knowledge base I built before applying is the foundation."*

### "Can you juggle 3-4 customer projects simultaneously?"

> *"That's the operating model on slide 10. Knowledge transfer designed in from day one. Weekly status one-pager up to the manager. Clear escalation triggers. Dashboard-driven priority management. The 'no surprises' rule — if Frank hears about something for the first time in a meeting, I've failed at communication. Same documentation protocol with customers — decisions written, not remembered. That's how you don't drop balls across multiple engagements."*

### "How do you drive ACR / consumption / Copilot seats with a customer?"

> *"The success metric MS tracks isn't the deployment — it's the consumption growth post-deployment. 30-day leading indicator: usage frequency on the deployed capability. 90-day business outcome: ACR growth, Copilot MAU, seat utilization rate. Defined in the SOW upfront."*

> *"The consulting lever is making the customer's adoption journey easier. Not just 'we deployed Copilot for M365' — 'we deployed Copilot for M365, here's the change-management playbook, here's the prompt library by department, here's the adoption dashboard the IT team owns post-handover.' Consumption growth is downstream of the customer being able to operate without us."*

---

## Data residency + Taiwan / GCR sensitivities (NEW — round 1 flag)

Frank flagged that Taiwan customer data — especially government, financial, sensitive verticals — must stay outside China-region clouds. Sol may probe this.

**Frame:** This is a real architectural constraint, not just a checkbox. Show you've thought about it.

**Say this if it comes up:**
> *"Taiwan customer data, especially government and regulated verticals, has data residency requirements that exclude China-region clouds. Azure region selection matters: Taiwan North when it's available, Japan East, or Southeast Asia as alternatives. Sovereign cloud commitments documented in customer contracts. Cross-region replication has to respect the residency rules — no implicit failover to a non-compliant region."*

> *"For AI specifically — Azure OpenAI deployments need to be in the same residency zone. The Microsoft Agent Framework runtime should run in Azure AI Foundry in the same zone. Customer data going through the AI layer doesn't get to take a shortcut through a different region."*

> *"Compliance posture for this is Defender for Cloud + Purview — sensitivity labels on data, region-aware policies, audit trails proving data didn't traverse non-compliant regions."*

**Watchpoint:** If Sol asks about specific Azure region availability or features, be honest if you don't know exact specs. *"I'd validate the current Azure region capabilities in Taiwan against the customer's specific requirement before committing in the design."*

---

## Morning-of checklist (Friday)

**60 minutes before:**
- Re-read the scenario interview prep section out loud, all 4 scenarios
- Re-read the MAF distinction (it's the single highest-leverage technical statement)
- Re-read the operating-model conversation answers (utilization, portfolio, ACR/MAU)
- Glance at slide 4, 5, 9, 12 — the slides you'll lean on hardest

**15 minutes before:**
- Water nearby
- QR code visible / phone accessible
- jazz-knowledge-management.pages.dev open in a tab — be ready to share screen
- Calm breath, slow speech

**During:**
- If Sol leads with a scenario, **welcome it** — don't insist on walking the deck
- Pause after each technical answer — let him probe
- If you don't know something, say so + offer the adjacent experience + the closing knowledge-base lookup
- Reference round 1 conversations naturally — *"Frank mentioned the practice runs at 70% utilization..."* — shows continuity, not gossip

**Closing question to ask Sol:**

> *"What does success look like for the first 90 days in this role from a peer architect's perspective? What separates someone who hits the ground running from someone who struggles?"*

This signals you're already thinking like a member of the practice, not a candidate.

---

## After the interview

Two things to capture before you forget:

1. **Surprising questions** — anything you didn't anticipate, regardless of how you answered
2. **The follow-up question Sol asked after each of your answers** — that's where his interest really lives

These notes will be gold for the blog post you mentioned writing later.

Go get it.
