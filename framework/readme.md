<!--
System Design Framework: README
Fill in sections marked with [TBD].
-->

# <img src="assets/favicon.png" alt="Icon" width="28" height="28" /> System Design Overview

## Problem Statement
- [TBD] One paragraph describing the user problem and why it matters.

## Requirements Summary
### Functional Requirements (High Level)
- [TBD] List 5-10 core capabilities.

### Non-Functional Requirements (High Level)
- [TBD] Latency, availability, durability, throughput, scale, security.

- **Inputs to estimate**: target geography, DAU/MAU, average sessions per user per day, average session length, requests per session, read/write ratio, payload sizes, data retention window.
- **Core traffic metrics**:
  - **QPS/TPS**: `(DAU * sessions_per_user_per_day * requests_per_session) / 86,400`
  - **Peak QPS/TPS**: `avg QPS * peak_factor` (e.g., 3-10x depending on product)
  - **CCU**: `DAU * (avg_session_length_seconds / 86,400) * sessions_per_user_per_day`
- **Data volume**:
  - **Daily writes**: `DAU * sessions_per_user_per_day * writes_per_session`
  - **Daily storage growth**: `daily_writes * avg_payload_size`
  - **Total storage**: `daily_growth * retention_days` (include indexes + replication)
- **Other factors to call out**: latency targets, availability SLA, fanout amplification, cache hit rate, and burst handling strategy.

## Goals and Non-Goals
### Goals
- [TBD] What success looks like for this system.

### Non-Goals
- [TBD] Explicitly exclude features or use cases.

## Scope and Assumptions
### Scope
- [TBD] In-scope features for this iteration.

### Assumptions
- [TBD] Known constraints and business assumptions.

## Stakeholders
- [TBD] Product, engineering, legal/compliance, operations, users.

## System Overview
- [TBD] 2-4 sentences summarizing the architecture at a high level.

## Architecture at a Glance
- [TBD] Bullet list of primary components and their roles.

## Key Workflows
- [TBD] 3-5 user or system flows (e.g., "User signup", "Create order").

## Data Model Summary
- [TBD] Key entities and relationships.

## Scale and Capacity
- [TBD] Expected DAU/MAU, peak RPS, data size, growth assumptions.

## Constraints and Risks
- [TBD] Regulatory constraints, budget, legacy integrations, risk areas.

## Open Questions
- [TBD] Items needing clarification.

## References
- [TBD] Links to docs, tickets, or external constraints.
