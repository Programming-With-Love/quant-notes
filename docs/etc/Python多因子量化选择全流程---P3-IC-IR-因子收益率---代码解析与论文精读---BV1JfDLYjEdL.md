# Python多因子量化选择全流程 - P3：IC／IR／因子收益率 - 代码解析与论文精读 - BV1JfDLYjEdL

哈喽各位小伙伴们大家好，今天我们来到多因子量化，选股与机器学习的第三讲，这一讲呢仍然是停留在最前面的那个，因子有效性分析的一部分啊，名字叫做ICIR与因子收益率的计算，嗯小伙伴们不要慌。

就是为什么还讲最开始的这些呃，因子的有效性检验呀，因子的预处理呀，因为这些东西是基础知识想要进入啊，想要写毕业论文或者是想要进入量化行业的，这些概念是必须要了解的，什么叫IC值，什么叫IR值。

什么叫因子收益率，做量化的必须要去懂的基础概念嗯，我们不能一口吃个大胖子，要一步一步来，所以今天就是讲第三讲啊，这个系列会非常漫长，那个后面也会定期的啊，为了防止大家比较烦躁。

后面也会定期更新一些其他的内容，嗯然后还是继续我们上次的内容，我们对这个因子的这个收益率，不是因因子的这个因子值，对它进行了一个预处理啊，因此中心化行业，中心化和呃是市值中心化进行了一些预处理。



![](img/966e948f1185fda56c90ff495049b7ec_1.png)

预处理完了之后，我们又进行了单调性检验。

![](img/966e948f1185fda56c90ff495049b7ec_3.png)

那今天第三讲，我们来讲三个概念，第一个是IIC值，IIC值其实就是呃，当前因子值和未来时刻收益率的相关系数，其实很简单，这个定义也很简单，但是如果不知道的，就真不知道。

就是其实就是当前因子值与未来时刻收益率的。

![](img/966e948f1185fda56c90ff495049b7ec_5.png)

呃那个相关系数，什么叫IR值呢，IR值呢就是这个因子的均值，与因子的标准差的比值，就是IR值，其实IR值其实就是就是由IIC值计算得到的，那还有一个值就比较具有迷惑性了。



![](img/966e948f1185fda56c90ff495049b7ec_7.png)

什么叫做因此收益率啊，因子收益率这边有有定义哈，因子收益率其实是权重系数，就是因子收益率在固定周期下，因因子的暴露值和下期收益率之间，构建横截面回归方程，得到的权重系数即为因子收益率值。

所以他其实啊构建了一个回归方程。

![](img/966e948f1185fda56c90ff495049b7ec_9.png)

回归方程里面的系数就是这个因子收益率值好。

![](img/966e948f1185fda56c90ff495049b7ec_11.png)

那话不多说，还是我们要啊看一下代码对吧，呃首先第一步呢就是把这个数据进行导入。

![](img/966e948f1185fda56c90ff495049b7ec_13.png)

导入这些因子呃。

![](img/966e948f1185fda56c90ff495049b7ec_15.png)

为什么选这么少呢，就是选这些因子啊，大家可以自己在各自的数据集上面进行计算啊。

![](img/966e948f1185fda56c90ff495049b7ec_17.png)

啊只是以这些因子值为例呃，以这些因子值为例呢。

![](img/966e948f1185fda56c90ff495049b7ec_19.png)

我们第一步要计算这个IC值，IC值其实就是横截面回归慢。

![](img/966e948f1185fda56c90ff495049b7ec_21.png)

我们要计算因子值，当前就是把每一个，因为每一个日期就会有一组因子值，和一组收益率值，所以我们对这个日期进行group by，我们每一个日期都计算当前因子值，X和收益率的一个回归系数。

correlation啊，其实核心就是这个代码，group by点data和play，然后X点correlation，和下一未来时刻的收益率的相关系数。



![](img/966e948f1185fda56c90ff495049b7ec_23.png)

就是IIC值，我们得到这个IIC值之后，我们先运行一下啊。

![](img/966e948f1185fda56c90ff495049b7ec_25.png)

看看是个什么结果，这个IC值我们打印一下哈。

