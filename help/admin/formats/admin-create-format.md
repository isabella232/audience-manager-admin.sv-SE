---
description: Använd formatsidan i administrationsverktyget för Audience Manager för att skapa ett nytt format eller för att redigera ett befintligt format.
seo-description: Use the Formats page in the Audience Manager Admin tool to create a new format or to edit an existing format.
seo-title: Create or Edit a Format
title: Skapa eller redigera ett format
uuid: ca1b1feb-bcd3-4a41-b1e8-80565f6c23ae
exl-id: 3c97d1e9-8093-4181-a1fd-fb1816cdaa3d
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 2%

---

# Skapa eller redigera ett format {#create-or-edit-a-format}

Använd [!UICONTROL Formats] i administrationsverktyget för Audience Manager för att skapa ett nytt format eller för att redigera ett befintligt format.

<!-- t_create_format.xml -->

>[!TIP]
>
>När du väljer ett format för dina utgående data är det bäst att återanvända ett befintligt format om det är möjligt. Om du använder ett redan beprövat format kan du vara säker på att dina utgående data genereras korrekt. Om du vill se exakt hur ett befintligt format är formaterat klickar du på [!UICONTROL Formats] på menyraden och sök efter ditt format antingen efter namn eller efter ID-nummer. Felformaterade format eller makron som används i format ger felaktigt formaterade utdata eller förhindrar att informationen skrivs ut helt.

1. Om du vill skapa ett nytt format klickar du på **[!UICONTROL Formats]** > **[!UICONTROL Add Format]**. Om du vill redigera ett befintligt format klickar du på det önskade formatet i dialogrutan **[!UICONTROL Name]** kolumn.

   ![](assets/create_format.png)

1. Fyll i fälten:
   * **Namn:** (Obligatoriskt) Ange ett beskrivande namn för formatet.
   * **Typ:** (Obligatoriskt) Välj önskat format:
      * **[!UICONTROL File]**: Skickar data via [!DNL FTP] filer.
      * **[!UICONTROL HTTP]**: Omsluter data i en [!DNL JSON] wrapper.

1. (Villkorligt) Om du väljer **[!UICONTROL File]**, fylla i fälten:

   >[!NOTE]
   >
   >En lista över tillgängliga makron finns på [Filformatmakron](../formats/file-formats.md#concept_A867101505074418A58DE325949E5089) och [HTTP-formatmakron](../formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE).

   * **[!UICONTROL File Name]:** Ange filnamnet för dataöverföringsfilen.
   * **Sidhuvud:** Ange texten som visas på den första raden i dataöverföringsfilen.
   * **[!UICONTROL Data Row]:** Ange den text som visas i varje avgränsad rad i filen.
   * **[!UICONTROL Maximum File Size (In MB)]:** Ange den maximala filstorleken för dataöverföringsfiler. Komprimerade filer måste vara mindre än 100 MB. Det finns ingen gräns för okomprimerad filstorlek.
   * **[!UICONTROL Compression]:** Välj önskad komprimeringstyp: gz eller zip för datafilerna. För leverans till [!UICONTROL AWS S3]måste du använda .gz-filer eller okomprimerade filer.
   * **[!UICONTROL .info Receipt]:** Anger att en överföringskontroll ([!DNL .info]) genereras. The [!DNL .info] -filen innehåller metadatainformation om filöverföringar så att partners kan verifiera att filöverföringar som hanteras i Audience Manager är korrekta. Mer information finns i [Överföringskontrollfiler för loggfilsöverföringar](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/transfer-control-files.html?lang=en).
   * **[!UICONTROL MD5 Checksum Receipt]:** Anger att [!DNL MD5] inleverans av kontrollsumma genereras. The [!DNL MD5] kvitto på checksum så att partners kan verifiera att Audience Manager har hanterat hela överföringen korrekt.

1. (Villkorligt) Om du väljer **[!UICONTROL HTTP]**, fylla i fälten:

   * **[!UICONTROL Method]:** Välj [!DNL API] metod som du vill använda för överföringsprocessen:
      * **[!UICONTROL POST]:** Om du väljer [!DNL POST]väljer du innehållstyp ([!DNL XML] eller [!DNL JSON]) och ange sedan begärandetexten.
      * **[!UICONTROL GET]:** Om du väljer [!DNL GET], anger frågeparametrarna.

1. Klicka **[!UICONTROL Create]** om du skapar ett nytt format, eller klickar på **[!UICONTROL Save Updates]** om du redigerar ett befintligt format.

## Ta bort ett format {#delete-format}

1. Klicka på **[!UICONTROL Formats]**.
2. Klicka  ![](assets/icon_delete.png) i **[!UICONTROL Actions]** -kolumn i önskat format.
3. Klicka **[!UICONTROL OK]** för att bekräfta borttagningen.
