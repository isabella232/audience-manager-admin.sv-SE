---
description: Information som hjälper dig att konfigurera destinationer i Audience Manager och undvika vanliga problem.
seo-description: Information som hjälper dig att konfigurera destinationer i Audience Manager och undvika vanliga problem.
seo-title: Felsökning av målinställningar
title: Felsökning av målinställningar
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
translation-type: tm+mt
source-git-commit: 118e8fa3f35bc77846c6518268448d57d779a2ee

---


# Felsökning av målinställningar {#destination-setup-troubleshooting}

Information som hjälper dig att konfigurera destinationer i Audience Manager och undvika vanliga problem.

## Jag ställer in ett mål, men jag ser inga filer. Var är de? {#destination-no-files}

<!-- c_dest_tshooting.xml -->

Vanliga problem med destinationskonfigurationen är bland annat följande:

### Felkonfigurerat mål

* **Felaktig[!UICONTROL UserID]nyckel:** Nyckeln [!UICONTROL UserID] är [!UICONTROL MasterDPID] destinationens namn och är grunden för de ID-värden som kommer att vara gränslösa. Även om en [!UICONTROL UserID] nyckel kan markeras via den nedrullningsbara listan behöver det inte innebära att ID:n/egenskaper/segment är mappade till det här värdet. Om [!UICONTROL Outbound] processen (som körs efter att mål har skapats) inte hittar några användare som är mappade till den här [!UICONTROL UserID] nyckeln, kommer inga data att vara gränslösa.
* **Nej i valda fildatakällor:** När du väljer en annan måltyp än [!UICONTROL S2S]visas ett avsnitt längst ned på skärmen med etiketten [!UICONTROL Configure Data Sources]. När det här avsnittet visas första gången markeras inga värden. Om du glömmer att klicka i [!UICONTROL All First Party] kryssrutan eller väljer datakällor individuellt från [!UICONTROL Available Data Sources] fönstret, kommer inga data att vara gränslösa.

### Felkonfigurerat format

När du väljer ett format för dina utgående data är det bäst att återanvända ett befintligt format om det är möjligt. Om du använder ett redan beprövat format kan du vara säker på att dina utgående data genereras korrekt. Om du vill se exakt hur ett befintligt format är formaterat klickar du på [!UICONTROL Formats] alternativet på menyraden och söker efter formatet antingen efter namn eller efter ID-nummer. Felformaterade format eller makron som används i format ger felaktigt formaterade utdata eller förhindrar att informationen skrivs ut helt.

