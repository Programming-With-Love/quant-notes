# 完全可自学！人工智能金融领域知识图谱+Python金融分析与量化交易实战全套课程！入门真的超级简单！——机器学习／深度学习／NLP自然语言处理 - P53：02-2-Alphalens工具包介绍 - AI算法-漆漆 - BV1Wgz3YVEx1

然后一会儿啊我们在做的过程当中，哎不是在我们这个notebook当中去写啊，是在我们的平台当中啊，平台当中去写，一会给大家演示一下，在pi当中啊，咱们怎么写，因为这里啊咱想去拿一些指标，太麻烦了。

咱一会直接到平台当中去做，让我顺便把这个再再再介绍完，然后咱们就写代码，还有个东西要给大家介绍，就是叫做alpha learns啊，这个东西很好用啊，相当于就是接下来我们所有的计算的操作。

以及所有的画图操作啊，你省事了，你不用自己去做了，有现成的工具包帮我们去完成。

![](img/e3a9a0ecda760c560a4b173b2f02897f_1.png)

我们来点开看一下吧，点进去啊看一下，这个是它GITHUB的一个链接啊。

![](img/e3a9a0ecda760c560a4b173b2f02897f_3.png)

这个阿尔法learns，然后呢他就是专门啊去做这个因子分析的，但是它里边功能啊可能是比较多的，呃咱们这节课可能给大家讲一些最核心的，然后剩下其他的大家就是可以自己哎，按照自己的喜好了。

然后大家用这个工具包啊，就是第一步啊，你需要去先装一下，装这个工具包其实很简单，你看这它这个我这个链接给大家列出来了，一个是它的GITHUB的一个网址，一个是它的一个使用文档，在他GITHUB当中啊。

它会告诉你啊怎么去安装pip inststore，一下是就行了，打开你的any account permit里边pip install e一下啊，这就完事了，安装非常简单。

但是大家其实你也可以不用去装了，因为一会儿我们是用人家现成的平台，人家已经帮我们装好了，如果大家想在本地玩，那你自己也装一下，然后装完之后呢，我建议这样就是可以看一看它的一个使用文档。

然后他的一些给三跑建议大家看什么，你可以看一看，这里它有很多个小例子吧。

![](img/e3a9a0ecda760c560a4b173b2f02897f_5.png)

你点进去之后啊，这一块啊哦这块哦。

![](img/e3a9a0ecda760c560a4b173b2f02897f_7.png)

不不是这个不是这个咱不看这个，看这里看这块它得有一些examples，我找一找这块啊。

![](img/e3a9a0ecda760c560a4b173b2f02897f_9.png)

它有一些说明文档，在这些数据文档当中啊，它会有诶，不是这里在它的，我看看这个啊，ALICE当中有没有这个啊。



![](img/e3a9a0ecda760c560a4b173b2f02897f_11.png)

也三跑这里了，在这里它有一些呃写的还不错的一些示例文档，相当于啊就是教你一些诶最基本的使用方法，然后大家如果说你想看这些文档，来去简单去下也行，或者说一会听我讲也行，我这些东西哪来的。



![](img/e3a9a0ecda760c560a4b173b2f02897f_13.png)

基本上所有东西啊，都是参考人家的一个官方的小例子啊。

![](img/e3a9a0ecda760c560a4b173b2f02897f_15.png)

看一看他怎么去做的，然后我照着人家学一学，我该怎么给大家去讲啊，其实啊就是我觉着最好的学些东西，就是官方文档，还有一些官方的小例子，这里啊他介绍的比较详细，咱们内容啊相当于就是把它给你介绍的。

到时候都给大家去说啊，这些图什么意思，把他给你介绍这些所有东西啊，咱们给大家总结起来了啊，然后咱们一步一步照着去做，这里它有一个非常详细的小例子呃，我不给大家一个去读了，读的太花太太花时间了。

你想深入去学习，你可以去看一看他的一些具体的一些描述，如果说呢你想只哎只想去做咱们课程当中，要完成的任务，看我给大家准备的一个小例子，哎给大家准备的案例就行了，这个是他的一个文档里边教程还是不错的。



![](img/e3a9a0ecda760c560a4b173b2f02897f_17.png)

然后呢第二个还有使用文档，使用文档就是它的一些API说明了，点进去之后啊，你可以看一下，在这里诶它会有一些简单的介绍，然后下面还有一些呃就是基本的说明吧，到这里你想看他的一些各种各样的API。

其实我们主要的就用这几个，你想看的时候，这块有些说明啊，看他听他说也行。

![](img/e3a9a0ecda760c560a4b173b2f02897f_19.png)

然后一会听我说也行啊，这是人家的一个文档，然后大家用的时候啊，这是哎先把这个简单看一下就行，知道有一个叫alpha learns的东西，帮助我们去计算啊，我们要的比如说这个IC值，比如说我们要画这个图。

这个是一会儿啊，咱要用到的一个工具，然后介绍另一个呃，还有个工具啊，在这里在这个呃，这个就是进入到我们pi当中了吧，在这个片段当中啊，咱之前哎是不是说我们去新建一个策略，然后我们去跑一下回测呀。

哦今天咱们先不用跑回测，因为我们现在要干什么，对我们数据哎做一些分析，对我们数据做一些处理的操作吧，所以这里啊咱们来看这块啊，有这个有叫做一个投资研究啊，就是左在左边的时候啊，有一个东西叫投资研究。

再来点一下，就是进入到你的策略当中，然后这块有投资研究，咱不好回测了，所以说点进来点开一下看一看，点开完之后呢，他这块哎，你看像不像跟我们那个notebook启动的画面，一样的啊。

好了这里我说我新建一个哎，新建一个python3，新建一个意思啊。

![](img/e3a9a0ecda760c560a4b173b2f02897f_21.png)

就是说这里哎你去哦，在人家的一个服务器上去写啊，因为你在自己电脑上去写，你数据获取不了啊，必须在人家服务器上去写行了，咱来写一下吧，这个我们就叫做一个因子分析好。



![](img/e3a9a0ecda760c560a4b173b2f02897f_23.png)

然后重命名一下，在这里呢我们需要一会儿呃，就是一会儿咱们代码在这里写啊，到时候我会把代码拷贝给大家一份，到时候大家用的时候啊，你可以去上传到，或者是你复制到你的这个平台当中。

或者说照着咱们视频自己写也行，这个是一会儿啊，我们要用到的一个写代码的一个工具啊，其实说白了就是在人家服务器上去写啊。



![](img/e3a9a0ecda760c560a4b173b2f02897f_25.png)