# Seismic facies class prediction using U-net based on Parihaka-3D dataset

Seismic Facies Classification (SFC) is a technique of classifying different geologic regions of seismic images (facies). This is done to understand the characteristic of target reservoir based on it related properties and heterogenities. Facies interpretation is determined by seismic reflector information such as reflection geometry, lateral continuity and amplitude (SEG Wiki, 2019).

In this project, the author aims to predict seismic facies in a deep learning multi-class semantic segmentation problem based on seismic Parihaka-3D dataset. It is a public domain data interpreted with labels released by SEG in 2020 Machine Learning Challange. It is a 3D seismic data for input and 6 class labels for prediction. 

In this project, we managed to get a good fitting with above 98% validation accuracy and geologically accurate imaged facies prediction. The key elements of the project is as below:

- Use seismic data points (numpy array) instead of images (e.g: jpeg, png, etc.) in 2D slices.
- For a geologically accurate 2D seismic slices, we generate data from ZX (inline) and ZY (crossline) planes which form a total of 1372 vertical seismic slices.
- Uses original U-net with addition of normalization layers (credit to @aladdinpersson).
- Cross-entropy loss and hyperparameters of 1e3 learning rate, 10 epochs, and 16 batches.

Good luck and have fun exploring!
    
-----------------------------------------------------------------------------------------------
 
Data generation:
![4](https://user-images.githubusercontent.com/71542986/184467564-710df525-b929-4deb-aadd-3eeee6f9d123.jpg)

-----------------------------------------------------------------------------------------------

U-net:
![3](https://user-images.githubusercontent.com/71542986/184467581-f255ffc6-85a3-4745-90ee-564153d47e88.jpg)

-----------------------------------------------------------------------------------------------

Model fitting:
![2](https://user-images.githubusercontent.com/71542986/184467601-b782d23a-6fc0-4d0f-9b2b-0893cad4b1c5.jpg)

-----------------------------------------------------------------------------------------------

Output (1: input slice |2: label |3:prediction):
![5](https://user-images.githubusercontent.com/71542986/184467519-1659d1c0-e0bc-483a-b59f-2b72efa41ae8.jpg)

-----------------------------------------------------------------------------------------------

Prediction of upper epochs:
![1](https://user-images.githubusercontent.com/71542986/184467537-1ab0ba94-bd09-4596-ab83-374c66f4e4e8.jpg)
