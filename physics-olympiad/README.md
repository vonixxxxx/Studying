# IPhO Curriculum: Topic-Based, Math-Backward-Chained, Depth-Unlimited

*Supersedes `../physics-olympiad-curriculum.md` (kept in git history — see that file's final commit for the original month-by-month version). This version is organized by **IPhO syllabus topic**, not calendar month, and every physics subtopic below is preceded by the exact math you need to read first. Work backward: hit a physics idea you don't fully own → find its row in the topic file → go read that math chapter → come straight back and re-derive the physics with it in hand.*

## Why this is organized differently now

A calendar plan is the wrong shape for solo self-study, because you never study strictly in order — you hit a wall on Tuesday of "month 6" that's actually caused by a math gap from "month 2," and a month-numbered document doesn't help you find it fast. This version drops the calendar and organizes around the **IPhO official syllabus structure** instead, so you can enter at any topic, and it puts a **math-prerequisite table at the top of every topic**, so "I don't get this physics" always resolves to a specific, named math chapter to go read *right now*, not a vague "go learn more calculus."

## The three depth tiers, used consistently in every file

You asked for no ceiling, so every topic is built in three tiers instead of one:

- **Tier 1 — IPhO-sufficient.** The actual content tested at IPhO, from a solid, well-chosen undergraduate source. This tier alone, done properly with its problem sets, gets you to competitive medal-range content knowledge.
- **Tier 2 — Graduate depth.** The standard graduate-level textbook treatment of the same topic. This is a large step past what any IPhO problem requires, and that's the point: understanding *why* the Tier-1 result is true at the level a physics PhD student is expected to, not just how to apply it, makes unfamiliar Tier-1 problems look like special cases you already understand rather than puzzles you have to pattern-match.
- **Tier 3 — Research-literature depth.** Primary sources (the original papers where the physics was first worked out) and the most advanced standard monographs in the field. This is "better conceptual grounding than a gold medalist" territory — most working physicists never read Tier 3 in most of these topics, and it's here because you asked for it, not because IPhO requires it.

## Read this honestly before you build your schedule around it

Depth and speed are two different things, and this document only gives you one of them directly. Everything above builds **understanding** — the kind that lets you generalize to a problem you've never seen, because you actually know why the tool works rather than recognizing it from a past paper. That's a real and durable edge, and pushing to Tier 2/3 is a legitimate way to build it precisely because it removes the need to have seen a trick before — if you understand the Lagrangian at Landau's level of generality, you don't need to have memorized "the Kalda effective-potential trick," you can just derive it under time pressure.

But it does **not**, by itself, close what the field calls the instinct gap: the specific trained reflex of recognizing, in the first 90 seconds of reading an unfamiliar problem, which of a few hundred structural patterns it is, and retrieving the right method fast enough to finish a 5-hour paper. That reflex is built by one thing only — **volume of timed, unfamiliar problem-solving**, the same way sight-reading speed in music or board vision in chess is built by repetition under time pressure, not by reading more theory. A student who has read Jackson's *Classical Electrodynamics* cover to cover but has solved 30 timed problems will lose to a student who has read only Purcell but has solved 300, on exam day, most of the time. So: treat this document as your **Track A** (theory, math, depth) and pair it, every week, without exception, with the **Track B** (timed problem sets) and **Track C** (experimental physics) and the mock-exam calendar in [`resources.md`](./resources.md) — those are unchanged from the original plan and are just as load-bearing as the depth this document adds.

## How to actually use this, step by step

1. Pick the topic file below that matches what you're studying (or what a problem you're stuck on requires).
2. Before opening the physics chapter, find the relevant row in that file's **math-prerequisite table**.
3. Go read that math chapter/section *in the math book*, right now, and work a handful of its own exercises — not physics problems yet, just the math on its own terms.
4. Immediately return to the physics chapter and **re-derive the result yourself on paper**, using the math tool you just built, before reading the book's derivation.
5. If it still doesn't click, follow that row's "if still stuck, go deeper" pointer into the Tier 2/3 source, or reread the physics text's own derivation, then repeat step 4.
6. Once the derivation is solid cold (no notes, next day), do that subtopic's Tier-1 problem set before you let yourself go further into Tier 2/3 — depth without the base problem set solved is the most common self-study failure mode, because it feels like progress and isn't measured against anything.
7. Tier 2/3 material is there whenever you want it — no gate, no requirement to "finish" Tier 1 first if a Tier 2 explanation is what actually makes the Tier 1 result click. Follow curiosity; just don't let it replace the Tier-1 problem sets.

