# 1. Mechanics (IPhO Syllabus: Mechanics)

Mechanics is the largest single component of almost every IPhO paper and the topic where the gap between "can solve textbook problems" and "can solve IPhO problems" is widest, because the hard problems are almost always textbook mechanics plus one extra structural idea (a constraint, a non-inertial frame, an energy method that avoids messy force analysis, or a symmetry that makes Lagrangian mechanics dramatically faster than Newtonian bookkeeping). This file is ordered so each subtopic's math prerequisite is solved *before* you need it.

## Subtopics, in dependency order

| Subtopic | Math prerequisite (Tier 1 — go read this first) | If still stuck → deeper math | Physics text (Tier 1) | Tier-1 problem set |
|---|---|---|---|---|
| Vectors, 1D/2D kinematics | `00-mathematical-toolkit.md`: vector algebra, single-variable calculus | — | Kleppner & Kolenkow (K&K), ch. 1; Morin, ch. 1 | K&K ch. 1 + Morin ch. 1, all problems |
| Newton's laws, forces (friction, tension, springs) | Single-variable ODEs (`x'' = F/m` is already an ODE) | Tenenbaum & Pollard's lessons on simple ODEs if the differential-equation framing feels unfamiliar | K&K ch. 2-3; Morin ch. 2-3 | K&K ch. 2-3, Morin ch. 2-3; begin Irodov mechanics chapter |
| Work, energy, conservative forces | Line integrals (work as `∫F·dl`) | Schey's divergence/curl chapters, to understand *why* only some forces are conservative (curl-free) | K&K ch. 8 (energy); Morin ch. 3-4 | Same, plus Kalda's *Mechanics* handout, energy-method section |
| Momentum, collisions, center of mass | — (algebra-level once vectors are solid) | — | K&K ch. 4; Morin ch. 3 | K&K ch. 4, Morin ch. 3 |
| Circular motion, non-inertial frames, fictitious forces (centrifugal, Coriolis) | Rotation matrices and vector calculus in a rotating frame — `00-mathematical-toolkit.md` vector calculus row | Taylor, *Classical Mechanics*, ch. 9 ("Rotating Reference Frames") for the full rigorous derivation of the Coriolis/centrifugal terms from `d/dt` in a rotating basis | K&K ch. 9; Morin ch. 9 | K&K/Morin non-inertial-frame problems; these are a classic, heavily-tested IPhO category |
| Angular momentum, torque, fixed-axis rotation | Cross products, basic calculus | — | K&K ch. 5-6 | K&K ch. 5-6, Morin's rotation chapters |
| Rigid-body motion, moment of inertia, the inertia tensor | Multiple integrals (for computing `I`); eigenvalues/eigenvectors (for principal axes) — both in `00-mathematical-toolkit.md` | Goldstein, Poole & Safko, *Classical Mechanics*, ch. 4-5, for the full tensor treatment of rigid-body motion (Euler's equations, precession of asymmetric tops) — genuinely graduate material and a common source of the hardest IPhO mechanics problems in years the syllabus leans hard | K&K ch. 7; Morin's rigid-body chapter | K&K ch. 7, Morin; Kalda's *Mechanics* handout, rigid-body section |
| Gravitation, Kepler's laws, orbital mechanics | Calculus of `1/r²` force integrals; conic sections (precalculus review) | Goldstein ch. 3 ("The Kepler Problem") for the full derivation of orbit shapes from the Lagrangian/effective-potential method | K&K ch. 9-10 (gravitation sections); Morin's gravitation chapter | K&K/Morin gravitation problems; Kalda's *Mechanics* handout has a strong orbital-mechanics section |
| Simple harmonic motion, damped/driven oscillators | Linear constant-coefficient ODEs, complex exponentials — both in `00-mathematical-toolkit.md` | Full treatment in `03-oscillations-and-waves.md`, which this subtopic hands off to | Morin's oscillation chapter | Morin's problems; cross-reference `03-oscillations-and-waves.md` |
| Fluid mechanics (hydrostatics, Bernoulli's equation, basic viscosity) | Multivariable calculus, pressure as a scalar field | Landau & Lifshitz, *Fluid Mechanics* (Course of Theoretical Physics Vol. 6) for the genuinely deep version (Navier-Stokes, viscous flow) — most IPhO fluids questions never need this, but it exists if you want it | Kalda's *Hydrodynamics* handout (the primary source — standard intro texts barely cover this) | Kalda's *Hydrodynamics* handout problems |
| **Lagrangian and Hamiltonian mechanics** | Calculus of variations, the Euler-Lagrange equation (`00-mathematical-toolkit.md`) | See the dedicated section below — this is the single highest-leverage "beyond gold medalist" tool in this whole document | Taylor, *Classical Mechanics*, ch. 6-7 (Lagrangian), ch. 13 (Hamiltonian); Morin's own Lagrangian chapter as a second, more problem-focused pass | Taylor's and Morin's end-of-chapter problems; then re-solve five earlier mechanics problems from this file using Lagrangian methods instead of Newtonian force analysis, and time the difference yourself |

## Why Lagrangian mechanics is worth learning even though most IPhO solutions don't require it

This deserves its own note because it's the clearest example in this whole curriculum of Tier 2 depth directly buying IPhO-relevant speed, not just understanding. A constrained system (a bead on a rotating wire, a pendulum whose pivot itself accelerates, a block sliding on a wedge that is itself free to slide) is often a multi-page nightmare of constraint forces and free-body diagrams in Newtonian mechanics, and a five-line write-down of the kinetic and potential energy in generalized coordinates in Lagrangian mechanics. Learning it properly — not just memorizing "write `L = T - V`, take `d/dt(∂L/∂q̇) = ∂L/∂q`" but understanding *why* that equation follows from the calculus of variations applied to the action — is what lets you trust it enough to reach for it under exam time pressure instead of falling back to the slower method you're more confident in.

## Tier 2 — Graduate depth

| Source | What it adds beyond Tier 1 |
|---|---|
| Herbert Goldstein, Charles Poole & John Safko, *Classical Mechanics*, 3rd ed. | The standard first-year graduate mechanics text: full rigor on Lagrangian/Hamiltonian formalisms, rigid-body dynamics via Euler angles and the inertia tensor, canonical transformations, Hamilton-Jacobi theory |
| John R. Taylor, *Classical Mechanics* | A gentler bridge between undergraduate and Goldstein-level treatment — good as the first Lagrangian/Hamiltonian pass before Goldstein |
| L.D. Landau & E.M. Lifshitz, *Mechanics* (Course of Theoretical Physics, Vol. 1) | Extraordinarily terse and deep; derives the entire structure of classical mechanics from the principle of least action and symmetry considerations in under 200 pages — read this once Goldstein feels comfortable, not before |

## Tier 3 — Research-literature depth

| Source | Why it's here |
|---|---|
| V.I. Arnold, *Mathematical Methods of Classical Mechanics* (Springer) | Recasts all of mechanics in the language of symplectic geometry and differential forms — this is what "understanding mechanics better than a gold medalist" actually looks like: seeing conservation laws, integrability, and chaos as geometric facts about phase space, not formulas to apply |
| Emmy Noether, *Invariante Variationsprobleme*, Nachrichten von der Gesellschaft der Wissenschaften zu Göttingen (1918) — English translation: "Invariant Variation Problems," trans. M.A. Tavel, *Transport Theory and Statistical Physics* 1(3), 1971 | The original proof that every continuous symmetry of the action implies a conservation law — this is *why* momentum, energy, and angular momentum conservation exist at all, not just useful facts about them; reading the source is the difference between using Noether's theorem and understanding it |

## Problem sources specific to this topic

- Irodov, *Problems in General Physics* — mechanics chapters, worked roughly in step with the subtopics above.
- Jaan Kalda's free *Mechanics* and *Hydrodynamics* handouts — the single best bridge between the textbook material above and actual IPhO-difficulty mechanics problems; work every problem in both.
- David Morin's own book doubles as a problem source at every level from introductory to olympiad-adjacent.
- Gnädig, Honyek & Vigh, *200 Puzzling Physics Problems* and *200 More Puzzling Physics Problems* — a large fraction of both books is mechanics, and they're specifically built to require the cross-subtopic creativity (e.g., combining energy methods with a non-inertial frame) that pure textbook problems don't demand.
- The ipho-unofficial.org archive, filtered to mechanics problems by year — see `resources.md` for how to use the full past-paper archive as a problem source.

## Self-check milestone

Pick any five problems from *200 Puzzling Physics Problems*' mechanics section you haven't seen before. Solve at least three using Lagrangian mechanics as your primary method rather than Newtonian force analysis, cold, in under 20 minutes each. If you can't set up the Lagrangian confidently within the first two minutes of reading a new mechanics problem, that's a signal to revisit the Lagrangian subtopic above before moving on to `02-electromagnetism.md`.
