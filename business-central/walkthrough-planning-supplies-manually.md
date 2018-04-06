---
title: "Vaihekuvaus – Toimitusten manuaalinen suunnittelu | Microsoft Docs"
description: "Tässä vaihekuvauksessa kuvataan toimitustilausten suunnitteluprosessi uuden kysynnän täyttämiseksi. Voit aloittaa tarjonnan suunnittelun tietyin välein, esimerkiksi joka aamu tai joka maanantai, tai kun myynti tai tuotanto ilmoittaa ne kysyntätyypin mukaan."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2992c2a9cbd2142e69cfb59294791ec31ce4dcb1
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-planning-supplies-manually"></a>Vaihekuvaus: Toimitusten manuaalinen suunnittelu
Tässä vaihekuvauksessa käsitellään toimitustilausten suunnitteluprosessia uuden kysynnän täyttämiseksi. Voit aloittaa tarjonnan suunnittelun tietyin välein, esimerkiksi joka aamu tai joka maanantai, tai kun myynti tai tuotanto ilmoittaa ne kysyntätyypin mukaan. Tässä vaihekuvauksessa käytetään **Tilauksen suunnittelu** -ikkunaa. Se on yksinkertainen toimitusten suunnittelutyökalu, joka perustuu parametripohjaisen automaattisen suunnittelun asemesta manuaaliseen päätöksentekoon.  

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
 Ennen kuin aloitat tämän vaihekohtaisen ohjeen, sinun on asennettava [!INCLUDE[d365fin](includes/d365fin_md.md)]. Tietokantaan on tehtävä seuraavat muutokset:  

-   Poista kaikki aiemmat polkupyörien myyntitilaukset.  
-   Luo kymmenelle polkupyörälle yksi myyntitilaus SININEN-sijaintiin.  
-   Poista kaikki suunnitellut ja sitovasti suunnitellut tuotantotilaukset. Älä poista aloitettuja tilauksia, joissa on aiemmin kirjattuja tapahtumia.  

 Tässä vaihekuvauksessa kannattaa käyttää ehdotettuja tietoja, koska näissä tiedoissa on tarvittavat tietueet.  

## <a name="story"></a>Taustatietoja  
 Pienen teollisuusyhtiön tuotantosuunnittelija Karl aikoo suunnitella tuotanto- ja ostotilaukset uuden myyntikysynnän täyttämiseksi.  

 Koska tuotteissa ei ole useaa tuoterakennetasoa eikä tilauksia ole paljon, Karl luo toimitustilaukset manuaalisesti **Tilauksen suunnittelu** -ikkunassa yksi tuotetaso kerrallaan.  

 Monimutkaisemmissa tuotantoympäristöissä suunnittelutyökirjaa käytetään toimitusten suunnitteluun, joka perustuu nimikeparametreihin, kuten uudelleenajoitusjaksoon, toimitusajan varmistukseen ja uusintatilauspisteeseen, sekä kaikkien tuotetasojen yhdistetyn kysynnän erälaskentaan.  

## <a name="setting-up-the-sample-data"></a>Esimerkkitietojen määrittäminen  
 Tavallisessa CRONUS-esimerkkiyrityksessä on tällä hetkellä paljon suunnittelematonta kysyntää. Tämän vaihekuvauksen suunnittelutehtävien aikana realistisesta liiketoimintojen työnkulusta täytyy poiketa. Siitä poiketaan jättämällä huomiotta kysyntä, jonka eräpäivät ovat lähellä, ja käyttämällä sen sijaan kysyntää, jonka eräpäivät ovat myöhäisempiä.  

## <a name="using-the-order-planning-window"></a>Tilauksen suunnittelu -ikkunan käyttäminen  

<!-- 
The **Order Planning** window can be accessed from several different locations on the **Departments** menu in the navigation pane:  

-   Manufacturing, Planning  
-   Sales & Marketing, Order Processing  
-   Purchase, Planning  
-   In addition, you can open this window for a specific production order by choosing **Planning** on the **Navigate** tab in the **Order** group.

-->  

### <a name="to-use-the-order-planning-window"></a>Tilauksen suunnittelu -ikkunan käyttäminen  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tilauksen suunnittelu** ja valitse sitten aiheeseen liittyvä linkki.  

     Kun **Tilauksen suunnittelu** -ikkuna aukeaa, suunnitelma on laskettava, jotta uusi, edellisen laskennan jälkeinen kysyntä tulee näyttöön.  

