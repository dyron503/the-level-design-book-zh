什么是关卡设计？
=====
关卡和关卡设计的定义，以及本书的使用方法


.. _installation:

什么是关卡
------------

**关卡**是游戏发生的空间。这有一些例子：

* 《堡垒之夜》中的岛和《罗布乐思》中的障碍赛
* 篮球场、赛车场和操场
* 大富翁棋盘、填字游戏和涂色书

所有这些游戏空间都为玩家设定 **界限**， 供其移动和交互。

不同的关卡间 **体验各异**。所有室内球场的形状类似，但野场和室内健身房提供不同的 **体验、文化和情绪。**

关卡策划关照玩家的 **感觉和行为** 如何随游戏空间改变。

什么是关卡设计
----------------

本书对关卡设计的定义很宽泛，仅在游戏类型方面作限缩：

**关卡设计即规划和构建电子游戏之空间——**

**——这里仅仅讨论第一人称/第三人称的动作射击游戏。**

本书的内容对于设计横向卷轴平台游戏、俯视角策略游戏或非战斗游戏仍有教益。即便如此，大多数关卡设计理论都默认媒介是3D射击游戏，这可以追溯到20世纪90年代。届时伴随射击游戏流行，关卡策划应运而生。

*关于关卡策划这一职能的更多信息，请参阅关卡策划的历史*

.. autofunction:: lumache.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
will raise an exception.

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']

