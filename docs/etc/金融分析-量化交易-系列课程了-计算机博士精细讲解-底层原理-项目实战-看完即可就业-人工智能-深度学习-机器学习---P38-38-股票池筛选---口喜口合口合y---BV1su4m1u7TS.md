# 强推！这可能是B站最全的【Python金融分析+量化交易】系列课程了，计算机博士精细讲解，底层原理+项目实战，看完即可就业！人工智能／深度学习／机器学习 - P38：38.股票池筛选 - 口喜口合口合y - BV1su4m1u7TS

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_0.png)

好了，那咱们现在就是这个中性化操作，我们也写完了，在这里回头来看一下吧。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_2.png)

现在我们是不是在这块儿就可以去执行诶，咱们刚才写那几个操作了。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_4.png)

好了一个来执行吧，啊在在在这里啊。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_6.png)

改写了预处理操作，预处理操作当中，咱们来写第一个，第一个就是咱们去啊做一个3C格玛，30码当中啊，我们要传进来什么，哎对谁做呀，哎对我的设子做还是对有因子做啊，做因子做吧，好了，把我们的因子拿到手呃。



![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_8.png)

这里边这里边的一个结果还没有返回值，我给他个返回值吧，在这块哦，我说咱们现在得到一个返回值，把它复制过来，把它复制过来，FMAL呃，fundamental当中它指定一个名字吧，Fundamental。

然后做data frame就行了，然后在这个data frame当中就有我们需要的啊，我们想要的这个指标了，好了，把它拿过来fundamental，然后对其中谁操作呀，是不是咱们之前写好的。

我们当前的一个试镜，试镜这个东西好了，把它传进来，然后这样咱们做的第一步就是我的一个哦，去我们这个离群值。



![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_10.png)

去完离群值之后啊，然后咱们写一下吧，就是现在呃现在我这个指标就是没有什么。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_12.png)

没有我的一个极值了。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_14.png)

咱们现在做了一个没有极值的，做完没有进去之后还没完，我们还得再做什么。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_16.png)

是不是说再做下一个操作，做一个标准化的一个操作呀，好了。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_18.png)

把咱们当前这个结果传进去，下面我做了一个标准化的操作，相当于呃相当于一个标准化的操作。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_20.png)

就是这个东西吧。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_22.png)

直接把它拿过来，然后再点上一个DDER呃。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_24.png)

dd等于当前的结果行了，这是我做了一个标准化的操作。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_26.png)

做完咱们这个标准化操作之后，接下来还有什么，还有一个中性化操作吧，好了再给他复制过来。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_28.png)

在复制过来之后说哎呀他就叫这个名字得了，他就叫做预处理完之后杠这个东西。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_30.png)

然后等于咱的这个结果好了。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_32.png)

等于我们这个结果，然后把上面这个值再传进来，是不是就可以了，那现在我们就完成了。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_34.png)

咱们所需要的所有的预处理操作了，那接下来呢那接下来是不是说我现在啊哎呦。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_36.png)

我要对这个因子做一些筛选了好了，咱们来指定一下哦，对因子啊，不是对因子基于因子啊，对池子，对咱们的股票池子做做一个筛选。



![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_38.png)

或者做一个调仓，做筛选吧，做一个筛选操作，筛选操作，咱们想一想怎么去做啊，是不是这里哎你得给我指定一个指标啊，比如说我这个QQ当中呢啊，你说是小于这个因子是小点好还是大点好啊，咱们之前不是说小点好吗。

所以说我对当下这个指标我看一下吧，他的呃比如说从小到大就是20%的时候，它是等于多少，就是我们希望选出来前20%最小的，可以吧，还在这里我们来指定一下，切一下吧，咱们来选多少个，那我就选这么呃0。

2个吧。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_40.png)

相当于选了20%，然后呢这里这是我做了一个因子策略，然后接下来接下来是不是说我要去选股了，那好了，现在我们要选股，在这个选股过程当中，我需要再怎么样，我们看一下当前当前我得到这个结果。

这个是我的一个因子。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_42.png)

对我的因子当中，我要做一个所有的股票当中都有这个因子是吧，那所以说我现在可以做判断吧，做一个筛选吧，在这里哎我说现在啊如果说啊它的一些值啊，如果说他的指标怎么样。



