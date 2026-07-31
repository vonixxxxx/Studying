# 4. Electromagnetic Waves and Optics (IPhO Syllabus: Electromagnetic Waves and Optics)

Optics splits cleanly into two regimes that need different math and different intuition: geometric optics (rays, no wave effects — mostly algebra and trigonometry) and physical/wave optics (interference, diffraction, polarization — everything from `03-oscillations-and-waves.md`'s wave toolkit, now applied to light specifically). Don't skip straight to physical optics because it looks more "advanced" — a large fraction of IPhO optics points come from fast, clean geometric-optics ray tracing under time pressure.

## Subtopics, in dependency order

| Subtopic | Math prerequisite (Tier 1) | If still stuck → deeper math | Physics text (Tier 1) | Tier-1 problem set |
|---|---|---|---|---|
| Reflection, refraction, Snell's law | Trigonometry | — | Eugene Hecht, *Optics*, geometric-optics chapters | Hecht's geometric-optics problems |
| Thin lenses and mirrors, ray tracing, the thin-lens equation | Algebra, similar triangles | — | Hecht, same chapters | Hecht's problems; build real speed here since these are the fastest points on any IPhO optics section |
| Dispersion | — | — | Hecht | Hecht |
| Interference (double-slit, thin films) | Superposition of waves with a phase difference — `00-mathematical-toolkit.md`/`03-oscillations-and-waves.md` complex-exponential method | — | Hecht's interference chapter | Hecht's problems |
| Diffraction (single slit, gratings) | Fourier transforms — `00-mathematical-toolkit.md` | Howard Georgi, *The Physics of Waves*, the diffraction chapter, for the full derivation of a diffraction pattern as the Fourier transform of the aperture's transmission function — this reframing makes grating/multi-slit problems a matter of reading off a known Fourier-transform pair rather than re-deriving from scratch each time | Hecht's diffraction chapter | Hecht's problems |
| Polarization | Vector nature of the E-field, Malus's law | — | Hecht's polarization chapter | Hecht's problems |
| Optical instruments (microscopes, telescopes, resolution limits) | Combines geometric optics and the diffraction limit above | — | Hecht | Hecht's problems |

## Tier 2 — Graduate depth

| Source | What it adds beyond Tier 1 |
|---|---|
| Max Born & Emil Wolf, *Principles of Optics* (Cambridge University Press) | The standard graduate optics reference — full electromagnetic (not ray-approximation) treatment of diffraction theory, coherence, and interferometry; reading the diffraction-theory chapters after Hecht is the single biggest optics depth upgrade available, and it directly explains *why* the ray-optics approximation in the earlier subtopics works at all (it's the short-wavelength limit of the full wave theory) |

## Tier 3 — Research-literature depth

| Source | Why it's here |
|---|---|
| Augustin-Jean Fresnel's original memoirs on diffraction (1818, submitted to the French Academy of Sciences) — historically notable as the paper whose diffraction predictions were confirmed by the famous "Poisson/Arago spot" experiment, turning a proposed *refutation* of the wave theory of light into its strongest confirmation | Seeing how a genuinely correct, non-obvious prediction (a bright spot at the center of a circular object's shadow) was derived and then tested is a better education in how physical theories actually get validated than any modern textbook re-telling |
| James Clerk Maxwell's electromagnetic-wave sections in *A Treatise on Electricity and Magnetism* (already cited in `02-electromagnetism.md`) | The historical unification of optics with electromagnetism — light *as* an electromagnetic wave was Maxwell's result, and this topic file is where that unification actually gets used |

## Problem sources specific to this topic

- Hecht's own problems, worked chapter by chapter.
- Irodov's optics chapter.
- Kalda's *Optics* handout (part of his standard set) for olympiad-specific difficulty and technique.
- *200 (More) Puzzling Physics Problems*'s optics sections.
- ipho-unofficial.org archive, filtered to optics.

## Self-check milestone

Given an unfamiliar multi-element optical system (e.g., two lenses and a mirror in some arrangement), ray-trace it correctly using the thin-lens/mirror equations in under 10 minutes, and separately, given a diffraction setup, correctly identify from the geometry alone (slit width vs. wavelength vs. distance to screen) whether you're in the Fraunhofer or Fresnel diffraction regime before choosing which formula to apply.
