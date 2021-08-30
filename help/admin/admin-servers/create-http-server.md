---
description: Använd serversidan i administrationsverktyget för Audience Manager för att skapa en ny HTTP-server eller för att redigera en befintlig server.
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new HTTP server or to edit an existing server.
seo-title: Create or Edit an HTTP Server
title: Skapa eller redigera en HTTP-server
uuid: 1ef0e751-e239-4dc6-a4f6-73cc05686807
exl-id: 8b3dfb1e-2dee-4a05-835e-3c32643336bc
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 3%

---

# Skapa eller redigera en HTTP-server {#create-or-edit-an-http-server}

Använd sidan [!UICONTROL Servers] i administrationsverktyget för Audience Manager om du vill skapa en ny HTTP-server eller redigera en befintlig server.

>[!NOTE]
>
>Du måste ha rollen [!UICONTROL DEXADMIN] för att kunna skapa nya servrar eller redigera befintliga servrar.

1. Om du vill skapa en ny server går du till **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Om du vill redigera en befintlig server klickar du på önskad server i kolumnen **[!UICONTROL Label]**.
1. Ange önskad etikett för den här servern.
1. Välj önskat protokoll i listrutan **[!UICONTROL Protocol]**: [!DNL HTTP].
1. Fyll i fälten:

   * **[!UICONTROL Domain]:** Ange önskad domän (värd) för den här servern.
   * **[!UICONTROL Port]:** Ange önskad port för den här servern. Standardporten visas för varje krypteringstyp. Du kan ändra standardporten om det behövs
   * **[!UICONTROL Maximum Users Per Request]:** Ange maximalt antal användare per begäran som tillåts för den här servern.
   * **[!UICONTROL URL Prefix]:** Ange det  [!DNL URL] prefix som ska användas för den här servern.
   * **[!UICONTROL Authentication URL]:** Ange  [!UICONTROL Authentication URL] för den här  `HTTP` servern.
   * **[!UICONTROL Authentication]:** Ange önskad autentiseringsmetod:  **[!UICONTROL None]**,  **[!UICONTROL Username/Password]** eller  **[!UICONTROL SSH Key]**.
   * **[!UICONTROL HTTP Signature Header]:** Namnet på det  [!DNL HTTP] huvud som kunden anger som innehåller  [!DNL HTTP] signaturnyckeln. Standardvärdet är [!UICONTROL X-Signature], vilket visas i exemplet nedan:

      ```
      * Connected to partner.website.com (127.0.0.1) port 80 (#0)
      > POST /webpage HTTP/1.1
      > Host: partner.host.com
      > Accept: */*
      > Content-Type: application/json
      > Content-Length: 20
      > X-Signature: wxa2ByMWhhP328EvHQsVlOD5jTc=
      POST message content
      ```

   * **[!UICONTROL HTTP Signature Key]:** Nyckeln som används för att signera  [!DNL HTTP] begäran, som tillhandahålls av kunden.
   * **[!UICONTROL Show Signature Key]:** Växla om signaturen ska visas eller inte i webbläsaren.
   * **[!UICONTROL HTTP Signature Encryption Method]:** Ange den metod vi använder för att kryptera signaturen. Använd [!UICONTROL SHA1] om inte kunden föredrar något annat.

   >[!NOTE]
   >
   >Om du vill aktivera [OAuth 2.0-autentisering för dataöverföringar i realtid](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html?lang=en) för en partner fyller du i fälten som i tabellen nedan. Fälten i *kursiv* måste fyllas i exakt som i tabellen.

   | Namn | Värde |
   |---|---|
   | [!UICONTROL Label] | [!UICONTROL Server with OAuth 2.0 enabled] |
   | [!UICONTROL Protocol] | [!UICONTROL HTTP] |
   | [!UICONTROL Domain] | [!UICONTROL api.partner.com] |
   | [!UICONTROL Port] | [!UICONTROL 443] |
   | [!UICONTROL Maximum Users per Request] | [!UICONTROL 10] |
   | [!UICONTROL URL Prefix] | [!UICONTROL /segments/aam] |
   | [!UICONTROL Authentication URL] | [!UICONTROL api.partner.com/oauth2/token] |
   | [!UICONTROL Authentication] | [!UICONTROL Username/Password] |
   | [!UICONTROL Username] | [!UICONTROL *Behörighet*] |
   | [!UICONTROL Password] | your_password_here |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. Klicka på **[!UICONTROL Create]** om du skapar en ny server eller klicka på **[!UICONTROL Update]** om du redigerar en befintlig server.
