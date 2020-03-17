---
description: Följ dessa anvisningar för att generera en fullständig synkroniseringsfil som endast innehåller nyligen aktiva användare. Du kanske vill filtrera så att aktiva användare kan skicka relevanta data till ett målsystem på plats eller begränsa storleken på de filer som skickas till en DSP. Du kan inte använda det här filtret med inkrementell synkronisering.
seo-description: Följ dessa anvisningar för att generera en fullständig synkroniseringsfil som endast innehåller nyligen aktiva användare. Du kanske vill filtrera så att aktiva användare kan skicka relevanta data till ett målsystem på plats eller begränsa storleken på de filer som skickas till en DSP. Du kan inte använda det här filtret med inkrementell synkronisering.
seo-title: Filtrera utgående data endast för aktiva användare
title: Filtrera utgående data endast för aktiva användare
uuid: a2b4a385-eee3-458c-b978-09509cacb397
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Filtrera utgående data endast för aktiva användare {#filter-outbound-data-by-active-users-only}

Följ dessa anvisningar för att generera en fullständig synkroniseringsfil som endast innehåller nyligen aktiva användare. Du kanske vill filtrera så att aktiva användare kan skicka relevanta data till ett målsystem på plats eller begränsa storleken på de filer som skickas till en DSP. Du kan inte använda det här filtret med inkrementell synkronisering.

>[!NOTE]
>
>En besökare behöver inte ses på en viss kundwebbplats eller i annonstrafiken för att kvalificera sig som&quot;aktiv&quot;. De kan ses av alla [!DNL Audience Manager] kunder eller partners för att kvalificera sig som&quot;aktiva&quot;.

Så här filtrerar du endast efter aktiva användare:

1. Klicka på **[!UICONTROL Companies]**.
1. Välj företaget som du vill arbeta med och klicka på **[!UICONTROL Destinations]**.
1. Ange följande alternativ i [!UICONTROL Batch Data] avsnittet:

   * **[!UICONTROL Sync Type]**: Markera **[!UICONTROL Customer]** eller **[!UICONTROL Platform]**.
   * **[!UICONTROL Sync Type Lookback Period]**: Det här tidsintervallet definierar datafilens intervall. Du kan välja **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]**.
   * **[!UICONTROL Incremental Sync Scheduled Run]**: Välj **[!UICONTROL Never]**. Kom ihåg att det här filtret endast gäller fullständiga synkroniseringsfiler.
   * **[!UICONTROL Full Sync Scheduled Run]**: Detta avgör hur ofta du vill få filen. Du kan välja mellan **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]** eller **[!UICONTROL Never]** (för att inaktivera).

1. Klicka på **[!UICONTROL Save]**.
