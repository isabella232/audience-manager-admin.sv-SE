---
description: På sidan Integreringsanvändare kan du visa en lista med användare i din Audience Manager-konfiguration. Du kan redigera eller ta bort befintliga användare eller skapa nya användare, förutsatt att du har tilldelats rätt användarroller.
seo-description: På sidan Integreringsanvändare kan du visa en lista med användare i din Audience Manager-konfiguration. Du kan redigera eller ta bort befintliga användare eller skapa nya användare, förutsatt att du har tilldelats rätt användarroller.
seo-title: Integreringsanvändare
title: Integreringsanvändare
uuid: 13dcb3fb-4561-409c-84da-943d0d390cf3
translation-type: tm+mt
source-git-commit: 10adb6b06160f5a5c4068483b407e5798fc10150

---


# Integreringsanvändare {#integration-users}

Använd [!UICONTROL Integration Users] sidan för att visa en lista över användare i din Audience Manager-konfiguration. Du kan redigera eller ta bort befintliga användare eller skapa nya användare, förutsatt att du har tilldelats rätt användarroller.

<!-- c_integration_users.xml -->

Du kan sortera varje kolumn i stigande eller fallande ordning genom att klicka på den önskade kolumnens rubrik.
Använd [!UICONTROL Search] rutan eller sidnumreringskontrollerna längst ned i listan för att hitta önskad användare.

## Skapa eller redigera en användare {#create-edit-user}

Använd sidan [!UICONTROL Integration Users] i Audience Manager- [!UICONTROL Admin] verktyget för att skapa en ny användare eller för att redigera en befintlig användares konto.

<!-- t_create_user.xml -->

>[!NOTE]
>
>Du måste ha rollen för [!UICONTROL CREATE_USER] att kunna skapa nya användare. Du måste ha rollen för att kunna redigera befintliga användare [!UICONTROL EDIT_USER] .

1. Om du vill skapa en ny användare klickar du på **[!UICONTROL Integration Users]** > **[!UICONTROL Create a New User]**. Om du vill redigera en befintlig användare klickar du på önskad användare i **[!UICONTROL Username]** kolumnen.
2. Fyll i fälten:
   * **[!UICONTROL First Name]**: (Obligatoriskt) Ange användarens förnamn.
   * **[!UICONTROL Last Name]**: (Obligatoriskt) Ange användarens efternamn.
   * **[!UICONTROL Username]**: (Obligatoriskt) Ange användarens användarnamn.
   * **[!UICONTROL Email Address]**: (Obligatoriskt) Ange användarens e-postadress.
   * **[!UICONTROL Phone Number]**: Ange användarens telefonnummer.
   * **[!UICONTROL IMS ID]**: Ange användarens [!UICONTROL Internet Messaging Service ID]namn.
   * **[!UICONTROL User Roles]**: Välj önskade användarroller:
      * **[!UICONTROL DEXADMIN]**: Ger administratörsåtkomst för att utföra uppgifter i Audience Manager- [!UICONTROL Admin] verktyget. Om du inte markerar det här alternativet kan du välja enskilda roller. Med de här rollerna kan användare utföra uppgifter med hjälp av [!DNL API] anrop, men inte med hjälp av administrationsverktyget.
      * **[!UICONTROL CREATE_USERS]**: Tillåter användare att skapa nya användare med ett [!DNL API] samtal.
      * **[!UICONTROL DELETE_USERS]**: Tillåter användare att ta bort befintliga användare med ett [!DNL API] samtal.
      * **[!UICONTROL EDIT_USERS]**: Tillåter användare att redigera befintliga användare med ett [!DNL API] samtal.
      * **[!UICONTROL VIEW_USERS]**: Låter användarna visa andra användare i Audience Manager-konfigurationen med hjälp av ett [!DNL API] samtal.
      * **[!UICONTROL CREATE_PARTNERS]**: Användare kan skapa Audience Manager-partners med hjälp av ett [!DNL API] samtal.
      * **[!UICONTROL DELETE_PARTNERS]**: Tillåter användare att ta bort Audience Manager-partners med hjälp av ett [!DNL API] samtal.
      * **[!UICONTROL EDIT_PARTNERS]**: Låter användarna redigera Audience Manager-partners med hjälp av ett [!DNL API] samtal.
      * **[!UICONTROL VIEW_PARNTERS]**: Låter användarna visa Audience Manager-partners med hjälp av ett [!DNL API] samtal.
   * **Status:** Välj **[!UICONTROL Active]** att göra den här användaren till en aktiverad Audience Manager-användare.
3. Klicka på **[!UICONTROL Submit]**.

## Ta bort en användare {#delete-user}

Använd sidan [!UICONTROL Integration Users] i Audience Manager- [!UICONTROL Admin] verktyget för att ta bort en befintlig användare.

<!-- t_delete_user.xml -->

>[!NOTE]
>
>Du måste ha rollen för **[!UICONTROL DELETE_USER]** att kunna skapa nya användare.

1. Klicka på **[!UICONTROL Integration Users]**.
2. Klicka ![](assets/icon_delete.png) i **[!UICONTROL Actions]** kolumnen för den önskade användaren.
3. Klicka **[!UICONTROL OK]** för att bekräfta borttagningen.