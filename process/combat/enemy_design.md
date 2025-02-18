---
description: 对具有特定行为、优劣势的不同类型NPC进行原型设计
---

# 敌人设计

## 何为敌人设计？

**敌人设计**即对具有特定行为、优劣势的不同类型敌对NPC进行原型设计。

敌人设计通常需 AI 策划、程序员、角色美术、动画师、音效设计师等多方深度协作，远超出本关卡设计书籍之限。不过，即便关卡策划不负责实现敌人设计，也需具备相关的概念构思与理论思考能力。

_部分敌人设计示例可参照 《毁灭战士》 和 《雷神之锤》 的关卡体验参数设计_

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption><p>敌人设计可能极为复杂多样；图为 id Software 《毁灭战士2》（1994年）中怪物的 sprite 图</p></figcaption></figure>

## 敌人清单

假定你在开发动作游戏。以下是敌人清单（即不同敌人类型及其战斗职能）需涵盖的基本角色：

<table><thead><tr><th width="133">角色</th><th>行为</th></tr></thead><tbody><tr><td>杂兵</td><td>近距离直线近战攻击玩家，易推动</td></tr><tr><td>小队</td><td>中远程攻击，理想状态下成组轮攻</td></tr><tr><td>首领</td><td>高生存能力，可强化附近盟友</td></tr><tr><td>重装</td><td>高生存能力，但速度慢、体型大（易打中或躲避）</td></tr><tr><td>蜂群怪</td><td>体型小、速度快，生命值低但近距离伤害高</td></tr><tr><td>狙击手</td><td>攻速慢、生命值低的远程攻击者，缺少掩护时极其脆弱</td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p>维尔福（Valve Software） 《半衰期 2》（2004年）和 《半衰期：爱莉克斯》（2020年）中联合军士兵的不同设计</p></figcaption></figure>

完成一个可用的敌方NPC通常需要设计师、艺术家和程序员协同合作。这工作量颇大，远超这本关卡设计书籍的覆盖范围。

在这里，我们将专注于战斗/关卡策划在推动游戏性功能和增强易读性方面的职责：

* 敌人需**外形独特**，以便玩家在中距离（约10米以上）即可分辨类型。
* 通过设计细节和动画，**展现**敌人的状态、意图及长短处。
  * 例如在《上古卷轴5：天际》中，巨人高大且行动迟缓，玩家必须灵活走位并消耗其体力

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption><p>莫比·弗兰科（Moby Francke）与兰迪·伦丁（Randy Lundeen）在 Gamefest 2008 中发表的 <a href="https://cdn.cloudflare.steamstatic.com/apps/valve/2008/GameFest08_ArtInSource.pdf">《Valve 如何将艺术指导融入游戏玩法》（"How Valve Connects Art Direction to Gameplay"）</a>中，强调角色外形和胸高之对比的 「阅读层级」 幻灯片</p></figcaption></figure>

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

### 定义核心设计

对多数3D动作游戏而言，设计敌人时要回答以下问题：

* **生命值**：敌人多耐打，一般能存活多久？
* **速度**：敌人移动快慢，和玩家比又如何？
* **伤害**：敌人攻击有多危险？
* **攻击范围/行为**：敌人进行近程、中程还是远程攻击？

初步设计时，具体数值没那么要紧，毕竟它们很可能大幅改变。 估算为“10% / 50% / 100%”或“低/中/高”就行，等实际开展原型制作和游戏测试时再去调整具体数值。

### 生命值

玩家要耗费多少资源才能打倒这个敌人？

生命值的b：护甲/护盾、眩晕/受创踉跄
