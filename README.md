<div align="center">

# Hi, I'm Sambit Karmakar

### AI Engineer & Data Scientist | LLMs · RAG · Fine-Tuning · Time Series Forecasting

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" />
  <img src="https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logo=ollama&logoColor=white" />
</p>

<p>
  <a href="https://www.linkedin.com/in/sambit03"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:sambit.karmakar311003@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white" /></a>
</p>

</div>

---

## 👨‍💻 About Me

I'm an **AI Engineer and Data Scientist** with a Mathematics and Computing foundation, currently pursuing an **MS in Artificial Intelligence and Data Science at IIITM Gwalior**. I enjoy building end-to-end systems, from data engineering and model training to evaluation and deployment, and turning complex deep learning ideas into reliable, real-world solutions.

My work sits at the intersection of two worlds:

- 🤖 **Generative AI:** LLM fine-tuning, RAG pipelines, and systematic reliability evaluation.
- 📈 **Statistical modeling:** probabilistic forecasting, hypothesis testing, and rigorous model validation.

I care about one question above all: **"Can we actually trust this model's output?"** That's why my projects emphasize calibration, statistical significance tests, and honest evaluation rather than headline accuracy alone.

### 🌟 Quick Facts

- 🔭 **Currently working on:** adaptive AI tutoring systems and LLM reliability benchmarking pipelines
- 🌱 **Currently learning:** on-device / edge inference and probabilistic forecasting
- 👯 **Open to collaborating on:** open-source ML projects in semantic text analysis and volatility modeling
- 💬 **Ask me about:** Python, Llama 3.2 fine-tuning, Quantile Regression, and Retrieval-Augmented Generation
- 📍 **Based in:** Kolkata, India
- 📫 **Reach me:** [sambit.karmakar311003@gmail.com](mailto:sambit.karmakar311003@gmail.com) · [LinkedIn](https://www.linkedin.com/in/sambit03)
- 😄 **Pronouns:** He/Him

---

## 🛠️ Skills

| Area | Tools & Technologies |
|---|---|
| **Programming & Analysis** | Python, SQL, R, Java, EDA, Feature Engineering, Statistical Analysis, Hypothesis Testing, Probability & Statistics, Time Series Forecasting |
| **Machine Learning** | Scikit-learn, XGBoost, LightGBM, Statsmodels (SARIMA), Regression, Classification, Clustering, PCA, SHAP, Model Evaluation |
| **LLMs & Generative AI** | HuggingFace Transformers, SentenceTransformers, Llama 3.2, RoBERTa-MNLI, RAG, FAISS, ChromaDB, Prompt Engineering, LangChain, Groq API, Unsloth, LoRA |
| **Python Libraries** | NumPy, Pandas, Matplotlib, Seaborn, SciPy |
| **Deployment & Tools** | FastAPI, Streamlit, Ollama, MySQL, Git, GitHub, Google Colab, LaTeX |
| **Soft Skills** | Clear Communication, Data Storytelling, Simplifying Technical Concepts, Collaborative Teamwork, Adaptability |

---

## 🎓 Education

| Degree | Institution | Score | Duration |
|---|---|---|---|
| **MS in Artificial Intelligence & Data Science** | Atal Bihari Vajpayee Indian Institute of Information Technology and Management (IIITM), Gwalior | CGPA: 8.70 / 10 | Expected April 2027 |
| **B.Sc in Mathematics & Computing** | Birla Institute of Technology (BIT), Mesra | CGPA: 7.05 / 10 | 2022 – 2025 |

---

## 💼 Experience

**AI Engineer / Intern: Ryukyu GLOCAL Co., Ltd.** · *Remote, Okinawa, Japan* · May 2026 onward

Built an adaptive AI math tutor for kids, covering difficulty classification, child-friendly feedback, and personalized practice questions. Fine-tuned small language models with LoRA and Unsloth, added RAG retrieval with ChromaDB, and served everything through a FastAPI backend.

---

## 🚀 Featured Projects

### 🧮 Adaptive AI Math Tutor
**The idea:** A friendly AI tutor that figures out how hard a question is, gives kid-friendly feedback, and serves up practice problems matched to the learner's level.

**How it works:** A difficulty classifier routes questions, a fine-tuned small language model (LoRA + Unsloth + SFTTrainer) generates feedback, and ChromaDB-backed RAG grounds responses. Served through a FastAPI backend and designed for local deployment with Ollama.

**Results:** A complete, locally deployable tutoring system, evaluated with a multi-metric LLM reliability pipeline.

`Llama 3.2` `Phi-3.5 mini` `LoRA` `Unsloth` `FastAPI` `ChromaDB` `Ollama`

---

### 🔍 LLM Reliability Benchmarking Engine
**The idea:** LLMs can sound confident and still be wrong. This engine scores *how trustworthy* an answer is by checking it against real evidence retrieved from the web.

**How it works:** An async FastAPI service retrieves evidence (DuckDuckGo / Trafilatura, with Wikipedia failover) while generating 3 self-consistency samples in parallel. RoBERTa-MNLI checks for contradictions, and a learned reliability model (L2-regularized logistic regression with Platt calibration, 11 features, trained on TriviaQA) produces the final score.

**Results:**
- 📈 Test ROC-AUC improved from **0.83 → 0.94** (95% CI 0.88–0.98)
- 🎯 Well calibrated: Brier score **0.102**, ECE **0.091**
- ✅ Keeping the top 50% most confident answers lifts accuracy from **51.9% → 85.0%**
- ⚡ ~3.8s p50 latency, with explicit "unverifiable" flagging when retrieval or models fail

`FastAPI` `Ollama` `Llama 3.2` `RoBERTa-MNLI` `scikit-learn` `Groq API`

---

### 📉 Hybrid GARCH–Quantile LSTM Volatility Forecasting
**The idea:** Instead of predicting a single volatility number, forecast a *range* of likely outcomes, which is far more useful for risk decisions.

**How it works:** A GARCH(1,1)-enhanced Quantile LSTM forecasts forward 10-day realized volatility for 20 assets (equities and ETFs), blending conditional volatility with returns, rolling volatility, and volume z-scores. It outputs Q10 / Q50 / Q90 forecasts with a monotonic head (0% quantile crossing), and uses expanding-window GARCH fits and date-based splits to prevent lookahead bias.

**Results vs. baseline LSTM:**
- 📉 **23.5%** lower Mean Pinball Loss
- 📉 **24.7%** lower MAE and **23.1%** lower RMSE
- 🎯 80% prediction-interval coverage improved from **75.09% → 82.87%**
- 🧪 Diebold–Mariano test (HAC-corrected): pooled DM = 10.73, p < 10⁻¹⁵; **14 of 20** assets individually significant

`GARCH` `LSTM` `Quantile Regression` `Python`

---

### 📝 Two-Stage Automated Student Answer Grading (ASAG)
**The idea:** Grade student answers automatically: use a fast classifier for clear cases and escalate the tricky ones to an LLM.

**How it works:** Stage 1 uses all-MiniLM-L6-v2 embeddings, PCA (384 → 168 dims, 95% variance retained), and XGBoost. Stage 2 uses a local FAISS index (13,000+ vectors) for few-shot RAG context and routes ambiguous answers to Llama 3.2 (3B) via Ollama, with edge-case logic for semantic contradictions.

**Results:**
- 📚 Processed **8,700+** answers across 4 grading classes
- ⚖️ Reduced class imbalance from **16.6× → 3.5×** via targeted augmentation
- ✅ **85%** weighted accuracy in the classification stage

`XGBoost` `Llama 3.2` `FAISS` `RAG` `Sentence Transformers` `Ollama`

---

### 🦠 Multi-Country Influenza Outbreak Forecasting
**The idea:** Forecast flu cases and detect outbreak spikes across countries whose seasons behave very differently.

**How it works:** A pooled LightGBM pipeline trained on WHO FluNet/FluID data for 4 countries, using harmonic seasonal encodings. Feature design was guided by statistical tests (Kruskal-Wallis, Rayleigh), then lagged, rolling-window, and cyclical features were engineered. Validated with rolling-origin backtesting against SARIMA baselines.

**Results (statistically significant, p < 0.05):**
- 🇺🇸 Up to **71.7%** MASE reduction (USA)
- 🇬🇧 **81.4%** WAPE reduction (UK)

`LightGBM` `SARIMA` `Python` `Diebold-Mariano`



## 🤝 Let's Connect

I'm always happy to talk about LLM evaluation, forecasting, or building ML systems that hold up in the real world. Feel free to reach out!

<div align="center">

⭐ *If you find any of my projects useful, consider giving them a star!* ⭐

</div>
