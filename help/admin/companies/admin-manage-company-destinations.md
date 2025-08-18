---
description: 创建、编辑和删除Audience Manager目标。
seo-description: Create, edit, and delete Audience Manager destinations.
seo-title: Manage Company Destinations
title: 管理公司目标
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
exl-id: a2e73613-07cd-4ab8-8c6e-be451ed50bfc
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '1061'
ht-degree: 0%

---

# 管理公司目标 {#manage-company-destinations}

创建、编辑和删除Audience Manager目标。

<!-- t_company_destinations.xml -->

有关详细信息，请参阅[Audience Manager用户指南](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/destinations.html)中的&#x200B;*目标*。

## 创建或编辑公司目标 {#create-edit-company-destinations}

浏览各个部分，获取有关如何创建新的[!DNL Audience Manager]目标或编辑现有目标的分步说明。

<!-- create-edit-company-destinations.xml -->

在设置目标之前，请访问[Experience Cloud合作伙伴集成页面](https://wiki.corp.adobe.com/x/mPIMPw)。 该页面包含您需要为每个[!DNL Audience Manager]合作伙伴集成填写的特定信息。

如果您的客户端希望使用[!DNL Adobe Media Optimizer]作为[!DNL Audience Manager]中的目标，则需要在[!DNL Adobe Media Optimizer]中设置此设置。

## 导航到目标选项卡 {#navigate-destinations}

1. 单击&#x200B;**[!UICONTROL Companies]**，然后找到并单击所需的公司以显示其[!UICONTROL Profile]页面。 您可以使用[!UICONTROL Search]框或列表底部的分页控件来查找所需的公司。 您可以通过单击所需列的标题，按升序或降序对每个列进行排序。
1. 单击&#x200B;**[!UICONTROL Destinations]**&#x200B;选项卡。
1. 要创建新目标，请单击&#x200B;**[!UICONTROL Add Destination]**。 要编辑现有目标，请在&#x200B;**[!UICONTROL Name]**&#x200B;列中单击目标的名称。

## 基本设置 {#basic-settings}

填写&#x200B;**[!UICONTROL Basic Settings]**&#x200B;窗口中的字段。

* **[!UICONTROL Name]：** （必需）指定此目标的名称。
* **[!UICONTROL Description]：**&#x200B;指定有关此目标的描述性信息。
* **[!UICONTROL Type]：**（必需）选择所需的目标类型：
   * **[!UICONTROL Bulk ID]**：在不同平台之间同步ID。
   * **[!UICONTROL Bulk Trait]**：将特征信息批量发送到不同的平台。
   * **[!UICONTROL Bulk Segment]**：将区段信息批量发送到不同的平台。
   * **[!UICONTROL S2S]**：使用服务器到服务器目标将实时数据和批量数据发送到不同的平台。
* **[!UICONTROL Auto-Fill Destination Mapping]：** （仅限[!UICONTROL S2S]）选择一个选项：
   * **[!UICONTROL Segment ID]：**&#x200B;如果选择此设置，则目标值映射将使用[!DNL Audience Manager]区段ID填充。
   * **[!UICONTROL Integration Code Value]：**&#x200B;如果选择此设置，则目标值映射将使用[!DNL Audience Manager]段集成代码填充。
* **[!UICONTROL User ID Key]：**（必需）从下拉列表中选择此目标所需的用户ID密钥。

此ID用作主数据源ID。 这会确定文件中要退出的用户ID。

>[!NOTE]
>
>对于[!UICONTROL Bulk ID]目标类型，不能使用[!DNL Audience Manager] [!UICONTROL User ID]或[!DNL Adobe Experience Cloud] ID。

如果您的数据源ID ([!UICONTROL DPID])未显示在下拉列表中，则必须选中&#x200B;**[!UICONTROL Outbound]**&#x200B;数据Source设置页面[上的数据源级别的](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/manage-datasources.html)复选框。

* **[!UICONTROL Target Data Source]：**（必需）从下拉列表中选择此目标所需的数据源。 此设置允许标记出站数据，允许将出站数据摄取到客户端的单独系统中。
* **[!UICONTROL Foreign Account ID]：**&#x200B;指定此目标的外部帐户ID。 这是收件人系统中此出站数据的标识值。
* **[!UICONTROL Outbound Sample Rate Denominator]：**&#x200B;当返回的数据总量未知时，使用此设置仅返回样本数据量，而不是全部数据量。 调整此处的数字以表示数据的一部分（例如，值“100”返回常规数据量的1/100，值“10”返回常规数据量的1/10）。 默认值为“1”，这将返回所有数据。

## 实时数据（用于S2S目标） {#realtime-s2s}

如果您正在创建[!UICONTROL S2S]目标，请填写以下字段：

**[!UICONTROL Servers]**：为此目标选择所需的`HTTP`服务器。
**[!UICONTROL Format]**：从下拉列表中选择此目标所需的格式： [!UICONTROL HTTP only]。

>[!NOTE]
>
>仅对于[!DNL S2S]，您可以使用屏幕关闭/开启滑块启用或禁用[!UICONTROL Realtime]或[!UICONTROL Batch]目标。 不能同时禁用这两个选项。

## 批量数据 {#batch-data}

对于[!UICONTROL Bulk ID]、[!UICONTROL Bulk Trait]或[!UICONTROL Bulk Segment]目标，请填写以下字段：

* **[!UICONTROL Protocol]**：（必需）从下拉列表中选择此目标的所需协议：
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**：（必需）从下拉列表中选择此目标所需的服务器。
* **[!UICONTROL Format]**：（必需）根据以上选择的协议，从下拉列表中选择此目标的所需格式： [!DNL HTTP]或文件类型。
* **[!UICONTROL Sync Type]**： （必需）为此目标选择所需的同步类型。 这表示客户端要包含在出站订单中的用户活动级别。 如果客户端只想从其属性分析区段资格，请选择&#x200B;**[!UICONTROL Customer]**。 如果他们想要在所有&#x200B;**[!UICONTROL Platform]**&#x200B;客户中包含来自站外活动的区段资格，请选择[!DNL Audience Manager]。
* **[!UICONTROL Customer]**：文件包含的活动用户仅在选定时间段的客户端属性（与客户端的[!UICONTROL PID]关联）上实现至少1个特征。 您的客户应使用此选项将其&#x200B;*实时*&#x200B;区段资格出站到目标。
* **[!UICONTROL Platform]**：文件包含的活动用户至少在1个实时交互中，无论是ID同步还是特征实现，在选定时间段内，在所有[!DNL Audience Manager]客户端属性（与所有客户端PID关联）中的任何位置。 您的客户应使用此选项将其总计&#x200B;*个*&#x200B;区段资格出站到目标。
* **[!UICONTROL Lifetime]**：文件包含自目标创建以来在所有[!DNL Audience Manager]客户端属性中看到的活动用户。
* **[!UICONTROL Sync Type Lookback Period]**：如果您选择[!UICONTROL Customer]或[!UICONTROL Platform]，请选择一个时间段。 文件包含选定时间段的活动用户。
接下来，选择订单类型。 这指示与合作伙伴的每次出站集成的频率和范围。 在增量订单和完整订单之间进行选择。
* **[!UICONTROL Incremental Scheduled Run]**：每次运行时，[!DNL Audience Manager]将只出站自上次出站订单以来符合条件的净新用户。 选择您希望[!DNL Audience Manager]执行增量同步进程的所需时间段。 例如，您可以选择每24小时、每7天、每30天或从不。

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>第一个递增订单等于完整订单，因为从未将任何先前用户发送到目标。

* **[!UICONTROL Full Sync Scheduled Run]**：每次运行时，[!DNL Audience Manager]将出站自目标首次设置以来的所有活动用户。 选择您希望[!DNL Audience Manager]用于执行完整同步进程的所需计划。 例如，您可以选择每24小时、每7天、每30天或从不。

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>我们建议使用增量同步的频率高于完全同步。 增量同步仅发送包含新特征实现或ID同步的文件。 完全同步会发送所有文件，无论它们是否包括新的实现或ID同步。 只有在客户端需要其所有用户的完整副本时才使用[!UICONTROL Full Sync Scheduled Run]配置，以减少出站数据量。

## 配置数据源 {#configure-data-sources}

对于[!UICONTROL Bulk ID]、[!UICONTROL Bulk Trait]或[!UICONTROL Bulk Segment]目标，请填写以下字段。 这些设置允许您发送与数据源关联的所有数据（特征、区段或ID，基于所选类型）。

* **[!UICONTROL All Unrestricted First Party Data]**：选择以使用所有第一方数据源。 如果选择此选项，则会禁用[!UICONTROL Available Data Sources]选项。
* **[!UICONTROL Available Data Sources]**：使用箭头在&#x200B;**[!UICONTROL Available Data Sources]**&#x200B;和&#x200B;**[!UICONTROL In File Data Sources]**&#x200B;框之间移动数据源。

## 保存并完成 {#save-and-finalize}

填写完所有必填字段后激活&#x200B;**[!UICONTROL Save]**&#x200B;按钮。 单击&#x200B;**[!UICONTROL Save]**&#x200B;以完成创建目标进程。

## 删除公司目标 {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

要删除目标，请执行以下操作：

1. 单击&#x200B;**[!UICONTROL Companies]**，找到并单击所需的公司，然后单击&#x200B;**[!UICONTROL Destinations]**&#x200B;选项卡。
1. 在所需目标的![](assets/icon_delete.png)列中单击&#x200B;**[!UICONTROL Actions]**。
1. 单击&#x200B;**[!UICONTROL OK]**&#x200B;以确认删除。

>[!NOTE]
>
>如果目标具有映射到它的区段，则无法删除目标。
