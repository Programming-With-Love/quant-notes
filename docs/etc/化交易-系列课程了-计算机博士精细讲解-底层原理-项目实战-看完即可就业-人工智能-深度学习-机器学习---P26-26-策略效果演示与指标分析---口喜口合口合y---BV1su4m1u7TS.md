# 强推！这可能是B站最全的【Python金融分析+量化交易】系列课程了，计算机博士精细讲解，底层原理+项目实战，看完即可就业！人工智能／深度学习／机器学习 - P26：26.策略效果演示与指标分析 - 口喜口合口合y - BV1su4m1u7TS

我们想法什么样，我们想法它是横着来是吧，就是横着去写每个股票名字啊，第一个股票，然后第二股票，然后第三个股票，然后第四个股票我们一般怎么样，我们一般大家是不是都喜欢这样啊，就是竖着去写。

唉我说第一个股票，然后他的一个财务的一个营收啊，怎么怎么样，第二个股票营收怎么怎么样。

![](img/4434b3fb6275f28eaf9365218cb2c59b_1.png)

第三股票，第四个股票是不是咱把它稍微改一改，这个咱们来改一改啊，这块我说我在执行这个结尾的时候，然后我说把最后的一个结果，稍微的给他去变一下吧，呃来把这个东西稍微改一改，对这个DFRAME做什么。

其实只需要对它做一个转置，是不是就可以了，然后呢咱们来看一下吧，就是打印一下它的一个转置的一个结果，现在试试这个结果对不对，然后对的话，咱再往下走，转置一下，转制完之后，其实这一步咱还没完。

在before trading的时候，我们最终要的目的是什么，不是说打印出来给你看一看吧，是把那什么那十个找到手吧，所以这块就是呃我们最终想要得到的这一块，我是再写一下吧，最终我说我们想要得到的结果。

应该是对他先做一个转置来看转制的结果。

![](img/4434b3fb6275f28eaf9365218cb2c59b_3.png)

转接结果你看就是竖着的。

![](img/4434b3fb6275f28eaf9365218cb2c59b_5.png)

就是这个东西就是一个股票名字，然后后面是他实际的一个指标吧，那第一个第一个就是一个index，一个索引，后面就是一个实际的一个值是吧行了，那此时我们只需要把索引拿到手就行吧。



![](img/4434b3fb6275f28eaf9365218cb2c59b_7.png)

你看有没有什么变化，看起来就是这间隔太短了，看不出来什么变化行。

![](img/4434b3fb6275f28eaf9365218cb2c59b_9.png)

咱不管了，一会儿策略分析吧，在这里我说我把他的index拿到手啊，这个是我想要的一个股票名字，然后我把股票名字给他重新设置一下，在这个context context当中啊，我说啊把它当做是一会儿啊。

我要返回的一个结果，或者说你就把它存到我的一个content当中这一块，这个就是咱们要的，这个就是沪深300当中选了一个十个啊，随便取个名字得了好了，这是我们现在这个打印。



![](img/4434b3fb6275f28eaf9365218cb2c59b_11.png)

咱一会也不需要了，打印这东西没什么用行了，这是我们的一个皮肤trading，我们在做交易之前，已经能够把这些个筛选工作给做完了吧。



![](img/4434b3fb6275f28eaf9365218cb2c59b_13.png)

那接下来就是一个HANDBAR啊，这里就是呃我们要实际的做一些事情了，这里咱就不pass了，咱们来写啊，往下一点再往下一点吧。



![](img/4434b3fb6275f28eaf9365218cb2c59b_15.png)

放中间给他好了，我们来写吧，第一步要干什么，首先我们要去做一个判断吧，判断什么，当前啊，哎呀我这个context当中，或者说当前啊我是否是持有一些股票，这里给大家看这个API。



![](img/4434b3fb6275f28eaf9365218cb2c59b_17.png)

先看这个API，然后咱们再参考API去写。

![](img/4434b3fb6275f28eaf9365218cb2c59b_19.png)

其实啊就是给大家准备的，所有的这些例子都是一点点翻API翻出来的。

![](img/4434b3fb6275f28eaf9365218cb2c59b_21.png)

API当中可解释的东西其实蛮多的，找一找那个context，那东西我找一下context啊。

![](img/4434b3fb6275f28eaf9365218cb2c59b_23.png)

不是在这里，在这里在这个找一找他的一个。

![](img/4434b3fb6275f28eaf9365218cb2c59b_25.png)

这是行情股票。

![](img/4434b3fb6275f28eaf9365218cb2c59b_27.png)

