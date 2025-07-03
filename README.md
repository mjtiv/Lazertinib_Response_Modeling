# Lazertinib_Response_Modeling
Integrated bioinformatics pipeline to predict Lazertinib drug response using CRISPR knockout and gene expression data. Includes data preprocessing, variance filtering, Random Forest modeling, hyperparameter optimization, and biological interpretation of top predictive features.






✅ Variance Cutoff Strategy: Data-Driven, Not One-Size-Fits-All

    For CRISPR gene effect data, variance cutoff = 0.02
    ▫️ Low baseline variance due to dependency scores clustering around 0
    ▫️ ✅ 0.02 retained informative genes, filtering out uninformative noise

    For expression (TPM log+1) data, variance cutoff = 2.0
    ▫️ Much broader dynamic range
    ▫️ ✅ 2.0 marked the start of the long tail — genes with biologically meaningful variation

    🧠 Key Insight: Cutoff thresholds were selected based on data-specific variance distributions, not arbitrary values.



