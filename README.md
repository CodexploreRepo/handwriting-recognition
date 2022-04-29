# Handwriting Recognition


# 1. Dataset
## 1.1. List of Datasets
## 1.2. Standarization
- Some general rules for input image standarization
  - Gray Scale (Black and White): only 1 channel, no RGB (3 channel) 
  - White background & Black Character (refer to the normalization)
  - Normalization: images should be in the range
    - **0 to 1**: using `min-max` scaler
    - **-1 to 1**: either `(image/ 127.5 -1)` or  `-(image/ 127.5 -1)` to convert to white background & black character (Depend on the dataset)

<p align="center">
<img src="https://user-images.githubusercontent.com/64508435/165878389-8f9ff6dc-4b58-4187-b455-9a860e99dcd1.png" width="600" />
  <br> 10 classes of Kuzushiji-MNIST
</p>
