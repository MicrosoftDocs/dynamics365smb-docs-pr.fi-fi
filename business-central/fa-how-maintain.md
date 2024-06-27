---
title: Käyttöomaisuuden ylläpitäminen
description: Tallenna käyttöomaisuuden korjaukset ja huolto arvon säilyttämiseksi.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'repair, service'
ms.search.form: '5642, 5625'
ms.date: 05/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="maintain-fixed-assets"></a>Käyttöomaisuuden ylläpitäminen

Kunnossapitokustannukset ovat toimintakuluja asioille, joita tehdään käyttöomaisuuden ehdon säilyttämiseksi. Toisin kuin pääoman kohentaminen, kunnossapito ei lisää käyttöomaisuuserien arvoa.

Aina, kun käyttöomaisuus lähetetään huoltoon, tallennetaan kaikki olennaiset tiedot, kuten huoltopäivämäärä, työn suorittaneen toimittajan numero ja huoltoliikkeen puhelinnumero. Kunnossapitotietoja syötetään useammalle sivulle:

* Käyttöomaisuuden kortti
* Ostotilaus
* Ostolasku
* Käyttöom. KP-päiväkirja

Indeksointia käytetään muuttamaan arvoja yleisten hintatason muutosten mukaan. Käytä **Tee indeksimuutos KO:teen** -eräajoa kunnossapitokulujen uudelleenlaskemiseen.

## <a name="record-a-maintenance-cost-directly-on-a-fixed-asset"></a>Kirjaa ylläpitokustannukset suoraan käyttöomaisuuteen

