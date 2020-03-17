---
description: Alla uppdateringar (tillägg, borttagningar och korrigeringar) till Audience Manager Admin Guide, per datum.
seo-description: Alla uppdateringar (tillägg, borttagningar och korrigeringar) till Audience Manager Admin Guide, per datum.
seo-title: Dokumentationsuppdateringar
title: Dokumentationsuppdateringar
uuid: 1c02dff5-8e3f-42bf-a50c-03b75e121ac7
translation-type: tm+mt
source-git-commit: e60aa0ac341d74454bfe00a4f56add3a9f9e281b

---


# Dokumentationsuppdateringar {#documentation-updates}

Alla uppdateringar (tillägg, borttagningar och korrigeringar) till Audience Manager Admin Guide, per datum.

Information om funktionsreleaser, förbättringar och felkorrigeringar finns i [versionsinformationen](https://marketing.adobe.com/resources/help/en_US/whatsnew/)för Experience Cloud. Se [föregående versionsinformation](https://marketing.adobe.com/resources/help/en_US/whatsnew/c_legacy_releases.html) för äldre Experience Cloud-meddelanden. För [!DNL Audience Manager documentation changes, see] dokumentationsuppdateringar [](https://docs.adobe.com/content/help/en/audience-manager/user-guide/documentation-updates/docs-2019.html).

## AAM 2019 - dokumentationsuppdateringar {#aam-2019-docs-updates}


| Ämne | Beskrivning |
---------|----------|
| HTTP-formatmakron | Vi har lagt till ett nytt makro `REGION_ID_LIST`och tre nya fält,`sda`och`sda``sda` till `USER_LIST` makrot. |
| HTTP-formatmakron | Vi har lagt till två nya makron: `ECID` och `MCID`. |


## AAM 2018 - dokumentationsuppdateringar {#aam-2018-docs-updates}

<!-- c_doc_updates.xml -->

<table id="table_AECF59E131F84E7791A5A421BFB203FA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Ämne </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/create-ftp-server.md#task_BF1DD0E5ECA64AEC87EACABFCAEA2C6D"> Skapa eller redigera en FTP-server</a> </p> </td> 
   <td colname="col2"> <p>Vi lade till mer information om SSH-nyckelautentisering för SFTP-servrar (steg 5). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-destination-troubleshooting.md#set-up-destinations-export"> Så här konfigurerar du dina mål för att exportera Experience Cloud..</a> </p> </td> 
   <td colname="col2"> <p>På den här sidan visas hur du ställer in mål för att exportera data som är sparade från den ID-typ som du vill använda i utgående datafiler. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/admin-authorize-s3-cross-bucket.md#task_20B12994C5484A9D8CC40DF6F456CBE7"> Använda: Auktorisera åtkomst till Amazon S3 Bucket för batchdestinationer för korskonto</a> </p> </td> 
   <td colname="col2"> <p>Våra kunder kan använda kontobucket-behörigheter i Amazon S3 för att leverera utgående datafiler, om de inte vill dela åtkomstnycklar och hemliga nycklar för Amazon S3. I det här dokumentet visas hur du ställer in det här alternativet i gränssnittet för Audience Manager Admin. </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2017 - dokumentationsuppdateringar {#aam-2017-docs-updates}

<table id="table_81D2DA9293A9417085C630D00A7C96E1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Ämne </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE"> HTTP-formatmakron</a> </td> 
   <td colname="col2">Ersatte <code>segmentId</code> makrot med <code>legacySegmentId</code> och lade till <code>newSegmentId</code> makrot. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-company-limits.md#task_3004C10CB9A9430A8D25E25BB830B5D6"> Hantera företagsbegränsningar</a> </td> 
   <td colname="col2"> Mappnummer och strukturdjup för trait har lagts till i begränsningsdokumentationen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="formats/enable-outbound-seq.md#concept_526744C9433F40BF8269E18245B2F0BD"> Aktivera filöverföringar för Hadoop-sekvensöverföring för utgående</a> </td> 
   <td colname="col2"> Läs om hur du kan göra det möjligt för kunder att skicka utgående SEQ-filer till sin egen Hadoop-instans. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967"> Hantera behållare</a> </td> 
   <td colname="col2"> En kort instruktion om hur du skapar behållare har lagts till. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-manage-company-destinations.md#create-edit-company-destinations"> Skapa eller redigera företagsmål</a> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_527E0E75C03846B0AB39EEE544904BE2"> 
      <li id="li_FC276B34158D44E3A5450C6C8BAF3184">Lagt till instruktioner för att balansera användningen av fullständiga och inkrementella synkroniseringar. </li> 
      <li id="li_3975DA78DE9E441D8F8CB80F752DD7B7">Tillhandahållandet av <span class="keyword"> Adobe Media Optimizer</span> som <span class="keyword"> Audience Manager</span> -mål görs i <span class="keyword"> Adobe Media Optimizer</span>. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> Hantera företagsdestinationer</a> </p> </td> 
   <td colname="col2"> <p>Mindre ändringar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-amo-sync.md#concept_2B5537233DAA4860B3503B344F937D83"> ID-synkronisering med Media Optimizer</a> </p> </td> 
   <td colname="col2"> <p>Ny dokumentation som beskriver kryssrutan för synkronisering av AMO i varje företagsbehållare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-device-graph-options.md#concept_563615F1018340C683E0EE075F8F639D"> Alternativ för enhetsdiagram för företag</a> </p> </td> 
   <td colname="col2"> <p>Ny dokumentation som beskriver hur du konfigurerar alternativ för enhetsdiagram. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-oauth2/aam-admin-api-requirements.md#concept_A7FAC9443CF34974A873E6B787616421"> Krav och rekommendationer för API</a> </p> </td> 
   <td colname="col2"> <p>Ny dokumentation som beskriver vissa krav och rekommendationer för att vara medvetna om och skicka vidare till kunderna. Detta dupliceras i de offentliga dokumenten med samma titel och ändras för olika läsare. Se <a href="https://marketing.adobe.com/resources/help/en_US/aam/aam-api-requirements.html" format="https" scope="external"> API-krav och -rekommendationer</a> i de offentliga dokumenten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2016 - dokumentationsuppdateringar {#aam-2016-docs-updates}

<table id="table_E9D9810EA8244B58A4F27D56CFE521FD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Ämne </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="admin-servers/create-ftp-server.md#task_BF1DD0E5ECA64AEC87EACABFCAEA2C6D"> Skapa eller redigera en FTP-server</a> </td> 
   <td colname="col2">Added the egress FTP IP <b>52.44.29.204</b>. </td> 
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
   <td colname="col1"> <p><a href="admin-beta-environment.md#concept_4AA12E66F49A452C8BA4E91AA28060AA"> Beta Environment</a> </p> </td> 
   <td colname="col2"> <p>Uppdaterade URL:er och värdnamn i betamiljön. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/outbound-active-user-filter.md#task_F5CF8BDDA5DB4D23837B59CADF7A623B"> Filtrera utgående data endast för aktiva användare</a> </p> </td> 
   <td colname="col2"> <p>Instruktioner för att generera en fullständig synkroniseringsfil som endast innehåller aktiva användare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE"> HTTP-formatmakron</a> </p> </td> 
   <td colname="col2" morerows="1"> <p>Ny dokumentation som visar HTTP-makron och vanliga exempel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> Exempel på makro i HTTP-format</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2015 - dokumentationsuppdateringar {#aam-2015-docs-updates}

<table id="table_90F524BAAED44A45A1F6BF8BBA9F26F9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Datum och ämne </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>December 2015 </p> <p><a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> Format</a> </p> </td> 
   <td colname="col2"> <p>Ändrat makroavsnitt och nya exempel. </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2014 - dokumentationsuppdateringar {#aam-2014-docs-updates}

<table id="table_FA9962E19248418BA73D5A794A378C9D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Datum och ämne </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>12 november 2014 </p> <p> <a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> Format</a> </p> </td> 
   <td colname="col2"> <p>Information om makrot &lt;MCID&gt; har lagts till. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>23 oktober 2014 </p> <p><a href="formats/admin-create-format.md#task_1A51FC9189DB439FB218D91F3875FD67"> Skapa eller redigera ett format</a> </p> </td> 
   <td colname="col2"> <p>Information om <span class="wintitle"> .info- </span>kvittoalternativet har lagts till. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>23 oktober 2014 </p> <p><a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> Format</a> </p> </td> 
   <td colname="col2"> <p>Ny sida. Observera att den här sidan är ett pågående arbete och kommer att uppdateras under de kommande dagarna. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>22 oktober 2014 </p> <p><a href="admin-destination-troubleshooting.md#"> Felsökning av målinställningar</a> </p> </td> 
   <td colname="col2"> <p>Nytt ämne. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>21 oktober 2014 </p> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> Hantera företagsdestinationer</a> </p> </td> 
   <td colname="col2"> <p>Hela ämnet har omarbetats. Ytterligare information och ytterligare inställningar har lagts till. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>25 september 2014 </p> <p><a href="companies/admin-manage-company-profiles.md"> Skapa ett företag</a> </p> </td> 
   <td colname="col2"> <p>Ytterligare information har lagts till i avsnitten <span class="wintitle"> Livscykel</span> och <span class="wintitle"> Kontotyper</span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>25 september 2014 </p> <p><a href="companies/admin-manage-company-profiles.md#edit-company-profile"> Redigera en företagsprofil</a> </p> </td> 
   <td colname="col2"> <p>Ytterligare information har lagts till i avsnitten <span class="wintitle"> Livscykel</span> och <span class="wintitle"> Kontotyper</span> . </p> </td> 
  </tr> 
 </tbody> 
</table>