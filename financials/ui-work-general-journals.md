---
title: "Kirjaaminen suoraan pääkirjanpitoon yleisten päiväkirjojen avulla| Microsoft Docs"
description: "Tutustu, miten yleisiä päiväkirjoja käytetään rahoitustapahtumien kirjaamisessa pääkirjanpitotileille sekä muille tileille, kuten pankki- ja toimittajatileille."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2aac957fc253f6c7d2f621ea2e5e039733081a19
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="working-with-general-journals"></a>Yleisten päiväkirjojen käyttäminen
Useimmat rahoitustapahtumat kirjataan pääkirjanpitoon erityisten yritysasiakirjojen, kuten ostolaskujen ja myyntitilausten välityksellä. Liiketoiminnan aktiviteeteille, joihin ei liity [!INCLUDE[d365fin](includes/d365fin_md.md)]-asiakirjaa, kuten pienille kuluille tai käteissuorituksille voi luoda liittyvät tapahtumat kirjaamalla päiväkirjarivit **Yleinen päiväkirja** -ikkunassa. Lisätietoja on kohdassa [Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md).

Voit esimerkiksi kirjata työntekijöiden itse maksamat liiketoimintaan liittyvät kulut myöhemmin hyvitettäväksi. Lisätietoja on kohdassa [Työntekijöiden kulujen kirjaaminen ja hyvittäminen](finance-how-record-reimburse-employee-expenses.md).

Yleisiä päiväkirjoja käytetään rahoitustapahtumien kirjaamisessa suoraan pääkirjanpitotileille sekä muille tileille, kuten pankki-, asiakas-, toimittaja- ja työntekijätileille. Yleisen päiväkirjan avulla kirjaaminen luo aina tapahtumia kirjanpitotileille. Näin tapahtuu silloinkin, kun kirjataan esimerkiksi päiväkirjan rivi asiakkaan tilille, koska tapahtuma kirjataan pääkirjanpidon myyntisaamisten tilille kirjausryhmän kautta.

Päiväkirjaan lisäämäsi tiedot ovat väliaikaisia, ja niitä voi muuttaa niiden ollessa päiväkirjassa. Kun kirjaat päiväkirjan, tiedot siirretään yksittäisten tilien tapahtumiin, missä niitä ei voi muuttaa. Voit kuitenkin peruuttaa kirjattujen tapahtumien kohdistuksen tai kirjata peruuttavia tai korjaavia tapahtumia. Lisätietoja on kohdassa [Kirjauksien peruuttaminen](finance-how-reverse-journal-posting.md).

## <a name="using-journal-templates-and-batches"></a>Päiväkirjan mallit ja erien käyttäminen
Yleisen päiväkirjan malleja on useita. Kullakin päiväkirjamallilla on määritetty ikkuna, jossa on erityistoimintoja sekä näitä toimintoja varten tarvittavat kentät. Näitä ikkunoita ovat esimerkiksi **Maksujen täsmäytyskirjauskansio**, jossa käsitellään pankkimaksuja, ja **Maksupäiväkirja**, jossa maksetaan toimittajille tai maksetaan hyvitykset työntekijöille. Lisätietoja on kohdissa [Maksujen suorittaminen](payables-make-payments.md) ja [Asiakkaan maksujen täsmäyttäminen manuaalisesti](receivables-how-apply-sales-transactions-manually.md).

Voit määrittää kullekin päiväkirjan mallille oman henkilökohtaisen päiväkirjan päiväkirjan eränä. Voit esimerkiksi määrittää maksupäiväkirjalle oman päiväkirjan erän, jolle on määritetty henkilökohtainen asettelu ja asetukset. Seuraava vihje on esimerkki päiväkirjan mukauttamisesta.

> [!TIP]  
> Jos valitset **Yleisen päiväkirjan erät** -ikkunan erän rivillä olevan **Ehdota vastasummaa** -valintaruudun, esimerkiksi saman asiakirjanumeron yleisen päiväkirjan rivien **Summa**-kenttään esitäytetään automaattisesti arvo, joka vaaditaan asiakirjan täsmäyttämiseksi. Lisätietoja on ohjeaiheessa [[!INCLUDE[d365fin](includes/d365fin_md.md)] saa ehdottaa arvoja](ui-let-system-suggest-values.md).

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Päätilit ja vastatilit
Jos olet määrittänyt päiväkirjan erille oletusvastatilit **Yleiset päiväkirjat** -sivulla, vastatili täytetään automaattisesti, kun täytät **Tilinro**-kentän. Muussa tapauksessa täytä sekä **Tilinro**-kenttä että **Vastatilin nro** -kenttä manuaalisesti. Positiivinen summa **Summa**-kentässä veloitetaan päätililtä ja hyvitetään vastatilille. Negatiivinen summa hyvitetään päätilille ja veloitetaan vastatililtä.

