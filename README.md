# VisionAndPerception - Image Captioning

*"Vision and Perception" Course at Sapienza University of Rome, A.Y. 2021/2022.* <br />
*Professors: Prof. Irene Amerini, Prof. Paolo Russo*

This project is intended to deal with the problem of image captioning, that is, given an image as input, the expected output is the caption of the image. 
In order to solve such a problem, we merge computer vision techniques for object classification and detection with Natural Language Processing (NLP) techniques, 
pre-processing the ground truth caption of each image through Recurrent Neural Networks (RNNs). Specifically, this project idea is to implement a model that learns 
where to look: during the training phase, as the system reads the ground-truth caption, word by word, you can see the model’s gaze shifting across the image.

The dataset chosen to train our model contains real-world images from MS-COCO (82’783 training images, 40’504 validation images, 81’434 testing images), and other 
abstract clipart scenes created from models of humans and animals to remove the need to process noisy images and only perform high level reasoning (20’000 training 
images, 10’000 validation images, 20’000 testing images). Anyway, I opened the Dataset according to my GPU and to proceed with a clearer presentation of the results.

In here I compared the performance of a baseline model based on an Encoder-Decoder architecture, with the performance of a second model consisting of the same
Encoder-Decoder architecture in which the "Bahdanau Attention" mechanish is used.
Model evaluation is carried out by the automated BiLingual Evaluation Understudy (BLEU) metric which is the standard in the caption generation literature. 
This evaluates “generated captions” against “reference captions”.
<br />
<br />

*References:* 
1. Show and Tell: A Neural Image Caption Generator. By Oriol Vinyals, Alexander Toshev, Samy Bengio, Dumitru Erhan ICML 2015.
2. Microsoft COCO dataset
3. Bird, Steven, Edward Loper and Ewan Klein (2009). Natural Language Processing with Python. O'Reilly Media Inc. 
(nltk.translate package)
 <br />

*NOTE: Instructions to run the code.* <br />
In order to run the code, first thing to do is to run the notebook *V&P_PROJECT-DataProcessing.ipynb*, in which I built the Dataset, the Vocabulary and the Word Embeddings for the images captions. The complete execution of the notebook will take a while, since in here I opened the Dataset by choosing just 4/91 different categories with 1k images for each category.
Consequently, in order to proceed with Image Captioning, run the notebook *V&P_PROJECT-ImageCaptioning.ipynb*. <br />
-All the file paths need to be changed according to your files location.
