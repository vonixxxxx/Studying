# 6. Quantum Physics and Relativity (IPhO Syllabus: Quantum Physics and Relativity)

IPhO's modern-physics content is deliberately narrow — special relativity (no general relativity), early-quantum-theory results (photoelectric effect, Compton scattering, the Bohr model, de Broglie waves, the uncertainty principle at a qualitative/order-of-magnitude level), and basic atomic/nuclear physics. Tier 1 below matches that scope tightly; Tier 2/3 goes well past it into full quantum mechanics and general relativity, because you asked for no ceiling specifically here.

## Subtopics, in dependency order

| Subtopic | Math prerequisite — exact source, read this first | If still stuck → deeper math | Physics text (Tier 1) | Tier-1 problem set |
|---|---|---|---|---|
| Special relativity: postulates, time dilation, length contraction, simultaneity | Algebra (the Lorentz factor `γ`); spacetime diagrams need only basic geometry | — | Edwin F. Taylor & John Archibald Wheeler, *Spacetime Physics: Introduction to Special Relativity*, 2nd ed., W.H. Freeman, 1992 | Taylor & Wheeler's problems — the book is built around them, do all of them |
| Relativistic momentum and energy, `E = γmc²` | James Stewart, *Calculus: Early Transcendentals*, 8th ed., 2015, ch. 11 ("Infinite Sequences and Series") — Taylor series for the low-velocity limit that recovers Newtonian mechanics | — | Taylor & Wheeler | Taylor & Wheeler's relevant chapters |
| The photoelectric effect, photon momentum, Compton scattering | Algebra; conservation of energy/momentum applied relativistically | — | Kenneth S. Krane, *Modern Physics*, 3rd ed., Wiley, 2012 | Krane's problems |
| The Bohr model of the atom | Circular-orbit mechanics from `01-mechanics.md`, plus the ad hoc angular-momentum quantization postulate | Full quantum-mechanical derivation of hydrogen energy levels is Tier 2 below | Krane | Krane's problems |
| De Broglie waves, wave-particle duality | Basic wave concepts from `03-oscillations-and-waves.md` | — | Krane | Krane's problems |
| The uncertainty principle (qualitative/order-of-magnitude) | Mary L. Boas, *Mathematical Methods in the Physical Sciences*, 3rd ed., Wiley, 2005, ch. 7 ("Fourier Series and Transforms") — the uncertainty principle is, at bottom, a Fourier-transform fact about any wave packet | Full derivation in Tier 2 below | Krane | Krane's problems |
| Atomic and nuclear physics basics: energy levels, radioactive decay, binding energy | Morris Tenenbaum & Harry Pollard, *Ordinary Differential Equations*, Dover Publications, 1985, the lessons on exponential-decay ODEs | — | Krane | Krane's problems |

## Tier 2 — Graduate depth

| Exact source | What it adds beyond Tier 1 |
|---|---|
| David J. Griffiths, *Introduction to Quantum Mechanics*, 3rd ed. (with Darrell F. Schroeter), Cambridge University Press, 2018 | The standard first course in actual quantum mechanics: solving the Schrödinger equation for real potentials (infinite square well, harmonic oscillator, hydrogen atom), from which the Bohr model's quantized levels fall out as a special case — read ch. 1-4 (through hydrogen) |
| J.J. Sakurai & Jim Napolitano, *Modern Quantum Mechanics*, 2nd ed., Addison-Wesley/Cambridge University Press, 2011 | The standard graduate quantum text — full operator/Dirac-notation formalism, a much more rigorous uncertainty principle as a general property of non-commuting operators |
| L.D. Landau & E.M. Lifshitz, *The Classical Theory of Fields* (Course of Theoretical Physics, Vol. 2), 4th ed., Butterworth-Heinemann, 1975, the special-relativity chapters | Derives relativistic kinematics and electrodynamics together as one structure |

## Tier 3 — Research-literature depth

| Exact source | Why it's here |
|---|---|
| Albert Einstein, "Zur Elektrodynamik bewegter Körper," *Annalen der Physik*, 322(10), 1905, pp. 891–921 | The original special-relativity paper — remarkably readable; the Lorentz transformation derived from the two postulates in the order Einstein actually reasoned through it |
| Albert Einstein, "Über einen die Erzeugung und Verwandlung des Lichtes betreffenden heuristischen Gesichtspunkt," *Annalen der Physik*, 322(6), 1905, pp. 132–148 | The photoelectric-effect paper — the one that actually won Einstein his Nobel Prize |
| Niels Bohr, "On the Constitution of Atoms and Molecules, Part I," *Philosophical Magazine*, Series 6, 26(151), 1913, pp. 1–25 (first of a three-part series published through 1913) | The original derivation of the quantized-orbit atomic model, showing exactly how ad hoc the original postulate was |
| Louis de Broglie, *Recherches sur la théorie des quanta*, PhD thesis, Paris, 1924 (published in *Annales de Physique*, 10e série, tome III, 1925) | The original matter-wave hypothesis, proposed on symmetry grounds before direct experimental confirmation |
| Erwin Schrödinger, "Quantisierung als Eigenwertproblem," *Annalen der Physik*, four-part series: 384(4), 1926, pp. 361–376; 384(6), 1926, pp. 489–527; 385(13), 1926, pp. 437–490; 386(18), 1926, pp. 109–139 | The original derivation of the Schrödinger equation and its application to hydrogen — the direct source of the Griffiths Tier 2 material above |
| Charles W. Misner, Kip S. Thorne & John Archibald Wheeler, *Gravitation*, W.H. Freeman, 1973 | The standard graduate general-relativity text ("MTW") — IPhO stops at special relativity, but this is the natural next step if you want to go further, included because you asked for depth with no ceiling |

## Problem sources specific to this topic

- Taylor & Wheeler's own problems.
- Kenneth S. Krane's end-of-chapter problems.
- I.E. Irodov, *Problems in General Physics*, Mir Publishers, 1981 — atomic/nuclear/quantum chapters.
- No dedicated Kalda handout exists for this topic — lean on the ipho-unofficial.org archive's modern-physics problems by year.

## Self-check milestone

Given an unfamiliar relativistic kinematics problem (particle decay, relativistic collision), set up conservation of relativistic four-momentum correctly from scratch — and separately, derive the Bohr model's hydrogen energy levels from the angular-momentum quantization postulate alone, cold, in under 10 minutes.
