# Expertise Roadmap: A Transferable Deep-Tech Stack
*A 10-year positioning plan — robotics as one output, not the destination. Written 2026-07-29, revised same day to generalize across deep tech.*

## The reframe

The first version of this plan aimed the same core stack (physics + pure math + applied math + AI + AI infra) squarely at humanoid robotics. That was a mistake in framing, not in content: almost everything in that stack was never robotics-specific — robotics was just the first vertical I hung it on. The actual insight is one level up.

**Every deep-tech frontier in 2026 reduces to the same abstract loop:** a learned model proposes an action or design → a physical (or simulated) system executes it → sensors/assays/detectors observe the outcome → the model updates. Call it Design-Build-Test-Learn, model-predictive control, or closed-loop autonomous experimentation — it's the same object wearing different clothes:

- **Robotics:** policy proposes a motor command → robot body executes it → proprioception/vision observes → world model updates.
- **Self-driving materials/chemistry labs:** AI proposes a synthesis → robotic arm executes it → spectroscopy observes → model updates. [Sources: matter.toronto.edu, Nature Communications Materials, qpillars.com]
- **Protein/drug design:** generative model proposes a sequence → the physics of folding "executes" it → assay/structure prediction observes → model updates. [Sources: openpr.com AI Protein Design Market, intuitionlabs.ai]
- **Quantum error correction:** decoder proposes a correction → hardware applies it within a computational cycle → syndrome measurement observes → decoder updates, now at sub-microsecond latency on custom silicon. [Sources: IBM Quantum Technology Atlas 2026, riverlane.com, thequantuminsider.com]
- **Fusion/plasma control:** controller proposes a magnetic field adjustment → the plasma (governed by PDEs) responds → sensors observe → controller updates in real time.

Once you see it this way, the "epicentre" isn't a robotics specialization — it's fluency in the primitives that make *any* closed loop like this work: the physics of the substrate, the math that makes simulation/control/inference tractable, the learned model that closes the loop, and the hardware that makes it fast/cheap/power-feasible enough to run in real time. That's why deep-tech VC in 2026 is explicitly rewarding this exact combination: $26.1B into climate tech in H1 2026 alone (+55% YoY), record fusion rounds ($900M Series A at Pacific Fusion), and — tellingly — **"technical de-risking has replaced growth velocity as the primary metric for follow-on funding," with hardware-focused infrastructure investment dominating the highest-valuation segments.** [Source: insidedeeptech.com Deep Tech Funding 2026] That is a market explicitly paying for people who can de-risk the physics/hardware/math, not just the software layer on top.

**Positioning statement, revised:** don't become "a humanoid robotics person." Become the person who is fluent in closed-loop learned control of physical systems — the physics of the substrate, the applied math that simulates and controls it, the AI that learns from it, and the hardware that runs it fast enough — such that you can walk into robotics, materials discovery, protein design, quantum control, or fusion/energy and be productive within months, because you already own the shared 80%. The vertical becomes a late, reversible choice driven by where the best data/lab access/market timing is in a given year — not a bet you make at 22 and are stuck with at 32.

---

## Layer 0: Universal foundations (unchanged, and now clearly general-purpose)

This layer was already field-agnostic; the earlier document just described it through a robotics lens. Restated by *why it transfers everywhere*, not by which vertical it serves:

- **Real analysis, linear algebra (proof-based), multivariable calculus, measure-theoretic probability** — the load-bearing language under every quantitative deep-tech field, full stop. No vertical-specific justification needed; skipping this closes doors permanently.
- **Classical mechanics (Lagrangian/Hamiltonian)** — the formalism of robot dynamics, *and* of Hamiltonian neural networks, *and* of the symplectic integrators used in molecular dynamics for protein folding, *and* of plasma/fluid modeling in fusion. One derivation, four verticals.
- **Statistical mechanics & stochastic processes** — underlies diffusion/flow-matching models (robotics policies, protein generative models, materials generative design), and is the literal physics of noise in quantum hardware and thermodynamic limits of computation (relevant to any hardware-efficiency question).
- **Information theory & entropy** — model evaluation and uncertainty quantification in *every* field above; also the exact language of quantum error correction (syndrome decoding is an information-theoretic problem).
- **Convex & non-convex optimization, later Riemannian optimization** — the training algorithm underneath any of the AI systems in any vertical, and directly needed the moment your parameters live on a manifold (robot configuration spaces, molecular conformations, quantum gate spaces all do).
- **Differential geometry & Lie groups** — rigid-body robotics (SE(3)), molecular conformation spaces, quantum gate manifolds (SU(2)/SU(N)) — the same object recurs everywhere physical configuration matters.

