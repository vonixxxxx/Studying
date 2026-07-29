# From High School Algebra to the Epicentre: A Full Curriculum
*Companion to `ai-robotics-expertise-roadmap.md`. That document is the strategic "why" and "which niches." This document is the operational "how" — books, lectures, projects, people, labs — assuming you start with nothing but high school algebra.*

## How to use this document

This is not a reading list to complete linearly and then "graduate." It is a curriculum where **math, physics, programming, and building things run in parallel from day one**, because bulletproof foundations are built by hitting the same idea from four directions (a proof, a physical derivation, a line of code, a real experiment), not by mastering one subject before touching the next. Each stage below lists a rough elapsed-time window assuming serious, near-daily effort (10-25 hrs/week); treat the timing as a planning tool, not a deadline — depth beats speed everywhere in this document. Every stage ends with a **"prove it" milestone** — a concrete, checkable output, not a feeling of having learned something. If you can't do the milestone, you're not done with the stage, regardless of how many books you've "read."

Four disciplines run **concurrently, always**, from Stage 0 onward: (1) rigorous math, (2) physics, (3) programming/CS, (4) building — a project, a robot, a model, a lab notebook. Treat any week where only one of these four moved as a warning sign.

---

## Stage 0 — The Bridge (Months 0-6)

**Goal:** true algebraic fluency and fearless comfort writing a proof and a program, before calculus starts.

| Track | Resource | Why this one |
|---|---|---|
| Algebra, rebuilt properly | *Algebra* and *Trigonometry* — I.M. Gelfand & Shen / Gelfand & Saul | Gelfand rebuilds algebra as reasoning, not mechanical symbol-pushing — this matters enormously later, when you need to *derive* rather than *recall*. |
| Problem-solving intuition | Art of Problem Solving, *Introduction to Algebra* and *Introduction to Geometry* | Competition-grade problem sets build the "stuck for an hour, then it clicks" muscle you'll need for the rest of this document. |
| Proof literacy (start now, not later) | *How to Prove It* — Daniel Velleman | Everyone who self-studies math hits a wall at "prove this" for the first time. Hitting that wall now, in isolation, is much cheaper than hitting it simultaneously with real analysis later. |
| Programming | CS50 (Harvard, free on edX) → *Automate the Boring Stuff with Python* (free online) | CS50 gives real CS fundamentals (memory, algorithms, C and Python); the second book converts that into daily fluency writing small useful scripts. |

**Prove it:** solve a full AoPS Introduction to Algebra problem set unaided; write and understand a two-page proof by induction and one by contradiction; write a Python script from scratch (no tutorial open) that reads data, transforms it, and plots something.

---

## Stage 1 — Calculus, Linear Algebra, Discrete Math (Year 1)

| Track | Resource |
|---|---|
| Calculus (rigor) | *Calculus*, Vol. 1 & 2 — Tom Apostol (integrates linear algebra with calculus, the classic hardcore choice) |
| Calculus (lectures) | MIT OCW 18.01 / 18.02 (Single & Multivariable Calculus) |
| Linear algebra (intuition first) | *Introduction to Linear Algebra* — Gilbert Strang + his MIT OCW 18.06 lectures (legendary — watch these regardless of what textbook you use) |
| Linear algebra (rigor, basis-free) | *Linear Algebra Done Right* — Sheldon Axler — do this **after** Strang, not instead of |
| Discrete math / logic / combinatorics | MIT OCW 6.042 (*Mathematics for Computer Science*) — free, excellent, feeds directly into CS |
| ODEs | MIT OCW 18.03 (*Differential Equations*) |
| CS fundamentals | *Introduction to Algorithms* — Cormen, Leiserson, Rivest, Stein (CLRS) + MIT OCW 6.006 |

**Prove it:** diagonalize a matrix and prove why the eigendecomposition works (not just compute it); solve a nontrivial ODE system by hand and verify numerically in code; implement a binary heap, a hash table, and Dijkstra's algorithm from scratch in a language with manual memory management (C or C++), no library calls.

