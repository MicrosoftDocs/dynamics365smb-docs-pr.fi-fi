---
title: Yleisten KO-tietojen määrittäminen
description: 'Ennen kuin voit käyttää käyttöomaisuutta, sinun tulee määrittää oletusarvoiset KP-tilit, kirjausryhmät, kohdistusavaimet, päiväkirjamallit ja -erät, sekä luokkakoodit.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5623, 5615, 5661, 5662, 5627, 5616, 5620, 5629, 5633, 5609, 5631, 5630, 5617, 5612, 5613, 5608, 5609, 5635, 9277'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-general-fixed-assets-information" />Käyttöomaisuuden yleisten tietojen määrittäminen

Ennen kuin voit hallita käyttöomaisuuseriä, sinun on määritettävä oletusarvoiset KP-tilit, kohdistustunnukset, päiväkirjamallit ja -erät käyttöomaisuuden kirjaamista ja uudelleenluokittelua varten. Voit luokitella käyttöomaisuuserät luokkiin, kuten aineellisiin ja aineettomiin.

## <a name="to-set-up-general-default-values-for-fixed-assets" />Yleisten oletusarvojen määrittäminen käyttöomaisuudelle

Voit määrittää yleisen toiminnan tai käyttöomaisuuserien toiminnallisuuden ja määrittää asiakirjanumerosarjat **Käyttöomaisuuden asetukset** -sivulla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuuden asetukset** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-fixed-asset-posting-groups" />Käyttöomaisuuden kirjausryhmien määrittäminen

Kirjausryhmiä käytetään määrittelemään käyttöomaisuusryhmiä. Näiden kirjausryhmien tapahtumat kirjataan samoille KP-tileille.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n kirjausryhmät** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.
3. Täytä **KO:n kirjausryhmän kortti** -sivulla tarvittavat kentät.

    > [!NOTE]  
    >   Varmista, että eri käyttöomaisuuserien kirjausten vastatilit lisätään automaattisesti, kun päiväkirjarivien **Syötä KO-vastatil** -toiminto valitaan, tee seuraavan vaiheen osoittamat toiminnot arvonkorotuksen kirjaamisen perusteella.
4. Valitse **Vastatili**-pikavälilehden **Arvonkorotuksen vastatili** -kenttään se pääkirjanpitotili, jolle haluat kirjata arvonkorotuksen vastatilitapahtumat.

Lisätietoja **Syötä KO-vastatili** -toiminnon käyttämisestä käyttöomaisuuden KP-päiväkirjariveillä on esimerkiksi kohdassa [Käyttöomaisuuden uudelleenarvostus](fa-how-revalue.md).

## <a name="to-set-up-fixed-asset-allocation-keys" />Käyttöomaisuuden kohdistustunnusten määrittäminen

Transaktioita voidaan kohdistaa useille osastoille tai projekteille käyttäjäkohtaisten kohdistusavainten mukaisesti. Voit määrittää esimerkiksi kohdistusavaimen kohdistamaan autojen poistokustannuksia 35 %:lla hallinto-osastolle ja 65 %:lla myyntiosastolle. Lisätietoja on kohdassa [Kustannusten ja tulojen kohdistaminen](year-allocate-costs-income.md).

Kohdistusavaimet koskevat käyttöomaisuusluokkia yksittäisten omaisuuserien sijaan.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n kirjausryhmät** ja valitse sitten vastaava linkki.  
2. Valitse **KO:n kirjausryhmät** -sivulla **Kohdistukset**-toiminto ja valitse sitten kirjaustyyppi.
3. Täytä **KO:n kohdistukset** -sivulla tarvittavat kentät.
4. Toista vaihe 2 ja 3 kunkin kirjaustyypin osalta, jolle haluat määritellä kohdistusavaimia.

## <a name="to-set-up-fixed-asset-journal-templates" />Käyttöomaisuuden päiväkirjamallien määrittäminen

Malli on päiväkirjan ennalta määritelty asettelu. Mallissa on tietoja jäljityskoodeista, raporteista ja numerosarjoista. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).

[!INCLUDE[prod_short](includes/prod_short.md)] luo automaattisesti käyttöomaisuuden päiväkirjamallin, kun avaat **Käyttöomaisuuspäiväkirja**-sivun ensimmäisen kerran. Voit kuitenkin määrittää lisää päiväkirjamalleja.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n päiväkirjan mallit** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät.

## <a name="to-set-up-fixed-asset-journal-batches" />Käyttöomaisuuden päiväkirjaerien määrittäminen

Voit määrittää useita päiväkirjan eriä eli yksittäisiä päiväkirjoja kullekin päiväkirjan mallille. Käyttäjällä voi esimerkiksi olla oma päiväkirjan erä, jossa käytetään työntekijän nimikirjaimia päiväkirjan erän nimenä. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n päiväkirjan mallit** ja valitse sitten liittyvä linkki.  
2. Valitse asiaankuuluva päiväkirjamalli ja valitse sitten **Erät**-toiminto.
3. Täytä **KO-päiväkirjan erät** -sivulla tarvittavat kentät.

## <a name="to-set-up-fixed-asset-reclassification-journal-templates" />Käyttöomaisuuden uudelleenluokituspäiväkirjamallien määrittäminen

Kyseisiä uudelleenluokituspäiväkirjoja voidaan käyttää käyttöomaisuuserien siirtämisessä, jakamisessa ja yhdistämisessä. [!INCLUDE[prod_short](includes/prod_short.md)] luo automaattisesti käyttöomaisuuden uudelleenluokituspäiväkirjan mallin, kun avaat **KO:n uudelleenluokituspvk** -sivun ensimmäisen kerran. Voit kuitenkin määrittää lisää uudelleenluokituspäiväkirjan malleja. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n uud.luok.pvk:n mallit** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät.

