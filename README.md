# Merlion-Ops: Autonomous Regulatory Compliance & Auditing Graph

An autonomous enterprise compliance agent engineered for the **Kaggle Agents for Business** track. Merlion-Ops automates corporate registry auditing and residential zoning risk detection using a deterministic execution loop powered by Gemini.

To provide real-world fidelity, the pipeline models regulatory frameworks from Singapore (symbolized by the iconic **Merlion**):
* **ACRA:** Accounting and Corporate Regulatory Authority (Corporate registries).
* **HDB:** Housing & Development Board (Public residential estates with strict commercial zoning limits).

---

## Core Architecture

* **Model Armor Input Shield (`run_model_armor_shield`):** Pre-ingress isolation layer intercepting user inputs to scrub sensitive PII and neutralize prompt-injection vulnerabilities prior to inference.
* **Decoupled Model Context Protocol (MCP):** An out-of-process tool datastore simulation (`mock_data.json`) modeling production registry tables. Eliminates active network polling, runtime latency, and cloud API token vulnerability.
* **Cognitive Reasoning Engine (`gemini-2.5-flash`):** Evaluates multi-variable raw data strings against strict system invariants. A rigid `max_output_tokens=400` ceiling guarantees low latency and predictable token economics.
* **Governance Telemetry:** Generates standard OpenTelemetry span structures natively, optimized for downstream ingestion into enterprise tracing platforms like Arize Phoenix.

---

## Evaluation Test Matrix

The agent executes zero-shot, autonomous reasoning across four synthetic corporate entities to evaluate compliance pipelines under strict data-privacy masking constraints:
1. **Delta-Merlion Logistics Ltd (FAIL):** Flags a 5-month temporal filing delinquency and an illegal heavy logistics operation inside a residential zone (`HDB 3-Room`).
2. **Alpha Corporate Holdings (PASS):** Validates a fully compliant baseline operating within a designated commercial tower.
3. **Apex Cloud Tech Solutions (PASS - Exemption):** Demonstrates deep semantic contextual reasoning by granting a *Home Office Exemption* for lightweight IT consulting within an HDB flat over a blind string match.
4. **Vanguard Heavy Industrial Trades (FAIL):** Isolates a pure 6-month temporal filing delay while verifying its physical industrial park zoning footprint is correct.

---

## Repository Manifest

* `app.py`: Core orchestration pipeline logic, reasoning loops, and input shielding.
* `mock_data.json`: Synthetic corporate registry entries, SSIC business classifications, and zoning tables.
* `skills.md`: Documentation mapping capabilities directly to Day 2-4 course schemas.
