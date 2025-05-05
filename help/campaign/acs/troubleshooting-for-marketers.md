---
title: 营销人员疑难解答
description: 了解最常见的错误有助于更快地解决问题，并提高工作效率。 这些疑难解答提示可帮助您有效地解决发生的类似错误。
solution: Campaign Standard
feature-set: Campaign
feature: Workflows
role: User
level: Beginner, Intermediate, Experienced
doc-type: Article
last-substantial-update: 2023-05-18T00:00:00Z
jira: KT-13256
thumbnail: KT-13256.jpeg
exl-id: 1f27e284-73e3-4f28-988e-51163775eec8
source-git-commit: 02e3a6dfa59df45113242bd8e874e18e9e1efd58
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 2%

---

# 营销人员故障诊断：5个常见的工作流和交付错误

作者：[Suraj Patra](https://www.linkedin.com/in/suraj-p-51612053/){target="_blank"}，梅耶高级顾问

作为过去五年中[!DNL Adobe]Experience Cloud产品的高级工程师和客户专家，我让[Meijer](https://www.meijer.com/){target="_blank"}（一家美国超级中心连锁企业，创建于1934年）的业务用户能够与ACS一起开展复杂的营销和事务性营销活动。 我参与过的几个项目包括用于存储个性化选件和订单详细信息的自定义营销活动、与[!DNL Adobe]Audience Manager集成以及用于区段摄取的客户洞察。

在使用ACS期间，我遇到一些错误，解决这些错误会非常耗时且令人沮丧。 了解最常见的错误有助于更快地解决问题，并提高工作效率。 下面是我的疑难解答提示，可帮助您在出现类似错误时有效地解决它们。

## 数据类型不匹配错误

**错误代码：**
`PGS-220000 PostgreSQL error: ERROR: operator does not exist: character varying = bigint`

**原因：**
当您尝试使用不同数据类型的字段进行协调时，工作流中会出现这些类型的错误。 例如，当您使用具有字符串字段的加载文件上载文件时，并尝试将该字符串字段与数据类型为int的用户档案字段相协调。

![数据类型不匹配错误](/help/_assets/kt-13256/data-type-mismatch.png)

**解决方案：**
将“加载文件”活动中字段的数据类型更改为与您匹配的数据类型。 打开“加载文件”活动。 移动到“COLUMN DEFINITION”选项卡并更改所需字段的数据类型。


![数据类型不匹配解决方案](/help/_assets/kt-13256/data-type-mismatch-solution.png)

## 投放Personalization错误

**错误代码：**
`The schema for profiles specified in the transition ('') is not compatible with the schema defined in the delivery template ('nms:recipient'). They should be identical.`

**原因：**
当您向某个地址发送电子邮件，但该电子邮件或任何其他标识符未与用户档案进行协调时，会出现此错误。 要发送电子邮件通信，电子邮件或标识符应始终链接到用户档案。

具有协调活动的![工作流](/help/_assets/kt-13256/del-persn-error-wf.png)

**解决方案：**
带有收件人表的加载文件中必须存在公共ID。 此公用键将加载文件联接到协调活动中的收件人表。 电子邮件可能不会发送给收件人表中不存在的记录，收件人表需要在工作流中进行此协调步骤。 在执行此操作时，您将使用用户档案中的电子邮件ID等标识符来协调传入加载文件活动。 `nms:recipient`架构引用了配置文件表，并通过配置文件协调传入记录使其在电子邮件准备期间可用。

请参阅如下所示的协调活动的屏幕截图。

具有协调详细信息的![工作流](/help/_assets/kt-13256/del-persn-error-wf-solution.png)

了解有关[协调](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/data-management-activities/reconciliation.html?lang=zh-Hans)的详细信息。

## 通用字段数据集错误

**错误代码：**
`The document types of inbound events (''and'') are incompatible (step 'Exclusion'). Unable to perform the operation. `

**原因：**
在ACS工作流中使用&#x200B;**排除活动**&#x200B;时，当主集和排除集的字段名称不同时，根据ID执行排除时，会出现此问题。


![公用字段数据集错误](/help/_assets/kt-13256/dataset-error.png)

**解决方案：**

可通过两种方式解决此错误：

1. 在主字段和排除字段中使用相同的字段名称，并将该字段用作ID

   或者

2. 使用JOINS排除方法选择要排除记录的字段。

![公共字段数据集错误 — 解决方案](/help/_assets/kt-13256/dataset-error-solution.png)

## 字段名称删除错误

**错误代码：**
`XTK-170036 Unable to parse expression 'i__name'`

**原因：**

在&#x200B;**扩充活动**&#x200B;中可能会出现失败点。 下面显示了其中最常用的一种方法。

![字段名称丢弃错误](/help/_assets/kt-13256/field-name-dropped-error.png)

在活动中手动编辑表达式名称时，会发生这种情况。 图像显示该表达式已从`name `修改为`i__name`。

**解决方案：**

您可以通过三种方式解决此错误：

1. 将名称更改回原来的表达式。

2. 如果要使用新名称，请更改&#x200B;**扩充活动**&#x200B;中的值。

3. 如果您不记得发生了什么变化，则最好是重新创建该活动。

## 临时表删除错误 

**错误代码：**
`XTK-170024 The temporary schema "temp:deliveryEmail1" is not defined in the current context.`

**原因：**
这是涉及扩充或其他活动的复杂工作流中的常见错误。 这可能意味着在对工作流进行多项更改期间，某些活动工作流无法正确保存。

![临时表丢弃错误](/help/_assets/kt-13256/temp-table-dropped-error.png)

**解决方案：**
此错误可能以多种方式出现，因此不存在简单的修复。 如果它是一个简单的工作流，那么重新配置活动会更好。 在复杂的工作流中，最好将工作流活动复制到新的工作流中，保存并重新运行该工作流。
