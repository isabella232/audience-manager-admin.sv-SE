---
description: Skapa, redigera och ta bort mål för Audience Manager.
seo-description: Create, edit, and delete Audience Manager destinations.
seo-title: Manage Company Destinations
title: Hantera företagsdestinationer
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
exl-id: a2e73613-07cd-4ab8-8c6e-be451ed50bfc
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 1%

---

# Hantera företagsdestinationer {#manage-company-destinations}

Skapa, redigera och ta bort mål för Audience Manager.

<!-- t_company_destinations.xml -->

Mer information finns i [Destinationer](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/destinations.html) i *Användarhandbok för Audience Manager*.

## Skapa eller redigera företagsdestinationer  {#create-edit-company-destinations}

Bläddra igenom avsnitten för steg-för-steg-instruktioner om hur du skapar nya [!DNL Audience Manager] destinationer eller redigera befintliga destinationer.

<!-- create-edit-company-destinations.xml -->

Besök [Experience Cloud partnerintegrationssida](https://wiki.corp.adobe.com/x/mPIMPw) innan du ställer in mål. Sidan innehåller den specifika information som du behöver fylla i för varje [!DNL Audience Manager] partnerintegrering.

Om din kund vill använda [!DNL Adobe Media Optimizer] som mål i [!DNL Audience Manager] måste du konfigurera detta i [!DNL Adobe Media Optimizer].

## Navigera till fliken Destinationer {#navigate-destinations}

1. Klicka **[!UICONTROL Companies]** letar du upp och klickar på önskat företag för att visa [!UICONTROL Profile] sida. Du kan använda [!UICONTROL Search] eller sidnumreringskontrollerna längst ned i listan för att hitta det önskade företaget. Du kan sortera varje kolumn i stigande eller fallande ordning genom att klicka på den önskade kolumnens rubrik.
1. Klicka på **[!UICONTROL Destinations]** -fliken.
1. Om du vill skapa ett nytt mål klickar du på **[!UICONTROL Add Destination]**. Om du vill redigera ett befintligt mål klickar du på målets namn i dialogrutan **[!UICONTROL Name]** kolumn.

## Grundinställningar {#basic-settings}

Fylla i fälten i **[!UICONTROL Basic Settings]** -fönstret.

* **[!UICONTROL Name]:** (Obligatoriskt) Ange namnet på det här målet.
* **[!UICONTROL Description]:** Ange beskrivande information om det här målet.
* **[!UICONTROL Type]:** (Obligatoriskt) Välj önskad måltyp:
   * **[!UICONTROL Bulk ID]**: Synkronisera ID:n mellan olika plattformar.
   * **[!UICONTROL Bulk Trait]**: Skicka satsvis information till olika plattformar.
   * **[!UICONTROL Bulk Segment]**: Skicka gruppinformation till olika plattformar.
   * **[!UICONTROL S2S]**: Använd server-till-server-mål för att skicka realtids- och batchdata till olika plattformar.
* **[!UICONTROL Auto-Fill Destination Mapping]:** ( [!UICONTROL S2S] bara) Välj ett alternativ:
   * **[!UICONTROL Segment ID]:** Om du väljer den här inställningen fylls målvärdesmappningen med [!DNL Audience Manager] Segment-ID.
   * **[!UICONTROL Integration Code Value]:** Om du väljer den här inställningen fylls målvärdesmappningen med [!DNL Audience Manager] Integreringskod för segment.
* **[!UICONTROL User ID Key]:** (Obligatoriskt) Välj önskad användar-ID-nyckel för det här målet i listrutan.

Detta ID används som överordnad ID för datakälla. Detta avgör vilka användar-ID:n som ska vara gränslösa i filen.

>[!NOTE]
>
>För [!UICONTROL Bulk ID] måltyp, du kan inte använda [!DNL Audience Manager] [!UICONTROL User ID] eller [!DNL Adobe Experience Cloud] ID.

Om ditt ID för datakälla ( [!UICONTROL DPID]) visas inte i listrutan. Du måste välja **[!UICONTROL Outbound]** kryssrutan på datakällnivå på [Sidan Inställningar för datakälla](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/manage-datasources.html).

* **[!UICONTROL Target Data Source]:** (Obligatoriskt) Välj önskad datakälla för det här målet i listrutan. Den här inställningen aktiverar märkning av utgående data, vilket gör det möjligt att mata in i separata system på klientsidan.
* **[!UICONTROL Foreign Account ID]:** Ange ID för det externa kontot för det här målet. Detta är ID-värdet i mottagarens system för dessa utgående data.
* **[!UICONTROL Outbound Sample Rate Denominator]:** När den totala mängden returnerade data är okänd använder du den här inställningen för att bara returnera en exempelmängd data, i stället för hela mängden. Justera talet här för att representera en bråkdel av data (t.ex. returnerar värdet 100 1/100 av den normala mängden data och värdet 10 returnerar 1/10 av den normala mängden data). Standardvärdet är &quot;1&quot;, som returnerar alla data.

## Realtime-data (för S2S-mål) {#realtime-s2s}

Om du skapar en [!UICONTROL S2S] mål, fyll i fälten nedan:

**[!UICONTROL Servers]**: Markera önskat `HTTP` server för det här målet.
**[!UICONTROL Format]**: Välj önskat format för det här målet i listrutan: [!UICONTROL HTTP only].

>[!NOTE]
>
>För [!DNL S2S] kan du bara aktivera eller inaktivera [!UICONTROL Realtime] eller [!UICONTROL Batch] mål med hjälp av skjutreglagen Av/På på på skärmen. Du kan inte inaktivera båda alternativen.

## Batchdata {#batch-data}

För [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] eller [!UICONTROL Bulk Segment] mål, fyll i fälten nedan:

* **[!UICONTROL Protocol]**: (Obligatoriskt) Välj önskat protokoll för det här målet i listrutan:
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**: (Obligatoriskt) Välj önskad server för det här målet i listrutan.
* **[!UICONTROL Format]**: (Obligatoriskt) Välj önskat format för det här målet i listrutan: [!DNL HTTP] eller filtypen, beroende på vilket protokoll du väljer ovan.
* **[!UICONTROL Sync Type]**: (Obligatoriskt) Välj önskad synkroniseringstyp för det här målet. Detta anger nivån för användaraktiviteter som klienter vill inkludera i utgående order. Välj **[!UICONTROL Customer]** om kunderna bara är intresserade av att analysera segmentens kvalifikationer från sina egenskaper. Välj **[!UICONTROL Platform]** om de vill inkludera segmentkvalifikationer från externa aktiviteter i alla [!DNL Audience Manager] kunder.
* **[!UICONTROL Customer]**: Filen innehåller aktiva användare som endast har 1 trait-realisering i klientens egenskaper (associerat med klientens [!UICONTROL PID]) för den valda tidsperioden. Dina kunder bör använda det här alternativet för att skicka ut *realtid* segmentkvalifikationer för destinationer.
* **[!UICONTROL Platform]**: Filen innehåller aktiva användare som har minst en realtidsinteraktion, oavsett om det är ID-synkronisering eller spårbarhet, var som helst i alla [!DNL Audience Manager] klientens egenskaper (som är kopplade till alla klient-PID:n) för den valda tidsperioden. Dina kunder bör använda det här alternativet för att skicka ut *total* segmentkvalifikationer för destinationer.
* **[!UICONTROL Lifetime]**: Filen innehåller aktiva användare som kan ses överallt [!DNL Audience Manager] klientens egenskaper sedan målet skapades.
* **[!UICONTROL Sync Type Lookback Period]**: Om du väljer [!UICONTROL Customer] eller [!UICONTROL Platform]väljer du en tidsperiod. Filerna innehåller aktiva användare för den valda tidsperioden.
Välj sedan ordertyp. Detta anger frekvens och omfattning för varje utgående integrering med partners. Välj mellan stegvis och fullständig beställning.
* **[!UICONTROL Incremental Scheduled Run]**: För varje körning [!DNL Audience Manager] kommer endast att utgående de nya nettoanvändare som är kvalificerade sedan föregående utgående order. Välj önskad tidsperiod [!DNL Audience Manager] för att utföra inkrementella synkroniseringsprocesser. Du kan till exempel välja var 24:e timme, var 7:e dag, var 30:e dag eller aldrig.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>Den första stegvisa ordningen motsvarar en fullständig ordning eftersom inga tidigare användare någonsin skickades till målet.

* **[!UICONTROL Full Sync Scheduled Run]**: För varje körning [!DNL Audience Manager] kommer att utgående alla aktiva användare sedan målet först konfigurerades. Välj önskat schema som du vill ha [!DNL Audience Manager] för att utföra fullständiga synkroniseringsprocesser. Du kan till exempel välja var 24:e timme, var 7:e dag, var 30:e dag eller aldrig.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>Vi rekommenderar att du använder inkrementell synkronisering oftare än med fullständig synkronisering. Inkrementell synkronisering skickar bara filer som innehåller nya trait-implementeringar eller ID-synkroniseringar. Fullständig synkronisering skickar alla filer, oavsett om de innehåller nya implementeringar eller ID-synkroniseringar eller inte. Använd bara [!UICONTROL Full Sync Scheduled Run] konfiguration när klienterna behöver en fullständig kopia av alla sina användare för att minska volymen för utgående data.

## Konfigurera datakällor {#configure-data-sources}

För [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] eller [!UICONTROL Bulk Segment] mål, fyll i fälten nedan. Med de här inställningarna kan du skicka alla data (egenskaper, segment eller ID:n, baserat på vald typ) som är kopplade till datakällorna.

* **[!UICONTROL All Unrestricted First Party Data]**: Välj att använda alla datakällor från första part. Om du väljer det här alternativet visas [!UICONTROL Available Data Sources] alternativ är inaktiverade.
* **[!UICONTROL Available Data Sources]**: Använd pilarna för att flytta datakällor mellan **[!UICONTROL Available Data Sources]** och **[!UICONTROL In File Data Sources]** rutor.

## Spara och slutför {#save-and-finalize}

The **[!UICONTROL Save]** knappen aktiveras när alla obligatoriska fält har fyllts i. Klicka **[!UICONTROL Save]** för att slutföra målprocessen.

## Ta bort företagsdestinationer {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

Så här tar du bort ett mål:

1. Klicka **[!UICONTROL Companies]**, letar upp och klickar på önskat företag och klickar sedan på **[!UICONTROL Destinations]** -fliken.
1. Klicka  ![](assets/icon_delete.png) i **[!UICONTROL Actions]** -kolumnen för det önskade målet.
1. Klicka **[!UICONTROL OK]** för att bekräfta borttagningen.

>[!NOTE]
>
>Du kan inte ta bort ett mål om det har mappade segment.
