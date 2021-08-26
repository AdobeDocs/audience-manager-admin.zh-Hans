---
description: 测试版环境用于测试Audience Manager实施。 测试版中所做的更改不会影响生产数据。 Audience Manager测试版环境是生产环境的较小规模的独立版本。 必须在此环境中输入和收集您要测试的所有数据。
seo-description: The beta environment is for testing Audience Manager implementations. Changes made in beta do not affect production data. The Audience Manager beta environment is a smaller-scale, standalone version of the production environment. All the data that you want to test must be entered and collected in this environment.
seo-title: Beta Environment
solution: Audience Manager
title: 测试版环境
uuid: 6a253f4e-96e7-4395-a783-a8eb213b7daf
exl-id: 78d5a1ff-c016-4366-ba34-9814a0d92067
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 3%

---

# 测试版环境 {#beta-environment}

测试版环境用于测试Audience Manager实施。 测试版中所做的更改不会影响生产数据。 Audience Manager测试版环境是生产环境的较小规模的独立版本。 必须在此环境中输入和收集您要测试的所有数据。

## 概述 {#overview}

<!-- beta_environment_admin.xml -->

| 服务 | URL/主机名 | 配置步骤 |
|--- |--- |--- |
| S3 |  | 请参阅[配置Amazon S3存储段](admin-beta-environment.md#provision-s3-buckets)。 |
| DCS | https&amp;amp；冒号；//dcs-beta.demdex.net/.. | 我们这边不需要额外的步骤。 请参阅[在测试版环境中访问DCS](admin-beta-environment.md#access-dcs-beta-environment)。 |
| 用户界面 | https&amp;amp；冒号；//bank-beta.demdex.com | 数据会按月从生产环境复制到测试环境。 生产凭据对测试版有效。 |
| API | https&amp;amp；冒号；//api-beta.demdex.com/... | 数据会按月从生产环境复制到测试环境。 生产凭据对测试版有效。 |

## 配置Amazon S3存储段 {#provision-s3-buckets}

>[!NOTE]
>
>我们将不再使用[!DNL FTP/SFTP]。 此外，请注意，出站数据传输不适用于测试版环境。

要为集客数据配置[!DNL S3]存储段，请执行以下操作：

1. 使用&#x200B;[**SKMS请求技术运营帮助**](https://skms.adobe.com/)功能。
1. 转到左导航边栏中的&#x200B;**[!UICONTROL Request TechOps Help]**。
1. 在&#x200B;**[!UICONTROL Request Search]**&#x200B;的搜索字段中键入Audience Manager。
1. 在搜索结果中向下滚动，然后单击&#x200B;**Audience Manager- S3入站/出站帐户配置**。
1. 填写预配窗口中的字段，并在&#x200B;**[!UICONTROL Environment]**&#x200B;字段中指定&#x200B;**沙盒环境**。

>[!NOTE]
>
>我们阻止使用[!DNL FTP/SFTP]，并鼓励使用[!UICONTROL Amazon S3]。 [Amazon S3:About](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html)中列出了我们鼓励使用[!UICONTROL Amazon S3]的原因。

## 在测试版环境中访问DCS {#access-dcs-beta-environment}

要访问测试版环境中的[!UICONTROL DCS]，请执行以下操作：

1. 使用[!DNL curl] [命令](https://curl.haxx.se/docs/manpage.html)进行[!UICONTROL DCS]调用。 [!DNL Curl] 是使用多种受支持协议之一从服务器向服务器传输数据的工具。

   例如：`curl -v https://dcs-beta.demdex.net/event`

1. 通过在[!UICONTROL DCS]响应标头中查找“[!DNL sandbox]”，验证测试版[!UICONTROL DCS]是否为您的请求提供了。

   例如：

   ```
   curl -v http://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```

<!--
1. Determine the load balancer's endpoint IP addresses.

   Run the `dig` [command](https://en.wikipedia.org/wiki/Dig_(command)) to determine the IP address of the nearest load balancer. The `dig` command queries the Domain Name System and returns the name and IP addresses of the Audience Manager [!UICONTROL Data Collection Servers (DCS)].

   ```
   dig dcs-beta.demdex.net
   ...
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.87.15.51
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 50.16.150.8
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.2.228.100
   ```

1. Using one of the addresses in the above table, add a static DNS entry in the [!DNL `/etc/hosts`] file.

   On Windows, modify [!DNL `c:\WINDOWS\system32\drivers\etc\hosts`].

   For example:

[!DNL `52.87.15.51 samplepartner.demdex.net`]

   >[!NOTE]
   >
   >The addresses change occasionally, so you must keep your [!DNL /etc/hosts] file up to date.

   Additionally, if you need to set up ID synchronization, you must add a similar entry for [!DNL dpm.demdex.net.]

[!DNL `52.87.15.51 dpm.demdex.net`] [!DNL]. 

1. Make a [!UICONTROL DCS] call, using the `curl` [command](https://curl.haxx.se/docs/manpage.html). Curl is a tool to transfer data from or to a server, using one of many supported protocols.

   For example:

[!DNL `https://<domain>/event?product=camera`] 

1. Verify that your request was served by the beta [!UICONTROL DCS] by looking for "sandbox" in the [!UICONTROL DCS] response header.

   For example:

   ```
   curl -v https://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```
-->
