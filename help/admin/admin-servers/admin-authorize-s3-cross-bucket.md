---
description: 某些客户可能不希望提供其Amazon Simple Storage Service (Amazon S3)访问或密钥以Adobe授权将目标数据上传到其存储桶。
seo-description: Some customers may not want to provide their Amazon Simple Storage Service (Amazon S3) access or secret keys to Adobe to authorize destination data upload to their buckets.
seo-title: How To  Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations
title: 如何授权跨帐户Amazon S3存储段访问以实现批处理目标
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
exl-id: f3b97c31-714f-4841-884b-bc507267a932
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# 如何授权跨帐户Amazon S3存储段访问以实现批处理目标{#authorize-cross-account-bucket-batch}

某些客户可能不想提供其[!DNL Amazon S3]访问或密钥以Adobe授权将目标数据上传到其存储桶。

我们可以为客户提供替代方案是[!DNL Amazon S3]中的[!UICONTROL Cross-Account Bucket Permissions]。 [AWS文档](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html)中介绍了此过程。 要在Audience Manager中启用此替代方法，请执行以下步骤：

1. 转到&#x200B;**[!UICONTROL Servers]**&#x200B;并选择&#x200B;**[!UICONTROL Create Server]**。
1. 在&#x200B;**[!UICONTROL Protocol/Credentials]**&#x200B;下拉掩码中选择&#x200B;**[!UICONTROL S3]**。
1. 选中&#x200B;**[!UICONTROL Use Internal Adobe Key]**&#x200B;选项。
1. 在[!DNL Amazon S3]中使用客户的帐户和存储段名称。
1. 确保您的客户将[!DNL Amazon S3]帐户`975822914085`列入其[!DNL S3]存储段上的白名单。

>[!NOTE]
>
>我们的出站发布者确保针对已上传数据设置了权限级别`bucket-owner-full-control`，以便您的客户可以拥有该数据。
