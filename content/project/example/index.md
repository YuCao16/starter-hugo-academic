---
title: Chest X-Ray Pneumonia Classification Using ResNet.
summary: The use of ResNet enabled the model to achieve 95% accuracy in classifying the type of pneumonia based on chest x-ray.

tags:
- Deep Learning
- Classification Task
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
url_code: "https://drive.google.com/file/d/1QrGzxwE00JCMH3aB6Sk5GavnCmc7mJU3/view?usp=sharing"
url_pdf: ""
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
In this project, my task was to identify the type of pneumonia based on x-ray photographs, where the labels included normal, common pneumonia and Covid-19. And to make the accuracy rate as high as possible.

## Methodology

* **Data normalization**: We normalized the image tensors by subtracting the mean and dividing by the standard deviation of pixels across each channel. Normalizing the data prevents the pixel values from any one channel from disproportionately affecting the losses and gradients.

* **Data augmentation**: We applied a random transform when loading the images from the training dataset. Specifically, we crop the photos so that they are transformed into square, 24×24 pixel size photos.

* **Residual connections**: We added the original input back to the output feature map obtained by passing the input through one or more convolutional layers. (We used the ResNet9 architecture.)

* **Batch normalization**: After each convolutional layer, we added a batch normalization layer, which normalizes the outputs of the previous layer. This is somewhat similar to data normalization, except it's applied to the outputs of a layer, and the mean and standard deviation are learned parameters.

* **Learning rate scheduling**: Instead of using a fixed learning rate, we will use a learning rate scheduler, which will change the learning rate after every batch of training. There are many strategies for varying the learning rate during training, and we used the "One Cycle Learning Rate Policy".

* **Weight Decay**:We added weight decay to the optimizer, yet another regularization technique which prevents the weights from becoming too large by adding an additional term to the loss function.

* **Gradient clipping**: We also added gradient clippint, which helps limit the values of gradients to a small range to prevent undesirable changes in model parameters due to large gradient values during training.

* **Adam optimizer**: Instead of SGD (stochastic gradient descent), we used the Adam optimizer which uses techniques like momentum and adaptive learning rates for faster training. There are many other optimizers to choose froma and experiment with.

## Results and Discussion
After ten minutes of training, the accuracy finally stabilised at around 95%, while no over-fitting occurred. The effect of the dynamic learning rate and the structure of ResNet is remarkable.

**If interested in the details of the report, please click on the Code block at the top of the page.**
