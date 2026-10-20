<p align="center">
  <img src="assets/hero.svg" alt="Hardik Choudhary, AI and data systems engineer. An isometric neural core of three floating layers and a glowing cube, orbited by data bodies and connected to ingest, model, retrieve and act nodes." width="100%" />
</p>

<p align="center">
  <a href="assets/Hardik_CV.pdf"><img src="assets/buttons/download-cv.svg" alt="Download AI and Engineering CV (PDF)" width="270" /></a>
  <a href="assets/Hardik_CV_DA.pdf"><img src="assets/buttons/data-analytics-cv.svg" alt="Download Data Analytics CV (PDF)" width="270" /></a>
  <!-- Portfolio button: replace PORTFOLIO_URL with your portfolio address, then remove the comment markers around this line.
  <a href="PORTFOLIO_URL"><img src="assets/buttons/portfolio.svg" alt="View portfolio" width="270" /></a>
  -->
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/hardik8/"><img src="assets/connect/linkedin.svg" alt="LinkedIn" width="84" /></a>
  <a href="mailto:hardikkumar2583@gmail.com"><img src="assets/connect/gmail.svg" alt="Email" width="84" /></a>
  <a href="https://github.com/Har-dik25?tab=repositories"><img src="assets/connect/github.svg" alt="GitHub repositories" width="84" /></a>
  <a href="https://www.kaggle.com/choudhary25"><img src="assets/connect/kaggle.svg" alt="Kaggle" width="84" /></a>
  <a href="https://leetcode.com/u/Choudhary_25/"><img src="assets/connect/leetcode.svg" alt="LeetCode" width="84" /></a>
  <a href="https://www.hackerrank.com/profile/hardikkumar2583"><img src="assets/connect/hackerrank.svg" alt="HackerRank" width="84" /></a>
</p>

<p align="center">
  <a href="#how-the-systems-fit-together">Architecture</a> ·
  <a href="#featured-systems">Featured systems</a> ·
  <a href="#more-projects">More projects</a> ·
  <a href="#toolkit">Toolkit</a> ·
  <a href="#experience">Experience</a> ·
  <a href="#credentials">Credentials</a>
</p>

<p align="center"><img src="assets/divider.svg" alt="" width="100%" /></p>

## About

I'm a Computer Science and Engineering student at **Lovely Professional University**, focused on **applied AI, data engineering, and analytics**. I build end-to-end projects that turn raw data into useful tools—from ingestion and analysis to retrieval or machine learning, APIs, and user interfaces. My work includes healthcare access analytics, legal document retrieval, market-news analysis, and explainable NLP. I work mainly with Python and SQL, alongside FastAPI, PyTorch, scikit-learn, React, and Streamlit.

<p align="center">
  <img src="assets/lanes.svg" alt="Four lanes of work. Data engineering: ingestion and cleaning pipelines, SQLite and Parquet stores, make-driven rebuilds and pytest-backed validation. Data science: analytics, composite indices, lead-lag correlation, SHAP-explained models, geospatial analysis and what-if simulation. Applied AI: hybrid retrieval, cross-encoder reranking, vector search and transformer text classification with token-level explanations. Agentic systems: policy-gated tool chains with retries, human escalation and audit logs, behind FastAPI back ends and React, Next.js or Streamlit front ends." width="100%" />
</p>

## How the systems fit together

<p align="center">
  <img src="assets/engineering-map.svg" alt="A vertical stack of four isometric layers with data flowing down through them. Ingest and shape: RSS, SEC EDGAR, FNSPID and NSE feeds; a SQLite warehouse of 640 districts and 673,638 villages; Parquet feature tables. Model: MiniLM embeddings in Qdrant and ChromaDB; Random Forest and Gradient Boosting with SHAP; a BERT and BiLSTM-attention hybrid. Reason: BM25 and dense search with reciprocal rank fusion; cross-encoder reranking over 3,840+ legal chunks; a nine-tool policy chain with human escalation. Deliver: FastAPI services behind React and Next.js consoles; Streamlit dashboards with GIS maps; an audit log of every decision. Tests, Docker, CI and structured logging run across every stage." width="100%" />
</p>

## Featured systems

Six projects that show how I work across data, applied AI, analytics, and software.

### [Rural Healthcare Access Gap Mapper](https://github.com/Har-dik25/Rural-Healthcare-Access-Gap)

<p align="center"><img src="assets/projects/rural-healthcare.svg" alt="Isometric district map of columns coloured by access gap severity with pulsing hotspots, fed by a SQLite warehouse. Stack: Python, pandas, NumPy, SQLite, Streamlit, Plotly, GIS maps, pytest." width="100%" /></p>

- Combines MoHFW, Census, NFHS-5, and travel-time data for **640 districts and 673,638 villages** in a SQLite analytical warehouse.
- Adds a composite Access Gap Index and a 12-module Streamlit dashboard with GIS maps, district drill-downs, and resource-allocation what-if analysis.
- **Status:** Decision-support prototype using public data; runs locally with documented tests.

