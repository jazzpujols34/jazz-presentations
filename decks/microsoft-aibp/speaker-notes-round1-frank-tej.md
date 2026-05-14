# Microsoft AI Business Solutions — Speaker Notes

Total runtime target: ~18–22 minutes of material if walked end-to-end. In practice, you'll spend more time on 3–4 slides driven by their questions. Each slide can carry 60–120 sec of narration.

**Posture:** Conversational, not presentational. Slides are anchors for discussion, not a monologue. Pause after each slide's main point — give the interviewer space to interrupt.

**Voice principles:**
- Lead with the answer. Skip preamble.
- Concrete over abstract. Numbers, examples, names of tools.
- When you don't know something, say so. Don't bluff.
- Push back gently when relevant. Show you have a point of view.

---

## This week's interviewers — read this first

**Frank Chang** — *Consulting Capability Lead @ Microsoft | AI Business Solutions*

He owns the **practice** — methodology, hiring bar, capability development. As the lead, his questions will be more **strategic** than tactical:
- Where do you see AI consulting going? Why this practice, why now?
- How do you think about building consulting capability — yours and others'?
- Show me a customer engagement where you owned the outcome end-to-end.
- Cultural fit: growth mindset, customer obsession, how you handle being wrong.

**Lean into with Frank:**
- Slides 6, 7 (AOAI evangelism + Copilot rollout) — these show "translating AI capability into enterprise adoption at scale," which is the literal practice mission.
- Slide 9 (Claude Code Workflow) — the OSS system + the "~10 colleagues onboarded" line is capability development in action.
- Slide 11 (Why AI Business Solutions) — the triangle visual is a strategic frame, his language.

**Don't lead with on Frank:** raw multi-agent architecture without business framing. He's been senior enough that he wants to see how you frame value, not how you wire components.

---

**Kanwartej Basrai** — *Principal Consultant at Microsoft*

He's a senior individual contributor — likely a peer level (or one above) to the role being filled. His questions will be more **technical and operational**:
- Walk me through how you'd actually design X for client Y.
- What would you configure first? What edge cases would you watch?
- How does that translate to Copilot Studio / Power Platform / D365?
- Where's the line between "AI architect" and "Microsoft Modern Workplace consultant"?

**Lean into with Kanwartej:**
- Slide 4 (Architecture SVG) — walk the diagram with him; this is the technical depth he wants to see.
- Slide 5 (Cost framework) — token math + budget envelope reads as someone who's done the work.
- Slide 12 (Gap & Ramp) — be honest about Modern Workplace stack gaps; show the ramp.

**Be ready for** specific Microsoft-stack questions (see "Microsoft-stack Q&A" section below). Kanwartej will probe whether you can hold up in a customer room when the topic is Intune policy authoring or Conditional Access design, not just abstract AI.

---

**Reading both signals:**
- If Frank goes first → frame the conversation, set the strategic posture, then go technical when invited.
- If Kanwartej goes first → he'll test depth on a specific scenario. Don't dodge — answer concretely, then bridge to your AI work as the differentiator.
- If both at once → answer the technical question concretely, then add one strategic sentence so both feel addressed.

---