## Topic files (the IPhO syllabus, restructured for self-study)

| # | File | IPhO syllabus section |
|---|---|---|
| 0 | [`00-mathematical-toolkit.md`](./00-mathematical-toolkit.md) | General problems: mathematical tools, dimensional analysis, order-of-magnitude estimation |
| 1 | [`01-mechanics.md`](./01-mechanics.md) | Mechanics |
| 2 | [`02-electromagnetism.md`](./02-electromagnetism.md) | Electric charges and fields, electric current, magnetic field |
| 3 | [`03-oscillations-and-waves.md`](./03-oscillations-and-waves.md) | Oscillations and waves |
| 4 | [`04-optics.md`](./04-optics.md) | Electromagnetic waves and optics |
| 5 | [`05-thermodynamics-and-statistical-physics.md`](./05-thermodynamics-and-statistical-physics.md) | Thermodynamics and statistical physics |
| 6 | [`06-modern-physics-relativity-and-quantum.md`](./06-modern-physics-relativity-and-quantum.md) | Quantum physics and relativity |
| 7 | [`07-experimental-physics.md`](./07-experimental-physics.md) | Experimental competition (Part B) |
| — | [`resources.md`](./resources.md) | Full resource stack, checkpoint/mock-exam calendar, and the complete bibliography |

## Quick master lookup — "I don't understand X, what math do I need"

A fast-access index across every topic file. **Every row below is already inlined, with the exact book and chapter, directly inside the physics topic file itself** — you don't need to visit `00-mathematical-toolkit.md` to get the pointer; it's repeated right where you need it. That file exists only as the single-page complete reference if you want to read the whole toolkit once, end to end, before starting.

| If you're stuck on... | Math tool | Exact source (also inlined in the topic file itself) | Applied in |
|---|---|---|---|
| Taylor/small-angle approximations, why `sin θ ≈ θ` | Series & power series | James Stewart, *Calculus: Early Transcendentals*, 8th ed., ch. 11; Mary L. Boas, *Mathematical Methods in the Physical Sciences*, 3rd ed., ch. 1 | `01-mechanics.md`, `06-modern-physics-relativity-and-quantum.md` |
| Dot/cross products, projecting forces | Vector algebra | Stewart, ch. 12; H.M. Schey, *Div, Grad, Curl, and All That*, 4th ed., opening chapter | `01-mechanics.md`, `02-electromagnetism.md` |
| Gradient, divergence, curl, flux integrals | Vector calculus | Schey, cover to cover; Boas, ch. 6 | `02-electromagnetism.md` |
| Eigenvalues/eigenvectors (normal modes, inertia tensor) | Linear algebra | Gilbert Strang, *Introduction to Linear Algebra*, 5th ed., ch. "Eigenvalues and Eigenvectors" | `01-mechanics.md`, `03-oscillations-and-waves.md` |
| Solving `x'' + ω²x = 0` and driven/damped versions | Linear ODEs, constant coefficients | Morris Tenenbaum & Harry Pollard, *Ordinary Differential Equations* (Dover) | `01-mechanics.md`, `03-oscillations-and-waves.md` |
| Complex exponentials for AC circuits/waves | Complex numbers | Boas, ch. 2 | `02-electromagnetism.md`, `03-oscillations-and-waves.md`, `04-optics.md` |
| Fourier series for non-sinusoidal periodic driving/diffraction | Fourier analysis | Boas, ch. 7 | `03-oscillations-and-waves.md`, `04-optics.md`, `06-modern-physics-relativity-and-quantum.md` |
| Rotating/non-inertial reference frames, fictitious forces | Vector calculus + rotation | Schey; John R. Taylor, *Classical Mechanics*, ch. 9 | `01-mechanics.md` |
| The action integral / why Lagrangian mechanics works at all | Calculus of variations | Boas, ch. 9; Cornelius Lanczos, *The Variational Principles of Mechanics*, 4th ed. | `01-mechanics.md` |
| Partition functions, statistical averages | Multivariable calculus + probability | Stewart, ch. 14-15; Boas, ch. 15 | `05-thermodynamics-and-statistical-physics.md` |
| Wave equation as a PDE | Partial differential equations | Boas, ch. 13 | `03-oscillations-and-waves.md`, `04-optics.md` |
| Propagating uncertainty through a formula | Partial derivatives (error propagation) | Boas, ch. 4 | `07-experimental-physics.md` |

---

*Keep the daily/weekly rhythm, error-log habit, and the honest calibration about IPhO's national-selection gate from the original document's opening section — none of that changed, only the organizing axis did.*
