## RS04 Thinking
**1.  高德地图中的路径规划原理是怎样的？**

答：1）建模：将路口设置成节点，两个节点间如果可达则添加一条边，边的权重为两节点间通行时间（通过雷达测试实时流速计算得到），边与节点构成图；2）利用Dijkstra/Floyd算法进行路径规划

**2. football.gml数据集中，美国大学生足球联赛，包括115支球队，被分为12个联盟。为什么使用LPA标签传播进行社区发现，只发现了11个社区？**

答：由于比赛机制是联盟内部的球队进行小组赛,然后是联盟之间比赛，因此不仅同一联盟间存在边，不同联盟的球队之间也存在边，使用LPA标签传播进行社区发现时，节点向邻居节点传播自己的标签，其最终发现的社区只是通过挖掘队伍间比赛的行为得到的，与静态的联盟不一样。

**3.  微博采用了类似FaceBook的EdgeRank算法，如果你给微博的信息流做设计，你会如何设计？**

答：将通过粉丝亲密度（互动情况）、内容质量原创度、新鲜度等来计算得到权重，再对权重进行排序，按权重从高到低推荐内容给用户。