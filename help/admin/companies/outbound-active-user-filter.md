---
description: 按照以下说明生成仅包含最近活动用户的完整同步文件。 您可能需要筛选活动用户，以将相关数据推送到现场定位系统，或限制发送到DSP的文件的大小。 不能将此筛选器用于增量同步。
seo-description: Follow these instructions to generate a full synchronization file that includes recently active users only. You may want to filter for active users to push relevant data to an on-site targeting system or to limit the size of the files sent to a DSP. You cannot use this filter with incremental synchronization.
seo-title: Filter Outbound Data by Active Users Only
title: 仅按活动用户筛选出站数据
uuid: a2b4a385-eee3-458c-b978-09509cacb397
exl-id: d501cfd1-64dd-448e-92c5-180c0081d3e5
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 7%

---

# 仅按活动用户筛选出站数据 {#filter-outbound-data-by-active-users-only}

按照以下说明生成仅包含最近活动用户的完整同步文件。 您可能需要筛选活动用户，以将相关数据推送到现场定位系统，或限制发送到DSP的文件的大小。 不能将此筛选器用于增量同步。

>[!NOTE]
>
>访客无需出现在选定的客户网站上或其广告流量中，即可获得“活动”资格。 任何人都可以看到它们 [!DNL Audience Manager] 客户或合作伙伴，以符合“活动”资格。

要仅按活动用户筛选，请执行以下操作：

1. 单击 **[!UICONTROL Companies]**.
1. 选择要使用的公司，然后单击 **[!UICONTROL Destinations]**.
1. 在 [!UICONTROL Batch Data] 部分，设置以下选项：

   * **[!UICONTROL Sync Type]**：选择 **[!UICONTROL Customer]** 或 **[!UICONTROL Platform]**.
   * **[!UICONTROL Sync Type Lookback Period]**：此时间间隔定义数据文件的范围。 选项包括 **[!UICONTROL 24 hours]**， **[!UICONTROL 7 days]**， **[!UICONTROL 30 days]**.
   * **[!UICONTROL Incremental Sync Scheduled Run]**: Select **[!UICONTROL Never]**. 请记住，此过滤器仅适用于完整同步文件。
   * **[!UICONTROL Full Sync Scheduled Run]**：此值决定您接收此文件的频率。 选项包括 **[!UICONTROL 24 hours]**， **[!UICONTROL 7 days]**， **[!UICONTROL 30 days]**，或 **[!UICONTROL Never]** （禁用）。

1. 单击 **[!UICONTROL Save]**.
