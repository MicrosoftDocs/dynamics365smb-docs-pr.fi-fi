---
title: Raporttien määrittäminen tulostumaan tiettyihin tulostimiin | Microsoft Docs
description: Tutustu, miten tulostin määritetään raportille ja miten Tulostimen valinnat -sivua käytetään.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 59e3efb3800b309203c77f566bf909f92d7e0882
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390628"
---
# <a name="set-up-printers"></a>Tulostimien määrittäminen
Koska [!INCLUDE[prod_short](includes/prod_short.md)] on pilvipalvelu, se ei voi käyttää paikallisia tulostimia, jotka on yhdistetty käyttäjien koneisiin. Se voi kuitenkin muodostaa yhteyden pilvipalveluun yhteensopiviin tulostimiin. Sovelluksen [!INCLUDE[prod_short](includes/prod_short.md)] yleisessä versiossa pilvitulostin nimeltä **Sähköpostitulostin** asennetaan laajennuksena. Se on käyttövalmis alkuasetusten jälkeen.

Jos pilvitulostinta ei ole asennettu ja määritetty tai jos asennettu tulostin ei toimi kunnolla, tulostuksessa käytetään selaimen tulostusasetusten oletustulostinta. Tämä osoitetaan tällä arvolla **Tulostin**-kentässä raportin pyyntösivulla: *(ei mitään, selain käsittelee)*.

**Tulostimen hallinta** -sivulla näkyvät määritetyt tulostimet. Kun olet määrittänyt vähintään yhden tulostimen, voit avata **Tulostinvalinnat**-sivun ja määrittää käyttäjätilillä, mitä raportteja milläkin tulostimella tulostetaan.

