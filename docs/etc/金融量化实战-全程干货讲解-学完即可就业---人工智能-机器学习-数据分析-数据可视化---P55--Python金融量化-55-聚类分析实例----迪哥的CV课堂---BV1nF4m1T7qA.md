# 比刷剧还爽！公认最全的Python金融分析与量化交易实战教程，从编程基础到金融量化实战，全程干货讲解，学完即可就业！——人工智能／机器学习／数据分析／数据可视化 - P55：【Python金融量化】55-聚类分析实例( - 迪哥的CV课堂 - BV1nF4m1T7qA

好这节课咱们来看一下聚类啊，还有统计的策略方法，我们在Python当中啊，咱们该怎么样去做。

![](img/f84608097431785e9c4b2b6a11cd51e5_1.png)

首先呢还是第一步，先把咱们这个工具包全部的给导进来，跟咱们之前一样。

![](img/f84608097431785e9c4b2b6a11cd51e5_3.png)

工具包还是没有发生任何变化的，然后第二步呢就是导入啊，咱们现在要用的这份数据，上节课咱们是不是跟大家说过了，哎对这个数据我们要提取出来一些特征吧。



![](img/f84608097431785e9c4b2b6a11cd51e5_5.png)

这块呢我们选了两个特征啊，就是前一天啊他这个指标，还有前两天他这个指标这两个信息啊，是一会儿我们要建模的时候用到的啊，两个具体的指标，然后接下来有了指标之后。



![](img/f84608097431785e9c4b2b6a11cd51e5_7.png)

我们就可以做一些建模的事情了吧，这次咱们做的任务跟之前不太一样。

![](img/f84608097431785e9c4b2b6a11cd51e5_9.png)

之前呢我们是用一些回归的方法去做，这回咱们拿聚类的方法来去做，首先第一步咱们在这个sk learn当中，唉，这咱们不说了，做一些建模方法最好用的包啊，就是这个sk learn了。

然后这回我们选的模块跟之前不太一样，之前是回归，这回呢我们用聚类，这当中有一个算法叫做k means啊，咱们之前给大家讲了，k means建模的一个基本方法好了。



![](img/f84608097431785e9c4b2b6a11cd51e5_11.png)

这是第一步，先把我的一个模块给导进来哦。

![](img/f84608097431785e9c4b2b6a11cd51e5_13.png)

上面没执行，重新的都执行一下啊，导进一下我们的模块，然后接下来我执行这样一个k means的操作，在这里啊，我说我建立一个模型，这个模型就是k means，然后这里边需要我们指定一个参数。

就是呃我们要建立有这么多少个醋吧啊，一个cluster，Cluster，这里啊我们需要自己指定一下，也就是一个K值，咱们这个任务当中啊比较简单，我是不是说呀我想去判断一下嗯，什么时候涨了。

什么时候跌了吧，那也就是说两个结果，一个一，一个一说就行了好了，我说指令二去构成这么两个醋就行了。

![](img/f84608097431785e9c4b2b6a11cd51e5_15.png)

然后呢咱们来执行一下吧，哦我看这里哦。

![](img/f84608097431785e9c4b2b6a11cd51e5_17.png)

N clutter，我看这里哦，少一个S是吧，再执行一下，这样呢咱完成了一个建模的操作啊，不是建模，就是一个模型实例化操作，然后呢对我的model我说点feat一下。



![](img/f84608097431785e9c4b2b6a11cd51e5_19.png)

把咱们的实际数据啊传进去，实际数据啊，之前我说这里有一个data啊。

![](img/f84608097431785e9c4b2b6a11cd51e5_21.png)

我们的数据data当中呢我们要选择其中的某些列。

![](img/f84608097431785e9c4b2b6a11cd51e5_23.png)

这列名咱之前是不是也做好了好了，把这些列传进去。

![](img/f84608097431785e9c4b2b6a11cd51e5_25.png)

我们进行一个模型的建立就完事了，这里显示出来了，就是当我们建模时会用到的一些参数，这些参数当中都有一些初始值，比如说呃我的一个就是两个类别，中心点初始化的一个方法，然后最大的一个叠加次数。

然后要锯成几个对，然后呢就是我这个模型会重复执行多少次呃，重复执行多少次，这样就直接给大家演示k means当中啊，不是每一次结果都是不一样嘛，所以说当我们用聚类建模的时候啊。

