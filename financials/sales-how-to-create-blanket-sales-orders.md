---
title: Puitemyyntitilauksien luominen | Microsoft Docs
description: "Käytä puitetilauksia, kun asiakas on päättänyt ostaa suuria määriä, jotka toimitetaan useissa pienissä toimituserissä määritetyn aikajakson sisällä."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0b91925a7ec6adb40cdf99d5bcf3398b62c28b3f
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-blanket-sales-orders"></a>Toimintaohje: Puitemyyntitilausten käyttäminen
Puitemyyntitilaus kuvastaa yrityksesi ja asiakkaan välisen pitkäaikaisen sopimuksen runkoa.

Puitetilaus tehdään yleensä silloin, kun asiakas on päättänyt ostaa suuria määriä, jotka toimitetaan useissa pienissä toimituserissä määritetyn aikajakson sisällä. Puitetilaukset kattavat usein vain yhden nimikkeen ja ennalta määritetyt toimituspäivämäärät. Pääsyy puitetilauksen käytölle myyntitilauksen käytön sijaan on se, että puitetilaukseen syötetyt määrät eivät vaikuta nimikkeen saatavuuteen, eli niitä voidaan käyttää valvonnan, ennustamisen ja suunnittelun lomakkeina.

Puitetilauksen jokainen erillinen toimitus voidaan määrittää tilausriviksi, joka voidaan toimitushetkellä muuntaa myyntitilaukseksi.

Esimerkki puitetilauksen käytöstä: Asiakas soittaa ja tilaa nimikettä 1 000 yksikköä. Asiakas haluaa, että nimikkeet toimitetaan 250 yksikön viikkoerissä seuraavan kuukauden aikana.

> [!NOTE]
> Puiteostotilaukset toimivat samoin kuin puitemyyntitilaukset. Näissä ohjeissa ei käsitellä puiteostotilauksia.

## <a name="to-create-a-blanket-sales-order"></a>Uuden puitemyyntitilauksen luominen  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Puitemyyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Uusi**-toiminto.  
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Jätä **Tilauspvm**-kenttä tyhjäksi. Kun puitetilauksesta luodaan erillisiä myyntitilauksia, ohjelma määrittää myyntitilauksen tilauspäivämääräksi todellisen käsittelypäivämäärän.
5. Luo **Rivit**-pikavälilehdessä erilliset rivit jokaista toimitusta varten. Jos asiakas haluaa esim. 1 000 yksikköä niin, että ne on jaettu tasaisesti neljälle viikolle, sinun on syötettävä neljä erillistä riviä, joilla jokaisella on 250 yksikköä.   

## <a name="to-create-a-sales-order-from-a-blanket-sales-order"></a>Myyntitilauksen luominen puitemyyntitilauksesta  

1.  Voit luoda tilauksen mille tahansa puitekokoonpanotilauksen riveille poistamalla kaikkien niiden rivien **Toimitettava määrä** -kentän määrä, joita ET halua toimittaa tällä kertaa.  
2.  Kun olet valmis luomaan tilauksia, valitse ensin **Tee tilaus** -toiminto ja sitten **Kyllä**. Näyttöön tulee sanoma, jossa kerrotaan puitetilauksen määrityksestä tilausnumeroon. Huomaa, että puitetilausta ei ole poistettu.  
3.  Valitse **OK**-painike.  
4.  Voit tuoda edellisten vaiheiden tulokset näkyviin valitsemalla ensin **Rivi**-toiminnon, sitten **Kirjaamattomat rivit** -toiminnon ja lopuksi **Tilaukset**-toiminnon.  
5.  Valitse ensin oikea myyntitilaus **Myyntirivit**-ikkunassa, sitten **Rivit**-toiminto ja lopuksi **Näytä asiakirja** -toiminto.  

Seuraava koskee myyntitilauksia sen jälkeen, kun ne on luotu puitemyyntitilauksista.  

- Puitetilauksen myyntitilaukseksi muuntamisen jälkeen myyntitilaus sisältää kaikki puitetilauksen rivit. Rivit, joiden **Toimitettava määrä** -kentän määrä poistettiin, tulevat näkyviin, mutta niiden **Määrä**-kentät ovat tyhjiä. Voit jättää tai poistaa rivit tai muokata niitä.  
- On tärkeä muistaa, että myyntitilausrivin määrä ei saa ylittää liitetyn puitetilausrivin määrää. Muussa tapauksessa myyntitilauksen kirjaus ei onnistu.  
- Kun myyntitilaus on kirjattu toimitettuna ja/tai laskutettuna, ohjelma päivittää liittyvän puitetilauksen **Toimitettu määrä**- ja **Laskutettu määrä** -kentät.  
- Ohjelma tallentaa puitetilausnumeron ja rivinumeron ominaisuuksina myyntiriveille, kun ne luodaan puitetilauksesta.  
- Jos myyntitilauksia ei luoda suoraan puitetilauksesta, mutta se liittyy puitetilaukseen, myyntitilauksen ja puitetilauksen välille voidaan muodostaa linkki syöttämällä liittyvän puitetilauksen numero myyntitilausrivin **Puitetilauksen nro** -kenttään.  
- Kun myyntitilaus on luotu puitetilauksen rivien kokonaismäärällä, muita myyntitilauksia ei voi luoda samalle riville. Käyttäjät eivät voi syöttää määrää **Toimitettava määrä** -kenttään. Jos puitetilaukseen täytyy kuitenkin lisätä määriä, voit kasvattaa **Määrä**-kentän arvoa. Sen jälkeen voit luoda lisätilauksia.  
- Laskutettu puitemyyntitilaus säilytetään järjestelmässä, kunnes se poistetaan yksittäisiä puitemyyntitilauksia poistettaessa tai suoritettaessa **Poista virheelliset puitemyyntitilaukset** -eräajo.  
- Jos asiakas on tallennettu myös kontaktina Markkinointi-kohdistusalueeseen ja jos olet määrittänyt puitemyyntitilauksille vuorovaikutusmallin koodin  **Kontaktienhallinnan asetukset** -ikkunassa, ohjelma tallentaa vuorovaikutuksen automaattisesti, kun tulostat puitemyyntitilauksen valitsemalla Vuorovaikutuslokin tapahtuma -taulukossa **Tulosta**.

