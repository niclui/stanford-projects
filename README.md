# Stanford MS Statistics Projects

This repo holds the projects I worked on during my M.S. in Statistics at Stanford.

## METER-ML: A Multi-sensor Earth Observation Benchmark for Automated Methane Source Mapping

**Co-first author, presented at IJCAI-ECAI 2022 Workshop on Complex Data Challenges in Earth Observations**

[Website](https://stanfordmlgroup.github.io/projects/meter-ml/) | [Report](https://arxiv.org/abs/2207.11166) | [Presentation](https://www.youtube.com/watch?v=WGVy_viLhgU)

Reducing methane emissions is essential for mitigating global warming. To attribute methane emissions to their sources, a comprehensive dataset of methane source infrastructure is necessary. Recent advancements with deep learning on remotely sensed imagery have the potential to identify the locations and characteristics of methane sources, but there is a substantial lack of publicly available data to enable machine learning researchers and practitioners to build automated mapping approaches. To help fill this gap, we construct a multi-sensor dataset called METER-ML containing 86,599 georeferenced NAIP, Sentinel-1, and Sentinel-2 images in the U.S. labeled for the presence or absence of methane source facilities including concentrated animal feeding operations, coal mines, landfills, natural gas processing plants, oil refineries and petroleum terminals, and wastewater treatment plants. We experiment with a variety of models that leverage different spatial resolutions, spatial footprints, image products, and spectral bands. We find that our best model achieves an area under the precision recall curve of 0.915 for identifying concentrated animal feeding operations and 0.821 for oil refineries and petroleum terminals on an expert-labeled test set, suggesting the potential for large-scale mapping. We make METER-ML freely available at this https URL to support future work on automated methane source mapping.


## Generating Robustness: Exploring Various Ways to Adapt Question Answering to New Domains

**Best Poster Award (top 3% of 500 students)**

[Report](/NLP/NLP_Report.pdf) | [Poster](/NLP/NLP_Poster.pdf)

Code: https://github.com/qqlabs/cs224n-project

Class: [CS 224N](https://web.stanford.edu/class/cs224n/) - Natural Language Processing

Question Answering (QA), or the task of asking a model to answer a question correctly given a passage, is one of the most promising areas in NLP. However, state-of-the-art QA models tend to overfit to training data and do not generalize well to new domains, requiring additional training on domain-specific datasets to adapt. In this project, we aim to design a QA system that is robust to domain shifts and can perform well on out-of-domain (OOD) fewshot data.

We implement a variety of techniques that boost the robustness of a QA model trained with domain adversarial learning and evaluated on out-of-domain data, yielding a 16% increase in F1 score in development and 10% increase in test. We find that the following innovations boost model performance: 1) finetuning the model on augmented out-of-domain augmented data, 2) aggregating Wikipedia type datasets during adversarial training to simplify the domain discriminator’s task, and 3) supplementing the training data with synthetic QA pairs generated with roundtrip consistency. We also ensemble the best-performing models on each dataset and find that ensembling yields further performance increases.


## Synthetic Data for Semantic Image Segmentation of Imagery of Unmanned Spacecraft

**Published at 2023 IEEE Aerospace Conference**

[Paper](https://arxiv.org/abs/2211.11941)

Code: https://github.com/madwsa/mms-imageseg

Class: [CS 230](https://cs230.stanford.edu/) - Deep Learning

Images of spacecraft photographed from other spacecraft operating in outer space are difficult to come by, especially
at a scale typically required for deep learning tasks. Semantic
image segmentation, object detection and localization, and pose
estimation are well researched areas with powerful results for
many applications, and would be very useful in autonomous
spacecraft operation and rendezvous. However, recent studies
show that these strong results in broad and common domains
may generalize poorly even to specific industrial applications
on earth. To address this, we propose a method for generating
synthetic image data that are labelled for semantic segmentation,
generalizable to other tasks, and provide a prototype synthetic
image dataset consisting of 2D monocular images of unmanned
spacecraft, in order to enable further research in the area of
autonomous spacecraft rendezvous. We also present a strong
benchmark result (Sørensen-Dice coefficient 0.8723) on these synthetic data, suggesting that it is feasible to train well-performing
image segmentation models for this task, especially if the target
spacecraft and its configuration are known.

## Gastro-Intestinal Tract Segmentation Using Multi-Task Learning

[Report](/Computer_Vision/CV_Report.pdf) | [Poster](/Computer_Vision/CV_Poster.pdf)

Class: [CS 231N](http://cs231n.stanford.edu/) - Computer Vision

Our paper investigates methods to improve on the baseline methods of semantic segmentation in medical imaging.
Building on the UNet architecture, we implement two baseline methods, a UNet trained with a ResNet50 backbone
and a more parsimonious and streamlined UNet. Building
on the better-performing streamlined UNet, we investigate
using multi-task learning via supervised (regression) methods and self-supervised (contrastive learning) methods. We
find that the contrastive learning method has some benefits
in cases where the test distribution is signficantly different
from the training distribution (i.e. the patient is not seen by
the model during training time). Finally, we also investigate a method of improving on the UNet model by adding
image metadata such as the position of the MRI scan crosssection, and the pixel height and width known as Featurewise Linear Modulation (FiLM). We find that FiLM is beneficial when there is a slight overlap in the training and
test distribution, in that the test distribution consist of future scans of patients previously trained on.

