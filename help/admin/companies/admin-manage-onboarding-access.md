---
description: För att förhindra att oavsiktliga filer och data introduceras i måldatakällor som ägs av andra partner eller kunder har Audience Manager lagt till ett mappningskrav mellan partner-ID (PID) och de datakällor som ägs av andra partner.
title: Hantera introduktionsåtkomst för data från andra part
exl-id: 03bec978-dd31-41cc-a3aa-d67fbb98963c
source-git-commit: cc04863272005964cfbf1bb2319cc0dd86863680
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Hantera startåtkomst för data från andra leverantörer {#manage-onboarding-access-for-second-party-data}

>[!IMPORTANT]
>
> Målgruppen för den här sidan är anställda i Adobe. Om du är en Audience Manager-kund och begär en mappning av en datakälla från en annan leverantör enligt beskrivningen på den här sidan kontaktar du kundtjänst eller den tekniska kontohanteraren.
> Observera att det inte krävs någon mappning för befintliga datautdelningsrelationer. Mappningen behövs inte heller när du registrerar data i måldatakällor som tillhör ditt PID.

För att förhindra att oavsiktliga filer och data introduceras i måldatakällor som ägs av andra partner har Audience Manager lagt till ett mappningskrav mellan partner-ID (PID) och de datakällor (DPID) som ägs av andra partner. Läs mer om PID och DPID i [index för Audience Manager-ID:n](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html).

Om en Audience Manager partner eller kund vill importera filer till en måldatakälla som de inte äger måste de begära en mappning mellan partner-ID:t (PID) och den specifika datakällan (DPID) för datadelning från andra leverantörer. Om mappningen saknas kommer filerna inte att bearbetas av det inkommande datajobbet och data läggs inte in i Audience Manager.

För att kunna skapa mappningen skickar du en Jira-biljett till Audience Manager ingenjörsteamet. Visa ett exempel på en Jira-biljett [här](https://jira.corp.adobe.com/browse/AAM-60353). Du behöver inte begära att mappningar skapas för befintliga datautdelningsrelationer.