---

## Stage 2 — Physics Core & Probability (Years 1.5–3, overlapping Stage 1's tail)

| Track | Resource |
|---|---|
| Classical mechanics (first pass) | *Introduction to Classical Mechanics* — David Morin (Harvard) — problem-dense, do every problem you can |
| Classical mechanics (graduate depth, Lagrangian/Hamiltonian) | *Classical Mechanics* — Goldstein, Poole, Safko |
| Conceptual scaffolding across all of physics | Leonard Susskind's **Theoretical Minimum** lecture series (Stanford, free on YouTube) and companion books — uniquely good for a self-studier because it assumes nothing but delivers real graduate-level content |
| Electromagnetism | *Introduction to Electrodynamics* — David Griffiths + MIT OCW 8.02 |
| Thermodynamics & statistical mechanics | *An Introduction to Thermal Physics* — Daniel Schroeder, then *Statistical Physics of Particles* — Mehran Kardar (MIT, lecture notes free from his site; OCW 8.333/8.044) |
| Quantum mechanics | *Introduction to Quantum Mechanics* — Griffiths, then *Modern Quantum Mechanics* — J.J. Sakurai |
| Probability (computational) | *A First Course in Probability* — Sheldon Ross |
| Mathematical statistics | *Statistical Inference* — Casella & Berger |

**Prove it:** derive the equations of motion for a double pendulum from the Lagrangian and simulate it numerically, comparing to a naive Newtonian derivation; solve the quantum harmonic oscillator and hydrogen atom by hand; compute a partition function and derive a thermodynamic quantity from it; solve a real probability problem (e.g. a Markov chain stationary distribution) both analytically and via Monte Carlo simulation, and check they agree.

---

## Stage 3 — Rigorous & Advanced Mathematics (Years 3–5)

This is the stage that makes the foundation "bulletproof" rather than merely functional — it's also the stage most self-taught people skip, and the gap shows up later as a ceiling on how deep you can go in ML theory, control theory, or physics-informed methods.

