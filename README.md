# Handwriting Recognition
![image](https://user-images.githubusercontent.com/64508435/172535844-3b632d6f-dc81-4090-b355-4fe168eb0091.png)


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
  - White background (255) & Character in Black (~0-180) (refer to the normalization)
  - Normalization: images should be in the range 
    - **0 (black) to 1 (white)**: `image/255.`
    - **-1 (black) to 1 (white)**: either `(image/ 127.5 -1)` or  `-(image/ 127.5 -1)` to convert to white background & black character (Depend on the dataset)
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

# Potentially useful links and tools for RNNs

## URLs

- [Blog page][BlogRNNSructure] that suggests a model structure that could prove useful to us.

- Courses for a [deep learning bootcamp][FullStackCourseMarch2019] that ended up on a "Build and deploy and end-to-end deep
learning system".

- [Tensorflow tutorial][tfTextGen] that implements and trains a text generator. Really clear for understanding what is
going on with RNNs.

- [Image annotation tool][annotator] implemented by Oxford.

[FullStackCourseMarch2019]: https://fullstackdeeplearning.com/march2019
[tfTextGen]: https://www.tensorflow.org/text/tutorials/text_generation
[BlogRNNSructure]: https://towardsdatascience.com/handwriting-to-text-conversion-using-time-distributed-cnn-and-lstm-with-ctc-loss-function-a784dccc8ec3
[annotator]: https://www.robots.ox.ac.uk/~vgg/software/via/via_demo.html

## Full Stack Deep Learning 
- [Full Stack Deep Learning ](https://fullstackdeeplearning.com/spring2021/)

## Conv-RNN-CTC network 
- [Build a Handwritten Text Recognition System using TensorFlow](https://towardsdatascience.com/build-a-handwritten-text-recognition-system-using-tensorflow-2326a3487cd5)
- [Handwritten Text Recognition with TensorFlow](https://github.com/githubharald/SimpleHTR)
- [Pytorch Repo](https://github.com/jc639/pytorch-handwritingCTC?fbclid=IwAR2E0vm1A06tsZuctxJT0YtA_3PelmwHDeDe94ylwY_hCuB9axQsn84nNdg)
- [Code gathering for everything we try to do !](https://githubharald.github.io/code.html)

## Japanese Multi Character Recognition
- [State-of-the-art image classification networks for hand-written hiragana characters](https://medium.com/@j.l/optical-character-recognition-on-hiragana-4de5e432d4b8)

## Region Proposal Network (RPN)
- [Faster R-CNN: Towards Real-Time Object Detection with Region Proposal Networks (6 Jan 2016)](https://arxiv.org/pdf/1506.01497v3.pdf). Gives a state of the art at the time about RPNs. And explains how anchor
based RPNs work

- [Region Proposal Network -- A detailed view](https://towardsdatascience.com/region-proposal-network-a-detailed-view-1305c7875853). Article that better explains how RPNs work and what are anchors.