![](img/966e948f1185fda56c90ff495049b7ec_27.png)

![](img/966e948f1185fda56c90ff495049b7ec_28.png)

![](img/966e948f1185fda56c90ff495049b7ec_29.png)

我们打印一下这个IC值，看到没有。

![](img/966e948f1185fda56c90ff495049b7ec_31.png)

这个IC值大家可以看一下哈，是每一个时刻，我们这个只选择的是2018年到，2017年到2018年，你看每一个时刻都有一组IC值，看这个这个因子的这个时刻的AC值，这个因子的这个时刻的AC值。

所以我们把每一个时刻的IC值算出来了。

![](img/966e948f1185fda56c90ff495049b7ec_33.png)

那么所有时刻的IC值的均值，就是这一列的均值除以这一列的标准差。

![](img/966e948f1185fda56c90ff495049b7ec_35.png)

就是这个IR值，额那额。

![](img/966e948f1185fda56c90ff495049b7ec_37.png)

接下来我们就开始这个IIC值算出来之后，那接下来我们就开始计算计算一个概率。

![](img/966e948f1185fda56c90ff495049b7ec_39.png)

看看我们要判断这个因子有没有效，看呢看看在这么多日期时期内。

![](img/966e948f1185fda56c90ff495049b7ec_41.png)

他这个因子的值大于0。03的这个概率。

![](img/966e948f1185fda56c90ff495049b7ec_43.png)

就是在这么多日期嗯。

![](img/966e948f1185fda56c90ff495049b7ec_45.png)

零我们以0。03为一个阈值，如果大于0。03，就证明它有效，就是其实就是计算因子有效率的一个方式。

![](img/966e948f1185fda56c90ff495049b7ec_47.png)

我们来做一个回归判断，他大概是不是大于0。03，如果大于0。03，就额好喷一下，然后除以这个除以这个总数。



![](img/966e948f1185fda56c90ff495049b7ec_49.png)

嗯然后看看这些因子。

![](img/966e948f1185fda56c90ff495049b7ec_51.png)

就是最后我们判断一下这个因子的有效概率是，0。91，0。75，0。16，看看这个视线率的有效，就是它大于0。03的概率非常低，就证明这个因子有效性很差。



![](img/966e948f1185fda56c90ff495049b7ec_53.png)

嗯那接下来我们就要计算这个因子收益率值，那因子收益率值，其实就是把因子值和未来的这个收益率值Y，进行一个回归，建立一个回归之后，我们取这个correlation，我们取这个呃呃系数，就是这个回归系数。

作为当前的这个呃因子收益率值。

![](img/966e948f1185fda56c90ff495049b7ec_55.png)

那每一个时刻都会有一个因子的系数。

![](img/966e948f1185fda56c90ff495049b7ec_57.png)

我们把这些系数相加，就可以得到总个总所有时刻的。

![](img/966e948f1185fda56c90ff495049b7ec_59.png)

因子收益率的一个均值。

![](img/966e948f1185fda56c90ff495049b7ec_61.png)

还要再除以一个N，还要再除以一个N，嗯就是就是因子收益率的均值。

![](img/966e948f1185fda56c90ff495049b7ec_63.png)

诶这里哦这里除不除不除温都一样，因为因为大家的时刻都一样，就是时间段都一样，所以这里就没有除N，其实应该除以一个N就是因子收益率的均值。



![](img/966e948f1185fda56c90ff495049b7ec_65.png)

然后这个除以100呢，就是把这个额因子收益率呢呃缩小。

![](img/966e948f1185fda56c90ff495049b7ec_67.png)

这个我为什么这么做，可能大家可能也不出一把也没事，所以我们最后得到了几组值哈。

![](img/966e948f1185fda56c90ff495049b7ec_69.png)

第一个是IIC的均值，就这么多时刻取平，就是每一列取平均，然后还有IIC的标准差，然后IIC的min除以IIC的标准差，就是IR值，然后我们还要计算这个因子的有效的概率，它在这么多时间内。

