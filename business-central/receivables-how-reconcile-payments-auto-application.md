---
title: Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta
description: 'Tietoja siitä, miten maksut voidaan täsmäyttää automaattisella kohdistustoiminnolla maksujen tai kassaanmaksujen kohdistamiseksi liittyviin avoimiin tapahtumiin.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '389, 1290, 1294, 1287'
ms.date: 06/22/2022
ms.author: bholtorf
---
# <a name="reconcile-payments-using-automatic-application" />Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta

**Maksujen täsmäytyskirjauskansio** -sivulla määritetään saapuvat ja lähtevät maksut, jotka on tallennettu tapahtumina verkkopankkitilille tai maksupalveluun. Voit kohdistaa maksut liittyviin avoimiin asiakas-, toimittaja-ja pankkitilitapahtumiin. Päiväkirjan voi täyttää tuomalla pankin tiliotteen pankkisyötteenä tai -tiedostona tai syöttämällä manuaalisesti transaktioita, joita teet maksupalvelussa.

> [!NOTE]
> Sivu tarjoaa automaattisen vastaavuustoiminnon, joka kohdistaa maksut niihin liittyviin avoimiin tapahtumiin pankin tiliotteen rivillä (päiväkirjan rivi) olevien tietojen vastaavuuden perusteella verrattuna yhden tai useamman avoimen tapahtuman tietoihin. Huomaa, että ehdotetut automaattiset kohdistukset voidaan korvata toisilla. Voit myös olla käyttämättä automaattista kohdistusta. Lisätietoja on vaiheessa 7.

Maksujen täsmäytyskirjauskansio liittyy yhteen pankkitiliin sovelluksessa [!INCLUDE[prod_short](includes/prod_short.md)]. Pankkitili vastaa verkkopankkitiliä, johon maksutapahtumat tallennetaan. Kaikki kohdistettuun asiakas- tai toimittajatapahtumaan liittyvät avoimet pankkitilitapahtumat suljetaan, kun valitset **Kirjaa maksut ja täsmäytä pankkitili** -toiminnon. Pankkitili täsmäytetään automaattisesti päiväkirjaan kirjattavia maksuja varten.

Jos käytössä on **Maksujen täsmäytyskirjauskansio** -sivu asiakasmaksujen rekisteröintiä ja käyttämistä varten, voit määrittää päiväkirjan tiettyjen numerosarjojen käyttöä varten. Jälkeenpäin voit määrittää numerosarjan **Maksujen täsmäytyksen numerosarjat** -kenttään pankkitilillä. Erillisen numerosarjan käyttäminen voi helpottaa päiväkirjan kautta kirjattujen tapahtumien tunnistamista.

Samoin kuin muissa päiväkirjoissa, kirjattujen tapahtumien korjaaminen voi peruuttaa tapahtumat, jotka on kirjattu maksujen täsmäytyskirjauskansion avulla **KP-rekisteri**-sivulla. Voit esimerkiksi haluta peruuttaa niiden maksujen tapahtumat, jotka olet kohdistasi väärälle asiakkaalle. Sinun täytyy ensin poistaa kirjattujen asiakastapahtumien kohdistus. Tämän jälkeen käytetään **Peruuta tapahtumat** -toimintoa **KP-rekisteri**-sivulla maksut kirjanneen päiväkirjan peruuttamiseksi. Vaihtoehtoisesti voit käyttää **Kirjatut yleiskirjauskansiot** -sivulla **Kopioi valitut rivit kirjauskansioon** -toimintoa, jos haluat peruuttaa tietyt rivit kirjatusta maksujen täsmäytyskirjauskansiosta. 

Kun käytät automaattista kohdistusta, [!INCLUDE[prod_short](includes/prod_short.md)] tunnistaa jo kirjatut pankkitapahtumat. Tämä auttaa estämään kaksinkertaisen kirjauksen.

