# 数据分析+金融量化+数据清洗，零基础数据分析金融量化从入门到实战课程，带你从金融基础知识到量化项目实战！【入门必备】 - P40：08 DataFrame合并-02 - Senior数据分析媛 - BV1Ak61YVEYX

呃这个合并啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_1.png)

我们这个总结一下。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_3.png)

![](img/f1fba616fb5a0b31b0a0b2b927313f40_4.png)

这是我们的一个默认函数啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_6.png)

首先这个呃合并呢有有这么几个前提啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_8.png)

首先第一个呢强调一下merge呢只支持列合并啊，比如你不要企图说我拿行来合并啊，没有这个没有这个玩玩法啊，都是拿列合并，所以它是以列为基准的啊，都是以以列为合并项的啊。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_10.png)

那另外呢你要想合的话呢，它这个参与合并的列呢，必须有呃有这样一个关系啊，参与合并的列必须满足一对一，一对多或者是多对多关系中的至少一种啊，必须有这样一个关系。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_12.png)

那另外呢就是我们参与合并的列，他的选择上啊应该是，选择离散型数据，而不是连续型数据啊，但是一般来讲离散型数据呢都是对象类型，当然这个不是绝对的啊，比如说我的数字就是有两个值，就零和一，零和一。

那它也能和对吧啊，所以还是这个离散型和连续型啊，你要分开啊，那离散型是什么，就是固定的几个取值啊，或者几十个或者几百个都行啊，总之这个值是固定的，而连续呢是不固定的啊，在这个范围内可以随机取值啊。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_14.png)

所以说他是这样一种关系啊，然后呢我们合并里面的参数啊，这个第一个how参数，这个是干嘛的呢，这个是决定了我们合并的方式啊，合并的方式有这个内合并外合并，然后左合并和这个右合并，右边合并，左边合并啊。

那么要知道这个各种关系的一个含义啊，内合并呢就是什么取这个内容的交集，外合并取内容的并集，左合并以左表的内容为准，右合并以右表的内容为准啊，然后除此之外呢，还有一个是这个on啊，on什么时候用呢啊。

它是指定指定参与合并的列是吧，通过标签来指定啊，那它用于什么情况啊，用于这个有多列多列标签相同的情况，如果你有两列三列或者更多的列的标签相同的，那我们需要在里面去选择更少的列来参与合并。

我们可以通过on来指定啊，它可以指定一个值或者是一个列表都行啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_16.png)

然后呢与on对应的是什么呢，就是这个left on和这个right on它呢是什么呢，是分别指定左左右表参与合并的列，参与合并列，它用于什么情况，用于两张表参与合并的列。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_18.png)

标签不同的情况啊，用这种情况啊，然后还有一个是看看啊这个left right right index啊，还有这个SELFIXES啊，surface it用什么呢，它一般会跟我们这个on来结合使用啊。

与on这个参数一起使用啊，它什么呢，它是把这个，它是给给相同列标签，但是没有参与合并的列添加后缀的啊，这么一个东西除了这个之外呢。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_20.png)

还有还有一个就是我们这个叫left index和write index啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_22.png)

那这个是干啥的呢，啊首先呢它是指定这个索引的啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_24.png)

指定索引的，那我比如说我们现在拿这个这个table1和table2。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_26.png)

来说啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_28.png)

K8来说，这里边呢比如说我们这个型号这一列，它成了索引，这边我们需要去扩展一个方法，就是我们怎么去把某一列给它设置成行索引，我可以用这set index我指定型号。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_30.png)

这样呢我就把型号啊给它设置成行索引了是吧。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_32.png)

这叫指定列啊，就是把某一把指定的列设置为行索引，那如果它成了行索引，我把它保存为叫table6啊，table5就行了是吧，Table5。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_34.png)

现在呢我这个table1和TAO5，他们俩想合的话，显然我得根据table1，我得根据手机型号这一列。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_36.png)

而TV5的话我得根据索引来合对吧，那对于这种情况的话。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_38.png)

我们就需要用到这个left index或者是right index这个函数，这个参数了啊，嗯pd点merge，然后左表table1，右表table5，然后呢我左表呢要依赖于手机型号这一点。

然后右表write index，因为因为right我on的话，它没有已经没有列了是吧，没有它只有一列，就是重量嘛对吧，我已经不能用right on了。

因为right on和right left on它都是指定列标签的，所以我们需要用左，用右边的这个索引来来参与合并，所以我应该用write index，因为索引就一个。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_40.png)

我把它设置为true就行了啊，这样的话呢我再和。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_42.png)

就可以了是吧，那同样道理，如果你把TV5设置成左表，它放到右边的话，那我应该写left index和和write on。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_44.png)

是不是啊，啊那总总结出这么几条啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_46.png)

就是我们这个啊这个指定指定索引，作为合并合并的参考参考值好了，搞定它几个前提。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_48.png)

然后呢去了解到这几个参数啊，这个合并我们就只能用好了啊，然后呢那我们现在去看一下这个嗯几个。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_50.png)

![](img/f1fba616fb5a0b31b0a0b2b927313f40_51.png)

![](img/f1fba616fb5a0b31b0a0b2b927313f40_52.png)

好看下这下面这个练习啊，呃这个假设有两个同学都叫李四啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_54.png)

![](img/f1fba616fb5a0b31b0a0b2b927313f40_55.png)

都是张三和李四的成绩表，这个怎么合并啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_57.png)

那这个这个表格我们得设计一下啊，因为我们有个前提就是咱们这个合并啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_59.png)

