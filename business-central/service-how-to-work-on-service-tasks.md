---
title: Huoltotehtävien käsitteleminen
description: Tässä aiheessa käsitellään erilaisia tapoja käsitellä huoltotehtäviä. Huoltotehtävät-sivulla on yleiskuvaus toimenpiteitä edellyttävistä huoltonimikkeistä.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="work-on-service-tasks"></a>Huoltotehtävien käyttäminen
Kun huoltotilaukset tai huoltotarjoukset on luotu, huoltonimikerivit rekisteröity ja resurssit on kohdistettu tilausten tai tarjousten huoltonimikkeille, huoltonimikkeiden korjauksen ja ylläpidon voi aloittaa.  

[!INCLUDE[prod_short](includes/prod_short.md)] sisältää **Huoltotehtävät**-sivun, jossa yleiskuvaus toimenpiteitä edellyttävistä huoltonimikkeistä. Ikkuna toimii huollon mittareina, joiden avulla voit nähdä odottavat tilaukset, etsiä ja rekisteröidä varaosia sekä pitää varaston ajan tasalla.  

Voit seurata huollon muutoksia sekä tarkastella huollon graafista näkyvää [!INCLUDE[prod_short](includes/prod_short.md)]:n tilastotyökalujen avulla, jotka luovat kaavoja ja analyyseja nopeasti ja automaattisesti.  

## <a name="to-work-on-a-service-task"></a>Huoltotehtävien parissa työskenteleminen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotehtävät** ja valitse sitten vastaava linkki.
2. Jos haluat nähdä luettelon huoltotehtävistä, joihin tietty resurssi tai resurssiryhmä on kohdistettu, täytä **Resurssisuodatus**- tai **Resurssiryhmän suodatus** -kenttä ja paina <kbd>Enter</kbd>-näppäintä.  
3. Jos haluat nähdä luettelon huoltotehtävistä, joiden vastauspäivämäärä tai -päivämäärät ovat tietyn aikajakson sisällä, täytä **Vastauspvm suodatus** -kenttä ja paina <kbd>Enter</kbd>-näppäintä.  
4. Jos haluat nähdä luettelon huoltotehtävistä, joilla on jokin tietty kohdistuksen tai korjauksen tila, täytä **Kohdistuksen tilan suodatus**- tai **Korjaustilakoodin suodatus** -kenttä ja paina <kbd>Enter</kbd>-näppäintä.  
5. Valitse huoltotehtävä, jota haluat työstää. Valitse **Nimikkeen työkirja** -toiminto. **Huoltonimikkeen työkirja** -sivu avautuu.  
6. Rekisteröi vakiotekstit, varaosat, resurssitunnit ja kustannukset käyttämällä **Tyyppi**-kentän vaihtoehtoja: \<Blank\>, **Nimike**, **Resurssi** ja **Kustannus**.  
7. Valitse **Korjauksen tila**-kentässä asianmukainen tila.  

   > [!NOTE]  
   >  Määritä **Korjauksen tila** -kenttään tilaksi  **Valmis** tai **Osittain huollettu**, jos huoltonimike on huollettu kokonaan tai huoltoa jatkaa toinen resurssi. Ohjelma valitsee huoltonimikkeen kohdistustapahtuman tilaksi automaattisesti  **Valmis** tai **Uudelleenkohdistamista tarvitaan**.  

## <a name="to-register-service-operations"></a>Huoltotoimintojen rekisteröiminen
Kun suoritat huoltotilauksen huoltoa, voit rekisteröidä käytetyt nimikkeet, aiheutuneet kustannukset ja kuluneen ajan määrittävät tiedot. Ohjelma tallettaa **Huoltonimikkeen työkirja** -sivulla määrittämäsi tiedot. Voit päivittää tietoja tarvittaessa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 2.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotilaukset** ja valitse sitten vastaava linkki.  
2. Avaa huoltotilaus, johon haluat rekisteröidä huollon, ja valitse nimikerivi.  
3. Valitse **Huoltonimiketyökirja**-toiminto  
4. Määritä riveillä käytetyt nimikkeet, aiheutuneet kustannukset ja huoltoon käytetty aika.  

   > [!NOTE]  
   >  Voit rekisteröidä huollon myös suoraan huoltotilaukseen linkitetyillä huoltoriveillä.  

## <a name="to-register-spare-parts"></a>Varaosien rekisteröiminen
Kun työskentelet huoltotilauksissa olevien huoltonimikkeiden parissa, voit tarvita huoltoa varten varaosia. Seuraavassa kuvataan, miten käyttämäsi varaosat rekisteröidään **Huoltonimikkeen työkirja** -sivulla.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotehtävät** ja valitse sitten vastaava linkki.
2. Valitse ensin huoltonimikkeen sisältävä rivi ja sitten **Nimikkeen työkirja** -toiminto.  
3. Määritä uusi huoltorivi.  
4. Valitse **Tyyppi**-kentässä **Nimike**.  
5. Valitse **Nro**-kenttään sopiva varaosa.  
6. Syötä **Määrä**-kenttään määrä nimikkeistä, joita haluat käyttää.  

 Samalla tavoin voidaan rekisteröidä varaosia **Huoltorivit**-sivulla, jonka voit avata **Huoltotilaus**-sivulta.  

