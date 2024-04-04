# Generative Adversarial Nets Notes

## Abstract Notes

- Estimate generative models using 2 neural network models
- Train models simultaneously, a generative model G and a discriminative model D
- Role of G is to maximise the probability of D making a mistake
- Role of D is to estimate if the sample came from the training data set or G
- Purpose is to allow for new similar data to be created from G

## Introduction

- Deep learning is used to represent the probability distribution for different kinds of data
- Deep learning has had success through backpropogation and dropout algorithms
- Use linear units which have gradients
- Traditional machine learning methods have not been as effecitvie with generative models

- In GANs the generative model is put against another model called a discriminator
- Generative model can be visualised as a team of countefeiters trying to produce fake currency and use it without detection
- The Discriminator model can be visualised as the police who are trying to detect the counterfeit currency
- The competition between the two mdoels improves each modelm until the counterfeits are indistiguishable from the real data
- When the generator model and the discriminative both use multilayer perceptron this is called adversarial nets
- In this case we can use backpropagrion and dropout algorithms
- The sample from the Generative model with only use forward propagation

## Related Work

- 

