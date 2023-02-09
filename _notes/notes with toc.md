---
title: Notes with TOC
description: testing TOC
skip_toc: true
---



## Multimodal Neurons in CLIP

Our paper builds on nearly a decade of research into interpreting convolutional networks,3456789101112 beginning with the observation that many of these classical techniques are directly applicable to CLIP. We employ two tools to understand the activations of the model: feature visualization,6512 which maximizes the neuron’s firing by doing gradient-based optimization on the input, and dataset examples,4 which looks at the distribution of maximal activating images for a neuron from a dataset.

Using these simple techniques, we’ve found the majority of the neurons in CLIP RN50x4 (a ResNet-50 scaled up 4x using the EfficientNet scaling rule) to be readily interpretable. Indeed, these neurons appear to be extreme examples of “multi-faceted neurons,” 11 neurons that respond to multiple distinct cases, only at a higher level of abstraction.

## Absent Concepts

While this analysis shows a great breadth of concepts, we note that a simple analysis on a neuron level cannot represent a complete documentation of the model’s behavior. The authors of CLIP have demonstrated, for example, that the model is capable of very precise geolocation,19 (Appendix E.4, Figure 20) with a granularity that extends down to the level of a city and even a neighborhood. In fact, we offer an anecdote: we have noticed, by running our own personal photos through CLIP, that CLIP can often recognize if a photo was taken in San Francisco, and sometimes even the neighborhood (e.g., “Twin Peaks”).

Despite our best efforts, however, we have not found a “San Francisco” neuron, nor did it seem from attribution that San Francisco decomposes nicely into meaningful unit concepts like “California” and “city.” We believe this information to be encoded within the activations of the model somewhere, but in a more exotic way, either as a direction or as some other more complex manifold. We believe this to be a fruitful direction for further research.

###  How Multimodal Neurons Compose

These multimodal neurons can give us insight into understanding how CLIP performs classification. With a sparse linear probe,19 we can easily inspect CLIP’s weights to see which concepts combine to achieve a final classification for ImageNet classification: