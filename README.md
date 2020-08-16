# DCGAN for generating Fashion MNIST Dataset
**GANs or Generative Adversarial Networks** are used for unsupervised learning of data disributions which, in turn, can be used for generating new data (generally images), which are very similar to the images present in the **REAL** data distribution. The original GAN paper consisted of 2 parts - **the generator and the discriminator** - used for this purpose. However, even though they were working with images, they used simple **MLP architectures** for both the parts, instead of using the Convolutional Neural Networks, which are widely used in supervised learning. 

Before the DCGAN paper was published, there had been many attempts at scaling the GANs using CNNs to get better results, given the fact that CNNs were primarily used for images in supervised learning. However, most of these attempts were unsuccessful. The **DC-GAN (Deep Convolutional Generative Adversarial Networks)** paper was hence, a new method, with CNN implementations of both the generator and the discriminator. Rather than downsampling and the upsampling the images in the generator, they input noise as a latent variable, which was then reshaped to given a low resolution image. This was **upsampled using Conv2DTranspose** to get the final image. The discriminator was a simple supervised learning based CNN architecture for classification of images - i.e. whether the images are **REAL or FAKE**. 

This repository contains my implementation of the original DC-GAN paper for **generating clothing images** which were used from the Fashion MNIST dataset. The model was trained on Google Colaboratory using their GPU for **100 epochs** which took about 1 hr to train. In some places, I used **SeLU activation**, as it appears to give a more stable training process than ReLU. Below are some results from the training process:- 

<p align="center">
 <img width="300" height="300" src="https://github.com/Terabyte17/DCGAN-for-Fashion-MNIST/blob/master/dcgan.gif"/>
</p>
