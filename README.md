<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=000000&height=120&section=header&text=⚡%20Aadi%20Pathak%20⚡&fontSize=42&fontColor=00BFFF&animation=twinkling&stroke=1E90FF&strokeWidth=2" alt="Aadi Pathak Banner"/>
</p>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Orbitron&size=26&duration=3000&pause=1000&color=FF6F00&center=true&vCenter=true&width=750&lines=MS+CS+(AI%2FML)+%40+UC+Davis;Fine-tuning+%26+Evaluating+VLMs;Edge+Inference+on+6+GB+GPUs;Physical+AI+Safety;Cricket+Club+President+🏏" alt="Typing SVG"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Vision--Language%20Models-%2376B900.svg?&style=for-the-badge&logo=nvidia&logoColor=white"/>
  <img src="https://img.shields.io/badge/PEFT%20%7C%20QLoRA%20%7C%20DoRA-%23FF6F00.svg?&style=for-the-badge&logo=huggingface&logoColor=white"/>
  <img src="https://img.shields.io/badge/Physical%20AI-%2300C7B7.svg?&style=for-the-badge&logo=ros&logoColor=white"/>
  <img src="https://img.shields.io/badge/Cricket-%23FF4500.svg?&style=for-the-badge&logoColor=white"/>
</p>

<p align="center">
  <a href="https://www.aadipathak.com"><img src="https://img.shields.io/badge/-Portfolio-00BFFF?style=for-the-badge&logo=vercel&logoColor=white"/></a>
  <a href="https://www.linkedin.com/in/aadipathak/"><img src="https://img.shields.io/badge/-LinkedIn-blue?style=for-the-badge&logo=Linkedin"/></a>
  <a href="mailto:aadipathak2323@gmail.com"><img src="https://img.shields.io/badge/-Email-red?style=for-the-badge&logo=gmail&logoColor=white"/></a>
</p>

---

## 👋 About Me

MS Computer Science (AI/ML) student at **UC Davis**. I fine-tune, evaluate and serve **vision-language models for physical AI**, and I care a lot about evaluation that doesn't fool itself: freeze the protocol before the results exist, compare against a strong baseline, and publish the limitations next to the numbers.

