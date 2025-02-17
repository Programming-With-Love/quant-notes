# 强推！这可能是B站最全的【Python金融分析+量化交易】系列课程了，计算机博士精细讲解，底层原理+项目实战，看完即可就业！人工智能／深度学习／机器学习 - P40：40.因子分析概述 - 口喜口合口合y - BV1su4m1u7TS

这节课咱们来说一下因子分析啊，今天大家解释一下我们要分析的一个目标，好比说现在这样，我们拿到了A股票当中很多的一些因子数据，那比如说啊，咱们现在啊，就是每个股票都能取出来各种各样指标吧。

那指标随便列两个，比如大家常见的一些基本面信息，我写个A还有一些技术指标的水也可以啊，那这一块如果说咱再往下去画，那我们因子能分成好多大类吧，有很多大类的因子，然后呢每个每个大类因子。

比如说基本面当中的，那你还能再细分吧，再细分个123点点点，一直好多好多个吧，各种各样指标，那问题来了，那比如现在你手里啊，你能拿到有这么300个指标，或者说你手里现在有300个因子。

那你说这300因子啊，一会儿当我要做一些回测的时候，或者说我要设计策略的时候，咱们是都用呢，还是用部分几个呀，我们是不是得做这样一件事，判断一下什么样的一个因子，诶是我想要的什么因子，是我不想要的。

换句话来说，哎现在300个因子我们给它放到这了，要干什么，我说给他们做一个排序吧，按照他们的一个成绩，什么叫做一个成绩呢，哎比如因此我说按他呀，对我最终的一个收益的影响，我说给打分吧，有打98分的意味。

这因子挺好的，有打九十七九十6951兆零分是吧，把这些因子从上到下。

![](img/edd1d5375d2d691a6d2e3c5c883b5a41_1.png)

我能不能排一个序啊，好像来说能，因为每个因子对最终结果影响是不一样的吧，那现在我们就要做这样一件事啊，看一看什么样的因子才是好的，那怎么看才是好的呢，其实最简单有几种方法。

在这里给大家介绍两种最基本的方法是什么，看我们的一个收益率，哎既然咱提到收益率啊，咱来解释解释什么叫收益率，你看我这边写了收益率，它是这样一件事啊，就是这个这些知识点大家简单的学习啊，都不用去记。

我觉得都很简单，也没有列公式啊，收益率这样，那比如咱们现在呃当你去统计的时候，你说你按月统计也行，按五天按一天也行，咱俩一天举例子，比如你现在你想看每天的收益率，那等于什么，当天的一个诶收盘价减去啊。

上一期就是上个交易日吧，它的一个收盘价再比上上一个交易日，它的一个收盘价叫做什么，我们当前这一天啊，我们的一个收益率，那其实呢是要这样一件事，那你说股票也挣钱诶，是不是说我要积少成多呀。

每一天都想去挣吧，那好了，我说看一下哎呦，我这个因子啊它也在变，我的收益率呢它也在变，我想看一看因子和收益率，我们现在不是有好多添加指标吗，比如这样，现在呢我说我连续啊取了这么一年。

一年可能有取到了250天吧，250天当中你有这个，因此我写一个F，还有一个收益率，你写一个二，是不是他俩之间会有很多对应的一个值啊，每天都在变化吧，我们需要看什么，哎呦，这个因子它的一个走势跟我收益率。

它的一个走势怎么样，有什么样的一个关系呢，你是一个建议性的呀，还是一个就是相关的，还是个不相关啊，如果相关的时候诶，你跟我这个相关宠物怎么样，是正的还是负的呀，咱要把这些指标拿出来吧。



![](img/edd1d5375d2d691a6d2e3c5c883b5a41_3.png)

其实说白了我们要对因子就是做这样一个分析，分析当中啊，咱们要做两件事，第一件事就是一个因子的C分析，什么叫C啊，呃呃先给大家解释什么叫IC，IC这样一件事其实很简单，他算的是一个相关性的指标啊。

你看这块我也写了一会儿，我们也要去做的计算什么来计算一个IC值，IC只是这样，他说啊计算一下因子啊，我们的因子就是你选择，比如咱们一会儿会选一个P指标是吧，拿某个指标诶，跟这个收益率我直接算一个相关性。

虽然这个相关性啊是一个斯皮尔曼相关系数啊，这个大家简单这个行啊，然后它的取值范围是一到正一，越近于正一的那月正相关越近于一的，负相关越近于零的表示没什么关系啊，这样一件事，要素因子和我们收益率之间。

这样一个相关相关性，然后呢，我们也可以把这件事叫做一个单因子分析，哎，为什么要单因子分析啊，比如现在我这个选项指标当中有300个，那收益率收益率相对来说是固定的吧，那每天什么样就是这个收益率吧，好了。

那收益率在相对固定的前提下，我是不是得看一下每一个因子，来跟我说一堆关系，第一个因子跟收益率的关系，第二个因子，第三个一直到第300个吧，所以给我们的感觉啊，一会儿唉我们可能会做一个for循环。

是不是在这个for循环当中。

![](img/edd1d5375d2d691a6d2e3c5c883b5a41_5.png)

要去便利每一个因子跟收益率啊，之间的一个关系，计算它们之间的一个A4平面进化系数，就行了啊，然后呢这个是不是要去计算诶。



![](img/edd1d5375d2d691a6d2e3c5c883b5a41_7.png)

那计算结果叫什么，因此和收益率之间的这个斯皮尔曼相关系数，我们计算出来的结果就把它叫做一个C值了啊，这就是它的一个缩写叫AC值，然后呢咱们来想吧，那你说你计算出这个C值之后。

我是不是得看一看它的C值的一个大小啊。

![](img/edd1d5375d2d691a6d2e3c5c883b5a41_9.png)

那下面我们还要做一个分析的操作，在这里呢，比如说啊，左边这个就是我们一会儿要去做的一个结果，那这里是统计了每一天，然后他的一个IC值，然后它的一个变化情况，然后右边这张图呢就是呃蓝色这条线他画的。

你看这块写的比较少，就是画了几个月的时间，蓝色这个就是它的IC值，然后它的一个就它的一个那个折线图啊，统计出来了，然后绿色的就是它的一个均线图啊，均线图当相当于就是呃你不是一天一天的。

你可以是十天的统计一个值，十天统计一个值，因为你看前面还有一个空值吧，相当于这个是个窗口统计均值，这个在一个窗口。



![](img/edd1d5375d2d691a6d2e3c5c883b5a41_11.png)

在一个窗口统一均值，诶，这是一个均线啊，这里给大家看了一下。

![](img/edd1d5375d2d691a6d2e3c5c883b5a41_13.png)

就是一会儿啊我们要做的几个指标，大家先不用去管啊，这些数字这些东西我们一会怎么去做，一会儿代码当转，咱给大家慢慢去说啊，怎么样画这个图，以及怎样把这个结果给它呈现出来，然后呢你看这个技术当中啊。

它是什么，是不是有一些正负值啊，唉像我刚才说的，我们有一个取值范围吧，一到正一之间我们要找啊，看一看哪些因子跟生育之间关系越大，关系越大的，我来挖掘一下他跟我什么关系，是不是说这件事做得越值得呀。

那跟我的没什么关系的，或者说你这个这个东西反而会影响我的。

![](img/edd1d5375d2d691a6d2e3c5c883b5a41_15.png)

是不是干脆咱不管就行了啊。