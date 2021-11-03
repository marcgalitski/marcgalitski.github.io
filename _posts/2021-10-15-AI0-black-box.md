---
title:  AI (0) - Black Box Model
mathjax: true
layout: post
categories: 
    - artificial intelligence
    - evolutionary computing
    - neural networks
---

## Black Box
A black box is a box where you put something and get something out. You do not know what happens inside the box, only what you put in - the input - and what comes out: the output. We use this view to describe computer systems where we are not quite sure what is going on inside. This is a common problem in neural networks, and especially deep neural networks. DNNs consist of many layers of computation and we often do not know what happens inside them. For example, how can a network say that our cat picture has a cat in it and our dog picture a dog? 

When we develop a neural network or some other type of problem-solving algorithm, it is good to know what kind of problem we are dealing with exactly. Are we trying to find an input which fulfills some sort of requirement? Or are we looking for a model which is great at predicting stockprices? The black box view of computational models helps us identify these problem types, by distinguishing between 3 components: the input, the model, and the output. 

## Optimization
If the input is not known, then we are dealing with an **optimization problem**: we only have the model and the output to our disposal. A typical problem is the travelling salesman problem: how can we visit all the cities in a region with a limited amount of moves? The goal is to find the input which optimizes this requirement; i.e. it finds the shortest sequence to visit all the cities. You may realize how finding the shortest sequence of any input can be quite useful across a wide range of problems: finding the shortest route on Google Maps, creating layouts for buildings, or creating schedules. What happens, however, when we have no idea what the model should look like in the first place? 

## Modelling
**Modelling problems** require us to estimate the unknown model by using inputs & outputs. After providing enough inputs we hope that the model learns some pattern so that it can predict future inputs' values. This type of problem is useful for building a stocktrading bot; here, we need to find a model which can predict stock prices (output) based on historical stock data (input). Another example would be image recognition, where we label images, feed them to our model, and hope to find a model which can correctly label new, unlabelled images. Interestingly, we can transform modelling problems into optimization problems: instead of asking for a model *m* which accurately maps an input *x* to its label *y*, we can attempt to find a model *m* which makes the least amount of mistakes. You may have noticed that this implies that if we find a solution to a optimization problem, we have also found a solution to our modelling problem, because we have found a model (modelling) with optimal performance (optimization). 

## Simulation
Lastly, if we do not know what the output of our model is supposed to be, we can phrase it as a **simulation problem**. This is quite useful for studying the effects of self-driving cars, for example. Instead of unleashing untested algorithms out on the street, we can have them spend millions of virtual miles behind a driving simulator to assess their performance. Because we are using a simulation, we have much more control over the different variables, the amount of experiments we can do, and the amount of testing data we can generate. This makes simulations much less expensive than conducting research in real world environment, which is also associated with great risks. However: no simulation is perfect, and the results should never be considered to be realistic. At best they are a proof-of-concept.

By using the black box view to classify a problem-at-hand as either a optimization, modelling, or simulation problem, we can take some of the guesswork out of our research. Understanding this view can help immensely in starting to think more pro-actively about what the goal of our model or system is supposed to be. 