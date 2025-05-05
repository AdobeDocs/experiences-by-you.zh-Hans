---
title: 本地CRM连接器的同步字段
description: 了解如何通过战略性选择供Marketo Engage使用的基本CRM字段来简化初始CRM集成。 执行数据字典练习，确定您需要用于平稳CRM同步的字段，以帮助您保持销售和营销团队的一致性。
role: Admin
level: Beginner
doc-type: Article
solution: Marketo Engage
duration: 0
last-substantial-update: 2024-05-04T00:00:00Z
jira: KT-14811
thumbnail: KT-14811.jpeg
exl-id: 42b7ca3d-e445-4c11-ad3d-d4e70c101c8e
source-git-commit: 1205848b1985a99b91f9d4d25e1a79f0df379589
workflow-type: tm+mt
source-wordcount: '1567'
ht-degree: 0%

---

# 本地CRM连接器的同步字段

您是否在组织中使用Salesforce或Microsoft Dynamics？ 如果是这样的话，借助Marketo Engage的本机CRM连接器(即Salesforce、Microsoft Dynamics和Veeva)，您可以通过在Marketo Engage和CRM之间无缝共享相关信息来协调营销和销售活动。 在配置初始CRM同步之前，请确保确定要在两个系统之间同步的字段，以保持Marketo Engage数据库干净。

详细了解如何使用Adobe Professional Services建议的最佳实践来进行此练习。 请跟着了解标准字段和自定义字段，并记录它们在Marketo Engage与您的CRM之间的关系。

## 在将CRM与Marketo Engage集成之前，识别要同步的字段

在将CRM与Marketo Engage集成时，您可能不需要同步所有要Marketo Engage的CRM字段。 从战略角度考虑所需的字段可帮助您的Marketo Engage实例更有效地处理数据流。

您的Marketo Engage与CRM系统之间的初始同步将自动关联大部分现有的标准字段（即电子邮件、名字/姓氏、公司等）。 此外，连接器还通过在Marketo Engage中创建自动映射到您CRM中的这些字段的新字段，为您的潜在客户、联系人、客户和商机同步[自定义字段](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/administration/field-management/custom-field-type-glossary){target="_blank"}。

在执行初始同步之前，确定并组织要从CRM同步的字段，是本机连接器设置过程中的关键步骤。 我们称之为数据字典练习，可帮助您最大限度地减少创建的重复字段数，并使任何后续的重新映射步骤尽可能顺畅地进行。 本练习通常涉及营销和销售团队以及您的CRM管理员的输入，以确保只有相关字段会同步到您的Marketo Engage实例。

## 构建数据字典

通常，最佳实践是仅同步营销所需的CRM字段。 从本练习开始，整理CRM中需要映射到Marketo Engage的字段，并在第一次正确运行初始CRM同步。

