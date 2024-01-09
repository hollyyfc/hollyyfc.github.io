---
title: "Machine Learning in Healthcare: Lab Test Harmonization"
image: 
  path: /images/banner1.jpg
  thumbnail: /images/HDS.png
  caption: "Photo from [Vecteezy.com](https://www.vecteezy.com/)"
---

As public health increasingly moves toward automated capture, lab data are becoming an invaluable asset for public health agencies. However, a major challenge emerges when the code sets for lab test names appear differently from one information system to another, and the raw data inputs from different labs are of poor quality. Building on top of the issue, we bring up our core question:

**Given two lab test inputs (raw names), can we harmonize the same type (grouper)?** For example, a raw name *ACT PARTIAL THROMBOPLASTIN TIME (BKR)* belongs to a grouper type of *aptt*.

### What is Harmonization?

Harmonization is essentially a process of NLP deduplication. In this project, we attempt to: 
- Match messy lab test data of poor quality
- Identify the same test type based on texts provided by the structured dataset
- Validate the process of cross-connection between different datasets or test representations

## Part I: Text-Space Matching

✨ Find details [HERE](https://docs.google.com/presentation/d/1tCqjBRsl3fW9TjSYCGKtXaSswkXwlyfSaqDJqcTCKN4/edit?usp=sharing)

- Generate test names embeddings with [Bio-BERT](https://doi.org/10.1093/bioinformatics/btz682), a BERT architecture pretrained on biomedical corpora.
- Compare cosine similarity between raw names and groupers embeddings within identified ground-truth data and match each unique raw name with the grouper representing the highest similarity in cross-comparison.
- Evaluations and diagnosis on the model performance show that our current Bio-BERT structure performs well on linking specific groupers label (such as *bilirubin*, *fibrinogen*, and *hematocrit*) to raw names with high AUC scores and clear similarity threshold to separate the grouper vs. non-grouper.

## Part II: Text-Numeric Concatenated Matching

✨ Find details [HERE](https://github.com/hollyyfc/Duke-AI-Health-Data-Science-2022.git)

- Incorporate numeric test result for each unique raw names in the lab database for accuracy, calculate a 7-dimension statistics (minimum, 25 th percentile, median, 75 th percentile, maximum, mean, and standard deviation) based on observations within each raw name and grouper label for numeric embeddings, and repeat the cross-comparison and AUC evaluation process. The legitimacy of numeric embeddings has been pre-evaluated by two-component PCA.
- Concatenate both numeric and text embeddings to evaluate the full performance of the model.

![poster](/images/HDSposter.png)

## Results

Based on numeric-only embeddings, we show that the ability for linking raw names to correct labels is effective for some groupers but limited to relatively low predictive performance for others.

With the addition of text embeddings from Bio-BERT, the full model yields high-performing ability in identification and linkage, capturing both the distribution characteristics of numeric test results and the semantic meaning of the biomedical text labels. This indicates a promising results on the integrative method to include more essential information while avoiding overfitting on the current dataset.















