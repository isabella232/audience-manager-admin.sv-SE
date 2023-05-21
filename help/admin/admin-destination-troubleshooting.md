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

* **Felaktig [!UICONTROL UserID] Nyckel:** The [!UICONTROL UserID] nyckeln är [!UICONTROL MasterDPID] för den här destinationen och är grunden för de ID-värden som kommer att vara gränslösa. Även om en [!UICONTROL UserID] tangenten är markeringsbar via listrutan, vilket inte nödvändigtvis innebär att det finns ID:n/egenskaper/segment som är mappade till det här värdet. Om [!UICONTROL Outbound] (som körs efter att mål har skapats) inte hittar några användare som är mappade till detta [!UICONTROL UserID] kommer inga data att vara gränslösa.
* **Nej i valda fildatakällor:** När du väljer en annan måltyp än [!UICONTROL S2S]visas ett avsnitt längst ned på skärmen med etiketten [!UICONTROL Configure Data Sources]. När det här avsnittet visas första gången markeras inga värden. Om du glömmer bort att klicka på [!UICONTROL All First Party] kryssrutan eller välj datakällor individuellt från [!UICONTROL Available Data Sources] kommer inga data att vara obegränsade.

### Felkonfigurerat format

När du väljer ett format för dina utgående data är det bäst att återanvända ett befintligt format om det är möjligt. Om du använder ett redan beprövat format kan du vara säker på att dina utgående data genereras korrekt. Om du vill se exakt hur ett befintligt format är formaterat klickar du på [!UICONTROL Formats] på menyraden och sök efter ditt format antingen efter namn eller efter ID-nummer. Felformaterade format eller makron som används i format ger felaktigt formaterade utdata eller förhindrar att informationen skrivs ut helt.

