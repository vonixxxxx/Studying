# 7. Experimental Physics (IPhO Syllabus: Part B, the Experimental Competition)

IPhO's score is split roughly 50/50 between the theoretical papers and a single 5-hour experimental exam, and this is consistently the most under-prepared half of self-study olympiad prep. Treat this file as co-equal to the six theory topics.

## Subtopics, in dependency order

| Subtopic | Math prerequisite — exact source, read this first | If still stuck → deeper math | Physics text (Tier 1) | Practical exercise |
|---|---|---|---|---|
| Significant figures, basic uncertainty, reporting a measurement | Basic algebra | — | John R. Taylor, *An Introduction to Error Analysis: The Study of Uncertainties in Physical Measurements*, 2nd ed., University Science Books, 1997, ch. 1-2 | Measure a fixed physical quantity 20 times and report the result with correct significant figures and uncertainty |
| Propagation of uncertainty through a formula | Mary L. Boas, *Mathematical Methods in the Physical Sciences*, 3rd ed., Wiley, 2005, ch. 4 ("Partial Differentiation") — the error-propagation formula is a first-order multivariable Taylor expansion of the result around the measured values | Same chapter's more advanced sections if the multivariable-Taylor-expansion origin isn't clear | Taylor, *Error Analysis*, ch. 3 | Propagate uncertainty by hand through a formula with several measured inputs and verify it against the spread of repeated trials |
| The normal distribution, standard deviation, standard error of the mean | Boas, ch. 15 ("Probability and Statistics") | — | Taylor, *Error Analysis*, ch. 4-5 | — |
| Least-squares fitting a line to data, uncertainty in a fitted slope/intercept | James Stewart, *Calculus: Early Transcendentals*, 8th ed., Cengage Learning, 2015, ch. 14 ("Partial Derivatives") — minimizing a sum of squares is a stationary-point condition | — | Taylor, *Error Analysis*, ch. 8 | Take real data (e.g., pendulum period at several lengths) and extract a physical constant from a linearized plot's slope, with correctly propagated uncertainty |
| Systematic vs. random error, experimental design | — | — | Taylor, *Error Analysis*, ch. 1 and 9 | Design an experiment to measure a given quantity with minimal systematic error, using commonly available equipment |
| Common apparatus and techniques (oscilloscopes, multimeters, calipers/micrometers, optical benches) | — | — | No single canonical text — learn by using real equipment; university intro-lab manuals are a fine substitute if you lack lab access | Hands-on time with every instrument category before exam-condition mock experimentals |

## Tier 2 — Graduate depth

| Exact source | What it adds beyond Tier 1 |
|---|---|
| Philip R. Bevington & D. Keith Robinson, *Data Reduction and Error Analysis for the Physical Sciences*, 3rd ed., McGraw-Hill, 2003 | Nonlinear least-squares fitting, the chi-squared goodness-of-fit test, and maximum-likelihood estimation — the statistical machinery underneath the qualitative judgment calls Tier 1 leaves informal |

## Tier 3 — Depth beyond the standard curriculum

| Exact source | Why it's here |
|---|---|
| E.T. Jaynes, *Probability Theory: The Logic of Science*, Cambridge University Press, 2003 | The deepest available treatment of what a "confidence interval" or "best estimate" actually means epistemically |

## How to actually train this without a physics lab

- A phone stopwatch, a ruler, and a protractor are enough for a genuine pendulum-period experiment with real uncertainty analysis.
- A cheap multimeter and a breadboard are enough for the RC-circuit experiment referenced in `02-electromagnetism.md`.
- A laser pointer, a diffraction grating, and a tape measure are enough for the diffraction experiment referenced in `04-optics.md`.
- Past official IPhO experimental problems (in the ipho-unofficial.org archive alongside the theory papers) come with the full apparatus list used at the actual competition — reproduce as many as your equipment allows.

## Self-check milestone

Given a past official IPhO experimental problem, complete the full cycle — real measurements, correctly propagated uncertainty, a correctly-linearized plot with error bars, a final answer with stated uncertainty — within the official 5-hour time budget, and compare against the official solution.
