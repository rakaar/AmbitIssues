The emergence of Generative Adversarial Networks (GANs)

-Utkarsh Sinha, 4th year ECE, IIT KGP

Introduced in 2014 by Ian Goodfellow, GANs have taken the Deep Learning Community by storm. GANs are based on an interesting game-theoretic framework of a two-player mini-max game. Being one of the best Deep Generative Models with exciting applications makes GANs a domain of extensive research and thought leadership. This article is meant for readers having a basic understanding of machine learning and probability theory.

An introduction to Deep Generative Models:

A Deep Generative Model is a powerful way of learning any kind of data distribution using unsupervised learning and it has achieved tremendous success in just a few years. All types of generative models aim at learning the true data distribution of the training set so as to generate new data points with some variations. But it is not always possible to learn the exact distribution of our data either implicitly or explicitly and so we try to model a distribution which is as similar as possible to the true data distribution.

 The promise of deep learning is to discover rich, hierarchical models that represent the probability

distributions over the kinds of data encountered in artificial intelligence applications, such as natural images, audio waveforms containing speech, and symbols in natural language corpora. So far, the most striking successes in deep learning have involved discriminative models, usually those that map a high-dimensional, rich sensory input to a class label. These striking successes have

primarily been based on the backpropagation and dropout algorithms, using piecewise linear units

which have a particularly well-behaved gradient.

Deep Generative Models have had less of an impact, due to the difficulty of approximating many intractable probabilistic computations that arise in maximum likelihood estimation and related strategies, and due to the difficulty of leveraging the benefits of piecewise linear units in the generative context. 

GANs sidestep the difficulties faced by traditional Deep Generative Models and deliver outstanding results. Owing to this, GANs along with Variational Auto-Encoders (VAEs) are the most efficient Deep Generative models to date. 

The GAN Framework:

GANs combine concepts of  Game Theory and Deep Neural Networks. 

The basic idea of GANs is to set up a game between two players. One of them is called the generator. The generator creates samples that are intended to come from the same distribution as the training data. The other player is the discriminator. The discriminator examines samples to determine whether they are real or fake. The discriminator learns using traditional supervised learning techniques, dividing inputs into two classes (real or fake). The generator is trained to fool the discriminator. We can think of the generator as being like a counterfeiter, trying to make fake money, and the discriminator as being like police, trying to allow legitimate money and catch counterfeit money. To succeed in this game, the counterfeiter must learn to make money that is indistinguishable from genuine money, and the generator network must learn to create samples that are drawn from the same distribution as the training data.

The two players in the game are represented by two functions, each of which is differentiable both with respect to its inputs and with respect to its parameters. The discriminator is a function D that takes x as input. The generator is defined by a function G that takes z from a latent noise function as input. Both players have cost functions that are defined in terms of both players’ parameters. Because each player’s cost depends on the other player’s parameters, but each player cannot control the other player’s parameters, this scenario is most straightforward to describe as a game rather than as an optimization problem. The solution to an optimization problem is a (local) minimum, a point in parameter space where all neighboring points have greater or equal cost. The solution to a game is a Nash equilibrium. 

This game is, in fact, a two-player mini-max game. We need to minimize the cost function over the generator and maximize over the discriminator.

The applications of Deep Generative models:

One might legitimately wonder why generative models are worth studying, especially generative models that are only capable of generating data rather than providing an estimate of the density function. After all, when applied to images, such models seem to merely provide more images, and the world has no shortage of images. There are several reasons to study generative models, including:

Training and sampling from generative models is an excellent test of our ability to represent and manipulate high-dimensional probability distributions. High-dimensional probability distributions are important objects in a wide variety of applied math and engineering domains.

Generative models of time-series data can be used to simulate possible futures. Such models could be used for planning and for reinforcement learning in a variety of ways. A generative model used for planning can learn a conditional distribution over future states of the world, given the current state of the world and hypothetical actions an agent might take as input. The agent can query the model with different potential actions and choose actions that the model predicts are likely to yield a desired state of the world. Another way that generative models might be used for reinforcement learning is to enable learning in an imaginary environment, where mistaken actions do not cause real damage to the agent. Generative models can also be used to guide exploration by keeping track of how often different states have been visited or different actions have been attempted previously.

Finally, many tasks intrinsically require the realistic generation of samples from some distribution. Examples of some of these tasks that intrinsically require the generation of good samples using GANs include:

1. The suggestion of merchandise based on celebrity pictures has been popular for fashion bloggers and e-commerce. PixelDTGAN creates clothing images and styles from an image. 
2. The creation of super-resolution images from a lower resolution. This is one area where GAN shows impressive results with immediate commercial possibility. 
3. Text to image is one of the applications of a domain-transfer GAN. We input a sentence and generate multiple images fitting the description. 
4. Repairing of images has been an important subject for decades. GAN is used to repair images and fill the missing/obscure part with generated “content”. 
5. Active research is also going on in the direction of video generation and music generation from given videos and music respectively. 

GAN issues and ongoing research:

Even after being backed by the exciting theory of adversarial learning and game theory, GANs are yet to address some major practical issues. Some of the critical issues that have become interesting fields of research in the Deep Learning community are:

1. Mode Collapse: It is one of the most popular problems that is currently being worked upon by GAN researchers. The issue lies in the fact that GANs tend to converge after learning only one/ or a few modes of the given distribution. A mode is a maxima of the given probability distribution. Learning only a few modes of the given distribution leads to a reduction in the diversity of the generated samples. There is a trade-off between image diversity and image quality that researchers are currently trying to overcome. 
2. Non Convergence: The Nash Equilibrium solution of the zero-sum game can’t be reached in all cases by the Gradient Descent Algorithm. Many a time the model parameters oscillate, destabilize and never converge. 
3. Vanishing Gradient: If the discriminator gets too successful in the beginning then the generator gradients vanish and hence the generator learns nothing. 
4. Overfitting: It may also happen that the Generator overfits on the training dataset. In the overfitting scenario the generator does not add stochastic changes to the produced samples and rather simply copies the training data set.  

The addressal of these issues has led to the development of a lot of variants built on top of the vanilla GAN. Notably, WGAN, DCGAN, Unrolled GAN, and MGGAN are some of the successful variants. Google Brain, Facebook AI Research and renowned professors from top universities are putting their minds into this. With the impact that GANs can have, this research is something cool to look out for!