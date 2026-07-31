# 3. Oscillations and Waves (IPhO Syllabus: Oscillations and Waves)

This topic is the payoff for the ODE and complex-number work below, and the direct bridge into `04-optics.md` (light is a wave) and half of `02-electromagnetism.md` (AC circuits are driven oscillators). Get the single damped-driven-oscillator equation genuinely solid here — it recurs, with only the variable names changed, in at least four other topics in this curriculum.

## Subtopics, in dependency order

| Subtopic | Math prerequisite — exact source, read this first | If still stuck → deeper math | Physics text (Tier 1) | Tier-1 problem set |
|---|---|---|---|---|
| Simple harmonic motion | Morris Tenenbaum & Harry Pollard, *Ordinary Differential Equations*, Dover Publications, 1985, the lessons on linear, constant-coefficient, second-order ODEs | — | A.P. French, *Vibrations and Waves* (MIT Introductory Physics Series), W.W. Norton & Company, 1971, ch. 1-2 | French ch. 1-2 |
| Damped oscillations | Same Tenenbaum & Pollard lessons, the case of complex roots of the characteristic equation | Mary L. Boas, *Mathematical Methods in the Physical Sciences*, 3rd ed., Wiley, 2005, ch. 8 ("Ordinary Differential Equations"), the section on complex characteristic roots | French, ch. 3 | French ch. 3 |
| Driven oscillations, resonance | Boas, ch. 2 ("Complex Numbers") — assume `x = Ae^{iωt}`, take the real part at the end | — | French, ch. 4 | French ch. 4 |
| Coupled oscillators, normal modes | Gilbert Strang, *Introduction to Linear Algebra*, 5th ed., Wellesley-Cambridge Press, 2016, the "Eigenvalues and Eigenvectors" chapter | Herbert Goldstein, Charles P. Poole Jr. & John L. Safko, *Classical Mechanics*, 3rd ed., Addison Wesley, 2002, ch. 6 ("Small Oscillations") for the full `N`-body mass-matrix/stiffness-matrix treatment | French, ch. 5 | French ch. 5; Kalda's *Mechanics* handout also has a normal-modes section |
| The wave equation, traveling and standing waves | Boas, ch. 13 ("Partial Differential Equations"), separation of variables | Howard Georgi, *The Physics of Waves*, Prentice Hall, 1993 (free, author-hosted PDF), ch. 1-2, deriving the wave equation from a discrete chain of coupled oscillators taken to the continuum limit | French, ch. 6-7 | French ch. 6-7 |
| Sound waves, the Doppler effect | Same PDE machinery, applied to pressure/density fields | — | French, ch. 8 | French ch. 8 |
| Superposition, beats, group vs. phase velocity | Boas, ch. 7 ("Fourier Series and Transforms") | Georgi's dispersion chapter, deriving group velocity properly from a wave packet's Fourier decomposition | French's relevant sections | French's problems on this topic |

## Tier 2 — Graduate depth

| Exact source | What it adds beyond Tier 1 |
|---|---|
| Howard Georgi, *The Physics of Waves*, Prentice Hall, 1993 (freely available, author-hosted) | A full course built around the thesis that mechanical waves, sound, E&M, and quantum wavefunctions are one unified subject — sets up both `04-optics.md` and `06-modern-physics-relativity-and-quantum.md` |
| Herbert Goldstein, Charles P. Poole Jr. & John L. Safko, *Classical Mechanics*, 3rd ed., Addison Wesley, 2002, ch. 6 | The fully general `N`-coupled-oscillator normal-mode machinery |

## Tier 3 — Research-literature depth

| Exact source | Why it's here |
|---|---|
| John William Strutt (Lord Rayleigh), *The Theory of Sound*, Macmillan, Vol. 1: 1877, Vol. 2: 1878 (public domain, widely available via Internet Archive) | The original comprehensive treatment of acoustic wave phenomena, resonance, and normal modes |
| L.D. Landau & E.M. Lifshitz, *Mechanics* (Course of Theoretical Physics, Vol. 1), 3rd ed., Butterworth-Heinemann, 1976, the small-oscillations chapters | Terse, general derivation of the normal-mode problem from the Lagrangian, including the general theory of parametric resonance (relevant to "pumping a swing" style problems) |

## Problem sources specific to this topic

- A.P. French's own problems, worked chapter by chapter.
- I.E. Irodov, *Problems in General Physics*, Mir Publishers, 1981 — oscillations chapter.
- Jaan Kalda's *Mechanics* and *Electromagnetism* handouts (no dedicated waves handout exists — pull oscillation problems from these two).
- P. Gnädig, G. Honyek & K.F. Vigh, *200 Puzzling Physics Problems*, Cambridge University Press, 2001, and its 2016 sequel — oscillation/wave sections.
- ipho-unofficial.org archive, filtered to oscillations/waves.

## Self-check milestone

Given an arbitrary system of `N` masses connected by springs (any topology), write down the mass matrix and stiffness matrix directly from inspection within a few minutes, and state how many normal modes it has and which symmetry, if any, lets you guess one mode shape without computation.
