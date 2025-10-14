---
title: "Understanding Gradient Descent"
draft: false
ShowToc: true
date: 2024-08-27
tags: ["gradient descent"]
author: Carlos Lima
---


Nowadays, even the most sophisticated tools that use [AI](https://en.wikipedia.org/wiki/Artificial_intelligence) are favored by the optimization algorithm, Gradient Descent. From [ChatGPT](https://openai.com/chatgpt/) to [Midjourney](https://www.midjourney.com/home), the concept is applicable due to the central theme in Machine Learning: minimizing the cost function.

**This post aims** to give readers a general overview of this tool, which exists beyond the field of Machine Learning but plays a crucial role, being continuously mentioned in tutorials, books, or videos when the topic is Artificial Intelligence.

## Gradient

Before diving into the understanding of Gradient Descent, we need to understand what a Gradient is. Simply put, [it is the slope of a curve at a given point in a specific direction](https://towardsdatascience.com/gradient-descent-algorithm-a-deep-dive-cf04e8115f21).

In cases where the function is univariate, the gradient is given by the first derivative of the function. For multivariable cases, it becomes a vector of partial derivatives (since what matters is the slope in a specific direction).

![](https://www.googleapis.com/download/storage/v1/b/kaggle-forum-message-attachments/o/inbox%2F11611801%2Fe8073cf2b16c0c619aac9993c7944bb3%2Ffig1.gif?generation=1723230893699524&alt=media)

## Gradient Descent

Gradient Descent is an algorithm used in the optimization of neural networks, and today it is one of the most popular [(Ruder, 2017)](https://arxiv.org/pdf/1609.04747). Understanding how it works will allow the reader to grasp how models function at their deepest level, rather than seeing them as a black box. This can be advantageous for several reasons, including improvement and debugging.


## How Does Gradient Descent Work?

First, it is necessary to consider that there are two conditions we depend on to calculate the Gradient of a function:

1. The function is differentiable.
2. The function is convex.

![](https://www.googleapis.com/download/storage/v1/b/kaggle-forum-message-attachments/o/inbox%2F11611801%2Fca22565954ad5fbbcef9fa2bd998ded7%2Ffig2.png?generation=1723231013642809&alt=media)


>In their work (Du, et al. 2016), they prove that it is possible to reach the global minimum even for functions that do not satisfy the second condition.

In the mathematical field of optimization, the cost function is a metric that maps an event to a real value, which in this case would be the cost. An optimization problem is characterized precisely by the reduction of this real value; therefore, the gradient descent algorithm plays a fundamental role in this process.

![](https://www.googleapis.com/download/storage/v1/b/kaggle-forum-message-attachments/o/inbox%2F11611801%2F975197d26c40583ad4279c5371868f1d%2FComparison_of_loss_functions.png?generation=1723231091653054&alt=media)

We can conclude that gradient descent is an optimization technique specialized in machine learning algorithms, which consist of minimizing a metric by which we can evaluate the performance of statistical models. Even the most modern tools today rest on this simple yet powerful idea.

![](https://www.googleapis.com/download/storage/v1/b/kaggle-forum-message-attachments/o/inbox%2F11611801%2Fca55d98c47dd06f35bd89f317e5ba520%2Ffeatured_huf8623e3651292c46251c2f19af84c2fd_651010_720x0_resize_lanczos_2.png?generation=1723231132565700&alt=media)


### Mentioned Blogs

- [How ChatGPT Actually Works](https://www.assemblyai.com/blog/how-chatgpt-actually-works/)
- [Gradient Descent Algorithm: A Deep Dive](https://towardsdatascience.com/gradient-descent-algorithm-a-deep-dive-cf04e8115f21)
- [Gradient Descent](https://www.ibm.com/topics/gradient-descent)
- [What is Gradient Descent?](https://www.khanacademy.org/math/multivariable-calculus/applications-of-multivariable-derivatives/optimizing-multivariable-functions/a/what-is-gradient-descent)
- [Gradient](https://en.wikipedia.org/wiki/Gradient)
- [Navigating the Terrain: Convex vs Non-Convex Functions in Optimization](https://ai.plainenglish.io/navigating-the-terrain-convex-vs-non-convex-functions-in-optimization-86812e9a1989)
- [Comparison Between Deep Learning vs Machine Learning](https://dzone.com/articles/comparison-between-deep-learning-vs-machine-learni)

**Papers:**

- [An Overview of Gradient Descent Optimization Algorithms (1609.04747)](https://arxiv.org/abs/1609.04747)
- [Gradient Descent Finds Global Minima of Deep Neural Networks (1811.03804)](https://arxiv.org/abs/1811.03804)
- [Loss Functions](https://faculty.ist.psu.edu/vhonavar/Courses/ds310/lossfunc.pdf)

**Extra:**

- [YouTube Video 1](https://youtu.be/xOB10eTjoQ8)
- [YouTube Video 2](https://www.youtube.com/watch?v=sDv4f4s2SB8)

**Wikipedia:**

- [Loss Function](https://en.wikipedia.org/wiki/Loss_function)

### Appendix

Fig.1 The Gradient for a Function with n Dimensions. (Image Source: [https://en.wikipedia.org/wiki/Gradient](https://en.wikipedia.org/wiki/Gradient))

Fig.2 When the function is not convex, there is no guarantee that the global minimum will be found. (Image Source: [https://ai.plainenglish.io/navigating-the-terrain-convex-vs-non-convex-functions-in-optimization-86812e9a1989?gi=8ecc65586601](https://ai.plainenglish.io/navigating-the-terrain-convex-vs-non-convex-functions-in-optimization-86812e9a1989?gi=8ecc65586601))

Fig.3 Comparison of Cost Functions Used in Regression Problems. (Image Source: [https://en.wikipedia.org/wiki/Loss_function#/media/File:Comparison_of_loss_functions.png(https://en.wikipedia.org/wiki/Loss_function#/media/File:Comparison_of_loss_functions.png))

Fig.4 Operation of Gradient Descent. (Image Source: [https://halfrost.me/post/how-to-understand-gradient-descent/](https://halfrost.me/post/how-to-understand-gradient-descent/))
