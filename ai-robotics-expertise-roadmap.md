# Expertise Roadmap: Robotics × AI × AI Infra × Mathematics × Physics
*A 10-year positioning plan, written 2026-07-29*

## The core bet

Two macro shifts define the next decade, and they point at the same intersection.

**1. The robotics/embodied-AI market is inflecting, not incrementing.** Humanoid robot market forecasts for 2035 range from $50B (MarketsandMarkets, 28% CAGR) to $192B (GM Insights, 37.6% CAGR) to $165B (Fortune Business Insights, 50.6% CAGR) — a spread that itself signals a market nobody has priced correctly yet, which is exactly where outsized returns to expertise live. Manufacturing deployment is growing fastest (27-30%), and Asia-Pacific is expected to hold >50% share. [Sources: gminsights.com, marketsandmarkets via finance.yahoo.com, fortunebusinessinsights.com]

**2. AI competition is shifting from "more data/more parameters" to "physical grounding + efficient silicon."** In June 2026, 13 new embodied-AI foundation models shipped — one every 48 hours — and the field explicitly frames this as *robotics competition shifting from hardware to software intelligence*. Simultaneously, 2026 is the year inference compute overtakes training compute in data centers, and custom ASICs/chiplets are beating general GPUs on cost-per-inference. The interconnect (not the chip) is now the bottleneck — co-packaged optics, photonics. [Sources: eweek.com, vast.ai, insidedeeptech.com, semiwiki.com]

Put together: the money is moving into *bodies that act in the physical world*, and the compute story moving under it is *specialized, power-constrained, physically-adjacent silicon* (photonics, neuromorphic, edge inference). A pure ML researcher (no physics, no hardware literacy) and a pure controls/mechanical engineer (no modern learning, no hardware literacy) are each missing two of the three legs. The person who has genuine depth in classical/statistical physics, the applied math that makes simulation and control tractable, and modern learned world models/policies, *and* understands what's actually deployable on real silicon — that person is the epicentre. This is a deliberately narrow bet, not "learn everything a little."

**Positioning statement for 2036:** be the person who can (1) derive a robot's dynamics from first principles (Lagrangian/Hamiltonian mechanics), (2) build a learned world model that respects those dynamics well enough to close the sim-to-real gap, (3) train and run it efficiently using the numerical/optimization machinery under the hood, (4) know what that policy can and cannot do on the power/latency budget of the actual target chip (photonic, neuromorphic, or edge ASIC), and (5) verify/interpret the resulting behavior well enough to certify it on a body that can hurt someone if it's wrong.

---

## Why each pillar, and the *exact* niche within it

### Physics

- **Lagrangian & Hamiltonian mechanics** — not "physics 101," but the actual formalism robot dynamics are written in, and simultaneously the formalism modern physics-informed and geometric deep learning borrows wholesale (Hamiltonian neural networks, symplectic integrators, Neural ODEs on manifolds). Learning it once pays for both a robotics job and a physics-informed-ML job.
- **Nonlinear dynamics & stability theory** (Lyapunov functions, contraction analysis, limit cycles) — this is what turns "the policy usually works" into "the policy is provably stable," which is the actual requirement for shipping a humanoid, not a demo.
- **Statistical mechanics & stochastic processes** (Langevin dynamics, Fokker-Planck) — this is the literal math under diffusion and flow-matching models, which the 2026 literature shows are now the dominant policy architecture for dexterous manipulation ("diffusion policies," diffusion-based robot foundation models). Most ML people use diffusion models without knowing where they came from; that gap is your edge.
- **Condensed matter / photonics / semiconductor device physics** — the AI infra bottleneck moved from "the chip" to "between chips, between racks" (co-packaged optics, silicon photonics), and neuromorphic computing runs on genuinely new device physics (nanolasers, spiking hardware). Almost no one works this seam between physics-of-the-substrate and AI systems; it is a near-empty niche today. [Source: semiwiki.com, photonics.com, patsnap.com neuromorphic landscape]

### Pure Mathematics