2.  Valitse **Laske suunnitelma** -toiminto.  

     Suunnittelujärjestelmä analysoi mahdollisen uuden kysynnän, kuten uuden myynnin, muuttuneen myynnin tai tuotantotilaukset.  

     Kunkin kysyntärivin tarvittu määrä lasketaan kokonaissaatavuuden perusteella. Nämä laskelmat tehdään tilauskohtaisesti. Toisin sanoin ensin lasketaan kysyntärivin sisältävä tilaus, jolla on varhaisin eräpäivä tai lähetyksen päivämäärä. Tämän jälkeen muut kysyntärivit lasketaan samassa järjestyksessä eräpäivästä ja lähetyksen päivämäärästä riippumatta.  

3.  Varmista, että **Tilauksen suunnittelu** -ikkuna on suurennettu ja että sarakkeen kenttien kokoa on muutettu siten, että kaikki oletuskenttänimet näkyvät.  

     Kun laskutoimitukset on suoritettu, täyttämätön kysyntä näkyy ikkunassa supistettuina tilauksen otsikkoriveinä, jotka on lajiteltu varhaisimman mahdollisen kysyntäpäivämäärän mukaan.  

     Huomaa, että CRONUSilla on useita tilauksia, joissa on täyttämätöntä kysyntää. Jokainen lihavoitu suunnittelurivi vastaa tilausta &mdash; myyntitilausta tai tuotantotilausta &mdash; ja mukana on vähintään yksi tilausrivi, jossa saatavuus on riittämätön.  

4.  Valitse **Näytä kysyntä muodossa** -kentän **Kaikki kysyntä** -suodatin.  

     **Kysyntätyyppi**-kentän avulla voit valita, mitkä tilaustyypit on tarkoitus tuoda näkyviin.  

     Tilaukset, joissa ei ole saatavuusongelmia, eivät näy. Jos suunnitelman laskemisen jälkeen ei ole tilauksia, näyttöön tulee sanoma, mutta ei suunnittelurivejä.  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a>Ostotilauksen suunnitteleminen komponenttien kysynnän täyttämiseksi  
 Näissä toimintaohjeissa luodaan ostotilaus tarvittavia valmistuskomponentteja varten.  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a>Ostotilauksen suunnitteleminen täyttämään tuotannon komponenttitarve  

1.  Laajenna ensimmäinen rivi (napsauta plusmerkkiä).  
2.  Valitse ensimmäinen kysyntärivi, jossa on nimike **LSU-15**, ja valitse sitten **Näytä asiakirja** -toiminto.  
3.  Siirry takaisin **Tilauksen suunnittelu** -ikkunaan sulkemalla avattu tuotantotilaus.  
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
7.  Valitse **Nimikkeen toimittajaluettelo** -ikkunassa **Uusi**-toiminto ja valitse toimittaja **30000**.  
8.  Valitse **OK**-painike palataksesi **Tilauksen suunnittelu** -ikkunaan.  
9. Kopioi toimittajan numero **30000** tämän tuotantotilauksen kaiutinkomponenttien muihin riveihin.  

     Nyt voit luoda ostotilauksen.  

10. Valitse **Tee tilaukset** -toiminto. **Tee toimitustilaukset** -ikkuna avautuu.  
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
    >  Ikkunan alaosassa on neljä tietokenttää. **Varhaisin mahdollinen päivämäärä** -kentässä näkyy, että tarvittavat kymmenen kappaletta tulevat saataville saapuvassa toimitustilauksessa yhdeksän päivää nykyisen eräpäivän jälkeen. Jos tämä on asiakkaalle liian myöhäinen ajankohta, **Siirtoon saatavilla** -kentässä näkyy, että nimikettä on 13 kappaletta toisessa sijainnissa. Tätä tavaraa varten on tarkoitus laatia suunnitelma.  

