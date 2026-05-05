# Crisis Simulation Command Portal

A command portal for planning, running, scoring, and learning from cyber crisis simulations.

This repository provides a production-minded PHP 8.x and MySQL 8.0 portal aligned with themes from Musaab Hasan's book, [Artificial Intelligence for Security Culture Transformation](https://www.amazon.com/Artificial-Intelligence-Security-Culture-Transformation/dp/3639876954). It translates the book's security culture transformation concepts into a working application foundation that can be extended for institutional, enterprise, and professional development contexts.

## Book Alignment

- Primary reference: **Chapter 10: Use of Digital Twins and Simulations for Crisis Scenarios**
- Transformation theme: Crisis labs, ransomware exercises, cross-functional decision-making, and resilience rehearsal.
- Broader framing: moving from compliance-centered activity to measurable security culture, adaptive learning, and organizational resilience.

## Core Capabilities

- Role or unit assessment intake with CSRF protection and server-side validation.
- Weighted scoring model with maturity bands.
- MySQL schema for assessments, dimension scores, initiatives, evidence, and audit records.
- Dashboard view with maturity score, assessment volume, initiative tracking, and dimension cards.
- Roadmap view for implementation workflows and improvement planning.
- JSON summary endpoint for integration with reporting tools.
- Docker-based local development environment.
- Lint and self-test scripts for maintainability.

## Assessment Dimensions

- **Scenario Realism**: Measures realism of technical, operational, and stakeholder injects.
- **Decision Velocity**: Tracks time from signal to coordinated decision.
- **Role Clarity**: Measures whether crisis roles and decision rights are understood.
- **Communication Quality**: Assesses internal, executive, customer, and regulator messaging.
- **Recovery Alignment**: Connects response actions to recovery objectives and dependencies.
- **Lessons Conversion**: Tracks whether exercise lessons become funded improvements.

## Operating Workflow

- Design a scenario with business, technical, legal, and communications injects.
- Assign participants, observers, decision owners, and evidence collectors.
- Run the simulation and capture decision timing, assumptions, and gaps.
- Convert lessons learned into owners, deadlines, and retest criteria.

## Quick Start

```bash
cp .env.example .env
docker compose up --build
```

Then open:

- Application: `http://localhost:8080`
- Health endpoint: `http://localhost:8080/health`
- JSON summary: `http://localhost:8080/api/summary`

## Local Checks

```bash
php bin/lint.php
php bin/test.php
```

## Repository Structure

```text
public/              Web entry point and assets
src/                 PHP application services, repository, and support classes
config/              Portal configuration and scoring dimensions
database/            MySQL migration and seed data
docs/                Architecture, security, testing, and extension documentation
bin/                 Developer and release checks
```

## Production Notes

- Store database credentials and application secrets outside source control.
- Enforce HTTPS at the reverse proxy or load balancer.
- Use least-privilege database users.
- Route logs and audit records to approved monitoring systems.
- Review assessment data retention rules before collecting identifiable responses.

## License

MIT License. See [LICENSE](LICENSE).
