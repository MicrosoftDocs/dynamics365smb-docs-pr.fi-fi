---
title: "Kirjanpidon käyttöomaisuuden määrittäminen| Microsoft Docs"
description: "Ennen kuin voit käyttää käyttöomaisuutta, sinun tulee määrittää oletusarvoiset KP-tilit, kirjausryhmät, kohdistusavaimet, päiväkirjamallit ja -erät, sekä luokkakoodit."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 29/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 97ff0418c2e3ffe2ace8412bb889fafd5788510b
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-general-fixed-assets-information"></a>Käyttöomaisuuden yleisten tietojen määrittäminen
Ennen kuin voit hallita käyttöomaisuuseriä, sinun on määritettävä oletusarvoiset KP-tilit, kohdistustunnukset, päiväkirjamallit ja -erät käyttöomaisuuden kirjaamista ja uudelleenluokittelua varten. Voit luokitella käyttöomaisuuserät luokkiin, kuten aineellisiin ja aineettomiin.

## <a name="to-set-up-general-default-values-for-fixed-assets"></a>Yleisten oletusarvojen määrittäminen käyttöomaisuudelle
Voit määrittää yleisen toiminnan tai käyttöomaisuuserien toiminnallisuuden ja määrittää asiakirjanumerosarjat **Käyttöomaisuuden asetukset** -ikkunassa.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Käyttöomaisuuden asetukset** ja valitse sitten aiheeseen liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-fixed-asset-posting-groups"></a>Käyttöomaisuuden kirjausryhmien määrittäminen
Kirjausryhmiä käytetään määrittelemään käyttöomaisuusryhmiä. Näiden kirjausryhmien tapahtumat kirjataan samoille KP-tileille.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KO:n kirjausryhmät** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Uusi**-toiminto.
3. Täytä **KO:n kirjausryhmän kortti** -ikkunassa tarvittavat kentät.

    > [!NOTE]  
>   Varmista, että eri käyttöomaisuuserien kirjausten vastatilit lisätään automaattisesti, kun päiväkirjarivien **Syötä KO-vastatil** -toiminto valitaan, tee seuraavan vaiheen osoittamat toiminnot arvonkorotuksen kirjaamisen perusteella.
4. Valitse **Vastatili**-pikavälilehden **Arvonkorotuksen vastatili** -kenttään se pääkirjanpitotili, jolle haluat kirjata arvonkorotuksen vastatilitapahtumat.

Lisätietoja **Syötä KO-vastatili** -toiminnon käyttämisestä käyttöomaisuuden KP-päiväkirjariveillä on esimerkiksi kohdassa [Käyttöomaisuuden uudelleenarvostus](fa-how-revalue.md).

## <a name="to-set-up-fixed-asset-allocation-keys"></a>Käyttöomaisuuden kohdistustunnusten määrittäminen
Transaktioita voidaan kohdistaa useille osastoille tai projekteille käyttäjäkohtaisten kohdistusavainten mukaisesti. Voit määrittää esimerkiksi kohdistusavaimen kohdistamaan autojen poistokustannuksia 35 %:lla hallinto-osastolle ja 65 %:lla myyntiosastolle. Lisätietoja on kohdassa [Kustannusten ja tulojen kohdistaminen](year-allocate-costs-income.md).

Kohdistusavaimet koskevat käyttöomaisuusluokkia yksittäisten omaisuuserien sijaan.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KO:n kirjausryhmät** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **KO:n kirjausryhmät** -ikkunassa **Kohdistukset**-toiminto ja valitse sitten kirjaustyyppi.
3. Täytä **KO:n kohdistukset** -ikkunassa tarvittavat kentät.
4. Toista vaihe 2 ja 3 kunkin kirjaustyypin osalta, jolle haluat määritellä kohdistusavaimia.

## <a name="to-set-up-fixed-asset-journal-templates"></a>Käyttöomaisuuden päiväkirjamallien määrittäminen
Malli on päiväkirjan ennalta määritelty asettelu. Mallissa on tietoja jäljityskoodeista, raporteista ja numerosarjoista. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).

[!INCLUDE[d365fin](includes/d365fin_md.md)] luo automaattisesti käyttöomaisuuden päiväkirjamallin, kun avaat **Käyttöomaisuuspäiväkirja**-ikkunan ensimmäisen kerran. Voit kuitenkin määrittää lisää päiväkirjamalleja.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KO:n päiväkirjan mallit** ja valitse sitten aiheeseen liittyvä linkki.  
2. Täytä tarvittavat kentät.

## <a name="to-set-up-fixed-asset-journal-batches"></a>Käyttöomaisuuden päiväkirjaerien määrittäminen
Voit määrittää useita päiväkirjan eriä eli yksittäisiä päiväkirjoja kullekin päiväkirjan mallille. Käyttäjällä voi esimerkiksi olla oma päiväkirjan erä, jossa käytetään työntekijän nimikirjaimia päiväkirjan erän nimenä. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KO:n päiväkirjan mallit** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse asiaankuuluva päiväkirjamalli ja valitse sitten **Erät**-toiminto.
3. Täytä **KO-päiväkirjan erät** -ikkunassa tarvittavat kentät.

## <a name="to-set-up-fixed-asset-reclassification-journal-templates"></a>Käyttöomaisuuden uudelleenluokituspäiväkirjamallien määrittäminen
Kyseisiä uudelleenluokituspäiväkirjoja voidaan käyttää käyttöomaisuuserien siirtämisessä, jakamisessa ja yhdistämisessä. [!INCLUDE[d365fin](includes/d365fin_md.md)] luo automaattisesti käyttöomaisuuden uudelleenluokituspäiväkirjan mallin, kun avaat **KO:n uudelleenluokituspvk** -ikkunan ensimmäisen kerran. Voit kuitenkin määrittää lisää uudelleenluokituspäiväkirjan malleja. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KO:n uud.luok.pvk:n mallit** ja valitse sitten aiheeseen liittyvä linkki.  
2. Täytä tarvittavat kentät.

