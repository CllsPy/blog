---
title: "Perceptron: The Neuron That Will Help You Understand Neural Networks"
draft: false
ShowToc: true
date: 2024-08-26
tags: ["neural networks"]
author: Carlos Lima
---

## What is the utility of the perceptron?

The perceptron was created in 1943 by Warren McCulloch and Walter Pitts. The fundamental idea behind its architecture is the ability to map an input value (x1, x2, ..., xn) to a simple binary output value.

However, the perceptron has some limitations, such as being useful only for binary classifications and requiring that the problem be linearly separable (which will be discussed later).

The goal of this post is to address the origin and mathematics behind the perceptron and explain why understanding it will provide a solid foundation for understanding other machine learning models (such as logistic regression) and neural networks.

Rosenblatt (1958) proposed the perceptron as an architecture to understand intelligent systems, applying to both hypothetical nervous systems and machines. The model enables the simulation of artificial intelligence similarly to how a biological neuron functions, through its activation.

## The Mathematics of the Perceptron

The algorithm for mapping involves calculating the product of input values (x1, x2, ..., xn) by weights (initially random) and summing these products (x1*w1 + b, x2*w2 + b, ..., xn*wn + b) for each occurrence.

![Fig. 1: Visualization of the perceptron design (Image source: Neural Networks and Perceptron — Lesson 9)](https://www.googleapis.com/download/storage/v1/b/kaggle-forum-message-attachments/o/inbox%2F11611801%2Fff9fb2148076f7a13adbac0fa7a3c18c%2F1.png?generation=1721706259635777&alt=media)
*Fig. 1: Visualization of the perceptron design (Image source: Neural Networks and Perceptron — Lesson 9)*

The resulting value then passes through an activation function, which performs a classification based on the value computed in the previous step.

![](https://www.googleapis.com/download/storage/v1/b/kaggle-forum-message-attachments/o/inbox%2F11611801%2Fcce0491c398eaa1beca519adcb52c419%2F2.png?generation=1721706308814624&alt=media)
*Fig. 2: The activation function classifies the value computed in the previous step as 0 or 1 (Image source: Perceptron)*

When the result is obtained, we can finally update the weights, which were initialized with arbitrary values. This process repeats until we achieve the correct output.

![](https://www.googleapis.com/download/storage/v1/b/kaggle-forum-message-attachments/o/inbox%2F11611801%2Fdbb924cc7315d9effefab02c6ff85c97%2F3.png?generation=1721706343082261&alt=media)
*Fig. 3: The formula for updating the weights is the product of the learning rate, the error, and the input value (Image source: Machine Learning with Sklearn and Pytorch)*

These steps are known as the Perceptron Learning Rule and can be simplified as follows:
1. Start with random values for weights and bias, typically 0, to simplify the calculation.
2. For each example:
   - Calculate the output value.
   - Update the weight and bias.

![](https://www.googleapis.com/download/storage/v1/b/kaggle-forum-message-attachments/o/inbox%2F11611801%2Fb85db5dba48f679c95713dc18050fc1c%2F4.png?generation=1721706378833540&alt=media)
*Fig 4. The Perceptron Learning Rule (Image source:  Machine Learning with Sklearn and Pytorch)*

## Limitations

Although the perceptron has limitations, such as difficulty in classifying non-linearly separable problems, its design is the foundation for modern neural network architectures. This includes models that later inspired the creation of the Adaline (Adaptive Linear Neuron). The reason is that the essence of the perceptron architecture lies in the core problems in machine learning: minimizing the cost or objective function.

![](https://www.googleapis.com/download/storage/v1/b/kaggle-forum-message-attachments/o/inbox%2F11611801%2F48a50487a376a3003a8e3dd8d77ce5b6%2F5.png?generation=1721706422482076&alt=media)
*Fig. 5: Example of linearly separable and non-linearly separable functions (Image Source: Machine Learning with Sklearn and Pytorch)*

## References

1. Rosenblatt, F. (1958). The perceptron: A probabilistic model for information storage and organization in the brain. *Psychological Review, 65*(6), 386.
2. Cortiz, D. (2020, July 8). Redes neurais e Perceptron - Aula 9 [Video]. YouTube. https://www.youtube.com/watch?v=fEukSrpDPH0
3. Perceptron. (n.d.). *Wikipedia*. https://pt.wikipedia.org/wiki/Perceptron
4. Doe, J. (2023). *Machine learning with Sklearn and Pytorch*. Tech Press.
