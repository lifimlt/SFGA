# B07项目需求分析书



## 1 项目需求分析

### 1.1 整体架构设计

根据需求方表述，要求设计一套“自动售货机安全卫士”系统，项目内部代码"B07"。功能概述为，实现自动售货机的反防盗和及时通知功能，包含外部入侵检测、现场照片拍摄和传输、报警（现场声音播放、现场报警器鸣叫、手机软件通知）、无线MIMO功能等，将本着节约成本原则，对其提供设计方案和器件型号选型。

### 1.2 软件设计部分

- 【**系统开发：**】 ：对主CPU系统进行嵌入式编程，包含配置树莓派操作系统，搭建硬件运行环境，对整体系统运行架构，流程设计。
- 【**驱动开发：**】 ：以嵌入式系统为核心，开发摄像头驱动（拍照）、网络驱动（通信）、振动检测传感器驱动（振动检测）、报警器驱动（语音，蜂鸣器等等）的开发。
- 【**APP开发：**】  ：基于Android手机，将开发出配套的APP作为上位机，该APP在无线局域网内可检测系统状态，获取防盗信息，并可以辅助验证身份得到权限开启售货机。
- 【**算法部分：**】 ：为了更**有效准确的识别防盗或者避盗窃行为误判**，振动传感器可能并非单一的传感器，可能是传感器组，可能采取陀螺仪（检测角速度）、N个振动传感器（检测线性振动），不同位置振动不同，会进行加权分配，和其他多传感器组合的方式，则需要对多元数据进行融合和逻辑仲裁。**可作为参赛的特色点**

### 1.3 硬件设计部分

在需求中，没有对硬件部分设计的方面的需求，采用成型模块组合的方式即可解决问题，因此，不涉及硬件设计部分。



## 2 成本估算

### 2.1 成本估算

成本分为一期成本和二期成本，在设计中过程中将涉及硬件开发器件，则需要购买硬件器材，作为一期成本，可**在研发过程中，可能会遇到不可预料的问题，解决这些问题则需要引入新的器件或更换器件型号。算为二期**

**一期成本：**

| 设备列表          |   价格   |                                       链接 |
| :------------ | :----: | ---------------------------------------: |
| 树莓派3代B型（核心板）  | 249.00 | [淘宝链接](https://detail.tmall.com/item.htm?spm=a230r.1.14.6.ebb2eb2Ix3xqW&id=527595656123&cm_id=140105335569ed55e27b&abbucket=13) |
| CSI接口摄像头+线材   | 35.00  | [淘宝链接](https://item.taobao.com/item.htm?spm=a230r.1.14.71.ebb2eb2WxEHU0&id=526925746552&ns=1&abbucket=13#detail) |
| 树莓派3代配件       |  36.4  | [有电源、散热片、外壳和小风扇，因为这块和树莓派一起买的话配件太贵了，去另一家买划算。节约近70元。](https://shop130793151.taobao.com/?spm=2013.1.0.0.2e538ffeCmPJPr) |
| 16GB大小SD卡     |   50   | [淘宝链接](https://detail.tmall.com/item.htm?spm=a220o.1000855.0.da321h.4732a2bd7fibi6&id=39448266376&skuId=3440503221007) |
| GY-521陀螺仪     |  11.3  | [淘宝链接](https://detail.tmall.com/item.htm?spm=a230r.1.14.13.ebb2eb257m2Wu&id=41337720621&cm_id=140105335569ed55e27b&abbucket=13) |
| 振动模块 SW-1801P | 2.37*4 | [淘宝链接](https://detail.tmall.com/item.htm?spm=a1z10.3-b-s.w4011-16538328900.53.fa763f4rNq8ur&id=41236271649&rn=ca9105e05d22a219a7a72639db508aad&abbucket=6) |
| 高分贝报警器        |  1.72  | [淘宝链接](https://detail.tmall.com/item.htm?spm=a1z10.3-b-s.w4011-16538328900.53.22d9c2c3iHwiCC&id=41272278488&rn=1bd764f752d9f0add44782c3c0ea8842&abbucket=6) |
| 路由器           |   0    |                                       自备 |

**二期成本：**

二期成本是对项目需求进行修改，或者研发过程中出现的困难，在研发过程进行增加，预计不会产生大量费用。

### 2.2 时间估算

- 【时间】：预计3周
- 【人数】：2人

### 2.3 开发费用

**人工费：【3000.0元】**



## 3 付款说明

- 需求方需支付￥1000.00元启动资金，用于购买器件。
- 若我方没有按照要求完成项目，我方将退回所有启动资金。
- 验收完成后，需求方支付￥3000.0元。

## 4 补充说明

### 4.1 软件开源协议

为了代码后续的维护服务，所有代码版权均声明为POWERED BY MULTIBEANS，并将每个更新版本备份至GitLab上，由我们团队进行GPL（GNU General Public License）协议签署，以授权的方式给需求方，需求方可按照GPL公约对代码进行修改移植，用于自己其他任何项目上。

### 4.2 维护与培训

- 更新服务：在MULTIBEANS团队发展历程中，会不停的对于软硬件细节进行探索，在做其他项目的时候可能会有重叠功能，此时我们会更新底层代码或者硬件，也同样为涉及的项目推出更新。
- 培训服务：**由我方设计的整个系统，在验收完毕后我们会推出相应的配套视频，并且进行同步培训，提供学习资料，引导其快速掌握项目涉及的知识，并对其进行比赛技巧指导。**



**联系信息：**

------

负责人： Carlos Lopez

参与开发：Carlos Lopez

通信地址：广东省深圳市南山区西丽镇西丽大学城；

联系电话：183-0004-1052

邮箱： elvis.mlt@qq.com

------

**付款方式：**

![款方式](http://images2017.cnblogs.com/blog/810200/201708/810200-20170811150005788-470795354.png)













