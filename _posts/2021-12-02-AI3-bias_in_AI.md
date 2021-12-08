---
title:  AI (3) - Biased AI
mathjax: true
layout: post
categories: 
    - artificial intelligence
    - neuroscience
    - neural networks
---

# How is AI biased?

Many articles have been written about the increasing problem of 'racist' AI. But how come AI systems are biased in the first place? First, we must understand how these systems are trained.

# Machine Learning

AI is basically a machine learning technique on stereoids: they take large amounts of data to create intelligent behaviour. Basic ML algorithms can do things like predicting housing prices, classifying data, and reducing the dimensionality of data (PCA, SVD, Fourier). [Explain dimensionality reduction] One problem we always face is how to set the parameters of our machine learning model.

During training of a model, such as a deep neural network, we need to optimize the weights. We do this by feeding the model with information in form of input data. This could be images, text, or even speech. At the beginning of training the input data gets passed through the network. We call this the **feedforward** **pass**. The input is transformed into numbers (e.g. a numerical representation of images would be a list of numbers - the pixel values) and undergoes various processing steps before the network returns an output. We then compare this predicted output to the actual input. We typically denote the output as *y* and the input as *x<sub>i</sub>*. 

When we compare the prediction to the actual input we compute the error the network made - the bigger the error, the more it must be punished (or trained). We do this via the **backward pass** which is known as **backpropagation**. To keep it simple: backpropagation simply adjusts the weights in each layer by multiplying a weight *w<sub>n</sub>* by some amount. The larger the error, the larger this update to the weight. Repeating this procedure of feedforward and backward passes enough times, results in a network whose weights are tuned towards the data we've used as input. The idea is that the model is now able to approximate this data. 

When we feed it new data which it hasn't seen before, we expect it to classify it correctly based on its trained weights. However, the training procedure poses a big problem: how do we fit the model to the data just the right amount as to not limit ourselves to only just data?

This is where bias comes into play: the more biased a network is, the more it fits the data it was trained on. For example, if the majority of input data used for training involves criminal cases which consist largely of african-american repeat offenders [CITE], it will tune it's weights to fit that distribution; the result is a model which will predict, based on its training, that an african-american will be more likely to engage in criminal acitvities again. 

In machine learning we make a trade-off between bias and variance. The variance describes how large the error is between our prediction and the actual values; low variance means that the network or model is **overfit**. This bares the risk of performing well on training data, but not being able to generalize to new input data. High variance is the opposite. Bias on the other hand controls how much error the network causes by missing important connections in the data. Both control how well the network will generalize to new input. 

The dilemma is that 'racist' AI is in reality a biased AI: it was incorrectly & insufficiently trained on the data. 

Future research should explore the bias/variance trade-off and find ways to optimize training data for representability & lack of underlying assumptions. However, it should also explore the benefits that may arise from 'stereotyping': it is possible that despite the negative implications for socioeconomic based issues, such as income, gender or race, stereotyping offers a valuable way for quickly categorizing novel instances by making use of heuristic assumptions. In this respect, deep meta-Reinforcement Learning offers a promising avenue, due to it's approach of creating cognitively nimble AI with deep sophisticated knowledge.

