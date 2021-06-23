---
title: Vaihekuvaus – Toimitusten manuaalinen suunnittelu | Microsoft Docs
description: Tässä vaihekuvauksessa kuvataan toimitustilausten suunnitteluprosessi uuden kysynnän täyttämiseksi. Voit aloittaa tarjonnan suunnittelun tietyin välein, esimerkiksi joka aamu tai joka maanantai, tai kun myynti tai tuotanto ilmoittaa ne kysyntätyypin mukaan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c1ab3c48ae09b75ab9e54e0c9fe9afd49b833f09
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214676"
---
# <a name="walkthrough-planning-supplies-manually"></a>Vaihekuvaus: Toimitusten manuaalinen suunnittelu

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Tässä vaihekuvauksessa kuvataan toimitustilausten suunnitteluprosessi uuden kysynnän täyttämiseksi. Voit aloittaa tarjonnan suunnittelun tietyin välein, esimerkiksi joka aamu tai joka maanantai, tai kun myynti tai tuotanto ilmoittaa ne kysyntätyypin mukaan. Tässä vaihekuvauksessa käytetään **Tilauksen suunnittelu** -sivua. Se on yksinkertainen toimitusten suunnittelutyökalu, joka perustuu parametripohjaisen automaattisen suunnittelun asemesta manuaaliseen päätöksentekoon.  

## <a name="about-this-walkthrough"></a>Tietoja tästä vaihekuvauksesta  
 Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:  

-   ostotilauksen suunnitteleminen valmistuskomponentteja varten  
-   myyntikysynnän täyttäminen siirtotilauksia suunnittelemalla  
-   monitasoisen nimikkeen tuotantotilauksen suunnitteleminen.  

## <a name="roles"></a>Roolit  
 Tässä vaihekuvauksessa havainnollistetaan seuraavien käyttäjäroolien tehtäviä:  

-   Tuotantosuunnittelija  
-   Ostaja  
-   myyntitilausten käsittelijä  

## <a name="prerequisites"></a>Vaatimukset  
 Ennen kuin aloitat tämän vaihekohtaisen ohjeen, sinun on asennettava [!INCLUDE[prod_short](includes/prod_short.md)]. Tietokantaan on tehtävä seuraavat muutokset:  

-   Poista kaikki aiemmat polkupyörien myyntitilaukset.  
-   Luo kymmenelle polkupyörälle yksi myyntitilaus ITÄ-sijaintiin.  
-   Poista kaikki suunnitellut ja sitovasti suunnitellut tuotantotilaukset. Älä poista aloitettuja tilauksia, joissa on aiemmin kirjattuja tapahtumia.  

 Tässä vaihekuvauksessa kannattaa käyttää ehdotettuja tietoja, koska näissä tiedoissa on tarvittavat tietueet.  

## <a name="story"></a>Taustatietoja  
 Pienen teollisuusyhtiön tuotantosuunnittelija Karl aikoo suunnitella tuotanto- ja ostotilaukset uuden myyntikysynnän täyttämiseksi.  

 Koska tuotteissa ei ole useaa tuoterakennetasoa eikä tilauksia ole paljon, Karl luo toimitustilaukset manuaalisesti **Tilauksen suunnittelu** -sivulla yksi tuotetaso kerrallaan.  

 Monimutkaisemmissa tuotantoympäristöissä suunnittelutyökirjaa käytetään toimitusten suunnitteluun, joka perustuu nimikeparametreihin, kuten uudelleenajoitusjaksoon, toimitusajan varmistukseen ja uusintatilauspisteeseen, sekä kaikkien tuotetasojen yhdistetyn kysynnän erälaskentaan.  

## <a name="setting-up-the-sample-data"></a>Esimerkkitietojen määrittäminen  
 Tavallisessa CRONUS esimerkkiyrityksessä on tällä hetkellä paljon suunnittelematonta kysyntää. Tämän vaihekuvauksen suunnittelutehtävien aikana realistisesta liiketoimintojen työnkulusta täytyy poiketa. Siitä poiketaan jättämällä huomiotta kysyntä, jonka eräpäivät ovat lähellä, ja käyttämällä sen sijaan kysyntää, jonka eräpäivät ovat myöhäisempiä.  

