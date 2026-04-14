# MAOS-GEAR Article Knowledge Migration (2026 Q2)

Purpose: Capture available landing-gear-related knowledge from aerocommons and seed MAOS-GEAR execution priorities.

Scope note: This is R&D guidance for Experimental Amateur-Built development. It is not a certification claim.

## Source Articles

- 2026-04-06-maos-geometry-design-decisions.md

## Imported Decisions and Working Baseline

- Landing gear drag has meaningful system-level impact and cannot be treated as a late packaging detail.
- A constrained-complexity mechanism (single-axis pivot family) is preferred over high-DOF retract systems for early phases.
- Stroke, clearance, and structural hard-point integration are coupled constraints that must be solved together.

## Gear Guidance to Carry Into This Repo

- Keep mechanism simplicity as a governing principle for Phase 1.
- Use explicit sink-rate energy absorption assumptions in concept evaluation.
- Tie gear concept decisions to pod-belly geometry and integration hard points.

## Open Decisions Assigned to MAOS-GEAR

- Select fixed faired, partial-retract, or alternate concept for Phase 1 baseline.
- Define required stroke and damping strategy for hard-landing envelope.
- Define up/down position clearance constraints including prop and belly clearance.
- Define actuation/fail-safe behavior for selected mechanism.

## Immediate Work Items

1. Create docs/GEAR_CONCEPT_TRADE_STUDY_V1.md.
2. Create docs/GEAR_STROKE_AND_ENERGY_ABSORPTION_REQUIREMENTS.md.
3. Create docs/GEAR_CLEARANCE_AND_INTEGRATION_CONSTRAINTS.md.
4. Create docs/GEAR_FAILSAFE_AND_ACTUATION_LOGIC.md.

## Suggested Deliverables to Add Next

- docs/GEAR_CONCEPT_TRADE_STUDY_V1.md
- docs/GEAR_STROKE_AND_ENERGY_ABSORPTION_REQUIREMENTS.md
- docs/GEAR_CLEARANCE_AND_INTEGRATION_CONSTRAINTS.md
- docs/GEAR_FAILSAFE_AND_ACTUATION_LOGIC.md
