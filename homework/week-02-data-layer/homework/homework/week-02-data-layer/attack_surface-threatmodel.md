# Task 1 — Attack Surface Mapping & Threat Model

Objective
- Produce an architecture diagram and STRIDE-style threat model for a minimal AI data stack:
  ingestion -> transformation -> storage -> feature store -> training -> inference.

Deliverables
1. A concise architecture diagram (PNG or Mermaid diagram embedded).
2. `threat_model.md` containing:
   - enumerated assets and trust boundaries
   - attacker capabilities and likely entry points
   - STRIDE findings with severity and remediation suggestions
   - a short attack graph mapping sequence(s) of compromise

Guidance (technical)
- Consider concrete components (e.g. Airbyte or Kafka for ingestion, dbt for transformations, Postgres/Snowflake, Feast as feature store, Airflow for orchestration). Document the specific versions you assume.
- For each entry point, provide:
  - Required preconditions for the attacker (network access, credentials, insider threat, supply chain)
  - Possible consequences to model integrity (label flips, time-shifted features, delayed triggers)
  - Detection signals (observable metrics/logs) and minimum telemetry to detect the compromise

Evaluation criteria
- Completeness of attack surface mapping
- Correctness of STRIDE analysis and realistic mitigations
- Clarity of attack graph and detection signals
