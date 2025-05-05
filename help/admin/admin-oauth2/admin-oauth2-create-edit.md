---
description: 使用“OAuth2客户端”页可查看Audience Manager配置中的OAuth2客户端列表。 只要分配了相应的用户角色，就可以编辑或删除现有客户机或创建新客户机。
seo-description: Use the OAuth2 Clients page to view a list of OAuth2 clients in your Audience Manager configuration. You can edit or delete existing clients or create new clients, providing that you have the appropriate user roles assigned.
seo-title: OAuth2 Clients
title: OAuth2客户端
uuid: 3e654053-fb2f-4d8f-a53c-b5c3b8dbdaaa
exl-id: 993eae04-02e8-4554-a6fe-cf599053bfc9
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 1%

---

# OAuth2客户端 {#oauth-clients}

使用[!UICONTROL OAuth2 Clients]页面查看[!DNL Audience Manager]配置中[!UICONTROL OAuth2]客户端的列表。 只要分配了相应的用户角色，就可以编辑或删除现有客户机或创建新客户机。

## 概述 {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>确保您的客户阅读《Audience Manager用户指南》中的[OAuth2](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html?lang=zh-Hans#oauth)文档。

[!DNL OAuth2]是一个开放标准，用于授权代表资源所有者提供对[!DNL Audience Manager]资源的安全委派访问权限。

![](assets/oauth.png)

您可以通过单击所需列的标题，按升序或降序对每个列进行排序。

使用列表底部的[!UICONTROL Search]框或分页控件查找所需的客户端。

## 创建或编辑OAuth2客户端 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

使用Audience Manager[!UICONTROL Admin]工具中的[!UICONTROL OAuth2 Clients]页创建新的[!UICONTROL Oauth2]客户端或编辑现有客户端。

1. 要创建新[!UICONTROL OAuth2]客户端，请单击&#x200B;**[!UICONTROL OAuth2 Clients]** > **[!UICONTROL Add OAuth2 Client]**。 要编辑现有的[!UICONTROL OAuth2]客户端，请在&#x200B;**[!UICONTROL Client ID]**&#x200B;列中单击所需的客户端。
1. 为此[!UICONTROL OAuth2]客户端指定所需的名称。 请注意，这是仅记录的名称。
1. 指定[!UICONTROL OAuth2]客户端的电子邮件地址。 电子邮件地址数量有限。
1. 从&#x200B;**[!UICONTROL Partner]**&#x200B;下拉列表中，选择所需的合作伙伴。
1. 在&#x200B;**[!UICONTROL Client ID]**&#x200B;框中，指定所需的ID。 这是提交[!DNL API]请求时使用的值。 在前一步骤的下拉列表中选择了[!UICONTROL Partner]后，当您开始键入时，前缀会自动填充。 正确的格式为&lt; *`partner subdomain`*> - &lt; *`Audience Manager username`*>。
1. 根据需要选中或取消选中&#x200B;**[!UICONTROL Restrict to Partner Users]**&#x200B;复选框。 如果选中此复选框，则该用户必须是为所选合作伙伴列出的[!DNL Audience Manager]用户。 作为最佳实践，我们建议您选择此选项。
1. 在&#x200B;**[!UICONTROL Scope]**&#x200B;部分中，根据需要选中或取消选中&#x200B;**[!UICONTROL Read]**&#x200B;和&#x200B;**[!UICONTROL Write]**&#x200B;复选框。
1. 在&#x200B;**[!UICONTROL Grant Type]**&#x200B;部分中，选择所需的授权方式。 我们建议您使用[!UICONTROL Password]和[!UICONTROL Refresh-token]选项的默认设置。

   * **[!UICONTROL Implicit]**：如果选择此选项，则会启用[!UICONTROL Redirect URI]框。 用户经过身份验证后会获得自动访问令牌，并且会立即发送到重定向[!DNL URI]。
   * **[!UICONTROL Authorization Code]**：如果选择此选项，则会启用[!UICONTROL Redirect URI]框。 用户经过身份验证后返回到客户端，然后发送到重定向[!DNL URI]。
   * **[!UICONTROL Password]**：使用用户输入的密码对用户进行身份验证，而不是通过授权服务器进行自动验证尝试。
   * **[!UICONTROL Refresh_token]**：用于刷新过期的访问令牌很长一段时间。

1. 在&#x200B;**[!UICONTROL Redirect URI]**&#x200B;框中，指定所需的[!DNL URI]。 仅当您选择&#x200B;**[!UICONTROL Implicit]**&#x200B;和&#x200B;**[!UICONTROL Authorization_code]**&#x200B;授权类型时，才会启用此选项。 **[!UICONTROL Redirect URI]**&#x200B;框允许您指定可接受[!DNL URI]值的逗号分隔值。 这是批准客户端访问[!DNL API]后，将其重定向到的客户端用户[!DNL URI]。
1. 为访问和刷新令牌过期指定所需的过期时间（以秒为单位）。

   * **[!UICONTROL Access Token Expiration Time]**：发出访问令牌后有效秒数。 可以为空以使用平台默认值（12小时）。 也可以为–1以指示访问令牌未过期。
   * **[!UICONTROL Refresh Token Expiration Time]**：刷新令牌发出后有效的秒数。 可以为空以使用平台默认值（30天）。

1. 单击 **[!UICONTROL Save]**。

要删除[!UICONTROL OAuth2]客户端，请单击&#x200B;**[!UICONTROL OAuth2 Clients]**，然后在&#x200B;**[!UICONTROL Actions]**&#x200B;列中单击所需客户端的![](assets/icon_delete.png)。

>[!MORELIKETHIS]
>
>* [API 要求和建议](../admin-oauth2/aam-admin-api-requirements.md)
