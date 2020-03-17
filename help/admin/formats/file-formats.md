---
description: Visar makron som du kan använda för att skapa FTP-baserade datafiler. Vissa makron kan användas för alla datafilsfält och rader. Andra makron är specifika för huvud- och datarader.
seo-description: Visar makron som du kan använda för att skapa FTP-baserade datafiler. Vissa makron kan användas för alla datafilsfält och rader. Andra makron är specifika för huvud- och datarader.
seo-title: Filformatmakron
title: Filformatmakron
uuid: f91c91b6-6581-4ed7-8d7f-f8532bd41df9
translation-type: tm+mt
source-git-commit: e1122a7f3d3e8c2d67616eb56cb186a4750ed29b

---


# Filformatmakron {#file-format-macros}

Visar makron som du kan använda för att skapa [!DNL FTP]baserade datafiler. Vissa makron kan användas för alla datafilsfält och rader. Andra makron är specifika för huvud- och datarader.

## Vanliga makron {#common-macros}

Dessa makron kan användas i alla formatfält. Exempel finns i Exempel på [filformatsmakro](../formats/file-format-examples.md).

<table id="table_A3309E175ABF4651BD11CE3632B3C553"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Makro </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>ASCII_SOH</code> </p> </td> 
   <td colname="col2"> <p>Ett ASCII-tecken som inte skrivs ut. Det anger början på en rad eller ett avsnitt med innehåll. Den kan också användas för att avgränsa datakolumner i en fil. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p>ID för måldataprovider. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_DPID</code> </p> </td> 
   <td colname="col2"> <p>Nyckelproviderns ID för användar-ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ID</code> </p> </td> 
   <td colname="col2"> <p>Order-/mål-ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PIDALIAS</code> </p> </td> 
   <td colname="col2"> <p>Ett alias för ett order-/mål-ID. </p> <p>Värdet för det här aliaset anges i <span class="wintitle"> fältet Sekundärt konto-ID </span> för ett mål (i <span class="wintitle"> avsnittet Grundinställningar </span> ). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_MODE</code> </p> </td> 
   <td colname="col2"> <p>Anger synkroniseringstyp. Accepterar följande valfria variabler: </p> 
    <ul id="ul_87E8E3CE6565447A9810B5119298CC7B"> 
     <li id="li_66F4889FB84E40AC92F69F3FF6B0042C"> <code>full</code>: Fullständig synkronisering. </li> 
     <li id="li_BFE2C2D9A33A44FB9A840A7232ECCFFF"> <code>iter</code>: Inkrementell synkronisering. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_TYPE</code> </p> </td> 
   <td colname="col2"> <p>Anger dataöverföringsmetod. Accepterar följande valfria variabler: </p> 
    <ul id="ul_13BE35BBBF7C4C67AEFC514C5D192902"> 
     <li id="li_195FE9B4C5494600BD17D7172A8FB630"> <code>ftp</code> </li> 
     <li id="li_751AD59C4C934D66BC530D9806B500AF"> <code>http</code> </li> 
     <li id="li_4638AF7D1FB54E2C890045048B85309C"> <code>s3</code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIMESTAMP</code> </p> </td> 
   <td colname="col2"> <p>En 10-siffrig UTC-, Unix-tidsstämpel. </p> <p>Den kan även formateras som <code>YYYYMMDDhhmmss</code> följande formateringsregler för Java-datum/tidsstämpel. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Makron för rubrikfält {#header-field-macros}

Makron används endast i rubrikfält. Exempel finns i Exempel på [filformatsmakro](../formats/file-format-examples.md).

<table id="table_1A8BD1750F4940B3A34E3F80371A447A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Makro </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>Makrot används som avgränsare och infogar en tabb mellan fält. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Dataradmakron {#data-row-macros}

Makron används endast i datarader. Exempel finns i Exempel på [filformatsmakro](../formats/file-format-examples.md).

<table id="table_E378F94A3907407AA8110C8EE6C10909"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Makro </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>CLOSE_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>Infogar ett avslutande klammerparentes }-tecken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>COMMA</code> </p> </td> 
   <td colname="col2"> <p>Infogar ett komma. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="term"> Unik användaridentifierare för datapartnern </span>. Returnerar det ID som du har tilldelat en användare/webbplatsbesökare om detta ID redan har synkroniserats med ett <span class="keyword"> Audience Manager- </span> enhets-ID. </p> <p>Om DPID är 0 returnerar det här makrot <span class="keyword"> Audience Manager- </span> ID:t i stället för användarens ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID_LIST</code> </p> </td> 
   <td colname="col2"> <p>Returnerar en lista som innehåller flera ID:n för en datapartner. Detta är användbart om du har en stor organisation med flera indelningar eller andra organisationsgrupper som du kan dela data med. Detta makro returnerar en lista över ID:n för dessa underordnade grupper. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPUUIDS</code> </p> </td> 
   <td colname="col2"> <p>Utdata för det här makrot mappar DataProvider ID (DPID) till relaterade unika användar-ID:n (DPUID). Detta makro måste ha en formateringssträng för att styra utdata. Exempelutdata skulle se ut ungefär så här: </p> <p> <code>"dpids=dpid1,dpid2,...dpid n|maxMappings= n|format=json"</code> </p> <p>Inställningen anger <code>maxMappings</code> hur många mappningar du vill att makrot ska returnera. När <code>maxMappings=0</code>det här makrot returnerar alla mappningar för varje angivet DPID. Data sorteras efter tidsstämpel (senaste först) och returnerar resultat med den största tidsstämpeln först. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>endif</code> </p> </td> 
   <td colname="col2"> <p>Krävs när du använder villkorsstyrda <code>if</code> makron samt <code>SEGMENT_LIST</code> - och <code>REMOVED_SEGMENT_LIST</code> -makron. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>if(SEGMENT_LIST &amp;&amp; REMOVED_SEGMENT_LIST)endif</code> </p> </td> 
   <td colname="col2"> <p>Den här kombinationen av makron skapar en villkorssats som listar de segment som användarna tillhör <i>och</i> har tagits bort från. Den returnerar en tom sträng om båda villkoren inte uppfylls eller om det inte finns några data. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Experience Cloud </span> ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPEN_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>Infogar en öppen klammerparentes {-tecken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPT_OUT</code> </p> </td> 
   <td colname="col2"> <p>Föråldrat. Skall ej användas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_TYPE</code> </p> </td> 
   <td colname="col2"> <p>Föråldrat. Skall ej användas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_VALUE</code> </p> </td> 
   <td colname="col2"> <p>Returnerar <code>1</code> som ett statiskt, hårdkodat värde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID</code> </p> </td> 
   <td colname="col2"> <p>Partner-ID (PID). PID:t visas under <span class="wintitle"> fliken Profil </span> i administratörsgränssnittet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Returnerar en lista med eventuella segment som har tagits bort. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Returnerar en lista med segment i en lista. Accepterar följande valfria variabler: </p> 
    <ul id="ul_B111AA0D6C18445598A1444B8B7E9325"> 
     <li id="li_8603B40229624856AF1FBC434DB8F16A"> <code>segmentId</code>: Äldre ID. Föråldrat. Använd <code>sid</code> (endast gemener). </li> 
     <li id="li_1EF40DDCA3C5447586904CF021D8F912"> <code>csegid</code>: Äldre ID. Föråldrat. Använd <code>sid</code> (endast gemener). </li> 
     <li id="li_D85F0A5D16AE4DAFB55C17DBB35EA66E"> <code>sid</code>: Segment-ID. </li> 
     <li id="li_9BE103EFD8384464B46FAC00422431DB"> <code>type</code>: Returnerar <code>5</code>ett statiskt, hårdkodat värde som identifierar data som segmentdata. </li> 
     <li id="li_FE5049089F2944FA9DB9F9D546DBA167"> <code>alias</code>: Mappning av segmentet. Föråldrat. Använd <code>sid</code> (endast gemener). </li> 
     <li id="li_DD778AA2D1DB4D409CF5026B5D9DBD27"> <code>lastUpdateTime</code>: En Unix-tidsstämpel som anger när ett segment senast realiserades. </li> 
    </ul> <p>Placera dessa variabler inom klammerparentes efter makrot. I den här koden avgränsas resultatet med ett vertikalstreck (|): <code>&lt;SEGMENT_LIST:{seg|&lt;seg.type&gt;,&lt;seg.sid&gt;}; separator="|"&gt;</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ATTRIBUTES</code> </p> </td> 
   <td colname="col2"> <p>Returnerar <code>1</code> som ett statiskt, hårdkodat värde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>Infogar en tabbavgränsare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Returnerar en lista med egenskaper. Accepterar följande valfria argument: </p> 
    <ul id="ul_757DEB56E4F849768468F3C166B0D171"> 
     <li id="li_859E1F4F21D645519F150DC512B3EB1A"> <code>type</code>: Trait-typer som identifieras av ett numeriskt ID. Den här variabeln returnerar: 
      <ul id="ul_C9839266783D42CCADAAC3FEA33BE4D7"> 
       <li id="li_6996A218E3F04EC3BC70032559DD87FC"> <code>10</code> som identifierar en DPM-egenskap (offline, tilldelad av ett inkommande jobb). </li> 
       <li id="li_831FF929BF50434C8804C13E5786DF79"> <code>3</code> som identifierar en regelbaserad egenskap (realtid, via <span class="wintitle"> DCS </span>). </li> 
      </ul> </li> 
     <li id="li_E84D6BC80AEE4F10963C9882C4151ED4"> <code>traitId</code>: Trait ID. </li> 
     <li id="li_D30A849BA35248E6B9110FA3ADEFC332"> <code>lastRealized</code>: Sist trait realiserades. Unix tidsstämpel. </li> 
    </ul> <p>Placera dessa variabler inom klammerparentes efter makrot. I den här koden avgränsas resultatet med ett vertikalstreck (|): <code>TRAIT_LIST{type|traitId};separator="|"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Användar-ID </span> för Audience Manager. </p> </td> 
  </tr> 
 </tbody> 
</table>