---
title: Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta
description: Tässä ohjeaiheessa kerrotaan, miten maksut tai kassaanmaksut voidaan kohdistaa automaattisella kohdistustoiminnolla liittyviin avoimiin tapahtumiin ja maksut täsmäyttää.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.search.form: 389, 1290, 1294, 1287
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2418ca1164d0a3d67ca9ae3403733dfbd9a56660
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8520810"
---
# <a name="reconcile-payments-using-automatic-application"></a>Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta

**Maksujen täsmäytyskirjauskansio** -sivu määrittää tulevat tai lähtevät maksut, jotka on tallennettu tapahtumina verkkopankkitilille tai maksupalveluun ja jotka voit kohdistaa niihin liittyviin avoimiin asiakas-, toimittaja- ja pankkitilitapahtumiin. Päiväkirjan rivit voi täyttää tuomalla pankin tiliotteen pankkisyötteenä tai -tiedostona tai syöttämällä manuaalisesti transaktioita, joita teet maksupalvelussa.

> [!NOTE]
> Sivu tarjoaa automaattisen vastaavuustoiminnon, joka kohdistaa maksut niihin liittyviin avoimiin tapahtumiin pankin tiliotteen rivillä (päiväkirjan rivi) olevien tietojen vastaavuuden perusteella verrattuna yhden tai useamman avoimen tapahtuman tietoihin. Huomaa, että ehdotetut automaattiset kohdistukset voidaan korvata toisilla. Voit myös olla käyttämättä automaattista kohdistusta. Lisätietoja on vaiheessa 7.

Täsmäytyksen maksukirjauskansioon liittyy [!INCLUDE[prod_short](includes/prod_short.md)]issa yksi pankkitili, joka vastaa verkkopankkitiliä, jolle maksutapahtumat kirjataan. Kaikki kohdistettuun asiakas- tai toimittajatapahtumaan liittyvät avoimet pankkitilitapahtumat suljetaan, kun valitset **Kirjaa maksut ja täsmäytä pankkitili** -toiminnon. Tämä tarkoittaa sitä, että pankkitili täsmäytetään automaattisesti päiväkirjaan kirjattaville maksuille.

Voit tuoda pankkitapahtumia .csv-pankkitiedostoina tai muussa pankkisi muodossa. Jos haluat ottaa pankin tiliotteet käyttöön pankkisyötteinä, ota ensin käyttöön erillinen pankin integrointipalvelu ja linkitä sitten pankkitili siihen liittyvään verkkopankkitiliin. Maksujen täsmäytyskirjauskansio havaitsee automaattisesti pankkisyötteet, kun valitset **Tuo pankkitapahtumat** -toiminnon. Lisäksi voit määrittää pankkitilin niin, että se tuo uudet tiliotesyötteet tunnin välein automaattisesti. Niiden maksujen tapahtumia, jotka on jo kohdistettu ja/tai täsmäytetty, ei tuoda. Voit käyttää tähän Envestnet Yodlee Bank Feeds -palvelua, joka on esiasennettu joidenkin maiden/alueiden [!INCLUDE[d365fin](includes/d365fin_md.md)] -versioissa. Lisätietoja on kohdassa [Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md). Voit myös ottaa yhteyttä Microsoft-kumppaniisi yrityksesi tai maasi vaatimusten täyttämiseksi.

