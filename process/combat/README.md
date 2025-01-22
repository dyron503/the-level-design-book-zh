---
description: 设计玩家之间或玩家与NPC的物理冲突
---

# 🔫 战斗设计

## 什么是战斗设计？

战斗设计是为设计冲突相关的系统。既包括玩家之间，也包括玩家与 AI 驱动敌人的冲突。

在关卡设计中，通常假定战斗设计发生在第一人称射击游戏或其他实时 3D 动作游戏内。

请注意，玩家与玩家之间的竞技战斗（PvP）与单人/合作玩家与敌人之间的战斗（PvE）在功能上有很大不同。 PvP 通常意味着所有战斗者都有公平获胜机会； 相比之下，PvE 则提供延迟但有保证的胜利。两类游戏对玩家作出的承诺堪称天壤之别，因此关卡设计也不尽相同。

_如果你不打算在游戏内设计战斗，可以跳过此节直接开始学习_[_绘制关卡草图_](../layout/)_。_

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>《毁灭战士》（Doom）（1993）截图。《毁灭战士》是早期 FPS 的代表，许多战斗设计模式仍在影响今天的射击游戏</p></figcaption></figure>

## 战斗系统

制作战斗系统时有两种选择：

* 为包含战斗要素的现有游戏制作模组；
* 从头开始制作自己的战斗 Gameplay。

良好的战斗系统为优质关卡奠定基础，但这样的核心战斗工具包需要大量的代码、美术、动画、音频资产，以及经过反复调整后才能开发出来。

这个话题很复杂，已经超出一本关卡设计书籍所能涉及。「做好战斗体验」 这个话题和 「做出好游戏」 一样是个大话题。

因此我们强烈推荐制作模组。制作模组时，你重用经验证的现有战斗系统而无需从头开始自己做一个。

_推荐制作模组和研究的的包含战斗要素游戏见_[_工具_](../../appendix/tools.md)

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption><p>Mike Stout 的演讲 《走进玩具箱： 探究 Skylanders Spyro's Adventure 的设计》（<a href="https://www.gdcvault.com/play/1015838/Reaching-Into-the-Toy-Chest">"Reaching Into Toy-Chest：A Look into Skylanders Spyro's Adventure's Design "</a>）幻灯片，来自 GDC 2012</p></figcaption></figure>

即便只是修改已有的含战斗游戏，你也须能够从理论上解释它如何运作。含战斗游戏无论单人或多人，都以某种方式具备下面这些要素：

* 战斗机制
* 武器设计
* 经济系统

在大型商业工作室中岗位很细，关卡策划之职并不囊括这些核心战斗要素。但是，身为关卡策划不了解这些要素的话，也很难制作关卡。

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption><p>图片来自迈克尔-巴克利（Michael Barclay）等人的<a href="https://www.gdcvault.com/play/1023791/Creating-Conflict-Combat-Design-for"> "创造冲突：3A 级动作游戏的战斗设计"（Creating Conflict: Combat Design for AAA Action Games），</a>来自 GDC 2016</p></figcaption></figure>

### 战斗机制

战斗机制是指玩家在与敌人战斗时反复使用的动作/技能/武器。 一些常见的战斗机制：&#x20;

* **移动**以摆脱危险，控制地盘；
* **瞄准**特定的敌人类型/薄弱点；
* **据时机**攻击以获得**tell / telegraph** (opportunity)
* 组合动作或武器，将攻击串成**连招**
* **阻止**敌人攻击；适时**招架/反击/闪避**&#x20;
* 使用爆炸桶、水、熔岩、悬崖等**陷阱**

{% embed url="https://book.leveldesignbook.com/~gitbook/image?url=https%3A%2F%2F1666186240-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-legacy-files%2Fo%2Fassets%252F-LtVT8pJjInrrHVCovzy%252F-MCcQT9RgVLd-yLRamEE%252F-MCcQmBwTl4MKjF33SYl%252FGodOfWar2014_CombatPrototype.gif%3Falt%3Dmedia%26token%3De4c053d2-c9b7-4bbb-92e7-ec21bee8bc54&width=400&dpr=3&quality=100&sign=1ea02b63&sv=2" %}
索尼圣莫妮卡工作室 2014 年为 《战神》（2018）制作的早期测试地图 + 战斗原型 GIF 动画
{% endembed %}

### 武器设计

许多游戏都为玩家提供多种可使用的武器。**武器设计**就是对这些武器进行构思、实现和平衡。 需要考虑以下几个方面：

* **武器感受、幻想程度**（如慢吞吞大枪 vs. 鬼祟祟小刀 vs. 响当当电锯）
* 伤害、范围、开火速度、弹量等**数据**
* **强度区间**，玩家在不同时候选择最适合/有效的武器

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p>《毁灭战士》（1993）中的武器启发了之后许多射击游戏：(1) 电锯，(2) 手枪，(3) 霰弹枪，(4) 超级霰弹枪，(5) 橡皮枪，(6) 火箭发射器，(7) 等离子枪，(8) BFG</p></figcaption></figure>

### 经济系统

经济是一个游戏设计通用术语，指玩家在整个游戏过程中必须考虑的成本/收益/回报的整体系统。 玩家对资源的获取会影响到他们使用哪些机制和武器以及何时使用：

* **武器经济学：**&#x5F39;量、时间（DPS）、武器库 / 装备
  * _例如：玩家只剩 1 枚火箭弹，则会把火箭弹留到对火箭弹有弱点的强敌交战时使用_
  * _例如：玩家在水下只有 15 秒的氧气时间，因此需要高 DPS 武器来对付水下敌人_
* **玩家状态：**&#x751F;命值、库存和消耗品这类短期数据
  * 例如：玩家有99%生命值，则一般不会选择将浪费24%的回复25%物品
* **玩家成长：**&#x7ECF;验值、被动技、升级、装备等长线收益
  * 例如：玩家的生命值为 99%，但有一条被动技能——如果生命值满了，就能获得双倍伤害——就大概率会决定还是选择 +25% 生命值的物品，因为伤害奖励比浪费的治疗值更有价值

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption><p>用于动作 RPG 游戏《战神：毁灭之战》（God of War: Ragnarok）（2022）的武器升级电子表格，摘自罗伯-迈耶（Rob Meyer）的演讲 "命运的抉择：毁灭之战的战斗规模"（<a href="https://youtu.be/6iTBqcBv5QA?t=1311">"Reckoning With Fate: Combat At The Scale of Ragnarok" </a>）（2023 年）（来自 YouTube）。</p></figcaption></figure>