## <a name="using-the-order-planning-page"></a>Tilauksen suunnittelu -sivun käyttäminen  

**Tilauksen valmistelu** -sivua voi käyttää useista eri sijainneista:  

-   Tuotanto, Suunnittelu  
-   Myynti ja markkinointi, Tilauksen käsitteleminen  
-   Osto, Suunnittelu  
-   Lisäksi voit avata tämän sivun tietylle tuotantotilaukselle valitsemalla **Suunnitelma**-toiminnon.

### <a name="to-use-the-order-planning-page"></a>Tilauksen suunnittelu -sivun käyttäminen  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Tilauksen suunnittelu** ja valitse sitten liittyvä linkki.  

     Kun **Tilauksen suunnittelu** -sivu avautuu, suunnitelma on laskettava, jotta uusi, edellisen laskennan jälkeinen kysyntä tulee näyttöön.  

2.  Valitse **Laske suunnitelma** -toiminto.  

     Suunnittelujärjestelmä analysoi mahdollisen uuden kysynnän, kuten uuden myynnin, muuttuneen myynnin tai tuotantotilaukset.  

     Kunkin kysyntärivin tarvittu määrä lasketaan kokonaissaatavuuden perusteella. Nämä laskelmat tehdään tilauskohtaisesti. Toisin sanoin ensin lasketaan kysyntärivin sisältävä tilaus, jolla on varhaisin eräpäivä tai lähetyksen päivämäärä. Tämän jälkeen muut kysyntärivit lasketaan samassa järjestyksessä eräpäivästä ja lähetyksen päivämäärästä riippumatta.  

3.  Varmista, että **Tilauksen suunnittelu** -sivu on suurennettu ja että sarakkeen kenttien kokoa on muutettu siten, että kaikki oletuskenttänimet näkyvät.  

     Kun laskutoimitukset on suoritettu, täyttämätön kysyntä näkyy sivulla supistettuina tilauksen otsikkoriveinä, jotka on lajiteltu varhaisimman mahdollisen kysyntäpäivämäärän mukaan.  

     Huomaa, että CRONUS -ohjelmalla on useita tilauksia, joissa on täyttämätöntä kysyntää. Jokainen lihavoitu suunnittelurivi vastaa tilausta &mdash; myyntitilausta tai tuotantotilausta &mdash; ja mukana on vähintään yksi tilausrivi, jossa saatavuus on riittämätön.  

4.  Valitse **Näytä kysyntä muodossa** -kentän **Kaikki kysyntä** -suodatin.  

     **Kysyntätyyppi**-kentän avulla voit valita, mitkä tilaustyypit on tarkoitus tuoda näkyviin.  

     Tilaukset, joissa ei ole saatavuusongelmia, eivät näy. Jos suunnitelman laskemisen jälkeen ei ole tilauksia, näyttöön tulee sanoma, mutta ei suunnittelurivejä.  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a>Ostotilauksen suunnitteleminen komponenttien kysynnän täyttämiseksi  
 Näissä toimintaohjeissa luodaan ostotilaus tarvittavia valmistuskomponentteja varten.  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a>Ostotilauksen suunnitteleminen täyttämään tuotannon komponenttitarve  

1.  Laajenna ensimmäinen rivi (napsauta plusmerkkiä).  
2.  Valitse ensimmäinen kysyntärivi, jossa on nimike **LSU-15**, ja valitse sitten **Näytä asiakirja** -toiminto.  
3.  Siirry takaisin **Tilauksen suunnittelu** -sivulle sulkemalla avattu tuotantotilaus.  
4.  Valitse **Täydennysjärjestelmä**-kentässä **Osto**.  

     Oletusarvo on nimikkeen kortti (tai varastoyksikön kortti), mutta sen voi vaihtaa yhdeksi kolmesta vaihtoehdosta:  

    -   **Osto** – luodaan ostotilaus.  
    -   **Siirto** – Siirtotilauksen luominen  
    -   **Tuot.til.** – luodaan tuotantotilaus.  