>[!NOTE]
>如果您的CRM中存在自定义字段，则在开始初始Marketo Engage之前该字段中已具有相同的自定义字段，则会在Marketo Engage中为CRM字段创建一个新的“重复”字段。 您可以将CRM字段重新映射到原始Marketo Engage字段，并在初始同步完成后隐藏重复字段，但您需要联系[Adobe客户支持](https://experienceleague.adobe.com/zh-hans/docs/customer-one/using/home#create-a-support-ticket-with-admin-console){target="_blank"}以执行此操作。 有关更多详细信息，请参阅步骤7。

**步骤1：**&#x200B;构建CRM中当前可用字段的粗略列表，并标记是否要在Marketo Engage中显示这些字段。

* 在决策过程中包含CRM管理员、营销和销售团队的反馈。
* 记录每个字段的API名称和字段类型
* 确定这些字段应该具有的访问Marketo Engage级别（即只读或读写）


**步骤2：**&#x200B;查看Marketo Engage实例的[管理员>字段管理部分](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/administration/field-management/view-field-mappings-between-marketo-and-salesforce){target="_blank"}，以识别先前在系统中直接创建并要包含在同步中的任何自定义字段。

* 记录每个字段的API名称和字段类型。
* 表示您的CRM中已具有等效字段的字段。
* 表示您的CRM中没有等效字段的字段。


**步骤3：**&#x200B;开始使用默认映射字段构建数据字典

* 由于Marketo Engage使用平面数据库，因此建议按如下方式设置数据字典的格式：

   * 第一列：Marketo Engage字段名称
   * 第二列：Marketo EngageAPI名称
   * 第三列：[Marketo Engage字段类型](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/administration/field-management/custom-field-type-glossary){target="_blank"}（即布尔值、货币、日期等）
   * 在后续列中，对CRM对象类型(Lead、Contact、Account、Opportunity)重复显示一个附加列，用于显示您希望Marketo Engage具有的访问权限级别（即，读取、写入、编辑）

  <br>

  以下是它的外观示例：
  ![数据字典表](/help/marketo-tutorial-implementing-new-instance/assets/data_dictionary.png){width="100%" zoomable="yes"}


* 首先，添加将为您的CRM自动映射的默认字段：

   * [Salesforce](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/default-salesforce-field-mapping){target="_blank"}
   * [Microsoft Dynamics](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/microsoft-dynamics-sync-details/default-dynamics-field-mapping){target="_blank"}
   * [Veeva](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/veeva-crm-sync/sync-details/default-veeva-field-mapping){target="_blank"}

* 确认Marketo Engage中的每个默认字段与要与同步的CRM中的字段匹配。 例如，Marketo Engage中的“已取消订阅”字段可能是CRM中的“电子邮件选择退出”字段。
* 根据需要调整CRM API名称、权限和[数据类型](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/administration/field-management/custom-field-type-glossary){target="_blank"}。

**步骤4：**&#x200B;向数据字典添加其他字段

* 包括显示名称、所需的CRM权限以及每个字段的数据类型。
* 如果某个字段在CRM中存在，但不在Marketo Engage中，请用CRM字段中的相同值填充Marketo Engage显示和API名称。
* 如果某个字段存在于Marketo Engage中而不是CRM中，请使用所需的值填充CRM显示名称，但将CRM API名称保留为空，直到创建该字段为止。
* 如果两个系统中都存在等效字段，请将它们包含在同一行中，并指明需要在“数据字典”工作表最右侧的“注释”部分重新映射它们。

>[!NOTE]
>如果您计划创建同步筛选器字段([Salesforce](https://nation.marketo.com/t5/product-blogs/instructions-for-creating-a-custom-sync-rule/ba-p/242758){target="_blank"}) | [Microsoft Dynamics](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/custom-dynamics-sync-filter-details/create-a-custom-dynamics-sync-filter){target="_blank"})，请确保将其包含在此步骤中，但将API名称保留为空，直到在CRM中创建该字段为止。

**步骤5：**&#x200B;与您的CRM管理员一起查看数据字典

* 在CRM中为Marketo Engage中已存在的字段创建字段，并使用新CRM字段的显示名称和API名称更新数据字典。
* 在CRM ([Salesforce](https://nation.marketo.com/t5/product-blogs/instructions-for-creating-a-custom-sync-rule/ba-p/242758){target="_blank"})中的潜在客户和联系人对象之间执行字段映射 | [Microsoft Dynamics](https://community.dynamics.com/blogs/post/?postid=8a91d93e-2181-45dd-a8fb-1092010bc8f1){target="_blank"})。 当Lead转化为Contact时，这将确保这些字段可以合并为Marketo Engage中的单个字段。
* 确保Marketo同步配置文件具有数据字典中所述的每个字段的适当权限：
   * [在Salesforce中设置配置文件权限](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/salesforce-sync/setup/enterprise-unlimited-edition/step-2-of-3-create-a-salesforce-user-for-marketo-enterprise-unlimited#set-profile-permissions){target="_blank"}
   * [在Microsoft Dynamics中设置配置文件权限](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/microsoft-dynamics-365-with-s2s-connection/step-2-of-3-set-up#create-application-user-in-microsoft){target="_blank"}
   * [在Veeva中设置配置文件权限](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/veeva-crm-sync/setup/step-2-of-3-create-a-veeva-crm-user-for-marketo-engage#set-profile-permissions){target="_blank"}

**步骤6：**&#x200B;执行初始同步

* 确保您要与Marketo Engage同步的所有字段在CRM中具有数据字典定义的相应权限。
* 确保在Marketo同步配置文件[&#128279;](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/hide-a-salesforce-field-from-the-marketo-sync){target="_blank"}中将隐藏您希望&#x200B;**不**&#x200B;与Marketo Engage同步的所有字段。 在以后向同步中添加新字段比删除意外同步的字段要容易得多。
* 您是否正在将您的CRM与同步筛选器字段连接？ 如果同步到Salesforce，请联系Adobe客户支持，以确保在开始初始同步之前已启用筛选功能。


**步骤7：**&#x200B;查看Marketo Engage中的“字段管理”部分

* 确认/更新新同步字段的显示和API名称。
* 识别任何可能需要重新映射的重复字段。 在以下几种情况中，会出现重复字段：
   * 如果Marketo Engage中已存在对等字段，则CRM中的自定义字段会在首次同步时在Marketo Engage中创建新的（可能重复的）字段。
   * 仅Marketo参与自定义字段(即直接在Marketo Engage中创建的字段)，并且您可能具有从CRM同步的等效字段。



**步骤8：**&#x200B;如果出现重复的字段，请联系Adobe客户支持以执行重新映射

* 对于需要重新映射的字段，请与支持人员联系并提供以下信息：
   * CRM创建的新重复字段的显示和API名称。
   * 要将CRM字段映射到的Marketo Engage字段的显示名称。
   * 请参阅此示例[此处](https://nation.marketo.com/t5/knowledgebase/re-mapping-sfdc-marketo-fields/ta-p/299284){target="_blank"}。
* 重新映射完成后，查看Marketo Engage中重新映射字段的API名称，并更新数据字典的“API名称”列中的值，以确保它包含最准确的信息。

## 接下来呢？

* 构建数据字典以整理CRM集成的字段。
* 熟悉CRM的初始同步过程

>[!BEGINTABS]

>[!TAB Salesforce]

了解Marketo Engage和Salesforce如何协同工作，保持销售和营销数据同步。

>[!VIDEO](https://video.tv.adobe.com/v/3424719/?learn=on)

+++视频中使用的&#x200B;**链接：**

* [了解Salesforce同步](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/salesforce-sync/understanding-the-salesforce-sync){target="_blank"}

* [将Marketo字段添加到Salesforce (Enterprise/Unlimited)](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/salesforce-sync/setup/enterprise-unlimited-edition/step-1-of-3-add-marketo-fields-to-salesforce-enterprise-unlimited){target="_blank"}

* [在Salesforce (Enterprise/Unlimited)中创建Marketo用户](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/salesforce-sync/setup/enterprise-unlimited-edition/step-2-of-3-create-a-salesforce-user-for-marketo-enterprise-unlimited){target="_blank"}

* [连接Marketo和Salesforce(Enterprise/Unlimited)](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/salesforce-sync/setup/enterprise-unlimited-edition/step-3-of-3-connect-marketo-and-salesforce-enterprise-unlimited){target="_blank"}

* [用户需要先在Salesforce端设置连接的应用程序，然后才能转到Marketo和Salesforce Sync。](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/salesforce-sync/log-in-using-oauth-2-0){target="_blank"}

* [Salesforce同步状态](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/salesforce-sync/salesforce-sync-status){target="_blank"}

* [隐藏和取消隐藏字段](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/administration/field-management/hide-and-unhide-a-field){target="_blank"}

* [教程：了解如何将Marketo同步到CRM](https://experienceleague.adobe.com/zh-hans/docs/marketo-learn/tutorials/lead-and-data-management/crm-sync-learn){target="_blank"}

+++

>[!TAB Microsoft Dynamics]

了解Microsoft Dynamics 365同步的工作方式并正确配置设置，以允许两个系统相互交谈。

>[!VIDEO](https://video.tv.adobe.com/v/3424737/?learn=on)

+++视频中使用的&#x200B;**链接：**

* [了解Microsoft Dynamics同步](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"}

* [下载Marketo潜在客户管理解决方案](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/download-the-marketo-lead-management-solution){target="_blank"}

* [更新Microsoft Dynamics的Marketo解决方案](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/update-the-marketo-solution-for-microsoft-dynamics){target="_blank"}

* [同意客户端ID和应用程序注册](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/grant-consent-for-client-id-and-app-registration)

* [验证Microsoft Dynamics同步](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/validate-microsoft-dynamics-sync){target="_blank"}

* [同步状态](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/microsoft-dynamics-sync-details/sync-status){target="_blank"}

* [修复Dynamics验证同步问题](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/fix-dynamics-validation-sync-issues){target="_blank"}

* [创建自定义Dynamics同步筛选器](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/custom-dynamics-sync-filter-details/create-a-custom-dynamics-sync-filter.html?lang=zh-Hans){target="_blank"}

* [查看组织服务URL](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/view-the-organization-service-url){target="_blank"}

* 在Dynamics中删除字段之前[正在编辑要同步的字段](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/microsoft-dynamics-sync-details/editing-fields-to-sync-before-deleting-them-in-dynamics){target="_blank"}

* [教程：了解如何将Marketo同步到CRM](https://experienceleague.adobe.com/zh-hans/docs/marketo-learn/tutorials/lead-and-data-management/crm-sync-learn){target="_blank"}

+++

>[!ENDTABS]

### 作者

{{peter-livadas}}

{{amy-chiu}}
