---
title: 创建标准化代码模板
description: 对于基线实施（即贵公司认为所有 [!DNL Adobe Analytics] 站点都必须具备的KPI），贵组织应尽可能采用单一的实施方法。
solution: Analytics
feature-set: Analytics
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10532.jpg
kt: 10532
exl-id: edd3df73-6d1a-4a26-a984-810cc7dd382f
source-git-commit: 058d26bd99ab060df3633fb32f1232f534881ca4
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# 创建标准化代码模板

**内容：**&#x200B;对于“基线”实施（即贵公司认为所有[!DNL Adobe Analytics]站点都必须具备的KPI），贵组织应尽可能采用单一的实施方法。 例如，跨站点使用相同的数据层结构，并利用相同的标签管理器规则/自定义代码来捕获内部搜索或访客资料信息等内容。

**原因：**&#x200B;进行可重复且可扩展的基线实施，可以使添加新元素或新站点/应用程序成为一种简化的、省力的工作，同时还可以保持您实施的干净度且易于故障排除。 使用统一的方法还可以使新的管理员/开发人员更容易联机并了解他们正在使用的内容。

**方式：**&#x200B;采用单一格式模板，在新站点或标记增强功能上线时交给开发人员。 通常，Word文档可以很好地概述以下项目：

* 正在实施的变量、它们的目的以及何时设置。 例如：

| AA变量 | 描述 | 何时/何地设置 | 如何设置 |
|--- |--- |--- |--- |
| EVAR8 | 内部搜索关键词 | 登录内部搜索结果页面时 | 数据层 |
| event8 | 内部搜索计数 | 登录内部搜索结果页面时 | Launch规则 |

* 有关如何设置的详细信息。 在这里，您可以指定所需的任何数据层对象及其语法，以及需要配置的任何TMS规则和规则设置的详细信息。
* 要确保的测试用例以及您希望在成功的测试用例中看到的所有变量都包含在QA中。 概述当开发人员测试此增强功能时，成功的实施应包括哪些内容。

理想情况下，此文档只需在下一个站点中进行调整，您可以在下一个站点中更新属性名称、页面命名惯例等基础知识。 无需每次都进行方向盘再造，这样可以节省更多时间。

## 作者

本文的共同作者为：

![Christel Guidon](assets/Christel-Headshot-150.png)

NortonLifeLock的Christel Guidon，数字[!DNL Analytics]平台经理
[!DNL Adobe Analytics]冠军

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick，高级顾问，位于[!DNL Adobe]
