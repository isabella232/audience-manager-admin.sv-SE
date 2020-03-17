---
description: Det är saker du bör uppmuntra dina kunder att vara medvetna om när de arbetar med Audience Manager API:er.
seo-description: Det är saker du bör uppmuntra dina kunder att vara medvetna om när de arbetar med Audience Manager API:er.
seo-title: Krav och rekommendationer för API
title: Krav och rekommendationer för API
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Krav och rekommendationer för API {#api-requirements-and-recommendations}

Det ni bör uppmuntra era kunder att vara medvetna om när de arbetar med Audience Manager [!DNL API]s.

## Krav {#requirements}

Observera följande när du arbetar med [!DNL Audience Manager][!DNL API] kod:

* **Begäranparametrar:** Alla frågeparametrar är obligatoriska om inte annat anges.
* **[!DNL JSON]innehållstyp:**Ange`content-type: application/json`och **`accept: application/json`i koden.

* **Förfrågningar och svar:** Skicka begäranden som ett korrekt formaterat [!DNL JSON] objekt. [!DNL Audience Manager] svarar med [!DNL JSON] formaterade data. Serversvar kan innehålla begärda data, en statuskod eller båda.

* **Åtkomst:** Din [!DNL Audience Manager] konsult kommer att förse dig med ett klient-ID och en nyckel som gör att du kan göra [!DNL API] förfrågningar.

* **Exempel på dokumentation och kod:** Text i *kursiv stil* representerar en variabel som du anger eller skickar in när du skapar eller tar emot [!DNL API] data. Ersätt *kursiv* text med egen kod, egna parametrar eller annan obligatorisk information.

## Rekommendationer: Skapa en allmän API-användare {#recommendations}

Vi rekommenderar att du skapar ett separat, tekniskt användarkonto för Audience Manager [!DNL API]. Det här är ett generiskt konto som inte är kopplat till eller associerat med en viss användare i din klientorganisation. Med den här typen av [!DNL API] användarkonto kan du uppnå två saker:

* Identifiera vilken tjänst som anropar [!DNL API] (t.ex. samtal från en klientapp som använder våra [!DNL API]funktioner eller från att göra satsförändringar).
* Ge dig tillgång till [!DNL API]dina kunder utan avbrott. Ett konto som är knutet till en viss anställd kan tas bort när de lämnar företaget. Detta förhindrar dina kunder från att arbeta med den tillgängliga [!DNL API] koden. Ett generiskt konto som inte är kopplat till en viss medarbetare hjälper till att undvika det här problemet.

Ett exempel eller ett användningsexempel för den här typen av konto kan vara att kunderna vill ändra många segment samtidigt med [grupphanteringsverktygen](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html). För att göra detta behöver de [!DNL API] åtkomst. I stället för att lägga till behörigheter till en viss användare skapar du ett icke-specifikt, användarkonto som har rätt autentiseringsuppgifter, nyckel och hemlighet för att ringa [!DNL API] [!DNL API] samtal. Detta är också användbart om kunden utvecklar egna program som använder [!DNL Audience Manager] dessa [!DNL API]program.