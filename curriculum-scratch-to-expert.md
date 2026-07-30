# From High School Algebra to the Epicentre: A Full Curriculum
*Companion to `ai-robotics-expertise-roadmap.md`. That document is the strategic "why" and "which niches." This document is the operational "how" — books, lectures, projects, labs, competitions, and people — aimed at producing both a frontier researcher and an inventor in the Feynman/Jobs/Bell-Labs mold: someone with bulletproof technical depth *and* the taste, curiosity, and cross-disciplinary habits that turn depth into original work.*

## Two paths through this document

This document now has two entry points, built for two different learning styles. Pick the one that matches how you actually learn — or run both, as intended here.

1. **The Fast Track** (immediately below) — a concept-first, top-down, 1-year path. It starts with AI/ML directly — you're training and dissecting real models in week one — and pulls in exactly the math, statistics, and physics each concept needs, right when you need it, not before. When something doesn't make sense, you work *backward* from the concept into the specific prerequisite, learn just that piece, and come straight back to the project. This is the path for someone who learns fastest by first seeing why a piece of math matters, then going and getting it.
2. **The Basics** (Stage 0 onward, further below) — the original bottom-up, multi-year sequence: algebra → calculus → physics → rigorous math → AI → infra → robotics → research, each stage building carefully on the last. This is not obsolete — it's the reference library the Fast Track sends you into whenever it says "go get X." Read it *simultaneously* with the Fast Track, not after it: the Fast Track tells you exactly which section of the Basics to open at exactly the moment you need it, and you can always choose to read a Basics stage in full for the complete, unhurried, fully rigorous version of anything the Fast Track only gave you "just enough" of.

Three things still run **concurrently, from day one, forever**, regardless of which path you're on:

1. **Rigorous technical mastery** — Fast Track and/or Basics, per above.
2. **Intuition-building and reading habits** — Track 0, immediately below. This starts *today*.
3. **Creative/inventive practice** — the "Inventor's Library" and tinkering practice, which most technical curricula omit and is precisely what separates a competent expert from Feynman, Shannon, or Jobs.

Every stage and every Fast Track module ends with a **"prove it" milestone** — a concrete, checkable output. If you can't do the milestone, you're not done, regardless of how many books you've "read."

---

## The Fast Track — A 1-Year, Concept-First Path to the Epicentre

### The philosophy, stated plainly

Most curricula (including the Basics half of this document) are bottom-up: months of algebra and calculus before you ever touch a neural network. That's the right approach for building a foundation nobody can ever poke a hole in — and it's why the Basics still exist below. But it is not the fastest way for an unusually strong, fast learner to reach research-level fluency across the math–physics–AI–robotics intersection, for a simple reason: motivation and retention are both dramatically higher when you learn a piece of math *because you are currently blocked by not knowing it*, rather than because it's "next in the sequence" and might matter someday. This is the same insight behind fast.ai's "teach the whole game first" philosophy and behind *Mathematics for Machine Learning* (Deisenroth, Faisal, Ong — free PDF at mml-book.github.io) — arguably the single best spine resource for this entire Fast Track, since it was written explicitly to teach exactly the math a given ML method needs, in the order ML needs it, not in the order a math department would teach it.

**The operating rule for this whole path: when a project stalls because you don't understand a piece of math, physics, or CS underneath it, stop, go get exactly that piece — no more — from the resource listed for that module (or from the relevant Basics stage for the fully rigorous version), and come straight back to the project.** Do not pre-emptively "finish" a subject before starting the next module. The spiral will bring you back to every subject multiple times at increasing depth — that's by design, not a gap.

**Honest calibration, carried over from the earlier "is this physically possible" discussion:** this path is built to get a genuinely fast learner to elite technical fluency and a real portfolio of original work across the intersection in one year. It does **not** compress the parts of Stage 7 (below) that run on other people's calendars — journal review cycles, REU program dates, a mentor's response time, a real reputation built over repeated public contact with a field. Those still take additional real years no matter how fast you learn. What compresses is the knowledge and the portfolio; what doesn't is anything that requires other people's clocks.