它只能是以列为合并项对吧。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_61.png)

所以这边呢我们得把这个，你得把张三和李四作为列标签来处理啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_63.png)

不然的话这不合逻辑啊，当然这只是一个练习啊，所以我们也不用太去去那个纠结，那个我先把这两张数据表啊，先给他构造出来啊，这个DF1等于一个data frame，然后data呢我用字典来处理啊。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_65.png)

第一个是张三的程序，张三冒号，然后呢他比如说有个150啊，148，然后一个130。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_67.png)

然后再来个李四，冒号，这是个110123，这个145，这是第一张表，然后呢，我再构造第二张表，点F2，因为这个张三是一个人对吧，张三是同一个人啊。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_69.png)

两张表都是同一个人啊，然后呢我这个张三这个成绩不能变啊，然后这个李四呢我换个成绩，他比如说这个这个是个学渣啊，要考这个啊。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_71.png)

34，然后23，然后45分好了。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_73.png)

好了现在这两张表我要合并，那我他俩如果合并的话，我是得根据张三来合呀，是不是张三来合呀啊那么我这个张三的值啊。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_75.png)

虽然说这个分数它是一个连续值啊，但是我们这边呢，就是先把它姑且当成是一个离散值来来用啊，就是我们我们这个真正在处理业务的时候呢，尽量不要用这种情况，因为它是数值型，数值型的话很容易出现重合的。

所以你要注意一个细节，你看我这块是没有写相同的值啊，因为一旦出相同的值啊，这个合并就紊乱了啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_77.png)

那我们先来看这个逻辑啊，他俩之间合并的话，我根据张三来合。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_79.png)

是不是如果我默认合的话，是张三李四要要一块合呀，如果我这个直接写这个DF1和DF2的话。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_81.png)

就没有值了，为啥呢，因为他俩得完全匹配上啊，张三李41501百一。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_83.png)

然后也得找张三李41501百一的，找不到，对不对，我们现在只能根据谁的，我们说根据张三来合呀。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_85.png)

根据张三来和我们得到李4X和李4Y，那当然你可以给他加个后缀，是不是，这个SELFIXES，那张三李四啊，这个李四来个大理寺和小李四是吧，大小啊。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_87.png)

这样就合了，可以了是吧。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_89.png)

![](img/f1fba616fb5a0b31b0a0b2b927313f40_90.png)

![](img/f1fba616fb5a0b31b0a0b2b927313f40_91.png)

还有这个啊，看这个练习啊，嗯也是两份成绩单。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_93.png)

第一个是张三李四王老五之外，还有一个是张三和张有六的成绩单啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_95.png)

这两个怎么合是吧，还是这个这个构造逻辑啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_97.png)

我把这个复制过来，老婆安天王。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_99.png)

第六有张三李四。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_101.png)

王老五，再加一个，然后另外一个是张三和赵小六，把他改成赵小六。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_103.png)

嗯好，那么这两张表合并张三是同一个人对吧，那我们也就是说我们要把占小，占小六是不是合并到这个总表里面啊。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_105.png)

那我们就得根据张三来进行合并吧，这pd点点merge啊，然后这个左边是DF1，右边是DF2，然后那我是就直接根据张三就行了，就不用再设置了。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_107.png)

因为没有重名了是吧啊，直接合就行了，这样吧，赵小六合进来了。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_109.png)

三十四二十三四十五是吧，那另外一种情况，如果把这个张三的名字打错了。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_111.png)

打成张三，那就这个地方我写成了张13啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_113.png)

写错了写错了，那我这样直接合出就不行了。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_115.png)

就找不到值了是吧，怎么办呢，我们说还是因为张三跟这个张13是一个人吧，他只是名字写错了对吧，所以我们可以通过left on指定为张三，然后write on我们指定为张13啊。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_117.png)

这样来处理，那这样的话我们就多了一个值啊，这两个人数一个人啊，是不可以把它删掉啊，删掉，那我们这个这个data frame想删除的话，是不是直接来一个job照我删除列，那我们把谁删，把张13删掉啊。

比如说这个labels果然等于这个张13，然后方向呢改成一列方向labels是吧，label写错了啊。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_119.png)

![](img/f1fba616fb5a0b31b0a0b2b927313f40_120.png)

好了啊，那咱们这个今天就这么多内容啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_122.png)

然后这个晚上大家把这个作业做一下啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_124.png)

这是一个简单的一个数据分析啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_126.png)

但是咱们咱们第一次做呢，恐怕难度有点高。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_128.png)

哈哈对，因为因为这里边确实有一些逻辑，我们是第一次接触对吧。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_130.png)

那么做做得出来，做不出来不是目的，目的是你要经过一个思考，经过一个磨练对吧，你有个有这个过程啊，这个过程你走了几次之后呢。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_132.png)

自然就能写出来了啊，但你要是不走啊，不走不行啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_134.png)

你一定要思考啊，你不能光听我讲，你听我讲的话，你印象是不深刻的，就是为什么是那样子的，可能你没有经过一个思考的过程啊，所以说呢大家不用说大家的目的。



![](img/f1fba616fb5a0b31b0a0b2b927313f40_136.png)

不用说带着把这东西做好，做完了，你要带的目的是，我这里面到底我投入了多少的思考时间啊。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_138.png)

你思考了多长时间，然后你实现了多少。

![](img/f1fba616fb5a0b31b0a0b2b927313f40_140.png)

![](img/f1fba616fb5a0b31b0a0b2b927313f40_141.png)