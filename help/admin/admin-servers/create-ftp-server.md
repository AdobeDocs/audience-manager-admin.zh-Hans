---
description: 使用“Audience Manager管理工具”中的“服务器”页面创建新的FTP服务器或编辑现有服务器。
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new FTP server or to edit an existing server.
seo-title: Create or Edit an FTP Server
title: 创建或编辑 FTP 服务器
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
exl-id: 9eae4ecf-ccde-483a-ae53-1cbac033d8d6
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 4%

---

# 创建或编辑 FTP 服务器 {#create-or-edit-an-ftp-server}

使用“Audience Manager管理工具”中的[!UICONTROL Servers]页面创建新的FTP服务器或编辑现有服务器。

>[!NOTE]
>
>要创建新服务器或编辑现有服务器，您必须具有[!UICONTROL DEXADMIN]角色。

1. 要创建新服务器，请单击&#x200B;**[!UICONTROL Servers]** > **[!UICONTROL Create Server]**。 要编辑现有服务器，请在&#x200B;**[!UICONTROL Label]**&#x200B;列中单击所需的服务器。
1. 为此服务器指定所需的标签。
1. 从&#x200B;**[!UICONTROL Protocol]**&#x200B;下拉列表中，选择所需的协议：**FTP**。

   >[!NOTE]
   >
   >作为最佳实践，我们建议使用[!DNL Amazon S3]作为从合作伙伴获取文件并将文件交付到合作伙伴的方法。 [!DNL Amazon S3] 提供简单的web服务界面，可用于随时从Web上的任意位置存储和检索任意数量的数据。有关更多信息，请参阅《Amazon用户指南》**&#x200B;中的[关于Audience ManagerS3](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html)。

1. 填写以下字段：

   * **[!UICONTROL Type]:** 选择所需的加密类型： **[!UICONTROL SFTP]** 或 **[!UICONTROL FTPs/TLS]**。
   * **[!UICONTROL Domain]:** 为此服务器指定所需的域（主机）。
   * **[!UICONTROL Port]:** 为此服务器指定所需的端口。每种加密类型均显示默认端口。 如有必要，可以更改默认端口。
   * **[!UICONTROL Remote Path]:** 为此服务器指定所需的远程路径。如果将此字段留空，则Audience Manager会将文件放在默认目录中。
   * **[!UICONTROL .tmp File Rename on Completion]:** 启用此选项可在完成时 `.tmp` 重命名文件。
   * **[!UICONTROL Filename Suffix]:** 指定要附加到传输文件的文本。
   * **[!UICONTROL Moved to When Finished]:** 指定完成时希望传输文件移动到的位置的路径。
   * **[!UICONTROL Authentication]:** 指定所需的服务器身份验证方法： **[!UICONTROL Username/Password]** 或 **[!UICONTROL SSH Key]**。

   >[!NOTE]
   >
   >请记住将我们的出口[!DNL FTP] [!DNL IP]添加到允许的IP列表中：**52.44.29.204**。

1. 对于&#x200B;**[!UICONTROL SSH Key]**&#x200B;身份验证：
   >[!NOTE]
   >
   >配置SSH密钥身份验证时，请确保始终仅以OpenSSH格式生成公钥和私钥。
   1. 从任何[!DNL Linux]或[!DNL Mac]计算机中生成公钥/私钥对。
   1. 将&#x200B;**公钥**&#x200B;赋给客户端，以在其[!DNL SFTP]服务器上进行更新。 它们必须包含来自其服务器上公钥的所有文本，包括`-----BEGIN RSA PRIVATE KEY-----`和`-----END RSA PRIVATE KEY-----` 。 作为交换，用户必须提供用于安装密钥的用户名。
   1. 使用客户端提供的用户名字段更新用户名字段，使用&#x200B;**私钥**&#x200B;更新键字段。
1. 如果要创建新服务器，请单击&#x200B;**[!UICONTROL Create]**；如果要编辑现有服务器，则单击&#x200B;**[!UICONTROL Update]**。