## <a name="to-register-spare-parts-from-a-service-order"></a>Rekisteröi varaosat huoltotilauksesta
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotilaukset** ja valitse sitten vastaava linkki.  
2. Avaa huoltotilaus, jolle haluat rekisteröidä varaosat.  
3. Valitse rivi, joka sisältää käsiteltävän huoltonimikkeen. Valitse ensin **Toiminnot**, sitten **Tilaus** ja lopuksi **Huoltorivit**.  
4. Anna uusi huoltorivi.  

## <a name="to-replace-a-service-item-or-a-service-item-component"></a>Huoltonimikkeen tai huoltonimikkeen komponentin korvaaminen
Kun huolletaan komponenteista koostuvaa huoltonimikettä, viallinen komponentti voidaan joutua vaihtamaan uuteen. Joka kerta, kun komponentteja sisältävälle huoltonimikkeelle syötetään varaosa, ohjelma antaa valita komponentin vaihtamisen tai uuden komponentin luomisen välillä. Ohjelma ei rekisteröi uutta nimikettä huoltonimikkeen komponentiksi, ennen kuin tämä huoltorivi tai huoltotilaus kirjataan.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 5.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotehtävät** ja valitse sitten vastaava linkki.
2. Valitse ensin huoltonimikkeen sisältävä rivi ja sitten **Nimikkeen työkirja** -toiminto.  
3. Anna uusi huoltorivi.  
4. Valitse **Tyyppi**-kentässä **Nimike**.  
5. Valitse **Nro**-kenttään korvattava komponentti.  
6. Valitse <kbd>Enter</kbd>-näppäin. Näyttöön tulee valintaikkuna, jossa on kolme vaihtoehtoa: **Vaihda komponentti**,  **Uusi komponentti** ja **Jätä huomiotta**. Asetukset kuvaillaan seuraavassa taulukossa.  

    |Asetus | Description|  
    |----------------------------------|---------------------------------------|  
    |**Korvaa osa**|Ohjelma muuttaa muuksi kuin aktiiviseksi sen komponentin tilan, jota olet vaihtamassa. Komponentti tulee näkyviin huoltonimikkeen vaihdettujen komponenttien luetteloon.|  
    |**Uusi komponentti**|Ohjelma syöttää uuden komponentin huoltonimikkeen komponenttiluetteloon.|  
    |**Ohita**|Ohjelma ei tee mitään huoltonimikkeen komponenttiluettelolle.|  

7. Valitse **Vaihda komponentti**.  
8. Valitse ensin korvattava komponentti ja sitten **OK**.  

## <a name="to-change-the-response-time-for-a-service-item-line"></a>Huoltonimikerivin vastausajan muuttaminen
Kun huoltonimikerivi rekisteröidään huoltotilaukseen tai -tarjoukseen ja jos huoltonimike on huoltosopimuksessa, automaattinen oletusvastausaika annetaan vastauspäivämäärä ja -aika lasketaan sen mukaisesti. Vastausajan tuntimäärää sekä vastauspäivämäärää ja -aikaa voi muuttaa tarpeen mukaan.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 6.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotilaukset** tai **Huoltotarjoukset** ja valitse sitten vastaava linkki.  
2. Avaa kortti valitsemalla huoltotilaus tai -tarjous.  
3. Anna sen huoltonimikkeen rivillä, jonka vastausajan haluat muuttaa, joko **Vastausaika (tuntia)** -kentässä tai **Vastauspvm**- ja **Vastausaika**-kentissä uusi vastausaika tunteina tai vastauspäivämäärä ja -aika.  

## <a name="to-register-faultresolution-codes"></a>Vika-/ratkaisukoodien rekisteröiminen
Huoltonimikkeen korjauksen jälkeen nimikkeelle voi rekisteröidä sekä vikakoodin että ratkaisukoodin valitsemalla yhdistelmän olemassa olevista vika-/ratkaisukoodien suhteista. Vika- ja ratkaisukoodit tulevat näkyviin vastaaviin kenttiin **Huoltonimikkeen työkirja** -sivulla. Koodit voi rekisteröidä myös suoraan tällä sivulla.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 7.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotehtävät** ja valitse sitten vastaava linkki.
2. Valitse ensin huoltonimikkeen sisältävä rivi ja sitten **Nimikkeen työkirja** -toiminto.  
3. Valitse **Huoltonimikkeen työkirja** -sivulla **Vika-/ratkaisukoodien suhteet**. **Vika-/ratkaisukoodien suhteet** -sivu avautuu.  

  >  [!NOTE]
  >  Ohjelma asettaa automaattisesti suodatuksia näyttämilleen suhteille kopioimalla huoltonimikeryhmän ja vikakoodit **Huoltonimikkeen työkirja** -sivulta.  

4. Täytä rivi. Valitse oikea vika- ja ratkaisukoodien yhdistelmä ja kopioi se sitten huoltonimikkeeseen valitsemalla **OK**. Jos sopivaa yhdistelmää ei löydy, sivulla voi luoda uuden yhdistelmän.  

## <a name="see-also"></a>Katso myös
[Vian raportoinnin määrittäminen](service-how-setup-fault-reporting.md)
[Kohdistuksen tila ja korjauksen tila](service-allocation-status-and-repair-status.md)  
[Huollon kirjaus](service-service-posting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
