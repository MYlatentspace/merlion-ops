# 🦁 Merlion-Ops: Agent Skill & Capability Manifest

This document outlines the structural skills, capabilities, and system tool mappings exposed to the `Merlion-Ops` Agent Engine for the Kaggle Agents for Business Track.

---

## 🛠️ 1. Model Context Protocol (MCP) Mapping (Day 2 Schema)
The framework leverages a decoupled protocol pattern to separate raw data fetching from core semantic model reasoning.
* **Skill Identifier:** `fetch_mock_government_data`
* **Interface Type:** Decoupled Data Server Simulation
* **Data Source:** Synthetic `data.gov.sg` ACRA / HDB cross-reference datastore
* **Operational Edge:** Pulls localized data structures safely without incurring external cloud token overhead or network processing dependency during evaluation cycles.

---

## 🧠 2. Context Engineering & Memory State Dynamics (Day 3 Schema)
To maintain an efficient token footprint, the agent bypasses conversational bloat by relying on strict system invariants.
* **Orchestration Choice:** `gemini-2.5-flash` for high multi-variable processing density.
* **Context Preservation:** Injects dynamic JSON arrays directly into the execution prompt layer alongside a hardened system instruction matrix.
* **Token Economic Ceiling:** Enforces a rigid `max_output_tokens=400` constraint, capping downstream resource usage and guaranteeing low operational latency.

---

## 🛡️ 3. Defensive Governance & Telemetry Guardrails (Day 4 Schema)
System safety and regional corporate data compliance are aggressively enforced via two explicit boundaries.
* **Skill Identifier:** `run_model_armor_shield`
* **Security Filter Layer:** Intercepts user inputs *prior* to model inference to detect prompt injection exploits and block sensitive PII data leakage.
* **Anonymization Invariant:** The model is structurally barred from printing raw Unique Entity Numbers (UENs) or exact public postal codes, replacing them with compliance-safe tokens (e.g., `Postal: 018XXX`).
* **Telemetry Output:** Employs standard OpenTelemetry formatting, compiling execution traces cleanly for downstream observability pipelines.