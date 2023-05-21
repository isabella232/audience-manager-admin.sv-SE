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

Använd [!UICONTROL OAuth2 Clients] sida för att visa en lista med [!UICONTROL OAuth2] dina kunder [!DNL Audience Manager] konfiguration. Du kan redigera eller ta bort befintliga klienter eller skapa nya klienter, förutsatt att du har tilldelats rätt användarroller.

## Översikt {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>Se till att kunden läser [OAuth2](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) i användarhandboken för Audience Manager.

[!DNL OAuth2] är en öppen standard för auktorisering för att ge skyddad delegerad åtkomst till [!DNL Audience Manager] resurser för en resursägares räkning.

![](assets/oauth.png)

Du kan sortera varje kolumn i stigande eller fallande ordning genom att klicka på den önskade kolumnens rubrik.

Använd [!UICONTROL Search] eller sidnumreringskontrollerna längst ned i listan för att hitta den önskade klienten.

## Skapa eller redigera en OAuth2-klient {#create-edit-client}

<!-- t_create_edit_auth.xml -->

Använd [!UICONTROL OAuth2 Clients] sida i Audience Manager [!UICONTROL Admin] verktyg för att skapa ett nytt [!UICONTROL Oauth2] eller för att redigera en befintlig klient.

1. Skapa en ny [!UICONTROL OAuth2] klient, klicka **[!UICONTROL OAuth2 Clients]** > **[!UICONTROL Add OAuth2 Client]**. Redigera en befintlig [!UICONTROL OAuth2] klickar du på önskad klient i **[!UICONTROL Client ID]** kolumn.
1. Ange önskat namn för detta [!UICONTROL OAuth2] klient. Observera att detta är ett namn som bara gäller för posten.
1. Ange [!UICONTROL OAuth2] klientens e-postadress. Endast en e-postadress får användas.
1. Från **[!UICONTROL Partner]** väljer du önskad partner.
1. I **[!UICONTROL Client ID]** anger du önskat ID. Detta är det värde som används när du skickar in [!DNL API] förfrågningar. Prefixet fylls i automatiskt när du börjar skriva efter att du har valt ett [!UICONTROL Partner] från listrutan i föregående steg. Rätt format är &lt; *`partner subdomain`*> - &lt; *`Audience Manager username`*>.
1. Markera eller avmarkera **[!UICONTROL Restrict to Partner Users]** kryssrutan efter behov. Om den här kryssrutan är markerad måste användaren vara en [!DNL Audience Manager] användare som anges för den valda partnern. Vi rekommenderar att du väljer det här alternativet.
1. I **[!UICONTROL Scope]** markerar eller avmarkerar **[!UICONTROL Read]** och **[!UICONTROL Write]** kryssrutor efter behov.
1. I **[!UICONTROL Grant Type]** väljer du metod för auktorisering. Vi rekommenderar att du använder standardinställningarna för [!UICONTROL Password] och [!UICONTROL Refresh-token] alternativ.

   * **[!UICONTROL Implicit]**: Om du väljer det här alternativet visas [!UICONTROL Redirect URI] är aktiverad. Användaren får en token för automatisk åtkomst efter att ha autentiserats och skickas omedelbart till omdirigeringen [!DNL URI].
   * **[!UICONTROL Authorization Code]**: Om du väljer det här alternativet visas [!UICONTROL Redirect URI] är aktiverad. Användaren returneras till klienten efter att ha autentiserats och skickas sedan till omdirigeringen [!DNL URI].
   * **[!UICONTROL Password]**: Användaren autentiseras med ett användarangivet lösenord i stället för ett automatiskt valideringsförsök via en auktoriseringsserver.
   * **[!UICONTROL Refresh_token]**: Används för att uppdatera en åtkomsttoken som har upphört att gälla under en längre tidsperiod.

1. I **[!UICONTROL Redirect URI]** anger du [!DNL URI]. Det här alternativet är bara aktiverat om du väljer **[!UICONTROL Implicit]** och **[!UICONTROL Authorization_code]** anslagstyper. The **[!UICONTROL Redirect URI]** kan du ange ett kommaavgränsat värde som är acceptabelt [!DNL URI] värden. Det här är [!DNL URI] en användare omdirigeras till efter att klienten har godkänts för [!DNL API] åtkomst.
1. Ange önskad förfallotid (i sekunder) för åtkomst och uppdatering av utgångsdatum för token.

   * **[!UICONTROL Access Token Expiration Time]**: Antalet sekunder som en åtkomsttoken är giltig efter att den har utfärdats. Kan vara null för att använda plattformens standardinställning (12 timmar). Även kan vara -1 för att ange att åtkomsttoken inte upphör att gälla.
   * **[!UICONTROL Refresh Token Expiration Time]**: Antalet sekunder som en uppdateringstoken är giltig efter att den har utfärdats. Kan vara null för att använda plattformens standardinställning (30 dagar).

1. Klicka på **[!UICONTROL Save]**.

Så här tar du bort en [!UICONTROL OAuth2] klient, klicka **[!UICONTROL OAuth2 Clients]** och sedan klicka  ![](assets/icon_delete.png) i **[!UICONTROL Actions]** -kolumn för den önskade klienten.

>[!MORELIKETHIS]
>
>* [Krav och rekommendationer för API](../admin-oauth2/aam-admin-api-requirements.md)

