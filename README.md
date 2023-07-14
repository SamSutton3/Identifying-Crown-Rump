# Identifying-Crown-Rump

Code for published paper:

Sutton, S., Mahmud, M., Singh, R., Yovera, L. (2022). Identification of Crown and Rump in First-Trimester Ultrasound Images Using Deep Convolutional Neural Network. In: Mahmud, M., Ieracitano, C., Kaiser, M.S., Mammone, N., Morabito, F.C. (eds) Applied Intelligence and Informatics. AII 2022. Communications in Computer and Information Science, vol 1724. Springer, Cham. https://doi.org/10.1007/978-3-031-24801-6_17

Due to file sizes, model files have been omitted these include '.pkl' and '.hdf5' files.

In accordance to the paper publication, the code has been submitted to the GitHub repositry - https://github.com/brai-acslab/CRL-UlS

![image](https://github.com/SamSutton3/Identifying-Crown-Rump/assets/56264828/937a4184-164f-4318-910a-08c33c506920)


# Identification of Crown and Rump in First-Trimester Ultrasound Images using Deep Convolutional Neural Network

# Summary
A Machine Learning Pipeline has been created utilisng 3 Machine Learning Models to identify the Crown and Rump in First-Trimester Ultrasound Images. The Crown and Rump is used to measure the Crown to Rump Length (CRL) which is used to the predict the gestational age of the fetus, this metric is used to inform important decisions in the early pregnancy.

The Machine Learning System segments the fetus in the image using a U-Net Model. The segmented image is then subject to an image classification model that implements a pre-trained CNN model, namely, VGG-16. This model is used to classify the segmented images into ‘Good’ and ‘Bad’. Finally, the segmented images are entered into a pre-trained ResNet34 model that identifies the Crown and Rump regions.

The three models are documented in the headings below.

# Image Segmentation Model
Image Segmentation was highlighted in background research as vital for medical imaging. Paper by https://lmb.informatik.uni-freiburg.de/people/ronneber/u-net/ informed of the importance of a U-Net Model. Code was adapted from an existing repositry from Yu-Jen Huang at https://github.com/Huangyuren/unet_SCM which details the implementation of the complex U-Net Model.

![image](https://github.com/SamSutton3/Identifying-Crown-Rump/assets/56264828/34bc0fd9-9e32-4f56-a525-1ac74887f4e8)


# Image Classification Model
The image classification model will classify the segmented images from the U-Net Model into 'Good' and 'Bad' segmentation categories. Different pre-trained architectures, including ResNet50, InceptionV3, VGG-16 and Xception, were evaluated for the performance. With the VGG-16 Model being best suited to perform the classification.

![image](https://github.com/SamSutton3/Identifying-Crown-Rump/assets/56264828/7e1c92ee-338b-4b61-99ea-dd9017bf8925)


# Identification Model
The image classification model will classify the segmented images from the U-Net Model into 'Good' and 'Bad' segmentation categories. Different pre-trained architectures, including ResNet50, InceptionV3, VGG-16 and Xception, were evaluated for the performance. With the VGG-16 Model being best suited to perform the classification.
