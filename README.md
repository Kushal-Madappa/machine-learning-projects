# machine-learning-projects

End-to-end ML projects. Each project is self-contained with data loading,
preprocessing, model training, evaluation, and a short write-up.

Planned projects:
- `titanic-classifier/` -- classic binary classification with feature
  engineering and model comparison
- `house-price-regressor/` -- regression with cross-validation and
  hyperparameter tuning
- `customer-churn/` -- imbalanced classification, ROC analysis
- `nlp-sentiment/` -- text classification using transformers

## Project conventions

Every project folder will follow the same layout so reviewers can scan
the repo quickly:

```
<project>/
  data/                # raw + processed (gitignored where appropriate)
  notebooks/           # exploration; one notebook = one question
  src/                 # importable code (preprocessing, model, eval)
  models/              # serialized artifacts (gitignored)
  reports/             # final write-up + figures
  README.md            # problem framing, results table, run instructions
  requirements.txt
```

**Next pickup:** `titanic-classifier` — start with EDA in `notebooks/01_eda.ipynb`,
then bake the cleaning pipeline into `src/preprocess.py` so the
notebook becomes thin. Target a small results table comparing logistic
regression, random forest, and gradient boosting on stratified CV.

---

### Log

- **2026-05-25** — Project layout above is the *contract* for every
  project in this repo. Picking `titanic-classifier` as the first
  pickup specifically because it forces all six folders to exist on
  day one — `data/`, `notebooks/`, `src/`, `models/`, `reports/`,
  `README.md` — which gives the second project a copy-paste skeleton
  rather than a blank canvas.

- **2026-05-27** -- Added a "results table" requirement to the project
  contract: every project's `reports/` folder must include a one-page
  results summary with (a) the headline metric on the test set, (b) at
  least one baseline for comparison, and (c) a brief error-mode
  paragraph (where the model fails and why). Without (c) the project
  is a leaderboard chase; with (c) it's a portfolio piece.
