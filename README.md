**Executive Summary & Problem Matrix**

Manual corporate auditing and spatial footprint verifications consume thousands of operational hours annually and remain highly susceptible to human oversight and regulatory friction. Merlion-Ops mitigates this systematic risk by establishing a production-grade, data-private Zero-Trust Autonomous AI Agent Framework and Observability Harness. The system ingests unstructured corporate profiles, programmatically parses regulatory timelines, cross-references localized spatial zoning boundaries, and compiles deterministic, anonymized compliance ledgers.

To anchor this platform in a robust, real-world regulatory environment, the operational parameters are modeled precisely after the statutory guidelines of the city-state of Singapore (symbolized by the iconic Merlion):

- ACRA (Accounting and Corporate Regulatory Authority): The primary statutory body overseeing national entity registrations, legal profiles, and strict annual financial filing timelines.
- HDB (Housing & Development Board): The national public housing authority managing high-density residential estates, enforcing rigorous zoning laws prohibiting unauthorized commercial or high-footprint logistics footprints.

Mitigation of Enterprise AI Bottlenecks 

1. Zero-Token Latency & Quota De-risking via MCP Datastore Ingestion: Rather than implementing fragile network polling or directly hitting external CKAN Datastore production APIs (which introduce token quota exhaustion risks and network instability), the architecture implements a decoupled Model Context Protocol (MCP) Datastore Ingestion Layer. Using a local sandbox resource mirror (mock_data.json) modeled strictly after production ACRA/HDB schemas, the harness handles bulk-data lookups completely out-of-process. This isolates the core LLM from high-frequency network queries, achieving deterministic, air-gapped sandbox execution with absolute zero latency and enabling the framework to scale seamlessly over millions of entries via chunked data streaming.
2. Sovereign & Legal Risk Mitigation: Implements localized semantic rule validation constraints via an isolated policy layer (skills.md), ensuring perfect alignment with regional compliance thresholds and eliminating hallucinated regulatory boundaries.
3. Elimination of Black-Box Skepticism: Instruments standard open-source tracing patterns, compiling automated structural execution span logs optimized for modern enterprise observability and deep lifecycle inspection.

**Architectural Blueprint & Data Flow**

The platform implements a highly scalable Model = Agent + Harness design pattern. The frontend GUI functions strictly as the Harness (managing safety configurations, data filtration, telemetry compilation, and ingestion parameters), while the backend functions as the Agent Execution Core (handling programmatic constraint evaluation over unparsed JSON arrays).

[User Request / Ingress] ──► [Model Armor Security Shield] ──► [MCP Datastore Ingestion Layer] ──► [Gemini Core Agent Loop] ──► [Anonymized Report Generation] ──► [OpenTelemetry Spans Export]

1. The Security Ingress Layer (Model Armor Interface): Prior to core processing, payloads pass through a local semantic security layer (run_model_armor_shield) that proactively intercepts prompt mutations, adversarial jailbreak vectors, edge-case structural exceptions, and sensitive parameter triggers.
2. Model Context Protocol (MCP) Decoupled Data Server: The orchestrator reads the unified global array (mock_data.json) directly from disk layout, separating raw database schemas cleanly from model weights. By managing data ingestion out-of-process, the harness streams records in controlled micro-batches, preventing memory exhaustion and front-end freezing.
3. Core Cognitive Evaluation & Verification Matrix: The system ingests the raw data payload directly alongside a hardened system instruction array. The processing engine analyzes multivariable objects programmatically on the fly, scaling flawlessly from a minimal testing pool to thousands of lines of data without relying on fragile, hardcoded string matches.

**System Verification & Core Findings**

To systematically validate the engine's programmatic reasoning without risking telemetry data leaks, the pipeline evaluates a synthetic ground-truth matrix embedded with injected operational discrepancies:
- Temporal Date Delta Discrepancy: The engine dynamically parses variable timelines, identifying that Delta-Merlion Logistics Ltd held an account_due_date of 2026-01-15 but an annual_return_date of 2026-06-20. It successfully flags a severe 5-month operational filing delinquency violating default corporate guidelines.

- Spatial/Zoning Violation Cluster: The pipeline programmatically cross-references an entity's declared classification (Logistics) with its registered postal address footprint type (HDB 3-Room Residential). It immediately exposes the regulatory compliance hazard of running high-footprint, heavy-traffic commercial supply chains within protected residential living spaces.
- Structural Invariant Guardrail Verification: To satisfy strict corporate data-privacy boundaries, the model forces an automated anonymization layer. Raw Unique Entity Numbers (UENs) and precise door numbers are systematically scrubbed and replaced with anonymous tokens (e.g., Company_A, Postal: 018XXX) before compiling the final span layer.

**Observability Harness & Interactive Control Deck*
- Telemetry & System Tracing
System execution metrics, parameter boundaries, and evaluation nodes are mapped natively into standardized OpenTelemetry span payloads. By tracking data limits locally, the repository structure is fully optimized out-of-the-box for seamless routing into downstream corporate tracing environments such as Arize Phoenix. This grants enterprise risk teams micro-level visibility into the agent’s logic framework, tracing prompt metrics with zero semantic drift. High-frequency execution traces generated across large data volumes are fed directly into the telemetry layer, keeping the client-facing presentation layer completely clean and stable.
-Non-Technical Graphical User Interface
Merlion-Ops features a local, air-gapped graphical dashboard built on top of Streamlit. Designed around absolute simplicity, a compliance officer or non-technical auditor only has to click a single button—"🚀 Run Cohort Analytics Matrix"—to evaluate an entire portfolio.

The interface translates raw backend JSON data tables into clean, color-coded, scannable Business Logic Cards. When scaled to millions of records, the interface completely prevents frontend clutter by aggregating clean, baseline passing profiles into a single high-level statistical summary banner, reserving individual visual cards exclusively for high-risk zoning and temporal anomalies that require manual administrative review. Non-technical stakeholders can also dynamically toggle system safety guardrails live without typing a single terminal command line.

Local Sandbox Quickstart
1. Clone the repository:
git clone https://github.com/MYlatentspace/merlion-ops.git
cd merlion-ops
2. Install core platform dependencies:
pip install streamlit
3. Launch the secure local server layer:
streamlit run gui.py --server.address=127.0.0.
4. Access the secure GUI portal instantly at http://127.0.0.1:8501.