它的有效率有多少是0。91，这个就比有效率有效率就比较高，这个0。16有效率就比较低，这个0。83就有效率比较高，然后0。41有效率就比较低，所以我们可以根据这个因子的有效率，来进行因子的筛选啊。

还有这个因子收益率的均值呃。

![](img/966e948f1185fda56c90ff495049b7ec_71.png)

是是这么多，然后正的就是正的，就是当前因子值与未来收益率值的，相关系数是正的，那么如果是负的，就证明当前因子值余额，未来收益率的值信那个那个回归系数是负的，就是负相关，正值正相关啊，负值负相关。

所以很明显这个净资产收益率正相关，这个也是正相关，这是正相关，这是正相关，然后这个呃资产负债率就是负相关，他负债越多，它的未来收益率就越低。



![](img/966e948f1185fda56c90ff495049b7ec_73.png)

所以大概就是这个这个意思，那我们接下来就开始呃筛选，我们我们筛选出IIC的均值。

![](img/966e948f1185fda56c90ff495049b7ec_75.png)

大于0。03的这个因子，有这么多因子。

![](img/966e948f1185fda56c90ff495049b7ec_77.png)

然后并且进行了一个排序，进行一个排序。

![](img/966e948f1185fda56c90ff495049b7ec_79.png)

那接下来就是绘图了，绘图完之后呃，因子收益率的这个额均值是什么样的。

![](img/966e948f1185fda56c90ff495049b7ec_81.png)

然后因子的这个IR值是什么样的。

![](img/966e948f1185fda56c90ff495049b7ec_83.png)

还有因子的这个呃大于0。03，它的额排序就是因子收益率均值的排序。

![](img/966e948f1185fda56c90ff495049b7ec_85.png)

因此IR值的排序，因子呃，这个有效有效性的这个直方图。

![](img/966e948f1185fda56c90ff495049b7ec_87.png)

那额我们也可以绘制一下它的走势。

![](img/966e948f1185fda56c90ff495049b7ec_89.png)

就是类似于这种。

![](img/966e948f1185fda56c90ff495049b7ec_91.png)

我们也可以绘制一下走势，它每一个因子值的额，这个啊直方图它的一个直方图的一个分布，我们可以选一个0。03和负的0。03。



![](img/966e948f1185fda56c90ff495049b7ec_93.png)

反正我们可以设置一条阈值，然后根据这个阈值我们来筛选这个因子值啊。

![](img/966e948f1185fda56c90ff495049b7ec_95.png)

我们这个一阈值是0。03，根据这个0。03。

![](img/966e948f1185fda56c90ff495049b7ec_97.png)

我们把因子值额有效性的因子筛选出来。

![](img/966e948f1185fda56c90ff495049b7ec_99.png)

筛选出来之后，我们对他的这个因子收益率均值，因此IR值和这个有呃有比率。

![](img/966e948f1185fda56c90ff495049b7ec_101.png)

就是大于0。13的比率，做画了一个直方图。

![](img/966e948f1185fda56c90ff495049b7ec_103.png)

好额，今天就主要讲了三个概念。

![](img/966e948f1185fda56c90ff495049b7ec_105.png)

一个是什么叫IIC值，什么叫IR值，什么叫因子收益率值呃，如果如果说的话，IC值是某一个时刻，它的因子值和未来收益率值的一个相关系数，而IR值是整体进行衡量，就是在总过去一段时间内。

IIC的均值除以IS的标准差，它是衡量整体一段时间的一个，因子的有效性的情况，而因子收益率呢是呃，到底就是它的相关性相关系数是正的还是负的，嗯那么呃它的绝对值越大，就证明它的那个相关性就越高。

其实是建立了一个回归方程。

![](img/966e948f1185fda56c90ff495049b7ec_107.png)

用回归方程来代表这个因子的有效性，的一种评判方式。

![](img/966e948f1185fda56c90ff495049b7ec_109.png)

好今天我们就讲到这里呃。

![](img/966e948f1185fda56c90ff495049b7ec_111.png)

那个呃其实还是概念普及哈，嗯嗯后面还会继续再下，下节课再讲好，祝大家生活愉快。

![](img/966e948f1185fda56c90ff495049b7ec_113.png)