## <a name="to-view-the-status-of-a-blanket-purchase-order"></a>Puiteostotilausten tilan katsominen  
Voit nähdä puiteostotilauksen tilan **Ostopuitetilauksen tilastot** -ikkunassa. Tällä voi olla merkitystä, kun aletaan laskuttaa tilausta, joka luotiin puiteostotilauksesta.  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Puiteostotilaukset** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse ensin puiteostotilaus ja valitse sitten **Tilastot**-toiminto.  
3.  **Ostopuitetilauksen tilastot** -ikkunan **Yleinen**-pikavälilehdessä voit tarkastella koko tilauksen yhteenvetotietoja puiteostotilauksen rivien eri **Määrä-kenttien** yhteismäärän perusteella.  

    - **Laskutus**-pikavälilehdessä voit tarkastella yhteenvetotietoja puiteostotilauksen rivien **Laskutettava määrä** -kenttien yhteismäärän perusteella.  
    - **Toimitus**-pikavälilehdessä voit tarkastella yhteenvetotietoja puiteostotilauksen rivien **Vastaanotettava määrä** -kenttien yhteismäärän perusteella.  
    - **Ennakkomaksu**-pikavälilehdessä voit tarkastella yhteenvetotietoja mahdollisista ennakkoon maksetuista summista.  
    - **Toimittaja**-pikavälilehdessä voit tarkastella toimittajaa koskevia perustietoja.    

## <a name="to-view-unposted-and-posted-blanket-sales-order-lines"></a>Kirjaamattomien ja kirjattujen puitemyyntitilausrivien näyttäminen   
Linkki puitemyyntitilauksen ja alkuperäisen myyntiasiakirjan, sekä kaikkien muiden myyntiasiakirjojen välillä säilytetään kirjaamisen jälkeen luettelona kirjatuista ja kirjaamattomista myyntitilauksen laskuriveistä.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Puitemyyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa tarkasteltava puitemyyntitilaus.
3. Näytä kirjaamattomat tapahtumat valitsemalla ensin kyseinen rivi, sitten **Rivi**-toiminto ja lopuksi **Kirjaamattomat rivit** -toiminto. Valitse yksi seuraavista vaihtoehdoista.  

    <table>
    <tr>
    <th>Asetus</th>
    <th>Description</th>
    </tr>
    <tr>
    <td>**Tilaukset**</td>
    <td>Määrittää avoimet tilaukset, jotka on merkitty liittyviksi valittuun riviin.</td>
    </tr>
    <tr>
    <td>**Laskut**</td>
    <td>Määrittää avoimet laskut, jotka on merkitty liittyviksi valittuun riviin. Avoimet laskut on liitetty manuaalisesti puitetilaukseen syöttämällä puitetilauksen numero myyntilaskuriville.</td>
    </tr>
    <tr>
    <td>**Palautustilaukset**</td>
    <td>Määrittää avoimet palautustilaukset, jotka on merkitty liittyviksi valittuun riviin.</td>
    </tr>
    <tr>
    <td>**Hyvityslaskut**</td>
    <td>Määrittää avoimet hyvityslaskut, jotka on merkitty liittyviksi valittuun riviin.</td>
    </tr>
    </table>
4. Näytä kirjatut tapahtumat valitsemalla ensin kyseinen rivi, sitten **Rivi**-toiminto ja lopuksi **Kirjatut rivit** -toiminto. Valitse yksi seuraavista vaihtoehdoista.  

    <table>
    <tr>
    <th>Asetus</th>
    <th>Description</th>
    </tr>
    <tr>
    <td>**Toimitukset**</td>
    <td>Valittuun riviin liitetyt kirjatut toimitukset.</td>
    </tr>
    <tr>
    <td>**Laskut**</td>
    <td>Valittuun riviin liitetyt kirjatut laskut.</td>
    </tr>
    <tr>
    <td>**Palautusvast.otot**</td>
    <td>Valittuun riviin liitetyt kirjatut palautusvastaanotot.</td>
    </tr>
    <tr>
    <td>**Hyvityslaskut**</td>
    <td>Valittuun riviin liitetyt kirjatut hyvityslaskut.</td>
    </tr>
    </table>
5. Näytä tapahtuma valitsemalla **Näytä asiakirja** -toiminto **Myyntirivit**-ikkunassa.

## <a name="see-also"></a>Katso myös
[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