> [!NOTE]  
>   ALV lasketaan erikseen päätiliä varten ja vastatiliä varten, joten niillä voi olla eri ALV-prosentit.

## <a name="working-with-recurring-journals"></a>Toistuvien päiväkirjojen käyttäminen
Toistuva päiväkirja on yleinen päiväkirja, jossa on erityiskenttiä sellaisten tapahtumien hallintaa varten, jotka kirjataan usein vähäisin muutoksin tai ilman muutoksia. Käyttämällä näitä kenttiä toistuviin tapahtumiin, voit kirjata sekä vakiosummia että muuttuvia summia. Voit myös määrittää automaattisen peruutuksen tapahtumat kirjauspäivämäärän jälkeisenä päivänä sekä käyttää kohdistusavaimia toistuvien tapahtumien kanssa.

## <a name="working-with-standard-journals"></a>Vakiopäiväkirjojen käyttäminen
Kun olet luonut päiväkirjan rivejä, joita todennäköisesti käytät myös vastaisuudessa, voit tallentaa rivit vakiopäiväkirjana, ennen kuin kirjaat rivit päiväkirjaan. Tämä toiminto koskee nimikepäiväkirjoja sekä yleisiä päiväkirjoja.

> [!NOTE]  
>   Vaikka seuraavassa puhutaan nimikepäiväkirjasta, samat tiedot koskevat myös yleistä päiväkirjaa.

### <a name="to-save-a-standard-journal"></a>Tallentaminen vakiopäiväkirjana
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Nimikepäiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.
2. Lisää koodi yhdelle tai usealle päiväkirjariville.
3. Valitse ne päiväkirjan rivit, joita haluat käyttää uudelleen.
4. Valitse **Tallenna vakiopäiväkirjana** -toiminto.
5. Määritä **Tallenna vakionimikepäiväkirjana** -pyyntöikkunassa uusi tai aiemmin luotu vakionimikepäiväkirja, johon rivit on tarkoitus tallentaa.

    Jos olet aiemmin luonut vähintään yhden vakionimikepäiväkirjan ja haluat korvata jonkin niistä uusilla päiväkirjan riveillä, valitse haluamasi vakionimikepäiväkirjan koodi napsauttamalla Koodi-kenttää.
6. Kun valitset **OK**, ohjelma pyytää varmistamaan aiemmin luodun vakionimikepäiväkirjan ja kaiken sen sisällön korvaamisen.
7. Valitse **Tallenna yksikkösumma** -kenttä, jos haluat tallentaa arvot vakionimikepäiväkirjan **Yksikkösumma** -kenttään.
8. Valitse **Tallenna määrä** -kenttä, jos ohjelman on tarkoitus tallentaa arvot **Määrä**-kenttään.
9. Valitse **OK**-painike tallentaaksesi vakionimikepäiväkirjan.

Kun olet tallentanut vakionimikepäiväkirjan, ohjelma siirtyy takaisin Nimikepäiväkirja-ikkunaan, jossa voit kirjata rivit. Tämän jälkeen voit kirjata samat tai vastaavat rivit vaivattomasti aina, kun tilanne sitä edellyttää.

### <a name="to-reuse-a-standard-journal"></a>Vakiopäiväkirjan käyttäminen uudelleen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Nimikepäiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Hae vakiopäiväkirjat** -toiminto.

    Näkyviin tulee Vakionimikepäiväkirjat-ikkuna, jossa on kaikkien luotujen vakionimikepäiväkirjojen koodit ja kuvaukset.
3. Voit tarkastella vakionimikepäiväkirjaa, ennen kuin valitset sen uudelleenkäytettäväksi, valitsemalla **Näytä päiväkirja** -toiminto.

    Vakionimikepäiväkirjaan tekemäsi muutokset toteutetaan heti. Ne ovat siellä, kun kyseinen vakionimikepäiväkirja seuraavan kerran avataan tai sitä käytetään uudelleen. Tämän vuoksi sinun täytyy olla varma, että muutos on tarpeeksi tärkeä sovellettavaksi yleisesti. Muutoin tee tarvittava muutos nimikepäiväkirja, kun nimikepäiväkirjan vakiorivit on lisätty. Lisätietoja on alla vaiheessa 4.
