SSA‑S2 — Regulatory Antinomy Specification (RA‑1)
Version: 1.0
Status: Draft
Authority: Semantic Standards Authority (SSA)
Document Class: Semantic Standard
Identifier: S2

1. Purpose
This standard defines the semantic structure, properties, and operational implications of Regulatory Antinomy Class RA‑1, a condition in which two or more sovereign legal obligations cannot be lawfully satisfied simultaneously.

RA‑1 is a deterministic semantic fact, not an error condition.

2. Scope
This specification covers:

formal definition of RA‑1,

structural properties,

semantic constraints,

operational behaviour in deterministic systems,

audit and publication requirements.

3. Definition
RA‑1 exists when:

Two or more sovereign jurisdictions impose mutually exclusive obligations on the same subject;

No lawful mechanism exists to resolve, prioritise, derogate, or interpret the obligations into compatibility;

Any attempt to satisfy one obligation necessarily violates the other.

Formally:

𝑂
1
(
𝑆
)
=
required
and
𝑂
2
(
𝑆
)
=
prohibited
and:

¬
∃
𝑅
such that
𝑅
(
𝑂
1
,
𝑂
2
)
→
lawful resolution
4. Properties of RA‑1
4.1 Mutual Negation
Each obligation negates the lawful possibility of fulfilling the other.

4.2 Sovereign Independence
The obligations originate from independent sovereign authorities that cannot be subordinated.

4.3 Non‑Resolvable Structure
No lawful interpretative, procedural, or hierarchical mechanism exists to resolve the conflict.

4.4 Deterministic Impact
RA‑1 directly affects deterministic execution systems, requiring explicit handling.

5. Operational Behaviour
5.1 System State: HOLD
Upon detection of RA‑1, the system MUST enter a HOLD state.

5.2 Jurisdiction‑Pure Artefacts
The system MUST generate artefacts that are pure to each jurisdiction, without cross‑contamination.

5.3 No Resolution Attempt
The system MUST NOT attempt to resolve, merge, prioritise, or reinterpret the obligations.

5.4 Mandatory Audit
RA‑1 MUST be recorded in the audit trail with:

timestamp,

jurisdictions involved,

obligations,

detection method,

system state change.

6. Semantic Unit Structure
RA‑1 MUST be represented as a semantic unit compliant with S1: Semantic Unit Specification.

Required fields:

id: RA‑1

class: regulatory_antinomy

jurisdictions: list

obligations: list

conflict_type: “mutual_negation”

resolution: “none”

system_state: “HOLD”

audit_reference: AD‑xxx

7. Examples
7.1 Canonical Example
US OFAC: prohibits execution

EU Blocking Regulation: prohibits non‑execution

Result:

US: DO NOT EXECUTE
vs
EU: DO NOT BLOCK
This is a pure RA‑1.

8. Versioning
Major changes require an Authority Decision.

Minor editorial changes do not alter semantic meaning.

Deprecated versions remain accessible.

9. Governance
This standard is governed by SSA‑GOV‑0001.
Approval requires Authority Decision AD‑002 (pending).

Document End