5.  Valitse **Tarjonta kohteesta** -kentässä jokin seuraavista vaihtoehdoista valitun täydennysjärjestelmän mukaisesti.  

    -   **Toimittaja** – ostoille  
    -   **Sijainti** – Siirrot  

     Jos kentän tietoja ei täytetä, näkyviin tulee virhesanoma toimitustilauksia luotaessa.  

    > [!NOTE]  
    >  Jos komponenteille on määritetty toimittajan oletusnumero nimikkeen kortteihin, rivit on määritetty ennalta.  

6.  Valitse **Tarjonta kohteesta** -kenttä.  
7.  Valitse **Nimikkeen toimittajaluettelo** -sivulla **Uusi**-toiminto ja valitse toimittaja **30000**.  
8.  Valitse **OK**-painike palataksesi **Tilauksen suunnittelu** -sivulle.  
9. Kopioi toimittajan numero **30000** tämän tuotantotilauksen kaiutinkomponenttien muihin riveihin.  

     Nyt voit luoda ostotilauksen.  

10. Valitse **Tee tilaukset** -toiminto. **Tee toimitustilaukset** -sivu avautuu.  
11. Valitse **Tee tilaukset** -kentän **Tilauksen suunnittelu** -pikavälilehdessä **Aktiivinen tilaus**.  
12. Valitse **Vaihtoehdot**-pikavälilehden **Luo ostotilaus** -kentästä **Tee ostotilaukset**.  
13. Luo ostotilaukset tilauksen kaikille komponenteille valitsemalla **OK**.  

     Ostotilaukset luodaan ja tallennetaan viimeisiksi tilauksiksi ostotilausten luetteloon.  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a>Siirtotilauksen suunnitteleminen myyntikysynnän täyttämiseksi  
 Näissä toimintaohjeissa kysyntää varten laaditaan suunnitelma myyntitilauksesta. Kysyntärivit vastaavat myyntirivejä, eivät komponenttirivejä, kuten tuotantokysynnässä.  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a>Siirtotilauksen suunnitteleminen myyntikysynnän täyttämiseksi  

1.  Siirrä kohdistin tilauksen numero **2008** suunnitteluriville.  
2.  Laajenna rivi ja siirrä kohdistin kysyntäriville.  

     Myyntitilaus numero **2008** koskee kymmentä kaiutinta, joiden tyyppi on **LS-120** ja jotka on tilannut Vakuutusyhtiö Meri.  

     Näkyviin tulevat nimikkeen määritetty täydennysjärjestelmä ja oletustoimittaja.  

    > [!NOTE]  
    >  Sivun alaosassa on neljä tietokenttää. **Varhaisin mahdollinen päivämäärä** -kentässä näkyy, että tarvittavat kymmenen kappaletta tulevat saataville saapuvassa toimitustilauksessa yhdeksän päivää nykyisen eräpäivän jälkeen. Jos tämä on asiakkaalle liian myöhäinen ajankohta, **Siirtoon saatavilla** -kentässä näkyy, että nimikettä on 13 kappaletta toisessa sijainnissa. Tätä tavaraa varten on tarkoitus laatia suunnitelma.  

3.  Avaa **Hae vaihtoehtoinen tarjonta** -sivu napsauttamalla **Siirtoon saatavilla** -kentän hakupainiketta.  
4.  Varaa kymmenen saatavilla olevaa nimikettä valitsemalla **OK**.  

    > [!NOTE]  
    >  Siirto PÄÄ-sijainnista on vaihdettu ehdotetun oston tilalle kysyntäriville. **Tee tilaukset** -toiminto luo siirtotilauksen PÄÄ-sijainnista vaadittuun sijaintiin. **Korvaavia olemassa** -kenttä toimii samalla tavalla.  