- 🎓 **M.S. CS (AI/ML) @ UC Davis** (2026–present) · B.S. CS @ Arizona State University (2026)
- 🔬 **Graduate Researcher @ [CHPS Lab](https://cphslab.com), UC Davis:** drone computer vision for wildlife health
- 🛡️ Working on **post-deployment safety for physical AI** (private for now)
- 🧠 Hands-on with **QLoRA / DoRA / LoRA, Hugging Face, bitsandbytes, CUDA, FastAPI, Docker, AWS**

---

## 🚀 Selected Work

### 🪶 [featherweight-ai](https://github.com/AadiPathak23/featherweight-ai): budget-matched PEFT for an edge VLM
QLoRA, DoRA and LoRA on NVIDIA **Cosmos-Reason2-2B**, compared at equal wall-clock time and peak VRAM on free-tier hardware (6 GB laptop GPU, Kaggle T4).
- 📈 QLoRA under a 60-minute budget on a 6 GB GPU: **47.2% vs 31.9%** zero-shot on a held-out night split (n = 659). That is **+15.3 pp over a per-question-type prior**, with McNemar p = 6.5e-9 and a scene-clustered bootstrap 95% CI of 9.7 to 21.0 pp.
- 🕵️ Found that **235 of 241 training images also appeared in the evaluation split** (byte-identical) before any training step, and rebuilt the benchmark as a leak-free day-to-night domain-shift evaluation.
- 🧯 Built an fp16 instability tripwire that halts on consecutive gradient-scaler skips, and validated it with a deliberate sabotage run.
- ⏳ *In progress:* the LoRA vs DoRA vs QLoRA comparison, seed variance, and edge latency/VRAM.

### ⚡ [cosmos-edge-serve](https://github.com/AadiPathak23/cosmos-edge-serve): serving a reasoning VLM on small GPUs
FastAPI + Docker inference service for Cosmos-Reason2-2B (image or video plus a prompt in, reasoning plus answer out). It runs 4-bit NF4 so it fits on 6 GB.
- ✅ Verified end to end on real weights, with 35 tests passing.
- 📊 A k6 load-test harness and EC2 T4 runbook are written and dry-run. No T4 numbers are published until they're actually measured.

### ⚗️ [distillery](https://github.com/AadiPathak23/distillery): self-verifying fine-tuning datasets
A multi-agent pipeline (planner → generator → critic → evaluator) that builds LLM fine-tuning datasets.
- 🧪 For code data it **executes the generated pytest tests in a sandbox and rejects the ones that fail**, instead of trusting the model.
- 🚫 It refuses to write empty or fully filtered datasets, and logs full telemetry for every run. CI on GitHub Actions.

### 🎙️ [Jaarvis](https://github.com/AadiPathak23/Jaarvis-Personal-assistant): local voice assistant for AI news
A fully local assistant with wake word (openWakeWord), speech-to-text (Whisper), streaming TTS (Piper), Hacker News AI-news ingestion and ranking, a FastAPI backend, a React dashboard and a Telegram bot.

### 🔍 [Atlas RAG](https://github.com/AadiPathak23/Atlas-RAG): RAG over PDFs and code
Hybrid semantic + TF-IDF retrieval so exact identifiers aren't missed, page and line-level citations, local LLM via Ollama, ChromaDB, and incremental re-indexing.

**🧩 Smaller projects:** [🏏 Cricket Win Predictor](https://github.com/AadiPathak23/Cricket-Win-Predictor) ([live demo](https://cricketwinpredictor.streamlit.app/)) · [🩺 Health Bot](https://github.com/AadiPathak23/Health-Bot-) · [✍️ LSTM Poem Generator](https://github.com/AadiPathak23/Poem-generator)

---

## 💼 Experience

### **Graduate Researcher, [CHPS Lab](https://cphslab.com), UC Davis (Oct 2026–present)**
- Student lead on a drone **RGB + thermal computer-vision** project supporting wildlife health monitoring, advised by Prof. Zhaodan Kong
- Comparing RGB-only, thermal-only and fused models on a leak-free train/test split

### **AI/ML Intern, Persistent Systems, Santa Clara (May–Sep 2025)**
- Fine-tuned **Qwen3** for repo-aware bug detection and test generation
- Built an ANTLR-based **COBOL → documentation** pipeline
- Designed **token-prioritized chunking** pipelines for large codebases

### **AI Strategy Intern, Persistent Systems, India (May–Aug 2024)**
- Designed a **40-parameter GenAI maturity framework** for enterprise AI readiness

### **Technology Consultant, Arizona State University (Nov 2023–Nov 2024)**
- Built Python automation tools and supported AV/IT systems

---

## 🏆 Recognition & Community

- 🥇 **Winner, Startup Village Hackathon** (ASU, 2025): Best Use Case of Supermemory AI
- 🧑‍⚖️ **Mentor & Judge, Sac Hacks** (Davis, Nov 2026)
- 🛠️ **Hack the Stack at Y Combinator**, SF HQ (Feb 2026)
- 🎟️ **NVIDIA GTC 2026** attendee · 📜 **NVIDIA DLI certified:** *Adding New Knowledge to LLMs*
- 🏏 **Former President, ASU Cricket Club:** two regional titles, a national quarterfinal, and a community of 400+ members

---

## 🧠 Tech Stack

### 🖥️ Languages
<p align="center">
  <img src="https://skillicons.dev/icons?i=python,cpp,java,cs,ts,js,matlab,mysql&perline=8" />
</p>

### 🤖 AI / ML
<p align="center">
  <img src="https://skillicons.dev/icons?i=pytorch,tensorflow,sklearn&perline=3" />
</p>
<p align="center">
  <img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black"/>
  <img src="https://img.shields.io/badge/LoRA%20%2F%20PEFT-412991?style=for-the-badge&logo=openai&logoColor=white"/>
  <img src="https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white"/>
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white"/>
  <img src="https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logo=ollama&logoColor=white"/>
</p>

### 🗄️ Backend & Databases
<p align="center">
  <img src="https://skillicons.dev/icons?i=fastapi,react,postgres,mongodb,sqlite&perline=5" />
</p>

### ☁️ Cloud, DevOps & Tools
<p align="center">
  <img src="https://skillicons.dev/icons?i=docker,aws,linux,git,github,vscode,postman,vercel&perline=8" />
</p>
<p align="center">
  <img src="https://img.shields.io/badge/ANTLR-E13D3D?style=for-the-badge&logoColor=white"/>
</p>

---

## 📊 GitHub Analytics

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=AadiPathak23&show_icons=true&include_all_commits=true&theme=tokyonight&hide_border=true" width="48%"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=AadiPathak23&layout=compact&theme=tokyonight&hide_border=true&hide=Jupyter%20Notebook" width="41%"/>
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=AadiPathak23&theme=tokyonight&hide_border=true" width="60%"/>
</p>

---

<p align="center">⚡ <i>Fine-tune it, measure it honestly, ship it, on and off the cricket field.</i> 🏏</p>
