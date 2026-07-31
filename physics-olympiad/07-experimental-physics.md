# 7. Experimental Physics (IPhO Syllabus: Part B, the Experimental Competition)

IPhO's score is split roughly 50/50 between the theoretical papers and a single 5-hour experimental exam, and this is consistently the most under-prepared half of self-study olympiad prep — it's easy to spend a year reading textbooks and never once propagate an uncertainty through a real, noisy measurement. Treat this file as co-equal to the six theory topics, not an afterthought at the end.

## Subtopics, in dependency order

| Subtopic | Math prerequisite (Tier 1) | If still stuck → deeper math | Physics text (Tier 1) | Practical exercise |
|---|---|---|---|---|
| Significant figures, basic uncertainty, reporting a measurement | Basic algebra | — | John R. Taylor, *An Introduction to Error Analysis* (2nd ed.), ch. 1-2 | Measure a fixed physical quantity (a table's length, a marble's diameter) 20 times and report the result with correct sig figs and uncertainty |
| Propagation of uncertainty through a formula | Partial derivatives — `00-mathematical-toolkit.md`; the general error-propagation formula is literally a first-order multivariable Taylor expansion of the result around the measured values | Boas ch. 4's partial-derivatives chapter, if the multivariable-Taylor-expansion origin of the propagation formula isn't clear | Taylor, *Error Analysis*, ch. 3 | Given a formula with several measured inputs (e.g., density from mass and measured dimensions), propagate the uncertainty by hand and verify it against the direct spread of repeated trials |
| The normal distribution, standard deviation, standard error of the mean | Probability and statistics — `00-mathematical-toolkit.md` | — | Taylor, *Error Analysis*, ch. 4-5 | — |
| Least-squares fitting a line to data, uncertainty in a fitted slope/intercept | Calculus (minimizing a sum of squares — this is a direct, concrete application of multivariable calculus's stationary-point condition) | — | Taylor, *Error Analysis*, ch. 8 | Take real data (e.g., a pendulum's period at several lengths) and extract a physical constant from the slope of a linearized plot, with a correctly propagated uncertainty on that constant |
| Systematic vs. random error, experimental design | — | — | Taylor, *Error Analysis*, ch. 1 and 9 | Design (don't just execute) an experiment to measure a given quantity with minimal systematic error, using only commonly available equipment |
| Common apparatus and techniques (oscilloscopes, multimeters, calipers/micrometers, optical benches) | — | — | No single canonical text — learn by using real equipment; university intro-lab manuals (freely available from most physics departments) are a fine substitute if you don't have lab access | Hands-on time with every instrument category above before exam-condition mock experimentals |

## Tier 2 — Graduate depth

| Source | What it adds beyond Tier 1 |
|---|---|
| Philip Bevington & D. Keith Robinson, *Data Reduction and Error Analysis for the Physical Sciences* | A more advanced, more computational treatment than Taylor's introductory book — covers nonlinear least-squares fitting, the chi-squared goodness-of-fit test, and maximum-likelihood estimation properly, which is the actual statistical machinery underneath the "does my fit look reasonable" judgment calls Tier 1 leaves qualitative |

## Tier 3 — Depth beyond the standard curriculum

| Source | Why it's here |
|---|---|
| E.T. Jaynes, *Probability Theory: The Logic of Science* (Cambridge University Press) | Already cited in `00-mathematical-toolkit.md` — the deepest available treatment of what a "confidence interval" or "best estimate" actually *means* epistemically, which is worth having once the mechanical procedures above are automatic |

## How to actually train this without a physics lab

You do not need a university lab to build real experimental competence — IPhO experimental problems are explicitly designed to be solvable with modest apparatus, and most of the skill is in the analysis, not exotic equipment:

- A phone stopwatch, a ruler, and a protractor are enough for a genuine pendulum-period experiment with real uncertainty analysis.
- A cheap multimeter and a breadboard are enough for the RC-circuit experiment referenced in `02-electromagnetism.md`.
- A laser pointer, a diffraction grating (cheap and widely available), and a tape measure are enough for the diffraction experiment referenced in `04-optics.md`.
- Past official IPhO experimental problems (available in the ipho-unofficial.org archive alongside the theory papers, see `resources.md`) come with the full apparatus list used at the actual competition — reproduce as many as your available equipment allows, and for the ones you can't physically reproduce, at minimum work through the data-analysis portion using the official sample data if published with the solutions.

## Self-check milestone

Given a past official IPhO experimental problem (or a self-designed equivalent), complete the full cycle — take real measurements, propagate uncertainty correctly through to a final answer, produce a correctly-linearized plot with error bars, and extract a physical constant with a stated uncertainty — within the official 5-hour time budget, and compare your final uncertainty and value against the official solution's.
