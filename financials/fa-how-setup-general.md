---
title: "Kirjanpidon käyttöomaisuuden määrittäminen| Microsoft Docs"
description: "Ennen kuin voit käyttää käyttöomaisuutta, sinun tulee määrittää oletusarvoiset KP-tilit, kirjausryhmät, kohdistusavaimet, päiväkirjamallit ja -erät, sekä luokkakoodit."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 4a41abe08412b357207cbbc08e8dc5041b12d942
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-set-up-general-fixed-assets-information"></a>Toimintaohje: Käyttöomaisuuden yleisten tietojen määrittäminen
Ennen kuin voit hallita käyttöomaisuuseriä, sinun on määritettävä oletusarvoiset KP-tilit, kohdistustunnukset, päiväkirjamallit ja -erät käyttöomaisuuden kirjaamista ja uudelleenluokittelua varten. Voit luokitella käyttöomaisuuserät luokkiin, kuten aineellisiin ja aineettomiin.

## <a name="to-set-up-general-default-values-for-fixed-assets"></a>Yleisten oletusarvojen määrittäminen käyttöomaisuudelle
Voit määrittää yleisen toiminnan tai käyttöomaisuuserien toiminnallisuuden ja määrittää asiakirjanumerosarjat **Käyttöomaisuuden asetukset** -ikkunassa.

1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Käyttöomaisuuden asetukset** ja valitse sitten aiheeseen liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-fixed-asset-posting-groups"></a>Käyttöomaisuuden kirjausryhmien määrittäminen
Kirjausryhmiä käytetään määrittelemään käyttöomaisuusryhmiä. Näiden kirjausryhmien tapahtumat kirjataan samoille KP-tileille.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KO:n kirjausryhmät** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Uusi**-toiminto.
3. Täytä **KO:n kirjausryhmän kortti** -ikkunassa tarvittavat kentät.

    > [!NOTE]  
>   Varmista, että eri käyttöomaisuuserien kirjausten vastatilit lisätään automaattisesti, kun päiväkirjarivien **Syötä KO-vastatil** -toiminto valitaan, tee seuraavan vaiheen osoittamat toiminnot arvonkorotuksen kirjaamisen perusteella.
4. Valitse **Vastatili**-pikavälilehden **Arvonkorotuksen vastatili** -kenttään se pääkirjanpitotili, jolle haluat kirjata arvonkorotuksen vastatilitapahtumat.

Lisätietoja **Syötä KO-vastatili** -toiminnon käyttämisestä käyttöomaisuuden KP-päiväkirjariveillä on esimerkiksi kohdassa [Toimintaohje: Käyttöomaisuuden uudelleenarvostus](fa-how-revalue.md).

## <a name="to-set-up-fixed-asset-allocation-keys"></a>Käyttöomaisuuden kohdistustunnusten määrittäminen
Transaktioita voidaan kohdistaa useille osastoille tai projekteille käyttäjäkohtaisten kohdistusavainten mukaisesti. Voit määrittää esimerkiksi kohdistusavaimen kohdistamaan autojen poistokustannuksia 35 %:lla hallinto-osastolle ja 65 %:lla myyntiosastolle. Lisätietoja on kohdassa [Toimintaohje: Kustannusten ja tulojen kohdistaminen](year-allocate-costs-income.md).

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
3. Käyttöomaisuuden poistokirjojen määrittäminen.  
4. Ota käyttöön pääkirjanpidon integrointi seuraavien vaiheiden avulla.
5. Syötä **Etsi**-ruudussa **Poistokirjat** ja valitse sitten vastaava linkki.  
6. Valitse asianmukainen poistokirja. Valitse **Kotisivu**-välilehden **Hallinta**-ryhmässä **Muokkaa luetteloa**, jolloin **Poistokirjan kortti** -ikkuna avautuu.
7. Varmista, että **Integrointi**-pikavälilehden kaikki kentät ovat tyhjiä (poista kaikki valintamerkit). Jos poistokirjoja on useita, ota jokaisessa käyttöön pääkirjanpidon integrointi.  
8. Anna käyttöomaisuuden päiväkirjassa seuraavat rivit kutakin käyttöomaisuutta varten:
   * Syötä rivi ja hankintameno.
   * Rivi, jolla on kumulatiivinen poisto edellisen tilikauden loppuun.
   * Rivi, jolla on kumulatiivinen poisto nykyisen tilivuoden alusta päivään, jonka [!INCLUDE[d365fin](includes/d365fin_md.md)] määrittää poiston laskennan aloituskohdaksi.

Jos avaussaldoja on muita, myös ne voidaan syöttää (esimerkiksi arvonalennukset ja \-korotukset).  

Jos käyttöomaisuutta ei ole integroitu käyttöomaisuuden kanssa, ohita työvaiheet 4–7.

## <a name="see-also"></a>Katso myös
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Käyttöomaisuus](fa-manage.md)  
[Rahoitus](finance.md)  
[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin!](index.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

