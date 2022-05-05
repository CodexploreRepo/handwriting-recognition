# Handwriting Recognition


# 1. Dataset
## 1.1. List of Datasets
### 1.1.1. Japanese
- **Hiragana (ETL 8)**: the main alphabet. Each Hiragana has a corresponding Katakana
- **Katakana (ETL 1)**: Katakana are used for foreign words.
- **Kanji (ETL 8)**: Kanji are Chinese characters that were adopted in Japanese
- Source for [ETL](http://etlcdb.db.aist.go.jp/): how to unpack using [Medium article](https://towardsdatascience.com/creating-a-japanese-handwriting-recognizer-70be12732889)
- **Kuzushiji**: Old Japanese Hiragana, but much more complex
  - Source:  [Kuzushiji-MNIST](http://codh.rois.ac.jp/kmnist/index.html.en#:~:text=KMNIST%20is%20a%20dataset%2C%20adapted,software%20from%20MNIST%20to%20KMNIST.)
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


# 2 Conv-RNN-CTC
# 2.1. CTC
- [Explanation of Connectionist Temporal Classification](https://sid2697.github.io/Blog_Sid/algorithm/2019/10/19/CTC-Loss.html)

# Resources
## Conv-RNN-CTC network 
- [Build a Handwritten Text Recognition System using TensorFlow](https://towardsdatascience.com/build-a-handwritten-text-recognition-system-using-tensorflow-2326a3487cd5)
- [Handwritten Text Recognition with TensorFlow](https://github.com/githubharald/SimpleHTR)
- [Pytorch Repo](https://github.com/jc639/pytorch-handwritingCTC?fbclid=IwAR2E0vm1A06tsZuctxJT0YtA_3PelmwHDeDe94ylwY_hCuB9axQsn84nNdg)

## Japanese Multi Character Recognition
- [State-of-the-art image classification networks for hand-written hiragana characters](https://medium.com/@j.l/optical-character-recognition-on-hiragana-4de5e432d4b8)

## Region Proposal Network (RPN)
- [Faster R-CNN: Towards Real-Time Object Detection with Region Proposal Networks (6 Jan 2016)](https://arxiv.org/pdf/1506.01497v3.pdf). Gives a state of the art at the time about RPNs. And explains how anchor
based RPNs work
