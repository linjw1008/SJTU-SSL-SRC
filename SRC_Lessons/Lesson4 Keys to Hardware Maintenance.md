﻿# Lesson4 Keys to Hardware Maintenance
标签（空格分隔）： RoboCup rbk hardware

Song Zhao
---

##**0.学习要点**

 **1. 了解平时的硬件维护方法
 2.了解比赛前的硬件准备
 3. 了解比赛中的硬件维护方法**

##**1.了解平时的硬件维护方法**
###1.1 硬件故障排查方法
硬件故障常常在平时的训练中和比赛中出现，当车辆出现表面的故障后，可单机用Crazy控制单个车辆探明是否为硬件问题，并通过比对排查的方式确定原因，进行检修，填写硬件故障记录表。
###1.2 硬件故障记录表
硬件故障记录表应该包括：登记时间、底盘号、问题描述、问题原因、解决办法、解决时间
**Demo：**
|**登记时间**|**底盘号**|**问题描述**|**问题原因**|**解决办法**|**解决时间**|
|:--:|:---:|:--:|:--:|:--:|
|2018.7.11|17-01|右后电机疯转|主板或者电机损坏|更换电机|2018.7.13|
|2018.7.11|17-01|左车轮不转|连接电机转轴与车轮的传动齿轮松动|连接电机转轴与车轮的传动齿轮松动	用乐泰680胶水固定传动齿轮|2018.7.13|
|2018.7.11|17-01|射门力度不够|升压开关未闭合、平射机构的弹簧未充分伸缩|用热熔胶枪或电工胶带粘合升压开关、重装平射机构|2018.7.13|

##**2.了解比赛前的硬件维护方法**
**赛前硬件检修**

为确保比赛的顺利进行，需要在赛前完成对硬件的全面检修
```flow
st1=>start: 开始硬件检修
op1=>operation: 清点车辆，登记底盘号，查阅之前的检修记录并汇总
op2=>operation: 再次检查车辆的性能，包括：
射门性能：将射门力度调至最大值，记录挑射距离、观察平射是否正常。
吸球性能：将吸球力度调整至2挡，让车吸球。Crazy控制车辆慢速后退、旋转，观察车辆是否可以带球
运动性能：我们车辆有一个固有问题，就是速度和加速度很大时，会发生运动路径偏移的现象，
但是在比赛中，速度和加速度并不会这么大所以车辆仍然可以正常使用。
用Crazy控制车辆，以最大速度前进、后退、左移、右移，记录车辆运动轨迹的偏移程度。
op3=>operation: 在可以使用的车辆中，记录每辆车的性能，并根据性能，排列出车辆使用的优先级，如第一梯队、第二梯队等，
挑选出性能最佳的n辆车作为首发队员
op4=>operation: 物料准备
st1->op1->op2->op3->op4
```
###**物料准备明细表**
|物品|备注|
|:--:|:--:|
|顶层螺丝|4个/车|
|M3*10 内六角螺丝|足量|
|M3*10 十字螺丝|少量|
|十字螺丝刀|2个|
|内六角扳手M3、M3.5|8+1|
|螺纹紧固胶|1瓶|
|乐泰680|1瓶|
|顶层铜柱|备用|
|尼龙柱|备用|
|拆下来的电机|备用|
|车轮|备用|
|顶层电路板|备用|
|平射弹簧|备用|
|挑射弹簧|备用|
|电工胶带|1卷|
|万用表|1块|
|电工工具箱|含电烙铁、焊锡丝、吸焊枪|
|备用电池|确保所有电池均满电|
|充电器|足量|
|润滑油|当地购买|

##**3.了解比赛中的硬件维护方法**

**注意！由于比赛激烈，硬件损耗很大，需要硬件组的同学时刻待命检修，不可松懈！**

###3.1 场地调试：
在比赛的第一天，会给调试时间。此时应该复查车辆性能，更新使用优先级。然后把第一梯队给代码组跑实车。在跑实车的过程中，会出现一些新的问题。常见的问题有：吸不到球、车停下时朝向角度与预设值不符合、传球传不到指定点位等等。这些问题，是在跑单车时发现不了的，应该及时记录。

对于吸不到球，小概率可能为吸球性能本身不好，一般是球与车的嘴巴有微小距离，吸球电机转了，但是根本没有碰到球，所以肯定不会吸球。这些问题，是调试程序来解决的，与硬件关系不大。

另外，还要再次确定所有电池是否满电。确定方法是连接充电器，若指示灯为绿色则充满，为红色则不满。更简便的方法是，用万用表测量电池正负极之间的电压，若为15V以上则为满电，否则需要充电。满电和缺电的电池应该分两个容器存放。

小工具箱的准备：带到比赛场地的工具箱很大，很多工具在比赛过程中用不上。小工具箱应该包括：剪刀、剪好的色标纸、螺丝刀、六角扳手、所有备用电池、4个充电器、备用螺丝。

###3.2 赛前准备：

比赛将要开始时，将所有车辆按照优先级排列在场地旁边（方便随时换车），把充电器准备好。

###3.3 比赛过程中：
比赛过程中，代码组同学可能会提出换车要求，由于之前车辆已经按照优先级排列好，这样就可以快速换车。比如，全国赛是3v3，决赛时我们就有9辆车，3个梯队。每个梯队的车辆都是1号、3号、8号。当第一梯队的1号损坏，就可以立即换上第二梯队的1号。

###3.4中场休息：
中场休息有一个很重要的任务，换电池。将场上车辆的的电池换下来，然后充电。

###3.5比赛结束：

一场比赛结束后，要复查车辆的性能。首先要检查车轮等重要机械结构，一场比赛下来，常见的问题有，全向轮的小轮子的胶皮常有个别会被跑丢，某些小轮子的转动不再润滑，这时可以上润滑油或者更换小轮子。还有一些其它问题，比如电机坏了等等，需要见机行事。在没有比赛的时间，也要抓紧时间复查车辆性能。