这是它的一些数据，没有数据还是在那里。

![](img/4434b3fb6275f28eaf9365218cb2c59b_29.png)

但这里边有这个来找一找交易相关的。

![](img/4434b3fb6275f28eaf9365218cb2c59b_31.png)

咱们之前咱们一会也要去用啊，这找到了这块。

![](img/4434b3fb6275f28eaf9365218cb2c59b_33.png)

我们需要这个就是咱们的一些组合的信息，我直接把这个复制过来再来写啊，这块就是我要看一下，我当前我的一个账户当中啊。



![](img/4434b3fb6275f28eaf9365218cb2c59b_35.png)

我的一些信息的情况，然后这一块有一个指标叫做一个position。

![](img/4434b3fb6275f28eaf9365218cb2c59b_37.png)

咱们来看一看啊，这块啊这块儿就是它有一个咱们点进去。

![](img/4434b3fb6275f28eaf9365218cb2c59b_39.png)

点开之后呢，它有一些属性啊。

![](img/4434b3fb6275f28eaf9365218cb2c59b_41.png)

咱们来看一看，我们会用这个position position，你看他说的是一个呃包含所有仓位的字典，相当于就是这里边描述的是，你现在手里有哪些个东西吧。



![](img/4434b3fb6275f28eaf9365218cb2c59b_43.png)

你都买啥东西了，是不是好了，那咱们来写一下吧。

![](img/4434b3fb6275f28eaf9365218cb2c59b_45.png)

首先第一步呃，把这个context找到手，我刚才是不是复制了一下context来这里把它。

![](img/4434b3fb6275f28eaf9365218cb2c59b_47.png)

我说我先复制过来，先看看我手里有啥东西吧。

![](img/4434b3fb6275f28eaf9365218cb2c59b_49.png)

这个关掉好啦，在这里我说我先去把做判断了呃，我看我手里有什么东西。

![](img/4434b3fb6275f28eaf9365218cb2c59b_51.png)

都手里东西的什么来着，position吧是吧，因为position当中描述的是啊，你的一个所有仓位的一个字典，所以说咱把它先拿到手。



![](img/4434b3fb6275f28eaf9365218cb2c59b_53.png)

那既然啊它是一个字典，那肯定是一个点，kiss当中存的是你所有的东西吧，那好了，我说我先做一个判断吧，如果说呀在你的字典当中啊，你这个所有买的东西那都是空的，那是不是说你现在手里啥也没有啊，好了。

先做个判断，如果现在啊都是为空的时候，如果能为空的时候，我要干什么，那我说我现在是不是就不等于零，就是现在我是一个不为空的时候，不为空的时候，咱们是不是要去卖一些东西了啊，因为只有第一次的时候。

咱们是去把所有就是买这么十只股票，然后后续啊就从第二天开始，咱们都是要去不断做判断吧，因为后续后续的时候就都不为空了，只要不为空的时候。



![](img/4434b3fb6275f28eaf9365218cb2c59b_55.png)

我们就要去卖出一些东西吧，咱要看一看，我手里有的和现在唉这个股票池当中。

![](img/4434b3fb6275f28eaf9365218cb2c59b_57.png)

给我筛选出来的是不是一样吧，那好了，我说我现在要去便利一下了，便利我手里有这些东西，便利啊，我的一个所有咱手里有的，那就是这个kiss吧，这当中保存的就是咱所有有的这些个，就是买买买的这些股票是吧。

好了，如果说如果说当前这个股票，那没在咱当前指定的我的这个股票池当中。

![](img/4434b3fb6275f28eaf9365218cb2c59b_59.png)

股票池啊，这里我看一下哎，这块呢咱是不是指定好一个名字了好了。

![](img/4434b3fb6275f28eaf9365218cb2c59b_61.png)

我说我做一个判断吧，如果说呀你没在我当前的这个股票池当中呃，我看一下这个股票池当中。

![](img/4434b3fb6275f28eaf9365218cb2c59b_63.png)

然后我就是给他要去卖掉吧，来看一看吧，卖怎么写API当中啊。

![](img/4434b3fb6275f28eaf9365218cb2c59b_65.png)

啊这里他会给你有详细的一个介绍在上面，这是交易相关的吧。

![](img/4434b3fb6275f28eaf9365218cb2c59b_67.png)

交易相关的其实有挺多东西去做啊，咱有一个呃比较方便的就是这个函数啊，order我们的一个不算值。

![](img/4434b3fb6275f28eaf9365218cb2c59b_69.png)

