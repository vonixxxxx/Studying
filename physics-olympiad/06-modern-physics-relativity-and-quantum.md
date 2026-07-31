# 6. Quantum Physics and Relativity (IPhO Syllabus: Quantum Physics and Relativity)

IPhO's modern-physics content is deliberately narrow compared to a full undergraduate course — special relativity (no general relativity), the early-quantum-theory results (photoelectric effect, Compton scattering, the Bohr model, de Broglie waves, the uncertainty principle at a qualitative/order-of-magnitude level), and basic atomic/nuclear physics. This file's Tier 1 matches that scope tightly; Tier 2/3 is where this document goes well past it, into full quantum mechanics and general relativity, because you asked for no ceiling specifically here.

## Subtopics, in dependency order

| Subtopic | Math prerequisite (Tier 1) | If still stuck → deeper math | Physics text (Tier 1) | Tier-1 problem set |
|---|---|---|---|---|
| Special relativity: postulates, time dilation, length contraction, simultaneity | Algebra, the Lorentz factor `γ`; spacetime diagrams need only basic geometry | — | Edwin Taylor & John Archibald Wheeler, *Spacetime Physics* | Taylor & Wheeler's problems — this book is built entirely around them, do all of them |
| Relativistic momentum and energy, `E = γmc²` | Same as above, plus Taylor series (`00-mathematical-toolkit.md`) for the low-velocity limit that recovers Newtonian mechanics | — | Taylor & Wheeler | Taylor & Wheeler's relevant chapters |
| The photoelectric effect, photon momentum, Compton scattering | Algebra, conservation of energy/momentum applied relativistically | — | Kenneth Krane, *Modern Physics*, the relevant chapters | Krane's problems |
| The Bohr model of the atom | Circular-orbit mechanics from `01-mechanics.md`, plus the ad hoc angular-momentum quantization postulate | Full quantum-mechanical derivation of hydrogen energy levels belongs in Tier 2/3 below | Krane | Krane's problems |
| De Broglie waves, wave-particle duality | Basic wave concepts from `03-oscillations-and-waves.md` | — | Krane | Krane's problems |
| The uncertainty principle (qualitative/order-of-magnitude) | Fourier analysis (`00-mathematical-toolkit.md`) — the uncertainty principle is, at bottom, a Fourier-transform fact about any wave packet | Full derivation in Tier 2 below | Krane | Krane's problems |
| Atomic and nuclear physics basics: energy levels, radioactive decay, binding energy | Exponential decay (linear ODEs, `00-mathematical-toolkit.md`) | — | Krane | Krane's problems |

## Tier 2 — Graduate depth

| Source | What it adds beyond Tier 1 |
|---|---|
| David Griffiths, *Introduction to Quantum Mechanics* | The standard first course in actual quantum mechanics: solving the Schrödinger equation for real potentials (infinite square well, harmonic oscillator, hydrogen atom), from which the Bohr model's quantized energy levels fall out as a special case rather than a postulate — read chapters 1-4 (through hydrogen) as the direct depth upgrade to this file's Bohr-model and uncertainty-principle rows |
| J.J. Sakurai & Jim Napolitano, *Modern Quantum Mechanics* | The standard graduate quantum text — full operator/Dirac-notation formalism, angular momentum theory, and a much more rigorous treatment of the uncertainty principle as a general property of non-commuting operators, not just position/momentum |
| L.D. Landau & E.M. Lifshitz, *The Classical Theory of Fields* (already cited in `02-electromagnetism.md`), the special-relativity chapters | Derives relativistic kinematics and electrodynamics together as one structure — the right second pass on special relativity once Taylor & Wheeler is solid |

## Tier 3 — Research-literature depth

Modern physics is the one topic in this curriculum where reading the actual founding papers is unusually tractable and unusually rewarding, because the original 1900s papers are short, mostly non-technical by later standards, and directly readable once Tier 1 is solid.

| Source | Why it's here |
|---|---|
| Albert Einstein, "Zur Elektrodynamik bewegter Körper" ("On the Electrodynamics of Moving Bodies"), *Annalen der Physik*, 1905 | The original special-relativity paper — remarkably readable, and seeing the two postulates used to derive the Lorentz transformation from scratch, in the order Einstein actually reasoned through it, is a different (and better) education than any modern textbook's after-the-fact presentation |
| Albert Einstein, "Über einen die Erzeugung und Verwandlung des Lichtes betreffenden heuristischen Gesichtspunkt" ("On a Heuristic Viewpoint Concerning the Production and Transformation of Light"), *Annalen der Physik*, 1905 | The photoelectric-effect paper — this is the one that actually won Einstein his Nobel Prize (not relativity), and it's short enough to read in one sitting |
| Niels Bohr, "On the Constitution of Atoms and Molecules," *Philosophical Magazine*, 1913 (the first of Bohr's "trilogy" papers) | The original derivation of the quantized-orbit atomic model this file's Tier 1 uses — reading it shows exactly how ad hoc the original quantization postulate was, and why it needed the full quantum mechanics of Schrödinger and Heisenberg a decade later to actually be justified |
| Louis de Broglie, *Recherches sur la théorie des quanta* (PhD thesis, 1924; English translations available) | The original matter-wave hypothesis, proposed essentially on symmetry grounds (if light can behave as particles, perhaps particles can behave as waves) before there was any direct experimental confirmation — a striking example of a correct physical leap made from aesthetic/symmetry reasoning alone |
| Erwin Schrödinger, "Quantisierung als Eigenwertproblem" ("Quantization as an Eigenvalue Problem"), *Annalen der Physik*, 1926 (four-part series) | The original derivation of the Schrödinger equation and its application to the hydrogen atom — the direct source of the Tier 2 Griffiths material above |
| Charles Misner, Kip Thorne & John Wheeler, *Gravitation* (San Francisco: W.H. Freeman) | IPhO's syllabus stops at special relativity, but if you want to go past it: this is the standard graduate general-relativity text ("MTW"), famously exhaustive — genuinely optional, included because you asked specifically for depth with no ceiling, and general relativity is the natural next step after special relativity is solid |

## Problem sources specific to this topic

- Taylor & Wheeler's own problems (extensive, and the book is structured around them).
- Krane's end-of-chapter problems.
- Irodov's atomic/nuclear/quantum chapters.
- Kalda does not maintain a dedicated relativity/quantum handout; lean directly on the ipho-unofficial.org archive's modern-physics problems by year, since this is the topic where past-paper practice matters most relative to a dedicated problem book.

## Self-check milestone

Given an unfamiliar relativistic kinematics problem (e.g., particle decay, relativistic collision), set up conservation of relativistic four-momentum correctly from scratch, without needing to look up which combination of `E` and `p` conserves — and separately, derive the Bohr model's hydrogen energy levels from the angular-momentum quantization postulate alone, cold, in under 10 minutes, as a check that the Tier-1 derivation (not just the final formula) is actually owned.