Mer information om hur du ställer in format och använder makron finns i [Filformatmakron](formats/file-formats.md#) och [HTTP-formatmakron](formats/web-formats.md).

### Felkonfigurerad server

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * Ange inga prefix för värdnamn. Om du får ett konto [!DNL ftp://hello.com], anger du [!DNL hello.com] i detta fält.
   * **[!UICONTROL Port/Type Combination]**
      * För [!DNL FTP] överföring, den önskade överföringstypen är [!DNL SFTP].
      * När du väljer [!DNL SFTP] typ, porten är nästan alltid 22.
      * När du väljer [!DNL FTPs/TLS] typ, porten är nästan alltid 21.
      * The [!DNL FTPs/TLS] -typen är inte densamma som en vanlig [!DNL FTP] överföring. Vi stöder inte regelbundet (osäkert) [!DNL FTP] överföringar.
   * **[!UICONTROL Remote Path]**
      * När du väljer en fjärrunderbana bör den anges utan inledande snedstreck.
      * Om den överförda filen ska placeras i [!DNL (root)/inbound] undermapp, lägga till [!DNL inbound] för fjärrsökvägen, inte [!DNL /inbound].
      * Om du skickar filer med flera kataloger längs sökvägen anger du snedstreck mellan varje katalog. Om du får plats för [!DNL /inbound/subdirectory1/subdirectory2]ska du ange [!DNL inbound/subdirectory1/subdirectory2] i detta fält.
      * Om filen ska placeras i katalogen automatiskt dirigeras till av den externa servern kan du lämna detta utrymme tomt. Ange ingen punkt (. ), snedstreck ( / ) eller något annat.

* **[!DNL S3]**
   * [!DNL S3] är det överföringsprotokoll som rekommenderas (över [!DNL FTP] eller [!DNL HTTP]).
      * **[!UICONTROL Bucket]**
         * Bucket-namnet ska visas utan snedstreck, prefix, suffix osv. Om du får adressen [!DNL s3://your-bucket] du bara lägger till [!DNL your-bucket] till detta fält.
      * **[!UICONTROL Directory]**
         * Lämna det här fältet tomt om du inte uttryckligen har fått en underkatalog där data ska placeras. Om du får adressen [!DNL s3://your-bucket/your-subdirectory], ange [!DNL your-bucket] i [!UICONTROL Bucket] fält och [!DNL your-subdirectory] ska läggas till i [!UICONTROL Directory] fält. Lägg inte till föregående snedstreck.
         * Om du behöver flytta flera kataloger nedåt i banan bör du bara använda snedstreck som avgränsare. Så en plats för [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] skulle ha [!DNL your-bucket] i [!UICONTROL Bucket] fält och [!DNL your-subdirectory1/your-subdirectory2] som anges i [!UICONTROL Directory] fält.
      * **[!UICONTROL Access / Secret Keys]**
         * När [!DNL TechOps] skapar en bucket och ger åtkomst/hemliga nycklar till en konsult. Dessa uppgifter är vanligtvis `READ-ONLY` autentiseringsuppgifter som ska lämnas ut till klienten. Dessa autentiseringsuppgifter ska inte anges i [!UICONTROL Access / Secret Key] fält, eftersom detta gör att överföringen misslyckas (eftersom dessa autentiseringsuppgifter är skrivskyddade, inte skrivbara). I det fall där [!DNL TechOps] skapar en bucket och anger autentiseringsuppgifter. Konsulten bör också begära ett nyckelpar i Adobe - INTE SKA GES TILL KLIENTEN - som gör det möjligt att skriva filer till den här bucket. Nyckeln ska läggas till i dessa fält.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * Ange prefixinformation för [!DNL HTTP] poster. Om du får ett konto [!DNL https://superduper.com], ange [!DNL https://superduper.com] i detta fält.
      * **[!UICONTROL URL Prefix]**
         * När du lägger till en [!DNL URL] utelämna det föregående snedstrecket. En adress till [!DNL https://hello.com/r/x/y/z] borde ha [!DNL https://hello.com] anges i [!UICONTROL Domain] fält och [!DNL r/x/y/z] anges här i [!UICONTROL URL Prefix] fält.
         * Om en [!UICONTROL URL Prefix] är inte nödvändigt, lämna det här värdet tomt.
      * **[!UICONTROL Authentication - SSH Key]**
         * Ange hela `SSH PRIVATE` nyckelvärdet i den här rutan, inklusive sidhuvuden, sidfötter och radbrytningar, för att säkerställa korrekt kryptering/nyckellagring.

### Inte tillräckligt med tid för utgående generering

Den utomordentliga processen körs två gånger dagligen och flera processer (överlagring, publicering, till externa platser osv.) måste köras innan en fil överförs till det slutliga målet. En bra tumregel är att ett mål ska vara helt konfigurerat minst 24 timmar innan du kan förvänta dig att data ska skickas till en extern plats.

### För stora fildelningsstorlekar

När du exporterar filer till mål kan du dela upp större utgående filer i filsegment. Kontrollera att de enskilda filsegmenten inte överstiger 10 GB. Se även [Namn på utgående datafil: Syntax och exempel](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html?lang=en).


## Så här konfigurerar du destinationer för att exportera Experience Cloud-ID, kund-ID eller Audience Manager-ID i utgående datafiler {#set-up-destinations-export}

På den här sidan visas hur du ställer in destinationer för att exportera data som är sparade från den ID-typ som du vill använda i [!UICONTROL Outbound Data Files].

<!-- set-up-destinations-mcid-aamid.xml -->

Destinationer gör att våra kunder kan aktivera sina data i valfritt antal digitala kanaler. De kan till exempel exportera målgruppsdata till andra [!DNL Adobe Experience Cloud] lösningar ([!DNL Target], [!DNL Campaign], osv.). Eller så kan de skicka data till [!UICONTROL DSP]s, [!UICONTROL SSP]s, eller någon plattform som är integrerad med Audience Manager. Vi har en lista över partners vi samarbetar med i [Integrering - Wiki-sida](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>En detaljerad genomgång av hur du skapar mål i administratörsgränssnittet finns i [Skapa eller redigera företagsmål](companies/admin-manage-company-destinations.md#create-edit-company-destinations) artikel.

Dina kunder vill exportera olika ID-typer beroende på destination. I konfigurationsdiagrammet nedan visas de alternativ du bör välja för att exportera profilinformation som är relaterad till olika ID-typer. Vi rekommenderar att du även läser [Index för ID:n i Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html?lang=en). Det finns tre viktiga inställningar att tänka på: [!UICONTROL User ID Key], [!UICONTROL Data Source Type] och [!UICONTROL Format]. Vi detaljerar alla nedan.

* [!UICONTROL User ID Key]. I [!UICONTROL Admin UI], gå till **[!UICONTROL Companies]**. Sök efter kundens företag och klicka på det. Leta efter **[!UICONTROL Destinations]** och tryck på **[!UICONTROL Add Destination]**. I **[!UICONTROL Add Destination]** arbetsflöde, välj [!UICONTROL User ID Key]. The [!UICONTROL User ID Key] kommer att filtrera inkommande ID:n från måldatakällan och endast tillåta att ID:n skickas.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]. Markera det här alternativet när du skapar ett mål i användargränssnittet för Audience Manager. Först av allt, markera [!UICONTROL Inbound]väljer du sedan önskad ID-typ. Alternativen är:

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]. Det här alternativet avgör vilket filformat du ska exportera. I **[!UICONTROL Add Destination]** arbetsflöde, under **[!UICONTROL Batch Data]** väljer du format.

Gå till **[!UICONTROL Admin UI > Formats]** och leta efter [!UICONTROL Data Row] -element. Detta element innehåller ett makro i filformatet, &lt;mcid> i exemplet nedan.

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
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
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
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
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
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
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
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
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

Säg att du använder Audience Manager och [!DNL Campaign]. För att göra kunddata användbara i [!DNL Campaign]som du vill exportera [!UICONTROL Experience Cloud IDs]. Du bör använda konfigurationsnummer 3 i det här fallet.
