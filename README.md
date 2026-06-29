# BugApp

BugApp is a computer-vision prototype for identifying common garden pests from
photos. It was designed to help homeowners and gardeners recognize a pest,
understand which plants may be affected, assess potential risks, and choose an
appropriate treatment.

![BugApp prototype](BugApp.gif)

## Project overview

The prototype classifies 12 pest categories:

- Ant
- Bee
- Beetle
- Caterpillar
- Earthworm
- Earwig
- Grasshopper
- Moth
- Slug
- Snail
- Wasp
- Weevil

The dataset was based on the
[Agricultural Pests Image Dataset](https://www.kaggle.com/datasets/vencerlanz09/agricultural-pests-image-dataset)
and supplemented with additional web images to improve class balance. Images
were manually divided into training, validation, and test sets using an
approximately 70/20/10 split.

Several convolutional-network iterations were evaluated. The strongest
documented result used transfer learning with MobileNetV2 and 64 × 64 input
images, reaching approximately **73.3% test accuracy** with a test loss of
**0.84**. The error analysis found that visually similar classes—especially
beetles versus caterpillars and slugs versus snails—remained the main source of
misclassification.

## Product concept

BugApp was designed around four user needs:

- Fast identification of a photographed pest
- Information about plants commonly affected by that pest
- Practical pest-management guidance
- Clear safety information about risks to people

Two interface variants were evaluated through an A/B study. The measured
differences were not statistically significant, indicating that further
qualitative research and interface iteration would be more useful than choosing
between the tested variants based on the available sample.

## Repository contents

| Path | Contents |
| --- | --- |
| `Deliverables/` | Creative brief, model experiments, analysis, and project presentation |
| `AB_test/` | Prototype variants, survey data, statistical analysis, and report |
| `DataLab/` | Deep-learning and explainable-AI experiments |
| `Extra Challenges/` | Additional computer-vision exercises |
| `Courses/` | Supporting UX and design coursework certificates |

## Project artifacts

- [Demo video](demo_video.mp4)
- [Project presentation](Deliverables/Project-Presentation.pdf)
- [Infographic](infographic_230623.pdf)
- [Creative brief and model analysis](Deliverables/CreativeBrief_MarioVelichkov_230623.ipynb)
- [A/B testing report](<AB_test/A&B Test.pdf>)

## Reproducibility notes

This repository is a portfolio archive of the research, experiments, and
prototype artifacts. The image dataset and trained model weights are not
included, and some notebook cells reference the original local dataset paths.
Reproducing the reported model therefore requires downloading the source
dataset, recreating the documented splits, and updating those paths.

## Status

BugApp is an academic prototype and should not be treated as a professional
pest-control or safety assessment tool.
