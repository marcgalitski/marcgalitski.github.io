---
title:  AI (2) - Three obvious reasons why the brain cannot be doing backpropagation
mathjax: true
layout: post
categories: 
    - artificial intelligence
    - neuroscience
    - neural networks
---

1. Cortical neurons do not communicate real-valued activities
   1. What are real-values?
      1. Numbers such 3.14 or 2/5 or -6.9. 
      2. In neural networks we use vectors of these numbers to represent the weights of the different layers. 
         1. For example, the first layer is a vector w<sub>1</sub> *n* real values. The first value might be 0.92, the second value 0.2 and so on until the *n-th* value. These are the **weights** of w<sub>1</sub>. 
      3. Neural networks use these weights to communicate information
         1. The weights are essentially the input to a function. Each weight is passed to a function as an *x* value (e.g. $f(x)$). 
         2. The function $f(x)$ can be for example a sigmoid or a Rectified Linear Unit (ReLU). 
         3. A neural network uses hundreds of these functions in each layer. This allows it to **learn** from input - by passing in different values for *x* we get different positions on the function. 
            1. We hope that by using the right activation function we will be able to abstract the information in the input. For this we need to translate it into real-values.
   2. How do neurons communicate
      1. Neurons communicate via spikes i.e. electrical activity
      2. What are action potentials?
2. Neurons need to two send two types of signals
   1. forward
   2. backward
      1. backpropagation only passes backwards
   3. neurons in ANNs do not send activity forward AND backward
         1. Recurrent Neural Networks
3. Neurons do not have point-wise reciprocal connections with the same weight in both directions
   1. Nodes in ANNs have connections to multiple neurons with different weights
      1. however the weight from a single node_A to a node_B is the same both ways (i.e. from A to B and from B to A)
   2. Neurons have connections to various different neurons - the reciprocal connections have different weights as well
      1. e.g. a sending neuron might have a larger weighting than a backpropagating neuron --> backpropagation does exist - just not in a purely mathematical form, nor as a unique mechanism
      2. parallel weight assignments - neurons can have reciprocal connections with different weights, allowing for parallel forward passing as well as backpropagation