## Project: Analyzing AI’s Industry Impact Through News Articles

This repository contains an NLP project that analyzes how artificial intelligence (AI) is portrayed across different industries using news articles. The goal is to understand **which sectors are most affected**, **how sentiment varies by industry**, and **what themes and narratives** are emerging around AI in the news.

The core analysis is implemented in the Jupyter notebook `NLP_final.ipynb`.

---

### 1. Research Questions

This project focuses on questions such as:

- **Industry coverage**: Which industries (e.g., finance, healthcare, education, manufacturing, tech) are most frequently mentioned in AI-related news?
- **Sentiment**: Are news articles about AI in a given industry mostly positive, negative, or neutral?
- **Themes and topics**: What topics (e.g., automation, regulation, ethics, productivity, job displacement) dominate AI coverage in each industry?
- **Temporal trends (if applicable)**: How has news sentiment and topic distribution evolved over time?

---

### 2. Data

**Data source**

- **Type**: News articles or headlines related to AI.
- **Origin**: (Fill in your actual source here, for example:)
  - A public news API (e.g., GDELT, NewsAPI, MediaCloud), OR
  - A curated dataset provided for a class project, OR
  - A custom web-scraped dataset (respecting robots.txt and terms of service).

**Typical fields (columns)**


- `title`
- `text`
- `url`
- `language`
- `date`


Data files are expected to be stored under the `data/` directory (not all raw data may be committed to this repo, depending on size and licensing).

---

### 3. Methods

At a high level, the project uses standard NLP techniques:

- **Data cleaning & preprocessing**
  - Lowercasing, punctuation and stopword removal
  - Tokenization
  - Lemmatization or stemming
  - Optional: language filtering, de-duplication of near-identical articles

- **Representation**
  - Bag-of-words / TF–IDF vectors, and/or
  - Transformer-based embeddings (e.g., BERT) for semantic representation

- **Analysis**
  - **Industry-level aggregation** of article counts and term frequencies
  - **Sentiment analysis** by industry (e.g., lexicon-based or model-based sentiment scoring)
  - **Topic modeling** (e.g., LDA, NMF, or BERTopic) to uncover coherent themes
  - **Temporal analysis** (if available) to track sentiment/topics over time
  - **Visualization** of:
    - Industry coverage
    - Sentiment distributions
    - Topic–industry relationships
    - Time series of sentiment or topic prevalence

The full, detailed pipeline is implemented in `NLP_final.ipynb`.


### 4. Setup & Installation

#### 4.1. Prerequisites

- **Python**: 3.9+ recommended
- **Package manager**: `pip` (or `conda` if you prefer)
- **Jupyter** or **JupyterLab** for running the notebook

#### 4.2. Clone the repository

git clone https://github.com/<your-username>/ai-industry-impact-news.git
cd ai-industry-impact-news#### 5.3. Create and activate a virtual environment (recommended)

Using `venv`:

python3 -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate#### 5.4. Install dependencies

pip install -r requirements.txt---

### 5. Running the Analysis

1. **Prepare data**

   - Place the raw data files (e.g., CSV/JSON) into the `data/` directory.
   - If your notebook expects specific filenames or paths, ensure they are present (update the notebook if needed).

2. **Launch Jupyter**

   From the repository root:

  
   jupyter notebook
      Then open:

   - `notebooks/NLP_final.ipynb`

3. **Run the notebook**

   - Execute all cells in order (Kernel → Restart & Run All).
   - The notebook will:
     - Load and preprocess the data
     - Conduct sentiment and/or topic analysis
     - Generate plots and tables
