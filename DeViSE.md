# DeViSE

[DeVise A Deep Visual-Semantic Embedding Model](pdf/41473.pdf)

Andrea Frome*, Greg S. Corrado*, Jonathon Shlens*, Samy Bengio Jeffrey Dean, Marc’Aurelio Ranzato, Tomas Mikolov

##Task
随着分类种类的增多，已标记的训练数据就不够了，所以利用其他类型的数据。使用visual data但是限制他们的预测。

文中提出一个新的 deep visual-semantic embedding model 来 identify visual objects using both labeled image data as well as semantic information gleaned from unannotated text(使用labeled image data识别视觉物体,也用未分配的语义信息)

N way分类会有一些问题，主要是他们之间本来互相有联系,但是却强行把他们分成了互不关联的东西（artifical label）（**不过我认为这并不一定**），也就不能transfer语义信息。

DeViSE利用textual data来学习labels之间的语义关联，之后更明确地maps images into a rich semantic embedding space.结果正确率与1-N的分类器相当，但是减少了一些语义冲突或者说是错误。另外model利用了visual and semantic 相似性来正确预测了 object category labels for unseen categories，比如zero-shot classification

##Zero-shot
Zero shot learning in simple terms is a form of extending supervised learning to a setting of solving for example a **classification problem when not enough labeled examples are available for all classes**.

Imagine this very interesting problem cited here [1] where we look at creating a classifier for certain held out classes **(say for CIFAR 100 you could hold 80 classes as train and 20 classes as test).** There is no intersection between the classes in train and test. 

Typical practises include training on a **unlabeled corpora like word2vec on Wikipedia** to **get word representation** and learning a regression function between image features (CNN,SIFT features) and **dimensions of word2vec** and this is then applied to the test classes. 

##Previous Model
###WSABIE
这个模型处理image feature和label到一个空间中

only explored linear mappings from image features to the embedding space, and the available labels were only those provided in the image training set. It could thus not generalize to new classes.

###Socher el al(zero shot learning)
种类太少，模型不同

##Model



##Model Detail (m-CNN的组成)



##Trick
