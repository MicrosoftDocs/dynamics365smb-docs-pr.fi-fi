---
title: Ostoasiakirjojen kirjaaminen
description: Lisätietoja ostoasiakirjojen kirjaamisen tavoista ja kirjattujen asiakirjojen päivittämisestä.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.form: ''
ms.date: 08/08/2022
ms.author: edupont
ms.openlocfilehash: 2f306fee236fda2bae4863e0e793239c2168f125
ms.sourcegitcommit: 8b95e1700a9d1e5be16cbfe94fdf7b660f1cd5d7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2022
ms.locfileid: "9461100"
---
# <a name="posting-purchases"></a>Ostojen kirjaaminen

Voit valita ostoasiakirjassa seuraavien kirjaustoimintojen välillä:

* **Kirjaa**
* **Esikatsele kirjausta**
* **Kirjaa ja tulosta**
* **Testiraportti**
* **Kirjaa erä**

Kun ostoasiakirja on kirjattu, toimittajan tili, pääkirjanpito (KP), nimiketapahtumat ja resurssitapahtumat päivitetään.

Jokaiselle ostoasiakirjalle luodaan ostotapahtuma **KP-tapahtuma**-taulukkoon. Myös toimittajan tilille **Toimittajatapahtuma**-taulukkoon luodaan tapahtuma ja lisäksi luodaan KP-tapahtuma asianmukaiselle ostovelkatilille. Lisäksi oston kirjauksen tuloksena saattaa olla arvonlisäverotapahtuman (ALV) ja KP-tapahtuman luonti alennussummalle. Se, kirjataanko alennukselle tapahtuma, määräytyy **Ostojen ja ostovelkojen asetukset** -sivun **Alennuksen kirjaus** -kentän sisällön perusteella.

Kullekin ostoriville luodaan soveltuvin osin tapahtumat:

* **Nimiketapahtuma**-taulukkoon, jos ostorivin tyyppi on **Nimike**.
* **KP-tapahtuma**-taulukkoon, jos ostorivien tyyppi on **KP-tili**.
* **Resurssitapahtuma**-taulukkoon, jos ostorivin tyyppi on **Resurssi**.

Lisäksi ostoasiakirjat tallennetaan aina **Tavaran vastaanoton otsikko**- ja **Ostolaskun otsikko** -taulukoihin.

Ennen kirjausta voit tulostaa testiraportin, jossa on kaikki tiedot ostotilauksesta ja joka osoittaa mahdolliset virheet. Kun haluat tulostaa raportin, valitse **Kirjaus** ja valitse sitten **Testiraportti**.

> [!IMPORTANT]  
> Kun kirjaat ostotilauksen nimikkeille, voit luoda sekä vastaanoton että laskun. Nämä voidaan luoda joko yhtäaikaa tai erikseen. Voit luoda osittaisen vastaanoton ja osittaisen laskutuksen täyttämällä **Vastaanotettava määrä** ja **Laskutettava määrä** -kentät yksittäisillä ostotilausriveillä ennen kirjausta. Huomaa, ettet voi luoda ostolaskua ostotilauksesta sellaisille tuotteille tai palveluille, joita ei ole vastaanotettu. Siispä ennen laskuttamista on täytynyt tallentaa vastaanotto, tai sinun täytyy valita samanaikainen vastaanotto ja laskutus.
>
> Luo asiakirja **Ostolaskut**-sivulla, jos haluat kirjata ostolaskun [!INCLUDE[prod_short](includes/prod_short.md)]-sovelluksessa ilman, että ostovastaanotto kirjataan. Lue lisätietoja kohdasta [Ostojen kirjaaminen ostolaskujen avulla](purchasing-how-record-purchases.md).

Voit kirjata tai kirjata ja tulostaa. Jos valitset kirjaamisen ja tulostamisen, raportti tulostetaan tilauksen kirjaamisen yhteydessä. **Kirjaa erä** -toiminnon kirjataksesi useita tilauksia samanaikaisesti. Lue lisätietoja kohdasta [Useiden asiakirjojen kirjaaminen samanaikaisesti](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Kirjaustapahtuminen katselu

Kun kirjaus on päättynyt, kirjatut ostorivit poistuvat tilauksesta. Viesti kertoo, milloin kirjaus on suoritettu loppuun. Tämän jälkeen voit nähdä kirjatut tapahtumat useissa kirjattuja tapahtumia sisältävissä sivuilla, kuten **Toimittajatapahtumat**, **KP-tapahtumat**, **Nimiketapahtumat**, **Resurssitapahtumat**, **Ostovastaanotot** ja **Kirjatut ostolaskut**.

Useimmissa tapauksissa voit avata tapahtumat kortista tai asiakirjasta, johon ne vaikuttavat. Valitse esimerkiksi **Toimittajakortti**-sivulla **Tapahtumat**-toiminto.

## <a name="editing-ledger-entries"></a>Kirjaustapahtuminen muokkaus

Voit muokata arvoja kirjattujen ostoasiakirjojen tietyissä kentissä, kuten **Maksuviite**-kentässä. Lisätietoja on kohdassa [Kirjattujen asiakirjojen muokkaaminen](across-edit-posted-document.md). Jos sinulla on enemmän kriittisiä kenttiä, jotka vaikuttavat jäljitysketjuun, sinun täytyy peruuttaa tai kumota kirjaus. Lue lisätietoja kohdasta [Päiväkirjakirjauksen peruuttaminen sekä vastaanottojen tai toimitusten kumoaminen](finance-how-reverse-journal-posting.md).

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/receive-invoice-dynamics-d365-business-central/index).

## <a name="see-also"></a>Katso myös

[Kirjattujen asiakirjojen muokkaaminen](across-edit-posted-document.md)  
[Useiden asiakirjojen kirjaaminen samanaikaisesti](ui-batch-posting.md)  
[Osto](purchasing-manage-purchasing.md)  
[Asiakirjojen ja päiväkirjojen kirjaaminen](ui-post-documents-journals.md)  
[Maksamattomien ostolaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla](ui-search.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