4. Valitse ensin **Vakionimikepäiväkirjat**-ikkunassa uudelleenkäytettävä vakiopäiväkirja ja sitten **OK**-painike.

    Vakiopäiväkirja täytetään riveillä, jotka olet tallentanut vakionimikepäiväkirjana. Jos nimikepäiväkirjassa on entuudestaan päiväkirjarivejä, lisättävät rivit sijoitetaan aiemmin luotujen päiväkirjarivien alle.

    Jos **Tallenna yksikkösumma** -kenttään ei lisätä valintamerkkiä **Tallenna vakionimikepäiväkirjana** -toiminnon suorittamisen yhteydessä, päiväkirjasta lisättyjen rivien **Yksikkösumma**-kenttä täytetään automaattisesti nimikkeen nykyisellä arvolla (joka kopioidaan nimikkeen kortin **Yksikkökustannus**-kentästä).

    > [!NOTE]  
>   Jos lisäät **Tallenna yksikkösumma**- ja/tai **Tallenna määrä** -kenttään valintamerkin, varmista, että lisätyt arvot ovat oikein tämän varastonmuutoksen osalta ennen niiden kirjaamista nimikepäiväkirjaan.

    Jos lisätyillä nimikepäiväkirjan riveillä on tallennettuja yksikkösummia, joita ei ole tarkoitus kirjata, voit muuttaa summan nopeasti nimikkeen nykyisen arvon mukaiseksi seuraavasti:

6. Valitse ensin muutettavat päiväkirjanrivit ja sitten **Laske yksikkösummat uudelleen** -toimintoa. Tällöin nimikkeen nykyinen yksikkökustannus tallennetaan Yksikkösumma-kenttään.
7. Valitse **Kirjaa**-toiminto.

## <a name="to-renumber-document-numbers-in-journals"></a>Asiakirjanumeroiden uudelleennumerointi päiväkirjoissa
Jos haluat varmistaa, että et saa kirjausvirheitä asiakirjan numerojärjestyksestä, voit käyttää **Numeroi asiakirjanumerot uudelleen**-toimintoa ennen päiväkirjan kirjaamista.

Kaikissa yleiseen päiväkirjaan perustuvissa päiväkirjoissa **Asiakirjanumero**-kenttä on muokattava, joten voit määrittää erilaisia asiakirjanumeroita päiväkirjan eri riveille tai saman asiakirjanumeron liittyville päiväkirjan riveille.

Jos **Nrosarja**-kenttä on kuitenkin täytetty päiväkirjaerässä, toiminnon kirjaaminen yleisessä päiväkirjassa vaatii, että asiakirjan numero yksittäisissä tai ryhmitetyissä päiväkirjarivissä on peräkkäisessä järjestyksessä. Jos haluat varmistaa, että et saa kirjausvirheitä asiakirjan numerojärjestyksestä, voit käyttää **Numeroi asiakirjanumerot uudelleen**-toimintoa ennen kuin kirjasit päiväkirjan. Jos liittyvät päiväkirjarivit ryhmitellään asiakirjanumeron mukaan ennen kuin käytit toimintoa, ne pysyvät ryhmiteltyinä, mutt saatetaan kohdistaa eri asiakirjanumeroon.

Tämä toiminto toimii myös suodatetuissa näkymissä.

Kaikissa asiakirjan numeroinneissa täytyy ottaa huomioon niihin liittyvät kohdistukset, kuten maksun kohdistus, joka on tehty asiakirjasta päiväkirjan rivillä toimittajan tiliin. Niinpä kyseisten tapahtumien **Kohdistetaan tunnisteeseen**- ja **Kohdistetaan asiakirjaan nro** -kentät voidaan päivittää.

Seuraavat toimenpiteet perustuvat **Yleinen päiväkirja** -ikkunaan, mutta niitä sovelletaan kaikkiin muihin päiväkirjoihin, jotka perustuvat yleiseen päiväkirjaan, kuten **Maksupäiväkirja**-ikkuna.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Yleiset päiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.
2. Kun olet valmis kirjaamaan päiväkirjan, valitse **Numeroi asiakirjanumerot uudelleen** -toiminto.

**Asiakirjanumero**-kentän arvoja muutetaan tarvittaessa siten, että yksittäisten tai ryhmitettyjen päiväkirjojen rivien asiakirjanumerot ovat peräkkäisessä järjestyksessä. Voit kirjata päiväkirjan, kun asiakirjat on numeroitu uudelleen.

## <a name="see-also"></a>Katso myös
[Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md)  
[Kirjausten peruuttaminen](finance-how-reverse-journal-posting.md)  
[Kustannusten ja tulojen kohdistaminen](year-allocate-costs-income.md)  
[Rahoitus](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

