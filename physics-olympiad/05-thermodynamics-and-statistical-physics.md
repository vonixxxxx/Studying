# 5. Thermodynamics and Statistical Physics (IPhO Syllabus: Thermodynamics and Statistical Physics)

This is the topic where the gap between "Tier 1 gets you through IPhO" and "Tier 2/3 genuinely changes how you think about the subject" is largest. Standard undergraduate thermodynamics presents entropy and the ideal gas law as things you apply; statistical mechanics explains why they're true at all, in a way that makes half of the Tier-1 formulas feel derivable on the spot instead of memorized.

## Subtopics, in dependency order

| Subtopic | Math prerequisite (Tier 1) | If still stuck → deeper math | Physics text (Tier 1) | Tier-1 problem set |
|---|---|---|---|---|
| The zeroth and first laws, heat, work, internal energy | Basic calculus, exact vs. inexact differentials (a genuinely subtle point — heat and work are path-dependent, internal energy isn't) | Boas ch. 4's treatment of exact differentials and partial derivatives, applied specifically to this distinction | Daniel Schroeder, *An Introduction to Thermal Physics*, ch. 1 | Schroeder ch. 1 |
| Ideal gases, kinetic theory | Multivariable calculus, basic probability (Maxwell-Boltzmann as a probability distribution) | — | Schroeder ch. 1 (kinetic theory) | Schroeder's problems |
| The second law, entropy, reversibility | Combinatorics/counting microstates — `00-mathematical-toolkit.md` probability row | — | Schroeder ch. 2-3 (Schroeder's ch. 2 derivation of entropy from counting microstates of simple toy systems, before ever invoking heat engines, is the best available undergraduate treatment of *why* entropy is defined the way it is) | Schroeder ch. 2-3 |
| Heat engines, refrigerators, the Carnot cycle | Basic calculus (`∮ dQ/T`) | — | Schroeder ch. 4 | Schroeder ch. 4 |
| Thermodynamic potentials (enthalpy, free energy) and Maxwell relations | Partial derivatives, exact differentials again, now with multiple variables | Callen, *Thermodynamics and an Introduction to Thermostatistics*, ch. 5-7, for the fully axiomatic derivation of all four potentials and the Maxwell relations from a single postulate structure — most IPhO prep skips this, and it's a genuine Tier 2 upgrade | Schroeder ch. 5 | Schroeder ch. 5 |
| The Boltzmann distribution, partition functions | Exponentials, sums/integrals over states, basic combinatorics | — | Schroeder ch. 6 | Schroeder ch. 6 |
| Basic statistical mechanics of gases, the equipartition theorem | Multivariable calculus (Gaussian integrals) | — | Schroeder ch. 6-7 | Schroeder ch. 6-7 |
| Phase transitions (qualitative) | — | Full quantitative treatment (critical exponents, mean-field theory) belongs to Tier 3 below | Schroeder ch. 5 | Schroeder's problems |

## Tier 2 — Graduate depth

| Source | What it adds beyond Tier 1 |
|---|---|
| Herbert Callen, *Thermodynamics and an Introduction to Thermostatistics* | The classic axiomatic treatment — builds all of thermodynamics from a small set of postulates about entropy maximization, which retroactively makes every Tier-1 formula look like a special case of one idea rather than a list of separate laws |
| Mehran Kardar, *Statistical Physics of Particles* (Cambridge; Kardar's original MIT 8.333 lecture notes are freely available via MIT OpenCourseWare) | A modern, rigorous graduate statistical-mechanics course — ensembles (microcanonical/canonical/grand canonical) derived carefully and connected explicitly back to the kinetic-theory and entropy-counting arguments in Schroeder |

## Tier 3 — Research-literature depth

| Source | Why it's here |
|---|---|
| L.D. Landau & E.M. Lifshitz, *Statistical Physics, Part 1* (Course of Theoretical Physics, Vol. 5) | Extremely dense, extremely deep — derives the entire ensemble formalism and thermodynamic relations from first principles with almost no wasted motion; read this once Kardar feels comfortable |
| J. Willard Gibbs, *Elementary Principles in Statistical Mechanics* (1902; public domain, widely available via Internet Archive/Project Gutenberg) | The founding text of statistical mechanics as a formal subject — Gibbs is the origin of the ensemble concept used in every modern textbook, including Schroeder and Kardar above |
| Ludwig Boltzmann's original papers on the H-theorem and the statistical definition of entropy (1870s, collected and discussed in most graduate stat-mech textbooks' historical notes) | Seeing entropy increase derived from molecular collision statistics, by the person who first did it, and understanding the controversy it caused at the time (the reversibility and recurrence objections), is a genuinely deeper education in what the second law actually claims than any modern restatement |
| Mehran Kardar, *Statistical Physics of Fields* (Cambridge) | Goes past particle statistical mechanics into field-theoretic methods (renormalization group, critical phenomena) — far past anything IPhO needs, included only because you asked for no ceiling on this specific topic, where the undergraduate-to-research gap is especially large |

## Problem sources specific to this topic

- Schroeder's own problems — unusually well-designed and worth doing in full, not skimmed.
- Irodov's thermodynamics chapter.
- Kalda's *Thermodynamics/Statistical Physics* handout — as with the other Kalda material, this is where textbook thermodynamics turns into IPhO-difficulty thermodynamics (cycles with unusual paths, combined thermodynamics-and-mechanics problems like pistons with masses on springs).
- *200 (More) Puzzling Physics Problems*'s thermodynamics sections.
- ipho-unofficial.org archive, filtered to thermodynamics.

## Self-check milestone

Given an arbitrary (non-Carnot) thermodynamic cycle drawn on a P-V diagram, correctly compute the work done, heat exchanged in each leg, and the overall efficiency without needing to look up which formula applies to which leg — this requires actually understanding `dU = dQ - dW` well enough to apply it fresh to an unfamiliar path, which is exactly what separates Tier-1-memorized thermodynamics from Tier-1-understood thermodynamics.
