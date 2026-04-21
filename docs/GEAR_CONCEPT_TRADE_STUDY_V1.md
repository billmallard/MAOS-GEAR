# Landing Gear Concept Trade Study V1

**Status:** Working Draft — Preliminary Design Phase  
**Date:** 2026-04-20  
**Scope:** Main gear concept selection for MAOS pod-fuselage aircraft, Phase 1 prototype  
**References:**
- `INITIAL_REQUIREMENTS_V0.md` — GER-SYS-001 through GER-VER-004
- `ARTICLE_KNOWLEDGE_MIGRATION_2026Q2.md` — imported design decisions and open items
- `aerocommons: 2026-04-06-maos-geometry-design-decisions.md` — pod geometry, CD budget, gear working notes
- PBY-5A Catalina amphibious landing gear — historical precedent, Section 3.4

---

## 1. Background and Design Constraints

### 1.1 Driving Constraints

The MAOS pod fuselage is the dominant structural body of the aircraft. Unlike a conventional aircraft where the landing gear retracts into wing volume or a deep fuselage bay, the MAOS gear must integrate with a pressurized composite pod whose cross-section (52" W × 58" H) is governed by interior cabin volume requirements. This creates four hard constraints that any gear concept must resolve together — not sequentially:

| Constraint | Source | Implication |
|---|---|---|
| Pod belly is lowest point in cruise | Geometry article | Belly clearance in roll must be maintained; gear-down geometry must provide prop clearance |
| Pod wall is structural and pressure boundary | Pod design | Wheel wells penetrating the pod require pressure boundary restoration, structural reinforcement, and doors — significant complexity |
| Stroke for 6–10 ft/s sink rate at MTOW = 2,600 lb | Geometry article | Gear leg (spring or oleo) needs sufficient travel; a short, stiff leg in a half-retract position may have inadequate stroke at the up-locked angle |
| CD contribution of fixed faired gear ≈ 0.0050 | Geometry article Swet budget | This is ~30% of total estimated body drag; meaningful but not mission-critical for Phase 1 |

### 1.2 Governing Principle

From the knowledge migration document:

> *A constrained-complexity mechanism (single-axis pivot family) is preferred over high-DOF retract systems for early phases.*

This study treats single-axis pivot as a hard constraint for Phase 1 concept selection. Multi-axis retraction (e.g., fore-aft + lateral fold, or rotation plus telescoping) is not evaluated here and is explicitly deferred to a later design phase if the Phase 1 concept proves inadequate.

### 1.3 Historical Precedent — PBY-5A Catalina

The Consolidated PBY-5A Catalina (1940s) is the closest historical precedent for this configuration challenge. The PBY was a hull-centric aircraft (flying boat hull, no wing volume available for gear bays) that solved the same problem: gear must integrate with the hull structure, hull integrity must not be compromised, and the mechanism must be simple enough for wartime production.

The PBY solution:
- Main strut pivot at the hull structural hard point (wing strut attach)
- Single-axis rotation: strut swings upward and inward along the hull side
- Stowed wheel sits exposed against the hull exterior — no wheel well, no gear doors
- Hydraulic actuation, one actuator per side, no sequence valves

The PBY accepted an exposed stowed wheel as the price for hull simplicity and mechanism reliability. This is the lower bound for mechanism complexity and the reference point for Concept D in this study.

**Key difference from MAOS:** PBY was an amphibian — the bottom of the hull was a watertight boat hull, and hull-side stow kept the gear entirely clear of the water surface. MAOS is land-based, so the water-clearing constraint does not apply, but the competing pressure from pod structural integrity and belly clearance is analogous.

---

## 2. Concept Definitions

Four concepts are evaluated. All use a single pivot axis per side (hard constraint).

### Concept A: Fixed with Wheel Fairings

**Description:**  
No retraction. Main gear legs are fixed, with aerodynamic fairings (wheel pants) over the tires and streamlined leg fairings. This is the simplest possible installation and the drag baseline.

**Mechanism:** None. Rigid strut attach to pod belly hard points.  
**Stow position:** N/A — gear is always deployed.  
**Actuation:** None.

**Drag:**  
CD ≈ 0.0050 (per geometry article Swet estimate with fairings). Without fairings, penalty is higher (~0.0080).

**Structural integration:**  
Lowest complexity. No wheel well, no door, no pod penetration beyond the strut attach fitting. Attach fitting must carry static ground loads and hard-landing dynamic loads — a single weld-in bulkhead frame at each gear hard point.

