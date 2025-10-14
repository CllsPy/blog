---
title: "How Do Machines Learn?"
draft: false
ShowToc: true
date: 2024-09-30
tags: ["machine learning"]
author: Carlos Lima
---


## Types of Learning
The types of learning determine what resources will be necessary to solve our problems. As suggested  Mohri (2018), there are four fundamental types of learning, each with its specifications:

- Supervised machine learning
- Semi-supervised learning
- Unsupervised machine learning
- Reinforcement learning

In this essay, we'll use supervised machine learning for simplicity. Generally, we use this approach to handle regression problems and classification. A regression problem needs a real output, such as the mean value of a house, while classification typically results in a binary output (e.g., yes/no or rain/no rain).

### Supervised Machine Learning
This is the most common method. What characterizes supervised learning is the presence of a label. Imagine you are a doctor receiving reports from your patients. These reports contain information, such as blood pressure and glucose levels, along with whether the patient has diabetes. If you want to use this information to predict diabetes in your future patients, you would call this a supervised learning problem.

## Unsupervised Machine Learning
In unsupervised machine learning, the model receives data but does not have access to any labels. The objective, similar to the supervised learning paradigm, is to predict patterns in unseen data. Clustering and dimensionality reduction are examples of unsupervised strategies.

## Semi-supervised Learning
Semi-supervised learning combines supervised and unsupervised learning. The main focus is to reduce the need for labeled data. We use part of the data with labels and another part without labels to find our output.

### Unsupervised Machine Learning
Unsupervised learning is characterized by the absence of labels. You input the data into the model and expect it to find something useful. For example, if we're working on a system to identify customer preferences for a product, we don't have labels; we're just seeking behavioral patterns.

### Reinforcement Learning
Imagine this type of learning as training a dog. You provide stimuli for actions you want to encourage and warnings for behaviors you want to discourage. In this way, the model learns by trying and adjusting. For example, a neural network learning how to play Go or chess.

## The Learning Problem
As saw in Koza (1996), there are situations where using data is a better way to solve a problem, meaning performing tasks without explicitly giving instructions, especially when you can't identify an analytical solution. For instance, weather forecasting requires complex equations to predict the future. Instead of using these equations, we can use historical data—let’s say from the last ten years—and create a statistical model to learn the unknown patterns and predict the weather based on certain characteristics (wind, temperature, etc.). We call those characteristics **features**, and the output value is our **target**.

## Components of Learning
To apply this strategy, we need to ensure that we have all the necessary components. These components are:

- Unknown target function
- Training data
- Algorithm
- Hypothesis
- Final Hypothesis

### Target Function
The first requirement is a target function. A target function is an unknown function that we aim to define, ensuring that f(x) = y, where x is a vector of features and y is a label. In the forecasting problem, f: x → y is the pattern that, given x (humidity, temperature, etc.), yields y (rain/no rain). An unknown target function indicates a problem for which no analytical solution exists.

### Training Data
The training data consists of pairs (xi, yi), ..., (xn, yn). It's essential to ensure that some correlation exists between x and y, which can be examined by analyzing their distribution. In the forecasting problem, y could be (rain/no rain), and x would be the features fed into f to obtain y. See Table 1.

**Table 1: The Problem Setup**  
*It's important to clarify that this is a supervised problem since we have a target.*

| Temperature | Wind    | Target  |
|-------------|---------|---------|
| 25º        | 13 km/h | Rain    |
| 10º        | 10 km/h | Rain    |
| 13º        | 5 km/h  | No Rain |

### Algorithm
The algorithm is the statistical model that learns the patterns; there are several models available. In Figure 1, we see a diagram illustrating how the Perceptron algorithm.

![image](https://github.com/user-attachments/assets/ded36d18-8f48-4c9c-aa0b-fb414459d1b5)


*Figure 1. The Perceptron archeteture (Image source: Rosenblatt, 1958)*

Other machine learning models include:

- Logistic regression
- SVM (Support Vector Machines)
- Naive Bayes
- Decision trees

### Hypothesis
The algorithm (in our case, the Perceptron) generates a set of hypotheses, from which we select the best one—i.e., the hypothesis that approximates f: x → y and can predict future unseen data. This is referred to as the bias-variance tradeoff.

![image](https://github.com/user-attachments/assets/a098940f-445b-4d8d-af5d-dc407f2de801)


*Figure 2. The bias-variance trade-off (Image source: Raschka et. al 2022)*

### Final Hypothesis
Ultimately, we arrive at a hypothesis g that approximates f. Remember that originally we don't know f. However, with our final hypothesis, we can validate its accuracy by testing it against future unseen data.

### Summing Up
In this essay I present the fundamental understanding, the components above demonstrate what is needed to train a statistical model and find a function g that approximates f (unknown) using only data. Figure 3 summarizes all the components. Keep in mind we can expand even more, but this is the foundational building block for understanding how machines learn.

![image](https://github.com/user-attachments/assets/4fcb808f-a098-4039-9aff-ac0f1b6d89e4)


*Figure 3. Components of Learning (Image source: Abu-Mostafa, 2012)*

## Further Reading
- https://www.ibm.com/think/topics/machine-learning-types
- https://maths.ucd.ie/~plynch/Publications/pcam0159_proof_2.pdf
- https://psycnet.apa.org/record/1959-09865-001
- https://towardsdatascience.com/perceptron-learning-algorithm-d5db0deab975
- https://machinelearningmastery.com/what-is-a-hypothesis-in-machine-learning/
- https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff
- https://towardsdatascience.com/understanding-the-bias-variance-tradeoff-165e6942b229

## References
[1] Mohri, M. (2018). Foundations of machine learning.

[2] Koza, J.R., Bennett, F.H., Andre, D., Keane, M.A. (1996). Automated design of both the topology and sizing of analog electrical circuits using genetic programming. In: Gero, J.S., Sudweeks, F. (eds) Artificial Intelligence in Design ’96. Springer, Dordrecht. https://doi.org/10.1007/978-94-009-0279-4_9

[3] Rosenblatt, F. (1958). The perceptron: a probabilistic model for information storage and organization in the brain. Psychological review, 65(6), 386.

[4] Raschka, S., Liu, Y. H., & Mirjalili, V. (2022). Machine Learning with PyTorch and Scikit-Learn: Develop machine learning and deep learning models with Python. Packt Publishing Ltd.

[5] 5. Abu-Mostafa, Y. S., Magdon-Ismail, M., & Lin, H. T. (2012). Learning from data (Vol. 4, p. 4). New York: AMLBook.

