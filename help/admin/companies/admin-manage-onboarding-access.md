---
description: 为了防止文件和数据意外载入其他合作伙伴或客户拥有的目标数据源，Audience Manager在合作伙伴ID (PID)与其他合作伙伴拥有的数据源之间添加了映射要求。
title: 管理对第二方数据的载入访问
exl-id: 03bec978-dd31-41cc-a3aa-d67fbb98963c
source-git-commit: cc04863272005964cfbf1bb2319cc0dd86863680
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# 管理对第二方数据的载入访问 {#manage-onboarding-access-for-second-party-data}

>[!IMPORTANT]
>
> 此页面的受众是Adobe内部员工。 如果您是Audience Manager客户，正在请求此页所述的第二方数据源映射，请联系客户关怀团队或您的技术客户经理。
> 请注意，不需要请求现有数据共享关系的映射。 将数据载入属于您的PID的目标数据源时，也不需要映射。

为了防止文件和数据意外载入其他合作伙伴拥有的目标数据源，Audience Manager在合作伙伴ID (PID)和其他合作伙伴拥有的数据源(DPID)之间添加了映射要求。 有关PID和DPID的更多信息，请参阅 [AUDIENCE MANAGERID](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html).

出于第二方数据共享的目的，如果Audience Manager合作伙伴或客户希望将文件摄取到他们并不拥有的目标数据源中，则需要请求在其合作伙伴ID (PID)与该特定数据源(DPID)之间进行映射。 如果缺少映射，集客数据作业将不会处理文件，并且数据也不会载入Audience Manager中。

要创建该映射，请向Audience Manager工程团队提交Jira票证。 查看示例Jira票证 [此处](https://jira.corp.adobe.com/browse/AAM-60353). 您无需请求为任何现有数据共享关系创建映射。