**Energy absorption:**  
Full design freedom — the leg can be as long and as compliant as needed. A trailing-link spring leg or conventional oleo can achieve required stroke without any geometry compromise.

**Fail-safe behavior:**  
Perfect — it is always down. No deployment failure mode exists.

**Phase 1 buildability:**  
Highest. Fixed gear with wheel pants is a solved problem in experimental aircraft construction. Many kit-aircraft precedents.

**Weaknesses:**  
Drag penalty persists through all flight phases. For a long-endurance or high-altitude design mission, 0.0050 CD is meaningful. Gear cannot be eliminated from the drag budget later without reworking pod attach structure.

---

### Concept B: Full Retraction into Pod Belly Well

**Description:**  
Gear fully retracts into an enclosed wheel well in the pod belly. Wheel well doors close flush with the pod skin. In cruise, the belly is clean — no gear protrusion.

**Mechanism:** Single-axis pivot into belly cavity. Gear doors actuated separately (add complexity — doors are a second mechanism).  
**Stow position:** Fully enclosed inside pod.  
**Actuation:** Electric or hydraulic; door actuation requires separate sequence.

**Drag:**  
CD ≈ 0.0000 (fully retracted, doors closed). Maximum drag benefit.

**Structural integration:**  
Highest complexity. Requires:
- Wheel well cavity in pod belly — competes directly with pod shell structural path
- Pressure boundary restoration if well is inside pressurized volume
- Gear doors with hinge, actuator, latch, and open/close sequence
- Uplock and downlock mechanisms
- GER-FLT-001 compliance requires position sensing and fault detection on each of these elements

Wheel well also places constraints on pod belly geometry at the exact location where the belly clearance, structural hard-point, and battery floor concepts are competing for space.

**Energy absorption:**  
Constrained by well depth. If well depth is shallow, strut stroke in the retracted position may be inadequate — this is the specific concern flagged in the geometry article. Requires early geometry resolution before pod cross-section is finalized.

**Fail-safe behavior:**  
Most complex. A door failure (open or closed) and a gear deployment failure are both possible. Fail-to-deploy and fail-to-close-doors are distinct failure modes. System requires explicit fail-safe design (gravity extend + manual unlock) per GER-FLT-001.

**Phase 1 buildability:**  
Lowest. Wheel wells in composite pods require custom tooling and significant integration effort. Gear door mechanisms are a known source of maintenance burden in production aircraft.

**Weaknesses:**  
Disproportionate complexity for Phase 1, where proving the airframe and hybrid propulsion system is the primary objective. Pod belly geometry must be committed early, before flight test data is available to validate it.

---

### Concept C: Single-Axis Belly Pivot — Partial Stow (Working Baseline)

**Description:**  
The gear leg pivots on a single fore-aft axis at the pod belly hard point. The leg rotates upward to lie in a shallow belly fairing — semi-recessed but not fully enclosed. The wheel is partially or fully exposed below the fairing in the stowed position. This is the concept described in the geometry article as the working baseline.

**Mechanism:** Single-axis rotation about a fore-aft hinge at the belly hard point. One actuator per side (electric linear or small hydraulic).  
**Stow position:** Leg approximately horizontal or angled upward, wheel exposed below shallow belly fairing.  
**Actuation:** Electric linear actuator preferred for Phase 1 simplicity. No separate door actuator required — fairing is fixed.

**Drag:**  
CD estimated 0.0015–0.0025 in retracted position (wheel partially exposed in fairing). Roughly 50–70% reduction vs. fixed faired gear. Actual value depends on fairing geometry and wheel exposure depth — requires CFD validation at Phase 2.

**Structural integration:**  
Moderate. Belly hard point carries gear loads — same as Concept A. No pod pressure boundary penetration required if the pivot fitting is designed as an external attach. Fairing is non-structural and can be designed independently. The belly hard point geometry and the battery floor concept must be coordinated — they likely share the same structural frame.

**Energy absorption:**  
The critical geometry constraint. When the leg is at the "up" angle (near-horizontal), the effective stroke available for shock absorption is reduced — the leg is nearly parallel to the load vector for a hard landing, and a small linear displacement in the pod-normal direction corresponds to a small angular rotation. A **trailing-link configuration** partially resolves this: the shock absorber is the trailing link itself, which can be sized for full stroke regardless of the main leg retraction angle. This is the most direct path to meeting the 6–10 ft/s sink rate requirement in this geometry.

**Trailing-link reference:** Piper Comanche, several kit aircraft (Sonex, Velocity). Well-understood structurally in the experimental amateur-built community.