3.  Avaa **Hae vaihtoehtoinen tarjonta** -ikkuna napsauttamalla **Siirtoon saatavilla** -kentän hakupainiketta.  
4.  Varaa kymmenen saatavilla olevaa nimikettä valitsemalla **OK**.  

    > [!NOTE]  
    >  Siirto VIHREÄ-sijainnista on vaihdettu ehdotetun oston tilalle kysyntäriville. **Tee tilaukset** -toiminto luo siirtotilauksen VIHREÄ-sijainnista vaadittuun sijaintiin. **Korvaavia olemassa** -kenttä toimii samalla tavalla.  

5.  Valitse **Tee tilaukset** -toiminto. **Tee toimitustilaukset** -ikkuna avautuu.  
6.  Valitse **Tee tilaukset** -kentän **Tilauksen suunnittelu** -pikavälilehdessä **Aktiivinen tilaus**.  
7.  Valitse **Vaihtoehdot**-pikavälilehden **Luo siirtotilaus** -kentässä **Tee siirtotilaukset** -vaihtoehto.  
8.  Luo siirtotilaus myyntitilauksen toimittamista varten valitsemalla **OK**.  

     Siirtotilaus luodaan ja tallennetaan luetteloon avointen siirtotilausten luettelon viimeiseksi tilaukseksi.  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a>Monitasoisen tuotantotilauksen suunnitteleminen myyntikysynnän täyttämiseksi  
 Näissä toimintaohjeissa laaditaan suunnitelma, jossa tuotetun nimikkeen myyntikysyntä täytetään usealla tuotetasolla. Jokainen taso luo riippuvaisen tuotantokysynnän.  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a>Monitasoisen tuotannon suunnitteleminen myyntikysynnän täyttämiseksi  

1.  Valitse tilauksen numero **1001** suunnittelurivi, jolla on myyntikysyntää (se luotiin aiemmin vaihekuvauksen valmistavissa toimissa).  

     Tämä kysyntä on myyntirivi, mutta nimikkeelle on määritetty täydennysjärjestelmäksi **Tuotantotilaus**. Lisää ylimääräinen kello kunkin polkupyörän komponenttitarpeeseen.  

2.  Avaa **Suunnittelu komponentit**-ikkuna valitsemalla **Komponentit**-toiminto.  
3.  Vaihda Kello-nimikkeen rivillä **Määrä per** -kentän arvo **1** arvoksi **2**.  
4.  Harkitse suunnitteluvaihtoehtoja **Tilauksen suunnittelu** -ikkunassa. Tässä tilanteessa vaihtoehtoisia toimitustapoja &mdash; siirtoa tai korvaavaa tai myöhempää toimitusta &mdash; ei ole. Ehdotettu toimitustilaus, tuotantotilaus, on luotava.  
5.  Luo tuotantotilaus valitsemalla **Tee tilaukset** -toiminto.  

     Huomaa, että myyntitilauksen **1001** suunnitteluriviä ei enää ole **Tilauksen suunnittelu** -ikkunassa. Alustava myyntikysyntä on täytetty.  

6.  Sulje **Tilauksen suunnittelu** -ikkuna.  

     Tässä vaiheessa kaikki suunnittelutehtävät voitaisiin jäädä suorittamaan tähän näkymään. Nyt kuitenkin omaksutaan tuotantosuunnittelijan rooli, siirrytään äsken luotuun tuotantotilaukseen ja käytetään **Tilauksen suunnittelu** -ikkunaa.  

 Tuotantosuunnittelijan täytyy nyt suunnitella tietty tuotantotilaus.  

### <a name="to-plan-a-specific-production-order"></a>Tietyn tuotantotilauksen suunnitteleminen  

1.  Avaa tuotantotilaus **101001** (kymmenen polkupyörää), joka luotiin aiemmin **Tee tilaukset**-toiminnolla.  
2.  Avaa **Tuot.til. komponentit** -ikkunassa ja varmista, että ylimääräinen kello näkyy tuotantotilauksessa.  
3.  Valitse **Suunnittelu**-toiminto.  

     **Tilauksen suunnittelu** -ikkuna avautuu näkymään, joka on suodatetaan aina tiettyyn tuotannon kysyntään. Myyntikysyntä ei ole näkyvissä. Suunnitelma on laskettava, ennen kuin lisäkysyntä tulee näkyviin.  

