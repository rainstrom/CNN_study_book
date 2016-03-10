# SDT_RNN
***Grounded Compositional Semantics
for Finding and Describing Images with Sentences***

Richard Socher, Andrej Karpathy, Quoc V. Le*, Christopher D. Manning, Andrew Y. Ng
Stanford University, Computer Science Department, *Google Inc.

##Task
组合语义来通过句子来找到和描述图片。

通过RNN模型，对句子进行编码得到的sentence vector，并不能够准确的代表视觉基础的含义（visually grounded meaning）

DT- RNN 使用了依赖树(dependency tree) to embed sentences into a vector space in order to retrieve images。 DT-RNN更关注句子中的动作和主体focus on the action and agents in a sentence

图片中的物体和物体之间有互相的联系，同样句子中的主体和主体之间也有联系。

主要的解决方案是单一模态的数据分别进行学习，最后map into a jointly learned multimodal embedding space.

sentence映射使用idea(Recursive neural network)， our model computes compositional vector representations **inside dependency trees**

##Model(DT- RNN)



##Model Detail



##Trick