---

## Layer 1: The cross-cutting methods (the actual transferable core)

This is the layer that makes the stack "go anywhere," and it was under-emphasized in the first draft because it was filtered through robotics-only examples. These five methods are what actually recur, verbatim, across every vertical in Layer 2:

1. **Differentiable simulation & scientific machine learning (SciML)** — physics-informed neural nets, neural operators (e.g. Fourier Neural Operators), differentiable physics engines. In robotics this closes the sim-to-real gap; in materials/chemistry it's the surrogate model inside a self-driving lab; in fusion it's the fast plasma surrogate that makes real-time control possible; in drug discovery it's the differentiable folding/docking model.
2. **Bayesian inference & experimental design (active learning)** — literally the algorithm inside every Design-Build-Test-Learn loop: deciding *what experiment/action to try next* under uncertainty. Self-driving labs, protein design campaigns, robot exploration policies, and fusion operating-point search are all instances of Bayesian optimization / active learning over a physical search space.
3. **Optimal & stochastic control, real-time estimation (MPC, Kalman/particle filters)** — the closed-loop controller itself, whether the "plant" being controlled is a robot arm, a tokamak's plasma, or a quantum error-correction cycle.
4. **Numerical linear algebra & low-rank/sparse methods** — what makes any of the above tractable at scale (quantization, compressed sensing in imaging/spectroscopy, low-rank surrogates for expensive PDEs).
5. **Hardware-software co-design for real-time inference** — the difference between a decoder that works in a paper and one that works on real quantum hardware is sub-microsecond latency on custom silicon; the difference between a lab-demo robot policy and a deployed one is running within a power/latency budget on an edge chip. Same skill, same reasoning, different plant.

Master these five as *general methods*, each with one worked example from at least two different verticals, and you have a stack that is not "a robotics stack" — it is a deep-tech stack that happens to be demonstrable in robotics.

---

## Layer 2: The vertical menu (swap freely, choose late)

Each of these is a legitimate landing spot for the exact same Layer 0/1 stack. Treat this as a menu you revisit around year 5-7, not a decision to make now.

