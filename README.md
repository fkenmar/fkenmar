### Hey, I'm Kenmar Francisco

[![LinkedIn](https://img.shields.io/badge/LinkedIn-fkenmar-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/fkenmar/) [![Email](https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:kenmarfrancisco9@gmail.com) [![Hugging Face](https://img.shields.io/badge/Hugging%20Face-knmrfr-FFD21E?style=flat&logo=huggingface&logoColor=black)](https://huggingface.co/knmrfr)

**AI / ML engineer** building agents — and the eval infrastructure that proves they actually work. CS (AI concentration) at the University at Buffalo · U.S. Citizen. Currently forward-deploying agent workflows at Koi AgeTech Ventures and doing ML/bioinformatics research in Professor Ram Samudrala's lab. Recent: a [deepfake detector](https://github.com/fkenmar/Deepfake-Detector) at **98% ROC-AUC** on 300k+ images ([live demo](https://huggingface.co/spaces/knmrfr/deepfake-detector-demo)), and [RepoBrain](https://github.com/fkenmar/RepoBrain), a Rust codebase-mapper that **cut agent turns 41–43%**.

#### Experience

- **Forward Deployed Engineer Intern — Koi AgeTech Ventures** · 2026–present — PDF-to-dataset agent workflows with AI governance over 100k+-record healthcare datasets: schema mapping, drug-data API integration, extraction-confidence thresholds, patient–drug risk logic.
- **ML & Bioinformatics Researcher — University at Buffalo** *(Professor Ram Samudrala)* · 2026–present — ranking therapeutic candidates for muscle-wasting via the CANDO platform + DiffDock docking; investigating frequency-domain (FFT) features for model robustness and generalization.
- **AI Data Manager — DigitCells** · 2026–present — validated 2,500+ AI-generated pathology outputs across 25,000+ clinical fields at **99%+ review accuracy**, resolving 500+ model/metadata inconsistencies in HIPAA-conscious workflows.
- **Software Engineer — Body Alliance Physical Therapy** · 2025–2026 — built an AI movement-analysis observer giving therapists real-time feedback during PT sessions: **+15% patient outcomes, +20% engagement**.

#### Building

- **[Deepfake Detector](https://github.com/fkenmar/Deepfake-Detector)** · [live demo](https://huggingface.co/spaces/knmrfr/deepfake-detector-demo) — two-branch fusion classifier: a DoRA-fine-tuned CLIP ViT-L/14 backbone fused with a CNN over the 2D FFT magnitude spectrum, trained SupCon + cross-entropy. **98% ROC-AUC on 300k+ images**, improved cross-generator generalization, featured in Handshake's Learn Hub. *PyTorch · PEFT (DoRA) · multimodal fusion · deployed*
- **Medlee** *(private)* — multi-agent medication-safety pipeline for geriatric polypharmacy on one rule: **structured sources are the source of truth; the LLM only interprets**. Five Claude Sonnet agents read only orchestrator-fetched RxNorm/safety-DB records and emit pydantic-validated, individually-cited flags; a deterministic oversight layer scores every run, retries the weakest agent once, then escalates to human review or an Opus spot-check that fails closed. *Multi-agent orchestration · LLM-as-interpreter · deterministic eval*
- **[RepoBrain](https://github.com/fkenmar/RepoBrain)** — Rust CLI that compiles a codebase into a token-budgeted structural map for LLM coding agents: tree-sitter parse → personalized PageRank over the import/reference graph → packed to a token budget, so a 50k-LOC repo becomes a ~2k-token summary an agent holds in context. On a 10-task Claude Code benchmark, **cut agent turns 41–43%**. *Rust · tree-sitter · agent tooling · benchmarked*- **[NYPD Scheduling Optimizer](https://github.com/fkenmar/NYPD-Scheduling-Optimizer)** · [live dashboard](https://fkenmar.github.io/NYPD-Scheduling-Optimizer/) — K-Means clustering + LightGBM predicting precinct-level crime demand by time of day from ~2.3M NYC Open Data records (**0.908 test accuracy**), feeding a weekly-refreshed interactive dashboard. *PySpark · end-to-end ML*
- **[BatMan](https://github.com/fkenmar/BatMan)** — Fourier-native, phase-preserving baseline for automatic modulation classification on RadioML 2018.01A: complex I/Q samples in, an FFT *inside* the model, complex-valued spectral residual blocks reported down to −20 dB SNR. Groundwork for a drone-detection / RF-jamming agent. *DSP × deep learning · complex-valued nets*
- **DigitCells OCR pipeline** *(private)* — custom OCR + validation pipeline turning scanned pathology records into analysis-ready Excel: de-identifying pseudo-IDs, auto-assigned L1–L3 classification, controlled-vocabulary validation, and pathologist-review flags for missing/out-of-vocab/questionable values. *Python · OCR · clinical data pipelines*

#### Reach me

kenmarfrancisco9@gmail.com · kenmarfr@buffalo.edu · [résumé](resume.pdf)

<sub>Python · Rust · PyTorch · scikit-learn · PySpark · FastAPI · Next.js · React · tree-sitter · Docker</sub>
