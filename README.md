# Venture Intelligence Platform

A machine learning and LLM-powered platform for venture evaluation, funding prediction, explainability, similarity search, and automated investor/founder report generation.

## Project Structure

```
venture-intelligence-platform/
│
├── README.md                      # roadmap tracker + how to run
├── requirements.txt                # all deps, phase-tagged
│
├── data/
│   ├── raw/                        # ks-projects-201801.csv goes here
│   └── processed/                  # cleaned / feature-engineered data
│
├── notebooks/                      # exploratory .ipynb work
│
├── src/
│   ├── eda/                        # Phase 1: exploration, visual EDA
│   │   └── day1_explore.py
│   ├── features/                   # Phase 1: feature engineering
│   ├── models/                     # Phase 2 + 4: baseline, boosting, fusion NN
│   ├── explainability/             # Phase 3: SHAP, counterfactuals
│   ├── embeddings/                 # Phase 4: sentence-transformer text encoding
│   ├── retrieval/                  # Phase 5: FAISS vector store, similarity search
│   ├── agents/                     # Phase 6: pattern mining, recommendations, objection sim
│   └── reports/                    # Phase 7: LLM founder/investor report generation
│
├── api/                            # Phase 8: FastAPI backend
├── frontend/                       # Phase 8: Streamlit/React frontend
├── models/                         # saved trained model artifacts (.pkl, .json)
├── reports/
│   └── figures/                    # saved plots/charts from EDA & evaluation
├── tests/                          # unit tests for pipeline components
└── docs/                           # write-ups, technical report, presentation notes
```

## Getting Started

1. Set up a virtual environment and install dependencies:
   ```bash
   python -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```
2. Place the dataset `ks-projects-201801.csv` in `data/raw/`.