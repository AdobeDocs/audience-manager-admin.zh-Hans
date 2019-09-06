---
description: 创建、编辑和删除Audience Manager目标。
seo-description: 创建、编辑和删除Audience Manager目标。
seo-title: 管理公司目标
title: 管理公司目标
uuid: d9a6bffb1-7629-44e0-b7 d7-heg44 f65 ea2 b
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# 管理公司目标 {#manage-company-destinations}

创建、编辑和删除Audience Manager目标。

<!-- t_company_destinations.xml -->

有关详细信息，请参阅 [Audience](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html) *Manager用户指南*&#x200B;中的目标。

## 创建或编辑公司目标 {#create-edit-company-destinations}

滚动各个章节，以了解有关如何创建新 [!DNL Audience Manager] 目标或编辑现有目标的分步说明。

<!-- create-edit-company-destinations.xml -->

在设置目标之前访问 [Experience Cloud合作伙伴集成页面](https://wiki.corp.adobe.com/x/mPIMPw) 。该页面包含您需要为每个 [!DNL Audience Manager] 合作伙伴集成填写的特定信息。

如果客户希望将 [!DNL Adobe Media Optimizer] 其用作目标， [!DNL Audience Manager] 您需要设置此设置 [!DNL Adobe Media Optimizer]。

## Navigate to the Destinations Tab {#navigate-destinations}

1. 单击 **[!UICONTROL Companies]**，然后找到并单击所需的公司以显示其 [!UICONTROL Profile] 页面。您可以使用 [!UICONTROL Search] 列表底部的框或分页控件找到所需的公司。您可以单击所需列的标题，以升序或降序排列每个列。
1. Click the **[!UICONTROL Destinations]** tab.
1. 要创建新目标，请单击 **[!UICONTROL Add Destination]**。To edit an existing destination, click the destination's name in the **[!UICONTROL Name]** column.

## 基本设置 {#basic-settings}

Fill in the fields in the **[!UICONTROL Basic Settings]** window.

* **[!UICONTROL Name]：** (必需)指定此目标的名称。
* **[!UICONTROL Description]：** 指定有关此目标的描述性信息。
* **[!UICONTROL Type]：** (必需)选择所需的目标类型：
   * **[!UICONTROL Bulk ID]**：在不同平台之间同步ID。
   * **[!UICONTROL Bulk Trait]**：将特征信息批量发送到不同平台。
   * **[!UICONTROL Bulk Segment]**：将细分信息批量发送到不同平台。
   * **[!UICONTROL S2S]**：使用服务器到服务器目标将实时数据和批量数据发送到不同平台。
* **[!UICONTROL Auto-Fill Destination Mapping]：** ( [!UICONTROL S2S] 仅)选择一个选项：
   * **[!UICONTROL Segment ID]：** 如果您选择此设置，则使用 [!DNL Audience Manager] 区段ID填充目标值映射。
   * **[!UICONTROL Integration Code Value]：** 如果您选择此设置，目标值映射将填充 [!DNL Audience Manager] 区段集成代码。
* **[!UICONTROL User ID Key]：** (必需)从下拉列表中为此目标选择所需的用户ID密钥。

此ID用作主数据源ID。这会确定用户ID要超出文件中的限制。

>[!NOTE]
>
>[!UICONTROL Bulk ID] 对于目标类型，您无法使用 [!DNL Audience Manager][!UICONTROL User ID] 或 [!DNL Adobe Experience Cloud] ID。

如果您的数据源ID( [!UICONTROL DPID])未显示在下拉列表中，则必须在“ **[!UICONTROL Outbound]**[数据源设置”页面](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/data-sources/manage-datasources.html)上的数据源级别选中该复选框。

* **[!UICONTROL Target Data Source]：** (必需)从下拉列表中选择此目标所需的数据源。此设置支持标记出站数据，允许在客户端将其引入不同系统。
* **[!UICONTROL Foreign Account ID]：** 指定此目标的外键ID。这是接收方系统中此限制数据的标识值。
* **[!UICONTROL Outbound Sample Rate Denominator]：** 当返回的数据总量未知时，使用此设置只返回样本数量的数据，而不是完全返回。在此处调整数字以表示部分数据(例如，值'100'返回1/100的常规数据量，值'10'返回1/10的常规数据)。默认值为“1”，返回所有数据。

## 实时数据(针对S2S目标) {#realtime-s2s}

如果要创建 [!UICONTROL S2S] 目标，请填写以下字段：

**[!UICONTROL Servers]**：为此目标选择所需 `HTTP` 的服务器。
**[!UICONTROL Format]**：从下拉列表中选择此目标所需的格式： [!UICONTROL HTTP only]。

>[!NOTE]
>
>仅限， [!DNL S2S] 您可以使用屏幕关闭/开启滑块启用或禁用目标或 [!UICONTROL Realtime][!UICONTROL Batch] 目标。您无法禁用这两个选项。

## 批处理数据 {#batch-data}

对于或 [!UICONTROL Bulk ID][!UICONTROL Bulk Trait][!UICONTROL Bulk Segment] 目标，填写以下字段：

* **[!UICONTROL Protocol]**：(必需)从下拉列表中为该目标选择所需的协议：
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**：(必需)从下拉列表中为此目标选择所需的服务器。
* **[!UICONTROL Format]**：(必需)从下拉列表中选择此目标所需的格式： [!DNL HTTP] 或文件类型，具体取决于您选择的协议。
* **[!UICONTROL Sync Type]**：(必需)为此目标选择所需的同步类型。这表示客户端希望包含在出站订单中的用户活动级别。选择 **[!UICONTROL Customer]** 客户端是否仅有意分析其属性中的区段资格。选择 **[!UICONTROL Platform]** 是否希望包括所有 [!DNL Audience Manager] 客户跨现场活动的细分资格。
* **[!UICONTROL Customer]**：文件包含在选定时间段内仅在客户端属性(与客户端关联)上具有至少个 [!UICONTROL PID]特征的活动用户。您的客户应使用此选项超越其 *对目标* 的实时细分资格。
* **[!UICONTROL Platform]**：文件包含至少在选定时间段内所有 [!DNL Audience Manager] 客户端属性(与所有客户端PiPID关联)的实时交互的有效用户，即ID同步或特征实现。客户应使用此选项将 ** 其总细分资格超出目标。
* **[!UICONTROL Lifetime]**：文件包含自创建目标后所有 [!DNL Audience Manager] 客户端属性中都看到的活动用户。
* **[!UICONTROL Sync Type Lookback Period]**：如果您选择 [!UICONTROL Customer] 或 [!UICONTROL Platform]，请选择一段时间。在选定的时间段内，文件包含活动用户。
接下来，选择顺序类型。这表示与合作伙伴的每个出站集成的频率和范围。在增量和完整订单之间进行选择。
* **[!UICONTROL Incremental Scheduled Run]**：每次运行 [!DNL Audience Manager] 时，只会超出上一个出站订单后符合资格的新用户的数量。选择要 [!DNL Audience Manager] 执行增量同步流程的所需时间段。例如，您可以每隔24小时、每七天、每30天或从不选择一次。

>[!NOTE] {重要性=“high”}
>
>首次递增的订单相当于完整订单，因为以前没有任何一个用户发送到目标。

* **[!UICONTROL Full Sync Scheduled Run]**：每次运行 [!DNL Audience Manager] 时，将在第一次设置目标后，出站所有活动用户。选择要用于执行完全 [!DNL Audience Manager] 同步流程的所需计划。例如，您可以每隔24小时、每七天、每30天或从不选择一次。

>[!NOTE] {重要性=“high”}
>
>我们建议比完全同步更频繁地使用增量同步。增量同步只会发送包含新特征真实性或ID同步的文件。完全同步会发送所有文件，无论它们是否包括新的实码或ID同步。仅当客户端需要完整的所有用户副本时使用 [!UICONTROL Full Sync Scheduled Run] 配置，以减少出站数据量。

## 配置数据源 {#configure-data-sources}

对于或 [!UICONTROL Bulk ID][!UICONTROL Bulk Trait][!UICONTROL Bulk Segment] 目标，填写以下字段。这些设置允许您发送与数据源关联的所有数据(特征、区段或ID)。

* **[!UICONTROL All Unrestricted First Party Data]**：选择以使用所有第一方数据源。如果选择此选项，则 [!UICONTROL Available Data Sources] 禁用选项。
* **[!UICONTROL Available Data Sources]**：使用箭头在和 **[!UICONTROL Available Data Sources]****[!UICONTROL In File Data Sources]** 框之间移动数据源。

## 保存并完成 {#save-and-finalize}

填写所有必需字段后， **[!UICONTROL Save]** 将激活该按钮。单击 **[!UICONTROL Save]** 以完成创建目标进程。

## 删除公司目标 {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

删除目标：

1. 单击 **[!UICONTROL Companies]**，找到并单击所需的公司，然后单击 **[!UICONTROL Destinations]** 选项卡。
1. 单击 ![](assets/icon_delete.png) 所需目标 **[!UICONTROL Actions]** 的列。
1. Click **[!UICONTROL OK]** to confirm the deletion.

>[!NOTE]
>
>如果目标已映射到区段，则无法删除目标。