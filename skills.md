# Merlion-Ops: Agent Skill & Capability Manifest

This document outlines the structural skills, capabilities, and system tool mappings exposed to the `Merlion-Ops` Agent Engine for the Kaggle Agents for Business Track.

---

## 1. Model Context Protocol (MCP) Mapping (Day 2 Schema)
The framework leverages a decoupled protocol pattern to separate raw data fetching from core semantic model reasoning.
* **Skill Identifier:** `fetch_mock_government_data`
* **Interface Type:** Decoupled Data Server Simulation
* **Data Source:** Synthetic `data.gov.sg` ACRA / HDB cross-reference datastore (`mock_data.json`)
* **Operational Edge:** Pulls localized data structures safely without incurring external cloud token overhead or network processing dependency during evaluation cycles. Built to handle macro data-lake footprints seamlessly by allowing the harness layer to stream records out-of-process in chunked blocks.

---

## 2. Context Engineering & Memory State Dynamics (Day 3 Schema)
To maintain an efficient token footprint, the agent bypasses conversational bloat by relying on strict system invariants and stateless rule processing.
* **Orchestration Choice:** `gemini-2.5-flash` chosen for rapid multi-variable constraint validation and low latency.
* **Context Preservation:** Injects parsed JSON data structures directly into the execution prompt layer alongside a hardened system instruction matrix.
* **Analysis Constraints:** Forces structural cross-referencing of datetime variables (identifying temporal filing variances >= 1 month) and spatial boundaries (matching entity `classification` profiles against residential `address_type` fields).
* **Token Economic Ceiling:** Enforces a rigid `max_output_tokens=400` constraint and a deterministic `temperature=0.1` configuration, capping downstream resource usage and preventing reasoning drift.

---

## 3. Defensive Governance & Telemetry Guardrails (Day 4 Schema)
System safety and regional corporate data compliance are aggressively enforced via localized execution boundaries.
* **Skill Identifier:** `run_model_armor_shield`
* **Security Filter Layer:** Intercepts user queries *prior* to model inference via an automated ingress inspection loop to detect prompt injection exploits and block sensitive PII data leakage.
* **Anonymization Invariant:** Enforces strict structural privacy masking. The pipeline scrubs raw identifying dimensions and unique identifiers locally, formatting them into anonymous tokens (e.g., `Company_Alpha`, `Postal: 018XXX`) before data serialization.
* **Telemetry Output:** Compiles high-frequency execution traces silently behind the scenes into standardized OpenTelemetry span payloads. This isolates macro data fires from the presentation dashboard, routing high-volume logs directly to downstream observability environments such as Arize Phoenix.