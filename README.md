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

**ML & Bioinformatics Researcher — University at Buffalo** (Professor Ram Samudrala) · 2026–present
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

**Medlee** *(private)* — A multi-agent medication-safety pipeline for geriatric polypharmacy, built on one
rule: **structured sources are the source of truth; the LLM only interprets.** Five Claude Sonnet agents
(normalize → drug-interaction → Beers 2023 → clinical context → synthesize) read only orchestrator-fetched
RxNorm / safety-DB records and emit pydantic-validated, individually-cited flags — so a hallucinated drug
code can never reach the database. A deterministic oversight layer scores every run (geometric mean of
schema validity, inter-agent agreement, citation coverage, and signal coverage; threshold 0.85), retries
the weakest agent once with targeted feedback, then escalates to human review or an Opus spot-check that
fails closed. Every agent has a deterministic rule-based twin, so the LLM scaffolding swaps out
slot-by-slot without touching anything downstream. *Multi-agent orchestration · LLM-as-interpreter ·
deterministic eval/oversight · RxNorm · pydantic*

**[NYPD Scheduling Optimizer](https://github.com/fkenmar/NYPD-Scheduling-Optimizer)** ·
[live dashboard](https://fkenmar.github.io/NYPD-Scheduling-Optimizer/) — K-Means clustering + LightGBM to
predict precinct-level crime demand by time of day from ~2.3M NYC Open Data records — **0.908 test
accuracy** — feeding a weekly-refreshed interactive dashboard. *Data-intensive ML · PySpark · end-to-end*

**[BatMan](https://github.com/fkenmar/BatMan)** — A Fourier-native, phase-preserving baseline for
automatic modulation classification on RadioML 2018.01A: the network takes complex I/Q samples, runs an
FFT *inside* the model, and feeds complex-valued spectral residual blocks, reported down to −20 dB SNR.
Groundwork for a drone-detection / RF-jamming agent. *DSP × deep learning · complex-valued nets*

**DigitCells OCR pipeline** *(private)* — A custom OCR + validation pipeline that turns scanned pathology
records into analysis-ready Excel. Generates consistent pseudo-IDs for de-identification, auto-assigns the
L1–L3 classification hierarchy and codes, and validates every value against a controlled classification
vocabulary — flagging missing files, out-of-vocab values, and questionable readings for pathologist
review. Folds full L2 descriptions and patient context into cell comments and tallies category counts per
level. *Python · OCR · clinical data pipelines · HIPAA-conscious*

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
