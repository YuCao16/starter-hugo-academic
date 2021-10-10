---
title: Credit Card Default detection. 
summary: Build a model to predict whether a customer will default on their loan.

tags:
- Deep Learning
- Classification Task
date: "2020-03-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart
  preview_only: yes

links:
- icon: twitter
  icon_pack: fab
  name: Follow
  url: "https://twitter.com/YuCao33603223"
url_code: ""
url_pdf: "https://drive.google.com/file/d/1MXCwuaOiM2z3TPOd5SOQlOcr8ukUshQi/view?usp=sharing"
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: 
---
## Task
The task is to build a model to predict whether a customer will default on a loan. Use reasonable methods to deal with missing values in the data. Note that imbalances in the data can have a fatal negative impact on the classification algorithm.

## Conclusion
In this report I use two weighted algorithms, weighted logistic regression and weighted random forest, to predict defaults, and the results show that the weighted algorithm achieves signiﬁcant improvements in both accuracy and recall rate over the standard algorithm. There is no signiﬁcant diﬀerence in the values of optimal accuracy and optimal recall between the two weighted algorithms, but weighted regression yielded higher recall rate and AUC in both cases.
