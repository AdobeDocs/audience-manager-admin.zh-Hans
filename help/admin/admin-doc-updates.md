---
description: 按日期显示《Audience Manager 管理指南》的所有更新（内容添加、删除和更正）。
seo-description: All updates (additions, deletions, and corrections) to the Audience Manager Admin Guide, by date.
seo-title: Documentation Updates
title: 文档更新
uuid: 1c02dff5-8e3f-42bf-a50c-03b75e121ac7
exl-id: 8221b4df-99c2-47d3-a2ea-186a701a2b20
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 94%

---

# 文档更新 {#documentation-updates}

按日期显示《Audience Manager 管理指南》的所有更新（内容添加、删除和更正）。

有关功能发布、增强和错误修复的信息，请参阅 [Experience Cloud 发行说明](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=zh-Hans)。有关[!DNL Audience Manager]文档更改，请参阅[文档更新](https://experienceleague.adobe.com/docs/audience-manager/user-guide/documentation-updates/docs-2019.html?lang=zh-Hans)。

## AAM 2019年文档更新 {#aam-2019-docs-updates}

| 主题 | 描述 |
|--- |--- |
| HTTP 格式宏 | 我们向 `USER_LIST` 宏添加了一个新宏 `REGION_ID_LIST` 以及三个新字段 `sda`、`sda` 和 `sda`。 |
| HTTP 格式宏 | 我们添加了两个新宏：`ECID` 和 `MCID`。 |

## AAM 2018年文档更新 {#aam-2018-docs-updates}

<!-- c_doc_updates.xml -->

<table id="table_AECF59E131F84E7791A5A421BFB203FA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 主题 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/create-ftp-server.md#task_BF1DD0E5ECA64AEC87EACABFCAEA2C6D">创建或编辑 FTP 服务器</a> </p> </td> 
   <td colname="col2"> <p>我们添加了更多有关 SFTP 服务器的 SSH 密钥身份验证的信息（步骤 5）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-destination-troubleshooting.md#set-up-destinations-export">如何设置目标以导出 Experience Cloud...</a> </p> </td> 
   <td colname="col2"> <p>本页面向您展示如何设置目标，以导出“出站数据文件”中依赖于您所需 ID 类型的数据。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/admin-authorize-s3-cross-bucket.md#task_20B12994C5484A9D8CC40DF6F456CBE7">操作方法：授权跨帐户 Amazon S3 存储段访问以实现批处理目标</a> </p> </td> 
   <td colname="col2"> <p>如果您的客户不想共享 Amazon S3 访问密钥和密码密钥，则可以在 Amazon S3 中使用跨帐户存储段权限来传输出站数据文件。本文档说明了如何在 Audience Manager 管理 UI 中设置此替代方法。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2017年文档更新 {#aam-2017-docs-updates}

<table id="table_81D2DA9293A9417085C630D00A7C96E1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 主题 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE"> HTTP 格式宏</a> </td> 
   <td colname="col2">已使用 <code>legacySegmentId</code> 替换了 <code>segmentId</code> 宏，并且添加了 <code>newSegmentId</code> 宏。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-company-limits.md#task_3004C10CB9A9430A8D25E25BB830B5D6">管理公司限制</a> </td> 
   <td colname="col2"> 在限制文档中增加了最大特征文件夹数量和特征结构深度。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="formats/enable-outbound-seq.md#concept_526744C9433F40BF8269E18245B2F0BD"> 为出站启用 Hadoop 序列文件传输</a> </td> 
   <td colname="col2"> 了解如何让客户将出站 SEQ 文件发送到他们自己的 Hadoop 实例。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967">管理容器</a> </td> 
   <td colname="col2"> 添加了有关如何创建容器的简短说明。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-manage-company-destinations.md#create-edit-company-destinations">创建或编辑公司目标</a> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_527E0E75C03846B0AB39EEE544904BE2"> 
      <li id="li_FC276B34158D44E3A5450C6C8BAF3184">添加了有关平衡完全同步和增量同步使用的说明。 </li> 
      <li id="li_3975DA78DE9E441D8F8CB80F752DD7B7">在 <span class="keyword">Adobe Media Optimizer</span> 中完成了将 <span class="keyword">Adobe Media Optimizer</span> 配置为 <span class="keyword">Audience Manager</span> 目标的操作。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> 管理公司目标</a> </p> </td> 
   <td colname="col2"> <p>较小的修改。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-amo-sync.md#concept_2B5537233DAA4860B3503B344F937D83">ID 与 Media Optimizer 同步</a> </p> </td> 
   <td colname="col2"> <p>介绍每个公司容器中 AMO 同步复选框的新文档。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-device-graph-options.md#concept_563615F1018340C683E0EE075F8F639D"> 适用于公司的设备图选项</a> </p> </td> 
   <td colname="col2"> <p>介绍如何配置设备图选项的新文档。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-oauth2/aam-admin-api-requirements.md#concept_A7FAC9443CF34974A873E6B787616421"> API 要求和建议</a> </p> </td> 
   <td colname="col2"> <p>这是一个新文档，介绍了一些需要了解并传递给客户的要求和建议。它在具有相同标题的公共文档中有所重复，而且它针对不同的阅读群体进行了更改。请参阅公共文档中的 <a href="https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html?lang=zh-Hans#api-requirements-recommendations" format="https" scope="external">API 要求和建议</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2016年文档更新 {#aam-2016-docs-updates}

<table id="table_E9D9810EA8244B58A4F27D56CFE521FD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 主题 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="admin-servers/create-ftp-server.md#task_BF1DD0E5ECA64AEC87EACABFCAEA2C6D"> 创建或编辑 FTP 服务器</a> </td> 
   <td colname="col2">添加了出口 FTP IP <b>52.44.29.204</b>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations">管理公司目标</a> </p> </td> 
   <td colname="col2"> <p>较小的修改。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/create-http-server.md#task_5BF59581868E4144B965D644D36BEACD">创建或编辑 HTTP 服务器</a> </p> </td> 
   <td colname="col2"> <p>向“创建服务器配置”向导添加了 <b>HTTP 签名</b>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-beta-environment.md#concept_4AA12E66F49A452C8BA4E91AA28060AA"> 测试版环境</a> </p> </td> 
   <td colname="col2"> <p>更新了测试版环境中的 URL 和主机名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/outbound-active-user-filter.md#task_F5CF8BDDA5DB4D23837B59CADF7A623B">仅按活动用户筛选出站数据</a> </p> </td> 
   <td colname="col2"> <p>有关生成只包含活动用户的完整同步文件的说明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE"> HTTP 格式宏</a> </p> </td> 
   <td colname="col2" morerows="1"> <p>列出了 HTTP 宏和常见示例的新文档。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31">HTTP 格式宏示例</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2015年文档更新 {#aam-2015-docs-updates}

<table id="table_90F524BAAED44A45A1F6BF8BBA9F26F9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 日期和主题 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>2015 年 12 月 </p> <p><a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> 格式</a> </p> </td> 
   <td colname="col2"> <p>修订了宏部分并添加了一些示例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2014年文档更新 {#aam-2014-docs-updates}

<table id="table_FA9962E19248418BA73D5A794A378C9D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 日期和主题 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>2014 年 11 月 12 日 </p> <p> <a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> 格式</a> </p> </td> 
   <td colname="col2"> <p>添加了有关 &lt;MCID&gt; 宏的信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014 年 10 月 23 日 </p> <p><a href="formats/admin-create-format.md#task_1A51FC9189DB439FB218D91F3875FD67">创建或编辑格式</a> </p> </td> 
   <td colname="col2"> <p>添加了有关 <span class="wintitle">.info 接收</span>选项的信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014 年 10 月 23 日 </p> <p><a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> 格式</a> </p> </td> 
   <td colname="col2"> <p>新页面。请注意，此页面正在创建中，将在未来几天内进行更新。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014 年 10 月 22 日 </p> <p><a href="admin-destination-troubleshooting.md#">目标设置疑难解答</a> </p> </td> 
   <td colname="col2"> <p>新主题。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014 年 10 月 21 日 </p> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> 管理公司目标</a> </p> </td> 
   <td colname="col2"> <p>重写了整个主题。添加了其他信息和其他设置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014 年 9 月 25 日 </p> <p><a href="companies/admin-manage-company-profiles.md">创建公司</a> </p> </td> 
   <td colname="col2"> <p>向<span class="wintitle">生命周期</span>和<span class="wintitle">帐户类型</span>部分添加了其他信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014 年 9 月 25 日 </p> <p><a href="companies/admin-manage-company-profiles.md#edit-company-profile">编辑公司配置文件</a> </p> </td> 
   <td colname="col2"> <p>向<span class="wintitle">生命周期</span>和<span class="wintitle">帐户类型</span>部分添加了其他信息。 </p> </td> 
  </tr> 
 </tbody> 
</table>
