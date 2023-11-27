---
title: 创建标准的命名惯例
description: 标准命名惯例既适用于在 AA Admin UI 中启用的变量名称本身，也适用于传递到维度中的值。
solution: Analytics
feature-set: Analytics
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10531.jpg
kt: 10531
exl-id: 79cec21e-2b52-4e7b-88ad-db137a8cef4e
source-git-commit: 058d26bd99ab060df3633fb32f1232f534881ca4
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 80%

---

# 创建标准的命名惯例

**内容：** 标准命名惯例既适用于变量名称本身，也适用于中 [!DNL Adobe Analytics] (AA)管理员UI和传递到维度的值。 （即，页面名称将“页面名称 (v1)作为变量名称，传入的页面名称值应统一一致，并遵循特定的结构/层级结构，如“站点名称 | 主页”或“站点名称 | 搜索 | 搜索结果”）。

**原因：**&#x200B;命名惯例是一种保持所有内容统一一致的好方法，可使界面易于用户理解。如果您从一开始就创建这些惯例，并在平台和代码中进行实施，则会更容易扩展。

**方法：**&#x200B;界面和标记文档应与“名称”和“描述”匹配，这样用户就不必调出 Excel 文档，并且可以直接在界面中理解您的数据。为了保持一致性，还建议将所有内容保持小写。

最好在整个平台上保持页面名称（或应用程序的屏幕名称）一致。例如，可以将“property :section:sub section:sub sub section:unique page name”设置为变量/维度。如果所有这些都是数据层中的单独字段，那么您甚至可以直接在 JS 文件/Launch 中生成页面名称。将所有这些元素设置为其各自的维度，可以帮助您更轻松地分解站点/应用程序的特定属性或区域，并更好地了解流量和流程。

任何有助于用户查找和理解数据的内容（包括一些简单的命名约定）都会增加的使用次数。 [!DNL Adobe Analytics] 并为业务提供更好的见解。

## 作者

本文件由以下人员共同编写：

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon，数字 [!DNL Analytics] NortonLifeLock平台经理
[!DNL Adobe Analytics] 冠军

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

 高级顾问 Rachel Fenwick[!DNL Adobe]
