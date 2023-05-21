---
description: Vissa kunder kanske inte vill ge sina Amazon Simple Storage Service (Amazon S3) åtkomst eller hemliga nycklar till Adobe för att godkänna överföring av måldata till sina bukområden.
seo-description: Some customers may not want to provide their Amazon Simple Storage Service (Amazon S3) access or secret keys to Adobe to authorize destination data upload to their buckets.
seo-title: How To  Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations
title: Så här auktoriserar du Amazon S3 Bucket-åtkomst för flera konton för batchdestinationer
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
exl-id: f3b97c31-714f-4841-884b-bc507267a932
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Så här auktoriserar du Amazon S3 Bucket-åtkomst för flera konton för batchdestinationer{#authorize-cross-account-bucket-batch}

Vissa kunder kanske inte vill tillhandahålla sina [!DNL Amazon S3] åtkomst eller hemliga nycklar till Adobe för att tillåta överföring av måldata till deras bucket.

Ett alternativ som vi kan erbjuda våra kunder är [!UICONTROL Cross-Account Bucket Permissions] in [!DNL Amazon S3]. Den här processen beskrivs i [AWS-dokumentation](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html). Om du vill aktivera det här alternativet i Audience Manager följer du stegen nedan:

1. Gå till **[!UICONTROL Servers]** och markera **[!UICONTROL Create Server]**.
1. Välj **[!UICONTROL S3]** i **[!UICONTROL Protocol/Credentials]** nedrullningsbar mask.
1. Kontrollera **[!UICONTROL Use Internal Adobe Key]** alternativ.
1. Använd kundens konto och bucket-namn i [!DNL Amazon S3].
1. Se till att kunden hittar de vita listorna [!DNL Amazon S3] konto `975822914085` på [!DNL S3] bucket.

>[!NOTE]
>
>Vår utgående utgivare ser till att behörighetsnivån `bucket-owner-full-control` är inställt på överförda data, så att kunden kan äga dessa data.
