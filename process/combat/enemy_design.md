---
description: 对具有特定行为、优劣势的不同类型NPC进行原型设计
---

# 敌人设计

## 何为敌人设计？

**敌人设计**即对具有特定行为、优劣势的不同类型敌对NPC进行原型设计。

敌人设计通常需 AI 策划、程序员、角色美术、动画师、音效设计师等多方深度协作，远超出本关卡设计书籍之限。不过，即便关卡策划不负责实现敌人设计，也需具备相关的概念构思与理论思考能力。

_部分敌人设计示例可参照 《毁灭战士》 和 《雷神之锤》 的关卡体验参数设计_

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption><p>敌人设计可能极为复杂多样；图为 id Software 《毁灭战士2》（1994年）中怪物的 sprite 图</p></figcaption></figure>

## 敌人清单

假定你在开发动作游戏。以下是敌人清单（即不同敌人类型及其战斗职能）需涵盖的基本角色：

<table><thead><tr><th width="133">角色</th><th>行为</th></tr></thead><tbody><tr><td>杂兵</td><td>近距离直线近战攻击玩家，易推动</td></tr><tr><td>小队</td><td>中远程攻击，理想状态下成组轮攻</td></tr><tr><td>首领</td><td>高生存能力，可强化附近盟友</td></tr><tr><td>重装</td><td>高生存能力，但速度慢、体型大（易打中或躲避）</td></tr><tr><td>蜂群怪</td><td>体型小、速度快，生命值低但近距离伤害高</td></tr><tr><td>狙击手</td><td>攻速慢、生命值低的远程攻击者，缺少掩护时极其脆弱</td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption><p>维尔福（Valve Software） 《半衰期 2》（2004年）和 《半衰期：爱莉克斯》（2020年）中联合军士兵的不同设计</p></figcaption></figure>

完成一个可用的敌方NPC通常需要设计师、艺术家和程序员协同合作。这工作量颇大，远超这本关卡设计书籍的覆盖范围。

在这里，我们将专注于战斗/关卡策划在推动游戏性功能和增强易读性方面的职责：

* 敌人需**外形独特**，以便玩家在中距离（约10米以上）即可分辨类型。
* 通过设计细节和动画，**展现**敌人的状态、意图及长短处。
  * 例如在《上古卷轴5：天际》中，巨人高大且行动迟缓，玩家必须灵活走位并消耗其体力

<figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption><p>莫比·弗兰科（Moby Francke）与兰迪·伦丁（Randy Lundeen）在 Gamefest 2008 中发表的 <a href="https://cdn.cloudflare.steamstatic.com/apps/valve/2008/GameFest08_ArtInSource.pdf">《Valve 如何将艺术指导融入游戏玩法》（"How Valve Connects Art Direction to Gameplay"）</a>中，强调角色外形和胸高之对比的 「阅读层级」 幻灯片</p></figcaption></figure>

## 平衡敌方阵容

电子表格/矩阵或许很适合用来整理敌方阵容：

<table><thead><tr><th>角色</th><th>速度<select><option value="KMyusSlLSMTF" label="中等" color="blue"></option><option value="MUY8VzbthREk" label="快速" color="blue"></option><option value="NwjVYLyCE33I" label="慢速" color="blue"></option></select></th><th>生命值<select><option value="8524O3Zw28kC" label="较少" color="blue"></option><option value="RpewWXZhmOwE" label="中等" color="blue"></option><option value="dgwDRgV6Rq6z" label="较大" color="blue"></option></select></th><th>攻击范围<select><option value="msiw5sVmeT2p" label="近" color="blue"></option><option value="H3Pl4lO6LLI8" label="中" color="blue"></option><option value="iXQBYVdIlg5J" label="远" color="blue"></option></select></th><th>每秒伤害（DPS）<select><option value="UHXAiYT91JPI" label="较低" color="blue"></option><option value="9bKCpHkW2Gpl" label="中等" color="blue"></option><option value="pfCxmVU0hwjl" label="强大" color="blue"></option></select></th></tr></thead><tbody><tr><td>杂兵</td><td><span data-option="KMyusSlLSMTF">中等</span></td><td><span data-option="8524O3Zw28kC">较少</span></td><td><span data-option="msiw5sVmeT2p">近</span></td><td><span data-option="9bKCpHkW2Gpl">中等</span></td></tr><tr><td>小队</td><td><span data-option="KMyusSlLSMTF">中等</span></td><td><span data-option="RpewWXZhmOwE">中等</span></td><td><span data-option="H3Pl4lO6LLI8">中</span></td><td><span data-option="UHXAiYT91JPI">较低</span></td></tr><tr><td>首领</td><td><span data-option="KMyusSlLSMTF">中等</span></td><td><span data-option="RpewWXZhmOwE">中等</span></td><td><span data-option="H3Pl4lO6LLI8">中</span></td><td><span data-option="9bKCpHkW2Gpl">中等</span></td></tr><tr><td>重装</td><td><span data-option="NwjVYLyCE33I">慢速</span></td><td><span data-option="dgwDRgV6Rq6z">较大</span></td><td><span data-option="msiw5sVmeT2p">近</span></td><td><span data-option="pfCxmVU0hwjl">强大</span></td></tr><tr><td>蜂群怪</td><td><span data-option="MUY8VzbthREk">快速</span></td><td><span data-option="8524O3Zw28kC">较少</span></td><td><span data-option="msiw5sVmeT2p">近</span></td><td><span data-option="UHXAiYT91JPI">较低</span></td></tr><tr><td>狙击手</td><td><span data-option="NwjVYLyCE33I">慢速</span></td><td><span data-option="8524O3Zw28kC">较少</span></td><td><span data-option="iXQBYVdIlg5J">远</span></td><td><span data-option="pfCxmVU0hwjl">强大</span></td></tr></tbody></table>

