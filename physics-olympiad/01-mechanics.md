# 1. Mechanics (IPhO Syllabus: Mechanics)

Mechanics is the largest single component of almost every IPhO paper and the topic where the gap between "can solve textbook problems" and "can solve IPhO problems" is widest, because the hard problems are almost always textbook mechanics plus one extra structural idea (a constraint, a non-inertial frame, an energy method that avoids messy force analysis, or a symmetry that makes Lagrangian mechanics dramatically faster than Newtonian bookkeeping). Every math reference below is given in full — book, edition, publisher, year, and chapter title — so you shouldn't need to leave this file to know exactly what to go read.

## Subtopics, in dependency order

| Subtopic | Math prerequisite — exact source, read this first | If still stuck → deeper math | Physics text (Tier 1) | Tier-1 problem set |
|---|---|---|---|---|
| Vectors, 1D/2D kinematics | James Stewart, *Calculus: Early Transcendentals*, 8th ed., Cengage Learning, 2015, ch. 12 ("Vectors and the Geometry of Space"); H.M. Schey, *Div, Grad, Curl, and All That*, 4th ed., W.W. Norton & Company, 2005, opening chapter on vector algebra | — | Daniel Kleppner & Robert Kolenkow, *An Introduction to Mechanics*, 2nd ed., Cambridge University Press, 2013, ch. 1 ("Vectors and Kinematics"); David Morin, *Introduction to Classical Mechanics: With Problems and Solutions*, Cambridge University Press, 2008, ch. 1 | K&K ch. 1 + Morin ch. 1, all problems |
| Newton's laws, forces (friction, tension, springs) | Morris Tenenbaum & Harry Pollard, *Ordinary Differential Equations*, Dover Publications, 1985, the lessons on simple first- and second-order ODEs (`F = ma` is already a second-order ODE) | Same book's lessons on linear ODEs with constant coefficients, if the differential-equation framing feels unfamiliar | K&K ch. 2 ("Newton's Laws") and ch. 3 ("Forces and Equations of Motion"); Morin ch. 2-3 | K&K ch. 2-3, Morin ch. 2-3; begin I.E. Irodov, *Problems in General Physics*, Mir Publishers, 1981, mechanics chapter |
| Work, energy, conservative forces | Stewart, ch. 16 ("Vector Calculus"), the line-integral sections (work as `∫F·dl`) | Schey's chapters on divergence and curl, to understand *why* only some forces are conservative (curl-free) | K&K's energy chapter; Morin ch. 3-4 | Same, plus Jaan Kalda's *Mechanics* handout (Institute of Cybernetics, Tallinn University of Technology — free; search "Jaan Kalda physics olympiad handouts"), energy-method section |
| Momentum, collisions, center of mass | — (algebra-level once vectors are solid) | — | K&K ch. 4 ("Momentum"); Morin ch. 3 | K&K ch. 4, Morin ch. 3 |
| Circular motion, non-inertial frames, fictitious forces (centrifugal, Coriolis) | Schey's vector-calculus chapters, applied to `d/dt` of a vector in a rotating basis | John R. Taylor, *Classical Mechanics*, University Science Books, 2005, ch. 9 ("Rotating Reference Frames") for the full rigorous derivation of the Coriolis/centrifugal terms | K&K ch. 8 ("Non-inertial Systems and Fictitious Forces"); Morin's non-inertial-frame chapter | K&K/Morin non-inertial-frame problems — a classic, heavily-tested IPhO category |
| Angular momentum, torque, fixed-axis rotation | Stewart, ch. 12, cross-product sections | — | K&K's angular-momentum chapters | K&K, Morin's rotation chapters |
| Rigid-body motion, moment of inertia, the inertia tensor | Stewart, ch. 15 ("Multiple Integrals"), for computing `I`; Strang, *Introduction to Linear Algebra*, 5th ed., Wellesley-Cambridge Press, 2016, the "Eigenvalues and Eigenvectors" chapter, for principal axes | Herbert Goldstein, Charles P. Poole Jr. & John L. Safko, *Classical Mechanics*, 3rd ed., Addison Wesley, 2002, ch. 4-5, for the full tensor treatment (Euler's equations, precession of asymmetric tops) — genuinely graduate material and a common source of the hardest IPhO mechanics problems | K&K's rigid-body chapter; Morin's rigid-body chapter | K&K, Morin; Kalda's *Mechanics* handout, rigid-body section |
| Gravitation, Kepler's laws, orbital mechanics | Stewart's integral-calculus chapters (for `1/r²` force integrals); OpenStax *Precalculus* conic-sections review | Goldstein, Poole & Safko, ch. 3 ("The Kepler Problem"), for orbit shapes from the Lagrangian/effective-potential method | K&K's gravitation sections; Morin's gravitation chapter | K&K/Morin gravitation problems; Kalda's *Mechanics* handout's orbital-mechanics section |
| Simple harmonic motion, damped/driven oscillators | Tenenbaum & Pollard, the lessons on linear constant-coefficient ODEs; Boas, *Mathematical Methods in the Physical Sciences*, 3rd ed., Wiley, 2005, ch. 2 ("Complex Numbers") for the complex-exponential solution method | Full treatment in `03-oscillations-and-waves.md` | Morin's oscillation chapter | Morin's problems; cross-reference `03-oscillations-and-waves.md` |
| Fluid mechanics (hydrostatics, Bernoulli's equation, basic viscosity) | Stewart, ch. 14-15 (multivariable calculus; pressure as a scalar field) | L.D. Landau & E.M. Lifshitz, *Fluid Mechanics* (Course of Theoretical Physics, Vol. 6), 2nd ed., Butterworth-Heinemann, 1987, for the genuinely deep version (Navier-Stokes, viscous flow) | Jaan Kalda's *Hydrodynamics* handout — the primary source, since standard intro texts barely cover this | Kalda's *Hydrodynamics* handout problems |
| **Lagrangian and Hamiltonian mechanics** | Boas, ch. 9 ("Calculus of Variations") — the Euler-Lagrange equation | Cornelius Lanczos, *The Variational Principles of Mechanics*, 4th ed., Dover Publications, 1970 | Taylor, *Classical Mechanics*, ch. 6-7 (Lagrangian), ch. 13 (Hamiltonian); Morin's own Lagrangian chapter | Taylor's and Morin's end-of-chapter problems; then re-solve five earlier mechanics problems from this file using Lagrangian methods and time the difference yourself |

## Why Lagrangian mechanics is worth learning even though most IPhO solutions don't require it

A constrained system (a bead on a rotating wire, a pendulum whose pivot itself accelerates, a block sliding on a wedge that is itself free to slide) is often a multi-page nightmare of constraint forces and free-body diagrams in Newtonian mechanics, and a five-line write-down of the kinetic and potential energy in generalized coordinates in Lagrangian mechanics. Understanding *why* `d/dt(∂L/∂q̇) = ∂L/∂q` follows from the calculus of variations applied to the action — not just memorizing the recipe — is what lets you trust it enough to reach for it under exam time pressure.

## Tier 2 — Graduate depth

| Exact source | What it adds beyond Tier 1 |
|---|---|
| Herbert Goldstein, Charles P. Poole Jr. & John L. Safko, *Classical Mechanics*, 3rd ed., Addison Wesley, 2002 | The standard first-year graduate mechanics text: full rigor on Lagrangian/Hamiltonian formalisms, rigid-body dynamics via Euler angles and the inertia tensor, canonical transformations, Hamilton-Jacobi theory |
| John R. Taylor, *Classical Mechanics*, University Science Books, 2005 | A gentler bridge between undergraduate and Goldstein-level treatment |
| L.D. Landau & E.M. Lifshitz, *Mechanics* (Course of Theoretical Physics, Vol. 1), 3rd ed., Butterworth-Heinemann, 1976 | Extraordinarily terse and deep; derives the entire structure of classical mechanics from the principle of least action and symmetry considerations in under 200 pages — read once Goldstein is comfortable |

## Tier 3 — Research-literature depth

| Exact source | Why it's here |
|---|---|
| V.I. Arnold, *Mathematical Methods of Classical Mechanics*, 2nd ed., Springer, 1989 (Graduate Texts in Mathematics, Vol. 60) | Recasts all of mechanics in the language of symplectic geometry and differential forms — conservation laws, integrability, and chaos as geometric facts about phase space |
| Emmy Noether, "Invariante Variationsprobleme," *Nachrichten von der Königlichen Gesellschaft der Wissenschaften zu Göttingen, Mathematisch-physikalische Klasse*, 1918, pp. 235–257. English translation: M.A. Tavel, "Invariant Variation Problems," *Transport Theory and Statistical Physics*, 1(3), 1971, pp. 183–207 | The original proof that every continuous symmetry of the action implies a conservation law — *why* momentum, energy, and angular momentum conservation exist at all |

## Problem sources specific to this topic

- I.E. Irodov, *Problems in General Physics*, Mir Publishers, 1981 — mechanics chapters.
- Jaan Kalda's free *Mechanics* and *Hydrodynamics* handouts.
- David Morin's textbook doubles as a problem source at every level.
- P. Gnädig, G. Honyek & K.F. Vigh, *200 Puzzling Physics Problems: With Hints and Solutions*, Cambridge University Press, 2001, and P. Gnädig, G. Honyek, M. Vigh & K.F. Riley, *200 More Puzzling Physics Problems: With Hints and Solutions*, Cambridge University Press, 2016 — mechanics sections.
- ipho-unofficial.org archive, filtered to mechanics problems by year.

## Self-check milestone

Pick any five problems from *200 Puzzling Physics Problems*' mechanics section you haven't seen before. Solve at least three using Lagrangian mechanics as your primary method rather than Newtonian force analysis, cold, in under 20 minutes each.
