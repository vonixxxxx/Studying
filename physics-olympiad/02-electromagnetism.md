# 2. Electricity and Magnetism (IPhO Syllabus: Electric Charges and Fields, Electric Current, Magnetic Field)

E&M is where the vector-calculus investment from `00-mathematical-toolkit.md` pays off directly and immediately — nearly every derivation in this topic (Gauss's law, Ampère's law, Faraday's law) is a vector-calculus integral theorem applied to a specific symmetry. If the math prerequisite row below feels shaky, stop and fix it before touching the physics chapter; trying to memorize Gauss's law's applications without owning the divergence theorem is the single most common reason this topic feels like a wall of unrelated formulas instead of one coherent idea applied repeatedly.

## Subtopics, in dependency order

| Subtopic | Math prerequisite (Tier 1) | If still stuck → deeper math | Physics text (Tier 1) | Tier-1 problem set |
|---|---|---|---|---|
| Coulomb's law, electric field, superposition | Vector algebra, `1/r²` integrals | — | Purcell & Morin, *Electricity and Magnetism* (3rd ed.), ch. 1-2 | Purcell & Morin ch. 1-2 |
| Electric potential, potential energy | Line integrals (`00-mathematical-toolkit.md`) | — | Purcell & Morin ch. 2 | Same |
| Gauss's law | The divergence theorem — Schey, *Div, Grad, Curl*, in full, before this subtopic | Griffiths, *Introduction to Electrodynamics*, ch. 1 (vector calculus primer) then ch. 2 for Gauss's law derived from `∇·E = ρ/ε₀` | Purcell & Morin ch. 1 (Purcell's geometric derivation, unusually intuitive); Griffiths ch. 2 for the differential-form version | Purcell & Morin's Gauss's-law problems — deliberately chosen for high-symmetry setups where the law does most of the work |
| Conductors, capacitance, dielectrics | Multivariable calculus | — | Purcell & Morin ch. 3 | Purcell & Morin ch. 3 |
| DC circuits, Kirchhoff's laws, RC transients | Linear ODEs (`00-mathematical-toolkit.md`, for the RC time-constant equation) | — | Purcell & Morin ch. 4 | Purcell & Morin ch. 4; build a real RC circuit and measure the time constant (this is also `07-experimental-physics.md`'s first assignment) |
| Magnetic fields and forces, the Biot-Savart law | Cross products, line integrals | — | Purcell & Morin ch. 5-6 | Purcell & Morin ch. 5-6 |
| Ampère's law | Stokes' theorem — Schey, ch. on curl and Stokes' theorem, before this subtopic | Griffiths ch. 5 for the differential-form derivation `∇×B = μ₀J` | Purcell & Morin ch. 6 | Purcell & Morin's high-symmetry Ampère's-law problems |
| Electromagnetic induction, Faraday's/Lenz's law, inductance | Time-derivatives of flux integrals (combines earlier vector-calculus and calculus rows) | — | Purcell & Morin ch. 7 | Purcell & Morin ch. 7 |
| AC circuits, impedance, resonance | Complex exponentials (`00-mathematical-toolkit.md`) | — | Purcell & Morin ch. 8 | Purcell & Morin ch. 8; Kalda's *Electromagnetism* handout's AC-circuit section |
| Maxwell's equations, unification and the displacement current | All of the above combined | See Tier 2/3 below for the full relativistic unification | Purcell & Morin ch. 9 (their treatment of Maxwell's equations is unusually clear about *why* the displacement current is necessary for consistency) | Purcell & Morin ch. 9 |

## Tier 2 — Graduate depth

| Source | What it adds beyond Tier 1 |
|---|---|
| David Griffiths, *Introduction to Electrodynamics* (through ch. 9-11) | A more systematic, differential-equations-first treatment than Purcell & Morin — read this as your second pass through the whole topic once Tier 1 is solid, and use ch. 12 ("Electrodynamics and Relativity") as your bridge to `06-modern-physics-relativity-and-quantum.md` |
| J.D. Jackson, *Classical Electrodynamics*, 3rd ed. | *The* graduate standard — notoriously demanding, covers multipole expansions, radiation, waveguides, and relativistic electrodynamics with full mathematical rigor. Reading even the first few chapters carefully will make every Tier-1 symmetry argument feel like a special case of a much more general machine you now understand |

## Tier 3 — Research-literature depth

| Source | Why it's here |
|---|---|
| L.D. Landau & E.M. Lifshitz, *The Classical Theory of Fields* (Course of Theoretical Physics, Vol. 2) | Derives electrodynamics *from* special relativity (the field tensor formulation) rather than bolting relativity on afterward — the single best source for seeing E&M and relativity as one theory, not two |
| James Clerk Maxwell, *A Treatise on Electricity and Magnetism* (1873; public domain, widely available via Internet Archive/Project Gutenberg) | The original synthesis, in Maxwell's own (admittedly archaic, quaternion-flavored) notation — worth sampling the sections on the displacement current and electromagnetic waves specifically, where you can watch the unification actually happen historically rather than being handed the four equations as a fait accompli |

## Problem sources specific to this topic

- Irodov's electricity and magnetism chapters.
- Jaan Kalda's *Electromagnetism* handout — as with mechanics, this is the primary bridge to genuine IPhO difficulty, and it explicitly drills the symmetry-recognition skill ("this charge distribution has enough symmetry for Gauss's law to work in one line") that a first read of Purcell doesn't fully train.
- *200 (More) Puzzling Physics Problems* — the E&M sections lean heavily on exactly the kind of clever-symmetry-choice problems Kalda also emphasizes.
- ipho-unofficial.org archive, filtered to E&M problems.

## Self-check milestone

Given an unfamiliar charge or current distribution, decide within 30 seconds whether it has enough symmetry for Gauss's/Ampère's law to apply directly, and if not, correctly identify that you need to fall back to direct integration (Coulomb's law/Biot-Savart) or a potential-based method instead. This recognition speed — not the ability to execute the integral once you know which one to do — is the actual bottleneck in timed E&M problems.
