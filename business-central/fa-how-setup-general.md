---
title: Käyttöomaisuuden yleisten tietojen määrittäminen
description: 'Ennen kuin voit käyttää käyttöomaisuutta, sinun tulee määrittää oletusarvoiset KP-tilit, kirjausryhmät, kohdistusavaimet, päiväkirjamallit ja -erät, sekä luokkakoodit.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.form: '5623, 5615, 5661, 5662, 5627, 5616, 5620, 5629, 5633, 5609, 5631, 5630, 5617, 5612, 5613, 5608, 5609, 5635, 9277'
ms.date: 03/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="set-up-general-fixed-assets-information"></a>Käyttöomaisuuden yleisten tietojen määrittäminen

Ennen kuin käyttöomaisuutta voidaan hallita, oletusarvoiset KP-tilit, kohdistusavaimet sekä päiväkirjamallit ja -erät on määritettävä kirjaamaan käyttöomaisuus ja uudelleenluokittelemaan se. Lisäksi on määritettävä luokitteluhierarkia (luokat ja aliluokat) jäsentämään resurssit. Tarvittaessa on määritettävä myös sijainnit, jossa resurssit varastoidaan.

## <a name="to-set-up-general-behavior-for-fixed-assets-functionality"></a>Käyttöomaisuustoiminnan yleisen toiminnan määrittäminen

Käyttöomaisuustoiminnon ja sen asiakirjanumerosarjan yleinen toiminto voidaan määrittää **Käyttöomaisuuden asetukset** -sivulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuuden asetukset** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-fixed-asset-posting-groups"></a>Käyttöomaisuuden kirjausryhmien määrittäminen

Kirjausryhmiä käytetään määrittelemään käyttöomaisuusryhmiä. Näiden kirjausryhmien tapahtumat kirjataan samoille KP-tileille.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n kirjausryhmät** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.
3. Täytä **KO:n kirjausryhmän kortti** -sivulla tarvittavat kentät.

    > [!NOTE]  
    >   Varmista, että eri käyttöomaisuuserien kirjausten vastatilit lisätään automaattisesti, kun päiväkirjarivien **Syötä KO-vastatil** -toiminto valitaan, tee seuraavan vaiheen osoittamat toiminnot arvonkorotuksen kirjaamisen perusteella.
4. Valitse **Vastatili**-pikavälilehden **Arvonkorotuksen vastatili** -kenttään se pääkirjanpitotili, jolle haluat kirjata arvonkorotuksen vastatilitapahtumat.

Lisätietoja **Syötä KO-vastatili** -toiminnon käyttämisestä käyttöomaisuuden KP-päiväkirjariveillä on kohdassa [Käyttöomaisuuden uudelleenarvostus](fa-how-revalue.md).

## <a name="to-set-up-fixed-asset-journal-templates"></a>Käyttöomaisuuden päiväkirjamallien määrittäminen

Malli on päiväkirjan ennalta määritelty asettelu. Mallissa on tietoja jäljityskoodeista, raporteista ja numerosarjoista. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).

[!INCLUDE[prod_short](includes/prod_short.md)] luo automaattisesti käyttöomaisuuden päiväkirjamallin, kun **Käyttöomaisuuspäiväkirja**-sivu avataan ensimmäisen kerran. Myös muita päiväkirjamalleja voidaan määrittää.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n päiväkirjan mallit** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät.

## <a name="to-set-up-fixed-asset-class-and-subclass-codes"></a>Käyttöomaisuuden luokka- ja alaluokkakoodien määrittäminen

Käyttöomaisuudessa voidaan määrittää luokitteluhierarkia, jota voidaan käyttää resurssien ryhmittelyyn. Hierarkiassa on kaksi tasoa: luokat ja alaluokat.

### <a name="fixed-asset-class-codes"></a>Käyttöomaisuuden luokkakoodit

Käyttöomaisuusluokat ovat ylätason tapahtumia resurssien ryhmittelyyn käytetyssä luokitteluhierarkiassa. Luokkien avulla voidaan esimerkiksi jakaa resurssit aineellisiin ja aineettomiin resursseihin. Määrityksissä on luotava ainakin yksi käyttöomaisuusluokka.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n luokat** ja valitse sitten vastaava linkki.
2. Syötä niiden käyttöomaisuusluokkien koodit ja nimet, jotka halutaan luoda.

