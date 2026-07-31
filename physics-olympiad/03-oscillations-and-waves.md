# 3. Oscillations and Waves (IPhO Syllabus: Oscillations and Waves)

This topic is the payoff for the ODE and complex-number work in `00-mathematical-toolkit.md`, and it's the direct bridge into `04-optics.md` (light is a wave) and half of `02-electromagnetism.md` (AC circuits are driven oscillators). Get the single damped-driven-oscillator equation genuinely solid here — it recurs, with only the names of the variables changed, in at least four other topics in this curriculum.

## Subtopics, in dependency order

| Subtopic | Math prerequisite (Tier 1) | If still stuck → deeper math | Physics text (Tier 1) | Tier-1 problem set |
|---|---|---|---|---|
| Simple harmonic motion | Linear, constant-coefficient, second-order ODEs — `00-mathematical-toolkit.md` | — | A.P. French, *Vibrations and Waves*, ch. 1-2 | French ch. 1-2 |
| Damped oscillations | Same ODE with a first-derivative term; complex roots of the characteristic equation | Boas ch. 8's section on complex characteristic roots if the underdamped/overdamped/critically-damped case split isn't fully clear | French ch. 3 | French ch. 3 |
| Driven oscillations, resonance | Complex exponentials as a solution method (assume `x = Ae^{iωt}`, take the real part at the end) | — | French ch. 4 | French ch. 4 |
| Coupled oscillators, normal modes | Eigenvalues/eigenvectors of the coupling matrix — `00-mathematical-toolkit.md` linear algebra row | Goldstein, *Classical Mechanics*, ch. 6 ("Small Oscillations") for the full generalized-coordinates, mass-matrix/stiffness-matrix treatment of `N` coupled oscillators at once | French ch. 5 | French ch. 5; Kalda's *Mechanics* handout also has a normal-modes section worth cross-referencing |
| The wave equation, traveling and standing waves | Partial differential equations, separation of variables — `00-mathematical-toolkit.md` | Howard Georgi, *The Physics of Waves* (free), ch. 1-2, for a full derivation of the wave equation from a discrete chain of coupled oscillators taken to the continuum limit — this is the single best way to see *why* waves and oscillators are the same physics at different scales | French ch. 6-7 | French ch. 6-7 |
| Sound waves, the Doppler effect | Same PDE machinery, applied to pressure/density fields | — | French ch. 8 | French ch. 8 |
| Superposition, beats, group vs. phase velocity | Fourier series (`00-mathematical-toolkit.md`) for the non-monochromatic case | Georgi's *Physics of Waves*, dispersion chapter, for group velocity derived properly from a wave packet's Fourier decomposition rather than the usual hand-wavy `dω/dk` definition | French's relevant sections | French's problems on this topic |

## Tier 2 — Graduate depth

| Source | What it adds beyond Tier 1 |
|---|---|
| Howard Georgi, *The Physics of Waves* (freely available, author-hosted) | A full course built entirely around the thesis that "waves" is one unified subject spanning mechanical waves, sound, E&M, and quantum wavefunctions — read this cover to cover once French feels solid, since it directly sets up both `04-optics.md` and the quantum-mechanics sections of `06-modern-physics-relativity-and-quantum.md` |
| Goldstein, Poole & Safko, *Classical Mechanics*, ch. 6 | The fully general `N`-coupled-oscillator normal-mode machinery (mass matrix, stiffness matrix, simultaneous diagonalization) — makes any finite coupled-oscillator IPhO problem, however many masses it has, look like the same three-line calculation |

## Tier 3 — Research-literature depth

| Source | Why it's here |
|---|---|
| Lord Rayleigh (John William Strutt), *The Theory of Sound* (1877, 2 volumes; public domain, widely available via Internet Archive) | The original comprehensive treatment of acoustic wave phenomena — dated notation, but the physical reasoning about resonance, normal modes, and the physics of musical instruments is still the deepest treatment most physicists will ever encounter |
| L.D. Landau & E.M. Lifshitz, *Mechanics*, the chapters on small oscillations | Landau's characteristically terse, general derivation of the normal-mode problem directly from the Lagrangian, including the general theory of parametric resonance — a genuinely research-adjacent tool (parametric resonance drives the "pumping a swing" and "Paul trap" style problems that occasionally appear at the hardest end of IPhO) |

## Problem sources specific to this topic

- French's own problems, worked chapter by chapter.
- Irodov's oscillations chapter.
- Kalda's handouts don't have a dedicated "waves" file distinct from mechanics/electromagnetism, so pull oscillation problems from those two handouts plus this topic's textbook problems.
- *200 (More) Puzzling Physics Problems*'s oscillation/wave sections.
- ipho-unofficial.org archive, filtered to oscillations/waves.

## Self-check milestone

Given an arbitrary system of `N` masses connected by springs (any topology, not just a line), write down the mass matrix and stiffness matrix directly from inspection within a few minutes, and correctly state — without fully solving the eigenvalue problem — how many normal modes it has and what symmetry, if any, lets you guess one of the mode shapes without computation.
