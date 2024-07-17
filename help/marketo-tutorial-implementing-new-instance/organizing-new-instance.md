---
title: 组织新实例和建立命名约定
description: 了解如何在Marketo Engage实例中设置良好的组织，以便未来组织内的营销人员能够轻松浏览程序、修改资源和提取报表。
role: Admin
level: Beginner
doc-type: Article
solution: Marketo Engage
duration: 0
last-substantial-update: 2024-05-03T00:00:00Z
jira: KT-14813
thumbnail: KT-14813.jpeg
exl-id: 19b3de9e-53f3-4308-b46e-7b8f756c30a0
source-git-commit: e0d0c47eec98b7259363350d331ba69bbcaaa64b
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 2%

---

# 组织新实例和建立命名约定

作为实施新Marketo Engage实例的管理员，您将为将来允许组织内的营销人员轻松导航该实例奠定基础。 熟悉树文件夹结构和命名惯例可以使您的实例保持整洁并为长期成功做好准备。 本教程包含Adobe和Marketo Engage冠军(2019-2020) Natalie Kremer推荐的示例，可帮助您[统一组织文件夹并命名资源](https://nation.marketo.com/t5/champion-program-blogs/keep-marketo-engage-organized-with-folders-and-naming/ba-p/245630){target="_blank"}。

## 为何需要构造文件夹并应用命名约定？

通过在实例中保持井然有序，您和您的同事可以轻松跟踪活动、项目和资产并报告项目效果。 若要在实例中组织导航树并大规模生成，建议使用[文件夹](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/understanding-folders){target="_blank"}、[标准命名约定](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/programs/working-with-programs/best-practice-how-to-organize-your-programs#naming-schemes){target="_blank"}以及[克隆](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/programs/working-with-programs/best-practice-how-to-organize-your-programs#cloning){target="_blank"}等功能。

## 如何组织Marketo Engage实例

>[!VIDEO](https://video.tv.adobe.com/v/3421577/?quality=12&learn=on)

### 步骤1 — 设置文件夹结构以按顺序排列程序

组织实例的第一步是[设置文件夹结构](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/create-new-campaign-folder.html)以易于查找和有序的方式存放程序和资产。

在树中构造文件夹时，下面是一些快速提示：

* 保持平面文件夹结构以便可发现。
* 构建文件夹以反映组织的团队结构（例如区域或团队）或计划（例如新闻稿）。
* 包括基于时间标签，以启用可搜索性，并发出用于归档的适当定时的信号（例如2024）。
   * 建议管理员每年至少存档一次文件夹。 使用年度文件夹名称，您可以轻松停用实时智能营销活动并在年末存档整个文件夹。

以下是将这些提示付诸实践的文件夹示例。

树状结构中的&#x200B;**文件夹名称**

>[!BEGINTABS]

>[!TAB 营销活动]

![文件夹营销活动](/help/marketo-tutorial-implementing-new-instance/assets/folders-marketing-activities.png)

>[!TAB 设计工作室]

![文件夹设计工作室](/help/marketo-tutorial-implementing-new-instance/assets/folders-design-studio.png)

>[!TAB 数据库]

![文件夹数据库](/help/marketo-tutorial-implementing-new-instance/assets/folders-database.png)

>[!ENDTABS]

### 步骤2 — 在程序中生成文件夹

现在，让我们在项目级别应用文件夹结构。 作为最佳实践，将本地资产放在子文件夹中将有助于保持程序整洁并允许内部用户高效地修改或报告程序。 常见子文件夹包括电子邮件、登陆页、智能营销活动、列表、报告等。

**项目群中的文件夹名称**
* 营销活动 — *用于管理交互和状态跟踪的所有营销活动的文件夹。*
* 本地Assets - *此项目特定的所有资源的文件夹。*
   * 电子邮件
   * 登陆页面
   * 智能营销活动
   * 列表 — *仅当存在特定于程序的列表时才需要。*
   * Forms - *仅当存在特定于项目的Forms时才需要；大多数Forms都是全局Assets。*
   * 报告 — *仅当存在特定于项目的报告时才需要。*

### 步骤3 — 为项目和资产创建命名约定

在树中使用文件夹结构后，您需要以一致的方式命名项目和资产。 在这种情况下，标准化命名惯例将有助于在内部扩展命名流程。 以下是可用于建立命名惯例以确保可搜索性的几个组件：

* 计划类型缩写 — 电子邮件、内容、培养、网络研讨会等。
* 类别 — 计划类型 — 独立电子邮件、新闻稿等。
* 日期 — 项目群启动日期
* 简要说明 — 关于计划的简要说明

现在，我们将值放入公式中，并生成各种程序类型的程序名。

#### 程序命名公式

| **程序类型的缩写** | **YYYY** | **\-** | **毫米** | **\-** | **DD（可选）** | **类别** | **\-** | **计划的简要说明** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| EM — 电子邮件发送（电子邮件计划） | YYYY | \- | 毫米 | \- | DD（可选） | 类别 | \- | 项目简介 |
| NL — 新闻稿 | YYYY | \- | 毫米 | \- | DD（可选） | 类别 | \- | 项目简介 |
| ENG — 参与计划 | YYYY | \- | 毫米 | \- | DD（可选） | 类别 | \- | 项目简介 |
| WBN — 网络研讨会 | YYYY | \- | 毫米 | \- | DD（可选） | 类别 | \- | 项目简介 |
| IW — 交互式网络研讨会 | YYYY | \- | 毫米 | \- | DD（可选） | 类别 | \- | 项目简介 |
| TS — 贸易展 | YYYY | \- | 毫米 | \- | DD（可选） | 类别 | \- | 项目简介 |
| LE — 现场活动（路演） | YYYY | \- | 毫米 | \- | DD（可选） | 类别 | \- | 项目简介 |
| UG — 用户组 | YYYY | \- | 毫米 | \- | DD（可选） | 类别 | \- | 项目简介 |
| WC — 网站内容 | YYYY | \- | 毫米 | \- | DD（可选） | 类别 | \- | 项目简介 |
| CS — 内容联合 | YYYY | \- | 毫米 | \- | DD（可选） | 类别 | \- | 项目简介 |
| LI — 列表导入 | YYYY | \- | 毫米 | \- | DD（可选） | 类别 | \- | 项目简介 |
| OA — 在线Advertising | YYYY | \- | 毫米 | \- | DD（可选） | 类别 | \- | 项目简介 |
| PPC — 每次点击付费 | YYYY | \- | 毫米 | \- | DD（可选） | 类别 | \- | 项目简介 |

| **示例** |
| --- |
| ES 2023-10封闭式内容 — XYX白皮书 |
| WC-2023-10 — 每月网络研讨会 — ABC案例研究 |

#### 资产命名公式

从命名资产这一级别开始，最好不要重复程序名，并使用短标识符和通用标识符以便将来进行克隆。 请牢记以下一些快速提示：

* 根据资产在项目流程中的顺序对资产进行编号。
* 使用“ — ”（连字符）而不是“。”分隔命名组件。（点）或“\_”（下划线）。
   * 为什么？ Marketo Engage使用圆点将“项目名称”与“促销活动名称”隔开。 使用“\_”将阻止您在资产超链接时看到该标记。
* 在资产名称中使用标准首字母缩写可缩短引用并仍可轻松识别。

考虑到这些情况，我们将将这些提示应用于以下资产并创建公式以生成名称：

##### 根据项目流程中的顺序命名资产

| **程序进程中的序列** | **\-** | **描述** |
| --- | --- | --- |
| 01 | \- | 描述 |
| 02 | \- | 描述 |
| 03 | \- | 描述 |

| **示例：智能列表** |
| --- |
| 01 — 发送电子邮件 |
| 02 — 已打开 |
| 已单击03 |
| 04填写表单 |
| 05 — 影响（项目成功） |
| 06 — 已取消订阅 |

##### 使用资源类型的缩写命名资源

| **资源类型**&#x200B;的缩写 | **资源类型** | **\-** | **目标**&#x200B;的说明 |
| --- | --- | --- | --- |
| LP — 登陆页面 | LP | \- | 目标描述 |
| 电子邮件 — 电子邮件（出站） | EMAIL | \- | 目标描述 |
| 警报 — 电子邮件警报 | 警报 | \- | 目标描述 |
| WF - Web窗体 | WF | \- | 目标描述 |
| EXCL — 排除列表 | 不包括 | \- | 目标描述 |
| SLST — 智能列表 | SLST | \- | 目标描述 |
| LST — 静态列表 | LST | \- | 目标描述 |

| **示例** |
| --- |
| LP注册 |
| LP-ThankYou |
| 电子邮件出站 |
| 电子邮件新闻稿 |
| 电子邮件邀请 |
| 电子邮件提醒 |
| EXCL竞争对手 |

##### 使用资源类型的缩写命名可下载的文件(.pdf)

| **资源类型** | **内容描述** | **\-** | **资源类型**&#x200B;的缩写 | **.** | **PDF** |
| --- | --- | --- | --- | --- | --- |
| WP — 白皮书 | 内容描述 | \- | WP | 。 | pdf |
| CS — 案例研究 | 内容描述 | \- | CS | 。 | pdf |
| DS — 产品介绍 | 内容描述 | \- | DS | 。 | pdf |

| **示例：可下载的PDF文件** |
| --- |
| XYZ-Gadget-DS.pdf |
| Acme-Company-CS.pdf |
| How-XYZ-Gadgets-make-life-easier-WP.pdf |

>[!CAUTION]
>
>在命名上述示例中的文件时，请勿使用空格并避免使用下划线“\_”

## 接下来呢？

* 下载工作表：[Marketo Engage组织和命名约定](./assets/adobe-marketo-engage-organization-and-naming-conventions.xlsx){target="_blank"}以支持创建文件夹结构和命名约定。
* 在标准命名惯例中确定必要的组件后，请考虑将公式构建到Google工作表或Microsoft Excel中。 在以后使用时，只需在电子表格中输入您的值即可生成程序名。
* 在调整整个文件夹结构后，现在就可以根据最常见的用例和团队收到的最常见的请求来考虑您所需的模板。 然后，开始构建您的第一个项目模板。 阅读以开始使用[Adobe Marketo Engage计划模板](https://business.adobe.com/blog/how-to/get-started-with-marketo-engage-program-templates){target="_blank"}。

### 作者

{{natalie-kremer}}

{{amy-chiu}}