**Linkitä teksti tiliin** -toiminnolla voit määrittää maksujen tekstin kohdistukset ja tietyt debet-, kredit- ja kirjanpidon vastatilit siten, että nämä maksut kirjataan tietyille tileille, jotta nämä maksut kirjataan tietyille tileille, kun kirjaat maksun täsmäytyksen päiväkirjan. Tämä sopii esimerkiksi toistuviin saatuihin tuloihin tai kuluihin, kuten usein tapahtuvat auton polttoaineen ostot tai pankin kulut ja korko, jotka tapahtuvat pankin tiliotteessa säännöllisesti ja jotka eivät tarvitse niihin liittyvää liiketoiminta-asiakirjaa. (Katso alla vaihe 10.) Lisätietoja on kohdassa [Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Päiväkirjariveillä ei välttämättä ole ehdotettua kohdistusta. Tämä voi johtua useista syistä, esimerkiksi puuttuvasta asiakirjasta tai siitä, että asiakas on maksanut liikaa, niin että ylimääräinen summa on olemassa sen jälkeen, kun maksu on kohdistettu toiseen päiväkirjariviin. Tällaisissa tapauksissa voit käyttää **Siirrä erotus tilille** -toimintoa luodaksesi ja kirjataksesi puuttuvan pääkirjanpidon tapahtuman, esimerkiksi hyvityksen osalta, jota tarvitaan maksun kohdistamisessa. (Katso alla vaihe 11.) Lisätietoja on kohdassa [Niiden maksujen täsmäyttäminen, joita ei voi automaattisesti](receivables-how-reconcile-payments-cannot-apply-auto.md).

Voit käyttää **Kohdista automaattisesti** -toimintoa joko automaattisesti, kun tuot pankkitiedoston tai -syötteen ja maksutapahtumat, tai kun aktivoit sen maksujen kohdistamiseksi niiden vastaaviin avoimiin tapahtumiin, jotka perustuvat vastaavaan tekstiin pankin tiliotteen rivillä (päiväkirjarivillä), jossa on tekstiä avoimista tapahtumista. Tämä automaatio perustuu sääntöihin, jotka määritetään **Maksun kohdistussäännöt** -sivulla, jossa määritetään myös, edellyttääkö kohdistusehdotus tarkistusta. Lisätietoja on kohdassa [Määritä sääntöjä maksujen automaattiselle soveltamiselle](receivables-how-set-up-payment-application-rules.md).

Kirjauskansion riveillä, joilla maksu on kohdistettu automaattisesti yhteen tai useaan avoimeen tapahtumaan, **Vastaavuuden luotettavuus** -kentässä on arvo **Alhainen**, **Keskitaso** tai **Suuri**. Se osoittaa niiden kohdistettujen tietojen laadun, joihin ehdotettu maksusovellus perustuu.

Jotkin maksukohdistukset edellyttävät tarkistustasi sellaisena kuin se on määritelty käyteyssä vastaavuussäännössä, kuten riveillä, joiden luottamus on **Alhainen**. Muut rivit edellyttävät tarkistusta ja manuaalista muutosta, koska **Ero**-kentässä on arvo. Voit tarkistaa yhden tai useamman maksukohdistuksen valitsemalla **Tarkistettavat rivit**- tai **Rivit, joilla on erotus** -kentässä alaosassa. **Maksun kohdistuksen tarkistus** -sivulla näkyvät kaikki olennaiset tiedot asiakkaasta tai toimittajasta, johon maksu kohdistetaan, ja vastaavuuden tiedot sekä rivin käsittelyn toiminnot, kuten **Hyväksy kohdistus** -toiminto. (Katso vaiheet 7 ja 8 jäljempänä.)

Voit avata kullekin maksua esittävälle **Maksujen täsmäytyskirjauskansio** -sivun päiväkirjan riville **Maksun kohdistus** -sivun ja tarkastella kaikkia mahdollisia avoimia maksuja ja yksityiskohtaisia tietoja merkintöjen täsmäytyksestä, joihin maksujen kohdistus perustuu. Tässä voit kohdistaa maksuja manuaalisesti tai kohdistaa uudelleen maksuja, joka kohdistettiin automaattisesti väärään merkintään. (Katso alla vaihe 10.) Lisätietoja on kohdassa [Maksujen tarkasteleminen tai kohdistaminen automaattisen kohdistuksen jälkeen](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
> Voit aloittaa pankkitapahtumien tuonnin samaan aikaan kuin avaat **Maksujen täsmäytyskirjauskansio** -sivun aiemmin luodulle kirjauskansiolle. Seuraava toimenpide kuvaa kuinka pankkitapahtumat tuodaan **Maksujen täsmäytyskirjauskansio** -sivulle, kun olet luonut uuden päiväkirjan.

## <a name="to-reconcile-payments-using-automatic-application"></a>Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksujen täsmäytyskirjauskansiot** ja valitse sitten liittyvä linkki.
2. Voit käsitellä uuden maksun täsmäytyksen päiväkirjaa valitsemalla **Uusi päiväkirja** -toiminnon.
3. Valitse **Maksun pankkitililuettelo** -sivulla pankkitili, johon maksut täsmäytetään, ja valitse sitten **OK**-painike.
   **Maksujen täsmäytyskirjauskansio** -sivu avautuu valmisteltuna valitulle pankkitilille.
4. Valitse **Tuo pankkitapahtumat** -toiminto.
   Jos pankkitapahtumien tuontia varten ei ole määritetty valitun kirjauskansion pankkitiliä, valintaikkuna avautuu auttaen sinua täyttämään asianmukaiset kentät.
5. Valitse **Valitse tuotava tiedosto** -sivulla tiedosto, joka sisältää täsmäytettävät pankkitapahtumat täsmäytettäville maksuille, ja valitse sitten **Avaa**-painike.  
6. Jos Envestnet Yodlee Bank Feeds -palvelu on otettu käyttöön, määritä automaattisesti avautuvalla **Pankin tiliotteen suodatus** -sivulla pankin tiliotteiden tuonnille päivämääräväli.

    **Maksujen täsmäytyskirjauskansio** -sivu sisältää maksurivit, jotka kuvaavat tuodun pankin tiliotteen pankkitapahtumia.

     Maksujen riveillä, jotka on automaattisesti kohdistettu niiden vastaaviin avoimiin tapahtumiin, **Vastaavuuden luotettavuus** -kentässä on arvo väliltä **Alhainen** ja **Suuri**. Tämä osoittaa niiden kohdistettujen tietojen laadun, joihin ehdotettu maksusovellus perustuu. Lisäksi **Tilin nimi**- **Tilityyppi**- ja **Tilinumero**-kentät täytetään sen asiakkaan tai toimittajan tiedoilla, johon maksu kohdistetaan.

    Automaattiset kohdistukset, vastaavat ominaisuudet ja se, onko rivit tarpeen tarkistaa, määritetään säännöillä, joita voit muokata tulosten säätämistä varten. Lisätietoja on kohdassa [Määritä sääntöjä maksujen automaattiselle soveltamiselle](receivables-how-set-up-payment-application-rules.md).

7. Voit tarkistaa, hyväksyä/poistaa tai muuttaa manuaalisesti useita maksukohdistuksia, joilla on arvo **Ero** -kentässä, valitsemalla **Rivit, joilla on erotus** -toiminto alaosassa.

    Näyttöön tulee **Maksun kohdistuksen tarkistus** -sivu, jossa näkyy ensimmäinen tarkistettava kohdistus. Seuraava tarkistettava kohdistus näytetään sivulla, kun edellistä käsitellään. Kaikki olennaiset tiedot asiakkaasta tai toimittajasta, johon maksu kohdistetaan, ja vastaavuuden tiedot sekä rivin käsittelyn toiminnot, kuten **Hyväksy kohdistus**- ja **Hyväksy manuaalisesti** -toiminnot.

8. Jos haluat tarkastella, hyväksyä tai poistaa tai muuttaa manuaalisesti useampia tarkistettaviksi määritettyjä maksukohdistuksia, valitse maksun kohdistussäännön mukaan **Tarkistettavat rivit** -toiminto alaosassa. Sama kokemus kuin kuvattu vaiheessa 8

9. Voit muuttaa automaattista kohdistusta valitsemalla päiväkirjarivin ja sitten **Kohdista manuaalisesti** -toiminto, kun haluat kohdistaa uudelleen tai kohdistaa maksun manuaalisesti **Maksun kohdistus** -sivulla. Lisätietoja on kohdassa [Maksujen tarkasteleminen tai kohdistaminen automaattisen kohdistuksen jälkeen](receivables-how-review-apply-payments-auto-application.md).

10. Valitse kohdistamaton päiväkirjarivi toistuvalle kassasuoritukselle tai kululle, kuten auton polttoaineen hankinta ja valitse sitten **Linkitä teksti tiliin** -toiminto. Lisätietoja on kohdassa [Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

    Kun olet lopettanut maksutekstin yhdistämisen tileihin, valitse **Kohdista manuaalisesti** -toiminto.

    Kun tekstistä tiliin yhdistäminen on määritetty, tuloksena luotu automaattinen maksukohdistus sisältää **Suuri - Tekstin yhdistäminen tiliin** -arvon **Vastaavuuden luotettavuus** -kentässä.

11. Jos päiväkirjan rivillä ei ole ehdotettua kohdistusta, koska ei ole tapahtumaa, johon se voidaan kohdistaa, valitse **Siirrä erotus tilille** -toiminto luodaksesi ja kirjataksesi puuttuvan pääkirjanpidon tapahtuman, jota tarvitaan maksun kohdistamisessa. Lisätietoja on kohdassa [Niiden maksujen täsmäyttäminen, joita ei voi kohdistaa.](receivables-how-reconcile-payments-cannot-apply-auto.md)

10. Kun rivejä ei tarvitse enää tarkistaa ja **Ero**-kenttä on tyhjä kaikilla riveillä, valitse **Kirjaa**-toiminto ja valitse sitten jokin seuraavista vaihtoehdoista:

    - **Kirjaa maksut ja täsmäytä pankkitilit** – kirjataksesi maksut kohdistuksen mukaan ja myös sulkeaksesi liittyvät pankkitilitapahtumat täsmäytyksen mukaan.
    - **Kirjaa vain maksut** – kirjataksesi vain maksut kohdistuksen mukaan, mutta jättääksesi liittyvät pankkitilitapahtumat avoimiksi. Edellyttää, että täsmäytät pankkitilin erikseen, esimerkiksi: Lisätietoja on kohdassa [Pankkitilien täsmäyttäminen](bank-how-reconcile-bank-accounts-separately.md).
    - **Testiraportti** – Tarkastele kirjaamisen tulosta ennen kirjaamista valitsemalla. **Pankin tiliote** -raportti avautuu ja näyttää samat kentät kuin **Maksujen täsmäytyskirjauskansio** -sivun alaosassa.

Kun kirjaat maksun täsmäytyksen päiväkirjan, kohdistetut avoimet tapahtumat suljetaan ja liittyvät asiakas- tai toimittaja- tai kirjanpitotilit päivitetään. Määritetyt kirjanpitotilit päivitetään tekstin tiliin yhdistämiseen perustuville asiakas-, toimittaja ja kirjanpitotileille. Kaikille pankkitilitapahtumille luodaan kirjauskansiorivit. Jos valitset **Kirjaa maksut ja täsmäytä pankkitili** -toiminnon, kaikki kohdistettuun asiakas- tai toimittajatapahtumaan liittyvät avoimet pankkitilitapahtumat suljetaan. Tämä tarkoittaa sitä, että pankkitili täsmäytetään automaattisesti päiväkirjaan kirjattaville maksuille.

Voit verrata **Pankkitilin saldo kirjauksen jälkeen** -kentän ja **Tiliotteen loppusaldo** -kentän arvoa seurataksesi, milloin pankkitili täsmäytetään kirjaamiesi maksujen perusteella.

> [!NOTE]  
>   Jos et halua täsmäyttää pankkitiliä **Maksujen täsmäytyskirjauskansio** -sivulla, sinun on käytettävä **Pankkitilin täsmäytys** -sivua. Lisätietoja on kohdassa [Pankkitilien täsmäyttäminen](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-also"></a>Katso myös
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]