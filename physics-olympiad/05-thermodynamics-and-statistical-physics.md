# 5. Thermodynamics and Statistical Physics (IPhO Syllabus: Thermodynamics and Statistical Physics)

This is the topic where the gap between "Tier 1 gets you through IPhO" and "Tier 2/3 genuinely changes how you think" is largest. Standard undergraduate thermodynamics presents entropy and the ideal gas law as things you apply; statistical mechanics explains why they're true, in a way that makes half the Tier-1 formulas derivable on the spot instead of memorized.

## Subtopics, in dependency order

| Subtopic | Math prerequisite — exact source, read this first | If still stuck → deeper math | Physics text (Tier 1) | Tier-1 problem set |
|---|---|---|---|---|
| The zeroth and first laws, heat, work, internal energy | Mary L. Boas, *Mathematical Methods in the Physical Sciences*, 3rd ed., Wiley, 2005, ch. 4 ("Partial Differentiation") — exact vs. inexact differentials | — | Daniel V. Schroeder, *An Introduction to Thermal Physics*, Addison Wesley Longman, 2000, ch. 1 | Schroeder ch. 1 |
| Ideal gases, kinetic theory | James Stewart, *Calculus: Early Transcendentals*, 8th ed., 2015, ch. 14-15 (multivariable calculus); Boas, ch. 15 ("Probability and Statistics") | — | Schroeder, ch. 1 (kinetic theory) | Schroeder's problems |
| The second law, entropy, reversibility | Boas, ch. 15 ("Probability and Statistics") — combinatorics/counting microstates | — | Schroeder, ch. 2-3 (Schroeder's microstate-counting derivation of entropy, before ever invoking heat engines, is the best available undergraduate treatment) | Schroeder ch. 2-3 |
| Heat engines, refrigerators, the Carnot cycle | Stewart, ch. 5-7 (`∮ dQ/T` as a line/path integral) | — | Schroeder, ch. 4 | Schroeder ch. 4 |
| Thermodynamic potentials (enthalpy, free energy) and Maxwell relations | Boas, ch. 4 ("Partial Differentiation") — exact differentials with multiple variables | Herbert B. Callen, *Thermodynamics and an Introduction to Thermostatistics*, 2nd ed., Wiley, 1985, ch. 5-7, for the fully axiomatic derivation of all four potentials and Maxwell relations | Schroeder, ch. 5 | Schroeder ch. 5 |
| The Boltzmann distribution, partition functions | Stewart, exponentials/series review; Boas, ch. 15 | — | Schroeder, ch. 6 | Schroeder ch. 6 |
| Basic statistical mechanics of gases, the equipartition theorem | Stewart, ch. 15 ("Multiple Integrals" — Gaussian integrals) | — | Schroeder, ch. 6-7 | Schroeder ch. 6-7 |
| Phase transitions (qualitative) | — | Full quantitative treatment (critical exponents, mean-field theory) is Tier 3 below | Schroeder, ch. 5 | Schroeder's problems |

## Tier 2 — Graduate depth

| Exact source | What it adds beyond Tier 1 |
|---|---|
| Herbert B. Callen, *Thermodynamics and an Introduction to Thermostatistics*, 2nd ed., Wiley, 1985 | The classic axiomatic treatment — builds all of thermodynamics from postulates about entropy maximization |
| Mehran Kardar, *Statistical Physics of Particles*, Cambridge University Press, 2007 (Kardar's original MIT 8.333 lecture notes are freely available via MIT OpenCourseWare) | A modern, rigorous graduate statistical-mechanics course — ensembles (microcanonical/canonical/grand canonical) derived carefully |

## Tier 3 — Research-literature depth

| Exact source | Why it's here |
|---|---|
| L.D. Landau & E.M. Lifshitz, *Statistical Physics, Part 1* (Course of Theoretical Physics, Vol. 5), 3rd ed., Butterworth-Heinemann, 1980 | Extremely dense, extremely deep derivation of the ensemble formalism and thermodynamic relations from first principles |
| J. Willard Gibbs, *Elementary Principles in Statistical Mechanics, Developed with Especial Reference to the Rational Foundation of Thermodynamics*, Charles Scribner's Sons, 1902 (public domain, widely available via Internet Archive/Project Gutenberg) | The founding text of statistical mechanics as a formal subject — the origin of the ensemble concept used in Schroeder and Kardar above |
| Ludwig Boltzmann, "Weitere Studien über das Wärmegleichgewicht unter Gasmolekülen" ("Further Studies on the Thermal Equilibrium of Gas Molecules"), *Sitzungsberichte der Akademie der Wissenschaften Wien*, 66, 1872, pp. 275–370 (the H-theorem paper) | Entropy increase derived from molecular collision statistics by the person who first did it, including the reversibility/recurrence controversy it provoked |
| Mehran Kardar, *Statistical Physics of Fields*, Cambridge University Press, 2007 | Field-theoretic methods (renormalization group, critical phenomena) — far past IPhO, included because you asked for no ceiling specifically on this topic |

## Problem sources specific to this topic

- Daniel V. Schroeder's own problems — unusually well-designed, worth doing in full.
- I.E. Irodov, *Problems in General Physics*, Mir Publishers, 1981 — thermodynamics chapter.
- Jaan Kalda's *Thermodynamics/Statistical Physics* handout — where textbook thermodynamics turns into IPhO-difficulty thermodynamics.
- P. Gnädig, G. Honyek & K.F. Vigh, *200 Puzzling Physics Problems*, Cambridge University Press, 2001, and its 2016 sequel — thermodynamics sections.
- ipho-unofficial.org archive, filtered to thermodynamics.

## Self-check milestone

Given an arbitrary (non-Carnot) thermodynamic cycle on a P-V diagram, correctly compute the work, heat exchanged in each leg, and overall efficiency without looking up which formula applies to which leg.
