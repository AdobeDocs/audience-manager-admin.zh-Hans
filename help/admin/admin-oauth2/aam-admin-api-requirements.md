---
description: 您应当鼓励客户在使用Audience Manager API时注意的事项。
seo-description: Things you should encourage your clients to be aware of when they're working with the Audience Manager APIs.
seo-title: API Requirements and Recommendations
title: API要求和建议
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
exl-id: 24f90732-31a6-436d-862b-e6871d279c7a
TQID: https://experienceleague.adobe.com/mm5-TOwj8WckXoG4-E4wzuEF-1oBbxbBUvRLOoA--As
product_v2:
  - id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
feature_v2:
  - id: baaa0dd2-d27e-4921-aae3-7888623a5fa5
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 350
ht-degree: 0%

---

# API要求和建议 {#api-requirements-and-recommendations}

您应当鼓励客户在使用Audience Manager [!DNL API]时注意的事项。

## 要求 {#requirements}

使用[!DNL Audience Manager] [!DNL API]代码时请注意以下事项：

* **请求参数：**&#x200B;除非另有指定，否则所有请求参数都是必需的。
* **[!DNL JSON]内容类型：**&#x200B;在您的代码中指定`content-type: application/json` *和* `accept: application/json`。

* **请求和响应：**&#x200B;将请求作为正确格式化的[!DNL JSON]对象发送。 [!DNL Audience Manager]使用[!DNL JSON]格式的数据进行响应。 服务器响应可以包含请求的数据、状态代码或同时包含这两者。

* **访问：**&#x200B;您的[!DNL Audience Manager]顾问将为您提供客户端ID和密钥，以便您发出[!DNL API]请求。

* **文档和代码示例：**&#x200B;斜体&#x200B;*中的文本*&#x200B;表示在生成或接收[!DNL API]数据时提供或传入的变量。 将&#x200B;*斜体*&#x200B;文本替换为您自己的代码、参数或其他必需的信息。

## 推荐：创建通用API用户 {#recommendations}

我们建议创建一个单独的技术用户帐户来使用Audience Manager [!DNL API]。 这是一个通用帐户，它与客户组织中的特定用户无关，也与特定用户关联。 此类型的[!DNL API]用户帐户可帮助完成2件事：

* 识别正在调用[!DNL API]的服务（例如，从使用我们的[!DNL API]的客户端应用或进行批量更改的调用）。
* 提供对[!DNL API]的无中断访问。 与特定员工关联的帐户可能在他们离开公司时删除。 这会阻止您的客户使用可用的[!DNL API]代码。 不绑定到特定员工的通用帐户有助于避免此问题。

作为此类帐户的示例或用例，假设您的客户希望使用[批量管理工具](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/bulk-management-tools/bulk-management-intro.html?lang=en)一次更改多个区段。 为此，他们需要[!DNL API]访问权限。 不要向特定用户添加权限，而是创建一个非特定的[!DNL API]用户帐户，该帐户具有进行[!DNL API]调用所需的相应凭据、密钥和密钥。 如果客户端开发自己的使用[!DNL Audience Manager] [!DNL API]的应用程序，这也很有用。
