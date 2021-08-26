---
description: Alternativen för Device Graph är tillgängliga för företag som deltar i Adobe Experience Cloud Device Co-op. Om en kund också har ett avtalsförhållande med en tredjepartsleverantör av enhetsdiagram som är integrerad med Audience Manager, visas alternativ för det enhetsdiagrammet i det här avsnittet. De här alternativen finns i Företag > Företagsnamn > Profil > Alternativ för enhetsdiagram.
seo-description: The Device Graph Options are available to companies that participate in the Adobe Experience Cloud Device Co-op. If a customer also has a contractual relationship with a third-party device graph provider that is integrated with Audience Manager, this section will show options for that device graph. These options are located in Companies > company name > Profile > Device Graph Options.
seo-title: Device Graph Options for Companies
title: Alternativ för enhetsdiagram för företag
uuid: a8ced843-710c-4a8f-a0d7-ea89d010a7a5
exl-id: 2502f3d2-b43c-410c-acb6-03c2a2ba2c1d
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 3%

---

# Alternativ för enhetsdiagram för företag {#device-graph-options-for-companies}

[!UICONTROL Device Graph Options] är tillgängligt för företag som deltar i [!DNL Adobe Experience Cloud Device Co-op]. Om en kund också har ett avtalsförhållande med en tredjepartsleverantör av enhetsdiagram som är integrerad med Audience Manager, visas alternativ för det enhetsdiagrammet i det här avsnittet. Dessa alternativ finns i [!UICONTROL Companies] > företagsnamn > [!UICONTROL Profile] > [!UICONTROL Device Graph Options].

![](assets/adminUIdataSource.png)

I den här illustrationen används generiska namn för alternativ för enhetsdiagram från tredje part. I produktionen kommer dessa namn från enhetens diagramleverantör och kan variera från vad som visas här. Alternativen [!DNL LiveRamp] är vanligtvis (men inte alltid):

* Börja med [!DNL LiveRamp]
* Innehåller ett mellannamn som varierar
* Sluta med [!UICONTROL - Household] eller [!UICONTROL -Person]

## Alternativ för enhetsdiagram definierade {#device-graph-options-defined}

Alternativen för enhetsdiagram som du väljer här visar eller döljer de [!UICONTROL Device Options]-alternativ som är tillgängliga för en [!DNL Audience Manager]-kund när de skapar en [!UICONTROL Profile Merge Rule].

### Co-op Device Graph {#co-op-graph}

Kunder som deltar i [Adobe Experience Cloud Device Co-op](https://experienceleague.adobe.com/docs/device-co-op/using/about/overview.html?lang=en) använder dessa alternativ för att skapa en [!UICONTROL Profile Merge Rule] med [deterministiska och sannolika data](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=en). [!DNL Corporate Provisioning Team] aktiverar och inaktiverar det här alternativet via ett [!DNL API]-anrop. Du kan inte markera eller rensa de här rutorna i [!DNL Admin UI]. Alternativen **[!UICONTROL Co-op Device Graph]** och **[!UICONTROL Company Device Graph]** utesluter varandra. Kunder kan be oss att aktivera den ena eller den andra, men inte båda. När det här alternativet är markerat visas kontrollen **[!UICONTROL Co-op Device Graph]** i [!UICONTROL Device Options]-inställningarna för en [!UICONTROL Profile Merge Rule].

![](assets/adminUI1.png)

### Företagsenhetsdiagram {#company-graph}

Det här alternativet är till för [!DNL Analytics]-kunder som använder måttet [!UICONTROL People] i sin [!DNL Analytics]-rapportserie. [!DNL Corporate Provisioning Team] aktiverar och inaktiverar det här alternativet via ett [!DNL API]-anrop. Du kan inte markera eller rensa de här rutorna i [!DNL Admin UI]. Alternativen **[!UICONTROL Company Device Graph]** och **[!UICONTROL Co-op Device Graph]** utesluter varandra. Kunder kan be oss att aktivera den ena eller den andra, men inte båda. Vid markering:

* Enhetsdiagrammet använder deterministiska data som tillhör det företag du konfigurerar (inga sannolikhetsdata).
* [!DNL Audience Manager] skapar automatiskt ett  [!UICONTROL Data Source] namn `*` som kallas `*-Company Device Graph-Person`partnernamn. På informationssidan för [!UICONTROL Data Source] kan [!DNL Audience Manager]-kunder ändra partnernamn, beskrivning och använda [dataexportkontroller](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=en) på den här datakällan.
* [!DNL Audience Manager] kunder  *inte* ser någon ny inställning i  [!UICONTROL Device Options] avsnittet för en  [!UICONTROL Profile Merge Rule].

### LiveRamp Device Graph (Person eller Household) {#liveramp-device-graph}

Dessa kryssrutor aktiveras i [!DNL Admin UI] när en partner skapar en [!UICONTROL Data Source] och väljer **[!UICONTROL Use as an Authenticated Profile]** och/eller **[!UICONTROL Use as a Device Graph]**. Namnen på de här inställningarna bestäms av tredjepartsprovidern för enhetsdiagram (t.ex. [!DNL LiveRamp], [!DNL TapAd] osv.). När det här alternativet är markerat kommer det företag du konfigurerar att använda data från dessa enhetsdiagram.

![](assets/adminUI2.png)

>[!MORELIKETHIS]
>
>* [Beskrivning av alternativen för regler för profilsammanslagning](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/merge-rule-definitions.html?lang=en)
>* [Inställningar för datakälla och menyalternativ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html?lang=en)

