# MAOS-GEAR

Open-source landing gear subsystem development for MAOS aircraft concepts.

## Status

Concept and architecture phase.

## Safety Notice

This repository is for research and experimental development only. It is not approved for manned flight and must not be used as-is in safety-critical operation without formal system safety assessment, verification, validation, and regulatory compliance.

This project targets the Experimental Amateur-Built category. FAA certification is not a current design constraint, but engineering decisions should still follow conservative aerospace and safety-critical best practices where practical.

## Role in MAOS Multi-Project Architecture

This repository owns the MAOS landing gear domain.

- Landing gear architecture, load paths, and structural assumptions.
- Gear geometry, steering/braking interface assumptions, and operational limits.
- Landing gear subsystem verification artifacts and interface definitions.

Related repositories:

- MAOS-DESIGN owns aircraft-level geometry, packaging, and integration constraints.
- MAOS-FCS owns flight-control computation and flight-critical control paths.
- MAOS-ECS owns environmental control and pressurization subsystem development.
- aerocommons is the website and program-level communications hub.

## Mission

Develop a practical and robust landing gear subsystem architecture that supports reliable ground handling, rollout, and field operations with explicit load assumptions, clear interface boundaries, and traceable verification.

## Scope

In scope:

- Landing gear architecture trade studies and load-envelope assumptions.
- Structural and kinematic design constraints for gear, mounts, and fairings.
- Steering, braking, shock-absorption, and tire interface requirements.
- Fault/degraded operation behavior and maintenance-oriented design assumptions.
- Bench-test and analysis artifacts for subsystem verification.

Out of scope:

- Aircraft-level geometry governance and top-level configuration control (owned by MAOS-DESIGN).
- Primary flight-control law ownership (owned by MAOS-FCS).
- Propulsion subsystem ownership (owned by MAOS-ICE and MAOS-MOTOR).

## Interface-First Rules

Before detailed implementation, freeze and version:

- Mechanical interfaces: mount points, load paths, stroke/travel limits, and tolerances.
- Braking/steering interfaces: command semantics, feedback telemetry, and failure flags.
- Electrical interfaces (if applicable): power budgets, connector definitions, and shielding assumptions.
- Hydraulic/pneumatic interfaces (if applicable): pressure/flow limits and fault responses.
- Operational envelopes: taxi, takeoff, landing, and rough-field load assumptions.

Starter template: INTERFACE_CONTROL_DOCUMENT_TEMPLATE.md

## Suggested Repository Layout

- docs  Architecture, requirements, and verification plans
- analysis  Load, stress, fatigue, and kinematics studies
- cad  Geometry models and exchange artifacts
- tests  Bench, static-load, and subsystem test procedures
- tools  Analysis and post-processing utilities
- configs  Gear geometry and configuration presets
- data  Test captures, load cases, and reference datasets

## Verification Strategy

- Requirements-to-test traceability for landing gear safety-relevant behaviors.
- Static and dynamic load-case analysis with explicit margins.
- Bench validation for steering, braking, and damping behavior where applicable.
- Fault/degraded scenario evaluation for controllability and runway safety implications.
- Regression evidence for each interface-affecting design change.

## Current Milestones (As of 2026-04-14)

Current repository maturity is bootstrap-level.

Near-term milestones:

1. Establish baseline repo structure (docs, analysis, cad, tests, tools, configs, data).
2. Publish top-level gear subsystem requirements and load assumptions.
3. Draft first ICD covering mechanical, braking/steering, and any electrical/hydraulic interfaces.
4. Create initial load and kinematics study artifacts for baseline configuration.
5. Define first bench/static verification matrix for gear behavior and fault conditions.

## Knowledge Migration

- Article-derived subsystem migration notes: `docs/ARTICLE_KNOWLEDGE_MIGRATION_2026Q2.md`

## Licensing

This repository uses a dual-license model:

- Source code: PolyForm Noncommercial 1.0.0 (LICENSE-CODE)
- Documentation and non-code design content: CC BY-NC-SA 4.0 (LICENSE-DOCS)

Commercial use is not granted by default. For commercial licensing, contact contact@aerocommons.org.

Contribution and file classification guidance: CONTRIBUTING.md

## Program Context

MAOS is an open-source experimental aircraft development effort. The aircraft has not yet flown. All design and performance values are targets subject to revision as analysis and testing mature.
