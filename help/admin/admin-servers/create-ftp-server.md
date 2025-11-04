---
description: 使用Audience Manager管理工具中的“服务器”页面可创建新的FTP服务器或编辑现有服务器。
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new FTP server or to edit an existing server.
seo-title: Create or Edit an FTP Server
title: 创建或编辑FTP服务器
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
exl-id: 9eae4ecf-ccde-483a-ae53-1cbac033d8d6
source-git-commit: 92bf9b281c71e38d1bd5e0229f550a2124080b21
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 1%

---

# 创建或编辑FTP服务器 {#create-or-edit-an-ftp-server}

使用Audience Manager管理工具中的[!UICONTROL Servers]页面创建新的FTP服务器或编辑现有服务器。

>[!NOTE]
>
>您必须具有[!UICONTROL DEXADMIN]角色才能创建新服务器或编辑现有服务器。

1. 要创建新服务器，请单击&#x200B;**[!UICONTROL Servers]** > **[!UICONTROL Create Server]**。 要编辑现有服务器，请在&#x200B;**[!UICONTROL Label]**&#x200B;列中单击所需的服务器。
1. 为此服务器指定所需的标签。
1. 从&#x200B;**[!UICONTROL Protocol]**&#x200B;下拉列表中选择所需的协议： **FTP**。

   >[!NOTE]
   >
   >作为最佳实践，我们建议使用[!DNL Amazon S3]作为从合作伙伴获取文件并将文件传递给合作伙伴的方法。 [!DNL Amazon S3]提供了一个简单的Web服务界面，可用于随时随地从Web上存储和检索任意数量的数据。 有关详细信息，请参阅[Amazon用户指南](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html?lang=zh-Hans)中的&#x200B;*关于Audience Manager S3*。

1. 填写以下字段：

   * **[!UICONTROL Type]：**&#x200B;选择所需的加密类型： **[!UICONTROL SFTP]**&#x200B;或&#x200B;**[!UICONTROL FTPs/TLS]**。
   * **[!UICONTROL Domain]：**&#x200B;为此服务器指定所需的域（主机）。
   * **[!UICONTROL Port]：**&#x200B;为此服务器指定所需的端口。 将显示每种加密类型的默认端口。 您可以根据需要更改默认端口。
   * **[!UICONTROL Remote Path]：**&#x200B;为此服务器指定所需的远程路径。 如果将此字段留空，Audience Manager会将文件放置在默认目录中。
   * **[!UICONTROL .tmp File Rename on Completion]：**&#x200B;启用此选项以在完成时重命名`.tmp`文件。
   * **[!UICONTROL Filename Suffix]：**&#x200B;指定要附加以传输文件的文本。
   * **[!UICONTROL Moved to When Finished]：**&#x200B;指定要在完成时移动传输文件的位置的路径。
   * **[!UICONTROL Authentication]：**&#x200B;指定所需的服务器身份验证方法： **[!UICONTROL Username/Password]**&#x200B;或&#x200B;**[!UICONTROL SSH Key]**。

   >[!NOTE]
   >
   >请记得将我们的出口[!DNL FTP] [!DNL IP]添加到您的允许IP列表： **54.204.116.43**。

1. 对于&#x200B;**[!UICONTROL SSH Key]**&#x200B;身份验证：

   >[!NOTE]
   >
   >在配置SSH密钥身份验证时，请确保始终仅以OpenSSH格式生成公钥和私钥。

   1. 从任何[!DNL Linux]或[!DNL Mac]计算机生成公钥/私钥对。
   1. 将&#x200B;**公钥**&#x200B;提供给客户端在其[!DNL SFTP]服务器上更新。 它们必须包含其服务器上的公钥中的所有文本，包括`-----BEGIN RSA PRIVATE KEY-----`和`-----END RSA PRIVATE KEY-----` 。 作为交换，他们必须提供用于安装密钥的用户名。
   1. 使用客户端提供的用户名字段更新用户名字段，使用&#x200B;**私钥**&#x200B;更新密钥字段。

1. 如果要创建新服务器，请单击&#x200B;**[!UICONTROL Create]**；如果要编辑现有服务器，请单击&#x200B;**[!UICONTROL Update]**。
