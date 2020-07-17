---
description: Alla uppdateringar (tillägg, borttagningar och korrigeringar) till Audience Manager Admin-handboken efter datum.
seo-description: Alla uppdateringar (tillägg, borttagningar och korrigeringar) till Audience Manager Admin-handboken efter datum.
seo-title: Dokumentationsuppdateringar
title: Dokumentationsuppdateringar
uuid: 1c02dff5-8e3f-42bf-a50c-03b75e121ac7
translation-type: tm+mt
source-git-commit: e60aa0ac341d74454bfe00a4f56add3a9f9e281b
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 100%

---


# Dokumentationsuppdateringar {#documentation-updates}

Alla uppdateringar (tillägg, borttagningar och korrigeringar) till Audience Manager Admin-handboken efter datum.

Information om funktionsversioner, förbättringar och felkorrigeringar finns i [versionsinformationen för Experience Cloud](https://marketing.adobe.com/resources/help/en_US/whatsnew/). Se den [föregående versionsinformationen](https://marketing.adobe.com/resources/help/en_US/whatsnew/c_legacy_releases.html) för äldre Experience Cloud-meddelanden. För [!DNL Audience Manager documentation changes, see] [dokumentationsuppdateringar ](https://docs.adobe.com/content/help/sv-SE/audience-manager/user-guide/documentation-updates/docs-2019.html).

## AAM 2019 – dokumentationsuppdateringar {#aam-2019-docs-updates}


| Hjälpavsnitt | Beskrivning |
---------|----------|
| HTTP-formatmakron | Vi har lagts till ett nytt makro, `REGION_ID_LIST`, och tre nya fält, `sda`, `sda` och `sda`, i `USER_LIST`-makrot. |
| HTTP-formatmakron | Vi har lagt till två nya makron: `ECID` och `MCID`. |


## AAM 2018 – dokumentationsuppdateringar {#aam-2018-docs-updates}

<!-- c_doc_updates.xml -->

<table id="table_AECF59E131F84E7791A5A421BFB203FA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Hjälpavsnitt </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/create-ftp-server.md#task_BF1DD0E5ECA64AEC87EACABFCAEA2C6D"> Skapa eller redigera en FTP-server</a> </p> </td> 
   <td colname="col2"> <p>Vi har lagt till mer information om SSH-nyckelautentisering för SFTP-servrar (steg 5). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-destination-troubleshooting.md#set-up-destinations-export"> Så här konfigurerar du destinationer för att exportera från Experience Cloud...</a> </p> </td> 
   <td colname="col2"> <p>Den här sidan visar hur du ställer in destinationer för att exportera data för den ID-typ som du vill använda i utgående datafiler. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/admin-authorize-s3-cross-bucket.md#task_20B12994C5484A9D8CC40DF6F456CBE7"> Gör så här: Auktorisera kontoövergripande åtkomst till Amazon S3 Bucket för batchdestinationer</a> </p> </td> 
   <td colname="col2"> <p>En kund kan använda övergripande kontobehörigheter för buckets i Amazon S3 för att leverera utgående datafiler om kunden inte vill dela åtkomstnycklar och hemliga nycklar för Amazon S3. Det här dokumentet visar hur ni ställer in det här alternativet i gränssnittet för Audience Manager Admin. </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2017 – dokumentationsuppdateringar {#aam-2017-docs-updates}

<table id="table_81D2DA9293A9417085C630D00A7C96E1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Hjälpavsnitt </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE"> HTTP-formatmakron</a> </td> 
   <td colname="col2">Makrot <code>segmentId</code> har ersatts med <code>legacySegmentId</code> och makrot <code>newSegmentId</code> har lagts till. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-company-limits.md#task_3004C10CB9A9430A8D25E25BB830B5D6">Hantera företagsgränser</a> </td> 
   <td colname="col2"> Maximalt mappnummer och strukturdjup för traits har lagts till i dokumentationen om gränser. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="formats/enable-outbound-seq.md#concept_526744C9433F40BF8269E18245B2F0BD"> Aktivera Hadoop-sekvens för utgående filöverföringar</a> </td> 
   <td colname="col2"> Läs om hur kunder kan skicka utgående SEQ-filer till en Hadoop-instans. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967"> Hantera behållare</a> </td> 
   <td colname="col2"> En kort instruktion om hur du skapar behållare har lagts till. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-manage-company-destinations.md#create-edit-company-destinations">Skapa eller redigera företagsdestinationer </a> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_527E0E75C03846B0AB39EEE544904BE2"> 
      <li id="li_FC276B34158D44E3A5450C6C8BAF3184">Instruktioner om att balansera användningen av fullständiga och inkrementella synkroniseringar har lagts till. </li> 
      <li id="li_3975DA78DE9E441D8F8CB80F752DD7B7">Etableringen av <span class="keyword"> Adobe Media Optimizer</span> som <span class="keyword"> Audience Manager</span>-destination sker i <span class="keyword"> Adobe Media Optimizer</span>. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> Hantera företagsdestinationer</a> </p> </td> 
   <td colname="col2"> <p>Mindre ändringar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-amo-sync.md#concept_2B5537233DAA4860B3503B344F937D83"> ID-synkronisering med Media Optimizer</a> </p> </td> 
   <td colname="col2"> <p>Ny dokumentation som beskriver kryssrutan för AMO-synkronisering i varje företagsbehållare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-device-graph-options.md#concept_563615F1018340C683E0EE075F8F639D"> Alternativ för enhetsdiagram för företag</a> </p> </td> 
   <td colname="col2"> <p>Ny dokumentation som beskriver hur ni konfigurerar alternativ för enhetsdiagram. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-oauth2/aam-admin-api-requirements.md#concept_A7FAC9443CF34974A873E6B787616421"> Krav och rekommendationer för API</a> </p> </td> 
   <td colname="col2"> <p>Ny dokumentation som beskriver vissa krav och rekommendationer som du bör tänka på och skicka vidare till kunderna. Detta dupliceras i de offentliga dokumenten med samma titel och ändras för olika läsare. Se <a href="https://docs.adobe.com/content/help/sv-SE/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.translate.html#api-requirements-recommendations" format="https" scope="external"> Krav och rekommendationer för API</a> i de offentliga dokumenten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2016 – dokumentationsuppdateringar {#aam-2016-docs-updates}

<table id="table_E9D9810EA8244B58A4F27D56CFE521FD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Hjälpavsnitt </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="admin-servers/create-ftp-server.md#task_BF1DD0E5ECA64AEC87EACABFCAEA2C6D"> Skapa eller redigera en FTP-server</a> </td> 
   <td colname="col2">Utgående FTP IP <b>52.44.29.204</b> har lagts till. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> Hantera företagsdestinationer</a> </p> </td> 
   <td colname="col2"> <p>Mindre ändringar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/create-http-server.md#task_5BF59581868E4144B965D644D36BEACD"> Skapa eller redigera en HTTP-server</a> </p> </td> 
   <td colname="col2"> <p>En <b>HTTP-signatur</b> har lagts till i guiden Skapa serverkonfiguration. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-beta-environment.md#concept_4AA12E66F49A452C8BA4E91AA28060AA"> Beta-miljö</a> </p> </td> 
   <td colname="col2"> <p>Uppdaterade URL:er och värdnamn i betamiljön. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/outbound-active-user-filter.md#task_F5CF8BDDA5DB4D23837B59CADF7A623B"> Filtrera utgående data endast efter aktiva användare</a> </p> </td> 
   <td colname="col2"> <p>Instruktioner för att generera en fullständig synkroniseringsfil som endast innehåller aktiva användare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE"> HTTP-formatmakron</a> </p> </td> 
   <td colname="col2" morerows="1"> <p>Ny dokumentation som visar HTTP-makron och vanliga exempel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> Exempel på HTTP-formatmakro</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2015 – dokumentationsuppdateringar {#aam-2015-docs-updates}

<table id="table_90F524BAAED44A45A1F6BF8BBA9F26F9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Datum och hjälpavsnitt </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>December 2015 </p> <p><a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2">Format</a> </p> </td> 
   <td colname="col2"> <p>Ändrat makroavsnitt och nya exempel. </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2014 – dokumentationsuppdateringar {#aam-2014-docs-updates}

<table id="table_FA9962E19248418BA73D5A794A378C9D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Datum och hjälpavsnitt </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>12 november 2014 </p> <p> <a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2">Format</a> </p> </td> 
   <td colname="col2"> <p>Information om makrot &lt;MCID&gt; har lagts till. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>23 oktober 2014 </p> <p><a href="formats/admin-create-format.md#task_1A51FC9189DB439FB218D91F3875FD67"> Skapa eller redigera ett format</a> </p> </td> 
   <td colname="col2"> <p>Information om alternativet <span class="wintitle"> .info-kvitto</span> har lagts till. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>23 oktober 2014 </p> <p><a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2">Format</a> </p> </td> 
   <td colname="col2"> <p>Ny sida. Observera att den här sidan är ett pågående arbete och att den kommer att uppdateras under de kommande dagarna. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>22 oktober 2014 </p> <p><a href="admin-destination-troubleshooting.md#">Felsökning av destinationsinställningar</a> </p> </td> 
   <td colname="col2"> <p>Nytt hjälpavsnitt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>21 oktober 2014 </p> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> Hantera företagsdestinationer</a> </p> </td> 
   <td colname="col2"> <p>Hela hjälpavsnittet har omarbetats. Mer information och fler inställningar har lagts till. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>25 september 2014 </p> <p><a href="companies/admin-manage-company-profiles.md"> Skapa ett företag</a> </p> </td> 
   <td colname="col2"> <p>Mer information har lagts till i avsnitten <span class="wintitle"> Livscykel</span> och <span class="wintitle"> Kontotyper</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>25 september 2014 </p> <p><a href="companies/admin-manage-company-profiles.md#edit-company-profile"> Redigera en företagsprofil</a> </p> </td> 
   <td colname="col2"> <p>Mer information har lagts till i avsnitten <span class="wintitle"> Livscykel</span> och <span class="wintitle"> Kontotyper</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>