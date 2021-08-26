---
description: Använd serversidan i administrationsverktyget för Audience Manager för att skapa en ny S3-server eller för att redigera en befintlig server.
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new S3 server or to edit an existing server.
seo-title: Create or Edit an S3 Server
title: Skapa eller redigera en S3-server
uuid: 94fee787-eb26-45aa-b602-d61ab12969ea
exl-id: 89310de0-e24e-4d4b-8171-56faf0b441f6
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 5%

---

# Skapa eller redigera en S3-server {#create-or-edit-an-s-server}

Använd sidan [!UICONTROL Servers] i administrationsverktyget för Audience Manager om du vill skapa en ny [!DNL S3]-server eller redigera en befintlig server.

>[!NOTE]
>
>Du måste ha rollen [!UICONTROL DEXADMIN] för att kunna skapa nya servrar eller redigera befintliga servrar.

1. Om du vill skapa en ny server klickar du på **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Om du vill redigera en befintlig server klickar du på önskad server i kolumnen **[!UICONTROL Label]**.
1. Ange önskad etikett för den här servern.
1. Välj önskat protokoll i listrutan **[!UICONTROL Protocol]**: **[!UICONTROL S3]**.

   >[!NOTE]
   >
   >Vi rekommenderar att du använder [!DNL Amazon S3] som en metod för att hämta filer från och leverera filer till partners. [!DNL Amazon S3] har ett enkelt webbtjänstgränssnitt som kan användas för att lagra och hämta data när som helst, var som helst på webben. Mer information finns i [Om Amazon S3](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html) i *användarhandboken för Audience Manager*.

1. Fyll i fälten:

   * **[!UICONTROL Account]:** Ange önskat  [!DNL S3] konto.
   * **[!UICONTROL Bucket]:** Ange önskad  [!DNL S3] bucket.
   * **[!UICONTROL Directory]:** Ange önskad  [!DNL S3] katalog.
   * **[!UICONTROL Access Key]:** Ange önskad  [!DNL S3] åtkomstnyckel.
   * **[!UICONTROL Secret Key]:** Ange önskad  [!DNL S3] hemlig nyckel.

1. Klicka på **[!UICONTROL Create]** om du skapar en ny server eller klicka på **[!UICONTROL Update]** om du redigerar en befintlig server.
