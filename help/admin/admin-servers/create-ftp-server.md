---
description: Använd serversidan i administrationsverktyget för Audience Manager för att skapa en ny FTP-server eller för att redigera en befintlig server.
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new FTP server or to edit an existing server.
seo-title: Create or Edit an FTP Server
title: Skapa eller redigera en FTP-server
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
exl-id: 9eae4ecf-ccde-483a-ae53-1cbac033d8d6
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 3%

---

# Skapa eller redigera en FTP-server {#create-or-edit-an-ftp-server}

Använd sidan [!UICONTROL Servers] i verktyget Audience Manager Admin om du vill skapa en ny FTP-server eller redigera en befintlig server.

>[!NOTE]
>
>Du måste ha rollen [!UICONTROL DEXADMIN] för att kunna skapa nya servrar eller redigera befintliga servrar.

1. Om du vill skapa en ny server klickar du på **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Om du vill redigera en befintlig server klickar du på önskad server i kolumnen **[!UICONTROL Label]**.
1. Ange önskad etikett för den här servern.
1. Välj önskat protokoll i listrutan **[!UICONTROL Protocol]**: **FTP**.

   >[!NOTE]
   >
   >Vi rekommenderar att du använder [!DNL Amazon S3] som metod för att hämta filer från och leverera filer till partners. [!DNL Amazon S3] har ett enkelt webbtjänstgränssnitt som kan användas för att lagra och hämta data när som helst, var som helst på webben. Mer information finns i [Om Amazon S3](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html) i *användarhandboken för Audience Manager*.

1. Fyll i fälten:

   * **[!UICONTROL Type]:** Välj önskad krypteringstyp:  **[!UICONTROL SFTP]** eller  **[!UICONTROL FTPs/TLS]**.
   * **[!UICONTROL Domain]:** Ange önskad domän (värd) för den här servern.
   * **[!UICONTROL Port]:** Ange önskad port för den här servern. Standardporten visas för varje krypteringstyp. Du kan ändra standardporten om det behövs.
   * **[!UICONTROL Remote Path]:** Ange önskad fjärrsökväg för den här servern. Om du låter det här fältet vara tomt placerar Audience Manager filerna i standardkatalogen.
   * **[!UICONTROL .tmp File Rename on Completion]:** Aktivera det här alternativet om du vill ändra namn på  `.tmp` filen när den är klar.
   * **[!UICONTROL Filename Suffix]:** Ange den text som du vill ska läggas till för att överföra filer.
   * **[!UICONTROL Moved to When Finished]:** Ange sökvägen till den plats där du vill att överföringsfilen ska flyttas när den är klar.
   * **[!UICONTROL Authentication]:** Ange önskad metod för serverautentisering:  **[!UICONTROL Username/Password]** eller  **[!UICONTROL SSH Key]**.

   >[!NOTE]
   >
   >Kom ihåg att lägga till vår egress [!DNL FTP] [!DNL IP] i listan över tillåtna IP-adresser: **52.44.29.204**.

1. För **[!UICONTROL SSH Key]**-autentisering:
   >[!NOTE]
   >
   >När du konfigurerar SSH-nyckelautentisering ska du alltid generera de offentliga och privata nycklarna enbart i OpenSSH-format.
   1. Generera det offentliga/privata nyckelparet från en [!DNL Linux]- eller [!DNL Mac]-dator.
   1. Ge **den offentliga nyckeln** till klienten som ska uppdateras på sin [!DNL SFTP]-server. De måste innehålla all text från den offentliga nyckeln på servern, inklusive `-----BEGIN RSA PRIVATE KEY-----` och `-----END RSA PRIVATE KEY-----`. I stället måste de ange det användarnamn under vilket de installerar nyckeln.
   1. Uppdatera användarnamnsfältet med det som anges av klienten och nyckelfältet med **privat nyckel**.
1. Klicka på **[!UICONTROL Create]** om du skapar en ny server eller klicka på **[!UICONTROL Update]** om du redigerar en befintlig server.