Aina kun omaisuudelle tehdään huoltoa, kuten huoltokäynti, voit tallentaa sen **Kunnossapidon rekisteröinnit** -sivulle.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus** ja valitse sitten vastaava linkki.  
2. Valitse käyttöomaisuus, jolle haluat tallentaa kunnossapitotyön. Valitse sitten **Kunnossapidon rekisteröinti** -toiminto.
3. Täytä **Kunnossapidon rekisteröinti** -sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="post-maintenance-costs-from-a-fixed-asset-gl-journal"></a>Kunnossapitokustannusten kirjaaminen käyttöomaisuuden KP-päiväkirjasta

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poistokirjaluettelo** ja valitse sitten vastaava linkki.  
2. Valitse poistokirja, joka on liitetty käyttöomaisuuteen, ja valitse sitten **Muokkaa**-toiminto.
3. Varmista **Poistokirjan kortti** -sivulla, että **Kunnossapito**-valintaruutua ei ole valittu, jotta kunnossapitokustannuksia ei kirjata pääkirjanpitoon.
4. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO - KP-päiväkirjat** ja valitse sitten vastaava linkki.  
5. Luo alkuperäisen päiväkirjan rivi ja täytä kentät tarpeen mukaan.
6. Valitse **KO:n kirjaustyyppi** -kentässä **Kunnossapito**.
7. Valitse **Syötä KO-vastatili** -toiminto. Toinen päiväkirjan rivi luodaan vastatilille, joka on määritetty kunnossapidon kirjaamista varten.

    > [!NOTE]  
    > Vaihe 7 toimii vain, jos seuraavat arvot on määritetty: Käyttöomaisuuden kirjausryhmän **KO:n kirjausryhmän kortti** -sivun **Kunnossapitotili**-kenttä sisältää pääkirjanpidon debet-tilin ja **Kunnossapidon vastatili** -kenttä sisältää sen pääkirjanpitotilin, jolle arvonkorotuksen vastatilitapahtumat kirjataan. Lisätietoja on kohdassa [Käyttöomaisuuden kirjausryhmien määrittäminen](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
8. Valitse **Kirjaa**-toiminto.

## <a name="record-maintenance-cost-from-a-purchase-invoice"></a>Kunnossapitokustannusten kirjaaminen ostolaskusta

Seuraavassa kuvataan, miten käyttöomaisuuden kunnossapitokustannukset kirjataan ostolaskusta. Ostotilausten vaiheet ovat vastaavanlaiset.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolasku** ja valitse sitten vastaava linkki.
2. Täytä **Yleiset**-pikavälilehdessä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Valitse **Rivit**-pikavälilehden **Tyyppi**-kentässä **Käyttöomaisuus**.
4. Valitse **Nro**-kenttään -kentästä, valitse käyttöomaisuuserä ja määritä määrä ja kustannus.
5. Valitse **KO:n kirjaustyyppi** -kentässä **Kunnossapito**.
6. Kirjaa ostolasku.

## <a name="follow-up-on-service-visits"></a>Huoltokäyntien seuranta

Tulosta **Kunnossapito – Seuraava huolto** -raportti, kun haluat tarkastella käyttöomaisuuseriä, joille on aikataulutettu huolto. Tätä raporttia voidaan käyttää myös silloin, kun haluat päivittää käyttöomaisuuskorttien **Seuraava huoltopvm** -kenttää.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kunnossapidon seuraava huolto** ja valitse sitten vastaava linkki.  
2. Täytä **Aloituspvm**- ja **Lopetuspvm**-kenttä.  
3. Valitse **Tulosta**- tai **Esikatsele**-painike.

## <a name="monitor-maintenance-costs"></a>Kunnossapitokustannusten valvonta

Kunnossapitokustannusten seuraamiseksi voi katsoa tilastoja.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus** ja valitse sitten vastaava linkki.
2. Valitse käyttöomaisuus, jonka kunnossapitokustannuksia haluat tarkastella. Valitse sitten **Poistokirjat**-toiminto.
3. Valitse **KO:n poistokirjat** -sivulla kyseinen käyttöomaisuuden poistokirja ja valitse sitten **Tilasto**-toiminto.
4. Valitse **Käyttöomaisuustilastot**-sivulla **Kunnossapito**-kenttä.

Avautuvalla **Kunnossapitotapahtumat**-sivulla nähdäksesi ne tapahtumat, joista summa muodostuu **Kunnossapito**-kentässä.

## <a name="view-or-print-maintenance-costs-for-multiple-fixed-assets"></a>Useiden käyttöomaisuuserien kunnossapitokustannusten tarkasteleminen tai tulostaminen

**Kunnossapito – Analyysi** -raportissa voidaan valita, halutaanko kunnossapitokustannukset tutkia yhdeltä, kahdelta vai kolmelta kunnossapitokoodilta tietyn päivämäärän tai jakson osalta. Raportti voi näyttää kaikkien valittujen käyttöomaisuuserien kokonaissummaa vai tietyn omaisuuserän kokonaissummaa.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kunnossapitoanalyysi** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät.
3. Valitse **Tulosta**- tai **Esikatsele**-painike.

## <a name="view-maintenance-ledger-entries"></a>Kunnossapitotapahtumien katsominen

Voit tutkia kunnossapitokustannuksia myös tarkastelemalla kunnossapitotapahtumia.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus** ja valitse sitten vastaava linkki.
2. Valitse käyttöomaisuus, jonka tapahtumia haluat tarkastella. Valitse sitten **Poistokirjat**-toiminto.
3. Valitse **KO:n poistokirjat** -sivulla kyseinen käyttöomaisuuden poistokirja ja valitse sitten **Kunnossapitotapahtumat**-toiminto.

## <a name="view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a>Useiden käyttöomaisuuserien kunnossapitotapahtumien tarkasteleminen tai tulostaminen

**Kunnossapito - Erittely** -raportin avulla voit tarkastella ja tulostaa yhden tai usean käyttöomaisuuserän kunnossapitotapahtumia.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kunnossapitotiedot** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät.
3. Valitse **Tulosta**- tai **Esikatsele**-painike.

## <a name="see-also"></a>Katso myös

[Käyttöomaisuus](fa-manage.md)  
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Taloushallinto](finance.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
