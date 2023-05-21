---
description: Som standard synkroniserar alla företag data med Adobe Media Optimizer (AMO). I administratörsgränssnittet har varje företagsbehållare en datakälla som hanterar den här processen. Datakällan är Adobe AMO (ID 411). Klicka på en behållarrad (under fliken Behållare) för ett valt företag för att inaktivera den här standardsynkroniseringen eller för att lägga till och ta bort andra datakällor i AMO-synkroniseringsprocessen.
seo-description: By default, all companies sync data with Adobe Media Optimizer (AMO). In the Admin UI, each company container has a data source that manages this process. This data source is Adobe AMO (ID 411). Click a container row (under the Containers tab) for a selected company to disable this default sync or to add and remove other data sources to the AMO sync process.
seo-title: ID Syncing with Media Optimizer
title: ID-synkronisering med Media Optimizer
uuid: b741dfa7-2947-4288-b214-79eccf18d53a
exl-id: ebd978ef-3825-4a96-94bd-5cdae269cf7c
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 5%

---

# ID-synkronisering med Media Optimizer {#id-syncing-with-media-optimizer}

Som standard synkroniserar alla företag data med [!DNL Adobe Media Optimizer] ([!DNL AMO]). I [!UICONTROL Admin UI]har varje företagsbehållare en datakälla som hanterar den här processen. Den här datakällan är [!UICONTROL Adobe AMO] ([!UICONTROL ID] 411). Klicka på en behållarrad (under [!UICONTROL Containers] för ett valt företag att inaktivera den här standardsynkroniseringen eller att lägga till och ta bort andra datakällor i [!DNL AMO] synkroniseringsprocess.

![](assets/id-sync.png)

## Synkroniseringsstatus för ID {#id-sync-status}

I följande tabell beskrivs synkroniseringsstatusen för en datakälla.

| Status | Beskrivning |
|------ | -------- |
| Av | Ta bort alla datakällor från [!UICONTROL Selected Data Sources] för den här behållaren att inaktivera ID-synkronisering med [!DNL AMO] |
| På (oavsett ID-tjänstversion) | En datakälla synkroniseras med [!DNL AMO] oavsett ID-tjänstversion när: <ul><li>Datakällan visas i [!UICONTROL Selected Data Sources] lista.</li><li>The [!DNL AMO] kryssruta *är inte* markerat.</li></ul> |
| På (oavsett ID-tjänstversion) | En datakälla synkroniseras med [!DNL AMO] med ID-tjänstversion 2.0 (eller senare) när: <ul><li>Datakällan visas i [!UICONTROL Selected Data Sources] lista.</li><li>The [!DNL AMO] kryssruta *är* markerat.</li></ul> |

>[!MORELIKETHIS]
>
>* [Hantera behållare](../companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967)