**Cheng-Han "Sol" Lee** — *Architect at Microsoft (Friday's interview)*

9+ years at Microsoft, currently a senior Architect in Taipei. **The deepest technical interviewer of the three** — more senior than Kanwartej, with hands-on $2.8M architecture experience leading 24-person dev/QA teams.

**What he's built:**
- Banking: CDFH KGIB internet banking + mobile platform — Dapr, Kubernetes, DevSecOps, Azure Stack HCI
- Retail AI: FamilyMart order prediction with Azure ML — he's done real AI cost optimization
- Healthcare: Hospital Information System — ASP.NET Core, 5M lines of code, 93 third-party integrations
- DevOps Dojo facilitator: he ran customer training, avg 4.5/5 rating

**His expertise:** Azure architecture, DevOps, API management, microservices, test automation, networking. PMP + Agile. Currently working with OpenAI Products inside MS Industry Solutions Delivery.

**His questions will be more architectural than Kanwartej's:**
- System design end-to-end, not just policy authoring
- "How would you CI/CD a multi-agent system?"
- "How do you handle state and observability in distributed agents?"
- "Talk to me about cost-optimizing Azure workloads"
- "What's your API management story for agent endpoints?"
- "How do you ship — what's your DevOps muscle look like in practice?"

**Lean into with Sol:**
- Slide 4 (Architecture SVG) — walk it deeply, talk about specific tool choices and tradeoffs, not just shapes
- Slide 5 (Cost framework) — he ran cost optimization for FamilyMart; he'll respect the token math
- Slide 9 (Claude Code Workflow / Systems Thinking) — the persistent memory + handover protocols speak to his DevOps mindset. The "open-source workflow" framing is for him.
- Slide 12 (Gap + Ramp + knowledge base receipt) — Sol will appreciate concrete proof more than promises

**Don't lead with on Sol:** strategic vision (that's Frank's lane) or generic AI talking points. Sol wants engineering rigor — show him the wiring, not the marketing.

**Connection points to surface naturally:**
- Both came up through deep technical work before consulting
- He's done AI work for FamilyMart (Azure ML); you've done AI for gaming (Vertex AI + ADK) — both pre-sales-to-delivery patterns
- He's worked on Dapr/microservices in banking; mention Dapr if multi-agent state distribution comes up — it IS used in Microsoft Agent Framework for state persistence patterns

---

## Opening — before clicking into slide 1

> "Thanks for the time. I put together a short deck to walk through what I've been doing, what I've built, and how I think. Thirteen slides — mix of customer work and personal builds, ending with a 60-day ramp plan. Feel free to interrupt at any point. These slides are anchors for conversation, not a script. Let me start."

---

## Slide 1 — Title

**Setup (~10 sec):**

> "Jazz Lien. AI Business Solution Consultant — that's what I'm here for. Currently a solution architect at CloudMile. This is the portfolio walkthrough."

**Transition out:**

> "Let me give you the 60-second story first."

---

## Slide 2 — The 60-Second Story

**Setup:**

> "Each chapter of my career taught me the next stack. Three columns — the path, what I do, and the cloud credentials underneath."

**Path column:**

> "Started in foreign languages — graduated from 台科大 Applied Foreign Languages with a year in Spain. Then I was a tour leader for eight years. That's where I first learned to translate complex situations — visas, logistics, cultural friction — into clear instructions for diverse audiences. Then QA at Wipro. Took continuing education to pivot into Azure cloud at 展碁國際. Now GCP architecture and TAM at CloudMile."

> *(If they pause on tour leader — lean in)*: "It's the same muscle as enterprise consulting. A tour leader is a professional translator between a complex system and people who need it to just work."

**What I do column:**

> "Enterprise architecture across airline, gaming, media, Web3. Multi-agent AI, RAG, data modernization. I also ship AI products end-to-end on the side — including an open-source AI development workflow you'll see later. The customer side and the personal side feed each other."

**Cloud credentials column — point at the cert wall:**

> "Eleven cloud certifications, Azure first. Five Azure — AI Engineer Associate, Developer Associate, Data Engineer Associate, AI Fundamentals, and Azure Fundamentals. Six GCP Professional — Architect, DB, DevOps, Workspace, ML, and Security. Plus Google Cloud Authorized Trainer."

> *(Optional emphasis if asked about the AI cert specifically)*: "AI Engineer Associate is the one most directly relevant to this role. The cert wall isn't decorative — it's the proof that I pick up each stack as it lands."

**Transition out:**

> "Let me show you the most recent enterprise design — a gaming customer last quarter."

---

## Slide 3 — Featured Architecture: Multi-Agent Customer Service

**Setup:**

> "Q4 last year. Gaming client. Customer service team buried under repetitive queries, knowledge fragmented across DOCX, HTML, PPT. Staff attrition kept resetting service quality every few months. They wanted AI-first response with human-in-loop escalation."

**Right side — what I designed:**

> "Multi-agent. Root orchestrator on top, RAG agents handle knowledge retrieval, task agents handle transactional work — CRM, payments, game admin. Built on Vertex AI + Agent Development Kit. Model Armor on the LLM layer for safety screening. Five-phase rollout — discovery, MVP, beta, scale, multi-channel."

**The footer — say this out loud, especially to Frank:**

> "Client ultimately elected to build in-house. The architecture gave them the clarity to make that call. A valid consulting outcome — sometimes the win is enabling someone else's decision."

**Transition out:**

> "Here's how the pieces fit together."

---

## Slide 4 — The Architecture Diagram

**Walk the diagram with Kanwartej — don't just read it.**

> "Reading left to right: User comes in through an API Gateway. Root Agent — the orchestrator — decides where to route. Two branches."

> "Top branch: RAG. The agent group queries a vector DB. Vector DB is fed by knowledge sources — FAQ, patch notes, docs. That's the 'what does this customer need to know' path."

> "Bottom branch: Task agents. They call internal APIs — CRM, UserDB, PaymentDB, GameAdmin. That's the 'do something for the customer' path."

> "All LLM calls go through Model Armor before hitting the LLM itself. Safety, compliance, prompt injection screening. Non-negotiable for enterprise."

**The key line — the slide's bridge to Microsoft:**

> "Pattern's built on Vertex AI + ADK. The orchestration shape translates one-to-one to **Microsoft Agent Framework — MAF** — Microsoft's pro-code SDK for multi-agent systems. MAF came out of the AutoGen + Semantic Kernel merger in 2026; supports .NET and Python. Azure AI Foundry Agent Service is the managed hosting layer — equivalent to Vertex AI Agent Engine. Copilot Studio sits above both as the low-code conversational surface. Add Defender for Cloud Apps and you have the enterprise-grade Microsoft equivalent."

**Transition out:**

> "Now — designing it is one thing. Costing it is another. Let me show you how I cost an AI solution."

---

## Slide 5 — Costing the Solution *(your "fixed" slide — be ready)*

**Setup:**

> "When a client asks 'how much will this cost,' I work from two angles — bottom-up and top-down — and reconcile."

**Left card — bottom-up:**

> "Inference dominates the variable cost. Average tokens per query times volume times model price. To make it concrete: a chatbot handling 10K queries a day at roughly 2K tokens per query is 20M tokens daily. At $3 per million for a mid-tier model, that's two-ish-thousand US dollars a month on inference alone — before anything else."

> "Then I layer orchestration overhead — multi-agent stacks roughly 2-to-3× a single LLM call because the orchestrator plus the worker agents each consume tokens. Then retrieval — embeddings and vector DB queries. Platform — compute, storage, logs. Licenses — per-seat enterprise AI subscriptions. I'd cite Gemini Enterprise specifically, because that's the one I've actually deployed at CloudMile for internal agent-assist on the human service team. Same per-seat model translates directly to Copilot for M365 or Dynamics 365 Copilot for Service on the Microsoft stack — different SKU, same shape. And implementation — design, build, change management, training."

**Right card — top-down:**

> "Two anchors. First, the budget envelope — what the client will actually authorize. Second, status quo baseline — what they're spending today to deliver the same outcome. A 20-FTE service desk is roughly half a million US dollars a year, fully loaded. That's the number the solution has to beat. Then phased rollout — pilot small, prove value, expand. Caps blast radius if assumptions are wrong."

**The principle (point at the dark strip):**

> "The gap between the two numbers is what drives every design decision. Model selection. Agent count. Phasing. Not the other way around."

**Footer line:**

> "Value is tracked separately — 30-day leading indicator plus 90-day business metric, defined in the SOW. No metric, no deploy."

**If they ask about Modern Workplace cost specifically:** *"Same framework, different cost drivers. Bottom-up: M365 E3/E5/EMS per-user, Copilot for M365 add-on at $30/user/month, Defender plans, plus implementation hours. Top-down: current spend on endpoint helpdesk tickets, security incidents, device provisioning time. A typical mid-market client is paying real money for inefficient endpoint operations — the AI-infused Modern Workplace pitch is replacing that with automation."*

**Transition out:**

> "Now backwards — let me show you how I got here on the AI side."

---

## Slide 6 — First-Wave Azure OpenAI Evangelism

**Setup:**

> "Taiwan, 2023 to 2024. When Azure OpenAI launched, it was the only way for Taiwanese enterprises to get GPT models with compliance. I was on the front line."

> "Two roles in parallel — internally as a sales engineer at 展碁國際, externally as a bilingual technical writer."

**Left card — what I did:**

> "Internal: set up first AOAI demos for enterprise prospects. Trained sales teams on capabilities, role-based access, compliance. External: published 23 deep-dive tutorials in English and Traditional Chinese across 2023 and 2024."

**Right card — point at the Medium screenshot:**

> "Those are actual Medium analytics. Top article on GitHub Copilot in JetBrains hit 23K reads. Postman + Azure OpenAI API, 8.9K. Chinese GitHub Copilot tutorial, 7.4K. Five articles. 85K total views, 50K reads. Public dashboard — you can verify it."

**Footer line:**

> "Translating new AI capability into enterprise adoption — at scale."

> *(Let the line breathe; don't add commentary. The interviewer will draw the conclusion.)*

**Transition out:**

> "Same pattern with GitHub Copilot rollout — different tool, same job."

---

## Slide 7 — GitHub Copilot Rollout

**Setup:**

> "GitHub Copilot — same instinct as AOAI. Bring a new AI capability into an enterprise that's not AI-native."

**Left card:**

> "End-to-end demo: signup through seat assignment through IDE integration. Bilingual deployment guides — JetBrains and VS Code. Enabled my PM team to launch a new product line around AI-assisted dev services, which is a different revenue category than infrastructure resale."

**Right card — point at the screenshot:**

> "That's the Chinese GitHub Copilot tutorial republished on Weblink CSP — a Taiwanese industry blog. The bilingual content distributes; it doesn't just live on Medium."

**Footer line — emphasize the Microsoft parallel:**

> "Take a new AI capability, make it deployable, prove ROI, train the org to use it. That's the loop. Identical to what M365 Copilot rollout will require enterprises to do over the next two years."

**Transition out:**

> "That's the customer-facing side. Let me show you what I build on my own time."

---

## Slide 8 — Personal AI Builder Practice

**Setup:**

> "Modern AI dev tools in my hand. Twelve-plus projects shipped in two months. Six on the slide."

**Walk through quickly — don't dwell:**

> "Memorial video AI service — production, live payments through Stripe. Podsight — Taiwanese finance podcast transcription pipeline, Groq Whisper. Jazz Gallery — AI artwork gallery with auth and admin dashboard. Articulate — mobile app, 1,005 etymology-based vocabulary entries with 215 roots. GCP Landing Zone — production-grade, 7 Terraform modules, 54 resources. And the Claude Code Workflow open-source system, which gets its own slide."

**Caveat — be honest:**

> "These aren't toys. Three have paying customers. They're real but small. The point isn't scale — it's that I can take an idea from spec to production deployment in days, alone, end-to-end."

**Transition out:**

> "The last one is worth its own slide. It's how I scale."

---

## Slide 9 — Systems Thinking About AI

**Setup:**

> "Open-source AI development workflow system. The project is called Claude Code Workflow — that's the screenshot on the right, the actual project card from my portfolio."

**Core narration:**

> "I treat AI not as a chat tool but as a development partner with persistent memory. Six files, four protocols, one principle — every session builds on the last."

**Walk the components:**

> "CLAUDE.md plus soul.md — auto-loaded context. Identity, conventions, voice. HANDOVER.md — cross-session relay, so state survives context resets. Skills and Knowledge directories — on-demand capability and reference, kept separate. And a 10-chapter PM Handbook — decision frameworks for discovery, prioritization, ship discipline."

**Results:**

> "10× shipping velocity. Twelve-plus projects in two months proves it. About 10 colleagues at CloudMile have adopted some version across engineering, sales, and pre-sales."

**The hook — say this, especially to Frank:**

> "If you're hiring someone to help enterprises operationalize Copilot Studio agents — agents that need memory, handoff protocols, decision frameworks — this is the kind of thinking they should bring. Written up in detail at jazzlien.com/blog."

**Transition out:**

> "Speaking of operating model — let me show you how I actually run engagements."

---

## Slide 10 — Operating Model

**Setup:**

> "Three modes. Solo on a project. In parallel with other work. And when the manager isn't available."

**Solo card:**

> "Knowledge transfer is designed in from day one. The CLAUDE.md and HANDOVER.md system you just saw isn't just for AI — it's the same documentation protocol I use with human teammates and clients. Decisions are written, not remembered."

**Parallel card:**

> "Weekly status one-pager up to manager. Clear escalation triggers. Dashboard-driven priority management. The 'no surprises' rule — if the manager hears about something for the first time in a meeting, I've failed at communication."

**Manager-unavailable card:**

> "Own the decision. Document the reasoning. Flag the risk. Move forward. Synchronize on next available cadence. Cost of waiting usually exceeds cost of correcting."

**Footer line:**

> "Built for parallel engagement work — which is the AI Business Solutions shape, as I understand it."

**Transition out:**

> "OK — why this role, why now."

---

## Slide 11 — Why AI Business Solutions, Why Now

**Setup — point at the triangle:**

> "Three capabilities reinforcing each other. The role sits at the convergence — not at any single vertex."

**Customer translation:**

> "Google Cloud Authorized Trainer — official. Two years enterprise consulting at CloudMile. Bilingual technical writer with documented reach. Pre-sales and post-sales experience."

**AI architecture depth:**

> "Multi-agent designs you've seen. ADK orchestration pattern that translates directly to Microsoft Agent Framework — the AutoGen + Semantic Kernel successor — with Copilot Studio as the low-code layer. Production AI products shipped. Open-source AI workflow system."

**Learning velocity:**

> "Eleven cloud certs earned while delivering customer work — that's the velocity proof. AOAI → ADK → Claude Code → Microsoft Agent Framework is the four-stop arc. MAF is the direct Microsoft equivalent of ADK — pro-code, multi-agent orchestration, came out of the AutoGen and Semantic Kernel merger. Each chapter is fast adoption of a new AI capability the moment it lands."

**The point of the triangle:**

> "These aren't sequential — they reinforce each other. Customer translation makes the AI depth useful. Learning velocity keeps both fresh as the stack changes. The role lives where all three meet."

**Transition out:**

> "Honest gap, honest plan."

---

## Slide 12 — Honest Gap & Ramp

**Setup — open with the receipt:**

> "Before I walk the plan, one thing to flag: I haven't been waiting for this interview. I built a public knowledge base specifically on Microsoft Modern Work — nine sections, from identity and Zero Trust through Copilot, Power Platform, security and compliance, business case, and interview prep itself. It's live at **jazz-knowledge-management.pages.dev**. The ramp's already started — this slide is the forward plan from where I am now. Here's the gap and how I close the rest."

**Point at the gap card — be direct:**

> "Three real gaps. Intune policy authoring + Autopilot at enterprise scale. Native Defender for Endpoint operations plus Defender XDR signal correlation. And the Modern Desktop / M365 admin cert track depth. I've worked the Azure layer underneath all of this — identity, security, governance — but not the M365 admin layer at AIBS depth."

**Point at the timeline — walk it:**

> "First 20 days: Entra ID plus Conditional Access. Identity foundation. Closest to my existing Azure security work — this is translation, not learning from scratch. CA policies, MFA, device-state signals, the policy precedence model."

> "Days 20 to 40: Intune plus Autopilot. The endpoint layer — configuration profiles, compliance policies, app protection, enrollment workflows, Autopilot configuration for mixed-fleet provisioning."

> "Days 40 to 60: Defender for Endpoint. Threat protection on top of the foundation. Attack surface reduction rules, automated investigation, plus Defender XDR for cross-signal correlation. The AI layer infused via Security Copilot fits here too."

**The right card:**

> "Five Azure certs accelerate the Microsoft stack ramp because the Azure platform underneath is shared. Eleven-cert track record proves I close gaps fast — on the job, not in theory."

**Footer line:**

> "Same engine that produced 11 certs. Different stack."

**Transition out:**

> "That's the deck. One closing slide."

---

## Slide 13 — Closing

**Setup:**

> "Translating AI capability into enterprise outcomes. That's the work I've been building toward."

**Point at the QR:**

> "QR code on the left — scan with your phone for the full project archive at jazzlien.com. Projects, blog, and guides. Everything I just walked through plus a lot more."

**Closing line — pause, eye contact:**

> "Happy to take questions on any slide. Where do you want to go?"

---

# Microsoft-stack Q&A — refresh tonight

**Q: "Walk me through how you'd assess a customer's Modern Workplace posture."**
Frame: *Identity layer first (Entra ID + Conditional Access), device layer (Intune compliance + Autopilot enrollment), app layer (managed apps + protection policies), threat layer (Defender for Endpoint + ASR rules), then governance (reporting, audit, retention). Prioritize gaps by risk × effort.*

**Q: "How does Zero Trust differ from traditional perimeter security?"**
Frame: *Perimeter assumes trust inside the network. Zero Trust assumes breach and verifies every request. Three principles: verify explicitly, least privilege, assume breach. Identity becomes the new perimeter. Conditional Access is the policy engine that ties it together.*

**Q: "What's the difference between MDM and MAM in Intune?"**
Frame: *MDM = device-level management for company-owned devices. MAM = app-level management for BYOD scenarios where you don't enroll the device but protect company data inside specific apps. App protection policies enforce things like preventing copy-paste from Outlook to personal apps. Most enterprises use a mix.*

**Q: "How would you handle a Copilot for M365 rollout for a 5,000-seat enterprise?"**
Frame: *Same playbook as GitHub Copilot rollout, scaled. Pre-rollout assessment of data governance posture (DLP, sensitivity labels — Copilot for M365 inherits whatever you've set up). Pilot group of 50–100 with measurable use cases. Bilingual change management materials. Phased license expansion. Adoption metrics tied to specific scenarios (email drafting, meeting summarization, document Q&A), not generic "engagement."*

**Q: "Talk about a time you led a complex Microsoft technology rollout."**
**Slide 7 is your evidence here.** Frame: *Pre-rollout demo + seat assignment + IDE-side configuration + bilingual deployment guides + change management for a non-AI-native dev org. Different SKU than M365, same playbook.*

**Q: "Why are you applying for this when your background is GCP?"**
Frame: *"Two answers. One — five Azure certs from my time at 展碁國際 cover the platform layer underneath M365: identity, networking, security. Two — Microsoft is embedding AI into every layer of the Modern Workplace stack. The candidate who understands both the endpoint platform AND the AI layer being grafted onto it is the candidate enterprises will need over the next three years. I'm betting on that intersection."*

**Q: "What's your weakness for this role?"**
Honest: *"My direct hands-on Intune policy authoring isn't at the depth of someone who's done five 5,000-seat deployments. What I bring is the architecture pattern and consulting discipline plus 5 Azure certs that already cover the identity, security, and governance layers underneath. Specific Intune depth I close on the job — same way I closed 11 certs while delivering customer work."*

**Q: "What if the client wants to know about Copilot Studio specifically?"**
Frame: *Copilot Studio is the **low-code** layer of Microsoft's agent stack — conversational topics, Power Automate flows, connectors, knowledge sources. Sits above Microsoft Agent Framework (MAF, the pro-code SDK that came from AutoGen + Semantic Kernel). For most enterprise customers Copilot Studio is the right tool — citizen developers can build first agents in a week. For complex multi-agent orchestration you drop down to MAF on Azure AI Foundry. The pattern parallels what I designed for the gaming customer on Vertex AI + ADK: same orchestrator-plus-tools-plus-knowledge model, different runtime. Microsoft's edge: native connectors into M365 Graph, Dataverse, Power Platform, and unified identity through Entra ID — all without extra integration work.*

---

# Likely questions from Frank (strategic angle)

Each question below has: **Frame** (what they're really testing), **Say this** (full script in your voice), and **Watchpoint** (the trap to avoid).

---

### Q1: "Where do you see AI consulting going? Why this practice, why now?"

**Frame:** They want a POV on the market, not a recitation of facts. Show you've thought about it independently.

**Say this:**

> *"Three waves overlapping right now. Wave one — productivity Copilots like Copilot for M365. Already in deployment, easy adoption curve, customers buying it. Wave two — agentic workflows. What Copilot Studio enables in earnest over the next 18 months. Replacing process work that used to need humans or rigid RPA. Wave three — vertical AI on foundation models. Healthcare, retail, finance, custom-built on Azure OpenAI for industry-specific outcomes.*
>
> *Microsoft is uniquely positioned because no other vendor has the productivity stack, the platform layer, the security backbone, and the AI orchestration under one roof. AI Business Solutions sits at that intersection.*
>
> *Why now: AI capability is moving faster than enterprise adoption. The people who can translate capability into ROI'd, scoped, secured deployments are the differentiator over the next three years. That's the work I've been preparing for."*

**Watchpoint:** Don't list Microsoft products like a brochure. Frame the WAVES first (industry-level), then position Microsoft inside them. Showing you understand the *market* matters more than showing you read the product page.

**If pushed:** *"Where I think it goes wrong: enterprises trying to do agentic AI at scale without solving the foundational data and identity governance first. Customers will pay AI Business Solutions consultants to NOT skip the boring layers. That's where consulting is durable, not just an implementation handoff."*

---

### Q2: "How do you think about building consulting capability — yours and others'?"

**Frame:** Frank's actual job. He wants to know if you can scale yourself and others. The best answer connects personal practice to team practice.

**Say this:**

> *"Two layers, same system. For myself, I treat learning as a system, not a series of heroic moments. The Claude Code Workflow open-source project is the most concrete proof — documented decision frameworks, shared knowledge base, handover protocols. That's how I closed 11 cloud certs while delivering customer work. The system is repeatable, not heroic.*
>
> *For others — same instinct. About 10 colleagues at CloudMile have adopted some version of that workflow across engineering, sales, and pre-sales. Pattern: write the playbook so the next person doesn't have to rediscover it.*
>
> *For the AI Business Solutions practice specifically, I wouldn't propose methodology changes until I've spent 60–90 days on real engagements. Once I've seen the gaps in how the practice scales, then standardized cost estimation, reusable architecture patterns, and peer-learning protocols become real proposals — not abstractions."*

**Watchpoint:** Don't promise to "build methodology" in the first month. Frank knows that's the rookie answer. The pro move is "I'd earn the right to propose changes by doing the work first."

---

### Q3: "Show me a customer engagement where you owned the outcome end-to-end."

**Frame:** Standard STAR-style question. They want concrete ownership — start to finish — not just one phase.

**Say this — lead with the Microsoft Copilot rollout (it's relevant AND end-to-end):**

> *"The Microsoft GitHub Copilot rollout at 展碁國際 in 2024. I owned it end-to-end. Set up the initial enterprise demo from scratch — seat assignment, IDE integration on JetBrains and VS Code. Trained the sales engineers and customer-facing teams on the capability story and the compliance posture. Published bilingual deployment guides — English Medium and Traditional Chinese industry blogs — so customers could deploy themselves.*
>
> *The outcome: the PM team launched a new product line around AI-assisted dev services. Different revenue category than the infrastructure resale we usually did.*
>
> *That's the loop — capability assessment, internal enablement, customer-facing documentation, productized offering. I owned every layer, including the change management I did in Chinese for sales teams who'd never sold AI before."*

**Watchpoint:** Don't lead with the gaming client (slide 3). The honest answer is you OWNED the proposal, not the delivery — the client built it themselves. That's a valid consulting outcome but it's not what "end-to-end ownership" means in this question.

**If they ask for a second example:** *"On the AI architecture side, the gaming client multi-agent engagement on slide 3. I owned discovery through architecture proposal. The client elected to build in-house — which is a valid consulting outcome. I owned the work; they owned their execution choice. Both forms of ownership matter, just at different scopes."*

---

### Q4: "Cultural fit — growth mindset, customer obsession, how you handle being wrong."

This is Microsoft's stated values. Could come as one big question or three separate ones. Have all three ready.

**On growth mindset:**

> *"Most concrete example — the move from foreign languages to tour leader to QA to Azure cloud to GCP. I didn't have a CS degree. Continuing education, first Azure role at 展碁國際, then 5 Azure certs while delivering customer work, then jumped to GCP at CloudMile and earned 6 more. Each move was uncomfortable — new stack, new mental model, new customer type. The discomfort is the signal you're learning. Growth mindset isn't a value I subscribe to; it's how I've made every career decision."*

**On customer obsession:**

> *"The gaming client engagement on slide 3 is the best example. Multi-agent architecture, full proposal, and they elected to build in-house. The ego move would be to push for the deal or argue against their decision. Instead I made sure the proposal was clear enough that they could execute without me. The customer's outcome is the goal, not my outcome. If they get to AI value without me, that's still a win."*

**On handling being wrong:**

> *"Specific recent example: my first multi-agent cost estimate. I quoted as if it was 1× LLM call. It's actually 2-3× because the orchestrator plus the worker agents each consume tokens independently. Caught it before the proposal went out, but it was a real modeling mistake.*
>
> *What I did: admitted it to my team, documented what I missed in the cost framework, and now 'how many LLM calls does the orchestration actually require' is a question I always ask early. Wrong isn't fatal; not noticing wrong is. The fix is making the lesson available to the next person."*

**Watchpoint:** Avoid platitudes. Microsoft penalizes generic value-language harder than they reward it. Every answer needs a specific story attached.

---

### Q5 (bonus): "What's your career trajectory? Where do you want to be in 3 years?"

> *"Principal level on the technical track, leading complex AI engagements end-to-end. Not interested in management for management's sake — interested in leading the work, mentoring others, and building practice methodology. The Claude Code Workflow system is a small example: I figured out a way to scale myself, then I documented and shared it. That instinct applied to consulting practice is what I'm aiming at."*

---

### Q6 (bonus): "Microsoft has six core values. Pick one and tell me about a time."

Default pick: **customer obsession.** Use the gaming client story (see Q4 above). Safe, lands well.

If you want to be slightly bolder: **growth mindset** with the career-trajectory story (Q4 above). Slightly more memorable because it's about you, not about a client.

---

### Q7 (bonus): "What would you build for the AI Business Solutions practice in your first 6 months?"

> *"Nothing for the first 60-90 days. I'd be on customer engagements, watching where the practice has friction, where consultants reinvent wheels, where outcomes vary based on the consultant rather than the method. Then, if I see the gaps clearly, I'd propose standardized cost estimation — what we showed on slide 5 — reusable architecture patterns documented across engagements, and a peer-learning protocol. Same idea as my Claude Code Workflow but applied to consulting capability. Earning the right to propose by doing the work first."*

---

# Likely questions from Kanwartej (technical angle)

Same format: **Frame**, **Say this**, **Watchpoint**, **If pushed**.

---

### Q1: "Walk me through how you'd actually design X for client Y."

**Frame:** Generic technical design question. Pick a concrete sample (Conditional Access, Intune rollout, etc.). The structure matters more than the topic — Kanwartej is testing whether you have a repeatable design discipline.

**Use this structure every time:**
1. **Discovery first** — what's the problem, constraints, current state
2. **Layered design** — never one monolithic solution
3. **Edge cases** — show you've done this for real
4. **Phased rollout** — never one-shot

**Sample script (Conditional Access for a 5,000-user enterprise):**

> *"Start with discovery. Who are the user populations, what apps do they access, what's the current identity state — hybrid AD or cloud-only — and what compliance requirements drive the policy decisions.*
>
> *Then layered design. Layer one — baseline: require MFA for all users, block sign-in from unmanaged devices for sensitive apps. Layer two — segmented by population: frontline workers get device-compliance via Intune, knowledge workers add named-location and risk-based controls, admins get the strictest — Privileged Identity Management, dedicated devices. Layer three — exceptions: emergency-access accounts excluded with full audit, break-glass procedure, app-specific bypasses for legacy systems.*
>
> *Edge cases I'd watch: legacy app passwords that need migration to modern auth, B2B guest user scenarios, and the priority order if multiple policies apply — Conditional Access is additive, overlapping requirements stack cumulatively. Test that.*
>
> *Rollout: pilot 50 users in IT for two weeks. Then helpdesk plus finance. Then frontline. Each wave fixes the gaps in the previous one."*

**Watchpoint:** Don't dive into a specific Microsoft product without first hearing the question. If they say "design X," ASK what X is. If they're vague, lead with the structure (discovery → layered → edge cases → phased) using your strongest example.

---

### Q2: "What would you configure first? What edge cases would you watch?"

**Frame:** They want to know if you've actually done this — the "first config" question reveals real experience, and edge cases reveal expertise.

**Sample script (Intune rollout, since it's the most likely Modern Workplace setup):**

> *"For Intune specifically, the enrollment profile is first. If enrollment isn't right, nothing downstream matters. Enrollment restrictions by platform — block personal jailbroken devices, allow specific OS versions. Enrollment notification language — Chinese plus English for Taiwan enterprises. M365 admin auto-assignment so newly enrolled devices pick up the baseline immediately.*
>
> *Edge cases I watch: BYOD users on personal Apple IDs — Apple's Personal Information separation needs explicit consent flow. Users with multiple devices — per-user device limits in Entra ID. Failover behavior when Intune's tenant connector is unhealthy — devices should NOT lose access because Intune is having a bad day; the fallback must be defined.*
>
> *And the silent killer in real deployments: app deployment conflicts when Win32 apps and store apps target the same software with different versions. That's the bug that breaks helpdesk's faith in the tool. Always check the supersedence rules before rolling out apps at scale."*

**Watchpoint:** "Always check" and "I watch for" signal experience. Hedging like "I'd probably check" or "presumably" signals you're guessing. Even if you ARE guessing, don't sound like it. Frame as discipline, not uncertainty.

---

### Q3: "How does that translate to Copilot Studio / Power Platform / D365?"

**Frame:** The "translate your AI work to Microsoft" question. Critical because you're coming from GCP. Show clean translation muscle — and be precise: ADK does NOT translate to Copilot Studio directly. ADK translates to **Microsoft Agent Framework (MAF)**.

**Say this — start by correcting the framing if needed:**

> *"Quick clarification on the equivalents — ADK doesn't translate directly to Copilot Studio. It translates to **Microsoft Agent Framework — MAF** — which is Microsoft's pro-code SDK for multi-agent orchestration. MAF came out of the AutoGen and Semantic Kernel merger in 2026; supports .NET and Python; runs on Azure AI Foundry Agent Service for managed hosting — that's the equivalent to Vertex AI Agent Engine. Copilot Studio sits above MAF as the low-code conversational surface; M365 Agents SDK is the toolkit for agents inside Teams and Copilot for M365.*
>
> *So three direct translations:*
>
> *ADK orchestration → MAF. Both are pro-code multi-agent frameworks. ADK is event-driven and strongly typed; MAF is conversational plus workflow orchestration. The orchestrator-plus-tools-plus-knowledge pattern maps cleanly.*
>
> *Vector DB + RAG → Azure AI Search plus Microsoft Graph. Where I'd use Pinecone or Vertex AI Vector Search on the GCP side, Microsoft gives you Azure AI Search with embeddings, plus grounding into Microsoft Graph for tenant-specific content.*
>
> *Custom AI agents → MAF for pro-code, Copilot Studio for low-code, Dataverse for the data layer. The agent-data-action pattern is the same; data layer changes from Firestore to Dataverse.*
>
> *Where Microsoft clearly pulls ahead: identity is unified through Entra ID, and the connectors into M365 Graph, Dataverse, and Power Platform are first-class. Don't have to build the integration layer — it's there."*

**Watchpoint:** This is the answer that proves you've done your homework. The PRO move is correcting the question framing — naming MAF as the direct ADK equivalent (NOT Copilot Studio) signals you actually know the Microsoft agent stack. Then walking through the full hierarchy: MAF → Azure AI Foundry Agent Service → Copilot Studio → M365 Agents SDK.

**If pushed on MAF specifically:** *"I haven't built in MAF in production yet, but the architecture maps cleanly from ADK. Both are pro-code multi-agent. ADK is event-driven and strongly typed; MAF is conversational plus workflow. Coming from ADK, I'd start with MAF's chat completion agents — the closest analog to ADK's agent loops — then graduate to MAF's workflow orchestration where the enterprise-integration benefits through Azure AI Foundry kick in. My knowledge base has the architecture; the hands-on gap closes in week one of the ramp."*

---

### Q4: "Where's the line between 'AI architect' and 'Microsoft Modern Workplace consultant'?"

**Frame:** Self-positioning question. They want to see if you understand the role boundary and can place yourself honestly inside it.

**Say this:**

> *"Three differences in framing.*
>
> *Scope: AI architect designs the agent and orchestration layer. Modern Workplace consultant covers the broader stack — identity, endpoints, productivity, security — with AI as one layer integrated on top.*
>
> *Audience: AI architect typically interacts with technical buyers, CTOs, lead engineers. Modern Workplace consultant interacts with IT leadership, change management, and end users of the productivity tools themselves.*
>
> *Mode: AI architect builds something new. Modern Workplace consultant integrates AI into something existing. Different value proposition entirely.*
>
> *For this role, I'd land closer to Modern Workplace consultant. The AI architect skills are my differentiator, but the actual job is integrating AI into customers' existing M365 and Defender stack — not designing greenfield AI systems. I'm comfortable on both sides; the line is whether AI is the product or the layer."*

**Watchpoint:** Don't claim to be both equally. The honest answer is that you're stronger on the AI architect side and ramping into the Modern Workplace side. Pretending otherwise weakens the slide 12 gap-and-ramp honesty you've already established.

---

### Q5 (bonus): "Tell me about your most technically ambiguous customer problem."

> *"The gaming client. The ambiguity was: was this a chatbot problem or a knowledge-management problem? My first instinct said 'agent stack.' But I challenged it — the deeper issue was knowledge institutionalization. Attrition kept resetting service quality every few months because the knowledge lived in DOCX and PPT, not in a system. The architecture had to be multi-agent with explicit knowledge layers, not a single LLM call. The technical decision was downstream of the right problem framing. If I'd built what they originally asked for, they'd still have the underlying problem."*

---

### Q6 (bonus): "How would you migrate a 3,000-Windows-device customer from on-prem AD to Entra ID + Intune?"

> *"Discovery first. What's the Configuration Manager footprint — SCCM/MECM, or already in transition? Hybrid join versus cloud-only target? Co-management strategy or full cutover?*
>
> *Segment by use case: knowledge workers, frontline, developers. Different Intune profiles, different rollout cadences. Developer machines need different policies than kiosk-style frontline devices.*
>
> *Phase the rollout: pilot 50 devices, measure compliance and helpdesk ticket impact, then the next 250, etc. Identity migration runs in parallel — Entra Connect for the hybrid phase, then cutover.*
>
> *Watchpoints: GPO-to-Intune policy translation gaps, legacy apps that need IIS or COM registration, and the helpdesk's response time during transition. That's the metric that tells you the rollout is working or burning trust."*

---

### Q7 (bonus): "What technical mistake have you made recently?"

> *"Underestimated orchestration overhead in early multi-agent cost estimates. Quoted as if it was 1× LLM call. It's actually 2-3× because the orchestrator plus the worker agents each consume tokens independently. Caught it before the proposal went out, but it was a real modeling mistake. Now every multi-agent design starts with explicit agent topology and token-per-turn estimation. You cannot multiply average query volume by token cost in isolation — you have to model the agent shape."*

---

# Likely questions from Sol Lee (Friday — architecture + DevOps angle)

Sol is the deepest technical interviewer. Same format, but answers go further into engineering rigor — system design, DevOps practices, observability, distributed state.

---

### Sol Q1: "Walk me through the system design behind your multi-agent architecture."

**Frame:** This isn't slide 4's surface walkthrough — Sol wants the *engineering* design. Tool choices, tradeoffs, state, failure modes.

**Say this:**

> *"At the surface it's the slide 4 diagram — Root Agent dispatching to RAG agents and Task agents, Model Armor gating LLM calls. Underneath:*
>
> *State distribution — agents are stateless; conversation state lives in a session store keyed by user. For Vertex AI + ADK we used Firestore; on the Microsoft side that's Dataverse or Cosmos DB depending on access patterns. State is short-term in agent memory and long-term in the vector DB. Identity-bound through user tokens — agent never sees raw credentials.*
>
> *Tool exposure — task agents call internal APIs through an API gateway. Rate-limited per tenant, auth via Entra ID equivalent. Tools are versioned because the LLM contract changes as the prompt evolves.*
>
> *Failure modes — orchestrator timeout fallback, RAG retrieval miss returns explicit 'I don't know' instead of hallucination, Model Armor blocks become user-visible error states with human-escalation path.*
>
> *Cost ownership — every agent call tagged with a session ID and an agent ID; we can attribute spend to specific user journeys, not just monthly aggregate."*

**Watchpoint:** Sol has built $2.8M production systems. He'll hear hand-waving immediately. The specifics — Firestore vs Cosmos DB, Entra ID for auth, session-tagged cost attribution — are what separate "I've designed this" from "I've imagined this."

---

### Sol Q2: "How would you CI/CD a multi-agent system?"

**Frame:** Sol ran a DevOps Dojo. He cares HOW you ship, not just what.

**Say this:**

> *"Five layers, treating agents as code.*
>
> *One — source control everything: agent definitions, prompts, tool schemas, configuration. The Claude Code Workflow open-source system I built is the personal version of this discipline. Everything is in markdown or YAML, versioned, diffable.*
>
> *Two — CI: unit tests on tools (the deterministic part — does the SQL query return the right shape?), prompt regression tests (golden examples that should still pass), and schema validation. CI breaks if a prompt change degrades the golden set.*
>
> *Three — integration tests: end-to-end agent loops against a sandbox environment. These are slow and expensive (each test costs tokens), so run them on PR merge, not every commit.*
>
> *Four — staging deployment with shadow traffic. Real customer queries hit both prod and staging; staging output is logged but not returned to the user. Compare outputs, catch regressions before prod.*
>
> *Five — observability: every agent call instrumented for latency, token cost, tool invocations, and quality signals — thumbs up/down or downstream task completion. LangSmith or Azure Application Insights on the Microsoft side.*
>
> *Blue-green deployment for the orchestrator. Canary rollout for prompt changes."*

**Watchpoint:** Don't claim production CI/CD for multi-agent if you haven't done it. Frame as: *"This is how I'd architect it; the closest production CI/CD I've run is for the AI products on the side, which use a simpler version of this pattern."*

---

### Sol Q3: "How do you handle state in distributed agents?"

**Frame:** Sol uses Dapr in his banking work. State management in distributed systems is his territory. Show you've thought about it.

**Say this:**

> *"Three layers of state.*
>
> *Conversation state — short-term, lives in the agent process or a fast key-value store. Session-scoped, expires after user inactivity. On Microsoft side, Dapr's state management building block is the right fit — same pattern Sol may have used for the CDFH banking project.*
>
> *Memory state — long-term, what the agent remembers across sessions. Vector DB or graph DB depending on retrieval patterns. Embeddings indexed; recall ranked by relevance + recency.*
>
> *Configuration state — agent definitions, tool registrations, prompt templates. Source-controlled, deployed through CI/CD. Not stored in the agent at runtime — fetched at startup.*
>
> *The critical pattern: agents are stateless processes. State lives in the platform, not the agent. That's what makes horizontal scaling work — you can lose any agent instance without losing user context."*

**Watchpoint:** Calling out Dapr by name signals you've done your homework on his work. Don't force it if the question doesn't fit, but if state distribution comes up — name it.

---

### Sol Q4: "Tell me about cost-optimizing an AI workload. What levers did you pull?"

**Frame:** Sol did this for FamilyMart's Azure ML order prediction. He'll relate to specifics.

**Say this:**

> *"Slide 5 covers the framework — bottom-up plus top-down. The biggest lever in practice is model selection. For a customer service bot at 10K queries a day, dropping from a flagship model to a mid-tier model is a 60-80% cost reduction with often <10% accuracy drop on routine queries. The trick is segmenting query types and routing — frontline queries to the cheap model, edge cases to the flagship.*
>
> *Second lever is orchestration efficiency — multi-agent setups stack 2-3× a single LLM call. Sometimes consolidating two agent steps into one prompt halves the cost without losing quality. That's a refactoring exercise — review the agent topology after a month of production data.*
>
> *Third lever is caching — semantic caching for frequent queries that have the same intent. Even 20% cache hit means 20% inference savings.*
>
> *Fourth lever is right-sizing the infrastructure underneath — vector DB capacity, gateway throughput, log retention. These add up when LLM costs aren't dominant.*
>
> *The discipline I bring is doing this BEFORE the customer asks. Slide 5's framework is exactly that — cost discipline at design time, not after the bill shock."*

**Watchpoint:** Sol's FamilyMart experience means he knows the real numbers. Don't make up specific figures unless you've actually run them. The framework is defensible without specific numbers.

---

### Sol Q5: "What's your API management story for agent endpoints?"

**Frame:** API management is his expertise area. Don't reinvent — show you know the standard patterns.

**Say this:**

> *"Gateway pattern. Azure API Management — or Apigee on the GCP side — fronts the agent endpoints. Three jobs.*
>
> *One — auth and tenant isolation. Entra ID for identity, JWT validation at the gateway, tenant context propagated downstream. Per-tenant rate limits prevent one customer from starving another.*
>
> *Two — observability. Every request tagged, latency tracked, errors aggregated. Application Insights downstream for the deep-dive view.*
>
> *Three — versioning and rollback. Agent capabilities evolve fast; the gateway lets you route v1 of a tool to old agents while v2 rolls out, no downtime.*
>
> *For tool exposure specifically — agents call internal APIs through the same gateway as external traffic. Same security model, same observability. Tools don't get a backdoor."*

**Watchpoint:** Sol may push deeper here — "how would you handle async tool calls?" or "what about WebSocket vs REST for the agent-to-tool layer?" If pushed, be honest about what you've designed vs implemented. The framing is the strength; specific implementation details for systems you haven't built — say so.

---

### Sol Q6: "How do you handle compliance — say, banking or healthcare — in an AI architecture?"

**Frame:** Sol has built for CDFH (banking, regulated) and SKMH (healthcare). He knows the standard. Don't claim experience you don't have.

**Say this:**

> *"Three areas if I'm honest about what I've done versus what I've designed.*
>
> *Data flow controls — what data the agent can see, what data it can return. Sensitivity labels on Microsoft side, DLP policies, output filtering through Model Armor or equivalent for PII redaction. For the gaming customer this was less critical; for banking or healthcare it's table-stakes from day one.*
>
> *Audit trails — every agent decision logged with context. Compliance teams need to reconstruct 'why did the system give this answer to this user at this time.' Tag every LLM call with session, agent, prompt version, model version.*
>
> *Model governance — version pinning, change approval, output validation. The model the customer signed off on cannot change without process.*
>
> *I'd be honest with the customer if I were stepping into banking or healthcare for the first time — I'd partner with someone who's done HIPAA or banking-specific work for the first project. Compliance is where consulting humility matters. Sol, you've done healthcare HIS at SKMH — I'd want to learn that pattern from someone who's lived it."*

**Watchpoint:** The "I'd want to learn from you" close is genuine and disarms. Sol will respect it. Bluffing on compliance is a disqualifier — be specific about what you've done versus what you've designed in principle.

---

### Sol Q7 (bonus): "What's your test automation approach for AI?"

> *"Three layers. Deterministic tests on tools — does the SQL query return the right shape, does the API call succeed with auth. Prompt regression tests — a golden set of inputs that should produce specific output shapes; LLM judges or string matching on key fields. End-to-end agent loops — slow, expensive, run on merge not commit. The hardest part is the prompt regression layer — quality drift is silent. Output that's slightly worse for two weeks before someone notices. I'd instrument the production system with quality signals — task completion, user thumbs-up, fall-back-to-human rate — and treat them as real-time test signals, not just observability."*

---

# Cultural cues — Microsoft expects these

**Growth mindset:** When you're wrong or don't know something, say so. Frame it as "I haven't done that specific thing — here's the adjacent experience and how I'd close the gap." Microsoft penalizes false confidence harder than admitted gaps.

**Customer obsession:** Every story should be framed by customer outcome. Even your personal project slide (8) — translate from "12 projects" to "I shipped a memorial video service that has paying users grieving customers actually use."

**One Microsoft:** Frank's team is "AI Business Solutions" — broader than this specific role. If asked about cross-practice work (security, infrastructure, modern work), express enthusiasm for collaborating across practice lines.

**Diversity & inclusion:** If it comes up, be specific not platitudinal. Example: "Published bilingual technical content because the audience needed it — not for points. Same instinct on team composition: diverse perspectives win because the problem space is multilingual and multi-industry."

---

# Cadence reminders

- **First 3 minutes** (slides 1–2): set who you are. Confident, brief.
- **Slides 3–5** (8–10 min): the meaty technical block. Architecture + cost. This is where Kanwartej will engage hardest. Be ready for cross-examination.
- **Slides 6–9** (5–7 min): track record. Evidence, not narration. Let the screenshots and numbers do the work.
- **Slides 10–12** (3–5 min): operating model + fit + ramp. Frank's angle. Drives toward close.
- **Slide 13** (1 min): hand it back to them with the QR code.

Total walkthrough if uninterrupted: ~22 minutes. In a 45-minute interview window, expect 15–20 minutes of deck + 25 minutes of conversation. Don't rush. If they go deep on slide 3, you may never reach slide 8 — that's fine. The deck is a buffet, not a meal plan.

---

# Morning-of checklist (before tomorrow)

**Tech setup:**
- Open `index.html` in your presentation browser. Test once. Don't fight tech at the start.
- Have the QR code visible — interviewers will scan it during or after.
- Print to PDF as backup — the HTML has been built for that.
- If interviewing remotely: share screen, not "share window" (avoids confusion if you alt-tab).

**90 minutes before:**
- Re-read the "Microsoft-stack Q&A" section above. Out loud if possible.
- Re-read the "Frank" and "Kanwartej" sections — visualize each one asking their questions.
- Glance at slides 5, 11, 12 specifically — these are the ones most likely to need precise language.
- Don't read the deck again — you've internalized it.

**5 minutes before:**
- Water. Speak slowly. Pause.
- Make sure you can introduce yourself in 30 seconds. Practice it once.
- Remember: this is a conversation, not a recital. They want to like you.

**During:**
- When in doubt, ask: *"Want me to keep going, or zoom in on this?"*
- If you don't know something, say: *"I haven't done that specific thing. Here's the adjacent experience I'd bring."*
- If they push back: thank them for the challenge, then either defend with data or update your position. Don't dig in defensively.

**After:**
- Thank both interviewers by name. Quick handwritten or email follow-up within 24 hours referencing one specific thing they said. Personal, not corporate.

Go.