### Month 1 — The whole game, then backprop from scratch
**Project:** Train a real image classifier end-to-end in PyTorch this week, without yet understanding every internal detail (fast.ai's Practical Deep Learning for Coders, lesson 1, is built exactly for this — you get a working, reasonably good model on day one). Then spend the rest of the month tearing it open: implement backpropagation yourself, from raw NumPy, no autograd, following Andrej Karpathy's "Zero to Hero" series (starting with micrograd) until your from-scratch version matches PyTorch's gradients exactly.
**Math you need right now:** vectors, matrices, and matrix multiplication as *operations*, not proofs (3Blue1Brown's *Essence of Linear Algebra*, episodes 1-3 only); derivatives and the chain rule as *rates of change composing* (3Blue1Brown's *Essence of Calculus*, episodes 1-4); the specific matrix calculus backprop needs (Terence Parr & Jeremy Howard, *"The Matrix Calculus You Need for Deep Learning,"* free at explained.ai — this single short paper is scoped exactly to this problem, don't go further than it yet).
**If you get stuck and need the full rigor:** go backward into Stage 1's linear algebra row (Strang/Axler) or Stage 1's calculus row (Apostol) below — read only the specific section that's blocking you, then return here.
**Prove it:** your from-scratch backprop matches PyTorch's autograd on a small network to several decimal places; you can explain, on a whiteboard with no notes, why the chain rule is the entire content of backpropagation.

### Month 2 — Probability, statistics, and classical ML
**Project:** Implement linear regression, logistic regression, and a naive Bayes classifier from scratch (no scikit-learn), and understand each one's loss function as a maximum-likelihood argument, not just a formula to minimize.
**Math you need right now:** the interactive, visual first pass on probability at **Seeing Theory** (Brown University); *An Introduction to Statistical Learning* (James, Witten, Hastie, Tibshirani — free PDF, ISLR) chapters 2-4, which is deliberately gentler and more ML-directed than a full mathematical-statistics text; Bayes' rule and maximum likelihood estimation specifically, from *Mathematics for Machine Learning* ch. 5-8.
**If you get stuck:** Stage 2's probability row (Ross) below for the fully worked computational treatment, or Stage 2's statistics row (Casella & Berger) for full mathematical rigor on estimators.
**Prove it:** derive, from the maximum-likelihood principle, why minimizing mean-squared error is equivalent to assuming Gaussian noise — in writing, from scratch.

### Month 3 — Deep learning depth: CNNs and why optimizers work
**Project:** Train a CNN on real images (CIFAR-10 or similar) using Stanford CS231n's assignments as your problem set; when you hit the question "why does Adam train faster/more reliably than plain SGD," stop and actually answer it instead of just importing `torch.optim.Adam`.
**Math you need right now:** convexity, gradient descent convergence *intuition* (not full proofs yet) from Boyd & Vandenberghe's *Convex Optimization* — read only the chapters on gradient descent and momentum; eigenvalues of the Hessian as the reason ravines/saddle points slow down training (revisit the 3Blue1Brown eigenvector picture from Month 1, now applied to a loss landscape).
**If you get stuck:** Stage 3's optimization rows (Boyd, then Nocedal & Wright) below for the full convergence proofs.
**Prove it:** implement SGD, momentum, and Adam from scratch (no `torch.optim`), and produce a plot showing why each converges differently on a deliberately ill-conditioned toy loss surface.

### Month 4 — Sequence models and transformers
**Project:** Follow Karpathy's nanoGPT build, end to end, until you have a working, from-scratch GPT trained on a small corpus.
**Math you need right now:** attention as matrix multiplication (3Blue1Brown's neural network series covers this visually); cross-entropy and perplexity as information-theoretic quantities (Cover & Thomas, *Elements of Information Theory*, chapter 2 *only* — entropy and KL divergence, not the whole book yet).
**If you get stuck:** Stage 4's transformer row (the original paper + Jay Alammar's illustrated posts) below for a second pass at the architecture; Stage 3's information theory row (full Cover & Thomas) if you want the complete theory now instead of later.
**Prove it:** your from-scratch GPT trains and its loss curve matches nanoGPT's reference numbers; you can derive perplexity from cross-entropy from first principles, unaided.

### Month 5 — Reinforcement learning and control
**Project:** Implement DQN and then PPO from scratch (not Stable-Baselines3) and solve CartPole, then a harder control task.
**Math/physics you need right now:** Markov decision processes and the Bellman equation (Csaba Szepesvári's free, short monograph *Algorithms for Reinforcement Learning* is a deliberately condensed alternative to reading all of Sutton & Barto up front); just enough Newtonian mechanics to actually understand CartPole's own equations of motion (Morin's *Introduction to Classical Mechanics*, the chapter on rotational motion only).
**If you get stuck:** Stage 4's full RL row (Sutton & Barto, David Silver's course, CS285) below for complete depth; Stage 2's mechanics rows for the full physics treatment.
**Prove it:** your from-scratch PPO solves CartPole and one harder continuous-control environment; you can derive the Bellman equation from the definition of the value function, unaided.

### Month 6 — Real robots: kinematics, dynamics, control
**Project:** Move your RL agent into a simulated robot arm in MuJoCo; implement forward and inverse kinematics and a PID or MPC controller by hand.
**Math/physics you need right now, and this is where it becomes unavoidable:** rigid-body configuration as SE(3) and Lie groups — read *only* the forward-kinematics chapters of Murray, Li & Sastry's *A Mathematical Introduction to Robotic Manipulation* (free PDF) or the equivalent early chapters of Lynch & Park's *Modern Robotics*; Lagrangian mechanics *specifically as applied to a robot arm* (Goldstein's early chapters, or better, Lynch & Park's own dynamics chapter, which derives it in robotics notation directly).
**If you get stuck:** Stage 3's differential-geometry/Lie-group row below for the full mathematical treatment of manifolds and Lie groups in general, not just the robotics-specific slice.
**Prove it:** derive the forward and inverse kinematics of a simple arm from the Lie-group/twist formalism and implement a working MPC controller for it in simulation — this is the same milestone as Stage 6's "prove it" below, reached in month 6 instead of year 6.

### Month 7 — World models and physics-informed learning
**Project:** Build a small physics-informed neural network (PINN) for a simple dynamical system (a pendulum or double pendulum) and compare it against a plain learned model with no physics prior.
**Math/physics you need right now:** ODEs revisited at the level of actually solving the specific system you're modeling (3Blue1Brown's *Differential Equations* series, then the relevant Morin/Goldstein chapter for the exact system); enough statistical mechanics to understand *why* diffusion models work as denoising a stochastic process (Schroeder's *Thermal Physics*, the entropy and Langevin-adjacent chapters only).
**If you get stuck:** Stage 2's full ODE and stat-mech treatment below; the original PINN literature (Raissi, Perdikaris, Karniadakis) for the rigorous formulation.
**Prove it:** your PINN outperforms the plain model on out-of-distribution initial conditions, and you can explain in writing exactly why the physics prior generalizes better.

### Month 8 — AI infrastructure: making it fast
**Project:** Profile your slowest training loop from the previous seven months, find the actual bottleneck (not a guessed one), and write a custom CUDA kernel that measurably beats the naive PyTorch op.
**CS/math you need right now:** just enough computer architecture to reason about memory hierarchy and bandwidth vs. compute-bound operations (Patterson & Hennessy's entry chapters only); *Programming Massively Parallel Processors* (Kirk & Hwu) chapters on the specific kernel pattern you need (reduction, matrix multiply, etc.) — not the whole book.
**If you get stuck:** Stage 5's full systems stack below (OS, compilers, DNN accelerator design) for complete depth.
**Prove it:** a profiler shows your custom kernel is measurably faster than the PyTorch op it replaces, and you can explain exactly which memory-hierarchy effect you exploited to get the speedup.

### Month 9 — The rigor sprint: go back and actually prove things
**Project:** By now you have real, motivated questions ("does gradient descent actually always converge on this kind of loss surface? why does the Kalman filter's update rule actually follow from Bayes' rule? why do complex eigenvalues show up in stability analysis?") that a rigorous math pass will directly answer, instead of feeling like abstract homework. Spend this month doing a dedicated, condensed real-analysis and measure-theoretic-probability sprint.
**Resources:** Abbott's *Understanding Analysis* end to end (it's short); the specific Rudin chapters that address a question you actually hit in Months 1-8; Durrett's measure-theoretic probability, chapters 1-2 only, for the rigorous foundation under everything you've been doing computationally with probability since Month 2.
**Prove it:** write a complete epsilon-delta proof of a nontrivial analysis theorem cold, without notes, and explicitly connect it back to one specific thing you built in Months 1-8 that you previously only trusted empirically.

### Month 10 — Mechanistic interpretability
**Project:** Reproduce one small, real interpretability finding on an open-weight model using Neel Nanda's **TransformerLens**.
**Math you need right now, revisited at depth:** singular value decomposition and eigenvectors of weight matrices as *feature directions* — this is the same linear algebra from Month 1, now at a much deeper level, which is exactly the point of the spiral.
**If you get stuck:** Stage 4's full interpretability row (Olah's Circuits work, the Anthropic transformer-circuits paper) below.
**Prove it:** find and document a specific circuit in a small open model, the same milestone as Stage 4's "prove it" below.

### Months 11-12 — Capstone synthesis, write-up, and one real contribution
**Project:** Pick one Layer-2 vertical from `ai-robotics-expertise-roadmap.md` (robotics, materials, quantum, etc.) and build one original small project combining at least three of the previous ten months' skills — e.g., a physics-informed world model (Month 7) controlling a simulated robot (Month 6) via a policy interpreted for safety (Month 10), running efficiently thanks to the kernel work (Month 8). Write the whole thing up publicly. Land one real, reviewed, non-trivial open-source PR (see Track 0.5's open-source list) before the year ends.
**Prove it:** a single public artifact — code plus a write-up — that combines multiple pillars and that a stranger in the field could look at and conclude you're serious. This is Stage 7's "prove it" below, reached in month 12 instead of year 5-10 — with the explicit caveat, restated once more, that the *reputation* that normally accretes around that artifact over years of conferences and relationships still takes real time to build; the artifact itself does not.

---

## Track 0 — The Inventor's Operating System (Day 1, and every day after)

This is the single biggest addition a "genius-level" plan needs over a merely rigorous one: habits of mind, not more content. Start every item below **today**, before you've finished a single textbook.

### The daily loop
- **Read something every single day** — alternate technical reading (whatever stage you're in) with something from the Inventor's Library below. Neither should ever fully stop, for ten years.
- **Feynman it.** For every genuinely new idea, immediately write a short explanation of it in plain language, as if teaching a smart 12-year-old, with no jargon and no notes open. If you can't, you don't understand it yet — go back. This single habit, done consistently, is worth more than any book on this list.
- **Sketch it.** Before or alongside the rigorous derivation of anything, find or draw the visual/geometric picture (this is exactly what 3Blue1Brown does for math, and what Feynman diagrams do for physics). Abstract symbol manipulation without a mental picture is fragile; a picture makes it permanent.
- **Build a toy of it, same day.** The moment you learn a new concept — a theorem, a physical law, an algorithm — write ten lines of code or a small physical experiment that makes it concrete within 24 hours. Don't let understanding stay purely verbal.
- **Keep a commonplace book / idea journal from Day 1.** Not lecture notes — a running, permanent log of questions you can't yet answer, half-formed connections between fields ("this optimization landscape looks like the energy landscape in stat mech — why?"), and things that surprised you. Da Vinci's notebooks and Feynman's own notebooks are the model. Re-read it monthly; your best original ideas will come from re-combining entries months or years apart, not from any single day's insight.
- **Spaced repetition for the permanent stuff.** Put every theorem statement, key derivation, and formula you want to *never re-derive from scratch* into Anki. This frees working memory for the actual creative combination of ideas, which is where invention happens — you cannot be original while still looking up the chain rule.
- **Write publicly, weekly, from week one.** A blog, a GitHub repo with real explanatory READMEs, a public notebook — doesn't matter which. Summarize what you learned and state one original thought or connection you had, every week. This is uncomfortable at first specifically because it's valuable: it forces the Feynman step, creates a public trail of your thinking (which matters enormously later for labs/opportunities), and trains you to have an opinion, not just absorb material.
- **Unstructured tinkering time, every week, with no goal.** Steve Jobs pointed directly at an unrelated calligraphy class as the source of the Mac's typography. Block real time weekly for curiosity with no deliverable: take something apart, learn an unrelated skill (electronics, woodworking, music, drawing), read outside the stack entirely (history of science, philosophy of mind, art). Cross-pollination is not a luxury in this plan — it is the mechanism by which genuinely new combinations of ideas happen.

### The Inventor's Library (read gradually, in parallel with the technical stages — never gated behind them)
This list is about developing *taste* and *research judgment*, not technical skill. Read these interleaved with the technical books, one every month or two, for the whole ten years.

| Book | Author | Why it belongs here |
|---|---|---|
| *Surely You're Joking, Mr. Feynman!* | Richard Feynman | The clearest existing portrait of curiosity as a discipline, not a personality trait — read this first, in Stage 0. |
| *The Idea Factory: Bell Labs and the Great Age of American Innovation* | Jon Gertner | The best account that exists of what an actual frontier-research culture looks like day to day — information theory, the transistor, and satellite comms all came out of one building's culture. |
| *Creative Selection: Inside Apple's Design Process During the Golden Age of Steve Jobs* | Ken Kocienda | A firsthand, granular account of the actual mechanics of Apple's design process — inspiration, collaboration, craft, diligence, decisiveness, taste, empathy — not the mythologized version. |
| *Steve Jobs* | Walter Isaacson | The full arc, including the failures; useful specifically for how obsessive taste and technical understanding combined, and how often it looked like failure from the inside. |
| *The Innovators* | Walter Isaacson | A history of computing built explicitly around the thesis that breakthroughs come from teams and collisions of disciplines, not lone genius — a useful corrective to the "genius" framing in your own goal. |
| *Where Good Ideas Come From* | Steven Johnson | A structural theory of innovation (adjacent possible, slow hunches, exaptation) that will help you recognize when you're actually onto something versus just excited. |
| *How to Solve It* | George Pólya | The classic on mathematical heuristics — how to actually get unstuck on a hard problem. Reread this every year or two; it reads differently as your technical level rises. |
| *Gödel, Escher, Bach* | Douglas Hofstadter | Deliberately cross-disciplinary (logic, art, music, cognition) — trains exactly the kind of analogical thinking that finds the same structure in two unrelated fields, which is the essence of the "epicentre" bet in the companion roadmap document. |
| *The Structure of Scientific Revolutions* | Thomas Kuhn | Understand how fields actually change — useful for recognizing paradigm-level opportunities rather than only incremental ones. |
| *Zero to One* | Peter Thiel | The "secrets" framing (what true thing do very few people agree with you on) is a genuinely useful lens for picking research directions, independent of your views on the author. |
| *Loonshots* | Safi Bahcall | A structural account (drawing on phase transitions in physics, fittingly) of why radical ideas die inside organizations and what protects them — relevant the moment you're inside any lab or company. |
| *The Innovator's Dilemma* | Clayton Christensen | Explains why frontier labs and incumbents miss the disruptive version of their own field — useful for spotting where the epicentre bet from the companion document is currently under-priced. |
| *Change by Design* | Tim Brown | Design thinking from IDEO's founder — the discipline of starting from human need rather than only from technical capability. |
| *Creative Confidence* | Tom Kelley & David Kelley | A practical, exercise-based companion to Change by Design. |
| *The Design of Everyday Things* | Don Norman | The foundational text on why some things are intuitive and others aren't — directly relevant if any of your later work involves a human interacting with a robot, an interface, or a tool. |
| *A Technique for Producing Ideas* | James Webb Young | A tiny, 40-page classic on the actual mechanics of idea generation (gather material, digest, incubate, the "aha," refine) — read it in an afternoon, then actually use the method. |

### Intuition-first companions to run alongside every technical stage (not a substitute for the rigorous texts — the thing you consume *before or alongside* them so the rigor lands on top of a real picture)
- **3Blue1Brown** (Grant Sanderson, YouTube) — linear algebra, calculus, differential equations, Fourier analysis, probability, neural networks, all made geometric. Watch the relevant series before or during the corresponding math stage below, every time, without exception.
- **Leonard Susskind's Theoretical Minimum** (Stanford, free on YouTube, with companion books) — full graduate-level treatments of classical mechanics, QM, statistical mechanics, special and general relativity that assume nothing but deliver real content — the single best free resource for a serious autodidact in physics.
- **The Feynman Lectures on Physics** (Feynman, Leighton, Sands — all three volumes free online via Caltech) — read alongside Morin/Griffiths/Sakurai in Stage 2, not instead of them; Feynman's is the intuition, the standard texts are the rigor and the problem sets.
- **60 Symbols and Periodic Videos** (University of Nottingham, YouTube) — short, faculty-led, genuinely curious explorations of physics and chemistry concepts; good for casual daily-reading-habit consumption alongside the heavier texts.
- **Visual Complex Analysis** — Tristan Needham, and **Visual Group Theory** — Nathan Carter: two textbooks that are themselves intuition-first treatments of otherwise dry, symbol-heavy subjects (complex analysis, group theory) — use these as the *first* pass before any more traditional rigorous text on the same subject.

---

## Track 0.5 — The Resource Stack: Tools, Channels, Practice Sites, Podcasts, Open Source

Track 0 described the *habits* (commonplace book, spaced repetition, weekly public writing, Feynman-it). This section names the actual tools and resources that implement those habits, plus the broader media diet and hands-on project pipeline that should run underneath every stage above.

### Note-taking & knowledge-management stack
Don't scatter notes across five apps — pick this stack once and stay in it for ten years, because the compounding value of a commonplace book comes from it being one continuous, searchable, cross-linked body, not from switching tools every year.

| Tool | Role |
|---|---|
| **Obsidian** | Your commonplace book / Zettelkasten from Track 0. Plain local text files (you own the data forever), bidirectional linking, and a graph view that visually surfaces the cross-field connections this whole plan is betting on — this is the single best fit for a STEM autodidact tracking interlinked ideas across math, physics, and AI. |
| **Anki** | Spaced repetition for anything you never want to re-derive from scratch — theorem statements, key formulas, definitions. |
| **GoodNotes** (iPad) or a **reMarkable** tablet | Handwritten math/physics notes and derivations — equation-heavy work is still faster and more natural by hand than typed, and a tablet lets you archive and search it. |
| **Zotero** | Reference manager once you start reading arXiv/journal papers seriously (Stage 3 onward) — tag, annotate, and cite papers without losing track of what you've read. |
| **Overleaf** | LaTeX in the browser, zero setup — use it the moment you write your first real problem set solutions or paper. |

### YouTube channels (beyond 3Blue1Brown, Susskind, and Karpathy, already named above)
| Channel | Best for |
|---|---|
| **Veritasium** | General physical intuition and genuinely excellent science storytelling — good for the daily casual-reading-habit slot. |
| **StatQuest (Josh Starmer)** | Turns intimidating statistics/ML formulas into something you can actually hold in your head — the single best channel for building stats intuition before Casella & Berger. |
| **Yannic Kilcher** | Critical, detailed paper walkthroughs (motivation, method, results, and what's actually wrong with the paper) — watch this to learn *how to read a paper skeptically*, not just to stay current. |
| **Two Minute Papers** | Fast breadth — bite-sized summaries of new results, good for a "what's happening in the field this week" habit. |
| **Numberphile / Computerphile** (Brady Haran) | Short, expert-led explorations of math and CS ideas — excellent daily-habit consumption. |
| **PBS Space Time** | Physics depth beyond the standard curriculum — relativity, cosmology, QFT-adjacent topics presented rigorously but accessibly. |
| **The Coding Train** (Daniel Shiffman) | Creative coding — directly feeds the Track 0 "build a toy of it" habit; makes programming feel playful rather than purely utilitarian. |
| **Applied Science** (Ben Krasnow) | Real hands-on experimental hardware building — the physical-apparatus habit from Stage 2, modeled by an expert. |
| **Steve Mould / Practical Engineering / Real Engineering** | Physical/engineering intuition, demos, and real-world failure analysis. |
| **Robert Miles** | AI safety/alignment intuition — a good complement to the mechanistic interpretability material in Stage 4/7. |

### Podcasts (for commute/gym/passive listening — never a substitute for active reading, always a supplement)
| Podcast | Why |
|---|---|
| **Dwarkesh Podcast** | The most technically-prepared interviewer currently working in AI — long, deeply-researched conversations with frontier researchers (Karpathy, lab leaders, etc.); described by peers as close to a public peer-review process for the field. |
| **Machine Learning Street Talk (MLST)** | Rigorous, hype-stripped technical discussion spanning AI, cognitive science, and philosophy of mind — the most substantive technical AI podcast currently running. |
| **Lex Fridman Podcast** | Broad, long-form interviews across AI, robotics, physics, and mathematics — useful for hearing researchers reason out loud, not just present polished results. |
| **Sean Carroll's Mindscape** | Physics and philosophy of science from a working theoretical physicist — good for the "why do we believe this" layer underneath the technical material. |
| **In Our Time** (BBC Radio 4) | History of science and ideas — feeds the cross-disciplinary, Inventor's-Library side of this plan, not the technical side. |
| **The Idea Factory's real-world cousin: Acquired** | Deep-dive business/company histories (including frontier-tech companies) — useful for understanding how research becomes an institution, echoing the Bell Labs and Apple books above. |
| **80,000 Hours Podcast** | Career-strategy and AI-safety-adjacent conversations — useful specifically when making the credentialing and vertical-choice decisions in Stage 3/7. |

### Practice websites (where you go to get unstuck, or to drill until something is automatic)
| Site | Use |
|---|---|
| **Project Euler** | Math + programming problems, increasing difficulty — the best ongoing test of whether Stage 1 skills are actually automatic. |
| **Brilliant.org** | Interactive, problem-first courses across math, physics, and CS — a good structured alternative when a textbook chapter isn't landing. |
| **Advent of Code** (every December) | A month of daily programming puzzles — excellent low-stakes way to keep coding fluency sharp between bigger projects. |
| **Codeforces / LeetCode** | Competitive programming and algorithm drills — directly supports the CLRS/6.006 work in Stage 1 and general coding-interview-grade fluency. |
| **Exercism** | Mentored code practice with human review — useful specifically for closing the gap between "my code runs" and "my code is good." |
| **Paul's Online Math Notes** (Lamar University) | Extremely clear worked examples for calculus/ODEs — the best free supplement when Apostol's proofs are clear but you want more computational practice. |
| **Seeing Theory** (Brown University) | Fully interactive, visual introduction to probability — use it *before* Ross, the same way you use 3Blue1Brown before a rigorous math text. |
| **Kaggle** | Real datasets, real competitions — already named in Stage 4, listed here again as your go-to practice site once ML fluency exists. |

### Open-source projects to actually contribute to (not just star)
Use GitHub's **`good first issue`** label and the community-maintained **`awesome-for-beginners`** list (github.com/MunGell/awesome-for-beginners) to find a live, currently-open entry point in any of these — the exact issue available will change by the time you read this, which is the point of using the label rather than a fixed task list:

- **PyTorch** and **scikit-learn** — both maintain active `good first issue` queues; nothing teaches you how a serious ML codebase is actually engineered like fixing a real, reviewed bug in one.
- **Hugging Face Transformers** and **Hugging Face LeRobot** — high-visibility, fast-moving, and directly relevant to Stage 4 and Stage 6.
- **PyMC** — Bayesian modeling library, a good place to put the probability/statistics rigor from Stage 2/3 into practice on real inference code.
- **MoveIt** — the standard open-source robotics manipulation planning platform, a direct, practical complement to the Lynch & Park material in Stage 6.
- **MuJoCo, NVIDIA Isaac Lab, TransformerLens, ROS2** — already named earlier as core tools; treat them as contribution targets, not just consumption targets, once you're using them daily.

---

## The Basics — Full Bottom-Up Reference (Stages 0-7)

Everything from here down is the original multi-year, bottom-up sequence. Treat it as the reference library the Fast Track above keeps sending you into — read a stage in full whenever you want the complete, unhurried, fully rigorous version of something the Fast Track only gave you "just enough" of, or run it as its own multi-year path if you'd rather build the foundation before the applications, subject by subject.

## Stage 0 — The Bridge (Months 0-6)

**Goal:** true algebraic fluency and fearless comfort writing a proof and a program, before calculus starts.

| Track | Resource | Why this one |
|---|---|---|
| Algebra, rebuilt properly | *Algebra* and *Trigonometry* — I.M. Gelfand & Shen / Gelfand & Saul | Gelfand rebuilds algebra as reasoning, not mechanical symbol-pushing — this matters enormously later, when you need to *derive* rather than *recall*. |
| Problem-solving intuition | Art of Problem Solving, *Introduction to Algebra* and *Introduction to Geometry*; AoPS's free **AoPS Online** community and forums | Competition-grade problem sets build the "stuck for an hour, then it clicks" muscle you'll need for the rest of this document; the AoPS forums are also a genuine early community of serious young problem-solvers. |
| Proof literacy (start now, not later) | *How to Prove It* — Daniel Velleman | Everyone who self-studies math hits a wall at "prove this" for the first time. Hitting that wall now, in isolation, is much cheaper than hitting it simultaneously with real analysis later. |
| Programming | CS50 (Harvard, free on edX) → *Automate the Boring Stuff with Python* (free online) | CS50 gives real CS fundamentals (memory, algorithms, C and Python); the second book converts that into daily fluency writing small useful scripts. |
| Popular-level physics intuition (start the Feynman/Susskind habit now) | *Six Easy Pieces* — Feynman; first few Theoretical Minimum lectures | No math prerequisite yet, but starts building physical intuition and the habit of watching Susskind before you need the rigor. |

**Build/creative add-on:** join or start visiting a local makerspace or hackerspace now (see the Directory section below) — not to build anything sophisticated, just to get comfortable with tools (soldering iron, 3D printer, basic electronics) before you need them for real projects in Stage 6.

**Prove it:** solve a full AoPS Introduction to Algebra problem set unaided; write and understand a two-page proof by induction and one by contradiction; write a Python script from scratch (no tutorial open) that reads data, transforms it, and plots something; write your first public "what I learned this month" post.

---

## Stage 1 — Calculus, Linear Algebra, Discrete Math (Year 1)

| Track | Resource |
|---|---|
| Calculus (rigor) | *Calculus*, Vol. 1 & 2 — Tom Apostol (integrates linear algebra with calculus, the classic hardcore choice) |
| Calculus (lectures) | MIT OCW 18.01 / 18.02 (Single & Multivariable Calculus) |
| Calculus (intuition) | 3Blue1Brown's *Essence of Calculus* series — watch this **first**, before Apostol, every chapter |
| Linear algebra (intuition first) | *Introduction to Linear Algebra* — Gilbert Strang + his MIT OCW 18.06 lectures (legendary — watch these regardless of what textbook you use) + 3Blue1Brown's *Essence of Linear Algebra* |
| Linear algebra (rigor, basis-free) | *Linear Algebra Done Right* — Sheldon Axler — do this **after** Strang, not instead of |
| Discrete math / logic / combinatorics | MIT OCW 6.042 (*Mathematics for Computer Science*) — free, excellent, feeds directly into CS |
| ODEs | MIT OCW 18.03 (*Differential Equations*) + 3Blue1Brown's *Differential Equations* series for the geometric picture first |
| CS fundamentals | *Introduction to Algorithms* — Cormen, Leiserson, Rivest, Stein (CLRS) + MIT OCW 6.006 |
| Complex analysis (intuition-first entry, useful later for signal processing/control) | *Visual Complex Analysis* — Tristan Needham |

**Build/creative add-on:** enter a local or virtual math competition (AMC/AIME if age-eligible, or Project Euler for a programming-flavored version) — not for the prize, but because competition problems train the "invent your own approach" muscle that pure textbook exercises don't.

**Prove it:** diagonalize a matrix and prove why the eigendecomposition works (not just compute it); solve a nontrivial ODE system by hand and verify numerically in code; implement a binary heap, a hash table, and Dijkstra's algorithm from scratch in a language with manual memory management (C or C++), no library calls; explain eigenvectors, in writing, to someone with no linear algebra background, using only the 3Blue1Brown geometric picture.

---

## Stage 2 — Physics Core & Probability (Years 1.5–3, overlapping Stage 1's tail)

| Track | Resource |
|---|---|
| Classical mechanics (first pass) | *Introduction to Classical Mechanics* — David Morin (Harvard) — problem-dense, do every problem you can |
| Classical mechanics (graduate depth, Lagrangian/Hamiltonian) | *Classical Mechanics* — Goldstein, Poole, Safko |
| Conceptual scaffolding across all of physics | Leonard Susskind's **Theoretical Minimum** lecture series (Stanford, free on YouTube) and companion books; **The Feynman Lectures on Physics** Vol. I-III (free online) read alongside every topic below |
| Electromagnetism | *Introduction to Electrodynamics* — David Griffiths + MIT OCW 8.02 |
| Thermodynamics & statistical mechanics | *An Introduction to Thermal Physics* — Daniel Schroeder, then *Statistical Physics of Particles* — Mehran Kardar (MIT, lecture notes free from his site; OCW 8.333/8.044) |
| Quantum mechanics | *Introduction to Quantum Mechanics* — Griffiths, then *Modern Quantum Mechanics* — J.J. Sakurai; *QED: The Strange Theory of Light and Matter* — Feynman, for the popular-level intuition companion |
| Probability (computational) | *A First Course in Probability* — Sheldon Ross |
| Mathematical statistics | *Statistical Inference* — Casella & Berger |
| Special/general relativity (rounds out the physics picture, feeds later GPS/sensor-fusion intuition) | Susskind's *Special Relativity and Classical Field Theory* and *General Relativity* (Theoretical Minimum volumes) |

**Build/creative add-on:** build a real physical apparatus that demonstrates something you just derived on paper — a double pendulum, a simple gyroscope, a basic optics bench — and compare your measured data to your theoretical prediction, documenting the discrepancy. This is the single highest-leverage habit in this whole document for making physics *permanent*: you cannot un-learn a law of physics you've personally watched fail to match a sloppy experiment and then figured out why.

**Prove it:** derive the equations of motion for a double pendulum from the Lagrangian and simulate it numerically, comparing to a naive Newtonian derivation, *and* to a real physical double pendulum you built or borrowed; solve the quantum harmonic oscillator and hydrogen atom by hand; compute a partition function and derive a thermodynamic quantity from it; solve a real probability problem (e.g. a Markov chain stationary distribution) both analytically and via Monte Carlo simulation, and check they agree.

---

## Stage 3 — Rigorous & Advanced Mathematics (Years 3–5)

This is the stage that makes the foundation "bulletproof" rather than merely functional — it's also the stage most self-taught people skip, and the gap shows up later as a ceiling on how deep you can go in ML theory, control theory, or physics-informed methods.

| Track | Resource |
|---|---|
| Real analysis | *Understanding Analysis* — Stephen Abbott (entry) → *Principles of Mathematical Analysis* — Walter Rudin ("baby Rudin," the classic, unavoidable) |
| Measure theory & rigorous probability | *Probability: Theory and Examples* — Rick Durrett (free PDF from the author) |
| Functional analysis | *Introductory Functional Analysis with Applications* — Erwin Kreyszig |
| Differential geometry & manifolds | *Differential Geometry of Curves and Surfaces* — do Carmo (intuition) → *Introduction to Smooth Manifolds* — John Lee (rigor) |
| Group theory (intuition first) | *Visual Group Theory* — Nathan Carter, before any abstract-algebra treatment |
| Lie groups applied directly to robotics (load-bearing text) | *A Mathematical Introduction to Robotic Manipulation* — Murray, Li, Sastry (**free PDF** from Sastry's Berkeley page) |
| Convex optimization | *Convex Optimization* — Boyd & Vandenberghe (**free PDF**) + Stanford EE364a lectures (free on YouTube) — this is non-negotiable, do every homework |
| Non-convex / large-scale optimization | *Numerical Optimization* — Nocedal & Wright |
| Numerical linear algebra / scientific computing | *Numerical Linear Algebra* — Trefethen & Bau; *Finite Difference Methods for ODEs and PDEs* — LeVeque; *Computational Science and Engineering* — Strang |
| Control theory | *Feedback Systems* — Åström & Murray (**free PDF**) → *Nonlinear Systems* — Khalil → *Dynamic Programming and Optimal Control* — Bertsekas |
| Information theory | *Elements of Information Theory* — Cover & Thomas |
| Category theory (light touch, differentiator not foundation) | *Category Theory for Programmers* — Bartosz Milewski (free online) |

**Build/creative add-on:** by this stage you should be entering serious competitions and formal remote research programs, not just reading — see the Directory below for the **Regeneron Science Talent Search / ISEF** (if still in the eligible age range), the **Wolfram High School Summer Research Program**, or the **Lumiere Research Scholar Program** (remote, 1:1 with a PhD mentor) as concrete, currently-real ways to produce original work at this stage rather than only textbook exercises.

**Prove it:** write a complete epsilon-delta proof of a nontrivial analysis theorem cold, without notes; prove convergence of gradient descent on a convex function from the Boyd text's framework; derive the dynamics of a robot arm using the Lie-group/twist formalism from Murray-Li-Sastry and implement a working controller for it in simulation; derive and implement a Kalman filter from its Bayesian first principles, not from a library; produce one piece of original written research (even small) suitable for submission to a program or competition from the Directory.

---

## Stage 4 — Core AI / Machine Learning (start Year 2, deepen through Year 6)

Start this early and in parallel with Stage 3 — ML intuition benefits from being built up gradually alongside the math, not bolted on afterward.

| Track | Resource |
|---|---|
| Classical ML foundations | Stanford CS229 (Andrew Ng — lecture notes are free and unusually rigorous) |
| Deep learning theory & practice | *Deep Learning* — Goodfellow, Bengio, Courville (free online); *Understanding Deep Learning* — Simon J.D. Prince (free online, more current, excellent modern complement); **fast.ai** (Jeremy Howard) for hands-on-first practical building |
| Classical statistical learning (bridges Stage 2/3 stats into ML) | *The Elements of Statistical Learning* — Hastie, Tibshirani, Friedman (free PDF); *Pattern Recognition and Machine Learning* — Christopher Bishop |
| Build understanding from raw code, not APIs | Andrej Karpathy's "Zero to Hero" YouTube series — build backprop, a tokenizer, and a GPT completely from scratch. This single series does more for "bulletproof" understanding than any framework tutorial. |
| Vision / language architecture depth | Stanford CS231n (vision, free lecture videos) and CS224n (NLP, free lecture videos) |
| Reinforcement learning | *Reinforcement Learning: An Introduction* — Sutton & Barto (free PDF, the canonical text) + David Silver's RL course (UCL/DeepMind, free on YouTube) + Berkeley CS285 (*Deep RL*, Sergey Levine, free lectures) |
| Probabilistic / Bayesian ML | *Probabilistic Machine Learning: An Introduction* and *...Advanced Topics* — Kevin Murphy (both free PDFs) |
| Generative models / diffusion | Original papers: Ho et al. (DDPM), Song et al. (score-based generative models); Yang Song's blog/lecture notes; Stanford CS236 (*Deep Generative Models*) |
| Transformers / LLMs | "Attention Is All You Need" (paper) + Jay Alammar's illustrated blog posts + Karpathy's nanoGPT walkthrough |
| Mechanistic interpretability | Chris Olah's *Circuits* work (distill.pub, transformer-circuits.pub); Neel Nanda's YouTube tutorials + his open-source **TransformerLens** library; Anthropic's *"A Mathematical Framework for Transformer Circuits"* |

**Build/creative add-on:** enter Kaggle competitions for fast feedback loops on real data; but also, deliberately, apply an ML method you just learned to a dataset or problem from a completely unrelated hobby or interest of yours (music, sports, a game you like, a local community problem) — the goal is training the reflex of seeing a learnable-pattern problem in the wild, which is the actual skill frontier labs pay for, not just executing a known recipe on a known benchmark.

**Prove it:** implement backpropagation from raw numpy with no autograd and verify it against PyTorch; train a small transformer from scratch on a toy corpus; implement PPO or DQN from scratch and solve a non-trivial control task; implement a diffusion model from scratch and generate recognizable samples; reproduce one small, real mechanistic-interpretability finding on an open-weight model (e.g. find a specific circuit in GPT-2-small using TransformerLens); apply one method to a self-chosen, non-benchmark problem and write up the result publicly.

---

## Stage 5 — AI Infrastructure & Systems (Years 3–6, interleaved)

| Track | Resource |
|---|---|
| Computer architecture | *Computer Organization and Design* — Patterson & Hennessy (entry) → *Computer Architecture: A Quantitative Approach* — Hennessy & Patterson (depth) |
| Operating systems | *Operating Systems: Three Easy Pieces* — Arpaci-Dusseau (free online, excellent) + MIT 6.S081 (build a kernel) |
| Parallel & GPU computing | *Programming Massively Parallel Processors* — Kirk & Hwu (the CUDA reference) + Stanford CS149 (*Parallel Computing*, free lectures) + NVIDIA's own free Deep Learning Institute CUDA courses |
| Compilers | *Crafting Interpreters* — Bob Nystrom (free online) as an entry point before ML-specific compiler work (XLA / MLIR / Triton documentation) |
| DNN accelerator design (the specific niche layer) | *Efficient Processing of Deep Neural Networks* — Sze, Chen, Yang, Emer (MIT, the standard reference) |
| Datacenter-scale systems | *The Datacenter as a Computer* — Barroso, Hölzle, Ranganathan (free online, Google's own reference on this exact topic) |
| Photonics (physics of the substrate) | *Fundamentals of Photonics* — Saleh & Teich |
| Neuromorphic computing | Kwabena Boahen's (Stanford) published lectures and papers; Intel Loihi 2 and BrainChip Akida developer documentation for hands-on programming |

**Build/creative add-on:** hardware hackathons are the single best format to compress months of "systems intuition" into a weekend of forced, real building under a deadline — see the Directory below for specific current events (StarkHacks at Purdue, Robotech at Georgia Tech, MakeCU at Columbia).

**Prove it:** write a custom CUDA kernel that measurably outperforms the naive PyTorch op it replaces; build a toy compiler for a small language; explain, from the datasheet, the dataflow and memory hierarchy of a real DNN accelerator; get a small spiking neural network actually running on neuromorphic hardware (or a cycle-accurate simulator of one) and characterize its power/latency versus a conventional implementation; ship something real at a hackathon within 36 hours.

---

## Stage 6 — Robotics & Control, Hands-On (Years 4–7)

| Track | Resource |
|---|---|
| Robot kinematics/dynamics/control, tied to the Lie-group math from Stage 3 | *Modern Robotics: Mechanics, Planning, and Control* — Lynch & Park (free textbook + free Coursera videos) |
| Alternative depth reference | *Robot Dynamics and Control* — Spong, Hutchinson, Vidyasagar |
| State estimation / SLAM | *Probabilistic Robotics* — Thrun, Burgard, Fox |
| Underactuated systems / the connective course to control theory in Stage 3 | Russ Tedrake's *Underactuated Robotics* (MIT, free online course and notes) |
| Simulation | MuJoCo (free, open-sourced), NVIDIA Isaac Lab / Isaac Sim, Genesis simulator — build real sim-to-real pipelines, don't just read about them |
| Middleware for real hardware | ROS2 |
| Cheap real hardware to actually touch | Hugging Face's **LeRobot** project and its low-cost arm kits (e.g. SO-100/SO-101-class kits) — genuinely current, cheap, community-supported entry point into real robot learning; a quadruped kit (e.g. Unitree Go2 EDU or an open-source design like Stanford Pupper) once manipulation is solid |

**Build/creative add-on:** this is exactly the stage to pursue a formal robotics REU (Oregon State's *Robots in the Real World*, Kent State's *AUTOBOT*, New Mexico Tech's *INTENSE* — see the Directory) — a real lab, real hardware budget, and a real mentor will teach you things no textbook or YouTube channel can about the gap between simulation and reality.

**Prove it:** build and run a full sim-to-real pipeline — train a manipulation policy in simulation, transfer it to cheap real hardware, and document the reality gap you hit and how you closed it; implement an MPC controller from scratch on a real or simulated system; implement a working SLAM pipeline from scratch, not from a library wrapper.

---

## Stage 7 — Synthesis, Research, and Becoming Known in the Field (Years 5–10+)

Books and courses build competence. This stage is what actually builds "genius of the field" recognition — original public work, real institutional access, and relationships with the people who define the frontier. None of it is optional if the goal is "any opportunity open to me."

### Daily/weekly habits
- Read arXiv (cs.LG, cs.RO, and the relevant physics categories) as a daily habit — this should already be an established habit from Track 0, just with more technical depth now. Use a real triage workflow (e.g. Papers with Code, Alphaxiv, or a disciplined personal reading log) so this compounds instead of evaporating.
- Keep writing publicly, weekly — the habit from Track 0, now applied to real papers, real reproductions, real original ideas from your commonplace book.

### Open source — where reputations are actually built
Contribute real, reviewed changes (not typo fixes) to: PyTorch, MuJoCo, NVIDIA Isaac Lab, Hugging Face LeRobot, TransformerLens. A merged nontrivial PR into any of these is worth more to your reputation than a semester of coursework, because it's public, verifiable, and reviewed by the people who matter.

### Competitions (early fluency, later prestige)
Kaggle (ML fluency, early); RoboCup / FIRST Robotics (hands-on robotics, if age allows); NeurIPS/ICML competition tracks (later, once you have real skill to bring).

### The credentialing decision (make this explicitly, around Year 2–4)
Self-study alone will build the knowledge in this document, but it rarely alone opens doors to elite research labs, funded PhD positions, or frontier-lab internships — those run on institutional access: an advisor's recommendation, a lab's internal referral, a formal REU. Once Stage 0–2 (and ideally a good chunk of Stage 3) is genuinely solid, seriously evaluate enrolling in a real degree program — even non-traditional or later-in-life entry, or a targeted specialized Master's — specifically to obtain lab access, an advisor, and letters of recommendation. Treat self-study as what gets you *admitted with unusually strong preparation*, not as a permanent substitute for the institution.

### People whose work should shape your thinking — and how to actually reach them
Don't cold-email asking generically for mentorship; it doesn't work and wastes the one shot you get. Instead: (1) study their specific work deeply, (2) produce a small, real artifact engaging with it — reproduce a result, extend an experiment, find and fix a bug in their released code, (3) reach out with *that concrete thing attached*, not a request to be taught, and (4) show up where they actually are — the specific conferences and workshops they publish and speak at.

| Person | Area | Why they matter here | Where to find them |
|---|---|---|---|
| Russ Tedrake | Robotics, control | MIT's free *Underactuated Robotics* course is essential; ties directly to Stage 3/6 math | MIT CSAIL; ICRA/RSS/CoRL |
| Sergey Levine | Robot learning, deep RL | Berkeley RAIL lab; defines much of modern sim-to-real and robot learning research | Berkeley; NeurIPS/ICML/CoRL |
| Stephen Boyd | Convex optimization | Wrote the textbook this whole plan leans on; Stanford EE364a lectures are free | Stanford; his free course materials |
| Michael Bronstein | Geometric deep learning | The Lie-group/manifold math in Stage 3 connects directly to his work | Oxford; NeurIPS/ICML |
| George Karniadakis | Physics-informed ML (PINNs) | Originated the field connecting Stage 2/3 physics directly to modern ML | Brown; relevant SciML workshops |
| Yann LeCun | World models, self-supervised learning (JEPA) | Defines a major alternative research direction for the "world model" niche | Public talks, papers |
| Chris Olah | Mechanistic interpretability | Founded the field as practiced today; distill.pub and transformer-circuits.pub are essential reading | Anthropic; his public writing |
| Neel Nanda | Mechanistic interpretability | Extremely active public educator; his TransformerLens tutorials are how most people actually learn to do this hands-on | DeepMind; YouTube, public tutorials |
| Alán Aspuru-Guzik | Self-driving labs, materials discovery | Leading figure connecting AI + autonomous experimentation | University of Toronto (Matter Lab) |
| David Baker | Protein design | Nobel laureate (2024) for computational protein design; Rosetta/RFdiffusion define the field | University of Washington |
| John Preskill | Quantum computing, error correction | Foundational figure in quantum information theory | Caltech; QIP conference |
| Kwabena Boahen | Neuromorphic computing | Leading figure connecting device physics to brain-inspired computing | Stanford |

### Publication targets (realistic, not aspirational)
First workshop-paper-level contribution within 3–4 years of starting; first real peer-reviewed conference paper (NeurIPS/ICML/ICRA/CoRL/RSS depending on your Layer-2 vertical) within 5–7 years.

**Prove it (the only milestone that actually matters for this stage):** a public body of work — code, writing, at least one nontrivial open-source contribution, and ideally one publication or workshop paper — that a stranger in the field could look at and conclude, unprompted, that you're serious. That artifact, not a self-assessment, is what "genius of the field" actually cashes out to.

---

## Programs, Labs, Hackathons & Competitions Directory (US-focused, local and remote)

These are real, current (2026) entry points — apply to the ones matching your current stage, and re-check listings yearly since REU/fellowship cohorts and deadlines change every cycle. Treat **reufinder.com** and the **Society for Science** competitions page as your yearly refresh source for anything that's gone stale by the time you read this.

### Entry point, no prerequisites (start immediately — Stage 0/1)
- **Local hackerspace or makerspace** — nearly every US city has one (directory: hackerspaces.org); join now for tool access and a community of builders, independent of your current skill level.
- **Regeneron Science Talent Search** and **Regeneron International Science and Engineering Fair (ISEF)** (Society for Science) — the US's oldest and largest pre-college research competitions; STS awarded $1.8M+ and ISEF $7M+ in 2026 alone. Entering forces you to produce one real, original piece of research well before you'd otherwise attempt it.
- **Project Euler**, **AMC/AIME** (if age-eligible) — ongoing, no application needed.

### Remote research, high-school/early-undergraduate stage (Stage 2/3)
- **Wolfram High School Summer Research Program** — 3-week fully virtual research experience (ages 15-18) on computational projects in AI, physics, and related STEM fields with actual Wolfram scientists.
- **Lumiere Research Scholar Program** — fully remote, pairs you 1:1 with a PhD mentor on an independent research project; founded by Harvard/Oxford researchers.
- **ASPIRE Program, Johns Hopkins Applied Physics Laboratory** — for high school juniors/seniors, matched with a real APL mentor on live projects in AI, cybersecurity, or aerospace engineering.

### In-person, paid, undergraduate-stage REUs and national-lab internships (Stage 3-6)
- **Oregon State University REU: "Robots in the Real World"** — Corvallis, OR, summer program, open to CS/ME/EE/math/physics backgrounds, broad robotics research.
- **Kent State University AUTOBOT REU** — robotics/AI/UAV/guidance-navigation-control, $6,000 stipend plus housing and travel reimbursement.
- **New Mexico Institute of Mining and Technology INTENSE REU** — robotics, smart materials, shock physics, tied to federally funded research projects.
- **DOE SULI (Science Undergraduate Laboratory Internships)** — paid placement at one of 17 US Department of Energy national labs, 10 weeks summer or 16 weeks fall/spring, physics/CS/engineering, some remote projects available.
- **NIST SURF (Summer Undergraduate Research Fellowship)** — 11-week program, mostly in-person, strong physics/CS presence.
- Use **reufinder.com** to pull the current year's full list filtered to AI/robotics/physics/math — this changes annually and is not exhaustively listable here.

### Hardware hackathons and robotics competitions (any stage, ongoing, weekend-format)
- **StarkHacks** (Purdue University, hosted by the Humanoid Robot Club) — large-scale hardware hackathon, hundreds of participants, real prize pools.
- **Robotech Hackathon** (Georgia Tech IEEE Student Chapter) — free, 36-hour robotics build-and-compete event open to students within traveling distance.
- **MakeCU** (Columbia University Robotics Club) — flagship hardware hackathon.
- **FIRST Robotics / RoboCup** — longer-format, team-based robotics competitions, excellent if age/stage allows sustained team involvement.

### Frontier-lab and hardware-vertical internships (Stage 7, later-stage)
- University lab positions once you have institutional access: MIT CSAIL, Stanford SAIL, Berkeley RAIL — apply as an undergraduate researcher the moment you're enrolled.
- Frontier AI lab research internships: Anthropic, OpenAI, Google DeepMind — require a strong public portfolio (see Stage 7 above), usually alongside a degree in progress.
- Hardware-vertical labs for the physics-heavy verticals from the companion roadmap: **Commonwealth Fusion Systems** and ITER-adjacent programs (fusion); **IBM Quantum** and **Google Quantum AI** (quantum computing/control).

---

## How this maps back to the strategic roadmap

- Track 0 and the Inventor's Library are new relative to the companion roadmap's Layer structure — they are the mechanism that turns Layer 0/1 technical fluency into actual original insight and public visibility, rather than just competence.
- Stages 0–2 build **Layer 0** (universal foundations) from `ai-robotics-expertise-roadmap.md`.
- Stage 3 completes Layer 0 and starts **Layer 1** (the cross-cutting methods: differentiable simulation, Bayesian experimental design, optimal control, numerical linear algebra, hardware-aware inference).
- Stages 4–6 build Layer 1 out concretely across at least two substrates each (per that document's Phase 2 instruction — don't let every project be a robotics project).
- Stage 7 is that document's Phase 3 (vertical choice, made late) plus the actual mechanism — publications, open source, people, labs — by which "knowledge" converts into "opportunity."
