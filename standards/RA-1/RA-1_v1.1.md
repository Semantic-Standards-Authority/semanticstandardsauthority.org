# RA‑1: Regulatory Antinomy Semantic Class Specification  
Semantic Standards Authority (SSA)  

**Version:** RA‑1 v1.1  
**Date:** 2026  
**Location:** United Kingdom  

---

## 1. Preamble

The RA‑1 semantic class defines a formal structure for representing regulatory antinomies, unresolved conflict states and jurisdiction‑specific constraint interactions. RA‑1 provides a deterministic, machine‑interpretable semantic model enabling systems to encode, evaluate and expose regulatory conflicts without attempting to resolve them.

RA‑1 is part of the Semantic Standards Authority’s academic semantic research framework and is not associated with any external proprietary architecture or governance structure.

---

## 2. Scope and Purpose

The purpose of RA‑1 is to establish a formal, machine‑readable representation of regulatory conflicts, including but not limited to:

- jurisdictional antinomies  
- contradictory obligations  
- mutually exclusive prohibitions  
- authority‑boundary collisions  
- unresolved regulatory states  

RA‑1 does **not** provide conflict resolution.  
It provides **conflict representation**.

---

## 3. Definitions

- **Regulatory Antinomy:** A legal conflict where two or more regulatory obligations cannot be simultaneously satisfied.  
- **Conflict State:** A machine‑readable semantic artefact representing an unresolved regulatory contradiction.  
- **Authority Boundary:** A jurisdictional or institutional limit defining the scope of a regulatory actor.  
- **Deterministic Constraint:** A rule or obligation that must be evaluated without probabilistic interpretation.

---

## 4. Semantic Class Structure

RA‑1 defines the following core semantic artefacts:

- **RA‑1.Entity** — the regulated actor or object  
- **RA‑1.Constraint** — a deterministic regulatory obligation or prohibition  
- **RA‑1.ConflictState** — a formal representation of an unresolved regulatory contradiction  
- **RA‑1.AuthorityBoundary** — the jurisdictional scope within which constraints apply  
- **RA‑1.Trace** — a machine‑readable record of constraint evaluation  

Each artefact is represented as a deterministic semantic class with strict type boundaries.

---

## 5. Regulatory Conflict Representation

RA‑1 models regulatory conflicts as **first‑class semantic objects**.

A conflict is represented when:

- two constraints produce mutually exclusive obligations  
- a constraint cannot be satisfied without violating another  
- jurisdictional boundaries impose contradictory requirements  

RA‑1 does not attempt to resolve the conflict.  
It exposes it as a **machine‑readable regulatory conflict state**.

Conceptual example:  

- OFAC → prohibition  
- EU Blocking Regulation → prohibition of compliance with OFAC  
- RA‑1.ConflictState → *Unresolved Antinomy*

---

## 6. Deterministic Constraint Model

RA‑1 constraints must be:

- deterministic  
- non‑probabilistic  
- jurisdiction‑pure  
- semantically stable  

Each constraint includes:

- source authority  
- obligation/prohibition  
- scope  
- evaluation trace  
- conflict linkage  

---

## 7. Authority Boundaries

Authority boundaries define the jurisdictional scope of constraints.

RA‑1 requires:

- explicit authority identification  
- non‑overlapping semantic boundaries  
- formal representation of cross‑boundary collisions  

Authority boundaries are essential for identifying regulatory antinomies.

---

## 8. Institutional Independence Declaration

The RA‑1 semantic class operates under strict institutional independence to ensure academic neutrality and semantic integrity.

**Independence Clause:**  
No institutional, commercial, governance, partnership, affiliation or representative relationship exists between **Semantic Standards Authority Limited**, **Renatas Vaičiūnas** and **immo.quick Global**.

All RA‑1 semantic artefacts, definitions and structures are developed exclusively within SSA’s academic research scope.

---

## 9. Compliance Requirements

Entities implementing RA‑1 must:

- preserve semantic neutrality  
- maintain deterministic evaluation  
- avoid proprietary influence on semantic structures  
- expose conflict states without attempting resolution  

---

## 10. Amendments

RA‑1 may be amended by the Semantic Standards Authority.  
Core semantic principles remain immutable.

---

## 11. References

- SSA Charter  
- SSA‑REG‑0001 Registry Specification  
- Academic literature on regulatory antinomies  
- Jurisdiction‑specific legal frameworks  

---

## 12. Appendix

- Formal class diagrams  
- Constraint evaluation examples  
- Conflict state encoding samples  
- Authority boundary mapping templates
