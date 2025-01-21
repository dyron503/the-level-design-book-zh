---
description: 设计玩家与NPC的物理冲突
---

# 🔫 战斗设计

## 什么是战斗设计？

战斗设计是为设计冲突相关的系统。既包括玩家之间，也包括玩家与 AI 驱动敌人的冲突。

在关卡设计中，通常假定战斗设计发生在第一人称射击游戏或其他实时 3D 动作游戏内。

请注意，玩家与玩家之间的竞技战斗（PvP）与单人/合作玩家与敌人之间的战斗（PvE）在功能上有很大不同。 PvP 通常意味着所有战斗者都有公平获胜机会； 相比之下，PvE 则提供延迟但有保证的胜利。两类游戏对玩家作出的承诺堪称天壤之别，因此关卡设计也不尽相同。

_如果你不打算在游戏内设计战斗，可以跳过此节直接开始学习_[_绘制关卡草图_](../layout/)_。_

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption><p>《毁灭战士》（Doom）（1993）截图。《毁灭战士》是早期 FPS 的代表，许多战斗设计模式仍在影响今天的射击游戏</p></figcaption></figure>

## 战斗系统

制作战斗系统时有两种选择：

* 为包含战斗要素的现有游戏制作模组；
* 从头开始制作自己的战斗 Gameplay。

良好的战斗系统为优质关卡奠定基础，但这样的核心战斗工具包需要大量的代码、美术、动画、音频资产，以及经过反复调整后才能开发出来。

这个话题很复杂，已经超出一本关卡设计书籍所能涉及。「做好战斗体验」 这个话题和 「做出好游戏」 一样是个大话题。

因此我们强烈推荐制作模组。制作模组时，你重用经验证的现有战斗系统而无需从头开始自己做一个。

_推荐制作模组和研究的的包含战斗要素游戏见_[_工具_](../../appendix/tools.md)

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p>Mike Stout 的演讲 《走进玩具箱： 探究 Skylanders Spyro's Adventure 的设计》（<a href="https://www.gdcvault.com/play/1015838/Reaching-Into-the-Toy-Chest">"Reaching Into Toy-Chest：A Look into Skylanders Spyro's Adventure's Design "</a>）幻灯片，来自 GDC 2012</p></figcaption></figure>

