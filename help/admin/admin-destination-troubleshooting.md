---
description: Information som hjälper dig att skapa destinationer i Audience Manager och undvika vanliga problem.
seo-description: Information to help you set up destinations in Audience Manager and avoid common problems.
seo-title: Destination Setup Troubleshooting
title: Felsökning av destinationsinställningar
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
exl-id: 53c72b1a-f1a1-4266-a595-e4821c2640b2
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 2%

---

# Felsökning av destinationsinställningar {#destination-setup-troubleshooting}

Information som hjälper dig att skapa destinationer i Audience Manager och undvika vanliga problem.

## Jag ställer in ett mål, men jag ser inga filer. Var är de? {#destination-no-files}

<!-- c_dest_tshooting.xml -->

Vanliga problem med destinationskonfigurationen är bland annat följande:

### Felkonfigurerat mål

* **Felaktig  [!UICONTROL UserID] nyckel:**  [!UICONTROL UserID] Nyckeln är  [!UICONTROL MasterDPID] för det här målet och är grunden för de ID-värden som kommer att vara gränslösa. Även om en [!UICONTROL UserID]-nyckel kan markeras via den nedrullningsbara listan behöver det inte innebära att ID:n/egenskaper/segment är mappade till det här värdet. Om [!UICONTROL Outbound]-processen (som körs efter att mål har skapats) inte hittar några användare som är mappade till den här [!UICONTROL UserID]-nyckeln, kommer inga data att vara gränslösa.
* **Nej i valda fildatakällor:** När du väljer en annan måltyp än  [!UICONTROL S2S]visas ett avsnitt längst ned på skärmen med etiketten  [!UICONTROL Configure Data Sources]. När det här avsnittet visas första gången markeras inga värden. Om du glömmer att klicka i kryssrutan [!UICONTROL All First Party] eller markerar datakällor individuellt i fönstret [!UICONTROL Available Data Sources], kommer inga data att uteslutas.

### Felkonfigurerat format

När du väljer ett format för dina utgående data är det bäst att återanvända ett befintligt format om det är möjligt. Om du använder ett redan beprövat format kan du vara säker på att dina utgående data genereras korrekt. Om du vill se exakt hur ett befintligt format är formaterat klickar du på alternativet [!UICONTROL Formats] på menyraden och söker efter formatet antingen efter namn eller efter ID-nummer. Felformaterade format eller makron som används i format ger felaktigt formaterade utdata eller förhindrar att informationen skrivs ut helt.