它不是建模一次就给你返回的结果，它是建模的十次，看这十次诶，整体的一个结果把你返回每一个点，它的一个到底属于哪个醋这样的归属，这个就是有些参数啊，大家如果说想想去看啊，在sk learn当中。

官方官方文档里面，都会有这样一个详细的介绍的，然后呢接下来我说都有这个模型啊，我建完之后，然后呢我要去预测一下当前咱们这批数据点啊，它都是呃预测结果都是什么，或者说得到一个零。

还是一个一代表着它属于哪一个错，在这块电脑当中，我说指定一个新的店名吧，就叫做当前啊，我的错，它的一个归属就行了，cluster行了，然后我们来执行一下吧，看一下当前的一个效果。



![](img/f84608097431785e9c4b2b6a11cd51e5_27.png)

执行完之后，我们的数据当中已经有了这个错啊，这也这样，我把这个结果再稍微改一改，因为你看啊，就是当前我点开完之后。



![](img/f84608097431785e9c4b2b6a11cd51e5_29.png)

这里边它是一个零一吧，可能咱们要的并不是一个零一，而是什么，而是一个一和一个一吧，所以这里我说我给他稍微改一改啊，安排点位一下，数据当中呢就传入我们当前的一个预测结果，对预测结果做一个判断。

如果说它是一的时候，然后呢我说把一这个堆，然后当做一个一吧，然后把零那个对哎当做一个一啊，相当于判断了两个墩儿啊，这里我们对数据稍微改一改。



![](img/f84608097431785e9c4b2b6a11cd51e5_31.png)

名字不用去变了，还是这个名字就行，然后来执行一下吧，这回数据当中啊，就是我们想要的一个结果了，比如这里你可以去给大家好。



![](img/f84608097431785e9c4b2b6a11cd51e5_33.png)

打开来看一看，你看这里面是什么，就是一个一还有一了，这个结果我们现在已经有了吧，好了有了一个一，还有一个一，之后，接下来我是不是可以对我的一个数据，来给大家画个图吧，看一看咱这两都是长什么样子吧。

画一个三点图，在这个三点图当中啊，咱们来指定一下，第一个就是我的一个data，我先把这个数据啊给它传进去啊，这个是我们当前的一个数据，哎呀这个数据当中，我三点图里边得指定这个X轴，还有Y轴。

我得重新画一下，先画这个X轴数据吧，然后取所有的数据样本点冒号取所有吧，然后呢啊第一个维度当做一个X轴行了，然后第二维度我当做一个Y轴，这是第一个维度，然后这里我说改成第二个维度是不是就行了。

然后呢我说用呃不同的颜色吧，然后来表示这不同的一个错，我说指定一个CC当中呢，嗯它是什么呢，C是这个就是我们刚创建好的哎，它的一个到底它是一个一还是一个一，来进行一个展示。

然后接下来我说我选择一个呃颜色就行，选择颜色，那就是从浅到深的吧，从浅到深，其实说白了就是一个红色和一个蓝色，call棒一下看一下吧。



![](img/f84608097431785e9c4b2b6a11cd51e5_35.png)

这里他就把这个图画出来了，其中蓝色是一个醋诶，这个红色它是另外一个醋啊，这里咱们两个类别是不是已经划分好了呀，其实大家可以来看一下，在这个组当中啊，你看啊，如果说它是在负值的时候，就是昨天也跌。

前天也跌，那可能大概率今天也跌吧。

![](img/f84608097431785e9c4b2b6a11cd51e5_37.png)

可能是有这样一个趋势啊，这个是我拿了两个醋，但是现在问题来了。

![](img/f84608097431785e9c4b2b6a11cd51e5_39.png)

那你说现在啊你做这样一件事儿，那它能靠谱吗，你看这里哎，你就说这个东西一个是一个E，一个是一个一。

![](img/f84608097431785e9c4b2b6a11cd51e5_41.png)

你直接这么说，它能靠谱吗，其实啊这个策略我从这个剧类角度来说啊。

![](img/f84608097431785e9c4b2b6a11cd51e5_43.png)

用的不是特别多啊。

![](img/f84608097431785e9c4b2b6a11cd51e5_45.png)