相当于你填个百分数就行了，点进去给大家看一看，这里呢需要你主要就是传递两个参数，第一个参数就是卖谁，第二个参数就是啊你希望经过你交易完之后，然后他的一个就是占你现在的一个百分比，那比如这样。

你说你现在经过了一个交易，经外交易之后，你要写个零，什么意思啊，那写个零的意思就是全麦吧，你看这边写了，就是投资组合占现在的一个总和啊，这是一个百分比，如果一呢，那你就是把它买满零呢，就全卖了。

这样一个意思行了。

![](img/4434b3fb6275f28eaf9365218cb2c59b_71.png)

我把他的东西直接复制过来吧，复制过来，然后咱们要进行一个交易了，然后他的一个id就是我的一个股票，然后右边这个第二参数，咱们现在要干什么来着，是卖还是买啊，你不在我的交易池当中诶。

那我是不是不在我筛选的结果当中，你不咋地，那我是不是就卖了，卖完之后你就空了，那是不是占零占0%就行了，这个是我的一个Mac操作好了，那其实不光我们得有卖操作，还得有什么还得有买操作是吧，每天好了。

咱们这里在写啊，在这块还是一个便利的操作复制过来吧，好了，便利一下，咱们这个股票在这块就不用这个了，便利什么便利我的股票池吧，然后把这个复制过来，遍地咱们现在筛选的这个池子，那接下来我是不是说要去买了。



![](img/4434b3fb6275f28eaf9365218cb2c59b_73.png)

卖完了，那是不是剩下的就该买了呀，好了再来看一下吧，怎么样去买，还是这个函数啊，我直接的给他复制过来就行了，然后去买我当前的股票，但是买多少呢，这个策略啊就是大家可以自己定。

你可以根据它的一个咱不是说了吗。

![](img/4434b3fb6275f28eaf9365218cb2c59b_75.png)

有财务数据，你可以跟他的一个财务数据，它的一个涨幅设置一个百分比。

![](img/4434b3fb6275f28eaf9365218cb2c59b_77.png)

那是不是也行啊，或者说咱们工咱们简单点吧，那就是平均啊，平均一下得了，每一个都占到一个整体的一部分，然后看一下context当中，然后咱们之前哦直接把这个复制过来就行了，我第一个300一共有多少个。

那咱们这一比上整体啊，一个浪值相当于什么，我做了一个平均买的一个操作吧。

![](img/4434b3fb6275f28eaf9365218cb2c59b_79.png)

好了，咱们也不管买多少，就平均买就得了，下面这个给他删掉行了，然后最后我来检查一下啊，最后一个pass没问题行了，这个咱们基本都写完了。



![](img/4434b3fb6275f28eaf9365218cb2c59b_81.png)

然后先来运行一下吧，看一下它的结果，看没有什么问题，呃看这个结果，一会儿咱们来给大家说一说，就是这个结果当中包含的哎这些个信息啊。



![](img/4434b3fb6275f28eaf9365218cb2c59b_83.png)

它都是什么意思，哎呦看着咋咋这么恐怖呢，直接给我干到负的30%多，可能因为咱们这个时间的选择呀。

![](img/4434b3fb6275f28eaf9365218cb2c59b_85.png)

稍微的可能这个东西就是跟时间是有关的哦。

![](img/4434b3fb6275f28eaf9365218cb2c59b_87.png)

一会儿咱们来去换个时间再来看结果，哎行了，刚才吓死我了，刚才可能就是刚开始的时候可能比较赔吧，这个回测年化收益比这个基准年化收益都要都，怎么样，都看着更可怕，是不是行，再来看这个结果。

那现在我说我设计了一个策略，先从整体来看吧，这些指标是不是主要给大家说了，还有些指标咱现在不用的，咱们等到时候后续咱们说策略用的时候，大家解释就先看前四个得了，看指标其实就主要看什么。

你的一个回测就是我们设计的策略啊，它的一个效果，以及呢你跟着这个指数走的时候啊，就啥也不玩的时候，它的一个效果看起来反正都是赔了，是不是，但是我们的策略能让你怎么样少赔一点吧。

然后最大回撤区间占的有点赚的还行吧，不是特别大，占了17%点多啊，这是咱们基本的一个指标，那夏普率那肯定是一个负的，因为这都已经赔了，咱们单位风险肯定不值得，是不是好了，这是一个收益的概况啊。

咱们大概画出这样一个结果，然后呢右边还有这样一个交易详情，我对大家点进来。

![](img/4434b3fb6275f28eaf9365218cb2c59b_89.png)