## <a name="to-set-up-fixed-asset-reclassification-journal-batches" />Käyttöomaisuuden uudelleenluokituspäiväkirjaerien määrittäminen

Voit määrittää useita päiväkirjan eriä eli yksittäisiä päiväkirjoja kullekin uudelleenluokituspäiväkirjan mallille. Käyttäjällä voi esimerkiksi olla oma uudelleenluokituspäiväkirjan erä, jossa käytetään työntekijän nimikirjaimia uudelleenluokituspäiväkirjan erän nimenä. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n uud.luok.pvk:n mallit** ja valitse sitten liittyvä linkki.  
2. Valitse asiaankuuluva päiväkirjamalli ja valitse sitten **Erät**-toiminto.
3. Täytä **KO:n uud.luok.pvk:n erät** -sivulla tarvittavat kentät.

## <a name="to-set-up-fixed-asset-class-codes" />Käyttöomaisuuden luokkakoodien määrittäminen

Käyttöomaisuuden luokkakoodeja voidaan käyttää käyttöomaisuuserien, esimerkiksi aineellisten ja aineettomien hyödykkeiden, ryhmittelyyn.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n luokat** ja valitse sitten vastaava linkki.
2. Syötä koodit ja nimet niiden luokkien osalta, jotka haluat luoda.

## <a name="to-set-up-fixed-asset-subclass-codes" />Käyttöomaisuuden alaluokkakoodien määrittäminen

Käyttöomaisuuden alaluokkakoodia voi käyttää ryhmittelemään käyttöomaisuus luokkiin, esimerkiksi rakennuksiin, ajoneuvoihin, huonekaluihin ja koneisiin.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n alaluokat** ja valitse sitten vastaava linkki.
2. Syötä koodit ja nimet niiden luokkien osalta, jotka haluat luoda.

## <a name="to-set-up-fixed-asset-location-codes" />Käyttöomaisuuden sijaintikoodien määrittäminen

KO-sijaintikoodia voidaan käyttää rekisteröimään käyttöomaisuuden sijainti, esimerkiksi myyntiosasto, vastaanotto, hallinto, tuotanto tai fyysinen varasto. Nämä tiedot ovat tarpeen vakuutusta ja inventointia varten.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n sijainnit** ja valitse sitten vastaava linkki.
2. Syötä koodit ja nimet niiden käyttöomaisuuden sijaintien osalta, jotka haluat luoda.

## <a name="to-register-opening-entries" />Avaustapahtumien rekisteröiminen

Jos käytät käyttöomaisuutta ensimmäistä kertaa [!INCLUDE[prod_short](includes/prod_short.md)]issa, pääkirjanpidon kohdistusalue on määritettävä ennen käyttöomaisuuden määrittämistä. Se, miten tämä tehdään, riippuu siitä, onko käyttöomaisuus on integroitu pääkirjanpidon kanssa.  

 Seuraavaa menetelmää käytetään, jos käyttöomaisuustransaktioita tulee kirjata pääkirjanpitoon.  

1. Varmista, että olet saanut valmiiksi Käyttöomaisuuden asetusten perustoimenpiteet.  
2. Luo jokaiselle olemassa olevalle omaisuuserälle käyttöomaisuuskortti.  
3. Luo kullekin poistotarkoitukselle (kuten veroilmoituksille ja taloudellisille raporteille) käyttöominaisuuden poistokirja. Kunkin poistokirjan osalta tulee määritellä ehdot, kuten integrointi pääkirjanpitoon.  

    Ota käyttöön pääkirjanpidon integrointi seuraavien vaiheiden avulla. Varmista ensimmäiseksi, että pääkirjanpidon integrointi on poistettu käytöstä kaikissa poistokirjoissa, kirjaa sitten avaustapahtumat ja ota sitten pääkirjanpidon integrointi käyttöön.  
4. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poistokirjat** ja valitse sitten vastaava linkki.  
5. Valitse poistokirja ja valitse **Muokkaa**-toiminto avataksesi **Poistokirjakortti**-sivun.
6. Varmista, että **Integrointi**-pikavälilehden kaikki kentät ovat tyhjiä (poista kaikki valintamerkit). Jos poistokirjoja on monta, poista kunkin poistokirjan pääkirjanpidon integrointi käytöstä.  
7. Anna käyttöomaisuuden päiväkirjassa seuraavat rivit kullekin käyttöomaisuudelle:
   * Syötä rivi ja hankintameno.
   * Rivi, jolla on kumulatiivinen poisto edellisen tilikauden loppuun.
   * Rivi, jolla on kumulatiivinen poisto nykyisen tilivuoden alusta päivään, jonka [!INCLUDE[prod_short](includes/prod_short.md)] määrittää poiston laskennan aloituskohdaksi.

    Jos avaussaldoja on muita, myös ne voidaan syöttää (esimerkiksi arvonalennukset ja arvonkorotukset).  
8. Kun olet syöttänyt ja kirjannut kunkin omaisuuserän päiväkirjarivit, ota pääkirjanpidon integrointi käyttöön poistokirjoissa.

Jos käyttöomaisuutta ei ole integroitu käyttöomaisuuden kanssa, ohita työvaiheet 6 ja 8.

## <a name="see-related-microsoft-trainingtrainingpathsset-up-fixed-assets-management" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/paths/set-up-fixed-assets-management/)

## <a name="see-also" />Katso myös

[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Käyttöomaisuus](fa-manage.md)  
[Rahoitus](finance.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
