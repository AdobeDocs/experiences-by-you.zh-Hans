---
title: 现在只需等待一个区段……使用分段在Analysis Workspace中发掘新的见解
description: 了解如何使用  [!DNL Adobe Analytics]  中的区段来从 Analysis Workspace 可视化和自由格式表中发现新洞察。
feature-set: Analytics
feature: Segmentation
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00Z
jira: KT-13268
thumbnail: KT-13268.jpeg
exl-id: 3496b6ff-f8d6-48a1-92f4-442a792663e7
source-git-commit: 058d26bd99ab060df3633fb32f1232f534881ca4
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 8%

---

# 现在只需等待一个区段……使用区段在Analysis Workspace中发掘新见解

无论您是否为新手 [!DNL Adobe Analytics] user或经验丰富的专家，您将在Analysis Workspace项目中充分利用区段。 作为 [[!DNL Adobe] Experience League](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-overview.html?lang=en) 描述，“区段允许您根据特性或网站交互情况识别访客的子集。” 虽然此功能的基本结果意味着隔离您网站的用户组、访问或点击，但像您自己这样的思维敏锐的分析人员可以使用此工具进行创意，并找到了解您网站活动的新方法。 可供选择的选项有很多，因此您可以尝试创建自己的选项，并在组织内或诸如之类的社区中与其他人共享 [[!DNL Adobe Analytics] 社区](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics/ct-p/adobe-analytics-community) 在Experience League或 [#MeasureSlack](https://www.measure.chat/) 社区。

如果您需要有关如何创建区段的快速更新信息，请查阅关于使用的Experience League文档 [区段生成器](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=en) 在Analysis Workspace中。

## 比较和对比区段

在Analysis Workspace中，您可以使用“[区段比较](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/segment-comparison/segment-comparison.html?lang=zh-Hans)“。 区段比较可在左侧导航栏的“面板”部分找到：

![Seg 01](assets/seg01.png)

但是，有时您不需要完整的比较面板来为您的最终用户提供主键分析。 值得庆幸的是，某些功能也可以在标准面板中进行比较。

此 [维恩图可视化](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/venn.html?lang=zh-Hans) 可以帮助您创建快速比较，让您可以将光标悬停在该页面上并查看重叠的会话、订单、用户等。 介于2-3个自定义区段之间。 您还可以通过右键单击任何重叠部分来快速生成区段：

![2002年2月](assets/s02.png)

有时，重要的信息并不在重叠的数据中，而是在不重叠的数据中。 查看这种情况的快速方法是创建一个区段的副本，并将其设为“排除”区段：

![2003年03月](assets/s03.png)

通过将“排除”区段与比较中的其他区段栈叠，您现在可以快速计算点击菜单页面的访问量，而无需在同一会话中查看主页：

![2004年7月](assets/s04.png)

## 栈叠攻击

同样，只需将任意区段栈叠在一起，即可创建维恩图的相交数据。 您栈叠的区段或单个维度数量没有限制。 例如，如果我想快速了解一下上个月我的网站在手机上访问过哪些星期，特别是三星Galaxy A52，它确实看到了我的菜单和营养页面，但没有看到我的主页，我可以像这样快速构建主页：

![2005年00月](assets/s05.png)

但更棒的是，一旦我找到了用户或访问基础的完美子集，我就可以选择所有这些值，单击右键，并立即创建一个区段：

![2006年6月](assets/s06.png)

![2007年7月](assets/s07.png)

![2008年8月](assets/s08.png)

这在一个领域是很大的力量。

## 多个区段的数字区段

许多用户在构建区段时通常会查看名义、序数或间隔值，如访问的页面、用户的年龄范围或用户过去访问过的次数。 但是，在创建区段时，您还可以通过分段这些值来使用比率数据，无论这些值是标准维度、标准量度还是组织的自定义变量和量度。

例如，“页面逗留时间”或“每次访问逗留时间”具有预建的可用存储段：

![2009年9月](assets/s09.png)

但是，这些访问方式可能并不总是适合您组织的需求 — 也许网站的大多数访问时间都少于10分钟。 您可以使用粒度测量创建不同大小的桶。 下面创建了一个用于查看时长1分钟、1秒和1分钟30秒之间的访问：

![seg 10](assets/s10.png)

创建后，我现在可以按自定义的不同存储段时间组开始查看我的访问、订单和其他事件：

![Seg 11](assets/s11.png)

您甚至可以开始检查关键绩效指标(KPI)的变化情况，这些因素包括用户花费的时间、在一次访问中点击的页面数、过去访问过的次数或任何其他数字值，这基本上允许您查看某个指标作为另一个指标的系数：

![Seg 12](assets/s12.png)

使用区段来查找新见解的可能性是无穷的！ 这只是个起点。 自己尝试一些体验，并让社区知道您发现了什么： [[!DNL Adobe Analytics] 社区](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics/ct-p/adobe-analytics-community) 在Experience League或 [#MeasureSlack](https://www.measure.chat/) 社区。

分段快乐！

## 作者

本文作者：

![丹·卡明斯](assets/seg13.png)

**丹·卡明斯**，高级产品工程 [!DNL Analytics] 麦当劳公司经理

[!DNL Adobe Analytics] 冠军
