## Chapter 38、How to decide whether to include inconsistent data

**如何决定是否包含不一致的数据**

假设你想学习预测纽约的房价。给定房屋的大小（输入特征x），你想预测其价格（目标标签y）。

纽约的房价非常高。假设你有位于密西根州底特律的第二个房价数据集，该地房价要低的多。你应该在训练集中包含这些数据么？

给定相同的大小x，房子的价格根据其是在纽约还是底特律而大相径庭。如果你只关心预测纽约的房价，那么将两个数据集放在一起将损害你的表现。在这种情况下，最好忽略不一致的底特律数据【3】。

纽约vs底特律的例子和移动app vs互联网猫图的例子相比有什么区别？

猫图例子不同，因为给定输入图片x，它可以可靠的预测标签y表明是否有猫，甚至不需要知道图片是来自互联网还是移动app。即，有一个从输入x可靠地映射到目标输出y的函数f(x)，甚至不需要知道x的来源。因此，从互联网图片中识别的任务和从移动app图片中识别的任务是“一致的”。这意味着包含所有的图片几乎没有缺点（除了计算开销），并有可能有一些显著优点。相反，纽约和密西根州底特律的数据并不一致。给定相同的x（房子的大小），价格根据房子的所在地差别很大。

————————

【3】有一种方法可以解决底特律数据和纽约数据不一致的问题，就是给每个训练样例添加额外的特征来表征城市。给定输入x（现在指定城市），目标值y现在是明确的。然而，实际中这种方法不常见。

