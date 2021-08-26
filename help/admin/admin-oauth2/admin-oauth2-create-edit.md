---
description: Använd sidan för OAuth2-klienter för att visa en lista över OAuth2-klienter i din Audience Manager-konfiguration. Du kan redigera eller ta bort befintliga klienter eller skapa nya klienter, förutsatt att du har tilldelats rätt användarroller.
seo-description: Use the OAuth2 Clients page to view a list of OAuth2 clients in your Audience Manager configuration. You can edit or delete existing clients or create new clients, providing that you have the appropriate user roles assigned.
seo-title: OAuth2 Clients
title: OAuth2-klienter
uuid: 3e654053-fb2f-4d8f-a53c-b5c3b8dbdaaa
exl-id: 993eae04-02e8-4554-a6fe-cf599053bfc9
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 1%

---

# OAuth2-klienter {#oauth-clients}

Använd sidan [!UICONTROL OAuth2 Clients] för att visa en lista över [!UICONTROL OAuth2]-klienter i din [!DNL Audience Manager]-konfiguration. Du kan redigera eller ta bort befintliga klienter eller skapa nya klienter, förutsatt att du har tilldelats rätt användarroller.

## Översikt {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>Se till att kunden läser [OAuth2](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth)-dokumentationen i användarhandboken för Audience Manager.

[!DNL OAuth2] är en öppen standard för auktorisering som ger skyddad delegerad åtkomst till  [!DNL Audience Manager] resurser åt en resursägare.

![](assets/oauth.png)

Du kan sortera varje kolumn i stigande eller fallande ordning genom att klicka på den önskade kolumnens rubrik.

Använd rutan [!UICONTROL Search] eller pagineringskontrollerna längst ned i listan för att hitta önskad klient.

## Skapa eller redigera en OAuth2-klient {#create-edit-client}

<!-- t_create_edit_auth.xml -->

Använd sidan [!UICONTROL OAuth2 Clients] i verktyget Audience Manager [!UICONTROL Admin] om du vill skapa en ny [!UICONTROL Oauth2]-klient eller redigera en befintlig klient.

1. Om du vill skapa en ny [!UICONTROL OAuth2]-klient klickar du på **[!UICONTROL OAuth2 Clients]** > **[!UICONTROL Add OAuth2 Client]**. Om du vill redigera en befintlig [!UICONTROL OAuth2]-klient klickar du på önskad klient i kolumnen **[!UICONTROL Client ID]**.
1. Ange önskat namn för den här [!UICONTROL OAuth2]-klienten. Observera att detta är ett namn som bara gäller för posten.
1. Ange [!UICONTROL OAuth2]-klientens e-postadress. Endast en e-postadress får användas.
1. Välj önskad partner i listrutan **[!UICONTROL Partner]**.
1. Ange önskat ID i rutan **[!UICONTROL Client ID]**. Detta är det värde som används när [!DNL API]-begäranden skickas. Prefixet fylls i automatiskt när du börjar skriva efter att du har valt [!UICONTROL Partner] i listrutan i föregående steg. Det korrekta formatet är &lt; *`partner subdomain`*> - &lt; *`Audience Manager username`*>.
1. Markera eller avmarkera kryssrutan **[!UICONTROL Restrict to Partner Users]** efter behov. Om den här kryssrutan är markerad måste användaren vara en [!DNL Audience Manager]-användare som anges för den valda partnern. Vi rekommenderar att du väljer det här alternativet.
1. Markera eller avmarkera kryssrutorna **[!UICONTROL Read]** och **[!UICONTROL Write]** i **[!UICONTROL Scope]**-avsnittet.
1. Välj önskat sätt för auktorisering i **[!UICONTROL Grant Type]**-avsnittet. Vi rekommenderar att du använder standardinställningarna för alternativen [!UICONTROL Password] och [!UICONTROL Refresh-token].

   * **[!UICONTROL Implicit]**: Om du väljer det här alternativet aktiveras  [!UICONTROL Redirect URI] rutan. Användaren får en automatisk åtkomsttoken efter att ha autentiserats och skickas omedelbart till omdirigeringen [!DNL URI].
   * **[!UICONTROL Authorization Code]**: Om du väljer det här alternativet aktiveras  [!UICONTROL Redirect URI] rutan. Användaren returneras till klienten efter att ha autentiserats och skickas sedan till omdirigeringen [!DNL URI].
   * **[!UICONTROL Password]**: Användaren autentiseras med ett användarangivet lösenord i stället för ett automatiskt valideringsförsök via en auktoriseringsserver.
   * **[!UICONTROL Refresh_token]**: Används för att uppdatera en åtkomsttoken som har upphört att gälla under en längre tidsperiod.

1. Ange önskad [!DNL URI] i rutan **[!UICONTROL Redirect URI]**. Det här alternativet är bara aktiverat om du väljer anslagstyperna **[!UICONTROL Implicit]** och **[!UICONTROL Authorization_code]**. I rutan **[!UICONTROL Redirect URI]** kan du ange ett kommaavgränsat värde för tillåtna [!DNL URI]-värden. Det här är [!DNL URI] som en användare av en klient omdirigeras till efter att klienten har godkänt åtkomsten till [!DNL API].
1. Ange önskad förfallotid (i sekunder) för åtkomst och uppdatering av utgångsdatum för token.

   * **[!UICONTROL Access Token Expiration Time]**: Antalet sekunder som en åtkomsttoken är giltig efter att den har utfärdats. Kan vara null för att använda plattformens standardinställning (12 timmar). Även kan vara -1 för att ange att åtkomsttoken inte upphör att gälla.
   * **[!UICONTROL Refresh Token Expiration Time]**: Antalet sekunder som en uppdateringstoken är giltig efter att den har utfärdats. Kan vara null för att använda plattformens standardinställning (30 dagar).

1. Klicka på **[!UICONTROL Save]**.

Om du vill ta bort en [!UICONTROL OAuth2]-klient klickar du på **[!UICONTROL OAuth2 Clients]** och sedan på ![](assets/icon_delete.png) i **[!UICONTROL Actions]**-kolumnen för den önskade klienten.

>[!MORELIKETHIS]
>
>* [Krav och rekommendationer för API](../admin-oauth2/aam-admin-api-requirements.md)

