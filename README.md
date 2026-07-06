# The Knowledge–Action Chain (KAC)

**An AX Execution Ontology for Turning Validated Knowledge into Action, Outcome, and Learning**

*From knowledge flow to verified execution — a relational model linking skill derivation, runtime, action events, outcomes, review, and context feedback.*

- Author: **Ha Woo Sung (Ryo Ha)** — sopia19910@gmail.com
- Date: June 23, 2026
- Papers in this repository:
  - 📄 [English — Knowledge-Action Chain (KAC)]({EN%5D%20Knowledge-Action%20Chain%20(KAC).pdf)
  - 📄 [한국어 — Knowledge-Action Chain (KAC)]({KR%5D%20Knowledge-Action%20Chain%20(KAC).pdf)

---

> **Without KAC, knowledge is stored. With KAC, knowledge acts.**

In the age of AI, the core problem of organizational operation is no longer *"can AI produce an answer?"* — generative and agentic AI already draft documents, retrieve information, analyze, and execute tools. The real question is whether **validated knowledge** is derived into a specific **Skill** within a domain, compiled into an executable **Runtime**, produces an actual **ActionEvent** with distinct **Output** and **Outcome**, and passes **Review** and **Feedback** to update the organization's domain context. This paper defines that entire structure as the **Knowledge–Action Chain (KAC)**.

The central thesis: **a knowledge chain is a path of knowledge; a knowledge–action chain is the path along which knowledge is verified through action.**

## The Basic Path

```
Knowledge Chain_ext  →  Skill Derivation Chain  →  SkillRuntime  →  ActionEvent
        →  OutputObject  →  OutcomeObject  →  Review  →  Feedback  →  Context Update
```

As an object-form equation, KAC is a **nine-tuple**:

```
KAC = ⟨ KC_ext, SDC, R, A, P, Ω, V, F, DC_D(t+1) ⟩          (Eq. 1)
```

| Symbol | Component | Symbol | Component |
|---|---|---|---|
| `KC_ext` | External Knowledge Chain | `Ω` | OutcomeObject (verified change) |
| `SDC` | Skill Derivation Chain | `V` | Review |
| `R` | SkillRuntime (execution contract) | `F` | Feedback |
| `A` | ActionEvent (execution event) | `DC_D(t+1)` | Updated domain context |
| `P` | OutputObject (artifact) | | |

## Three Structures That Must Not Be Confused

| Structure | Core question | Role |
|---|---|---|
| **External knowledge chain** (`KC_ext`) | Where does knowledge come from; how is it connected, stored, shared, applied? | Knowledge flow |
| **Skill derivation chain** (`SDC`) | Why does a given Identity/Entity require a given Skill? | Knowledge → skill requirement (`Identity → Goal → Task → Knowledge → Method → Skill`) |
| **Knowledge–action chain** (`KAC`) | Did the derived Skill come alive as Runtime, Action, Outcome? | AX execution, verification, learning |

`Identity → … → Skill` is crucial, but by itself it is **not yet action** — it only justifies a skill requirement. KAC covers everything up to the moment that Skill actually enters the operational world.

## Key Concepts

### Prerequisite gate — Domain Context and DCI
KAC is not free-floating. A domain context (`DC_D = Instantiate(CCS, D)`, where **CCS** is the nine-slot Common Context Structure ⟨Purpose, Meaning, Situation, Criteria, Role, Limit, Source, Format, Feedback⟩) must first pass **DCI (Domain Context Integrity)** — a gate-first consistency verification, not a performance score. Fatal defects (absent owner, absent authority, ingested sensitive data, unspecified human accountability) cannot be compensated by a high quality score. **ValidKAC begins only after the domain context passes DCI.**

### SkillRuntime — the pivotal transition
A Skill is not execution but an **execution requirement**. The SkillRuntime compiles a derived Skill into an **execution contract** from which an actual ActionEvent can occur:

```
SkillRuntime = SkillInterface + InputContract + OutputContract + SourcePolicy + ToolPolicy
             + Guardrail + ValidationRule + TracePolicy + ApprovalPolicy + WorkflowSpec
             + InvocationContract + StateModel + ReleasePolicy                    (Eq. 6)
```

### Output ≠ Outcome
An **OutputObject** is the artifact produced (e.g., a customer-response draft); an **OutcomeObject** is the verified change it caused (inquiry resolved, re-inquiries reduced, no policy violation). Many AI deployments stop at artifact generation — KAC asks not *"what did AI produce?"* but *"what change did it produce, and was that change verified?"*

### Review → Feedback → Context Update
An Outcome must pass **Review** (authority, accountability, source, grounds, criteria, approval, records, risk — concretized by RCI). A passing result becomes **Feedback** — not an opinion but a *context change candidate* with evidence, scope, owner, approval status, and rollback plan. Approved feedback creates `DC_D(t+1)`, which must pass **DCI again**. This closes KAC into an **organizational learning cycle**.

### ValidKAC — nine validity conditions
```
ValidKAC = ValidKC ∧ ValidSDC ∧ RuntimeReady ∧ ValidAction ∧ ValidOutput
         ∧ ValidOutcome ∧ ReviewPassed ∧ FeedbackValid ∧ ContextRevalidated   (Eq. 11)
```
Any single failing segment collapses the chain — KAC is completed only when knowledge, skill, execution, output, outcome, review, feedback, and context update **all** hold.

## The Operating Metrics

| Metric | Role |
|---|---|
| **DCI** | Verifies the reference environment (domain context integrity) — the prior gate |
| **KCDI** | Measures field deployment success of the Skill (six multiplicative factors) |
| **RCI** | Verifies reflectability of artifacts and utterances at Review |
| **AHCI** | Measures human–AI augmentation capability (1:1 collaboration) |
| **ARBI** | Measures collaborative role balance (AI-mediated collaboration) |

## The Integrated Cycle

```
CCS → DC_D → DCI → Identity-based knowledge chain → ValidDerivation → ValidDeployment
    → SkillRuntime → ActionEvent → OutputObject → OutcomeObject
    → KCDI / AHCI / ARBI / RCI → Feedback → DC_D(t+1) → DCI Revalidation
```

When this cycle closes, the organization has not merely *used* AI — it has **accumulated AI execution results as organizational knowledge and criteria**.

## Worked Example — Customer Service

| KAC element | Example |
|---|---|
| `KC_ext` | Product policy, refund rules, customer history, legal criteria, FAQ |
| `SDC` | CustomerSupportAgent → CustomerIssueResolution → IssueClassification → ProductPolicyKnowledge → ResponseFramingMethod → Policy-grounded Response Skill |
| `SkillRuntime` | Input: customer inquiry / Sources: FAQ, terms / Guardrail: no legal advice / Approval: human approval for refunds |
| `ActionEvent` | AI classifies the inquiry and generates a response draft |
| `OutputObject` | A customer response draft with linked grounds |
| `OutcomeObject` | Inquiry resolved, re-inquiries reduced, no policy violation |
| `Review` | RCI reviews grounds, authority, accountability, expression, approval |
| `Feedback` | "Refund exception criteria are ambiguous" registered as a change candidate |
| `DC_D(t+1)` | Refund criteria updated in the customer-service domain context |

## Companion Framework Papers

KAC operates alongside a family of organizational-AX research papers (unpublished manuscripts, 2026):

- **[R1]** Development and Deployment of an Identity-driven Skill Derivation Knowledge Chain
- **[R2]** Knowledge-Chain Deployment Index (KCDI)
- **[R3]** Review Communication Integrity (RCI v3.0)
- **[R4]** Common Context and Governance Context
- **[R5]** Augmented Role Balance Index (ARBI) · Augmented Human Capability Index (AHCI)
- **[R6]** A Common-Context-Based Integrated Cycle of AX Execution, Verification, and Learning · Domain Context Integrity (DCI)

---

*KAC is an applied execution ontology proposed by this framework; the verification criteria and coefficients of each segment are operational parameters to be calibrated with real domain data.*