5.  Valitse **Tee tilaukset** -toiminto. **Tee toimitustilaukset** -sivu avautuu.  
6.  Valitse **Tee tilaukset** -kentän **Tilauksen suunnittelu** -pikavälilehdessä **Aktiivinen tilaus**.  
7.  Valitse **Vaihtoehdot**-pikavälilehden **Luo siirtotilaus** -kentässä **Tee siirtotilaukset** -vaihtoehto.  
8.  Luo siirtotilaus myyntitilauksen toimittamista varten valitsemalla **OK**.  

     Siirtotilaus luodaan ja tallennetaan luetteloon avointen siirtotilausten luettelon viimeiseksi tilaukseksi.  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a>Monitasoisen tuotantotilauksen suunnitteleminen myyntikysynnän täyttämiseksi  
 Näissä toimintaohjeissa laaditaan suunnitelma, jossa tuotetun nimikkeen myyntikysyntä täytetään usealla tuotetasolla. Jokainen taso luo riippuvaisen tuotantokysynnän.  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a>Monitasoisen tuotannon suunnitteleminen myyntikysynnän täyttämiseksi  

1.  Valitse tilauksen numero **1001** suunnittelurivi, jolla on myyntikysyntää (se luotiin aiemmin vaihekuvauksen valmistavissa toimissa).  

     Tämä kysyntä on myyntirivi, mutta nimikkeelle on määritetty täydennysjärjestelmäksi **Tuotantotilaus**. Lisää ylimääräinen kello kunkin polkupyörän komponenttitarpeeseen.  

2.  Avaa **Suunnittelukomponentit**-sivu valitsemalla **Komponentit**-toiminto.  
3.  Vaihda Kello-nimikkeen rivillä **Määrä per** -kentän arvo **1** arvoksi **2**.  
4.  Harkitse suunnitteluvaihtoehtoja **Tilauksen suunnittelu** -sivulla. Tässä tilanteessa vaihtoehtoisia toimitustapoja &mdash; siirtoa tai korvaavaa tai myöhempää toimitusta &mdash; ei ole. Ehdotettu toimitustilaus, tuotantotilaus, on luotava.  
5.  Luo tuotantotilaus valitsemalla **Tee tilaukset** -toiminto.  

     Huomaa, että myyntitilauksen **1001** suunnitteluriviä ei enää ole **Tilauksen suunnittelu** -sivulla. Alustava myyntikysyntä on täytetty.  

6.  Sulje **Tilauksen suunnittelu** -sivu.  

     Tässä vaiheessa kaikki suunnittelutehtävät voitaisiin jäädä suorittamaan tähän näkymään. Nyt kuitenkin omaksutaan tuotantosuunnittelijan rooli, siirrytään äsken luotuun tuotantotilaukseen ja käytetään **Tilauksen suunnittelu** -sivua.  

 Tuotantosuunnittelijan täytyy nyt suunnitella tietty tuotantotilaus.  

### <a name="to-plan-a-specific-production-order"></a>Tietyn tuotantotilauksen suunnitteleminen  

1.  Avaa tuotantotilaus **101001** (kymmenen polkupyörää), joka luotiin aiemmin **Tee tilaukset**-toiminnolla.  
2.  Avaa **Tuot.til. komponentit** -sivu ja varmista, että ylimääräinen kello näkyy tuotantotilauksessa.  
3.  Valitse **Suunnittelu**-toiminto.  

     **Tilauksen suunnittelu** -sivu avautuu näkymään, joka suodatetaan aina tiettyyn tuotannon kysyntään. Myyntikysyntä ei ole näkyvissä. Suunnitelma on laskettava, ennen kuin lisäkysyntä tulee näkyviin.  

4.  Valitse **Laske suunnitelma** -toiminto.  

     Huomaa, että neljä uutta tuotantotilausta näkyy tilauksesta **101001** johdettuna suunnittelemattomana tuotantokysyntänä. Uudet rivit vastaavat niiden alikokoonpanojen uutta tuotantokysyntää, joka täytyy luoda tilauksen tuottamista varten.  

