# FashionGAN
GAN - Generative Adversarial Networks
The basic agenda of a GAN is to identify patterns in input data, and produce examples resembling the original dataset.

Obviously considered as unsupervised learning models (as we implicitly do not point out the features, instead it just identifies patterns), but can also be used for semi-supervised learning.

They are made up of 2 neural networks, generator and discriminator.

Generator is used to generate synthetic data that mimics the real data.

Discriminator is used as a binary classifier to distinguish between real and fake data.

The goal of the discriminator is to classify real and fake data correctly, whereas the goal of the generator is to fool the discriminator into thinking the data generated is real. 

Tese 2 neural networks are made to compete with each other until generator is able to produce realistic data.
