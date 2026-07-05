**Executive Summary & Problem Matrix**

Manual corporate auditing and spatial footprint verifications consume thousands of operational hours annually and remain highly susceptible to human oversight and regulatory friction. Merlion-Ops mitigates this systematic risk by establishing a production-grade, data-private autonomous AI Agent and Observability Harness. The system ingests unstructured corporate profiles, programmatically parses regulatory timelines, cross-references localized spatial zoning boundaries, and compiles deterministic, anonymized compliance ledgers.

To anchor this platform in a robust, real-world regulatory environment, the operational parameters are modeled precisely after the statutory guidelines of the city-state of Singapore (symbolized by the iconic Merlion):

- ACRA (Accounting and Corporate Regulatory Authority): The primary statutory body overseeing national entity registrations, legal profiles, and strict annual financial filing timelines.
- HDB (Housing & Development Board): The national public housing authority managing high-density residential estates, enforcing rigorous zoning laws prohibiting unauthorized commercial or high-footprint logistics footprints.

Mitigation of Enterprise AI Bottlenecks

1. Zero-Token Latency & Quota De-risking: Rather than implementing fragile network polling or directly hitting external CKAN Datastore production APIs (which introduce token quota exhaustion risks and network instability), the harness utilizes a decoupled out-of-process data layer (mock_data.json) modeled strictly after production ACRA/HDB data schemas. This achieves deterministic, air-gapped sandboxed execution with absolute zero latency.
2. Sovereign & Legal Risk Mitigation: Implements localized semantic rule validation constraints via an isolated policy layer (skills.md), ensuring perfect alignment with regional compliance thresholds.
3. Elimination of Black-Box Skepticism: Instruments standard open-source tracing patterns, compiling automated structural execution span logs optimized for modern enterprise observability.

**Architectural Blueprint & Data Flow**

The platform implements a highly scalable Model = Agent + Harness design pattern. The frontend GUI functions strictly as the Harness (managing safety, telemetry, and ingestion parameters), while the backend functions as the Agent Execution Core (handling programmatic constraint evaluation over unparsed JSON arrays).

[User Request / Ingress] ──► [Model Armor Security Shield] ──► [MCP Datastore Ingestion Layer] ──► [Gemini Core Agent Loop] ──► [Anonymized Report Generation] ──► [OpenTelemetry Spans Export]

1. The Security Ingress Layer (Model Armor Interface): Prior to core processing, payloads pass through a local semantic security layer (run_model_armor_shield) that proactively intercepts prompt mutations, edge-case structural exceptions, and sensitive parameter triggers.
2. Model Context Protocol (MCP) Decoupled Data Server: The orchestrator reads the entire unified global array (mock_data.json) directly from disk layout, separating raw database schemas cleanly from model weights.
3. Core Cognitive Evaluation & Verification Matrix: The system ingests the raw data payload directly alongside a hardened system instruction array. The processing engine analyzes multivariable objects programmatically on the fly, scaling flawlessly from a minimal testing pool to thousands of lines of data without relying on fragile hardcoded string matches.


**System Verification & Core Findings**

To systematically validate the engine's programmatic reasoning without risking telemetry data leaks, the pipeline evaluates a synthetic ground-truth matrix embedded with injected operational discrepancies:

Temporal Date Delta Discrepancy: The engine dynamically parses variable timelines, identifying that Delta-Merlion Logistics Ltd held an account_due_date of 2026-01-15 but an annual_return_date of 2026-06-20. It successfully flags a severe 5-month operational filing delinquency violating default corporate guidelines.

Spatial/Zoning Violation Cluster: The pipeline programmatically cross-references an entity's declared classification (Logistics) with its registered postal address footprint type (HDB 3-Room Residential). It immediately exposes the regulatory compliance hazard of running high-footprint, heavy-traffic commercial supply chains within protected residential living spaces.

Structural Invariant Guardrail Verification: To satisfy strict corporate data-privacy boundaries, the model forces an automated anonymization layer. Raw Unique Entity Numbers (UENs) and precise door numbers are systematically scrubbed and replaced with anonymous tokens (e.g., Company_A, Postal: 018XXX) before compiling the final span layer.

**Observability Harness & Interactive Control Deck**
- Telemetry & System Tracing
System execution metrics, parameter boundaries, and evaluation nodes are mapped natively into standardized OpenTelemetry span payloads. By tracking data limits locally, the repository structure is fully optimized out-of-the-box for seamless routing into downstream corporate tracing environments such as Arize Phoenix. This grants enterprise risk teams micro-level visibility into the agent’s logic framework, tracing prompt metrics with zero semantic drift.

- Non-Technical Graphical User Interface
Merlion-Ops features a local, air-gapped graphical dashboard built on top of Streamlit. This interface translates raw backend JSON data tables into clean, color-coded, scannable Business Logic Cards. Compliance officers, internal auditors, and non-technical stakeholders can now dynamically toggle system safety guardrails and audit full cohort portfolios live without typing a single terminal command line.


---
Local Sandbox Quickstart
1. Execute the localized, data-private application harness on your workspace in seconds:
git clone https://github.com/MYlatentspace/merlion-ops.git
cd merlion-ops

2. Install core platform dependencies:
pip install streamlit

3. Launch the secure local server layer:
streamlit run gui.py --server.address=127.0.0.1

Access the secure GUI portal instantly at http://127.0.0.1:8501.

## Repository Manifest & Structural Architecture
The codebase implements a decoupled Model = Agent + Harness design pattern, clearly separating user-facing control systems from local data schemas and core verification execution blocks:

gui.py: The primary user control deck and presentation harness built on top of Streamlit. It manages safety toggles, orchestrates the out-of-process data injection loops, and renders color-coded compliance verdicts natively into a graphical user interface.

app.py: The core headless orchestration pipeline logic layer. It manages the underlying automated reasoning loops, constraint calculation matrices, and terminal-level input shielding.

mock_data.json: The unified data engine storage payload. It holds the synthetic corporate registry profiles, operational registration timelines, SSIC business classifications, and spatial zoning footprint variables.

skills.md: The compliance rulebook parameter dictionary. This file maps active entity verification rules, temporal constraints, and spatial zoning boundaries directly to the system's cognitive execution layer.