### <a name="fixed-asset-subclass-codes"></a>Käyttöomaisuuden alaluokkakoodit

Käyttöomaisuuden alaluokat ovat toisen tason tapahtumia resurssien ryhmittelyyn käytetyssä luokitteluhierarkiassa. Kukin aliluokkaa osoittaa ylätason luokkaan. Käyttöomaisuuden alaluokkakoodia voi käyttää käyttöomaisuuden ryhmittelyyn tarkennettuihin luokkiin, kuten rakennuksiin, ajoneuvoihin, huonekaluihin ja koneisiin. Määrityksissä on luotava ainakin yksi käyttöomaisuuden alaluokka.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n alaluokat** ja valitse sitten vastaava linkki.
2. Syötä niiden käyttöomaisuuden alaluokkien koodit nimet, jotka halutaan luoda.

## <a name="start-to-register-assets"></a>Resurssien rekisteröinnin aloittaminen

Jos käyttöomaisuutta käytetään ensimmäistä kertaa [!INCLUDE[prod_short](includes/prod_short.md)]issa, pääkirjanpidon sovellusalue on määritettävä ennen käyttöomaisuuden määrittämistä. Käytännössä tämä määräytyy sen mukaan, integroidaanko käyttöomaisuus pääkirjanpitoon.  

Seuraavaa menetelmää käytetään, jos käyttöomaisuustransaktioita tulee kirjata pääkirjanpitoon.  

1. Tee käyttöomaisuuden perusmääritykset.  
2. Täytä kunkin aiemmin luodun resurssin käyttöomaisuuskortti.  
3. Luo kullekin poistotarkoitukselle (kuten veroilmoituksille ja taloudellisille raporteille) käyttöominaisuuden poistokirja. Kunkin poistokirjan osalta määritetään ehdot, kuten integrointi pääkirjanpitoon.

    Ota käyttöön pääkirjanpidon integrointi seuraavien vaiheiden avulla. Varmista ensimmäiseksi, että pääkirjanpidon integrointia ei ole otettu käyttöön kaikissa poistokirjoissa, kirjaa sitten avaustapahtumat ja ota lopuksi pääkirjanpidon integrointi käyttöön.  
4. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poistokirjat** ja valitse sitten vastaava linkki.  
5. Valitse poistokirja ja valitse **Muokkaa**-toiminto avataksesi **Poistokirjakortti**-sivun.
6. Siirrä kaikki vaihtopainikkeet **Integrointi**-pikavälilehdessä käytöstäpoistoasentoon. Jos poistokirjoja on useita, toista tämä vaihe kunkin osalta.  
7. Anna käyttöomaisuuden päiväkirjassa seuraavat rivit kullekin käyttöomaisuudelle:
   * Syötä rivi ja hankintameno.
   * Rivi, jolla on kumulatiivinen poisto edellisen tilikauden loppuun.
   * Rivi, jolla on kumulatiivinen poisto nykyisen tilivuoden alusta päivään, jonka [!INCLUDE[prod_short](includes/prod_short.md)] määrittää poiston laskennan aloituskohdaksi.

    Jos avaussaldoja on muita, myös ne voidaan syöttää (esimerkiksi arvonalennukset ja arvonkorotukset).  
8. Kun kunkin omaisuuserän päiväkirjarivit on syötetty ja kirjattu, ota pääkirjanpidon integrointi käyttöön poistokirjoissa.

Jos käyttöomaisuutta ei ole integroitu pääkirjanpitoon, ohita vaiheet kuusi ja kahdeksan.

## <a name="to-set-up-fixed-asset-location-codes-optional"></a>Käyttöomaisuuden sijaintikoodien määrittäminen (valinnainen)