4.  Valitse **Laske suunnitelma** -toiminto.  

     Huomaa, että neljä uutta tuotantotilausta näkyy tilauksesta **101001** johdettuna suunnittelemattomana tuotantokysyntänä. Uudet rivit vastaavat niiden alikokoonpanojen uutta tuotantokysyntää, joka täytyy luoda tilauksen tuottamista varten.  

5.  Valitse **Laajenna kaikki** -toiminto, jos haluat nähdä yleiskuvauksen tuotantotilausten koko tuotantokysynnästä.  

     Antaaksesi lisätietoja kysyntäriveistä, saatat haluta lisätä **Kysyntämäärä** ja **Käytettävissä oleva kysyntämäärä** -kenttiä näkymääsi.  

     Seuraavaksi kutakin komponenttia on toimitettava kymmenen kappaletta.  

     Huomaa, että neljällä kysyntärivillä on täydennysjärjestelmä Tuotantotilaus. Nämä neljä osakokoonpanoa edustavat polkupyörän toista tuotantotasoa.  

     Oletustäydennysasetukset on täytetty valmiiksi, ja voit aloittaa tilausten tekemisen.  

6.  Valitse **Tee tilaukset** -toiminto.  

     Ennen kuin painat **OK**-painiketta, huomioi teksti **Tilauksen suunnittelu**-pikavälilehdessä. Tämä teksti on tärkeä, koska polkupyörän tuoterakenteessa tiedetään olevan joitakin tuotettuja komponentteja eli alikokoonpanoja, joilla voisi olla kysyntää, kun luot tämän tuotantotilauksen.  

7.  Valitse **Tee toimitustilaukset** -ikkunan **Tee tilaukset**-kentässä **Kaikki rivit** ja valitse sitten **OK**, jos haluat luoda tuotantotilaukset tilauksen toiselle tuotetasolle.  

     Huomaa, että tuotantotilauksella 101001 ei enää ole ylätason tuotantokysyntää. Se merkitsee, että alikokoonpanojen alustava tuotantokysyntä on otettu huomioon suunnittelussa.  

     Suunnitelma lasketaan uudelleen **Tilauksen suunnittelu** -ikkunassa, jotta polkupyörän rakenne voidaan suunnitella.  

8.  Laske suunnitelma uudelleen upotetun ohjetekstin ohjeiden mukaisesti valitsemalla **Laske suunnitelma**.  

     Kaksi uutta riviä vastaavat ylimääräistä tuotantokysyntää, joka on johdettu edellisissä vaiheissa suunnitelluista alikokoonpanoista. Pyörän napojen toimittamiseksi ehdotetaan kahta tuotantotilausta, yhtä kymmenelle etupyörän navalle ja niin ikään yhtä kymmenelle takapyörän navalle.  

9. Valitse **Laajenna kaikki** -toiminto, jos haluat nähdä yleiskuvauksen kahden tuotantotilauksen koko tuotantokysynnästä.  

     Ehdotettu toimitussuunnitelma osoittaa, että komponenteille luodaan yhteensä neljä ostotilausta. Ehdotetut tilaukset päätetään tehdä.  

10. Valitse **Tee tilaukset** -toiminto.  
11. Valitse **Tee tilaukset** -kentässä **Kaikki rivit** ja valitse sitten **OK**. Tarkista, onko päänimikkeen eli polkupyörän (myydään myyntitilauksella 1001) tuotannolla lisäkysyntää.  
12. Valitse **Laske suunnitelma** -toiminto.  

     Sanomassa ilmoitetaan, että kaikki vaaditut nimikkeet on nyt toimitettu. Varmista sitovasti suunnitellut tuotantotilaukset, jotka on luotu.  

13. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Sitovasti suunn. tuotantotil.** ja valitse sitten aiheeseen liittyvä linkki.  

     Tarkista **Sitovasti suunn. tuotantotil.** -ikkunassa, miten yksittäisten tilausten aloitus- ja päättymisajat on ajoitettu tuoterakenteen mukaan. Alimman tason komponentit tuotetaan ensin. Monitasoisten tilausten suunnitteleminen onkin tärkeää, kuten tässä suunnittelun työnkulussa on havainnollistettu.  

## <a name="see-also"></a>Katso myös  
 [Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)   
 [Vaihekuvaus: Toimitusten automaattinen suunnittelu](walkthrough-planning-supplies-automatically.md)