**Fail-safe behavior:**  
Good — gravity-down is achievable with spring-assist on the actuator. An actuator failure with spring pre-load defaults to the deployed position. Simpler than Concept B by elimination of doors and door sequence logic.

**Phase 1 buildability:**  
High. A single-pivot weld assembly with an off-the-shelf electric linear actuator is within the fabrication scope of a well-equipped experimental builder. The trailing-link sub-assembly adds some complexity but is well-precedented.

**Weaknesses:**  
Some residual drag penalty vs. Concept B. Fairing geometry must be validated against belly clearance in roll and crosswind. The trailing-link geometry needs to be resolved before the belly fairing is designed — these are coupled.

---

### Concept D: Single-Axis Side Pivot — PBY-Inspired, Exposed Stow

**Description:**  
The gear leg pivots on a fore-aft axis at the pod side, at or near the wing root / stub structural cluster. Retraction sweeps the leg upward and inward, with the stowed wheel resting against the lower pod side. No belly penetration. No fairing required — the stowed wheel is exposed against the pod exterior.

**Mechanism:** Single-axis rotation about a fore-aft hinge at the pod side hard point. One actuator per side.  
**Stow position:** Leg lies approximately horizontal against pod side, wheel exposed.  
**Actuation:** Electric linear or hydraulic.

**Drag:**  
CD estimated 0.0030–0.0040 in retracted position (wheel fully exposed on pod side). Reduction vs. fixed faired is modest — primarily from changing the frontal area angle and eliminating the strut-in-airstream contribution. Worse than Concept C.

**Structural integration:**  
Lowest complexity after Concept A. The pod side at the wing root is already the densest structural region of the airframe — wing attach, boom attach (if not top-mounted), and pod shell all converge here. Adding a gear pivot hard point at this location co-locates load paths rather than adding new penetrations. No belly fairing or wheel well required.

The key structural question is load transfer: the gear pivot must transmit ground loads (vertical, fore-aft, lateral) into the pod side frame. At the wing root, the pod side frame is already sized for wing bending loads — gear loads are compatible in direction and likely smaller in magnitude.

**Energy absorption:**  
Better than Concept C in the stow position. The leg in the stowed (side) orientation is still at a reasonable angle relative to the ground load vector when partially deployed. A conventional oleo or composite spring strut can achieve required stroke without the near-horizontal geometry constraint that affects Concept C.

**Fail-safe behavior:**  
Good — same gravity-down logic as Concept C. No door mechanism.

