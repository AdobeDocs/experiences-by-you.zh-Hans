---
title: 利用Dynamic Chat设计全渠道对话式营销
description: 快速开始使用Adobe Marketo Engage中的本机对话参与渠道Adobe Dynamic Chat设计对话营销。 本教程提供了实施用例的可操作方法，例如销售会议预订、网站内容参与和活动/网络研讨会促销。
role: Admin
level: Beginner
doc-type: Article
solution: Marketo Engage
duration: 0
last-substantial-update: 2024-05-23T00:00:00Z
jira: KT-14814
exl-id: 160dfb25-9f54-4dce-a08a-4a8d3c4c5368
source-git-commit: 1205848b1985a99b91f9d4d25e1a79f0df379589
workflow-type: tm+mt
source-wordcount: '1409'
ht-degree: 0%

---

# 利用Dynamic Chat设计全渠道对话式营销

营销人员、您的网站对于创造潜在客户、提高转化率和加快销售周期至关重要。 通过在您的网站上实时吸引访客，您的销售团队可以更有效地确定购买者的资格。 Adobe Dynamic Chat是Adobe Marketo Engage订阅中的本机聊天渠道，它使您能够自动进行对话以扩展Marketo Engage的功能。

本教程概述了Cornerstone OnDemand营销运营经理Sara Barriuso在“向同行学习”期间分享的思维过程和主要用例。 她解释了她的组织如何使用Dynamic Chat来最大限度地提高Marketo Engage的能力。

## 将对话参与集成到您的需求挖掘策略中

访客浏览您的网站是有原因的。 他们可能正在查找有关您的产品或服务的内容，或者寻找联系信息以便与您的销售代表交谈。 他们也可以是您的客户，正在寻找其他产品信息。 如果网站访客准备好与您的销售团队交谈，则通过聊天进行自助服务和自我认证。

当Sara Barriuso实现Dynamic Chat时，她被它与Marketo Engage和[预建活动触发器](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/dynamic-chat-activities){target="_blank"}的无缝集成所吸引，后者激活Marketo Engage程序，反之亦然。 她针对三个受众群体制定了对话式参与策略：

1. 未知的潜在客户：主动提供演示调用以生成新潜在客户。
2. 已知商机/客户：延长访客浏览内容所花费的时间，并提供演示调用以创造追加销售和交叉销售机会。
3. 潜在客户/客户：通过扩展营销活动的工作量来提供个性化的体验。


## 开始构建对话框的关键用例

为了实施这些策略，Sara围绕以下用例构建了她的Dynamic Chat对话框：

1. 默认全包对话框：为所有访客提供一个初始选项，指导他们更高效地完成任务。

2. 推广活动和网络研讨会注册：推动网站访客注册活动和网络研讨会，让他们更快地进入购买阶段。

3. 扩展促销活动内容参与：提供其他上下文或解决访客浏览网站内容时可能出现的问题。

让我们看一下这些用例的实际使用情况，Sara展示了她的流程，从规划对话流程到配置对话框以及在Dynamic Chat和Marketo Engage中进行定位。

### 用例1：所有网站访客的默认捕获全部对话框

此对话框提供五个初始选项供网站访客从中进行选择，从而创建自助式体验，帮助他们根据角色查找所需的信息。 首先，您可能需要浏览“联系我们”电子邮件收件箱，以确定常见主题并将它们归类到适用于网站访客的对话框选项中。 观看演示并按照以下步骤创建默认的“全包式”对话框：

