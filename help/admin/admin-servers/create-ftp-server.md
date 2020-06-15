---
description: Använd serversidan i Audience Manager Admin-verktyget för att skapa en ny FTP-server eller för att redigera en befintlig server.
seo-description: Använd serversidan i Audience Manager Admin-verktyget för att skapa en ny FTP-server eller för att redigera en befintlig server.
seo-title: Skapa eller redigera en FTP-server
title: Skapa eller redigera en FTP-server
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
translation-type: tm+mt
source-git-commit: 78d694670e7abdc18938c5be729ad499e2647825
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 4%

---


# Skapa eller redigera en FTP-server {#create-or-edit-an-ftp-server}

Använd [!UICONTROL Servers] sidan i Audience Manager Admin-verktyget för att skapa en ny FTP-server eller redigera en befintlig server.

>[!NOTE]
>
>Du måste ha rollen för [!UICONTROL DEXADMIN] att kunna skapa nya servrar eller redigera befintliga servrar.

1. Om du vill skapa en ny server klickar du på **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Om du vill redigera en befintlig server klickar du på önskad server i **[!UICONTROL Label]** kolumnen.
1. Ange önskad etikett för den här servern.
1. Välj önskat protokoll i **[!UICONTROL Protocol]** listrutan: **FTP**.

   >[!NOTE]
   >
   >Vi rekommenderar att du använder [!DNL Amazon S3] som metod för att hämta filer från och leverera filer till partners. [!DNL Amazon S3] har ett enkelt webbtjänstgränssnitt som kan användas för att lagra och hämta data när som helst, var som helst på webben. Mer information finns i [Om Amazon S3](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html) i användarhandboken för *Audience Manager*.

1. Fyll i fälten:

   * **[!UICONTROL Type]:**Välj önskad krypteringstyp:**[!UICONTROL SFTP]**eller **[!UICONTROL FTPs/TLS]**.
   * **[!UICONTROL Domain]:**Ange önskad domän (värd) för den här servern.
   * **[!UICONTROL Port]:**Ange önskad port för den här servern. Standardporten visas för varje krypteringstyp. Du kan ändra standardporten om det behövs.
   * **[!UICONTROL Remote Path]:**Ange önskad fjärrsökväg för den här servern. Om du låter fältet vara tomt placeras filerna i standardkatalogen.
   * **[!UICONTROL .tmp File Rename on Completion]:**Aktivera det här alternativet om du vill byta namn på`.tmp`filen när den är klar.
   * **[!UICONTROL Filename Suffix]:**Ange den text som du vill ska läggas till för att överföra filer.
   * **[!UICONTROL Moved to When Finished]:**Ange sökvägen till den plats där du vill att överföringsfilen ska flyttas när den är klar.
   * **[!UICONTROL Authentication]:**Ange önskad metod för serverautentisering:**[!UICONTROL Username/Password]**eller **[!UICONTROL SSH Key]**.
   >[!NOTE]
   >
   >Kom ihåg att lägga till vår utgång [!DNL FTP] [!DNL IP] i din lista över tillåtna IP-adresser: **52.44.29.204**.

1. För **[!UICONTROL SSH Key]** autentisering:
   >[!NOTE]
   >
   >När du konfigurerar SSH-nyckelautentisering ska du alltid generera de offentliga och privata nycklarna enbart i OpenSSH-format.
   1. Generera nyckelparet public/private från alla [!DNL Linux] datorer och [!DNL Mac] datorer.
   1. Ge klienten den **offentliga nyckeln** att uppdatera på [!DNL SFTP] servern. De måste innehålla all text från den offentliga nyckeln på servern, inklusive `-----BEGIN RSA PRIVATE KEY-----` och `-----END RSA PRIVATE KEY-----` . I stället måste de ange det användarnamn under vilket de installerar nyckeln.
   1. Uppdatera användarnamnsfältet med det som tillhandahålls av klienten och nyckelfältet med den **privata nyckeln**.
1. Klicka **[!UICONTROL Create]** om du skapar en ny server eller klicka **[!UICONTROL Update]** om du redigerar en befintlig server.
