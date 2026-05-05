# Database Schema

The portal uses MySQL 8.0 with `utf8mb4` collation.

## Tables

- `dimensions`: scoring dimensions and weights.
- `assessments`: assessment subject, weighted score, maturity band, and notes.
- `assessment_scores`: per-dimension scoring evidence.
- `initiatives`: improvement initiatives linked to impact areas.
- `evidence_items`: examples and supporting evidence records.
- `audit_events`: system activity trail.

## Portal Dimensions

- `scenario_realism`: Scenario Realism - Measures realism of technical, operational, and stakeholder injects.
- `decision_velocity`: Decision Velocity - Tracks time from signal to coordinated decision.
- `role_clarity`: Role Clarity - Measures whether crisis roles and decision rights are understood.
- `communication_quality`: Communication Quality - Assesses internal, executive, customer, and regulator messaging.
- `recovery_alignment`: Recovery Alignment - Connects response actions to recovery objectives and dependencies.
- `lessons_conversion`: Lessons Conversion - Tracks whether exercise lessons become funded improvements.

## Seeded Initiatives

- Ransomware executive tabletop (Business Continuity, high)
- Supply-chain compromise drill (Procurement Risk, high)
- Crisis communications rehearsal (Communications, medium)