## <a name="to-set-up-fixed-asset-reclassification-journal-batches"></a>Käyttöomaisuuden uudelleenluokituspäiväkirjaerien määrittäminen
Voit määrittää useita päiväkirjan eriä eli yksittäisiä päiväkirjoja kullekin uudelleenluokituspäiväkirjan mallille. Käyttäjällä voi esimerkiksi olla oma uudelleenluokituspäiväkirjan erä, jossa käytetään työntekijän nimikirjaimia uudelleenluokituspäiväkirjan erän nimenä. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KO:n uud.luok.pvk:n mallit** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse asiaankuuluva päiväkirjamalli ja valitse sitten **Erät**-toiminto.
3. Täytä **KO:n uud.luok.pvk:n erät** -ikkunassa tarvittavat kentät.

## <a name="to-set-up-fixed-asset-class-codes"></a>Käyttöomaisuuden luokkakoodien määrittäminen
Käyttöomaisuuden luokkakoodeja voidaan käyttää käyttöomaisuuserien, esimerkiksi aineellisten ja aineettomien hyödykkeiden, ryhmittelyyn.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KO-luokat** ja valitse sitten aiheeseen liittyvä linkki.
2. Syötä koodit ja nimet niiden luokkien osalta, jotka haluat luoda.

## <a name="to-set-up-fixed-asset-subclass-codes"></a>Käyttöomaisuuden alaluokkakoodien määrittäminen
Käyttöomaisuuden alaluokkakoodia voi käyttää ryhmittelemään käyttöomaisuus luokkiin, esimerkiksi rakennuksiin, ajoneuvoihin, huonekaluihin ja koneisiin.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KO:n alaluokat** ja valitse sitten aiheeseen liittyvä linkki.
2. Syötä koodit ja nimet niiden luokkien osalta, jotka haluat luoda.

## <a name="to-set-up-fixed-asset-location-codes"></a>Käyttöomaisuuden sijaintikoodien määrittäminen
KO-sijaintikoodia voidaan käyttää rekisteröimään käyttöomaisuuden sijainti, esimerkiksi myyntiosasto, vastaanotto, hallinto, tuotanto tai fyysinen varasto. Nämä tiedot ovat tarpeen vakuutusta ja inventointia varten.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KO-sijainnit** ja valitse sitten aiheeseen liittyvä linkki.
2. Syötä koodit ja nimet niiden käyttöomaisuuden sijaintien osalta, jotka haluat luoda.

## <a name="to-register-opening-entries"></a>Avaustapahtumien rekisteröiminen
Jos käytät käyttöomaisuutta ensimmäistä kertaa [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, pääkirjanpidon kohdistusalue on määritettävä ennen käyttöomaisuuden määrittämistä. Se, miten tämä tehdään, riippuu siitä, onko käyttöomaisuus on integroitu pääkirjanpidon kanssa.  

 Seuraavaa menetelmää käytetään, jos käyttöomaisuustransaktioita tulee kirjata pääkirjanpitoon.  

1. Varmista, että olet saanut valmiiksi Käyttöomaisuuden asetusten perustoimenpiteet.  
2. Luo jokaiselle olemassa olevalle omaisuuserälle käyttöomaisuuskortti.  
3. Luo kullekin poistotarkoitukselle (kuten veroilmoituksille ja taloudellisille raporteille) käyttöominaisuuden poistokirja. Kunkin poistokirjan osalta tulee määritellä ehdot, kuten integrointi pääkirjanpitoon.  

    Ota käyttöön pääkirjanpidon integrointi seuraavien vaiheiden avulla. Varmista ensimmäiseksi, että pääkirjanpidon integrointi on poistettu käytöstä kaikissa poistokirjoissa, kirjaa sitten avaustapahtumat ja ota sitten pääkirjanpidon integrointi käyttöön.  
4. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Poistokirjat** ja valitse sitten aiheeseen liittyvä linkki.  
5. Valitse asianmukainen poistokirja. Valitse **Kotisivu**-välilehden **Hallinta**-ryhmässä **Muokkaa luetteloa**, jolloin **Poistokirjan kortti** -ikkuna avautuu.
6. Varmista, että **Integrointi**-pikavälilehden kaikki kentät ovat tyhjiä (poista kaikki valintamerkit). Jos poistokirjoja on monta, poista kunkin poistokirjan pääkirjanpidon integrointi käytöstä.  
7. Anna käyttöomaisuuden päiväkirjassa seuraavat rivit kullekin käyttöomaisuudelle:
   * Syötä rivi ja hankintameno.
   * Rivi, jolla on kumulatiivinen poisto edellisen tilikauden loppuun.
   * Rivi, jolla on kumulatiivinen poisto nykyisen tilivuoden alusta päivään, jonka [!INCLUDE[d365fin](includes/d365fin_md.md)] määrittää poiston laskennan aloituskohdaksi.

    Jos avaussaldoja on muita, myös ne voidaan syöttää (esimerkiksi arvonalennukset ja arvonkorotukset).  
8. Kun olet syöttänyt ja kirjannut kunkin omaisuuserän päiväkirjarivit, ota pääkirjanpidon integrointi käyttöön poistokirjoissa.

Jos käyttöomaisuutta ei ole integroitu käyttöomaisuuden kanssa, ohita työvaiheet 6 ja 8.

## <a name="see-also"></a>Katso myös
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Käyttöomaisuus](fa-manage.md)  
[Rahoitus](finance.md)  
[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin!](index.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