### [Samvidhan AI (LegalMind)](https://github.com/Har-dik25/Samvidhan_AI)

<p align="center"><img src="assets/projects/samvidhan-ai.svg" alt="A stack of legal documents feeds a retrieval ring that returns a result card with highlighted statute lines. Stack: Python, FastAPI, React, Vite, ChromaDB, BM25, SQLite, DVC." width="100%" /></p>

- Implements hybrid retrieval over **3,840+ legal chunks**, combining ChromaDB dense search, BM25, reciprocal-rank fusion, and cross-encoder reranking.
- Returns extractive statutory passages and IPC/CrPC-to-BNS/BNSS mappings through a React and FastAPI workspace with streamed responses.
- **Status:** Full-stack legal research prototype; not legal advice.

<p align="center"><img src="assets/retrieval-pipeline.svg" alt="Samvidhan AI retrieval pipeline from top to bottom: a legal question is preprocessed, then searched in parallel by dense ChromaDB retrieval and BM25 sparse retrieval over indexes built offline from 3,840+ chunks. Results are merged with reciprocal rank fusion and a section boost, reranked by a cross-encoder, and assembled by an extractive synthesizer into five outputs: overview, sub-clause breakdown, penal liability, IPC and CrPC to BNS and BNSS mapping, and precedents, streamed to a React workspace." width="100%" /></p>

### [Algorithmic Market Sentiment and News Vector Correlation Platform](https://github.com/Har-dik25/Algorithmic-Market-Sentiment-News-Vector-Correlation-Platform)

<p align="center"><img src="assets/projects/market-sentiment.svg" alt="Floating news vectors stream into an isometric chart where a sentiment ribbon leads a price ribbon. Stack: Python, FastAPI, Next.js, Qdrant, scikit-learn, SciPy, Docker, GitHub Actions." width="100%" /></p>

- Ingests financial news, SEC filings, FNSPID data, and NSE feeds; cleans and indexes text in Qdrant for semantic search.
- Tests news-sentiment signals against returns with lead-lag correlation and p-values, with a HistGradientBoosting model for comparison.
- **Status:** End-to-end exploratory research pipeline; not a trading system.

### [TransitAI: Public Transport Delay Analyzer](https://github.com/Har-dik25/Public-Transport-Delays-with-Weather-Events)

<p align="center"><img src="assets/projects/transitai.svg" alt="A bus drives along an isometric road through rain and a delay zone, beside bars showing which factors drive a delay. Stack: Python, pandas, scikit-learn, SHAP, Parquet, Streamlit, Plotly, Docker." width="100%" /></p>

- Uses a `make`-driven pipeline to join **simulated NYC MTA bus trips** with historical weather and city events, then trains delay models with SHAP explanations.
- **Status:** Local analytics prototype; simulated trip records demonstrate the approach, not real MTA performance.

### [ShopWave: Autonomous Support Resolution Agent](https://github.com/Har-dik25/ShopWave_Autonomous_Support_Resolution_Agent)

<p align="center"><img src="assets/projects/shopwave.svg" alt="Tickets ride a conveyor through a glowing policy gate and split into resolved, awaiting-information and escalated lanes. Stack: Python standard library, JSON stores, thread pool, retries, audit log." width="100%" /></p>

- A deterministic Python agent classifies support tickets and routes them through policy-gated tools, with refund checks, retries, human escalation, and audit logging.
- **Status:** Standard-library prototype tested on synthetic tickets; no LLM calls.

<p align="center"><img src="assets/agent-loop.svg" alt="ShopWave agent loop: support tickets are classified, then routed through policy-gated tools with retries, human escalation, and audit logging." width="100%" /></p>

### [TruthLens AI: Fake News Detection](https://github.com/Har-dik25/Fake-News-Detection-System)

<p align="center"><img src="assets/projects/truthlens.svg" alt="A text document with attention highlights passes through BERT and BiLSTM blocks into a swinging real-versus-fake gauge. Stack: Python, PyTorch, Hugging Face, scikit-learn, FastAPI, Docker, Pydantic, NLTK." width="100%" /></p>

- Trains BERT and BiLSTM-attention models on **72,134 WELFake articles**, with NLP features and word-level attention visualizations.
- Serves predictions through FastAPI and an explainability-focused browser interface.
- **Status:** Training and serving pipeline with model-comparison and error-analysis tooling.

## More projects