Käyttöomaisuuden sijaintikoodit määrittävät resurssien sijainnin ilmaisemiseen käytettävät tunnisteet. Sijainti voi olla esimerkiksi myyntiosasto, vastaanotto, hallinto, tuotanto tai fyysinen varasto. Käyttöominaisuuden sijainti voidaan rekisteröidä niiden avulla. Nämä tiedot ovat tarpeen vakuutusta ja inventointia varten.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n sijainnit** ja valitse sitten vastaava linkki.
2. Syötä koodit ja nimet niiden käyttöomaisuuden sijaintien osalta, jotka haluat luoda.

## <a name="to-set-up-fixed-asset-allocation-keys-optional"></a>Käyttöomaisuuden kohdistustunnusten määrittäminen (valinnainen)

Kohdistustunnusten avulla voidaan kohdistaa tapahtumat eri osastoille tai projekteille. Kohdistustunnus voidaan esimerkiksi määrittää kohdistamaan ajoneuvojen poistokustannuksista 35 prosenttia hallinto-osastolle ja 65 prosenttia myyntiosastolle. Lisätietoja on kohdassa [Kustannusten ja tulojen kohdistaminen](year-allocate-costs-income.md).

Kohdistusavaimet koskevat käyttöomaisuusluokkia yksittäisten omaisuuserien sijaan.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n kirjausryhmät** ja valitse sitten vastaava linkki.  
2. Valitse **KO:n kirjausryhmät** -sivulla **Kohdistukset**-toiminto ja valitse sitten kirjaustyyppi.
3. Täytä **KO:n kohdistukset** -sivulla tarvittavat kentät.
4. Toista vaihe 2 ja 3 kunkin kirjaustyypin osalta, jolle haluat määritellä kohdistusavaimia.

## <a name="to-set-up-fixed-asset-journal-batches-optional"></a>Käyttöomaisuuden päiväkirjaerien määrittäminen (valinnainen)

Voit määrittää useita päiväkirjan eriä eli yksittäisiä päiväkirjoja kullekin päiväkirjan mallille. Käyttäjällä voi esimerkiksi olla oma päiväkirjan erä, jossa käytetään työntekijän nimikirjaimia päiväkirjan erän nimenä. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n päiväkirjan mallit** ja valitse sitten liittyvä linkki.  
2. Valitse asiaankuuluva päiväkirjamalli ja valitse sitten **Erät**-toiminto.
3. Täytä **KO-päiväkirjan erät** -sivulla tarvittavat kentät.

## <a name="to-set-up-fixed-asset-reclassification-journal-templates-optional"></a>Käyttöomaisuuden uudelleenluokituspäiväkirjamallien määrittäminen (valinnainen)

Erillisiä uudelleenluokituspäiväkirjoja voidaan käyttää käyttöomaisuuden siirtämiseen, jakamiseen ja yhdistämiseen. [!INCLUDE[prod_short](includes/prod_short.md)] luo automaattisesti käyttöomaisuuden uudelleenluokituspäiväkirjan mallin, kun **KO:n uudelleenluokituspvk** -sivu avataan ensimmäisen kerran. Myös muita uudelleenluokituspäiväkirjan malleja voidaan määrittää. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n uud.luok.pvk:n mallit** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät.

## <a name="to-set-up-fixed-asset-reclassification-journal-batches-optional"></a>Käyttöomaisuuden uudelleenluokituspäiväkirjaerien määrittäminen (valinnainen)

Voit määrittää useita päiväkirjan eriä eli yksittäisiä päiväkirjoja kullekin uudelleenluokituspäiväkirjan mallille. Käyttäjällä voi esimerkiksi olla oma uudelleenluokituspäiväkirjan erä, jossa käytetään työntekijän nimikirjaimia uudelleenluokituspäiväkirjan erän nimenä. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n uud.luok.pvk:n mallit** ja valitse sitten liittyvä linkki.  
2. Valitse asiaankuuluva päiväkirjamalli ja valitse sitten **Erät**-toiminto.
3. Täytä **KO:n uud.luok.pvk:n erät** -sivulla tarvittavat kentät.

## <a name="see-also"></a>Katso myös

[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Käyttöomaisuuden yleiskatsaus](fa-manage.md)  
[Taloushallinto](finance.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