- **Differential geometry & Lie groups (SO(3)/SE(3))** — every rigid-body robot's configuration space *is* a Lie group; this is also exactly the math behind equivariant and geometric deep learning. One investment, two payoffs.
- **Optimization theory** (convex, non-convex landscape theory, Riemannian optimization on manifolds) — 2026 research explicitly flags optimization as *the* primary lever left for cutting frontier training costs, and Riemannian optimization is required the moment your parameters live on SO(3)/SE(3) instead of flat Euclidean space (i.e., the moment you're doing robotics, not chatbots).
- **Measure-theoretic probability & information theory** (entropy, KL divergence, rate-distortion) — underlies generative/diffusion models, RL exploration bounds, and is explicitly the toolkit used for rigorous model evaluation and interpretability metrics in current research.
- **Category theory / compositional structure (light touch, not a full specialization)** — increasingly used to formalize compositionality in world models and multi-agent/program-synthesis systems. Treat as a differentiator you layer on later, not a foundation.

### Applied Mathematics

- **Numerical linear algebra & scientific computing** (low-rank/sparse factorizations, randomized NLA) — this is literally what makes large models trainable/servable at all (quantization, low-rank adapters, KV-cache compression); it's the applied-math layer directly behind the AI-infra story above.
- **PDEs & numerical methods for continuum/contact mechanics** — required to build *differentiable physics simulators*, and the 2026 robotics literature names the sim-to-real gap in contact dynamics as *the* unsolved bottleneck in dexterous manipulation, not a solved problem you can skip.
- **Optimal & stochastic control (MPC, LQR/LQG, Pontryagin)** — the real-time workhorse that current robot stacks blend with learned models; almost every deployed humanoid controller today is "learned model + classical MPC," not learned model alone.
- **Estimation theory & sensor fusion** (Kalman/particle filters) — every real robot needs to fuse noisy proprioception, vision, and tactile signals; this is unglamorous but load-bearing, and most ML-only people have never touched it.

### AI (core algorithms)

- **World models grounded in physics, not just video prediction** — named directly as the 2026 answer to the expense of collecting real embodied interaction data, with an explicitly acknowledged gap between simulated and real dynamics. This is your synthesis point with the physics/applied-math track above.
- **Vision-Language-Action (VLA) architectures** — the current dominant paradigm for embodied foundation models, but current literature is explicit that purely reactive VLA policies fail at long-horizon reasoning and compounding error — meaning the *next* wave (hybrid VLA + world-model + planning) is still open, not commoditized.
- **Diffusion / flow-matching policies for control** — confirmed as the leading architecture class for dexterous manipulation in 2026; pairs directly with your stochastic-processes physics.
- **Mechanistic interpretability, specifically for control/embodied policies (not just LLMs)** — interpretability is a booming, well-funded category (Anthropic, OpenAI, DeepMind, government AI safety institutes) but is almost entirely applied to language models. Nobody is doing serious interpretability of embodied/control policies, where the stakes (a humanoid that fails) are physical, not textual. This is a genuinely open sub-niche.

### AI Infrastructure

- **Hardware-software co-design for inference** (chiplets, sparsity-aware custom ASICs) — 2026 is the confirmed inflection where inference overtakes training compute and custom silicon starts beating GPUs on cost; patent filings in this exact area rose ~30x (11→335) from 2017-2025.
- **Neuromorphic / spiking computation for power-constrained edge robotics** — a humanoid cannot carry a data-center power budget; spiking/neuromorphic hardware is the physically-motivated answer, and it's still a research-stage field with room for a newcomer.
- **Photonics & co-packaged optics / interconnect** — explicitly named as *the* emerging AI-infra bottleneck for 2026+ ("bottleneck is no longer the chip, it's between chips/racks/switches"). This sits directly on your condensed-matter/photonics physics track — deliberately don't treat AI infra and physics as separate tracks; they're one track here.
- **Do not over-invest in generic distributed-training systems (megascale LLM pretraining infra)** — this is the most crowded, most commoditized corner of AI infra; the alpha has moved to the edge/embodied/inference side.

### Robotics (applied synthesis layer)

- **Whole-body control for legged/humanoid locomotion** (contact-rich dynamics, balance) — direct consequence of the market data: this is where the money and the jobs are concentrating.
- **Tactile sensing & contact-rich manipulation** — named explicitly as unsolved; the reality gap in simulating contact is the single most-cited blocker in current dexterous-manipulation papers.
- **Sim-to-real transfer & differentiable simulation** — the connective tissue between your physics/applied-math training and your AI training; this is where you personally close the gap the field is stuck on.

---

## Sequencing (what to actually study, in order)

**Phase 1 — Foundations (now → ~2 years)**
Real analysis, linear algebra (proof-based, not just computational), multivariable calc, probability & intro measure theory, convex optimization, classical mechanics (Lagrangian/Hamiltonian). In parallel: deep learning fundamentals (backprop, transformers, diffusion basics), solid systems skills (C++, CUDA basics, Linux, PyTorch), and enough digital logic/computer architecture to read a chip datasheet without flinching.

**Phase 2 — Specialization core (~2 → 5 years)**
Differential geometry & Lie groups, nonlinear control & stability theory, optimal/stochastic control (MPC), numerical methods for PDEs/contact mechanics, reinforcement learning & model-based RL / world models, VLA architectures. Pick *one* hardware-adjacent lane to go deep in now (photonics/silicon device physics **or** neuromorphic computing) rather than both — go deep, not broad, here.

**Phase 3 — Synthesis (~5 → 10 years)**
Combine into the actual niche: build/train physically-grounded world models for contact-rich manipulation, run them through the constraints of your chosen hardware lane, and add interpretability/verification for embodied policies as the safety layer. This is where you stop "studying" in the abstract and start working with real robot hardware, real sim-to-real pipelines (MuJoCo, Isaac Lab, Genesis-class simulators), and publishing/open-sourcing in the exact seam identified above — because that seam is where the field visibly doesn't have enough people yet.

---

## Sources
- [Humanoid Robot Market Size, Forecasts Report 2026-2035 (GM Insights)](https://www.gminsights.com/industry-analysis/humanoid-robot-market)
- [Humanoid Robot Market worth $50.27B by 2035 (MarketsandMarkets via Yahoo Finance)](https://finance.yahoo.com/technology/ai/articles/humanoid-robot-market-worth-50-140100251.html)
- [Humanoid Robot Market Size, Share Report (Fortune Business Insights)](https://www.fortunebusinessinsights.com/humanoid-robots-market-110188)
- [The global market for humanoid robots could reach $38B by 2035 (Goldman Sachs)](https://www.goldmansachs.com/insights/articles/the-global-market-for-robots-could-reach-38-billion-by-2035)
- [The State of AI Infrastructure 2026: Compute, Power, and Constraints](https://www.insidedeeptech.com/the-state-of-ai-infrastructure-2026-compute-power-and-constraints/)
- [The Future of AI Inference in 2026 (vast.ai)](https://vast.ai/article/the-future-of-ai-inference-in-2026)
- [Key Trends Shaping the Semiconductor Industry in 2026 (Edge AI and Vision Alliance)](https://www.edge-ai-vision.com/2026/04/key-trends-shaping-the-semiconductor-industry-in-2026/)
- [OFC 2026 Summary: Silicon Photonics, CPO, OCI, OCS (SemiWiki)](https://semiwiki.com/forum/threads/ofc-2026-summary-how-silicon-photonics-cpo-oci-and-ocs-are-redefining-the-physical-boundaries-of-data-centers.24852/)
- [Integrated Optics: Breaking the Bandwidth Bottleneck for Hyperscale AI (Photonics Spectra)](https://www.photonics.com/Articles/Integrated-Optics-Breaking-the-Bandwidth/a71993)
- [Every 48 Hours, a New Embodied AI Model Arrived in June 2026 (eWeek)](https://www.eweek.com/news/embodied-ai-robot-foundation-models/)
- [Foundation Models in Robotics: A Comprehensive Review (arXiv)](https://arxiv.org/pdf/2604.15395)
- [World Model for Robot Learning: A Comprehensive Survey (arXiv)](https://arxiv.org/html/2605.00080v1)
- [Sim-to-Real RL for Vision-Based Dexterous Manipulation on Humanoids (arXiv)](https://arxiv.org/abs/2502.20396)
- [Performant robotic manipulation with real-world RL (Science Robotics)](https://www.science.org/doi/10.1126/scirobotics.aed6267)
- [Physics-Informed Machine Learning collection (Nature)](https://www.nature.com/collections/jaihfcabgi)
- [Neuromorphic Computing SNN Landscape 2026 (PatSnap Eureka)](https://www.patsnap.com/resources/blog/rd-blog/neuromorphic-computing-snn-landscape-2026-patsnap-eureka/)
- [Neuromorphic computing for robotic vision: algorithms to hardware advances (Nature Communications Engineering)](https://www.nature.com/articles/s44172-025-00492-5)
- [The AI Revolution in Math Has Arrived (Quanta Magazine)](https://www.quantamagazine.org/the-ai-revolution-in-math-has-arrived-20260413/)
- [Mechanistic Interpretability for AI Safety — A Review (arXiv)](https://arxiv.org/pdf/2404.14082)
- [AI safety technical research career review (80,000 Hours)](https://80000hours.org/career-reviews/ai-safety-researcher/)
