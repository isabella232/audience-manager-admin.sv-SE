---
description: Det är saker du bör uppmuntra dina kunder att vara medvetna om när de arbetar med Audience Manager API:er.
seo-description: Things you should encourage your clients to be aware of when they're working with the Audience Manager APIs.
seo-title: API Requirements and Recommendations
title: Krav och rekommendationer för API
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
exl-id: 24f90732-31a6-436d-862b-e6871d279c7a
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 2%

---

# Krav och rekommendationer för API {#api-requirements-and-recommendations}

Saker du bör uppmuntra dina kunder att vara medvetna om när de arbetar med Audience Manager [!DNL API]s.

## Krav {#requirements}

Observera följande när du arbetar med [!DNL Audience Manager] [!DNL API] kod:

* **Begäranparametrar:** Alla frågeparametrar är obligatoriska om inte annat anges.
* **[!DNL JSON]innehållstyp:** Ange `content-type: application/json` *och* `accept: application/json` i koden.

* **Förfrågningar och svar:** Skicka begäranden som korrekt formaterade [!DNL JSON] -objekt. [!DNL Audience Manager] svarar med [!DNL JSON] formaterade data. Serversvar kan innehålla begärda data, en statuskod eller båda.

* **Åtkomst:** Dina [!DNL Audience Manager] konsulten ger dig ett klient-ID och en nyckel som gör att du kan [!DNL API] förfrågningar.

* **Exempel på dokumentation och kod:** Text in *kursiv* representerar en variabel som du anger eller skickar in när du skapar eller tar emot [!DNL API] data. Ersätt *kursiv* text med egen kod, egna parametrar eller annan obligatorisk information.

## Recommendations: Skapa en allmän API-användare {#recommendations}

Vi rekommenderar att du skapar ett separat, tekniskt användarkonto för Audience Manager [!DNL API]s. Det här är ett generiskt konto som inte är kopplat till eller associerat med en viss användare i din klientorganisation. Den här typen av [!DNL API] Med användarkontot kan du uppnå två saker:

* Identifiera vilken tjänst som anropar [!DNL API] (t.ex. samtal från en klientapp som använder vår [!DNL API]s eller från att göra större ändringar).
* Oavbruten åtkomst till [!DNL API]s. Ett konto som är knutet till en viss anställd kan tas bort när de lämnar företaget. Detta förhindrar dina kunder från att arbeta med tillgängliga [!DNL API] kod. Ett generiskt konto som inte är kopplat till en viss medarbetare hjälper till att undvika det här problemet.

Ett exempel eller ett användningsexempel för den här typen av konto kan vara att våra kunder vill ändra många segment samtidigt med [Masshanteringsverktyg](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/bulk-management-tools/bulk-management-intro.html?lang=en). För att göra detta behöver de [!DNL API] åtkomst. I stället för att lägga till behörigheter till en viss användare skapar du en icke-specifik, [!DNL API] användarkonto som har rätt autentiseringsuppgifter, nyckel och hemlighet att skapa [!DNL API] samtal. Detta är också användbart om klientens program utvecklar egna program som använder [!DNL Audience Manager] [!DNL API]s.