Voit tuoda pankkitapahtumia .csv-pankkitiedostoina tai muussa pankkisi muodossa. Jos haluat ottaa pankin tiliotteet käyttöön pankkisyötteinä, ota ensin käyttöön erillinen pankin integrointipalvelu ja linkitä sitten pankkitili siihen liittyvään verkkopankkitiliin. Maksujen täsmäytyskirjauskansio havaitsee automaattisesti pankkisyötteet, kun valitset **Tuo pankkitapahtumat** -toiminnon. Lisäksi voit määrittää pankkitilin niin, että se tuo uudet tiliotesyötteet tunnin välein automaattisesti. Niiden maksujen tapahtumia, jotka on jo kohdistettu ja/tai täsmäytetty, ei tuoda. Voit käyttää näiden tapahtumien hakemiseen Envestnet Yodlee Bank Feeds -palvelua, joka on esiasennettu joidenkin maiden/alueiden [!INCLUDE[d365fin](includes/d365fin_md.md)] -versioissa. Lisätietoja on kohdassa [Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md). Voit myös ottaa yhteyttä Microsoft-kumppaniin yrityksesi tai maasi vaatimusten täyttämiseksi.

**Linkitä teksti tiliin** -toiminnolla voit määrittää maksujen tekstin kohdistukset ja tietyt debet-, kredit- ja kirjanpidon vastatilit siten, että nämä maksut kirjataan tietyille tileille, jotta nämä maksut kirjataan tietyille tileille, kun kirjaat maksun täsmäytyksen päiväkirjan. Yhdistämismääritys sopii esimerkiksi toistuviin saatuihin tuloihin tai kuluihin, kuten usein tapahtuvat auton polttoaineen ostot tai pankin kulut ja korko, jotka tapahtuvat pankin tiliotteessa säännöllisesti ja jotka eivät tarvitse niihin liittyvää liiketoiminta-asiakirjaa. (Katso vaihe 10.) Lisätietoja on kohdassa [Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Päiväkirjariveillä ei välttämättä ole ehdotettua kohdistusta. Tähän voi olla useita eri syitä. Syy voi olla esimerkiksi puuttuva asiakirja tai se, että asiakas on maksanut liikaa niin, että ylimääräinen summa on olemassa sen jälkeen, kun maksu on kohdistettu toiseen päiväkirjariviin. Tällaisissa tapauksissa voit käyttää **Siirrä erotus tilille** -toimintoa luodaksesi ja kirjataksesi puuttuvan pääkirjanpidon tapahtuman, esimerkiksi hyvityksen osalta, jota tarvitaan maksun kohdistamisessa. (Katso vaihe 11.) Lisätietoja on kohdassa [Niiden maksujen täsmäyttäminen, joita ei voi automaattisesti](receivables-how-reconcile-payments-cannot-apply-auto.md).

Voit käyttää **Kohdista automaattisesti** -toimintoa joko automaattisesti, kun tuot pankkitiedoston tai -syötteen ja maksutapahtumat, tai kun aktivoit sen maksujen kohdistamiseksi niiden vastaaviin avoimiin tapahtumiin, jotka perustuvat vastaavaan tekstiin pankin tiliotteen rivillä (päiväkirjarivillä), jossa on tekstiä avoimista tapahtumista. Tämä automaatio perustuu sääntöihin, jotka määritetään **Maksun kohdistussäännöt** -sivulla, jossa määritetään myös, edellyttääkö kohdistusehdotus tarkistusta. Lisätietoja on kohdassa [Määritä sääntöjä maksujen automaattiselle soveltamiselle](receivables-how-set-up-payment-application-rules.md).

Kirjauskansion riveillä, joilla maksu on kohdistettu automaattisesti yhteen tai useaan avoimeen tapahtumaan, **Vastaavuuden luotettavuus** -kentässä on arvo **Alhainen**, **Keskitaso** tai **Suuri**. Se osoittaa niiden kohdistettujen tietojen laadun, joihin ehdotettu maksusovellus perustuu.

Jotkin maksukohdistukset edellyttävät tarkistustasi sellaisena kuin se on määritelty käyteyssä vastaavuussäännössä, kuten riveillä, joiden luottamus on **Alhainen**. Muut rivit edellyttävät tarkistusta ja manuaalista muutosta, koska **Ero**-kentässä on arvo. Voit tarkistaa yhden tai useamman maksukohdistuksen valitsemalla **Tarkistettavat rivit**- tai **Rivit, joilla on erotus** -kentässä alaosassa. **Maksun kohdistuksen tarkistus** -sivulla näkyvät kaikki olennaiset tiedot asiakkaasta tai toimittajasta, johon maksu kohdistetaan, ja vastaavuuden tiedot sekä rivin käsittelyn toiminnot, kuten **Hyväksy kohdistus** -toiminto. (Katso vaiheet 7 ja 8)

Voit avata kullekin maksua esittävälle **Maksujen täsmäytyskirjauskansio** -sivun päiväkirjan riville **Maksun kohdistus** -sivun ja tarkastella kaikkia mahdollisia avoimia maksuja ja yksityiskohtaisia tietoja merkintöjen täsmäytyksestä, joihin maksujen kohdistus perustuu. Tässä voit kohdistaa maksuja manuaalisesti tai kohdistaa uudelleen maksuja, joka kohdistettiin automaattisesti väärään merkintään. (Katso vaihe 10.) Lisätietoja on kohdassa [Maksujen tarkasteleminen tai kohdistaminen automaattisen kohdistuksen jälkeen](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
> Voit aloittaa pankkitapahtumien tuonnin samaan aikaan kuin avaat **Maksujen täsmäytyskirjauskansio** -sivun aiemmin luodulle kirjauskansiolle. Seuraava toimenpide kuvaa kuinka pankkitapahtumat tuodaan **Maksujen täsmäytyskirjauskansio** -sivulle, kun olet luonut uuden päiväkirjan.

## <a name="to-reconcile-payments-using-automatic-application" />Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksujen täsmäytyskirjauskansiot** ja valitse sitten liittyvä linkki.
2. Voit käsitellä uuden maksun täsmäytyksen päiväkirjaa valitsemalla **Uusi päiväkirja** -toiminnon.
3. Valitse **Maksun pankkitililuettelo** -sivulla pankkitili, johon maksut täsmäytetään, ja valitse sitten **OK**-painike.
   **Maksujen täsmäytyskirjauskansio** -sivu avautuu valmisteltuna valitulle pankkitilille.
4. Valitse **Tuo pankkitapahtumat** -toiminto.
   Jos valitun kirjauskansion pankkitiliä ei ole määritetty pankkitapahtumien tuontia varten, [!INCLUDE[d365fin](includes/d365fin_md.md)] auttaa asiassa.
5. Valitse **Valitse tuotava tiedosto** -sivulla tiedosto, joka sisältää täsmäytettävät pankkitapahtumat täsmäytettäville maksuille, ja valitse sitten **Avaa**-painike.  
6. Jos Envestnet Yodlee Bank Feeds -palvelu on otettu käyttöön, määritä automaattisesti avautuvalla **Pankin tiliotteen suodatus** -sivulla pankin tiliotteiden tuonnille päivämääräväli.

    **Maksujen täsmäytyskirjauskansio** -sivu sisältää maksurivit, jotka kuvaavat tuodun pankin tiliotteen pankkitapahtumia.

     Maksujen riveillä, jotka on automaattisesti kohdistettu niiden vastaaviin avoimiin tapahtumiin, **Vastaavuuden luotettavuus** -kenttä osoittaa niiden kohdistettujen tietojen laadun, joihin ehdotettu maksusovellus perustuu. Lisäksi **Tilin nimi**- **Tilityyppi**- ja **Tilinumero**-kentät näyttävät sen asiakkaan tai toimittajan tiedot, johon maksu kohdistetaan.

    Automaattiset kohdistukset, vastaavat ominaisuudet ja se, onko rivit tarpeen tarkistaa, määritetään säännöillä. Voit muokata sääntöjä ja muuttaa niiden tuloksia. Lisätietoja on kohdassa [Määritä sääntöjä maksujen automaattiselle soveltamiselle](receivables-how-set-up-payment-application-rules.md).

7. Voit tarkistaa, hyväksyä/poistaa tai muuttaa manuaalisesti useita maksukohdistuksia, joilla on arvo **Ero** -kentässä, valitsemalla **Rivit, joilla on erotus** -toiminto alaosassa.

    Näyttöön tulee **Maksun kohdistuksen tarkistus** -sivu, jossa näkyy ensimmäinen tarkistettava kohdistus. Seuraava tarkistettava kohdistus näytetään sivulla, kun edellistä käsitellään. Tarkistus sisältää tiedot asiakkaasta tai toimittajasta, johon maksu kohdistetaan, ja vastaavuuden tiedot sekä rivin käsittelyn toiminnot, kuten **Hyväksy kohdistus**- ja **Hyväksy manuaalisesti** -toiminnot.

8. Voit tarkistaa, hyväksyä ja poistaa sekä manuaalisesti muuttaa useita maksusovelluksia, jotka sääntö on määritetty tarkistamaan, valitsemalla **Tarkistettavat rivit** -toiminnon. 

9. Voit muuttaa automaattista kohdistusta valitsemalla päiväkirjarivin ja sitten **Kohdista manuaalisesti** -toiminto, kun haluat kohdistaa uudelleen tai kohdistaa maksun manuaalisesti **Maksun kohdistus** -sivulla. Lisätietoja on kohdassa [Maksujen tarkasteleminen tai kohdistaminen automaattisen kohdistuksen jälkeen](receivables-how-review-apply-payments-auto-application.md).

10. Valitse kohdistamaton päiväkirjarivi toistuvalle kassasuoritukselle tai kululle, kuten auton polttoaineen hankinta ja valitse sitten **Linkitä teksti tiliin** -toiminto. Lisätietoja on kohdassa [Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

    Kun olet lopettanut maksutekstin yhdistämisen tileihin, valitse **Kohdista manuaalisesti** -toiminto.

    Kun tekstistä tiliin yhdistäminen on määritetty, tuloksena luotu automaattinen maksukohdistus sisältää **Suuri - Tekstin yhdistäminen tiliin** -arvon **Vastaavuuden luotettavuus** -kentässä.

11. Jos päiväkirjan rivillä ei ole ehdotettua kohdistusta, koska ei ole tapahtumaa, johon se voidaan kohdistaa, valitse **Siirrä erotus tilille** -toiminto luodaksesi ja kirjataksesi puuttuvan pääkirjanpidon tapahtuman, jota tarvitaan maksun kohdistamisessa. Lisätietoja on kohdassa [Niiden maksujen täsmäyttäminen, joita ei voi kohdistaa.](receivables-how-reconcile-payments-cannot-apply-auto.md)

12. Kun rivejä ei tarvitse enää tarkistaa ja **Ero**-kenttä on tyhjä kaikilla riveillä, valitse **Kirjaa**-toiminto ja valitse sitten jokin seuraavista vaihtoehdoista:

    - **Kirjaa maksut ja täsmäytä pankkitilit** – kirjataksesi maksut kohdistuksen mukaan ja myös sulkeaksesi liittyvät pankkitilitapahtumat täsmäytyksen mukaan.
    - **Kirjaa vain maksut** – kirjataksesi vain maksut kohdistuksen mukaan, mutta jättääksesi liittyvät pankkitilitapahtumat avoimiksi. Edellyttää, että täsmäytät pankkitilin erikseen, esimerkiksi: Lisätietoja on kohdassa [Pankkitilien täsmäyttäminen](bank-how-reconcile-bank-accounts-separately.md).
    - **Testiraportti** – Tarkastele kirjaamisen tulosta ennen kirjaamista valitsemalla. **Pankin tiliote** -raportti avautuu ja näyttää samat kentät kuin **Maksujen täsmäytyskirjauskansio** -sivun alaosassa.

Kun kirjaat maksujen täsmäytyskirjauskansion, kohdistetut avoimet tapahtumat suljetaan. Asiakas-, toimittaja- ja pääkirjanpitotilit on päivitettävä. Määritetyt kirjanpitotilit päivitetään tekstin tiliin yhdistämiseen perustuville asiakas-, toimittaja ja kirjanpitotileille. Kaikille pankkitilitapahtumille luodaan kirjauskansiorivit. Jos valitset **Kirjaa maksut ja täsmäytä pankkitili** -toiminnon, kaikki kohdistettuun asiakas- tai toimittajatapahtumaan liittyvät avoimet pankkitilitapahtumat suljetaan. Tämä tarkoittaa sitä, että pankkitili täsmäytetään automaattisesti päiväkirjaan kirjattaville maksuille.

Voit verrata **Pankkitilin saldo kirjauksen jälkeen** -kentän ja **Tiliotteen loppusaldo** -kentän arvoa seurataksesi, milloin pankkitili täsmäytetään kirjaamiesi maksujen perusteella.

> [!NOTE]  
>   Jos et halua täsmäyttää pankkitiliä **Maksujen täsmäytyskirjauskansio** -sivulla, sinun on käytettävä **Pankkitilin täsmäytys** -sivua. Lisätietoja on kohdassa [Pankkitilien täsmäyttäminen](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-related-microsoft-trainingtrainingmodulesuse-journals-dynamics--business-central" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/use-journals-dynamics-365-business-central/)

## <a name="see-also" />Katso myös

[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
