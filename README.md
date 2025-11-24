# FashionGAN 🧵
**Context on GANs - Generative Adversarial Networks**
The basic agenda of a GAN is to identify patterns in input data, and produce examples resembling the original dataset.
Obviously considered as unsupervised learning models (as we implicitly do not point out the features, instead it just identifies patterns), but can also be used for semi-supervised learning.
They are made up of 2 neural networks, generator and discriminator.
Generator is used to generate synthetic data that mimics the real data.
Discriminator is used as a binary classifier to distinguish between real and fake data.
The goal of the discriminator is to classify real and fake data correctly, whereas the goal of the generator is to fool the discriminator into thinking the data generated is real. 
These 2 neural networks are made to compete with each other until generator is able to produce realistic data.
If the epochs are increased to 2000, you will be able to see better results and understand the potential of GANs.

This project implements a simple Generative Adversarial Network (GAN) using TensorFlow to generate Fashion-MNIST images. It includes loading the dataset, building the generator and discriminator, and training the GAN using a custom training loop.

---

## 🔧 Tech Stack
- **Language:** Python  
- **Framework:** TensorFlow / Keras  
- **Libraries:** TensorFlow Datasets, NumPy, Matplotlib  

---

## 📂 Dataset
- **Source:** Fashion-MNIST  
- **Classes:** 10 clothing categories  
- **Preprocessing:**  
  - Normalization (0–1)  
  - Caching, shuffling, batching  
  - Prefetching for GPU efficiency  

---

## 🧠 Model Architecture

### Generator
- Input: 128-dimensional noise  
- Layers: Dense → Reshape → Upsampling → Conv2D  
- Output: 28×28 grayscale fake image  

### Discriminator
- Input: 28×28 real or generated image  
- Layers: Conv2D → LeakyReLU → Dropout  
- Output: Real/Fake prediction  

---

## 🚀 Training
- Custom training loop using `tf.GradientTape`  
- Loss: Binary Cross-Entropy  
- Optimizers: Adam  
- Saves generated sample images after each epoch  

---

## 📌 Results
- GAN produces realistic Fashion-MNIST-like images after training    

---