5.  Valitse **Laajenna kaikki** -toiminto, jos haluat nähdä yleiskuvauksen tuotantotilausten koko tuotantokysynnästä.  

     Antaaksesi lisätietoja kysyntäriveistä, saatat haluta lisätä **Kysyntämäärä** ja **Käytettävissä oleva kysyntämäärä** -kenttiä näkymääsi.  

     Seuraavaksi kutakin komponenttia on toimitettava kymmenen kappaletta.  

     Huomaa, että neljällä kysyntärivillä on täydennysjärjestelmä Tuotantotilaus. Nämä neljä osakokoonpanoa edustavat polkupyörän toista tuotantotasoa.  

     Oletustäydennysasetukset on täytetty valmiiksi, ja voit aloittaa tilausten tekemisen.  

6.  Valitse **Tee tilaukset** -toiminto.  

     Ennen kuin painat **OK**-painiketta, huomioi teksti **Tilauksen suunnittelu**-pikavälilehdessä. Tämä teksti on tärkeä, koska polkupyörän tuoterakenteessa tiedetään olevan joitakin tuotettuja komponentteja eli alikokoonpanoja, joilla voisi olla kysyntää, kun luot tämän tuotantotilauksen.  

7.  Valitse **Tee toimitustilaukset** -sivun **Tee tilaukset**-kentässä **Kaikki rivit** ja valitse sitten **OK**, jos haluat luoda tuotantotilaukset tilauksen toiselle tuotetasolle.  

     Huomaa, että tuotantotilauksella 101001 ei enää ole ylätason tuotantokysyntää. Se merkitsee, että alikokoonpanojen alustava tuotantokysyntä on otettu huomioon suunnittelussa.  

     Suunnitelma lasketaan uudelleen **Tilauksen suunnittelu** -sivulla, jotta polkupyörän rakenne voidaan suunnitella.  

8.  Laske suunnitelma uudelleen upotetun ohjetekstin ohjeiden mukaisesti valitsemalla **Laske suunnitelma**.  

     Kaksi uutta riviä vastaavat ylimääräistä tuotantokysyntää, joka on johdettu edellisissä vaiheissa suunnitelluista alikokoonpanoista. Pyörän napojen toimittamiseksi ehdotetaan kahta tuotantotilausta, yhtä kymmenelle etupyörän navalle ja niin ikään yhtä kymmenelle takapyörän navalle.  

9. Valitse **Laajenna kaikki** -toiminto, jos haluat nähdä yleiskuvauksen kahden tuotantotilauksen koko tuotantokysynnästä.  

     Ehdotettu toimitussuunnitelma osoittaa, että komponenteille luodaan yhteensä neljä ostotilausta. Ehdotetut tilaukset päätetään tehdä.  

10. Valitse **Tee tilaukset** -toiminto.  
11. Valitse **Tee tilaukset** -kentässä **Kaikki rivit** ja valitse sitten **OK**. Tarkista, onko päänimikkeen eli polkupyörän (myydään myyntitilauksella 1001) tuotannolla lisäkysyntää.  
12. Valitse **Laske suunnitelma** -toiminto.  

     Sanomassa ilmoitetaan, että kaikki vaaditut nimikkeet on nyt toimitettu. Varmista sitovasti suunnitellut tuotantotilaukset, jotka on luotu.  

13. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Sitovasti suunn. tuotantotil.** ja valitse sitten liittyvä linkki.  

     Tarkista **Sitovasti suunn. tuotantotil.** -sivulla, miten yksittäisten tilausten aloitus- ja päättymisajat on ajoitettu tuoterakenteen mukaan. Alimman tason komponentit tuotetaan ensin. Monitasoisten tilausten suunnitteleminen onkin tärkeää, kuten tässä suunnittelun työnkulussa on havainnollistettu.  

## <a name="see-also"></a>Katso myös  
 [Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)   
<!--  [Walkthrough: Planning Supplies Automatically](walkthrough-planning-supplies-automatically.md) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]