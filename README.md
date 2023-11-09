# Mid_term_AI_mekdesbezah-uncc.edu
by Mekdes B.

# Background
Super Resolution GAN (SRGAN) Links to an external site.is a deep learning architecture that uses a combination of GANs and convolutional neural networks (CNNs) to generate high-resolution images from low-resolution images. The idea behind SRGAN is to train a generator network to create high-resolution images that are as close as possible to the real high-resolution images, and a discriminator network that is trained to distinguish between the generated high-resolution images and real high-resolution images. The training process involves feeding low-resolution images to the generator, which then generates a high-resolution image. The discriminator then evaluates the generated high-resolution image and provides feedback to the generator to improve the quality of the generated image. The generator and discriminator networks are trained iteratively until the generated images are of sufficient quality. Super Resolution GAN has many practical applications, such as in medical imaging, satellite imagery, and video processing. It can help to enhance the quality of low-resolution images, making them more useful for analysis and decision-making.

# Objective
To build a Generative Adversarial Network (GAN) and use it to generate high-resolution images for the binary classification problem you have already implemented in Assignment 1.

# Basic Steps
**Steps to follow**: 
1. Train a binary classifier (called A) on the dataset using transfer learning (exactly like Assignment 1). The images should be downscaled to 128x128.
     Divide the dataset into 70% training and 30% testing 
2. Train the SRGAN to generate 128x128 images at least 150 epochs
3. Show some examples of scaled images in JNB
4. Apply normalization and image transformation and demonstrate some of the transformed samples.
5. Utilize the images generated by SRGAN in order to train a new model (called B).
6. Compare the performance of both models using different metrics such as F1, Accuracy, and AUC.
   
 # How to use the models:
   - The following steps show how to use the models.
     
A. First, download the dataset from this link (https://www.kaggle.com/c/dogs-vs-cats/data) and add it to the directory.
   
B. Open the **Model A** directory, then run **Model A_train.py** to train a binary classifier Model A. The images are downscaled to 128x128.
   
C. Then, Open **SRGAN_files** directory:
                        - Run **Train_SRGAN.py** to train SRGAN to generate 128x128 images.
                        - Generate SRGAN images from 32x32 to 128x128 by running **SRGAN_generatedImages.py**. Those images generated by SRGAN were stored in the SRGAN_outputImages directory.
     
**Sample examples of Images generated by SRGAN:**

**Dog Image**

**32x32: Low-Resolution image**

![Dog_117_lr](https://github.com/MekdesBezabh/Mid_term_AI_mekdesbezah-uncc.edu/assets/150180879/d234a18e-c841-4632-b63e-e5fc729317fa)


**128x128: SRGAN generated Image**

![Dog_117_generated](https://github.com/MekdesBezabh/Mid_term_AI_mekdesbezah-uncc.edu/assets/150180879/3b2f4f8e-ee46-4508-9408-1c28172f760b)

**Cat Image**

**32x32: Low-Resolution image**

![Cat_26_lr](https://github.com/MekdesBezabh/Mid_term_AI_mekdesbezah-uncc.edu/assets/150180879/f22cb769-e043-4094-9d33-1c991a15d732)


**128x128: SRGAN generated Image**

![Cat_26_generated](https://github.com/MekdesBezabh/Mid_term_AI_mekdesbezah-uncc.edu/assets/150180879/73e9af1b-ca4a-4b14-8835-a1e42edc26d2)
   
  
D. After that, open the **Model_B** directory: Train the binary classification model (model B) on SRGAN-generated images by running **Train_Model_B.py**.


**Sample examples of High-resolution images compared to all model outputs**


**Low-Resolution Images:**

![Dog_15_lr](https://github.com/MekdesBezabh/Mid_term_AI_mekdesbezah-uncc.edu/assets/150180879/469fbbf5-b955-4ce2-8ec5-ae7723e5e5d3)

![Cat_59_lr](https://github.com/MekdesBezabh/Mid_term_AI_mekdesbezah-uncc.edu/assets/150180879/e227d83d-8c1d-475b-8456-a4c78edab13b)


**SRGAN Generated Images:**

![Dog_15_generated](https://github.com/MekdesBezabh/Mid_term_AI_mekdesbezah-uncc.edu/assets/150180879/f6059e17-bb74-4068-9964-762ee1e70719)

![Cat_59_generated](https://github.com/MekdesBezabh/Mid_term_AI_mekdesbezah-uncc.edu/assets/150180879/8db67fbf-6d1c-49ea-b2c4-6d12dc08ba49)


**High-Resolution Images:**

![Dog_15_hr](https://github.com/MekdesBezabh/Mid_term_AI_mekdesbezah-uncc.edu/assets/150180879/3fc631d5-7b88-40d1-9589-0dce66d75eb3)

![Cat_59_hr](https://github.com/MekdesBezabh/Mid_term_AI_mekdesbezah-uncc.edu/assets/150180879/1360db8a-8c48-459b-9f09-ac475f22a9f6)


E. Finally, open the **Result_Performance of Models** directory, then run **Comparison.py**, to compare the performance of both models by calculating their metrics such as F1, AUC, and their Accuracy.

**Comparison results of Model A and Model B**

![confusion_matrix_model_A](https://github.com/MekdesBezabh/Mid_term_AI_mekdesbezah-uncc.edu/assets/150180879/ec8ceb3d-4a9e-40c9-bd5e-be6ff0edd946)

![confusion_matrix_model_B](https://github.com/MekdesBezabh/Mid_term_AI_mekdesbezah-uncc.edu/assets/150180879/291b39ca-1fff-4bf5-82ca-ec1fdba6e532)


Model A:
────────────────────────────────────────────────────────────────
      test_accuracy         0.9700000286102295
        test_auc            0.9967048764228821
         test_f1            0.9705072641372681
        test_loss           0.08344254642724991
     test_precision         0.9531410932540894
────────────────────────────────────────────────────────────────




Model B:

────────────────────────────────────────────────────────────────
      test_accuracy         0.8634666800498962
        test_auc            0.9538756012916565
         test_f1            0.8747247457504272
        test_loss            0.321264386177063
     test_precision         0.8071799278259277
────────────────────────────────────────────────────────────────


# References:
1. https://www.kaggle.com/c/dogs-vs-cats/data
2. https://openaccess.thecvf.com/content_cvpr_2017/papers/Ledig_Photo-Realistic_Single_Image_CVPR_2017_paper.pdf
3. https://www.kaggle.com/code/ahmadjaved097/using-transfer-learning-to-classify-cats-dogs
4. https://medium.com/analytics-vidhya/implementing-srresnet-srgan-super-resolution-with-tensorflow-89900d2ec9b2