这有助于平衡阵容或找出不足之处，但不要让表格限制住自己，形成固定思维。例如，在上述矩阵中：

* 只有单一快速敌人吗？或许首领也应该设为快速型，这样才能与小队拉大差异。
* 没有设计在中程打高伤害的敌人。是否应该有这样的敌人呢？这样会有趣或有用吗？
* 这个矩阵设计是否太简单了？需要添加尺寸栏、行为栏等等吗？

要分析现有游戏中敌人列表的话：游玩多个关卡，然后用你自己设定的行列栏目创建一张电子表。

* 哪种地形/布局对每种敌人类型最有效？
* 哪些敌人编组效果好？为什么？
* 哪些关卡会出现哪些敌人组合？

<figure><img src="../../.gitbook/assets/image (45).png" alt=""><figcaption><p>the Grunt, Elite, Jackal, 和 Hunter 极具辨识度。它们是 Bungie 于 2001 年推出的 《光环：战斗进化》 中星盟阵营敌人。</p></figcaption></figure>

## 敌人设计建议

业界在设计敌人类型与编组上有以下普遍共识和建议：

* 追&#x6C42;_&#x591A;样_ 战斗体验：每类敌人体验作出区隔，避免设计相似敌人；
* 强&#x5EA6;_&#x5206;级_ ：划分敌人强弱层级，明确排名；
* 维&#x6301;_&#x957F;期价值_ ：避免敌人过时。前期弱小的敌人后期也应有趣味，比如中期 BOSS可转成普通敌人；
* 制造不&#x540C;_&#x60C5;境_ ：敌人组合应改变战局，限制玩家使用单一战术；
* 设计 _「聪明」_ 敌人：塑造智能假象，赋予敌人不同情绪（如害怕、愤怒等）：
  * 「聪明」 的敌人得有高生命值，不然来不及展现智慧就死了；
* 保&#x6301;_&#x4E00;致性_ ：让敌人行为有规律，方便玩家识别和利用。

<figure><img src="../../.gitbook/assets/image (46).png" alt=""><figcaption><p>《毁灭战士 2》 怪物 「正交单位差异化」 矩阵图，横轴是 「后退（STAY BACK）或冲锋（CHARGING）」 行为，纵轴为 「投射物（PROJECTILE）或即时命中（HITSCAN）」 攻击方式。源自<a href="https://www.youtube.com/watch?v=BEF4GVNzkUw"> Matthias Worch 2014 年游戏开发者大会（GDC 2014）演讲 「游戏与关卡设计中的有意义选择」（"Meaningful Choice in Game &#x26; Level Design"）</a>的幻灯片<a href="http://www.worch.com/2014/03/23/decisions-that-matter/">（PDF 文件）</a></p></figcaption></figure>

## 如何设计敌人

### 1.定义核心设计

对多数3D动作游戏而言，设计敌人时要回答以下问题：

* **生命值**：敌人多耐打，一般能存活多久？
* **速度**：敌人移动快慢，和玩家比又如何？
* **伤害**：敌人攻击有多危险？
* **攻击范围/行为**：敌人进行近程、中程还是远程攻击？

初步设计时，具体数值没那么要紧，毕竟它们很可能大幅改变。 估算为“10% / 50% / 100%”或“低/中/高”就行，等实际开展原型制作和游戏测试时再去调整具体数值。

#### 生命值

玩家要耗费多少资源才能打倒这个敌人？

生命值的变体：护甲/护盾、眩晕/受创踉跄

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption><p>这是 2002 年 Bungie 一场设计讨论会上有关 《光环》 敌人的幻灯片内容，显示出一种关联：「越强悍 = 越智能」</p></figcaption></figure>

#### 攻击范围/行为

针对 3D 动作游戏 《天空护卫：斯派罗大冒险》（Skylanders： Spyro's Adventure），动视暴雪（Activision-Blizzard）的设计师迈克·斯托特（Mike Stout）讲述了设计团队如何构思出四大主要类型（「近战型、远程 型、蜂群型、重型」）及其行为特点。他觉得单纯的近战敌人通常挺乏味的，而远程敌人对关卡设计意义重大：

