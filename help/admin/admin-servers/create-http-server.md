---
description: Använd sidan Servrar i Audience Manager Admin-verktyget för att skapa en ny HTTP-server eller för att redigera en befintlig server.
seo-description: Använd sidan Servrar i Audience Manager Admin-verktyget för att skapa en ny HTTP-server eller för att redigera en befintlig server.
seo-title: Skapa eller redigera en HTTP-server
title: Skapa eller redigera en HTTP-server
uuid: 1ef0e751-e239-4dc6-a4f6-73cc05686807
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# Skapa eller redigera en HTTP-server {#create-or-edit-an-http-server}

Använd [!UICONTROL Servers] sidan i Audience Manager Admin-verktyget för att skapa en ny HTTP-server eller för att redigera en befintlig server.

>[!NOTE]
>
>Du måste ha rollen för [!UICONTROL DEXADMIN] att kunna skapa nya servrar eller redigera befintliga servrar.

1. Om du vill skapa en ny server går du till **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Om du vill redigera en befintlig server klickar du på önskad server i **[!UICONTROL Label]** kolumnen.
1. Ange önskad etikett för den här servern.
1. Välj önskat protokoll i **[!UICONTROL Protocol]** listrutan: [!DNL HTTP].
1. Fyll i fälten:

   * **[!UICONTROL Domain]:**Ange önskad domän (värd) för den här servern.
   * **[!UICONTROL Port]:**Ange önskad port för den här servern. Standardporten visas för varje krypteringstyp. Du kan ändra standardporten om det behövs
   * **[!UICONTROL Maximum Users Per Request]:**Ange maximalt antal användare per begäran som tillåts för den här servern.
   * **[!UICONTROL URL Prefix]:**Ange det prefix som ska användas för den här servern[!DNL URL].
   * **[!UICONTROL Authentication URL]:**Ange sökvägen[!UICONTROL Authentication URL]för den här`HTTP`servern.
   * **[!UICONTROL Authentication]:**Ange önskad autentiseringsmetod:**[!UICONTROL None]**,**[!UICONTROL Username/Password]**eller **[!UICONTROL SSH Key]**.
   * **[!UICONTROL HTTP Signature Header]:**Namnet på den rubrik som[!DNL HTTP]tillhandahålls av kunden och som innehåller[!DNL HTTP]signaturnyckeln. Standardvärdet är[!UICONTROL X-Signature], vilket visas i exemplet nedan:

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

   * **[!UICONTROL HTTP Signature Key]:**Nyckeln som används för att signera[!DNL HTTP]begäran, som tillhandahålls av kunden.
   * **[!UICONTROL Show Signature Key]:**Växla om signaturen ska visas i webbläsaren eller inte.
   * **[!UICONTROL HTTP Signature Encryption Method]:**Ange den metod som vi använder för att kryptera signaturen. Använd[!UICONTROL SHA1]om inte kunden föredrar något annat.
   >[!NOTE]
   >
   >Om du vill aktivera [OAuth 2.0-autentisering för dataöverföringar](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html) i realtid för en partner fyller du i fälten som i tabellen nedan. Fälten i *kursiv* text måste fyllas i exakt som i tabellen.

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
   | [!UICONTROL Username] | [!UICONTROL *Behörighet *] |
   | [!UICONTROL Password] | your_password_here |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. Klicka **[!UICONTROL Create]** om du skapar en ny server eller klicka **[!UICONTROL Update]** om du redigerar en befintlig server.