### Robotics & embodied AI
Humanoid market forecasts range $50B-$192B by 2035 (28-50% CAGR); the bottleneck is explicitly sim-to-real/contact dynamics (Layer 1 #1) and real-time control (#3) on power-constrained edge hardware (#5). [Sources: gminsights.com, marketsandmarkets, fortunebusinessinsights.com]

### Computational biology & protein/drug design
AI protein design market projected to grow from ~$1.5B (2025) to $6.98B (2033); Generate Biomedicines' $425M IPO and the Recursion/NVIDIA compute expansion show the field is now compute- and infra-bound, not just biology-bound. Same Bayesian-design-loop (#2) and physics-informed generative modeling (#1, via statistical mechanics of folding) as robotics, applied to sequences instead of joint angles. [Sources: openpr.com, intuitionlabs.ai]

### Materials science & self-driving labs
Materials/chemistry lead current self-driving-lab adoption, with the field explicitly moving to "SDL 2.0": modular, agent-orchestrated Design-Build-Test-Learn loops. This is Layer 1 #1+#2 with a chemistry robot instead of a humanoid — closest structural cousin to robotics of any vertical here. [Sources: matter.toronto.edu, Nature Communications Materials, royalsocietypublishing.org]

### Quantum computing & control
2026 is the year error correction became engineering, not theory: 90-100 logical qubits, sub-microsecond decoders, exponential error suppression. This vertical is almost pure Layer 1 #3 (real-time control) + #5 (hardware co-design) + information theory from Layer 0 — arguably the most math-dense, least "AI-flavored" of the menu, good fit if you end up preferring the physics/hardware end of the stack over the learned-model end. [Sources: IBM Quantum Technology Atlas 2026, riverlane.com, thequantuminsider.com]

### Fusion & energy systems
Record capital concentration (Pacific Fusion's $900M Series A, General Fusion going public) and climate tech VC at $26.1B in H1 2026 alone, with money concentrating in fewer, larger, hardware-heavy bets. Plasma control is nonlinear PDE control in real time — Layer 0 (PDEs, nonlinear dynamics) and Layer 1 #1+#3 directly, almost no AI-specific work needed until you get to using learned surrogates for the (extremely expensive) physics simulations. [Sources: winssolutions.org, cleanenergy-platform.com]

*(Robotics-specific items from the original draft — whole-body locomotion control, tactile sensing, VLA architectures, humanoid-specific interpretability — still belong here; they've just been demoted from "the plan" to "one menu item," which is the point.)*

---

## Sequencing (revised)

**Phase 1 — Foundations (now → ~2 years): unchanged.**
Real analysis, linear algebra, probability/measure theory, convex optimization, classical mechanics, deep learning fundamentals, systems/programming (C++, CUDA, PyTorch, Linux). Vertical-agnostic by design — do not pick a vertical yet.

**Phase 2 — Cross-cutting methods (~2 → 5 years): reframed.**
Instead of "robotics specialization," build the five Layer 1 methods as portable skills, each demonstrated on **at least two different substrates** (e.g., build one differentiable-simulation project on a robot arm and one on a molecular system; one Bayesian active-learning project on a materials search and one on a robot exploration task). This is the deliberate difference from the first draft: force cross-vertical transfer early, before specializing, so you *know* the stack generalizes rather than assuming it.

**Phase 3 — Vertical choice (~5 → 10 years): now explicit and late.**
Pick the Layer 2 vertical based on where the market, the available lab/data access, and your own aptitude (learned-model-heavy vs. hardware/control-heavy) line up *at that time* — not based on what seemed exciting at 22. Because Layers 0-1 are shared, switching verticals even at year 6-7 costs you months, not years.

---

## Sources
- [Humanoid Robot Market Size, Forecasts Report 2026-2035 (GM Insights)](https://www.gminsights.com/industry-analysis/humanoid-robot-market)
- [Humanoid Robot Market worth $50.27B by 2035 (MarketsandMarkets via Yahoo Finance)](https://finance.yahoo.com/technology/ai/articles/humanoid-robot-market-worth-50-140100251.html)
- [Humanoid Robot Market Size, Share Report (Fortune Business Insights)](https://www.fortunebusinessinsights.com/humanoid-robots-market-110188)
- [AI for Discovery and Self-Driving Labs (The Matter Lab, Toronto)](https://www.matter.toronto.edu/basic-content-page/ai-for-discovery-and-self-driving-labs)
- [Managing autonomous materials labs with multi-agent AI (Nature Communications Materials)](https://www.nature.com/articles/s43246-026-01219-5)
- [Self-Driving Labs in 2026 - What Actually Works vs. What's Still Hype (QPillars)](https://qpillars.com/blog/self-driving-labs-2026-what-works-vs-hype)
- [Autonomous 'self-driving' laboratories: a review of technology (Royal Society Open Science)](https://royalsocietypublishing.org/rsos/article/12/7/250646/235354/Autonomous-self-driving-laboratories-a-review-of)
- [AI Protein Design Market 2026: The $6.9B Opportunity (OpenPR)](https://www.openpr.com/news/4486902/ai-protein-design-market-2026-the-6-9b-opportunity)
- [AI Biologics Discovery: 2026 Pharma Investment Trends (IntuitionLabs)](https://intuitionlabs.ai/articles/ai-biologics-discovery-pharma-investment-trends)
- [Quantum 2026 — IBM Technology Atlas](https://www.ibm.com/roadmaps/quantum/2026/)
- [Quantum Error Correction: 2025 trends and 2026 predictions (Riverlane)](https://www.riverlane.com/blog/quantum-error-correction-our-2025-trends-and-2026-predictions)
- [Understanding Quantum Error Correction (The Quantum Insider)](https://thequantuminsider.com/2026/03/16/understanding-quantum-error-correction-physical-logical-qubits/)
- [Climate tech VC funding hits $26.1bn in H1 2026 (Wins Solutions)](https://www.winssolutions.org/climate-tech-vc-funding-h1-2026/)
- [Fusion Industry Investment Trends 2026 (Clean Energy Platform)](https://www.cleanenergy-platform.com/insight/fusion-industry-investment-trends-2026-where-the-money-is-going)
- [Deep Tech Funding in 2026: Where the Money Is Actually Going (Inside Deep Tech)](https://www.insidedeeptech.com/deep-tech-funding-in-2026-where-the-money-is-actually-going/)
- [Top Deep Tech & Hard Science VC Firms — 2026 Guide (Waveup)](https://waveup.com/blog/top-deep-tech-and-hard-science-venture-capital-firms/)
- *(Original robotics/AI-infra/physics sources retained from the first draft — see git history for the full list.)*