| Project | What it is | Stack | Status |
|---|---|---|---|
| [CampusFlow: University Management System](https://github.com/Har-dik25/UMS-replica) | FastAPI and React application covering student and faculty records, academics, attendance, exams, fees and library operations. | <img src="assets/icons/fastapi.svg" width="22" height="22" alt="FastAPI" title="FastAPI" /> <img src="assets/icons/react.svg" width="22" height="22" alt="React" title="React" /> <img src="assets/icons/vite.svg" width="22" height="22" alt="Vite" title="Vite" /> | Full-stack application |
| [EcoEats: Food Waste Website](https://github.com/Har-dik25/Food-Wastage-website) | Responsive front end for coordinating surplus-food donations. | <img src="assets/icons/html5.svg" width="22" height="22" alt="HTML5" title="HTML5" /> <img src="assets/icons/css3.svg" width="22" height="22" alt="CSS3" title="CSS3" /> <img src="assets/icons/javascript.svg" width="22" height="22" alt="JavaScript" title="JavaScript" /> | Front-end concept |
| [Perfect Present: Gift Recommendation Website](https://github.com/Har-dik25/Personalized-Gift-recommendation-) | Front end for exploring gift ideas by recipient and occasion. | <img src="assets/icons/html5.svg" width="22" height="22" alt="HTML5" title="HTML5" /> <img src="assets/icons/css3.svg" width="22" height="22" alt="CSS3" title="CSS3" /> <img src="assets/icons/javascript.svg" width="22" height="22" alt="JavaScript" title="JavaScript" /> | Front end |
| [HitCast: Spotify Popularity Predictor](https://github.com/Har-dik25/HitCast-Spotify-Track-Popularity-Predictor) | Machine-learning project to estimate track popularity from audio features. | Not yet documented | In progress |
| [AI-Powered Traffic Congestion Analysis](https://github.com/Har-dik25/AI-Traffic-Congestion-Analysis) | Team project exploring historical traffic data, congestion prediction, and local dashboard visualizations. | Python, pandas, scikit-learn, Flask | Analytics project |
| [OCR Studio: Offline Image-to-JSON](https://github.com/Har-dik25/OCR-Studio-Offline-Image-to-JSON-Web-App) | Offline-first Flask utility that extracts image text and exports structured JSON. | Python, Flask, OpenCV, Tesseract | Local web utility |
| Nexus HR Core ([frontend](https://github.com/Har-dik25/hrms-frontend), [backend](https://github.com/Har-dik25/hrms-backend)) | Role-based employee, attendance, and leave management application. | FastAPI, PostgreSQL, React | Full-stack application |

## Toolkit

<p>Core areas: Python and SQL; data analysis and visualization; machine learning and NLP; retrieval and vector search; APIs and web applications; Docker, CI, and testing.</p>

<p align="center">
  <img src="assets/toolkit.svg" alt="Technical toolkit covering generative AI, agentic systems, RAG and vector search, machine learning, data engineering, Python and SQL, APIs and databases, visualization and geospatial interfaces, and cloud, testing, and DevOps." width="100%" />
</p>

## Experience

<p align="center">
  <img src="assets/timeline.svg" alt="Experience timeline. June to August 2025: Data Intern at Futurense Technologies, building models to forecast lead volume and conversion rates and cleaning marketing data for funnel and cohort analysis. June to July 2026: Applied AI and Intelligent Systems Intern at Futurense Technologies, prototyping AI pipelines across data ingestion, preprocessing, inference and API serving with prompt design and embeddings." width="100%" />
</p>

**Applied AI & Intelligent Systems Intern — Futurense Technologies (Jun–Jul 2026):** Prototyped AI/ML pipelines spanning data ingestion, preprocessing, inference, and API serving, using prompt engineering and embeddings.

**Data Intern — Futurense Technologies (Jun–Aug 2025):** Built lead-volume and conversion forecasts, cleaned marketing data, and created Power BI funnel and cohort dashboards that identified **15% critical inefficiencies** in CPL-focused optimization.

<p align="center">
  <a href="https://www.linkedin.com/posts/hardik8_internship-activity-7429402370805047296-5OnB">Data internship post</a> ·
  <a href="https://lnkd.in/p/dCbWkd-U">Applied AI internship certificate</a>
</p>

## Credentials

| Credential | Issuer | Link |
|---|---|---|
| Oracle Cloud Infrastructure 2025 Certified Generative AI Professional | Oracle University | [LinkedIn post](https://www.linkedin.com/posts/hardik8_generative-ai-professional-activity-7388917134468431872-ipzL) |
| Oracle Cloud Infrastructure 2025 Certified Data Science Professional | Oracle University | [LinkedIn post](https://www.linkedin.com/posts/hardik8_data-science-professional-activity-7389534104666476544-doIF) |
| SQL (Advanced) | <img src="assets/icons/hackerrank.svg" width="18" height="18" alt="" /> HackerRank | [Profile](https://www.hackerrank.com/profile/hardikkumar2583) |
| CSS (Basic) | <img src="assets/icons/hackerrank.svg" width="18" height="18" alt="" /> HackerRank | [Profile](https://www.hackerrank.com/profile/hardikkumar2583) |
| Build Generative AI Apps and Solutions with No-Code Tools | <img src="assets/icons/udemy.svg" width="18" height="18" alt="" /> Udemy | Course completion |

Also: 5-star HackerRank rating in Python and SQL (Oct 2025), and participant in the Google Gen AI Exchange Hackathon and Smart India Hackathon (2025).

<p align="center"><img src="assets/divider.svg" alt="" width="100%" /></p>
