# 文本对抗攻击与防御  
   “对抗攻击”（Adversarial Attack）最先起源于计算机视觉领域，指利用“对抗样本”（Adversarial Example）攻击神经网络模型，诱导其产生错误输出的过程。  
   “对抗样本”是指对正常的输入样本添加微小扰动之后的样本， 比如对于一张图片略微修改几个像素值，或者对于一段文本用同义词替换掉其中的几个词。这类样本不干扰人类的正常判断，但能误导神经网络模型出错，比如一张熊猫的图片在修改几个像素值之后会被CNN图片分类模型识别为其他的动物，一段积极的电影评论经过同义词替换之后会被LSTM情感分类模型判断为消极。  
  由于文本和图像具有天然的区别，CV和NLP领域中的对抗攻击技术也有很大不同，例如，图像数据是连续的，略微修改像素值人类几乎无法分辨，而文本数据是离散的，对于文本的轻微改动就很有可能引起语义的不同， 因此构造文本对抗样本需要格外注意语义的保持。总体来看，CV领域中的一些对抗攻击方法不能直接迁移至NLP领域，例如基于梯度的对抗攻击方法，需要进行调整以适应文本独有的特点。在防御方法上也是如此，两个领域互相借鉴但又有显著的区别。  

推荐一个华中科技大学的硕士整理的论文列表，非常详尽：
https://github.com/xiaosen-wang/Adversarial-Examples-Paper

这里的github尽量放一些我读过的文章，加上一些自己的理解。另外刘正宵师兄是该方面的大神，有问题可以与他讨论。

## 一、综述类文章
1. Adversarial Attacks on Deep Learning Models in Natural Language Processing: A Survey（非常推荐）
2. Adversarial Attacks and Defenses in Images, Graphs and Text: A Review
3. Towards a Robust Deep Neural Network in Texts: A Survey
4. Adversarial Attacks and Defense on Texts: A Survey
5.Review of Artificial Intelligence Adversarial Attack and Defense Technologies

## 二、文本对抗攻击
