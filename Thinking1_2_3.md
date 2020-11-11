## 什么是Graph Embedding，都有哪些算法模型
主要是两种：DeepWalk和Node2Vec
* deepwalk是random walk 和skip-gram的组合。
* random walk的指的是从某个特定的端点开始，游走的每一步都从与当前节点相连的边中随机选择一条，沿着选定的边移动到下一个顶点，不断重复这个过程。
* skip-gram指的是给一个词，预测两边的词的相似度

* Node2Vec是在DeepWalk基础上进行改进，可以控制进行BFS，DFS随机游走（带偏置的random walk策略）
* BFS，广度优先，倾向于在初始节点的周围游走，反映出一个节点的邻居的微观特性
* DFS，深度优先，倾向于跑得离初始节点越来越远，反映出一个节点邻居的宏观特性

## 如何使用Graph Embedding在推荐系统，比如NetFlix 电影推荐，请说明简要的思路
* 可以把用户做收藏，购买电影这些行为，基于某些时间段的session，做成一个的图,并进行embedding
* 用Node2Vec去做，结合BFS, DFS的不同超参数，得到不同的模型，并依据实际的效果进行调整。
* 比如说，对某个用户群体做BFS的模型，对另外一些用户群体做DFS


## 数据探索EDA都有哪些常用的方法和工具
* 主要是分成整体情况，缺失值，数据分布这几种。
* 整体情况常用的是：head, describe, profiling
* 缺失值：isnull, heatmap
* 数据分布：正态norm, min, max, mean

