# Kenmar Francisco

**AI / ML Engineer.** I build agents — and the eval infrastructure that tells me whether they actually work.
CS (AI concentration) at the University at Buffalo · U.S. Citizen.

I've been taking software apart since elementary school: Cheat Engine and hex edits, then forums and
Minecraft mods in high school. These days it's AI agents and the harnesses that keep them honest. What I
took from doing ML the long way — *Hands-On Machine Learning*, cover to cover — is that no architecture is
*correct* for a task. A model is a generalization, so the work stays half analytic (read the data, run the
experiment) and half intuition. I like that it keeps a human in the loop.

## Experience

**Forward Deployed Engineer Intern — Koi AgeTech Ventures** · 2026–present
Building PDF-to-dataset agent workflows with AI governance over 100k+-record healthcare datasets — schema
mapping, drug-data API integration, extraction-confidence thresholds, and patient–drug risk logic.

**ML & Bioinformatics Researcher — University at Buffalo** (Samudrala & Ratha labs) · 2026–present
Ranking therapeutic candidates for muscle-wasting with the CANDO platform and DiffDock molecular docking,
and investigating frequency-domain (FFT) feature methods to improve model robustness and generalization.

**AI Data Manager — DigitCells** · 2026–present
Validated 2,500+ AI-generated pathology outputs across 25,000+ clinical fields at 99%+ review accuracy,
resolving 500+ model/metadata inconsistencies in HIPAA-conscious workflows.

**Software Engineer — Body Alliance Physical Therapy** · 2025–2026
Built an AI movement-analysis observer giving therapists real-time feedback during PT sessions —
**+15% patient outcomes, +20% engagement.**

## Selected work

**[Deepfake Detector](https://github.com/fkenmar/Deepfake-Detector)** ·
[live demo](https://huggingface.co/spaces/knmrfr/deepfake-detector-demo) — A two-branch fusion classifier:
a DoRA-fine-tuned CLIP ViT-L/14 backbone (spatial features) fused with a CNN over the 2D FFT magnitude
spectrum (frequency artifacts), trained SupCon + cross-entropy. **98% ROC-AUC on 300k+ images**, improved
cross-generator generalization, featured in Handshake's Learn Hub. Flask API + React/Vite, deployed on
Hugging Face Spaces. *PyTorch · PEFT (DoRA) · multimodal fusion · deployed*

**[RepoBrain](https://github.com/fkenmar/RepoBrain)** — A Rust CLI that compiles a codebase into a
token-budgeted structural map for LLM coding agents: tree-sitter parse → personalized PageRank over the
import/reference graph → packed to a token budget, so a 50k-LOC repo becomes a ~2k-token summary an agent
holds entirely in context. The thesis is measured, not assumed — on a 10-task Claude Code benchmark,
injecting the map cut agent turns **41–43%**. *Rust · tree-sitter · agent tooling · benchmarked*

**[drift](https://github.com/fkenmar/drift)** — An agentic-AI eval harness disguised as a colony sim.
Your colonists are AI agents, the world is a noisy eval, and a Storyteller throws prompt injection, drift,
and deprecations at your fleet while you keep it shipping under budget. Under the hood: a zero-dependency
Python core (mock backend, graders, scoring), a FastAPI streaming server, and a Next.js front end. Built
eval-first, TDD. *Python · FastAPI · Next.js · evals*

**[NYPD Scheduling Optimizer](https://github.com/fkenmar/NYPD-Scheduling-Optimizer)** ·
[live dashboard](https://fkenmar.github.io/NYPD-Scheduling-Optimizer/) — K-Means clustering + LightGBM to
predict precinct-level crime demand by time of day from ~2.3M NYC Open Data records — **0.908 test
accuracy** — feeding a weekly-refreshed interactive dashboard. *Data-intensive ML · PySpark · end-to-end*

**[BatMan](https://github.com/fkenmar/BatMan)** — A Fourier-native, phase-preserving baseline for
automatic modulation classification on RadioML 2018.01A: the network takes complex I/Q samples, runs an
FFT *inside* the model, and feeds complex-valued spectral residual blocks, reported down to −20 dB SNR.
Groundwork for a drone-detection / RF-jamming agent. *DSP × deep learning · complex-valued nets*

## How I think about the work

- **Evals before features.** If I can't measure it, I don't trust it — hence the harness in *drift* and
  the benchmark in *RepoBrain*.
- **Ship the thinnest real thing.** A deployed demo beats a slide. Most of the above has one.
- **TDD where correctness matters,** demos where speed of learning matters.

## Reach me

- **Email** — kenmarfrancisco9@gmail.com · kenmarfr@buffalo.edu
- **LinkedIn** — [linkedin.com/in/fkenmar](https://www.linkedin.com/in/fkenmar/)
- **Résumé** — [resume.pdf](resume.pdf)

<sub>Python · Rust · PyTorch · scikit-learn · PySpark · FastAPI · Next.js · React · tree-sitter · Docker</sub>
