# 📊 Machine Learning Analysis of PRISM Drug Sensitivity and Gene Features

This repository presents an exploratory and predictive analysis using publicly available PRISM drug repurposing screen data from the Broad Institute's DepMap project (release 24Q2). Our goal was to identify molecular features (gene expression and gene essentiality) that associate with cancer drug response, with a particular focus on **Lazertinib**, a targeted EGFR inhibitor.
---

🧑‍🏫 **Teaching use welcome!**  
This pipeline is clean, modular, and reproducible — perfect for coursework in bioinformatics or computational biology.

Try swapping in another PRISM drug and see what features emerge!

---

## 📁 Repository Structure

Each subfolder corresponds to a full machine learning pipeline exploring either **expression-based** or **CRISPR-based** features. Each includes:

- **`feature_importance.png`** – Top predictive features (genes).
- **`roc_curve.png`** – Model performance for classifying sensitivity vs resistance.
- **`boxplot_1.png`, `boxplot_2.png`** – Gene expression or dependency stratified by drug response.
- **A Jupyter Notebook** with full preprocessing, modeling, and visualization steps.

---

## 🔬 Biological Motivation

Lazertinib was selected due to:
- Clear **sensitivity/resistance spread** across many cell lines.
- Strong clinical relevance as a **targeted cancer therapy**.
- Opportunity to evaluate both **gene expression** and **gene knockout (CRISPR)** as predictive features.

Drug selection was based on name patterns such as `-tinib`, `-mab`, etc., to identify potential cancer therapeutics rapidly from the PRISM dataset.

---

## 📂 Folders and Notebooks

### `Expression_RF_Pipeline/`
- Uses **gene expression (TPM)** features.
- Random Forest model trained to classify cell lines as sensitive or resistant to Lazertinib.
- Key output: Feature importance plot and expression boxplots for top hits (e.g., **TNK1**, **PDZRN3**).

### `CRISPR_RF_Pipeline/`
- Uses **CRISPR knockout dependency scores** from Achilles data.
- Same ML pipeline used, with ROC and top gene boxplots.
- Highlights genes whose **loss confers resistance or sensitivity**.

---

## 🧪 Data Sources

- **PRISM Drug Repurposing Data**: Drug response scores across 1,514 compounds and 859 cell lines.
- **Expression (TPM) and CRISPR dependency** data from DepMap portal.
- **Oncotree lineage annotations** used for cancer type grouping.

---

## 📈 Visualizations

Included figures:
- `Heat_Map_PRISM_Related_Cancer_Drugs.png`: Drug response scores across cancer types.
- `Cell_Line_Oncotree_Lineage_Count.png`: Number of cell lines per lineage.
- Lazertinib histogram: Distribution of sensitivity scores used for binarization.

---

## 🛠️ Requirements

You can recreate the pipelines by running the notebooks:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## 🚀 Getting Started

To run the analysis:
1. Clone this repo.
2. Open the notebook in `Expression_RF_Pipeline/` or `CRISPR_RF_Pipeline/`.
3. Execute cells step-by-step to replicate model training and visualizations.

---

## 🧠 Insights and Extensions

- **Gene hits** such as TNK1 (expression) and others show strong associations with Lazertinib response.
- This framework can be **extended to any drug** in PRISM using the same logic.
- Future work: test feature importance across pan-drug or lineage-specific contexts.

---

## 📬 Contact

For questions, suggestions, or collaboration inquiries, please contact Joe (mjt6ss@virginia.edu)

---

## 📜 License

This repository is licensed under the MIT License — see the [`LICENSE`](./LICENSE) file for details.

You are free to use, modify, and adapt this codebase for teaching, research, and commercial purposes. We welcome forks, contributions, and adaptations. If used in an academic or training setting, citation or acknowledgment is appreciated but not required.

Note: This repository is **educational and exploratory** in nature. All code is provided "as-is" without warranty or fitness for a particular use.