![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_44.png)

没有满足我的要求，没有满足什么，咱刚才不是说了吗。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_46.png)

我们自己来指定一个范围，通常就是我们这个市净率啊，我希望它不是小一点的时候，能怎么样能使得咱的一个收益，或者说我们的期望收益吧可能会更大一点吧。



![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_48.png)

就这里哎咱们说小于等于一个零，小于等于一个20%那个值啊。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_50.png)

是不是就行了，我们现在先来选小一点的那一些。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_52.png)

然后呢我需要把这些股票找到手，点点death一下，这是不是呃。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_54.png)

这个东西判断是基于值去判断的，均值判断完之后，咱们现在相当于传进来索引。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_56.png)

我得到什么所有的股票吧，好了，那这这这这是什么股票，这是不是说我这是我现在想要的这个股票。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_58.png)

判断完的，我想要的这批股票好了。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_60.png)

我们拿到这个股票呃，一会儿咱要对这个股票做一些做一些交易操作。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_62.png)

我们先把它传到这个context当中，contest当中呃，stock list等于一下我当前的一个结果啊，这块不改了，直接把它传过来就行好了。



![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_64.png)

这是我们现在有了一个stylist，然后接下来呢就是我们要干什么。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_66.png)

我们要执行一些调仓，还有买进买出的一些操作了哦，在这里就是我们要做买进买出啊，那你是不是说你得知道哎呀买什么。



![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_68.png)

或者说你把哪些要删除出去啊。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_70.png)

然后剩下的是在股票池子当中去选吧，那首先我得看一看一会儿啊。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_72.png)

有哪些不在这个池子，我得写一下啊，删掉删掉不在当前啊。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_74.png)

当前那个因此选中的池子中的股票啊。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_76.png)

咱们要做一个删除，删除怎么写呢，来写一下吧，呃删除我是不是得把这些股票啊给它删一下。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_78.png)

删完之后呢，我也知道你删了什么东西啊，好了，这是一个返回值，返回值啊，当中就包括了所有我要删的，那来想一想吧，哪些诶是我要去删的。



![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_80.png)

那肯定是之前咱有的啊，并且跟我当前池子是不一样的，这个是我当前的我的一个池子吧。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_82.png)

好了，我把它复制过来，这是我当前的一个池子，我先给它括号括起来，那我们要看的那肯定就是哎呀，现在手里有的股票跟我们当前池子那不一样的，我有一个操作呃。



![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_84.png)

Df f r e c，操作好了，这是对谁啊。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_86.png)

我手里有的这些啊，那好了。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_88.png)

手里有呃，咱们还在写一下，就是拿到拿到手里。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_90.png)

有的拿到手里，有的咱们也指定一下，在这个context当中把这个不用复制上面的。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_92.png)

咱这也有在这个context当中，我们要找谁呀，是不是找我们现在哎，我的一些账户的一些信息啊，在账户信息当中我要看什么，我持有什么东西吧，position诶，没有啊，这是position，找一下呃。

看一下，在我只有这是一个IO是吧。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_94.png)

哎没什么问题啊，他怎么没有这个东西啊，position咱试一下吧，一会儿看一看这个API有没有问题，有问题的改，我记住他是一个positions，好了，这是我现在手里用的吧，咱现在拿到手啊。



![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_96.png)

然后是这个名字，这个就是我的一个context点儿啊，咱们最后一次手里有的啊，咱指定一下，我们最后一次手里有的这些个股票吧，就叫做这个股票得了好了，然后呢，我是不用现在手里有这个东西啊。

跟我当前池子的诶，跟我当前这个池子的做一个判断，判断完之后，difference什么意思啊，那就是说当前你手里有这些股票，不在你池子里边的，哎这是difference吧，咱把这些股票给他拿到手吧。



![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_98.png)

啊是这个意思，然后这个这个我把这个前面就得给他复制一下。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_100.png)

好了就完事了，这个就是咱们当前啊完成了一件事。

![](img/af313b2aa1cc8d68b5a7ea4a7ef4b159_102.png)

好了，来点set一下吧。