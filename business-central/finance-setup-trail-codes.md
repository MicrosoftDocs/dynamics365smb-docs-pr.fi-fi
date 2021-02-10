---
title: Kirjausketjujen määrittäminen | Microsoft Docs
description: Lue lisää kirjausketjujen seurantaan käytettävien lähdekoodien ja syykoodien määrittämisestä.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fc491b060d6a4b1039376b0051ef58da104ff1d1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750353"
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a>Kirjausketjujen lähdekoodien ja syykoodien määrittäminen

Kaikille kirjatuille tapahtumille määritetään automaattisesti lähdekoodi niin, että tapahtumien alkuperä voidaan jäljittää. Jos haluat antaa tapahtumille lisälähdekoodin, voit käyttää syykoodeja. Syykoodien avulla ilmaistaan, miksi tapahtuma on luotu. Syykoodit voidaan määrittää luomisen yhteydessä koko päiväkirjan malliin ja erään sekä yksittäisiin päiväkirjan riveihin ja asiakirjoihin.  

Käytä koodeja, jotka on helppo muistaa ja jotka ovat kuvaavia, käyttämällä sekä lähdekoodeja että syykoodeja. Koodin tulee olla yksilöivä, ja voit määrittää niin monta koodia kuin haluat.

## <a name="define-source-codes"></a>Lähdekoodien määrittely

Joskus haluat saada selville, miten tietty tapahtuma on syntynyt: esimerkiksi onko tapahtuma syntynyt yleisen päiväkirjan kirjauksen vai ostolaskun kirjauksen tuloksena. Lähdekoodi ilmaisee, missä tapahtuma on syntynyt. Tapahtumia syntyy, kun päiväkirja tai lasku kirjataan ja kun tietyt eräajot suoritetaan. Jokaisella kirjaustyypillä on oma lähdekoodinsa, joka liitetään, kun yksittäinen tapahtuma luodaan.  

Päiväkirjojen, tilausten, laskujen ja hyvityslaskujen kirjaaminen, sekä eräajojen suorittaminen luovat tapahtumia taloudellisiin raportteihin. **Lähdekoodiasetukset**-sivulla on useita pikavälilehtiä, yksi kutakin sovellusaluetta varten. Jokaisessa pikavälilehdessä on asianomaisen sovellusalueen lähdekoodit.

Kun kirjaat tai suoritat eräajon, ohjelma liittää tapahtumaan automaattisesti oikean lähdekoodin. Kun esimerkiksi kirjaat yleisestä päiväkirjasta, ohjelma antaa tapahtumalle koodin *YLEINENPVK*. Tämän jälkeen voit suodattaa **Pääkirjanpidon tapahtumat** -sivun näyttämään, mitkä tapahtumat on kirjattu yleisestä päivä kirjasta tai myynti asiakirjoista, esimerkiksi

### <a name="to-define-source-codes"></a>Lähdekoodien määrittely

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, anna **Lähdekoodin määrittely** ja valitse sitten aiheeseen liittyvä linkki.  

2. Määritä **lähdekoodin määrittely** -ikkunassa kunkin kirjaustyypin ja eräajon osalta asianmukainen lähdekoodi.  

Kentän sisältöä voi muuttaa myöhemmin, ja muutos vaikuttaa tuleviin kirjauksiin.

## <a name="change-source-codes"></a>Lähdekoodien muuttaminen

Haluat ehkä muuttaa lähdekoodia. Saatat haluta muuttaa lähdekoodin *YLEINENPVK* koodiksi *YLEINEN*.

### <a name="to-change-source-codes"></a>Lähdekoodien muuttaminen

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, anna **Lähdekoodit** ja valitse sitten aiheeseen liittyvä linkki.

2. Valitse sillä rivillä, jolla muutettava koodi on, koodi **Koodi**-kentästä.

3. Syötä uusi koodi ja napsauta sitten **Kyllä**. Voit myös muuttaa **Kuvaus**-kentän sisältöä.

Kaikilla uusilla kirjauksilla, jotka jatkossa kirjataan yleisestä päiväkirjasta, tulee olemaan tämä uusi lähdekoodi.

## <a name="define-reason-codes"></a>Syykoodien määrittäminen

Syykoodit täydentävät lähdekoodeja, ja niiden avulla ilmaistaan, miksi tapahtuma luotiin. Voit määritellä syykoodeja yksittäisissä merkinnöissä ja voit liittää pysyvät koodit tiettyihin päiväkirjan malleihin ja päiväkirjan eriin. Kun syykoodi on linkitetty päiväkirjan riviin tai myyntien tai ostojen otsikkoon, ohjelma merkitsee kaikkiin tapahtumiin syykoodin kirjatessaan tapahtumat.  

### <a name="to-set-up-reason-codes"></a>Syykoodien määrittäminen

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, anna **Syykoodit** ja valitse sitten aiheeseen liittyvä linkki.

2. Anna **Syykoodit**-ikkunan **Koodi**-kenttään ensimmäinen koodi. Syötä **Kuvaus**-kenttään selittävä teksti.

Toista nämä vaiheet kaikkien niiden koodien osalta, joita haluat käyttää. Voit määrittää niin monta koodia kuin haluat.

Seuraavassa kuvataan, miten syykoodi lisätään päiväkirjan malliin, mutta vastaavat vaiheet koskevat syykoodin lisäämistä päiväkirjan riville tai päiväkirjan erään.  

### <a name="to-assign-reason-codes-to-journal-templates"></a>Syykoodien määrittäminen päiväkirjan malleissa

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, anna **Yleinen päiväkirjamalli** ja valitse sitten aiheeseen liittyvä linkki.

2. Määritä haluamasi koodi valitsemasi päiväkirjan mallin sisältävän rivin **Syykoodi**-kenttään.

3. Sulje päiväkirjan malli.

Valittu syykoodi kopioituu niihin uusiin päiväkirjan eriin, jotka on luotu tämän päiväkirjan mallin avulla. Syykoodeja liitetään päiväkirjan malleihin samalla tavalla muilla sovellusalueilla.

### <a name="to-use-reason-codes-on-sales-and-purchase-documents"></a>Syykoodien käyttäminen myynti- ja ostoasiakirjoissa

1. Avaa asianomainen myynti- tai ostoasiakirja.

2. Kirjoita koodi myynti- tai osto-otsikon **Syykoodi**-kenttään.

Kun lasku on kirjattu, syykoodi kopioituu kaikkiin KP-, asiakas- ja toimittajatapahtumiin. Et voi liittää erilaisia syykoodeja yksittäisille osto- ja myyntiriveille, koska kaikki rivit kirjataan yhtenä tapahtumana.

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Rahoitus](finance.md)  
[Pankkitilien täsmäytys](bank-manage-bank-accounts.md)  
[Dimensioiden käyttäminen](finance-dimensions.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Yrityksen kassavirran analysoiminen](finance-analyze-cash-flow.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