所以说啊今天这个任务，大家只需要简单熟悉一下聚类诶，咱们是怎么去做的。

![](img/f84608097431785e9c4b2b6a11cd51e5_47.png)

以及呢在这个句子当中，咱们得到什么样的一个结果就行了，实际当中啊可能距离效果啊，它的一个效率来说吧，并不是特别好啊，试一下吧，在咱们这个任务当中，然后returns之前乘上一个看不returns名字啊。



![](img/f84608097431785e9c4b2b6a11cd51e5_49.png)

是没写错，returns给拿过来。

![](img/f84608097431785e9c4b2b6a11cd51e5_51.png)

看一下咱这个聚类能使得咱们赚多少钱吧，这里算了一下咱们能挣多少钱，然后指定一下吧，指定一下，我们得到了一个新的列名，这个列名呢就叫做我们的一个clutter，然后他的一个returns吧。

然后我们来看一下执行一下，执行完之后咱就可以哦，这个数据还没还原，咱得把这个数据啊，之前不是做了个对数吗，现在我们给它还原一下呃，重新还原一下，把这个列还原回去，要对比哪两个指标来着。

第一个是一个returns啊，原始的第二个呢，就是一个咱们聚类得到的一个结果，对于他，然后说点sum下，扫完之后呢，我说点apply一下，咱们的一个南派点EXP数就行了。



![](img/f84608097431785e9c4b2b6a11cd51e5_53.png)

这回我们做一个还原，回了回去之后啊，再看结果吧，呃看起来这个效果不是特别好啊，你看第一次啊，就是当前啊，人家就是你啥都不做，你是亏了一点，做完剧烈之后，怎么好像亏的更多了呢。



![](img/f84608097431785e9c4b2b6a11cd51e5_55.png)

这也这样，可能就由于聚类当中有一些随机性。

![](img/f84608097431785e9c4b2b6a11cd51e5_57.png)

导致这样一个问题，这样我说我把这个东西给他restart一下，咱重新再执行一次。

![](img/f84608097431785e9c4b2b6a11cd51e5_59.png)

每次结果可能会不同啊，因为就业当中有一些随机性呃，这个当中还是一个0。6G，看起来效果反而不如之前了。



![](img/f84608097431785e9c4b2b6a11cd51e5_61.png)

是不是效果稍微的有这么一点点的下降啊。

![](img/f84608097431785e9c4b2b6a11cd51e5_63.png)

呃刚才忽略了一个问题哈，就是在这个句子当中，我们串算它的一个归属的时候，这两个点啊可能写的稍微有点反哦，应该什么应该是一个一和一个一。



![](img/f84608097431785e9c4b2b6a11cd51e5_65.png)

感觉会更靠谱一点吧，这样咱来重新执行一下啊，因为聚类来说这个结果不是特别可控啊。

![](img/f84608097431785e9c4b2b6a11cd51e5_67.png)

所以说咱们得到结果得多做一些尝试。

![](img/f84608097431785e9c4b2b6a11cd51e5_69.png)

你看刚才我是不是写反了，刚才这边写了一个一和一，那正常情况下应该是一和一吧。

![](img/f84608097431785e9c4b2b6a11cd51e5_71.png)

所以说现在啊当我们算完之后，哎我们的一个聚类，它的一个收益效果看起来还不错，是不是，这个只是给大家举个例子啊，在这个例子当中看起来收益还不错。



![](img/f84608097431785e9c4b2b6a11cd51e5_73.png)

但是实际当中啊，像我刚说的聚类这个东西啊，毕竟它是不靠谱的，并且当我们去评估去分析的时候，聚类很难去分析。



![](img/f84608097431785e9c4b2b6a11cd51e5_75.png)

很难评估吧，因为我没有标签，没法做什么，没法像是一些传统经济的问题做一些分析。

![](img/f84608097431785e9c4b2b6a11cd51e5_77.png)

还有评估，还有看一看最终结果怎么样吧。

![](img/f84608097431785e9c4b2b6a11cd51e5_79.png)

这个是一个聚类啊，给大家讲具体原因，就是一旦给你逼到实在没招的时候。

![](img/f84608097431785e9c4b2b6a11cd51e5_81.png)

咱采用聚类啊，一般情况下我们并不使用这种方法。

![](img/f84608097431785e9c4b2b6a11cd51e5_83.png)