**Tread width:**  
This concept places the gear pivot at the pod side rather than the pod belly. The resulting tread width is governed by pod width (52") plus strut lateral offset. Tread width is comparable to or narrower than Concept C — this is a stability concern that must be evaluated for the MAOS mass and CG height. The PBY was famously tippy under crosswind with its narrow-tread main gear under a 14-ton aircraft. MAOS is lighter but the proportional concern applies.

**Phase 1 buildability:**  
High — mechanism is simpler than Concept C. Side-pivot strut fabrication and actuator installation are straightforward.

**Weaknesses:**  
Worst cruise drag of the retractable concepts. Wheel sitting against the pod side creates a bluff-body protrusion into the boundary layer. Tread width is constrained by pod width. Less drag reduction than Concept C makes this concept most compelling as a **Phase 1 simplicity-first choice** if drag is accepted as a Phase 1 compromise, or as a **fallback** if Concept C geometry proves infeasible.

---

## 3. Comparison Matrix

| Criterion | Weight | Concept A: Fixed Faired | Concept B: Full Retract | Concept C: Belly Pivot (Partial) | Concept D: Side Pivot (PBY) |
|---|---|---|---|---|---|
| Drag reduction in cruise | 25% | 1 — no reduction | 5 — full clean | 4 — ~60% reduction est. | 2 — ~20% reduction est. |
| Mechanism complexity (fewer DOF = better) | 20% | 5 — none | 1 — well + doors + sequence | 4 — single pivot, no doors | 5 — single pivot, no doors |
| Structural integration with pod | 20% | 4 — simple belly attach | 1 — well + pressure boundary | 3 — belly hard point, fairing | 5 — side hard point, no fairing |
| Stroke adequacy for energy absorption | 15% | 5 — unconstrained | 3 — well depth constrains | 2 — near-horiz. geometry constrains | 4 — side angle is more favorable |
| Fail-safe behavior | 10% | 5 — always deployed | 2 — multiple failure modes | 4 — gravity-down viable | 4 — gravity-down viable |
| Phase 1 buildability | 10% | 5 — fully solved problem | 1 — high tooling and complexity | 4 — within EAB scope | 5 — within EAB scope |
| **Weighted score** | | **3.65** | **2.10** | **3.35** | **3.95** |

*Scores 1–5 per criterion; weighted score = sum(weight × score).*

---

## 4. Recommendation

### Phase 1: Concept D (Side Pivot) or Concept A, resolved by tread width analysis

The matrix favors Concept D (3.95) for Phase 1 on simplicity and integration grounds. However, **the tread width question must be answered first.** If the pod side pivot geometry produces a tread width that is inadequate for the MAOS CG height and crosswind envelope (see Section 5), Concept D is eliminated and Concept A (fixed faired) becomes the Phase 1 baseline — it scores 3.65 and has zero mechanism risk.

The ordering of decisions is:

1. **Resolve tread width** — calculate the tread achievable with a side-pivot at the pod side hard point. Check static tip-over angle and crosswind stability for MTOW = 2,600 lb at the estimated CG height. If tread is adequate: Concept D. If not: Concept A.

2. **If Concept D is selected:** Define the pivot hard point and co-locate with wing root structure. Confirm that gear loads can be transferred into the existing pod side frame without a separate gear beam.

3. **If Concept A is selected:** Design belly attach hard points with provisions for future conversion to Concept C — same fitting locations, same structural frame. Phase 2 adds the pivot fitting and fairing over the same hard point.

### Phase 2: Concept C (Belly Pivot, Trailing-Link)

Concept C (3.35) is the Phase 2 target regardless of Phase 1 selection. It achieves meaningful drag reduction (~60% of fixed gear penalty), maintains mechanism simplicity, and avoids the pod pressure boundary complexity of Concept B. The trailing-link sub-assembly resolves the stroke concern and has strong kit-aircraft precedent.

Phase 2 key development items:
- Trailing-link geometry sizing against 6–10 ft/s sink rate at MTOW
- Belly fairing design and clearance validation (roll, crosswind, prop)
- Actuator selection and fail-safe spring sizing
- Coordination with battery floor structure at shared belly frame

### Phase 3: Concept B — only if mission requirements justify it

Concept B (full retraction) is only warranted if a production design requires maximum cruise efficiency and the pod geometry can accommodate the wheel well without conflicting with the battery floor, belly clearance, or pod structural path. That decision should not be made before Phase 1 flight test data is available.

---

## 5. Open Items to Resolve Before Concept Lock

These items gate the concept selection decision. They are assigned to the documents listed in `ARTICLE_KNOWLEDGE_MIGRATION_2026Q2.md`:

| Item | Gate | Assigned Document |
|---|---|---|
| Tread width calculation for Concept D side-pivot | Concept D vs. Concept A decision | `GEAR_CLEARANCE_AND_INTEGRATION_CONSTRAINTS.md` |
| Static tip-over angle at MTOW, CG range | Same gate | `GEAR_CLEARANCE_AND_INTEGRATION_CONSTRAINTS.md` |
| Trailing-link stroke sizing for 6–10 ft/s sink rate | Concept C Phase 2 design entry | `GEAR_STROKE_AND_ENERGY_ABSORPTION_REQUIREMENTS.md` |
| Belly hard-point geometry vs. battery floor frame | Concept C integration | `GEAR_CLEARANCE_AND_INTEGRATION_CONSTRAINTS.md` |
| Actuator type selection and fail-safe logic | Concept C/D actuation | `GEAR_FAILSAFE_AND_ACTUATION_LOGIC.md` |
| Pod side hard-point load compatibility (Concept D) | Concept D structural entry | `GEAR_CLEARANCE_AND_INTEGRATION_CONSTRAINTS.md` |

---

## 6. Historical Reference Summary

| Aircraft | Gear Type | Stow Method | Structural Lesson |
|---|---|---|---|
| PBY-5A Catalina (1940) | Amphibious tricycle | Side pivot, exposed wheel | Co-locate pivot with existing structural cluster; accept exposed wheel as drag/complexity trade |
| Piper Comanche (1957) | Retractable, trailing-link | Full well retract | Trailing-link provides stroke independent of strut retraction angle |
| Piper PA-28 Cherokee (1960) | Fixed, spring steel | N/A | Simple fixed gear can accept fairings for modest drag reduction; structural simplicity has value |
| Velocity XL (kit) | Retractable, single pivot | Belly well, partial | Single-axis pivot in composite structure is feasible in EAB context |
| Sonex (kit) | Fixed, spring steel | N/A | Phase 1 fixed gear valid baseline for composite pod EAB |
