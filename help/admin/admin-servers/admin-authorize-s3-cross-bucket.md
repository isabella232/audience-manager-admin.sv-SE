---
description: Vissa kunder kanske inte vill ge sina Amazon Simple Storage Service (Amazon S3) åtkomst eller hemliga nycklar till Adobe för att godkänna överföring av måldata till sina bukområden.
seo-description: Vissa kunder kanske inte vill ge sina Amazon Simple Storage Service (Amazon S3) åtkomst eller hemliga nycklar till Adobe för att godkänna överföring av måldata till sina bukområden.
seo-title: Så här auktoriserar du Amazon S3 Bucket-åtkomst för flera konton för batchdestinationer
title: Så här auktoriserar du Amazon S3 Bucket-åtkomst för flera konton för batchdestinationer
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# Så här auktoriserar du Amazon S3 Bucket-åtkomst för flera konton för batchdestinationer{#authorize-cross-account-bucket-batch}

Vissa kunder kanske inte vill ge sina [!DNL Amazon S3]-nycklar eller hemliga nycklar till Adobe för att tillåta överföring av måldata till sina bukområden.

Ett alternativ som vi kan erbjuda våra kunder är [!UICONTROL Cross-Account Bucket Permissions] i [!DNL Amazon S3]. Den här processen beskrivs i [AWS-dokumentationen](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html). Om du vill aktivera det här alternativet i Audience Manager följer du stegen nedan:

1. Gå till **[!UICONTROL Servers]** och välj **[!UICONTROL Create Server]**.
1. Välj **[!UICONTROL S3]** i listrutan **[!UICONTROL Protocol/Credentials]**.
1. Markera alternativet **[!UICONTROL Use Internal Adobe Key]**.
1. Använd kundens konto och bucket-namn i [!DNL Amazon S3].
1. Se till att din kund anger [!DNL Amazon S3]-kontot `975822914085` på sin [!DNL S3]-bucket.

>[!NOTE]
>
>Vår utgivare ser till att behörighetsnivån `bucket-owner-full-control` är inställd på överförda data, så att kunden kan äga dessa data.
