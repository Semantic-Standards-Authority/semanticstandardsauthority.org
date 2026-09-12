SSA‑REG‑0001 — Semantic Standards Registry (Phase 1)
Version: 1.0
Status: Draft
Authority: Semantic Standards Authority (SSA)
Document Class: Registry Specification
Identifier: SSA‑REG‑0001

1. Purpose
Semantic Standards Registry (SSR) defines the authoritative catalogue of semantic standards, specifications, and decisions issued by the Semantic Standards Authority.
It provides a unified structure for registration, versioning, identification, and lifecycle management of all SSA‑approved semantic artefacts.

2. Scope
This document covers:

registry structure,

standard identifiers,

versioning model,

lifecycle states,

minimal API definition,

governance hooks for Authority Decisions.

3. Registry Structure
The registry consists of the following top‑level entities:

Standard — a semantic specification approved by SSA.

Version — a specific release of a standard.

Decision — an Authority Decision affecting a standard.

Metadata — descriptive and operational information.

Each entity is stored as a structured semantic unit according to SSA Semantic Integration Protocol v1.0.

4. Identifiers
Every standard receives a permanent identifier:

Code
S<Number>
Examples:

S1 — Semantic Unit Specification

S2 — Regulatory Antinomy Specification

S3 — Interoperability Layer Definition

Versions use the following format:

Code
S<Number>-v<Major>.<Minor>
Example:

S1-v1.0

Authority Decisions use:

Code
AD-<Number>
Example:

AD-001

5. Lifecycle States
Each standard version can be in one of the following states:

Draft — under development

Review — undergoing Authority review

Approved — formally accepted

Deprecated — replaced by a newer version

Withdrawn — removed from active use

Lifecycle transitions require an Authority Decision.

6. Registry Fields
Each registry entry must contain:

id — standard identifier

title — human‑readable name

version — version identifier

status — lifecycle state

description — short summary

authority_decision — reference to AD‑xxx

created_at — timestamp

updated_at — timestamp

semantic_unit — link to the semantic unit file

repository_path — GitHub path

7. Minimal API Definition (Phase 1)
API is conceptual in Phase 1 (no implementation required).

7.1 Endpoints
Code
GET /registry
GET /registry/{id}
POST /registry
PUT /registry/{id}
7.2 Data Model
All API responses must return semantic units compliant with SSA Semantic Integration Protocol v1.0.

8. Governance Integration
Registry operations are governed by SSA‑GOV‑0001.
Any creation, modification, approval, or withdrawal of a standard must reference an Authority Decision (AD‑xxx).

Example:

Code
authority_decision: AD-002
9. Audit Trail
Every change to registry entries must be recorded with:

timestamp,

actor (Authority, Editor, Reviewer),

change summary,

decision reference.

Audit trail is stored in /governance/audit/.

10. Initial Entries (Phase 1)
The registry begins with one initial standard:

Code
id: S1
title: Semantic Unit Specification
version: v1.0
status: Approved
description: Defines the structure of semantic units used across SSA.
authority_decision: AD-001
created_at: 2026-09-12
updated_at: 2026-09-12
semantic_unit: /standards/S1/S1_v1.0.md
repository_path: /standards/S1/

Minor version increments may be editorial.

Deprecated versions remain accessible.

Withdrawn versions are archived.

12. Publication
Registry is published in:

GitHub (primary)

Zenodo (archival)

Each version receives a DOI.

Document End