> _「远程敌人非常简单，就是会朝你射击的家伙。但他们很有意思，因为环境对他们影响很大。碰到近战敌人时，由于他们没法远程攻击你， 环境完全不重要：你把他们引到岩架上、藏身在掩体后——和在平地上与他们战斗没啥差别。所以在关卡里加入远程敌人，并与其他 类型的敌人搭配起来，关卡设计一下子就变得关键起来了。」_
>
> ——迈克·斯托特，[2012年游戏开发者大会：《探寻玩具箱：〈天空护卫：斯派罗大冒险〉的设计解析（GDC 2012：“Reaching Into The Toy-Chest： A Look Into Skylanders Spyro's Adventure's Design”)》](https://www.gdcvault.com/play/1015838/Reaching-Into-the-Toy-Chest)

敌人攻击范围的变化方式：

* 抛射物设计（速度、移动模式）
* 尺寸（远处小目标比大目标更难发现与攻击）

### 2.测试用白盒场地

* 通常一个大方形房间就够用，这步别花上超过几分钟；
* 对于远程敌人，还要设置不同凸起平台、沟壑或掩体；
* 迂回与掩护的简易通用模式：iceworld 三路线

### 3.制作敌人原型

* 创建占位对象：
  * 可滑动的彩色方块、胶囊状物体；
  * 利用现成资源，复用现有角色美术素材并换色。
* 编写行为脚本
  * 若游戏引擎或工具脚本或AI系统强大，或许不用直接改游戏代码就能做出敌人原型；
  * 但一般得写点脚本
  * 常见 AI 脚本模式：状态机、行为树或一系列`if()`语句
* 测试敌人原型
  * 若可能，拿到控制台命令或调试菜单，以便游戏运行时生成更多敌人

### 4.调整敌人

敌人在游戏中正常运行后，工作才刚开始。得调整其属性和行为，来达成预期体验。

前期调整时，只做大幅改动。别做小调整，早期阶段很难察觉其变化。

<details>

<summary><em>示例：假设要调整敌人生命值……</em></summary>

它有100点血，但感觉太弱，得加强。别调成115点：这改动小，试玩时可能没感觉。不妨调成200点血。

* 若感觉强度设为200太高，恭喜！你已确定了100 - 200的调节范围， 不妨试试150。
* 要是设为200仍感觉强度不足，那就试试300，甚至400。持续测试直至确定合适范围，然后逆向验证。

</details>

### 5.暂且搁置，稍后再议

在整个项目推进过程中，完整的敌人设计流程可能历时数年；你会逐步增添新敌人、武器、玩家升级机制、关卡等内容。&#x20;

项目团队可能为赶重要节点，突然砍掉未完成的敌人类型；或许你还 得把原本设计的 Boss 降格成较弱的可复用 「中Boss」。 精心调校的敌人，也可能突然过时或暴露缺陷。这就是创意和游戏设计的特性：项目会不断演变和发展。

待完成：以 《半衰期 2》 的直升机为例说明

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p>《毁灭战士2》 中，与小鬼、霰弹枪手和链锯枪手战斗时的不同节奏…… 幻灯片摘自 Matthias Worch 在 2014 年游戏开发者大会上的演讲<a href="https://www.youtube.com/watch?v=BEF4GVNzkUw">《游戏与关卡设计中的有意义抉择》（"Meaningful Choice in Game &#x26; Level Design"</a><a href="https://www.youtube.com/watch?v=BEF4GVNzkUw">）</a><a href="http://www.worch.com/2014/03/23/decisions-that-matter/">（幻灯片PDF）</a></p></figcaption></figure>

## Boss 设计

（待完成）

基本流程与普通敌人设计一致，但这可是个大场面。在制作 Boss 原型时，还得不断调整战斗场地白盒。

Boss不必是新敌人类型，也可以是给现有敌人加上特殊脚本，甚至是 围绕NPC设计的解谜环节。任何充满冲突与危险的高潮环节，都会有 Boss战的感觉。

## 总结一下……

* **敌人设计**任务繁重，通常需与美术和程序协作，才能做出游戏中可用的成品敌人；
* **敌人清单**有助于在游戏生态中平衡敌人类型，避免设计用途不明或重复的敌人；
  * **多样性**至关重要。你或许需要将强弱、快慢、大小、远近程等各类敌人组合搭配，并兼顾处于这些之间的其它类型。
* 设计敌人的方法：
  1. 确定核心属性数值，如**生命值、速度、伤害**及**攻击范围/行为模式**；
  2. 在**白盒**中搭建大型测试场地，但制作时间勿超几分；
  3. 制作敌人原型并**开展游戏测试**，你可能需具备脚本或编程知识；
  4. **调整**敌人属性：原型设计阶段，宜进行大幅改动，避免细微调整。
* BOSS设计是个特例，它是一种独特的场景遭遇，与特定关卡关联更 为紧密。要持续迭代 BOSS 场地白盒。

## 下一步怎么办？

* 考虑阅读其它通用[战斗设计](./)概念；
* 利用敌人设计[遭遇战](encounter.md)。