Mer information om hur du ställer in format och använder makron finns i [Filformatmakron](formats/file-formats.md#) och [HTTP-formatmakron](formats/web-formats.md).

### Felkonfigurerad server

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * Ange inga prefix för värdnamn. Om du har fått ett konto [!DNL ftp://hello.com]skriver du bara [!DNL hello.com] i det här fältet.
   * **[!UICONTROL Port/Type Combination]**
      * För en [!DNL FTP] överföring är den önskade överföringstypen [!DNL SFTP].
      * När du väljer [!DNL SFTP] typ är porten nästan alltid 22.
      * När du väljer [!DNL FTPs/TLS] typ är porten nästan alltid 21.
      * Typen [!DNL FTPs/TLS] är inte densamma som en vanlig [!DNL FTP] överföring. Vi stöder inte regelbundna (osäkra) [!DNL FTP] överföringar.
   * **[!UICONTROL Remote Path]**
      * När du väljer en fjärrunderbana bör den anges utan inledande snedstreck.
      * Om den överförda filen ska placeras i [!DNL (root)/inbound] undermappen lägger du bara till [!DNL inbound] fjärrsökvägen, inte [!DNL /inbound].
      * Om du skickar filer med flera kataloger längs sökvägen anger du snedstreck mellan varje katalog. Om du har fått platsen för [!DNL /inbound/subdirectory1/subdirectory2]bör du ange [!DNL inbound/subdirectory1/subdirectory2] i det här fältet.
      * Om filen ska placeras i katalogen automatiskt dirigeras till av den externa servern kan du lämna detta utrymme tomt. Ange ingen punkt (. ), snedstreck ( / ) eller något annat.

* **[!DNL S3]**
   * [!DNL S3] är det överföringsprotokoll som rekommenderas (framför [!DNL FTP] eller [!DNL HTTP]).
      * **[!UICONTROL Bucket]**
         * Bucket-namnet ska visas utan snedstreck, prefix, suffix osv. Om du får adressen [!DNL s3://your-bucket] behöver du bara lägga [!DNL your-bucket] till den här rutan.
      * **[!UICONTROL Directory]**
         * Lämna det här fältet tomt om du inte uttryckligen har fått en underkatalog där data ska placeras. Om du får adressen [!DNL s3://your-bucket/your-subdirectory]anger du [!DNL your-bucket] i [!UICONTROL Bucket] fältet och [!DNL your-subdirectory] läggs in i [!UICONTROL Directory] fältet. Lägg inte till föregående snedstreck.
         * Om du behöver flytta flera kataloger nedåt i banan bör du bara använda snedstreck som avgränsare. Så en plats för [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] skulle ha [!DNL your-bucket] i [!UICONTROL Bucket] fältet och [!DNL your-subdirectory1/your-subdirectory2] angetts i [!UICONTROL Directory] fältet.
      * **[!UICONTROL Access / Secret Keys]**
         * När [!DNL TechOps] skapar en bucket och ger åtkomst/hemliga nycklar till en konsult, är dessa uppgifter vanligtvis `READ-ONLY` autentiseringsuppgifter som ska skickas till klienten. Dessa autentiseringsuppgifter ska inte anges i [!UICONTROL Access / Secret Key] fälten eftersom det gör att överföringen misslyckas (eftersom autentiseringsuppgifterna är skrivskyddade och inte skrivbara). Om en bucket [!DNL TechOps] skapas och inloggningsuppgifterna tillhandahålls ska konsulten också begära ett nyckelpar från Adobe - INTE ATT GES TILL KLIENTEN - som gör det möjligt att skriva filer till den här bucket. Nyckeln ska läggas till i dessa fält.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * Ange prefixinformation för [!DNL HTTP] poster. Om du har fått ett konto [!DNL https://superduper.com]anger du [!DNL https://superduper.com] i det här fältet.
      * **[!UICONTROL URL Prefix]**
         * Lämna det föregående snedstrecket inaktiverat när du lägger till ett [!DNL URL] prefix. Adressen [!DNL https://hello.com/r/x/y/z] ska ha [!DNL https://hello.com] angetts i [!UICONTROL Domain] fältet och [!DNL r/x/y/z] angetts här i [!UICONTROL URL Prefix] fältet.
         * Om ett värde inte [!UICONTROL URL Prefix] behövs lämnar du det här värdet tomt.
      * **[!UICONTROL Authentication - SSH Key]**
         * Ange det fullständiga `SSH PRIVATE` nyckelvärdet i den här rutan, inklusive sidhuvuden, sidfötter och radbrytningar, för att säkerställa korrekt kryptering/nyckellagring.

### Inte tillräckligt med tid för utgående generering

Den utomordentliga processen körs två gånger dagligen och flera processer (överlagring, publicering, till externa platser osv.) måste köras innan en fil överförs till det slutliga målet. En bra tumregel är att ett mål ska vara helt konfigurerat minst 24 timmar innan du kan förvänta dig att data ska skickas till en extern plats.

### För stora fildelningsstorlekar

När du exporterar filer till mål kan du dela upp större utgående filer i filsegment. Kontrollera att de enskilda filsegmenten inte överstiger 10 GB. Se även [Namn på utgående datafil: Syntax och exempel](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html).


## Så här konfigurerar du destinationer för att exportera Experience Cloud-ID:n, kund-ID:n eller Audience Manager-ID:n i utgående datafiler {#set-up-destinations-export}

På den här sidan visas hur du ställer in destinationer för att exportera data som är sparade från den ID-typ som du vill använda [!UICONTROL Outbound Data Files].

<!-- set-up-destinations-mcid-aamid.xml -->

Destinationer gör att våra kunder kan aktivera sina data i valfritt antal digitala kanaler. De kan till exempel exportera målgruppsdata till andra [!DNL Adobe Experience Cloud] lösningar ([!DNL Target], [!DNL Campaign]osv.). Eller så kan de skicka data till [!UICONTROL DSP]s, [!UICONTROL SSP]s eller någon annan plattform som är integrerad med Audience Manager. Vi har en lista över partners vi samarbetar med på vår [Integrations-Wiki-sida](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>En detaljerad genomgång av hur du skapar mål i administratörsgränssnittet finns i artikeln [Skapa eller redigera företagsmål](companies/admin-manage-company-destinations.md#create-edit-company-destinations) .

Dina kunder vill exportera olika ID-typer beroende på destination. I konfigurationsdiagrammet nedan visas de alternativ du bör välja för att exportera profilinformation som är relaterad till olika ID-typer. Vi rekommenderar att du även refererar till [index för ID:n i Audience Manager](https://marketing.adobe.com/resources/help/en_US/aam/ids-in-aam.html). Det finns tre viktiga inställningar att tänka på: [!UICONTROL User ID Key], [!UICONTROL Data Source Type] och [!UICONTROL Format]. Vi detaljerar alla nedan.

* [!UICONTROL User ID Key]. Gå in [!UICONTROL Admin UI], gå till **[!UICONTROL Companies]**. Sök efter kundens företag och klicka på det. Leta efter **[!UICONTROL Destinations]** fliken och tryck **[!UICONTROL Add Destination]**. Markera alternativet i **[!UICONTROL Add Destination]** arbetsflödet [!UICONTROL User ID Key]. Inkommande ID:n [!UICONTROL User ID Key] filtreras från måldatakällan och endast ID:n kan skickas.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]. Välj det här alternativet när du skapar ett mål i gränssnittet för Audience Manager. Först markerar du [!UICONTROL Inbound]och sedan den ID-typ du vill använda. Alternativen är:

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]. Det här alternativet avgör vilket filformat du ska exportera. Välj format under **[!UICONTROL Add Destination]** arbetsflödet **[!UICONTROL Batch Data]**.

Om du vill kontrollera ett format går du till **[!UICONTROL Admin UI > Formats]** och letar efter [!UICONTROL Data Row] elementet. Det här elementet innehåller ett makro med filformatet &lt;MCID> i exemplet nedan.

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
   <td colname="col2"> <p>Experience Cloud-ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UID&gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud-ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud-ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud-ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Experience Cloud-ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager-ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UID&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager-ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud-ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager-ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID (Alla datakällor som företaget har tillgång till) </p> </td> 
   <td colname="col2"> <p>Kund-ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UID&gt; </p> </td> 
   <td colname="col4"> <p>Kund-ID (DPUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID (Alla datakällor som företaget har tillgång till) </p> </td> 
   <td colname="col2"> <p>Kund-ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud-ID </p> </td> 
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
   <td colname="col2"> <p>Audience Manager-ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UID&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID (Alla datakällor som företaget har tillgång till) </p> </td> 
   <td colname="col2"> <p>Audience Manager-ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud-ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID (Alla datakällor som företaget har tillgång till) </p> </td> 
   <td colname="col2"> <p>Audience Manager-ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
 </tbody> 
</table>

## Användningsexempel

Säg att du använder Audience Manager och [!DNL Campaign]. För att kunddata ska kunna användas i [!DNL Campaign]vill du exportera [!UICONTROL Experience Cloud IDs]. Du bör använda konfigurationsnummer 3 i det här fallet.