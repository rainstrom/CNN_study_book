####Multimodal Convolutional Neural Networks for Matching Image and Sentence


[](ICCV2015.pdf)

#Task
句子->图像 以及 图像->句子 双向检索 on the Flickr8K and Flickr30K datasets.

#Model

* one image CNN encoding the **image content** 

* one matching CNN modeling **the joint representation of image and sentence**.

  * The matching CNN composes **different semantic fragments** from words and learns the inter-modal relations between image and the composed fragments at different levels => to fully exploit the matching relations between image and sentence. 
  
  * letting **image** and **the composed fragments of the sentence** meet and interact at different levels. (**使图像和句子的组合片段，在不同的level交互**)

  * local与global结合，在不同的level，单词、句子和图片会有所对应

#Model Detail (m-CNN的组成)
####Image CNN

generate the **image representation** (a 4096-dimensional feature vector)

then use W_im? => a **d-dimension vector νim**.

####Matching CNN
input: the encoded image representation **V_im** and word representations **V_wd**

produces: the joint representation **ν_JR** (learnt **joint representation** of image and sentence）

过程是matching CNNs first compose different seman- tic fragments from the words and then learn the inter- modal structures and interactions between the image and composed fragments.

#####word level matcing CNN: MatchCNN_wd

![](QQ20160308-0@2x.png)

![detail](QQ20160308-1@2x.png)

这个结构非常特殊，因为我们注意到，对于文字的处理也是用CNN的，3个单词进行卷积，同时每个位置的卷积都把v_im加入

####Multilayerperceptron(MLP)
ν_JR (joint representation) => final matching score between image and sentence


