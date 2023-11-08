# Mid_term_AI_mekdesbezah-uncc.edu
by Mekdes B.
# Background
Super Resolution GAN (SRGAN) Links to an external site.is a deep learning architecture that uses a combination of GANs and convolutional neural networks (CNNs) to generate high-resolution images from low-resolution images. The idea behind SRGAN is to train a generator network to create high-resolution images that are as close as possible to the real high-resolution images, and a discriminator network that is trained to distinguish between the generated high-resolution images and real high-resolution images. The training process involves feeding low-resolution images to the generator, which then generates a high-resolution image. The discriminator then evaluates the generated high-resolution image and provides feedback to the generator to improve the quality of the generated image. The generator and discriminator networks are trained iteratively until the generated images are of sufficient quality. Super Resolution GAN has many practical applications, such as in medical imaging, satellite imagery, and video processing. It can help to enhance the quality of low-resolution images, making them more useful for analysis and decision-making.
# Objective
To build a Generative Adversarial Network (GAN) and use it to generate high resolution images for the binary classification problem you have already implemented in Assignment 1.

# Basic Steps
**Steps to follow**: Train a binary classifier (called A) on the dataset using transfer learning (exactly like Assignment 1). The images should be downscaled to 128x128.

Next, train the SRGAN to generate 128x128 images. Each image of the training is downscaled to 32x32.