Mer information om hur du ställer in format och använder makron finns i [Filformatmakron](formats/file-formats.md#) och [HTTP-formatmakron](formats/web-formats.md).

### Felkonfigurerad server

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * Ange inga prefix för värdnamn. Om du har fått ett konto [!DNL ftp://hello.com] anger du bara [!DNL hello.com] i det här fältet.
   * **[!UICONTROL Port/Type Combination]**
      * För en [!DNL FTP]-överföring är den rekommenderade överföringstypen [!DNL SFTP].
      * När du väljer typen [!DNL SFTP] är porten nästan alltid 22.
      * När du väljer typen [!DNL FTPs/TLS] är porten nästan alltid 21.
      * Typen [!DNL FTPs/TLS] är inte densamma som en vanlig [!DNL FTP]-överföring. Vi stöder inte vanliga (osäkra) [!DNL FTP] överföringar.
   * **[!UICONTROL Remote Path]**
      * När du väljer en fjärrunderbana bör den anges utan inledande snedstreck.
      * Om den överförda filen ska placeras i undermappen [!DNL (root)/inbound] lägger du bara till [!DNL inbound] för fjärrsökvägen, inte [!DNL /inbound].
      * Om du skickar filer med flera kataloger längs sökvägen anger du snedstreck mellan varje katalog. Om du får platsen [!DNL /inbound/subdirectory1/subdirectory2] ska du ange [!DNL inbound/subdirectory1/subdirectory2] i det här fältet.
      * Om filen ska placeras i katalogen automatiskt dirigeras till av den externa servern kan du lämna detta utrymme tomt. Ange ingen punkt (. ), snedstreck ( / ) eller något annat.

* **[!DNL S3]**
   * [!DNL S3] är det överföringsprotokoll som rekommenderas (framför  [!DNL FTP] eller  [!DNL HTTP]).
      * **[!UICONTROL Bucket]**
         * Bucket-namnet ska visas utan snedstreck, prefix, suffix osv. Om du får adressen [!DNL s3://your-bucket] behöver du bara lägga till [!DNL your-bucket] i det här fältet.
      * **[!UICONTROL Directory]**
         * Lämna det här fältet tomt om du inte uttryckligen har fått en underkatalog där data ska placeras. Om du får adressen [!DNL s3://your-bucket/your-subdirectory] anger du [!DNL your-bucket] i fältet [!UICONTROL Bucket] och [!DNL your-subdirectory] ska läggas till i fältet [!UICONTROL Directory]. Lägg inte till föregående snedstreck.
         * Om du behöver flytta flera kataloger nedåt i banan bör du bara använda snedstreck som avgränsare. En plats på [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] skulle därför ha [!DNL your-bucket] i fältet [!UICONTROL Bucket] och [!DNL your-subdirectory1/your-subdirectory2] i fältet [!UICONTROL Directory].
      * **[!UICONTROL Access / Secret Keys]**
         * När [!DNL TechOps] skapar en bucket och ger åtkomst/hemliga nycklar till en konsult, är dessa vanligtvis `READ-ONLY`-autentiseringsuppgifter som ska skickas till klienten. Dessa autentiseringsuppgifter ska inte anges i [!UICONTROL Access / Secret Key]-fälten eftersom det gör att överföringen misslyckas (eftersom dessa autentiseringsuppgifter är skrivskyddade, inte skrivbara). Om [!DNL TechOps] skapar en bucket och anger inloggningsuppgifter bör konsulten också begära ett nyckelpar i Adobe - INTE SKA GES TILL KLIENTEN - som gör det möjligt att skriva filer till den här bucket. Nyckeln ska läggas till i dessa fält.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * Ange prefixinformation för [!DNL HTTP]-poster. Om du har fått ett konto [!DNL https://superduper.com] anger du [!DNL https://superduper.com] i det här fältet.
      * **[!UICONTROL URL Prefix]**
         * Lämna det föregående snedstrecket inaktiverat när du lägger till ett [!DNL URL]-prefix. En adress på [!DNL https://hello.com/r/x/y/z] måste ha [!DNL https://hello.com] angivet i fältet [!UICONTROL Domain] och [!DNL r/x/y/z] angivet här i fältet [!UICONTROL URL Prefix].
         * Om [!UICONTROL URL Prefix] inte behövs lämnar du det här värdet tomt.
      * **[!UICONTROL Authentication - SSH Key]**
         * Ange det fullständiga `SSH PRIVATE`-nyckelvärdet i den här rutan, inklusive sidhuvuden, sidfötter och radbrytningar, för att säkerställa korrekt kryptering/nyckellagring.

### Inte tillräckligt med tid för utgående generering

Den utomordentliga processen körs två gånger dagligen och flera processer (överlagring, publicering, till externa platser osv.) måste köras innan en fil överförs till det slutliga målet. En bra tumregel är att ett mål ska vara helt konfigurerat minst 24 timmar innan du kan förvänta dig att data ska skickas till en extern plats.

### För stora fildelningsstorlekar

När du exporterar filer till mål kan du dela upp större utgående filer i filsegment. Kontrollera att de enskilda filsegmenten inte överstiger 10 GB. Se även [Namn på utgående datafil: Syntax och exempel](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html?lang=en).


## Så här konfigurerar du destinationer för att exportera Experience Cloud-ID, kund-ID eller Audience Manager-ID i utgående datafiler {#set-up-destinations-export}

På den här sidan visas hur du ställer in mål för att exportera data som är sparade från den ID-typ som du vill använda i [!UICONTROL Outbound Data Files].

<!-- set-up-destinations-mcid-aamid.xml -->

Destinationer gör att våra kunder kan aktivera sina data i valfritt antal digitala kanaler. De kan till exempel exportera målgruppsdata till andra [!DNL Adobe Experience Cloud]-lösningar ([!DNL Target], [!DNL Campaign] osv.). De kan också skicka data till [!UICONTROL DSP]s, [!UICONTROL SSP]s eller någon annan plattform som är integrerad med Audience Manager. Vi har en lista över partners vi arbetar med på vår [Integrations-Wiki-sida](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>Mer information om hur du skapar mål i Admin-gränssnittet finns i artikeln [Skapa eller redigera företagsmål](companies/admin-manage-company-destinations.md#create-edit-company-destinations).

Dina kunder vill exportera olika ID-typer beroende på destination. I konfigurationsdiagrammet nedan visas de alternativ du bör välja för att exportera profilinformation som är relaterad till olika ID-typer. Vi rekommenderar att du även refererar till [index för ID:n i Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html?lang=en). Det finns tre viktiga inställningar att tänka på: [!UICONTROL User ID Key], [!UICONTROL Data Source Type] och [!UICONTROL Format]. Vi detaljerar alla nedan.

* [!UICONTROL User ID Key]. Gå till **[!UICONTROL Companies]** i [!UICONTROL Admin UI]. Sök efter kundens företag och klicka på det. Leta efter fliken **[!UICONTROL Destinations]** och tryck på **[!UICONTROL Add Destination]**. Välj [!UICONTROL User ID Key] i **[!UICONTROL Add Destination]**-arbetsflödet. [!UICONTROL User ID Key] filtrerar inkommande ID:n från måldatakällan och tillåter bara att ID:n skickas.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]. Markera det här alternativet när du skapar ett mål i användargränssnittet för Audience Manager. Först väljer du [!UICONTROL Inbound] och sedan önskad ID-typ. Alternativen är:

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]. Det här alternativet avgör vilket filformat du ska exportera. Välj formatet under **[!UICONTROL Batch Data]** i **[!UICONTROL Add Destination]**-arbetsflödet.

Om du vill kontrollera ett format går du till **[!UICONTROL Admin UI > Formats]** och söker efter elementet [!UICONTROL Data Row]. Det här elementet innehåller ett makro med filformatet &lt;MCID> i exemplet nedan.

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> Konfigurationsnr </th> 
   <th colname="col1" class="entry"> <p>Användarnyckel </p> </th> 
   <th colname="col2" class="entry"> <p>Typ av datakälla </p> </th> 
   <th colname="col3" class="entry"> <p>Format </p> </th> 
   <th colname="col4" class="entry"> <p>Exporterad ID-typ </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> 1 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID (Alla datakällor som företaget har tillgång till) </p> </td> 
   <td colname="col2"> <p>Kund-ID </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>Kund-ID (DPUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID (Alla datakällor som företaget har tillgång till) </p> </td> 
   <td colname="col2"> <p>Kund-ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID (Alla datakällor som företaget har tillgång till) </p> </td> 
   <td colname="col2"> <p>Kund-ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID (Alla datakällor som företaget har tillgång till) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID (Alla datakällor som företaget har tillgång till) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID (Alla datakällor som företaget har tillgång till) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
 </tbody> 
</table>

## Användningsexempel

Säg att du använder Audience Manager och [!DNL Campaign]. Om du vill att kunddata ska kunna användas i [!DNL Campaign] vill du exportera [!UICONTROL Experience Cloud IDs]. Du bör använda konfigurationsnummer 3 i det här fallet.
