---
title: Käyttöomaisuuden ylläpito
description: Käyttöomaisuuserän korjauksista ja huolloista ylläpidetään kunnossapitotietuetta käyttöomaisuuden arvon säilyttämiseksi.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.search.form: 5642, 5625
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: 8427a75127775e1f10576067e4ea122e7f9ad8b3
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8523551"
---
# <a name="maintain-fixed-assets"></a>Käyttöomaisuuden ylläpito
Kunnossapitokulut ovat ajoittaisia rutiinikustannuksia, jotka aiheutuvat käyttöomaisuuden arvon säilyttämisestä. Toisin kuin pääoman kohentaminen, kunnossapito ei lisää arvoa.

Voit tallentaa ajantasaisen tiedoston käyttöomaisuuden kunnossapidosta ja huollosta ja ylläpitää sitä, jotta käyttöomaisuudesta olisi helposti saatavilla täydelliset kunnossapitotiedot. Aina, kun käyttöomaisuus lähetetään huoltoon, tallennetaan kaikki olennaiset tiedot, kuten huoltopäivämäärä, toimittajan numero ja huoltoliikkeen puhelinnumero. Kunnossapitorekisteröinti tallennetaan kunkin käyttöomaisuuserän osalta kyseisestä käyttöomaisuuden kortista.

Indeksointia käytetään muuttamaan arvoja yleisten hintatason muutosten mukaan. **Tee indeksimuutos KO:teen** -eräajoa voidaan käyttää kunnossapitokulujen uudelleenlaskemiseen.

## <a name="to-record-maintenance-work-on-a-fixed-asset"></a>Käyttöomaisuuden kunnossapitotyön tallentaminen
Kunnossapito, kuten huoltokäynti, voidaan tallentaa sen suorittamisen yhteydessä kyseiselle käyttöomaisuudelle **Kunnossapidon rekisteröinti** -sivulla.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus** ja valitse sitten vastaava linkki.  
2. Valitse käyttöomaisuus, jolle haluat tallentaa kunnossapitotyön. Valitse sitten **Kunnossapidon rekisteröinti** -toiminto.
3. Täytä **Kunnossapidon rekisteröinti** -sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-post-maintenance-costs-from-a-fixed-asset-gl-journal"></a>Kunnossapitokustannusten kirjaaminen käyttöomaisuuden KP-päiväkirjasta
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poistokirjaluettelo** ja valitse sitten vastaava linkki.  
2. Valitse poistokirja, joka on liitetty käyttöomaisuuteen, ja valitse sitten **Muokkaa**-toiminto.
3. Varmista, että **Poistokirjakortti**-sivun **Kunnossapito**-valintaruutua ei ole valittu. Näin varmistetaan, että kunnossapitokustannuksia ei kirjata pääkirjanpitoon.
4. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO - KP-päiväkirjat** ja valitse sitten vastaava linkki.  
5. Luo alkuperäisen päiväkirjan rivi ja täytä kentät tarpeen mukaan.
6. Valitse **KO:n kirjaustyyppi** -kentässä **Kunnossapito**.
7. Valitse **Syötä KO-vastatili** -toiminto. Toinen päiväkirjan rivi luodaan vastatilille, joka on määritetty kunnossapidon kirjaamista varten.

    > [!NOTE]  
    >   Vaihe 7 toimii vain, jos seuraavat arvot on määritetty: Käyttöomaisuuden kirjausryhmän **KO:n kirjausryhmän kortti** -sivun **Kunnossapitotili**-kenttä sisältää pääkirjanpidon debet-tilin ja **Kunnossapidon vastatili** -kenttä sisältää sen pääkirjanpitotilin, jolle arvonkorotuksen vastatilitapahtumat kirjataan. Lisätietoja on kohdassa [Käyttöomaisuuden kirjausryhmien määrittäminen](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
8. Valitse **Kirjaa**-toiminto.

## <a name="to-follow-up-on-fixed-assets-service-visits"></a>Käyttöomaisuuden huoltokäyntien seuraaminen
Tulosta **Kunnossapito – Seuraava huolto** -raportti, kun haluat tarkastella käyttöomaisuuseriä, joille on aikataulutettu huoltokäynti. Tätä raporttia voidaan käyttää myös silloin, kun päivitetään käyttöomaisuuskorttien **Seuraava huoltopvm** -kenttää.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kunnossapidon seuraava huolto** ja valitse sitten vastaava linkki.  
2. Täytä **Aloituspvm**- ja **Lopetuspvm**-kenttä.  
3. Valitse **Tulosta**- tai **Esikatsele**-painike.

## <a name="to-monitor-maintenance-costs"></a>Kunnossapitokustannusten valvonta
Kunnossapitokustannuksia voi tarkastella käyttöomaisuuden tilastossa.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus** ja valitse sitten vastaava linkki.
2. Valitse käyttöomaisuus, jonka kunnossapitokustannuksia haluat tarkastella. Valitse sitten **Poistokirjat**-toiminto.
3. Valitse **KO:n poistokirjat** -sivulla kyseinen käyttöomaisuuden poistokirja ja valitse sitten **Tilasto**-toiminto.
4. Valitse **Käyttöomaisuustilastot**-sivulla **Kunnossapito**-kenttä.

Avautuvalla **Kunnossapitotapahtumat**-sivulla näkyvät ne tapahtumat, joista summa muodostuu **Kunnossapito**-kentässä.

## <a name="to-view-or-print-maintenance-costs-for-multiple-fixed-assets"></a>Useiden käyttöomaisuuserien kunnossapitokustannusten tarkasteleminen tai tulostaminen
**Kunnossapito – Analyysi** -raportissa voidaan valita, halutaanko kunnossapitokustannukset nähdä yhdeltä, kahdelta vai kolmelta kunnossapitokoodilta tietyn päivämäärän tai jakson osalta. Voit myös tarkastella kaikkien valittujen käyttöomaisuuserien kokonaissummaa vai tietyn omaisuuserän kokonaissummaa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kunnossapitoanalyysi** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät.
3. Valitse **Tulosta**- tai **Esikatsele**-painike.

## <a name="to-view-maintenance-ledger-entries"></a>Kunnossapitotapahtumien katsominen
Voit tutkia kunnossapitokustannuksia myös tarkastelemalla kunnossapitotapahtumia.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus** ja valitse sitten vastaava linkki.
2. Valitse käyttöomaisuus, jonka tapahtumia haluat tarkastella. Valitse sitten **Poistokirjat**-toiminto.
3. Valitse **KO:n poistokirjat** -sivulla kyseinen käyttöomaisuuden poistokirja ja valitse sitten **Kunnossapitotapahtumat**-toiminto.

## <a name="to-view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a>Useiden käyttöomaisuuserien kunnossapitotapahtumien tarkasteleminen tai tulostaminen
**Kunnossapito - Erittely** -raportin avulla voit tarkastella ja tulostaa yhden tai usean käyttöomaisuuserän kunnossapitotapahtumia.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kunnossapitotiedot** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät.
3. Valitse **Tulosta**- tai **Esikatsele**-painike.

## <a name="see-also"></a>Katso myös
[Käyttöomaisuus](fa-manage.md)  
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Rahoitus](finance.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]