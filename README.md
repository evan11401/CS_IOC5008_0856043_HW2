# CS_IOC5008_0856043_HW2
## Brief introduction 
### 1. Development environment 
Python version : 3.7.4 

Framework : Pytorch 

Hardware : NVIDIA GeForce GTX 1080 Ti 11GB 

### 2. How to run the code. 
Open the BEGAN-CelebA-CS_IOC5008_0856043_HW2.ipynb 

Change the root of the dataset.

Run All

### 3. After train, the models will store in ./ckpt/

### 4. Load model and create Samples

## Methodology 

### 1.Data pre-precess
First, resize the image to (64+30, 64+30) and then Center Crop to (64, 64).
That will make the image focus on the face and decrease the background.

### 2. Model architecture
I using the Boundary Equilibrium GAN (BEGAN) that released on May 2017.

(1)The model is base on the Energy based GAN (EBGAN).

Instead of designing a discriminator similar to a classiﬁer, the discriminator uses an autoencoder which extracts latent features of the input image by an encoder and reconstruct it again with the decoder.

(2)The model also inspired by the Wasserstein GANs that introduced a loss that also acts as a measure of convergence

### 3.Hyperparameter
IMAGE_DIM = (64, 64, 3)

batch_size = 32

n_noise = 64

max_epoch = 20

lr_k = 0.001

gamma = 0.7

## Reference 
1.The EBGAN paper https://arxiv.org/abs/1609.03126
2.The BEGAN paper https://arxiv.org/abs/1703.10717 
3. Introduction to the BEGAN & EBGAN https://medium.com/@jonathan_hui/gan-energy-based-gan-ebgan-boundary-equilibrium-gan-began-4662cceb7824 
4. Introduction to the BEGAN (Chinese) https://read01.com/RjaeaM.html#.XcN2F5MzbLY
