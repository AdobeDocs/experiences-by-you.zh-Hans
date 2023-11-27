---
title: 记录CRM同步错误以便轻松进行故障排除
description: 了解如何使用CRM同步错误的日志来调查CRM同步问题并保持其顺利运行。
feature-set: Marketo Engage
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00Z
jira: KT-13875
thumbnail: KT-13875.jpeg
hide: false
exl-id: 6a38f5dd-5d25-43d8-a1d3-e75ab396e555
source-git-commit: 058d26bd99ab060df3633fb32f1232f534881ca4
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---

# 记录CRM同步错误以便轻松进行故障排除

作为 [!DNL Marketo Engage] 管理员，检查您的实例是否与CRM保持同步应该是您的关键部分 [每日例程](https://nation.marketo.com/t5/champion-program-blogs/my-marketo-morning-routine-tips-for-driving-marketing-operation/ba-p/247508){target="_blank"}. While the [Notifications section](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/notification-types.html){target="_blank"} (在页面的右上角找到 [!DNL Marketo Engage] 界面)，您将在此处开始查找和调查频繁出现的同步问题，这里有一个专业提示，可帮助您以有条理的方式管理实例运行状况。 [!DNL Adobe] Marketo Champion (2019-2022)，Amy Goldfine建议管理员用户保留CRM同步错误的日志，以便更轻松地执行故障排除。

![Sync Errors选项卡屏幕截图](/help/marketo-tutorial-inherited-instance/_assets/Marketo_Engage_Admin_Salesforce_Sync_Errors_Tab.png)

## 为什么要保留CRM同步错误的记录？

通过记录CRM同步错误， [!DNL Marketo Engage] 管理员可以与CRM管理员一起查看问题和趋势以修复根本原因。 请按照以下步骤记录您实例的CRM同步问题。

## 如何保留CRM同步错误的日志

在开始之前，请下载 [CRM同步错误日志模板](/help/marketo-tutorial-inherited-instance/_assets/downloads/Adobe-Marketo-Engage_CRM-Sync-Error-Log-Template.xlsx).

**第1步：** 转到 *[!UICONTROL 管理员] 部分* 在 [!DNL Marketo Engage]. 下 *[!UICONTROL 集成]*，单击 *[!DNL Salesforce]*， *[!DNL Microsoft Dynamics]*，或 *[!DNL Veeva]*，具体取决于哪些 [!DNL CRM] 使用，然后 *[!UICONTROL 同步错误]* 选项卡。

**第2步：** 您可以选择 [将错误记录导出为 [!DNL CSV] 文件通过 [!UICONTROL 筛选] 面板](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/salesforce-sync/salesforce-sync-errors.html#filter-sync-errors){target="_blank"}. 如果您只有几个小时，请直接从复制和粘贴 *[!UICONTROL 同步错误]* 跳卡就是最好的方法。

**步骤3：** 记下发生错误的日期。

**第4步：** 输入受该错误影响的人员记录数。 (有时，您的CRM将只针对一个人引发错误。 有时会有许多人同时出现相同的错误。)

**步骤5：** 记下受错误影响的一个人的电子邮件地址。 这样，您就可以轻松地与CRM管理员引用和讨论错误。

**步骤6：** 在[！DNL]中粘贴指向人员记录的链接 [!DNL Marketo Engage]]和 [!UICONTROL CRM潜在客户/联系人] 该人员的记录。

**步骤7：** 在最后一列，粘贴错误的实际文本。

## 展望未来

**识别错误代码：** 要了解错误代码，请查看开发人员文档中的描述 [响应级错误代码表](https://developers.marketo.com/rest-api/error-codes/#response_level_error_codes){target="_blank"} 并查找解决错误的典型后续步骤。

## 作者

**艾米·戈德法恩**\
[!DNL Adobe] Marketo冠军(2019-2022)
*创始人，MarketingOpsAdvice.com*

![艾米·戈德法恩](/help/marketo-tutorial-inherited-instance/_assets/authors/Customer_Author_Amy_Goldfine.png){width="25%"}

**赵蔼明**
*采用和维系市场经理，位于[!DNL Adobe]*

![赵蔼明](/help/marketo-tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width="25%"}
