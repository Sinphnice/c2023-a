1.test:
- [x] 向isStepTerminate与evaluate_line中加入活四判定为必胜的情况。
- [ ] 路径选择机制：有利最短，不利最长。
- [ ] 单侧不可能成5的伪活3优化/单侧不能成5的伪眠3优化
- [ ] 冲4延伸
- [x] Range limit()可以考虑局部刷新，traverse多一个参数range
- [x] evaluate_line()增加终点限制，射线改为线段
- [ ] 将被剪枝的未定值节点的终止值与剩余搜索栈储存到哈希表中，避免相同局面的部分重复计算

2.gui:
- [x] 增加胜利判别
- [ ] 增加悔棋、提前结束选择gui
- [ ] 显示5连棋子，最新下的棋子，棋子顺序编号
- [ ] 调整棋盘

启发式搜索
- [x] 评估一个位置
- [x] 储存分值与排序
- [x] 出现对方下后己方必输的位置(活3 变 活4，双活3），只搜索这些必输位。

局部更新
- [x] 搜索范围限制
- [x] 启发式搜索中点的评估和排序
- [x] 全局估值

Bug:
- [x] 使用内存随棋数大量增加

置换表可能的问题原因：
- [ ] 随机数质量不足，Zobrist 哈希值存在冲突
- [ ] 储存到置换表中的分值可能不合理
- [ ] 导致末分支点激增的未知原因