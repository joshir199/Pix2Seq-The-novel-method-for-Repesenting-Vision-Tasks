# Pix2Seq-The-novel-method-for-Representing-Vision-Tasks
Understanding Pix2Seq model and its applications in simplfying Vision task using Language transformer models


# Pix2Seq Model :
It is the novel method to redesign the vision tasks like object detection, image captioning, image segmentation, object description etc. into a combination image encoder and language decoder to describe it on its own. It does not require any task specific prior-computations as it was in conventional methods.
Further, this models can be extended for different vision tasks using command/prompts, thus making vision task assisted with natural language.   

Original Research Paper : https://arxiv.org/pdf/2109.10852

For more similar papers analysis, refer here: https://github.com/joshir199/Revisiting-famous-Deep-Learning-research-papers

--------------------------------------------------
# Architecture

It involves Encoder-Decoder based architecture.
Encoder : Image Encoder to get latent/feature representation of the input image.
Decoder : Language Decoder to predict target sequence (containing bounding box details and class) as tokenx (one at a time).

Loss function : The model is trained to maximize the log likelihood of tokens conditioned on the image and the preceding tokens (with a softmax cross-entropy loss).
In following code, we used DeiT (Data Efficient Image Transfomer) model as Image Encoder for faster training but in original paper, they used the best Image Encoders like ViT, ResNet etc.




---------------------------------------------------
# Dataset

Dataset used in original paper MS-COCO 2017 containing 118k training images and 5k validation images and Object365 dataset.
But for sake of easier training, here PASCAL VOC 2018 dataset is used which contains around 17K images paired with its object description. 


-------------------------------------------------
# Results



