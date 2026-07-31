# 4. Electromagnetic Waves and Optics (IPhO Syllabus: Electromagnetic Waves and Optics)

Optics splits into two regimes that need different math: geometric optics (rays, mostly algebra/trigonometry) and physical/wave optics (interference, diffraction, polarization — everything from `03-oscillations-and-waves.md`'s toolkit, now applied to light). Don't skip straight to physical optics because it looks more advanced — a large fraction of IPhO optics points come from fast, clean geometric-optics ray tracing under time pressure.

## Subtopics, in dependency order

| Subtopic | Math prerequisite — exact source, read this first | If still stuck → deeper math | Physics text (Tier 1) | Tier-1 problem set |
|---|---|---|---|---|
| Reflection, refraction, Snell's law | Jay Abramson et al., *Precalculus*, OpenStax, 2015 (free), trigonometry chapters | — | Eugene Hecht, *Optics*, 5th ed., Pearson, 2016, geometric-optics chapters | Hecht's geometric-optics problems |
| Thin lenses and mirrors, ray tracing, the thin-lens equation | OpenStax *Precalculus*, algebra/similar-triangles review | — | Hecht, same chapters | Hecht's problems — build real speed here |
| Dispersion | — | — | Hecht | Hecht |
| Interference (double-slit, thin films) | Mary L. Boas, *Mathematical Methods in the Physical Sciences*, 3rd ed., Wiley, 2005, ch. 2 ("Complex Numbers") — superposition of waves with a phase difference via complex exponentials | — | Hecht's interference chapter | Hecht's problems |
| Diffraction (single slit, gratings) | Boas, ch. 7 ("Fourier Series and Transforms") | Howard Georgi, *The Physics of Waves*, Prentice Hall, 1993 (free), the diffraction chapter — a diffraction pattern as the Fourier transform of the aperture's transmission function | Hecht's diffraction chapter | Hecht's problems |
| Polarization | James Stewart, *Calculus: Early Transcendentals*, 8th ed., Cengage Learning, 2015, ch. 12 (vector nature of the E-field) | — | Hecht's polarization chapter | Hecht's problems |
| Optical instruments (microscopes, telescopes, resolution limits) | Combines the geometric-optics and diffraction rows above | — | Hecht | Hecht's problems |

## Tier 2 — Graduate depth

| Exact source | What it adds beyond Tier 1 |
|---|---|
| Max Born & Emil Wolf, *Principles of Optics: Electromagnetic Theory of Propagation, Interference and Diffraction of Light*, 7th expanded ed., Cambridge University Press, 1999 | The standard graduate optics reference — full electromagnetic (not ray-approximation) treatment of diffraction theory, coherence, and interferometry; explains *why* the ray-optics approximation works at all (it's the short-wavelength limit of the full wave theory) |

## Tier 3 — Research-literature depth

| Exact source | Why it's here |
|---|---|
| Augustin-Jean Fresnel, *Mémoire sur la diffraction de la lumière*, submitted to the French Academy of Sciences, 1818 (the Grand Prix memoir whose diffraction predictions were confirmed by the "Poisson/Arago spot" experiment) | Seeing a non-obvious, correct prediction (a bright spot at the center of a circular object's shadow) derived and then tested is a better education in how physical theories get validated than any modern retelling |
| James Clerk Maxwell, *A Treatise on Electricity and Magnetism*, Clarendon Press, Oxford, 1873 (already cited in `02-electromagnetism.md`) | The historical unification of optics with electromagnetism — light as an electromagnetic wave |

## Problem sources specific to this topic

- Eugene Hecht's own problems, worked chapter by chapter.
- I.E. Irodov, *Problems in General Physics*, Mir Publishers, 1981 — optics chapter.
- Jaan Kalda's *Optics* handout (free; part of his standard olympiad handout set).
- P. Gnädig, G. Honyek & K.F. Vigh, *200 Puzzling Physics Problems*, Cambridge University Press, 2001, and its 2016 sequel — optics sections.
- ipho-unofficial.org archive, filtered to optics.

## Self-check milestone

Given an unfamiliar multi-element optical system, ray-trace it correctly using the thin-lens/mirror equations in under 10 minutes, and given a diffraction setup, correctly identify from the geometry (slit width vs. wavelength vs. screen distance) whether you're in the Fraunhofer or Fresnel regime before choosing a formula.
