---
title: Application of Generative Adversarial Networks on Unbalanced Datasets
summary: Questioning existing methods and exploring new applications, the right way to apply GANs on unbalanced datasets?

tags:
- Deep Learning
- Classification Task
- Generative Adversarial Networks
date: "2010-04-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart
  preview_only: no

links:
- icon: twitter
  icon_pack: fab
  name: Follow
  url: "https://twitter.com/YuCao33603223"
url_code: ""
url_pdf: "https://drive.google.com/file/d/1MvPx1QakcknmxZnMtEoc4a-PCoyJyod5/view?usp=sharing"
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: 
---
## Research Question and Aim
The plausibility of existing GAN-based (Generative Adversarial Network) oversampling models is questioned through a model remodelling and literature review approach, while the application of GANs to unbalanced datasets is explored, and information security issues when using GANs are considered.

## Abstract
Class imbalance is a common problem in data that impedes the predictive performance of classification algorithms. In the task of loan default prediction, the impact of the imbalance on classifiers can often be economically costly. Oversampling methods are commonly used to deal with unbalanced datasets, and a large number of linear interpolation and KNN-based oversampling methods such as SMOTE, ADASYN and their variants are constantly proposed by scholars. However, they have an inherent disadvantage in dealing with high-dimensional and complex datasets. Deep learning networks can model complex data well, and models based on generative adversarial networks(GANs) have made relatively significant progress in generating tabular data  (e.g., database tables). Research at this stage has generally focused on the use of GAN for generating tabular data as novel oversampling tools, however this often requires complex structures and extensive hyper-parameter tuning. As an exploration of the application of GAN to unbalanced datasets, this paper proposes a framework that combines GANs with traditional oversampling methods. We compare our framework with five resampling methods and the results demonstrate that it can lead to better stability of the classifier in the presence of insufficient data.

## Conclusion
We proposed a framework for handling imbalanced datasets based on CTGAN and SMOTE, CTGANS, and compared it with three oversampling methods, an undersampling method and a balanced dataset. We evaluated the P2P lending dataset with two classification algorithms, using three metrics of classification performance. We first evaluated the performance of the CTGAN model for generating tabular data and the validity of the CTGAN-based oversampling approach. The results showed that CTGAN successfully generated a complex dataset containing both numerical and categorical variables, with the distribution of most of the variables largely consistent with the original data, but mode collapse persisted in some variables. This resulted in the performance of the CTGAN-based oversampling method being significantly inferior compared to traditional oversampling methods.

While our method performs largely in line with traditional oversampling methods when the amount of data is sufficient, it has a significant performance advantage when the amount of data is insufficient, using only 10% of the samples to bring the performance of the classification algorithm close to that of other oversampling methods.

However, when comparing the performance of RLR and MLP, we found that the MLP trained on the datasets balanced by oversampling method performed significantly worse than the RLR model on the test set. Our conjecture is that the complexity of the model shifts the focus of learning from the features in the default data to the structure of the data, i.e. the MLP tends to recognise synthetic data in the dataset. Future research could test our conjecture by setting up two test sets, one with real data and one with synthetic data, and by observing the performance of the MLP on both sets.

**If interested in the details of the report, please click on the PDF block at the top of the page.**
