# RA‑1 v1.1 — Runtime Admissibility Standard  
Semantic Standards Authority (SSA)  
Version: 1.1  
Status: Active

---

## 1. Purpose
RA‑1 defines the **formal semantic structure** for agent actions, evidence, admissibility validation, delegation boundaries, antinomy resolution, and suspension states.  
Its purpose is to ensure that **every agent action is explainable, governed, and auditably admissible** before execution.

RA‑1 is the foundational runtime standard for semantic governance in agentic systems.

---

## 2. Core Concepts

### 2.1 Action Unit (AU)
An **Action Unit** is the smallest admissible execution step.

**Structure:**
- `au.id` — unique identifier  
- `au.actor` — agent or subsystem  
- `au.intent` — declared purpose  
- `au.inputs` — data, signals, or upstream outputs  
- `au.evidence` — structured evidence set  
- `au.constraints` — policy, risk, compliance, or domain constraints  
- `au.outcome` — expected result (pre‑execution)

An AU **cannot execute** until admissibility is validated.

---

### 2.2 Evidence Set (ES)
Evidence is formalized as a deterministic structure.

**Fields:**
- `es.id`  
- `es.source` — system, model, human, external API  
- `es.timestamp`  
- `es.confidence`  
- `es.materiality` — whether evidence materially affects decision context  
- `es.binding` — link to AU intent or constraints

Evidence must be **complete, traceable, and auditable**.

---

### 2.3 Delegation Boundary (DB)
Defines **what an agent is allowed to decide or execute**.

**Boundary types:**
- `DB-0` — no autonomous action  
- `DB-1` — constrained autonomous action  
- `DB-2` — domain‑bounded autonomy  
- `DB-3` — full autonomy with semantic governance

Delegation boundaries are enforced at runtime.

---

## 3. Admissibility Model

Admissibility is a **deterministic checkpoint** that validates whether an AU may proceed.

### 3.1 Validation Criteria
An AU is admissible only if:

1. **Context Validity**  
   - Inputs are consistent with current system state  
   - No contradictory evidence exists  

2. **Policy Validity**  
   - All constraints are satisfied  
   - Domain rules are respected  

3. **Evidence Validity**  
   - Evidence set is complete  
   - Material evidence is present  
   - No stale or superseded evidence  

4. **Delegation Validity**  
   - AU is within the agent’s delegation boundary  

### 3.2 Deterministic Evaluation Pipeline
1. Load AU  
2. Load evidence  
3. Evaluate constraints  
4. Resolve conflicts (if any)  
5. Determine admissibility  
6. Gate execution

If admissibility fails → AU **cannot** execute.

---

## 4. Antinomy Resolution

Antinomy = conflict between:
- agents  
- evidence sources  
- constraints  
- risk vs credit vs fraud signals  
- policy vs model output

### 4.1 Resolution Rules
1. **Semantic Priority**  
   Domain rules override model predictions.

2. **Materiality First**  
   Material evidence supersedes non‑material evidence.

3. **Temporal Priority**  
   Newer evidence overrides older evidence unless marked non‑material.

4. **Delegation Priority**  
   Higher delegation boundary agents override lower ones.

Antinomy resolution produces a **deterministic conflict‑free state**.

---

## 5. Suspension State (SS)

Suspension is triggered when **new material evidence** changes the decision context.

### 5.1 Suspension Triggers
- New fraud signal  
- New risk indicator  
- Updated policy  
- Updated constraints  
- Contradictory evidence detected  
- Upstream agent conflict

### 5.2 Suspension Behavior
When suspended:
- AU execution pauses  
- System re‑evaluates admissibility  
- Antinomy resolution re‑runs  
- Delegation boundaries re‑checked  
- Updated admissibility decision produced

Suspension ensures **safe, governed, context‑aware execution**.

---

## 6. Runtime Requirements

### 6.1 Determinism
All admissibility outcomes must be deterministic and reproducible.

### 6.2 Auditability
Every AU must produce:
- admissibility log  
- evidence log  
- conflict resolution log  
- suspension log (if applicable)

### 6.3 Explainability
Each decision must be explainable through:
- evidence  
- constraints  
- delegation boundaries  
- antinomy resolution  
- suspension triggers

---

## 7. Versioning
- v1.0 — initial release  
- v1.1 — formalization of admissibility pipeline, expanded antinomy rules, suspension triggers

---

## 8. Governance
RA‑1 is governed by the **Semantic Standards Authority (SSA)**.  
Updates follow SSA semantic governance procedures.

---


Evidence must be complete, traceable, and auditable.

### **3. Delegation Boundaries (DB)**
Defines what an agent is allowed to decide or execute.  
RA‑1 enforces delegation boundaries at runtime to prevent unauthorized actions.

---

## Admissibility Model

Admissibility is a **runtime checkpoint** that determines whether an AU may proceed.

An AU is admissible only if:
- context is valid,  
- constraints are satisfied,  
- evidence is complete and material,  
- delegation boundaries permit execution.

The admissibility pipeline is deterministic and reproducible.

---

## Antinomy Resolution

Antinomy = conflict between agents, evidence sources, constraints, or domain signals.

RA‑1 resolves conflicts using:
- semantic priority,  
- materiality rules,  
- temporal ordering,  
- delegation hierarchy.

This produces a conflict‑free state before execution.

---

## Suspension State

Execution is suspended when new **material evidence** changes the decision context.  
Suspension triggers a full re‑evaluation of:
- evidence,  
- constraints,  
- conflicts,  
- admissibility.

This ensures safe and context‑aware execution.

---

## Governance & Versioning

RA‑1 is governed by the **Semantic Standards Authority (SSA)**.  
Version 1.1 formalizes:
- the admissibility pipeline,  
- expanded antinomy rules,  
- suspension triggers,  
- deterministic runtime requirements.

---

## Repository Structure (Recommended)

