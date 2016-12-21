> by Nate Soares  
> translated by Unintell
[原文链接](https://intelligence.org/research-guide/)


**如果人类想要制造出具有正面作用的、强于人类本身的人工智能，我们必须面对三个艰巨的挑战。首先，我们制造的超人系统（smarter-than-human systems）必须具有高度的可靠性，这样才能确保它能够满足我们给定的目标或者偏好。其次，系统的设计必须具有容错性，这样才能在人为错误发生的时候对系统进行在线修改或者修正。第三，这个系统必须能够真的学习到有益的目标或者偏好。**

MIRI目前的研究项目着眼于了解如何在[原则](https://intelligence.org/2015/07/27/miris-approach/)上克服这些挑战。关于可靠推理（reliable reasoning）的问题的某些方面，我们甚至在理论上都不甚了解；有一些关于有限理智（bounded rationality）的问题，我们在有所简化的情况也无法解决。作为第一步，我们的研究主要考虑从简化的情况出发。由此看来，我们现在的研究更像是纯数学，而不是软件工程或者是实用的机器学习问题。

这篇简介简短地介绍了我们优先需要研究的问题，并且提供一些资料以帮助你快速了解相关问题的前沿状态。其目的不在于合理化这些研究课题，更多关于我们的研究动机的信息，请参考以下文章：[MIRI的研究方式](https://intelligence.org/2015/07/27/miris-approach/)，[技术日程](http://intelligence.org/files/TechnicalAgenda.pdf)，[支持文献](http://intelligence.org/technical-agenda).

注（2016-sep）：这篇研究指导基于我们的技术日程文档，2016年以来，我们又引入了[专注于机器学习的研究日程](https://intelligence.org/files/AlignmentMachineLearning.pdf)。请参考这个文档以了解另外一部分没有在此提及，但是我们认为很有价值的研究方向。

---

# 0. 目录 # 

1. 如何使用该指导  
2. 基础信息  
3. 现实建模（realistic World-models）  
4. 决策论  
5. 逻辑不确定性  
6. Vingean Reflection  
7. 可矫正性  
8. 价值学习  
9. 其他工具  
10. 了解我们的使命  

---

# 1. 如何使用该指导 #

本文的目的在于激励对这个领域相关知识不是非常熟悉的研究者。如果你已经在从事人工智能相关的工作，或者是成熟的数学家，请考虑跳过这篇文章直接阅读我们现有的[文献](https://intelligence.org/all-publications/)。（我们的[技术日程](http://intelligence.org/technical-agenda/)是一个很好的出发点）本文意在帮助未来有意加入MIRI的学生，或者其他想要了解我们工作的专业人士。

研究者加入MIRI通常有两个途径。第一种是参加MIRI Workshop和我们面对面交流。。你可以从[这里](https://machineintelligence.typeform.com/to/fot777)申请参加MIRI Workshop。请注意Workshop之间的时间间隔可能很长，容量也很有限。

第二种途径是独立根据我们的研究日程做出成果，并让我们知道你的结果。你可以在此[在线申请](https://machineintelligence.typeform.com/to/fot777)我们的帮助。但是最快的开始做出贡献的途径是在[Intelligent Agent Foundations Forum](http://agentfoundations.org/)(IAFF)上发言，选择一个还未被解决的问题，并尝试解决它。你可以把你的成果的链接[发表](http://agentfoundations.org/links)在论坛。

这个论坛的首要任务是允许正在进行研究的研究者交流未完成的工作，因此论坛中的内容可能显得模糊。这篇指导能帮助你快速跟上IAFF上正在被讨论的话题。这也可以帮助你培养参加Workshop的必要能力，或者帮助你获得在其他机构研究AI的能力。

这篇指导以列举对此领域至关重要的基本课题开始，例如概率论。在这之后，划分为一系列的话题，并提供帮助你了解相关领域前沿知识的文献链接。

这不是一篇线性的指导：如果你想成为一名MIRI研究者，我推荐你首先确保自己了解必须的基本知识，然后去深度了解一个自己最感兴趣的话题即可。当你可以很好地了解这些内容，你就可以尝试在IAFF上参与讨论了。

---

# 2. 基础信息 #

在开始研究之前，掌握一些基本的数学概念是非常重要的。对运算、逻辑、概率论的了解对相关的研究很有用处。以下是一些帮助你入门的学习资料。

你不必按顺序学完以下书籍。随便拿起一本在你看来比较有趣的，并按你的喜好学习吧。

## 集合论 ##

大部分的现代数学都在集合论中得到形式化的描述，列在这里的其他教材和论文也不例外。所以从集合论开始是很ok的。  
**[Naive Set Theory](https://www.amazon.com/gp/product/1614271313?pldnSite=1)**

## 可计算性和逻辑 ##

可计算性理论（以及对角化带来的限制（参见形式语言与自动机））涉及了机器的能力范围的知识。  
**[Computability and Logic](http://smile.amazon.com/Computability-Logic-George-S-Boolos/dp/0521701465/)**
(1-18章)

## 概率论 ##

概率论对理解智能体至关重要。关于如何在不确定的环境下决策的知识在我们所有的研究领域都大有用处。  
**[Probablity Theory: the Logic of Science](http://smile.amazon.com/Probability-Theory-The-Logic-Science/dp/0521592712/)**

## 概率推理 ##

这本书能帮助你了解在概率化的世界模型中如何进行推理。  
**[Probablistic Reasoning in Intelligent Systems](http://smile.amazon.com/Probabilistic-Reasoning-Intelligent-Systems-Representation/dp/1558604790/)**

## 人工智能 ##

我们的研究主要关注关于智能的基本数学理论，但是对现代AI领域的现状有所了解可以让我们的工作更加接地气。  
**[Artificial intelligence: A Modern Approach](http://www.amazon.com/Artificial-Intelligence-Modern-Approach-Edition/dp/0136042597)**

VNM 理性的概念也是很重要的，我推荐从[这篇维基文章](http://en.wikipedia.org/wiki/Von_Neumann%E2%80%93Morgenstern_utility_theorem)中学习，也可以阅读[原始书籍](http://smile.amazon.com/Economic-Behavior-Anniversary-Commemorative-Princeton-ebook/dp/B00AMAZL4I/)。冯诺依曼和摩根斯坦展示了任何遵守一些简单而自洽的公理的智能体，可以被一个效用函数表示。虽然有的人认为为了构造可靠的人工智能体我们必须抛弃VNM理性，但是这仍然是最能描述任意强大的智能体的行为的框架。（参见Bostrom的[超智能之愿（The Superintelligent Will）](http://www.nickbostrom.com/superintelligentwill.pdf)一书中的*正交性命题*和*Instrumental Convergence thesis*（基本上就是说，看起来有着无害目标的智能体可能在实现该目标的过程中做出很夸张的有害行为 --译注））这个概念在我们的研究中被广泛使用。



---

# 3. 现实建模 #

---

# 4. 决策论 #

---

# 5. 逻辑不确定性 #

---

# 6. Vingean Reflection #

---

# 7. 可矫正性 #

---

# 8. 价值学习 #

---

# 9. 其他工具 #

---

# 10. 了解我们的使命 #

---


*post under construction*