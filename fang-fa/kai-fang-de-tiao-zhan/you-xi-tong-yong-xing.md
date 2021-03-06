# 游戏通用性

能够解决一个问题并不能让你变得聪明；没有人会说Deep Blue或AlphaGo拥有一般智力，因为他们甚至不能玩跳棋\(没有再训练\)，更不用说煮咖啡或系鞋带了。要学习一般的智能行为，你不仅要训练一项任务，还要训练许多不同的任务。视频游戏被认为是学习一般情报的理想环境，部分原因是因为有很多视频游戏共享共同的界面和奖励惯例。然而，视频游戏中的深度学习的绝大多数工作集中在学习玩单一游戏，甚至在单一游戏中执行单一任务。

虽然深度基于RL的方法可以学习玩各种不同的Atari游戏，但是开发可以学习玩任何类型游戏的算法（例如Atari游戏，DOOM和星际争霸）仍然是一项重大挑战。对于特定类型的游戏，仍然需要花费大量精力来设计网络架构和奖励功能。

玩多个游戏的问题的进展包括Progressive neural networks，这允许学习新游戏（不会忘记以前学过的游戏）并通过横向连接利用先前学习的特征来更快地解决。但是，它们需要为每项任务分别设计网络。Elastic weight consolidation可以顺序地捕捉多个Atari游戏，并通过保护权重不被修改来避免灾难性遗忘，这对以前学过的游戏很重要。在PathNet中，进化算法用于选择神经网络的哪些部分用于学习新任务，展示ALE游戏的一些迁移学习性能。

在未来，将这些方法扩展到允许玩多个游戏是很重要的，即使这些游戏非常不同 - 大多数当前的方法都集中在ALE框架中的不同（已知）游戏上。这种研究的一个合适途径是Learning Track of the GVGAI竞赛。与ALE不同，GVGAI有一套潜在的无限游戏。 GVGAI最近的工作表明，无模型深度RL不仅适用于个人游戏，甚至适用于个人层面; 这在训练期间不断产生新的水平被抵消了。

多游戏问题的重大进展可能来自外部深度学习。 特别是，最近的Tangled Graph表示，一种遗传编程形式，在这项任务中显示出了希望。最近的IMPALA算法试图通过大规模缩放来解决多游戏学习问题，并取得了一些有希望的结果。