| Track | Resource |
|---|---|
| Real analysis | *Understanding Analysis* — Stephen Abbott (entry) → *Principles of Mathematical Analysis* — Walter Rudin ("baby Rudin," the classic, unavoidable) |
| Measure theory & rigorous probability | *Probability: Theory and Examples* — Rick Durrett (free PDF from the author) |
| Functional analysis | *Introductory Functional Analysis with Applications* — Erwin Kreyszig |
| Differential geometry & manifolds | *Differential Geometry of Curves and Surfaces* — do Carmo (intuition) → *Introduction to Smooth Manifolds* — John Lee (rigor) |
| Lie groups applied directly to robotics (load-bearing text) | *A Mathematical Introduction to Robotic Manipulation* — Murray, Li, Sastry (**free PDF** from Sastry's Berkeley page) |
| Convex optimization | *Convex Optimization* — Boyd & Vandenberghe (**free PDF**) + Stanford EE364a lectures (free on YouTube) — this is non-negotiable, do every homework |
| Non-convex / large-scale optimization | *Numerical Optimization* — Nocedal & Wright |
| Numerical linear algebra / scientific computing | *Numerical Linear Algebra* — Trefethen & Bau; *Finite Difference Methods for ODEs and PDEs* — LeVeque; *Computational Science and Engineering* — Strang |
| Control theory | *Feedback Systems* — Åström & Murray (**free PDF**) → *Nonlinear Systems* — Khalil → *Dynamic Programming and Optimal Control* — Bertsekas |
| Information theory | *Elements of Information Theory* — Cover & Thomas |

**Prove it:** write a complete epsilon-delta proof of a nontrivial analysis theorem cold, without notes; prove convergence of gradient descent on a convex function from the Boyd text's framework; derive the dynamics of a robot arm using the Lie-group/twist formalism from Murray-Li-Sastry and implement a working controller for it in simulation; derive and implement a Kalman filter from its Bayesian first principles, not from a library.

---

## Stage 4 — Core AI / Machine Learning (start Year 2, deepen through Year 6)

Start this early and in parallel with Stage 3 — ML intuition benefits from being built up gradually alongside the math, not bolted on afterward.

| Track | Resource |
|---|---|
| Classical ML foundations | Stanford CS229 (Andrew Ng — lecture notes are free and unusually rigorous) |
| Deep learning theory & practice | *Deep Learning* — Goodfellow, Bengio, Courville (free online) for theory; **fast.ai** (Jeremy Howard) for hands-on-first practical building |
| Build understanding from raw code, not APIs | Andrej Karpathy's "Zero to Hero" YouTube series — build backprop, a tokenizer, and a GPT completely from scratch. This single series does more for "bulletproof" understanding than any framework tutorial. |
| Vision / language architecture depth | Stanford CS231n (vision, free lecture videos) and CS224n (NLP, free lecture videos) |
| Reinforcement learning | *Reinforcement Learning: An Introduction* — Sutton & Barto (free PDF, the canonical text) + David Silver's RL course (UCL/DeepMind, free on YouTube) + Berkeley CS285 (*Deep RL*, Sergey Levine, free lectures) |
| Probabilistic / Bayesian ML | *Probabilistic Machine Learning: An Introduction* and *...Advanced Topics* — Kevin Murphy (both free PDFs) |
| Generative models / diffusion | Original papers: Ho et al. (DDPM), Song et al. (score-based generative models); Yang Song's blog/lecture notes; Stanford CS236 (*Deep Generative Models*) |
| Transformers / LLMs | "Attention Is All You Need" (paper) + Jay Alammar's illustrated blog posts + Karpathy's nanoGPT walkthrough |
| Mechanistic interpretability | Chris Olah's *Circuits* work (distill.pub, transformer-circuits.pub); Neel Nanda's YouTube tutorials + his open-source **TransformerLens** library; Anthropic's *"A Mathematical Framework for Transformer Circuits"* |

**Prove it:** implement backpropagation from raw numpy with no autograd and verify it against PyTorch; train a small transformer from scratch on a toy corpus; implement PPO or DQN from scratch and solve a non-trivial control task; implement a diffusion model from scratch and generate recognizable samples; reproduce one small, real mechanistic-interpretability finding on an open-weight model (e.g. find a specific circuit in GPT-2-small using TransformerLens).

---

## Stage 5 — AI Infrastructure & Systems (Years 3–6, interleaved)

| Track | Resource |
|---|---|
| Computer architecture | *Computer Organization and Design* — Patterson & Hennessy (entry) → *Computer Architecture: A Quantitative Approach* — Hennessy & Patterson (depth) |
| Operating systems | *Operating Systems: Three Easy Pieces* — Arpaci-Dusseau (free online, excellent) + MIT 6.S081 (build a kernel) |
| Parallel & GPU computing | *Programming Massively Parallel Processors* — Kirk & Hwu (the CUDA reference) + Stanford CS149 (*Parallel Computing*, free lectures) |
| Compilers | *Crafting Interpreters* — Bob Nystrom (free online) as an entry point before ML-specific compiler work (XLA / MLIR / Triton documentation) |
| DNN accelerator design (the specific niche layer) | *Efficient Processing of Deep Neural Networks* — Sze, Chen, Yang, Emer (MIT, the standard reference) |
| Photonics (physics of the substrate) | *Fundamentals of Photonics* — Saleh & Teich |
| Neuromorphic computing | Kwabena Boahen's (Stanford) published lectures and papers; Intel Loihi 2 and BrainChip Akida developer documentation for hands-on programming |

**Prove it:** write a custom CUDA kernel that measurably outperforms the naive PyTorch op it replaces; build a toy compiler for a small language; explain, from the datasheet, the dataflow and memory hierarchy of a real DNN accelerator; get a small spiking neural network actually running on neuromorphic hardware (or a cycle-accurate simulator of one) and characterize its power/latency versus a conventional implementation.

---

## Stage 6 — Robotics & Control, Hands-On (Years 4–7)

| Track | Resource |
|---|---|
| Robot kinematics/dynamics/control, tied to the Lie-group math from Stage 3 | *Modern Robotics: Mechanics, Planning, and Control* — Lynch & Park (free textbook + free Coursera videos) |
| State estimation / SLAM | *Probabilistic Robotics* — Thrun, Burgard, Fox |
| Simulation | MuJoCo (free, open-sourced), NVIDIA Isaac Lab / Isaac Sim, Genesis simulator — build real sim-to-real pipelines, don't just read about them |
| Middleware for real hardware | ROS2 |
| Cheap real hardware to actually touch | Hugging Face's **LeRobot** project and its low-cost arm kits (e.g. SO-100/SO-101-class kits) — genuinely current, cheap, community-supported entry point into real robot learning; a quadruped kit (e.g. Unitree Go2 EDU or an open-source design like Stanford Pupper) once manipulation is solid |

**Prove it:** build and run a full sim-to-real pipeline — train a manipulation policy in simulation, transfer it to cheap real hardware, and document the reality gap you hit and how you closed it; implement an MPC controller from scratch on a real or simulated system; implement a working SLAM pipeline from scratch, not from a library wrapper.

---

## Stage 7 — Synthesis, Research, and Becoming Known in the Field (Years 5–10+)

Books and courses build competence. This stage is what actually builds "genius of the field" recognition — original public work, real institutional access, and relationships with the people who define the frontier. None of it is optional if the goal is "any opportunity open to me."

### Daily/weekly habits
- Read arXiv (cs.LG, cs.RO, and the relevant physics categories) as a daily habit, not a occasional binge. Use a real triage workflow (e.g. Papers with Code, Alphaxiv, or simply a disciplined personal reading log) so this compounds instead of evaporating.
- Write up what you learn publicly (a blog, a GitHub with real READMEs, X/Twitter threads on papers you've actually reproduced). Visibility compounds exactly like the math does — nobody discovers "genius" that's never been shown.

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

### Internships and labs to target explicitly
University research positions (MIT CSAIL, Stanford SAIL, Berkeley RAIL — apply as an undergraduate researcher/UROP-equivalent the moment you have institutional access); frontier AI lab research internships (Anthropic, OpenAI, Google DeepMind — these require a strong public portfolio, usually alongside a degree in progress); hardware-adjacent national/industry labs for the physics-heavy verticals (fusion: Commonwealth Fusion Systems, ITER-adjacent programs; quantum: IBM Quantum, Google Quantum AI).

### Publication targets (realistic, not aspirational)
First workshop-paper-level contribution within 3–4 years of starting; first real peer-reviewed conference paper (NeurIPS/ICML/ICRA/CoRL/RSS depending on your Layer-2 vertical) within 5–7 years.

**Prove it (the only milestone that actually matters for this stage):** a public body of work — code, writing, at least one nontrivial open-source contribution, and ideally one publication or workshop paper — that a stranger in the field could look at and conclude, unprompted, that you're serious. That artifact, not a self-assessment, is what "genius of the field" actually cashes out to.

---

## How this maps back to the strategic roadmap

- Stages 0–2 build **Layer 0** (universal foundations) from `ai-robotics-expertise-roadmap.md`.
- Stage 3 completes Layer 0 and starts **Layer 1** (the cross-cutting methods: differentiable simulation, Bayesian experimental design, optimal control, numerical linear algebra, hardware-aware inference).
- Stages 4–6 build Layer 1 out concretely across at least two substrates each (per that document's Phase 2 instruction — don't let every project be a robotics project).
- Stage 7 is that document's Phase 3 (vertical choice, made late) plus the actual mechanism — publications, open source, people, labs — by which "knowledge" converts into "opportunity."
