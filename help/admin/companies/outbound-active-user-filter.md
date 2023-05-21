---
description: Följ dessa anvisningar för att generera en fullständig synkroniseringsfil som endast innehåller nyligen aktiva användare. Du kanske vill filtrera så att aktiva användare kan skicka relevanta data till ett målsystem på plats eller begränsa storleken på de filer som skickas till en DSP. Du kan inte använda det här filtret med inkrementell synkronisering.
seo-description: Follow these instructions to generate a full synchronization file that includes recently active users only. You may want to filter for active users to push relevant data to an on-site targeting system or to limit the size of the files sent to a DSP. You cannot use this filter with incremental synchronization.
seo-title: Filter Outbound Data by Active Users Only
title: Filtrera utgående data endast efter aktiva användare
uuid: a2b4a385-eee3-458c-b978-09509cacb397
exl-id: d501cfd1-64dd-448e-92c5-180c0081d3e5
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 7%

---

# Filtrera utgående data endast efter aktiva användare {#filter-outbound-data-by-active-users-only}

Följ dessa anvisningar för att generera en fullständig synkroniseringsfil som endast innehåller nyligen aktiva användare. Du kanske vill filtrera så att aktiva användare kan skicka relevanta data till ett målsystem på plats eller begränsa storleken på de filer som skickas till en DSP. Du kan inte använda det här filtret med inkrementell synkronisering.

>[!NOTE]
>
>En besökare behöver inte ses på en viss kundwebbplats eller i annonstrafiken för att kvalificera sig som&quot;aktiv&quot;. De kan ses av alla [!DNL Audience Manager] kund eller partner för att kvalificera sig som&quot;aktiv&quot;.

Så här filtrerar du endast efter aktiva användare:

1. Klicka på **[!UICONTROL Companies]**.
1. Välj företaget som du vill arbeta med och klicka på **[!UICONTROL Destinations]**.
1. I [!UICONTROL Batch Data] anger du följande alternativ:

   * **[!UICONTROL Sync Type]**: Välj **[!UICONTROL Customer]** eller **[!UICONTROL Platform]**.
   * **[!UICONTROL Sync Type Lookback Period]**: Det här tidsintervallet definierar datafilens intervall. Du kan välja bland annat **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]**.
   * **[!UICONTROL Incremental Sync Scheduled Run]**: Välj **[!UICONTROL Never]**. Kom ihåg att det här filtret endast gäller fullständiga synkroniseringsfiler.
   * **[!UICONTROL Full Sync Scheduled Run]**: Detta avgör hur ofta du vill få filen. Du kan välja bland annat **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]**, eller **[!UICONTROL Never]** (för att inaktivera).

1. Klicka på **[!UICONTROL Save]**.
