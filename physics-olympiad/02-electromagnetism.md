# 2. Electricity and Magnetism (IPhO Syllabus: Electric Charges and Fields, Electric Current, Magnetic Field)

E&M is where the vector-calculus investment pays off directly — nearly every derivation here (Gauss's law, Ampère's law, Faraday's law) is a vector-calculus integral theorem applied to a specific symmetry. If a math-prerequisite row below feels shaky, stop and fix it before touching the physics chapter.

## Subtopics, in dependency order

| Subtopic | Math prerequisite — exact source, read this first | If still stuck → deeper math | Physics text (Tier 1) | Tier-1 problem set |
|---|---|---|---|---|
| Coulomb's law, electric field, superposition | James Stewart, *Calculus: Early Transcendentals*, 8th ed., Cengage Learning, 2015, ch. 12 (vector algebra); ch. 5/7 (`1/r²` integrals) | — | Edward M. Purcell & David J. Morin, *Electricity and Magnetism*, 3rd ed., Cambridge University Press, 2013, ch. 1-2 | Purcell & Morin ch. 1-2 |
| Electric potential, potential energy | Stewart, ch. 16 ("Vector Calculus"), line-integral sections | — | Purcell & Morin, ch. 2 | Same |
| Gauss's law | H.M. Schey, *Div, Grad, Curl, and All That*, 4th ed., W.W. Norton & Company, 2005, the divergence-theorem chapter, in full, before this subtopic | David J. Griffiths, *Introduction to Electrodynamics*, 4th ed., Cambridge University Press, 2017, ch. 1 (vector-calculus primer) then ch. 2 for `∇·E = ρ/ε₀` | Purcell & Morin, ch. 1 (Purcell's geometric derivation); Griffiths ch. 2 for the differential-form version | Purcell & Morin's Gauss's-law problems (high-symmetry setups) |
| Conductors, capacitance, dielectrics | Stewart, ch. 14-15 (multivariable calculus) | — | Purcell & Morin, ch. 3 | Purcell & Morin ch. 3 |
| DC circuits, Kirchhoff's laws, RC transients | Morris Tenenbaum & Harry Pollard, *Ordinary Differential Equations*, Dover Publications, 1985, the lessons on first-order linear ODEs (the RC time-constant equation) | — | Purcell & Morin, ch. 4 | Purcell & Morin ch. 4; build a real RC circuit and measure the time constant (also `07-experimental-physics.md`'s first assignment) |
| Magnetic fields and forces, the Biot-Savart law | Stewart, cross-product and line-integral sections | — | Purcell & Morin, ch. 5-6 | Purcell & Morin ch. 5-6 |
| Ampère's law | Schey, the curl-and-Stokes'-theorem chapter, before this subtopic | Griffiths, ch. 5, for the differential-form derivation `∇×B = μ₀J` | Purcell & Morin, ch. 6 | Purcell & Morin's high-symmetry Ampère's-law problems |
| Electromagnetic induction, Faraday's/Lenz's law, inductance | Combines the vector-calculus (flux integrals) and single-variable-calculus (time derivatives) rows above | — | Purcell & Morin, ch. 7 | Purcell & Morin ch. 7 |
| AC circuits, impedance, resonance | Mary L. Boas, *Mathematical Methods in the Physical Sciences*, 3rd ed., Wiley, 2005, ch. 2 ("Complex Numbers") | — | Purcell & Morin, ch. 8 | Purcell & Morin ch. 8; Kalda's *Electromagnetism* handout, AC-circuit section |
| Maxwell's equations, unification and the displacement current | All rows above, combined | See Tier 2/3 below for the full relativistic unification | Purcell & Morin, ch. 9 | Purcell & Morin ch. 9 |

## Tier 2 — Graduate depth

| Exact source | What it adds beyond Tier 1 |
|---|---|
| David J. Griffiths, *Introduction to Electrodynamics*, 4th ed., Cambridge University Press, 2017 (through ch. 9-11) | A more systematic, differential-equations-first treatment than Purcell & Morin — use ch. 12 ("Electrodynamics and Relativity") as the bridge to `06-modern-physics-relativity-and-quantum.md` |
| J.D. Jackson, *Classical Electrodynamics*, 3rd ed., Wiley, 1998 | *The* graduate standard — multipole expansions, radiation, waveguides, relativistic electrodynamics with full mathematical rigor |

## Tier 3 — Research-literature depth

| Exact source | Why it's here |
|---|---|
| L.D. Landau & E.M. Lifshitz, *The Classical Theory of Fields* (Course of Theoretical Physics, Vol. 2), 4th ed., Butterworth-Heinemann, 1975 | Derives electrodynamics *from* special relativity (the field-tensor formulation) rather than bolting relativity on afterward |
| James Clerk Maxwell, *A Treatise on Electricity and Magnetism*, Clarendon Press, Oxford, 1873 (2 volumes; public domain, widely available via Internet Archive/Project Gutenberg) | The original synthesis, in Maxwell's own notation — read the sections on the displacement current and electromagnetic waves specifically |

## Problem sources specific to this topic

- I.E. Irodov, *Problems in General Physics*, Mir Publishers, 1981 — electricity and magnetism chapters.
- Jaan Kalda's *Electromagnetism* handout (free; search "Jaan Kalda physics olympiad handouts").
- P. Gnädig, G. Honyek & K.F. Vigh, *200 Puzzling Physics Problems*, Cambridge University Press, 2001, and P. Gnädig, G. Honyek, M. Vigh & K.F. Riley, *200 More Puzzling Physics Problems*, Cambridge University Press, 2016 — E&M sections.
- ipho-unofficial.org archive, filtered to E&M problems.

## Self-check milestone

Given an unfamiliar charge or current distribution, decide within 30 seconds whether it has enough symmetry for Gauss's/Ampère's law to apply directly, and if not, correctly fall back to direct integration (Coulomb's law/Biot-Savart) or a potential-based method.