Kun tulostin on määritetty ja liitetty tiettyihin raportteihin, voit tulostaa raportin valitsemalla raporttipyyntösivulla **Tulosta**-painikkeen. Lisätietoja on kohdassa [Raportin tulostaminen](ui-work-report.md#PrintReport).

### <a name="sizing-print-jobs"></a>Tulostustöiden mitoitus
Pilvitulostus on suunniteltu kohtuullisen kokoisia asiakirjoja varten. Useimmissa pilvipalveluissa, kuten PrintNode- ja HP ePrint -palveluissa, on enintään 10 megatavua työtä kohti. Jos haluat tulostaa suurempia raportteja, ne täytyy ehkä jakaa useisiin tulosteisiin.

## <a name="to-set-up-a-printer"></a>Tulostimen määrittäminen
**Tulostimen hallinta** -sivulla ovat näkyvissä määritetyt tulostimet. Voit käyttää kunkin tulostimen **Asetukset**-sivua ja muokata olemassa olevaa asetusta tai määrittää uuden tulostimen.

Seuraavassa kerrotaan, miten olemassa oleva **Sähköpostitulostin**-tulostin määritetään. Tämä on esiasennettu laajennus.

> [!NOTE]
> Sähköpostitoiminto on määritettävä sähköpostitulostusta varten. Lisätietoja on kohdassa [Sähköpostin määrittäminen](admin-how-setup-email.md).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tulostimen hallinta** ja valitse sitten liittyvä linkki.
2. Valitse **Sähköpostitulostin**-tulostimen rivi ja valitse sitten **Muokkaa tulostimen asetuksia** -toiminto.
3. Täytä **Asetukset**-sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Tulostimelle on valittava manuaalisesti sopiva paperikoko, koska paikallista tulostinta tai käyttäjän asetuksia ei voi tallentaa.
    >
    > Huomaa, että sähköpostitulostinlaajennuksen oletusasetuksena on **A4**-paperikoko. Tämä ei ole sopiva esimerkiksi Pohjois-Amerikkaa varten.
4. Voit määrittää tulostimesta oletustulostimen valitsemalla **Tulostimen hallinta** -sivulla **Määritä oletustulostimeksi** -kohdan.

### <a name="privacy-notice"></a>Tietosuojatiedot
Jos käytät sähköpostitulostinlaajennusta, kaikki tai jotkin tulostustyöt lähetetään tulostimen määrittämisen yhteydessä annettuun sähköpostiosoitteeseen. On suositeltavaa yhdistää yksilöllinen sähköpostitunnus tulostinlaitteeseen käyttämällä vain virallisia laitevalmistajan tarjoamia palveluita. Valmistaja voi olla esimerkiksi HP ePrint, KonicaMinolta EveryonePrint tai Epson Email Print.

Noudata varovaisuutta tietoturva-asioissa. Varmista esimerkiksi, että sähköpostitulostusratkaisun käyttöoikeudet, tietosuoja-asetukset ja tietojen säilyttämistä koskevat käytännöt on määritetty oikein. Vastuullasi on antaa oikea, varmistettu ja toimiva sähköpostiosoite. Lisätietoja on kohdassa [Microsoftin tietosuojatiedot](https://privacy.microsoft.com/en-us/privacystatement).

## <a name="to-select-which-printers-print-which-reports"></a>Tulostinten ja niiden tulostamien raporttien valitseminen

**Tulostinvalinnat**-sivulla voit määrittää käyttäjätilin ja kunkin tulostimen tulostamat raportit. Tämä on hyödyllistä, jos käytössä on raportteja, jotka vaativat eri tulostimien käyttämisen yrityksen sijoittelusta tai niiden tulostusominaisuuksista johtuen.

> [!IMPORTANT]
> [!INCLUDE[prod_short](includes/prod_short.md)]:n paikallista käyttöä varten **Tulostinvalinnat** -sivua voi käyttää vain tulostimen laajennusten määrittelemien tulostimien osalta. Sitä ei voi käyttää paikallisissa tulostimissa.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tulostinvalinnat** ja valitse sitten liittyvä linkki. Vaihtoehtoisesti voit valita **Tulostimen hallinta** -sivulla tulostimen ja valita sitten **Tulostinvalinnat**-toiminnon.
2. Valitse **Uusi**-toiminto, jos haluat lisätä tulostinvalinnan tiettyä raporttia varten.
3. Täytä tarvittavat kentät.

Määritetty raportti on nyt määritetty tulostamaan halutulle tulostimelle oletusarvoisesti.

> [!NOTE]
> Kun tulostat kyseisen raportin, voit ohittaa tämän asetuksen valitsemalla **Tulostusasetukset**-pyyntösivulla toisen tulostimen.

> [!NOTE]
> Jos et määritä raporttia tietylle tulostimelle **Tulostinvalinnat**-sivulla, se tulostetaan yrityksen oletustulostimeen **Tulostimen hallinta** -sivun määritysten mukaisesti.

Sinä tai järjestelmänvalvoja voitte käyttää myös **Tulostinvalinnat**-sivua käyttäjien ja raporttien muiden tulostusvaihtoehtojen määrittämisessä. Seuraava taulukko sisältää niiden arvojen yhdistelmät, joiden avulla määritetään raportin eri tulostusasetukset.

|Tehtävä                                                 |Määritä seuraavat arvot                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Tulosta raportti tiettyyn tulostimeen kaikille käyttäjille |Määritä arvot **Raportin tunnus**- ja **Tulostimen nimi** -kenttiin ja jätä **Käyttäjän tunnus** -kenttä tyhjäksi.|
|Tulosta kaikki raportit tiettyyn tulostimeen tietylle käyttäjälle|Määritä arvot **Käyttäjän tunnus**- ja **Tulostimen nimi** -kenttiin ja jätä **Raportin tunnus** -kenttä tyhjäksi.|
|Määritä oletustulostin kaikille raporteille|Määritä arvo **Tulostimen nimi** -kenttään ja jätä **Käyttäjän tunnus**- ja **Raportin tunnus** -kentät tyhjiksi.|
|Tulosta tietty raportti käyttäjän oletustulostimeen|Määritä arvo **Raportin tunnus** -kenttään ja jätä **Tulostimen nimi**- ja **Käyttäjän tunnus** -kentät tyhjiksi.|
|Tulosta tietty raportti tiettyyn tulostimeen tietylle käyttäjälle|Määritä arvot kaikkiin kolmeen kenttään.|

> [!NOTE]
> Yksityiskohtaiset tulostinvalinnat ohittavat yleisemmät tulostinvalinnat. Esimerkiksi tulostinvalinta, jossa on arvot **Käyttäjän tunnus**-, **Raportin tunnus**- ja **Tulostimen nimi** -kentissä, ohittaa tulostinvalinnan, jossa **Käyttäjän tunnus**- tai **Raportin tunnus** -kentät ovat tyhjät.

## <a name="see-also"></a>Katso myös
[Raportin tulostaminen](ui-work-report.md#PrintReport)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Eräajojen ajaminen](ui-how-run-batch-jobs.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]