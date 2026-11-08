# ITAI 1371 · Lab 10: Unsupervised Learning

**Author:** Joseph Clay · **Group:** JosephClay (individual)
**Submitted:** November 7, 2026

Two unsupervised learning techniques from scikit-learn:

- **K-Means clustering** on 300 synthetic customer points (`make_blobs`)
- **Principal Component Analysis (PCA)** on the 4-feature Iris dataset

## Deliverables

| File | Description |
|---|---|
| [`L10_JosephClay_Notebook.ipynb`](L10_JosephClay_Notebook.ipynb) | Completed notebook with all outputs |
| [`L10_JosephClay_Notebook.pdf`](L10_JosephClay_Notebook.pdf) | PDF of the completed notebook |
| [`L10_JosephClay_Reflection.pdf`](L10_JosephClay_Reflection.pdf) | Reflection journal |
| [`L10_JosephClay_Contribution.pdf`](L10_JosephClay_Contribution.pdf) | Contribution journal |

## Results

| Task | What was done | Result |
|---|---|---|
| 1. Elbow Method | KMeans for k = 1 to 10, plotted inertia | Clear elbow at **k = 4** |
| 2. K-Means | KMeans with k = 4, clusters plotted with centers | Four clean clusters, matching the raw data |
| 3. PCA | Iris reduced from 4 features to 2 components | PC1 92.46%, PC2 5.31%, **97.77% total** |

In the PCA plot, setosa separates cleanly from the other two species. Versicolor and virginica partly overlap.

## Notes

- **Line breaks:** The downloaded notebook had no line breaks in any cell, which caused a SyntaxError. I worked from a copy with only the line breaks restored.
- **Seaborn import:** The Task 3 plot uses `sns`, but the notebook never imports seaborn. I added `import seaborn as sns`.
- **Scaling:** The data is unscaled, following the notebook hints. The two blob features cover similar ranges.
- **"Over 95%" claim:** Knowledge Check question 3 says two components explain over 95% of the variance. My run confirms it: 97.77%.

## How to run

```bash
python3 -m venv .venv
.venv/bin/pip install scikit-learn numpy pandas matplotlib seaborn jupyter
.venv/bin/jupyter notebook L10_JosephClay_Notebook.ipynb
```

Tested with scikit-learn 1.9.1, numpy 2.5.4, pandas 3.1.1, matplotlib 3.11.2, seaborn 0.13.2. The notebook also runs in Google Colab.

## AI assistance

I used Claude Code (an AI assistant) to set up the environment, explain errors, check outputs, format my written answers, and export the PDFs. I wrote the notebook code and the answers myself.