>[!VIDEO](https://video.tv.adobe.com/v/3429194/?learn=on)

>[!BEGINTABS]

>[!TAB Dynamic Chat]

#### 阶段1

1. 构建对话框并创建测试链接。
2. 添加目标以跟踪转化（例如，演示请求提交）。
3. 让2-3人进行测试并收集反馈。

#### 阶段2

1. 在“受众”中，在“Target”中添加网页URL以指示将在何处显示对话框。
2. 在“设置”中，添加营销活动名称、描述、优先级和语言。
3. 单击“Publish”

>[!TAB Marketo Engage]

#### 阶段1

1. 创建您的跟踪Smart Campaign。
2. 在“智能列表”中，使用“实现对话框目标”触发器。 使用与Dialog相同的目标（例如演示请求）
3. 在“流量”中，包括一个“更改项目状态”步骤以跟踪转化。
4. 源将显示为“dynamicChat”。 您可以创建一个Smart Campaign，以将源更新到您认为合理的名称。

#### 阶段2

1. 在跟踪Smart Campaign上线后重新进行测试。

>[!ENDTABS]

#### 提升：基于帐户的营销

通过纳入行业目标内容，您可以进一步增强默认的全方位对话框，使对话对访客更有用。 例如，建议向访客下载行业特定的白皮书或案例分析。 观看演示，并按照以下步骤为基于帐户的营销创建默认的全方位对话框：

>[!VIDEO](https://video.tv.adobe.com/v/3429195/?learn=on)

>[!BEGINTABS]

>[!TAB Dynamic Chat]

1. 克隆“默认对话框”并重命名。
2. 在“流Designer”中，将Dialogue消息调整为目标行业（只有一个流+初始问题）。
3. 让2至3个人测试对话框并收集反馈。
4. 创建测试链接并共享它。
5. 在“受众”中，添加一个显示对话框的网页URL，并将目标更新到您想要的行业。
6. 在“设置”中，添加营销活动名称、描述优先级和语言。
7. 单击“Publish”。

>[!TAB Marketo Engage]

1. 创建跟踪Smart Campaign并测试目标。
2. 在发布对话框后重新测试跟踪Smart Campaign。

>[!ENDTABS]

### 用例2：推广活动和网络研讨会注册

活动和网络研讨会是B2B企业为创造需求而采用的流行营销策略。 他们提供引人入胜的体验和丰富的信息，吸引潜在客户。 将您的网站访客与即将举行的活动和网络研讨会连接起来，使您能够更快地确定潜在客户。 创建此对话框的工作量小，成本低，并且可以快速展示成功情况，帮助您获得营销利益相关者的支持，以将对话式参与添加到您的全渠道自动化计划中。 观看演示，并按照以下步骤创建活动/网络研讨会促销对话方块：

>[!VIDEO](https://video.tv.adobe.com/v/3429196/?learn=on)

>[!BEGINTABS]

>[!TAB Dynamic Chat]

#### 阶段1

1. 构建用于“事件注册”对话框的模板，以供持续营销活动使用。

#### 阶段2

1. 克隆模板。
2. 将文本复制并粘贴到新事件的对话框消息中
3. 更新事件链接中使用的UTM参数（例如utm_medium=website&amp;utm_source=adobe）。
4. 创建一个测试链接，单击“Publish”，然后与请求者共享。
5. 同行审查并应用反馈。


>[!TAB Marketo Engage]

#### 阶段1

1. 在网络研讨会/事件项目模板中创建跟踪Smart Campaign并对其进行测试。

#### 阶段2

1. 将您的营销活动名称添加到Marketo Engage中的跟踪智能营销活动并对其进行测试。

>[!ENDTABS]


#### 升级：注册已知人员

通过为网站访客注册参加您的活动和网络研讨会，无需他们填写表单，即可为他们提供更好的体验。 个性化的体验可建立信任并向访客展示您记住他们的情况。 我们来看看如何提升您的活动和网络研讨会促销对话的实际效果。

>[!NOTE]
>请思考某些保护州/国家涉及的潜在安全风险，并与您的法律团队协商后仔细实施此个性化。

>[!VIDEO](https://video.tv.adobe.com/v/3429197/?learn=on)

>[!BEGINTABS]

>[!TAB Dynamic Chat]

1. 克隆活动/网络研讨会提升对话框。
2. 在Designer流中，用户回答“是”后，添加一个问题卡“您之前与我们共享了您的电子邮件地址。 您想保留此项以详细了解活动吗？”
3. 如果他们回答“是”，请添加一张信息卡“您将在电子邮件中收到一封包含活动/网络研讨会详细信息的确认电子邮件”。
4. 如果他们回答“否” — 添加信息卡“请填写注册页面上的表格”。
5. 创建一个测试链接，单击“Publish”，然后与请求者共享。
6. 在“受众”选项卡中，添加[电子邮件不为空]。

>[!TAB Marketo Engage]

1. 将此新对话框添加到Marketo Engage中的跟踪Smart Campaign并对其进行测试。

>[!ENDTABS]

### 用例3：扩展营销活动内容参与

想象一下，一个迷人的橱窗显示器吸引你的眼球，把你吸引到一家商店里。 如果接待员随后帮助您选择产品或回答您的问题，您可能会觉得更适合购买产品。 要在线复制此体验，您可以在营销活动指导访客的网页上显示“Dynamic Chat”对话框。 当用户与Web内容互动时，Dynamic Chat会立即显示相关对话，从而建议其他内容或解决潜在问题。 这是通过利用自动化触发器根据Marketo Engage计划中的用户参与来激活Dynamic Chat活动来实现的。 现在，让我们看一看如何让此用例变得生动。

>[!VIDEO](https://video.tv.adobe.com/v/3429199/?learn=on)

扩展Campaign内容参与 — 配置：

>[!VIDEO](https://video.tv.adobe.com/v/3429200/?learn=on)

>[!BEGINTABS]

>[!TAB Dynamic Chat]

1. 通过电子邮件和社交营销活动的接触点，为您的营销活动生成新的潜在客户。 在此示例中，人才健康指数调查托管在品牌网站上。
2. 克隆现有对话框模板（例如，默认的“捕获全部”对话框）以为以下场景创建三个对话框，并相应地更新“受众”选项卡中的“目标URL”：
   * 当Web访客从您的营销渠道进入您的网页时。
   * 在感谢页面上
   * 任何在参与营销活动（重新定位）后45天内返回到您网站的访客

>[!ENDTABS]

## 接下来呢？

* 在[流Designer](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/automated-chat/stream-designer){target="_blank"}或流程图中离线绘制对话流。
* 在Dynamic Chat中创建默认的捕获所有对话框。
* 在Marketo Engage中使用自动触发器激活营销活动后参与对话。


## 作者

{{sara-barriuso}}

{{amy-chiu}}
