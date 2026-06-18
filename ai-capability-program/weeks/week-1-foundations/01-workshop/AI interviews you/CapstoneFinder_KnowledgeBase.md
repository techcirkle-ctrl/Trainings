# Capstone Finder — Knowledge Base
*(Upload this file to the Project. It grounds the interview: what a good capstone looks like, how to assign the AI stack layer correctly, and real example problems per function. Do not read this aloud to the user — use it to reason.)*

---

## 1. What makes a GOOD capstone problem

A good capstone is:
- **Specific, not a theme.** "Speed up month-end close" is a theme. "Draft the variance commentary for the month-end deck from the numbers and last month's notes" is a capstone.
- **Real and recurring.** It happens weekly or monthly, to a real person, and it's annoying or slow today.
- **Owned by this leader or their team.** They can actually deploy it and see the result.
- **Bounded.** One workflow, not a department transformation. It can be built in a few weeks.
- **Impactful if solved.** Saves meaningful time, reduces a real risk, or speeds a real decision.

A WEAK capstone is: too big ("transform our reporting"), too vague ("use AI in HR"), not owned by them, one-off (won't repeat), or trivial (saves five minutes a month).

When in doubt, steer them toward something they personally feel the pain of and could show a result on within a month.

---

## 2. The AI stack — assign the LOWEST layer that solves the core

These four are **composable capabilities on one engine**, not a ladder. Switch on only what the problem needs. Climbing higher than necessary is the most common and most expensive mistake.

- **LLM (plain).** Generate, rewrite, summarise, extract, classify, or reason over text the user supplies in the prompt. No access to outside documents, no actions. *Most capstones have a large LLM component.*
- **RAG (LLM + retrieval).** Answer from the organisation's OWN documents, pulled in at question time, with sources. Use when the task needs knowledge that lives in their files/policies/past work and isn't in the prompt. A RAG system is ~80% the quality of the documents behind it, 20% the model.
- **Agent (LLM + tools + a loop).** Given a GOAL (not a question), it has tools to take ACTIONS (search, email, query a system, update a record, run a calc), and it LOOPS — think → act → observe → decide — until the goal is met. Only truly agent-shaped if it takes actions in tools and loops.
- **Multi-agent.** Several specialised agents coordinated. Rarely the right answer for a first capstone — only when the work genuinely splits into distinct specialist roles.

**The three-part test for "is it really an Agent?"**
1. Is it chasing a GOAL, not answering a question?
2. Does it take ACTIONS in tools (not just produce text)?
3. Does it LOOP until done?
If it fails any of these, it is NOT an agent — it's an LLM or RAG task. Say so honestly.

**The governing rule:** the cheapest layer that works, wins. For every part, ask "what's the lowest capability that solves this, and why not the one above?"

---

## 3. How to decompose — most problems are a MIX

A real workflow is usually several parts at different layers. Don't force the whole thing onto one layer. Example pattern:
- pulling data from a system → Agent (takes an action)
- doing arithmetic / logic on it → LLM
- explaining "why" using past commentary → RAG (grounded in their notes)
- writing the summary → LLM

Notice how little is truly agent-shaped. That realisation is the point of the exercise.

---

## 4. Example problems by function (use as probes or fallbacks)

### Finance
- **Monthly vendor-spend variance note.** Pull spend by vendor, compare to budget, write the variance commentary for the leadership review. *(Mix: Agent to pull, LLM for the maths/write-up, RAG for prior-month context.)*
- **Contract terms extraction.** Pull payment terms, penalties, renewal/auto-renew clauses, SLAs from vendor contracts into a comparable table. *(Mostly LLM; RAG if comparing against a policy standard.)*
- **Vendor-quote reconciliation.** Normalise differently-structured quotes to a true like-for-like cost and flag hidden terms. *(LLM-heavy.)*
- **Audit-finding summariser.** Turn long audit findings into a tight leadership note with the actions and owners. *(LLM; RAG if drawing on prior findings.)*

### HR
- **Interview-note reconciliation.** Synthesise several interviewers' notes into one hiring recommendation, surfacing where they actually disagree. *(LLM; RAG if scoring against a competency framework in your docs.)*
- **JD generation from a messy brief.** Turn a hiring manager's rough requirement into a structured, consistent job description. *(LLM; RAG to match house style/levelling.)*
- **Policy Q&A for managers.** Answer "what does our policy say about X" from the actual HR policy library, with the source. *(RAG — classic case.)*
- **Exit-interview theme analysis.** Pull recurring themes and early-warning signals across exit interviews. *(LLM over supplied text; RAG if drawing on the archive.)*

### IT / Engineering / Product (this GCC builds & supports engineering software)
- **Engineering Change Request triage.** Read an incoming ECR, classify it, flag risk, route it, draft the first response. *(LLM + RAG on past ECRs; Agent only if it actually files/routes in a system.)*
- **Customer escalation triage.** Read a support escalation, pull the relevant product docs, draft a diagnosis and next step. *(RAG-heavy; Agent if it opens/updates the ticket.)*
- **Release-notes drafter.** Turn merged change logs into customer-readable release notes. *(LLM; RAG for product/terminology consistency.)*
- **Spec / requirements consistency check.** Check a new requirement against existing specs for conflicts. *(RAG — needs your own spec library.)*
- **Meeting-to-decisions tracker.** From meeting notes, extract decisions, owners, and deadlines and chase them. *(LLM to extract; Agent only if it actually sends the chase emails and loops.)*

### Cross-functional (any leader)
- **Status-report assembler.** Pull updates from several sources into the weekly leadership status. *(Agent to gather, LLM to write — or just LLM if they paste the inputs.)*
- **Inbox-to-actions.** Turn a pile of email into a prioritised action list with draft replies. *(LLM; Agent if it actually drafts in the mail system.)*

---

## 5. Data sensitivity — flag, don't block

When a workflow touches real internal content, name the data types that must NOT go into a public AI tool and must stay in the sanctioned workspace tool / account. Common sensitive types: supplier contracts and pricing, customer or employee PII, unpublished financials, source code, security details, anything under NDA. The rule is not "don't use internal data" — it's "use it only in the sanctioned tool, never a public chatbot."

---

## 6. Human-in-the-loop — name where authority runs out

For any workflow that could take an action with consequences (sending an external email, committing spend, making a customer promise, changing a record), identify the step where a human must approve before it acts. That approval point is the governance call the leader owns. The more consequential the action, the earlier the human checkpoint.
