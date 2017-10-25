---
title: "Rakennetiedot – Tarjonnan täsmäytys kysynnällä | Microsoft Docs"
description: "Suunnittelujärjestelmän ydin vaatii kysynnän ja tarjonnan tasapainotusta ehdottamalla käyttäjän toimenpiteitä tarkastamaan varastotilaukset epätasapainon välttämiseksi. Tämä tapahtuu variantin ja sijainnin yhdistelmän perusteella."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 76654f0390ef922f5a065e00b566e8876dbbaebc
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-balancing-supply-with-demand"></a>Rakennetiedot: tarjonnan täsmäytys kysynnällä
Suunnittelujärjestelmän ydin vaatii kysynnän ja tarjonnan tasapainotusta ehdottamalla käyttäjän toimenpiteitä tarkastamaan varastotilaukset epätasapainon välttämiseksi. Tämä tapahtuu variantin ja sijainnin yhdistelmän perusteella.  
  
Kuvittele, että jokainen varastoprofiili sisältää kysyntätapahtumien joukon (lajiteltuna päivämäärän ja prioriteetin mukaan) ja vastaavan tarjontatapahtumien joukon. Jokainen tapahtuma viittaa takaisin sen lähdetyyppiin ja tunnukseen. Nimikkeen tasapainotussäännöt ovat suoraviivaiset. Prosessin missä tahansa vaiheessa voi ilmetä neljä kohdistetun kysynnän ja tarjonnan esiintymää:  
  
1.  Nimikkeellä ei ole kysyntää tai tarjontaa = > suunnittelu on päättynyt (tai sen ei pitäisi käynnistyä).  
2.  Kysyntä on olemassa mutta ei ole tarjontaa => tarjontaa tulee ehdottaa.  
3.  Tarjonta on olemassa mutta sille ei ole kysyntää => tarjonta tulee peruuttaa.  
4.  Sekä kysyntä että tuotanto on olemassa = > kysymyksiin tulee vastata ennen kuin järjestelmä voi varmistaa, että kysyntä täyttyy ja tuotanto on riittävä.  
  
     Jos toimituksen ajankohta ei ole sopiva, ehkä toimitus voidaan aikatauluttaa uudelleen seuraavasti:  
  
    1.  Jos tarjonta on asetettu kysyntää aiemmin, tarjonta voidaan ehkä aikatauluttaa uudelleen niin, että varasto on mahdollisimman pieni.  
    2.  Jos tarjonta tapahtuu kysyntää ennen, tarjonnan voi mahdollisesti aikatauluttaa uudelleen. Muussa tapauksessa järjestelmä ehdottaa uutta tarjontaa.  
    3.  Jos tarjonta vastaa kysyntää kyseisenä päivämääränä, suunnittelujärjestelmä voi tutkia edelleen, voiko tarjonnan määrä kattaa kysynnän.  
  
     Kun ajoitus on valmis, riittävä toimitettava määrä voidaan laskea seuraavasti:  
  
    1.  Jos tarjonnan määrä on pienempi kuin kysyntä, on mahdollista, että tarjonnan määrää voidaan kasvattaa (tai ei, jos vähimmäismääräkäytäntö rajoittaa sitä).  
    2.  Jos tarjonnan määrä on suurempi kuin kysyntä, on mahdollista, että tarjonnan määrää voidaan vähentää (tai ei, jos vähimmäismääräkäytäntö rajoittaa sitä).  
  
     Tässä vaiheessa on olemassa yksi näistä kahdesta tilanteesta:  
  
    1.  Nykyiseen kysyntään voidaan vastata, jolloin se voidaan sulkea ja seuraavan kysynnän suunnittelu voidaan aloittaa.  
    2.  Tarjonta on saavuttanut enimmäismäärän, ja osa kysyntämäärästä on jäänyt kattamatta. Tässä tapauksessa suunnittelujärjestelmä voi sulkea nykyisen tarjonnan ja siirtyä seuraavaan.  
  
Toimenpide alkaa tyypillisesti seuraavasta kysynnästä ja nykyisestä tarjonnasta tai päinvastoin. Nykyinen tarjonta voi pystyä kattamaan myös tämän seuraavan kysynnän tai nykyiseen kysyntään ei ole vielä täysin vastattu.  
  
## <a name="rules-concerning-actions-for-supply-events"></a>Säännöt, jotka koskevat toimitustapahtumien toimintoja  
Kun suunnittelujärjestelmä suorittaa ylhäältä alaspäin tehtävän laskennan, jossa tarjonnan on täytettävä kysyntä, kysyntä saadaan muualta valmiina, eikä suunnittelujärjestelmä valvo sitä. Tarjontapuolta voidaan kuitenkin hallita. Tämän vuoksi suunnittelujärjestelmä ehdottaa uuden toimitustilauksen luomista, olemassa olevien uudelleenajoittamista ja/tai tilausmäärän muuttamista. Jos olemassa oleva toimitustilaus muuttuu tarpeettomaksi, suunnittelujärjestelmä ehdottaa, että käyttäjä peruuttaa sen.  
  
Jos käyttäjä haluaa jättää pois olemassa olevan toimitustilauksen suunnitteluehdotuksista, hän voi ilmoittaa, että sillä ei ole suunnittelun joustavuutta (suunnittelun joustavuus = ei mitään). Tilauksen ylimääräinen tarjonta käytetään kysynnän kattamisessa, mutta toimintoa ei ehdoteta.  
  
Yleisesti koko tarjonnalla on suunnittelun joustavuus, jota rajoittaa jokaisen ehdotetun toiminnon ehdot.  
  
-   **Aikatauluta uudelleen ulos**: olemassa olevan toimitustilauksen päivämäärä voidaan aikatauluttaa ulos, jotta se vastaa kysynnän eräpäivää, ellei:  
  
    -   Se kuvaa varastoa (aina päivänä nolla).  
    -   Sillä on tilausten välinen linkki toiseen kysyntään.  
    -   Se on aikavälin määrittämän uudelleenaikataulutuksen ikkunan ulkopuolella.  
    -   Voit käyttää myös paremmin sopivaa tarjontaa.  
    -   Toisaalta käyttäjä voi päättää, että aikataulutusta ei suoriteta uudelleen, koska:  
    -   Toimitustilaus on jo sidottu edellisen päivän toiseen kysyntään.  
    -   Tarvittu uudelleenaikataulutus on niin minimaalinen, että käyttäjä katsoo sen merkityksettömäksi.  
  
-   **Aikatauluta uudelleen sisään**: olemassa olevan toimitustilauksen päivämäärä voidaan aikatauluttaa sisään lukuun ottamatta seuraavia olosuhteita:  
  
    -   Se on linkitetty suoraan johonkin toiseen kysyntään.  
    -   Se on aikavälin määrittämän uudelleenaikataulutuksen ikkunan ulkopuolella.  
  
> [!NOTE]  
>  Kun suunnitellaan uusintatilauspistettä käyttävää nimikettä, toimitustilaus voidaan ajoittaa tarvittaessa, Tämä on normaalia eteenpäin ajastetuille toimitustilauksille, jotka uusintatilauspiste käynnistää.  
  
-   **Kasvatusmäärä**: olemassa olevan toimitustilauksen määrää voidaan kasvattaa vastaamaan kysyntää, ellei toimitustilausta linkitetä suoraan kysyntään tilausten välisellä linkillä.  
  
> [!NOTE]  
>  Vaikka toimitustilausta on mahdollista kasvattaa, se voi olla rajoitettu määritetyn enimmäistilausmäärän vuoksi.  
  
-   **Vähennysmäärä**: aiemmin luodun toimitustilauksen määrä, joka on ylijäämäinen verrattuna olemassa olevaan kysyntään, on vähennettävissä kysynnän täyttämiseksi.  
  
> [!NOTE]  
>  Vaikka määrää on mahdollista vähentää, kysyntäarvoon verrattuna saattaa vielä olla ylijäämää määritetystä vähimmäistilausmäärästä tai tilauskerrannaisesta johtuen.  
  
-   **Peruuta**: erityinen vähennä määrää -toiminnon tapahtuma, toimitustilaus voidaan peruuttaa, jos se on vähentynyt nollaan.  
-   **Uusi**: jos toimitustilausta ei ole jo olemassa tai olemassa olevaa ei voida muuttaa täyttämään tarvittavaa määrää vaadittuna eräpäivänä, järjestelmä ehdottaa uutta toimitustilausta.  
  
## <a name="determining-the-supply-quantity"></a>Tarjonnan määrän määrittäminen  
Käyttäjän määrittämät suunnitteluparametrit ohjaavat jokaisen toimitustilauksen ehdotettua määrää.  
  
Kun suunnittelujärjestelmä laskee uuden toimitustilauksen määrän tai olemassa olevan tilauksen määrä muuttuu, ehdotettu määrä voi olla eri kuin alkuperäisen kysynnän määrä.  
  
Jos enimmäisvarasto tai kiinteä tilausmäärä on valittuna, järjestelmä saattaa kasvattaa ehdotettua määrää tämän kiinteän määrän tai enimmäisvaraston täyttämiseksi. Jos uusintatilaustapa käyttää uusintatilauspistettä, määrää voidaan kasvattaa vähintään uusintatilauspisteen täyttämiseksi.  
  
Ehdotettua määrää voidaan muokata tässä sarjassa:  
  
1.  Alaspäin enimmäistilausmäärään (jos sellainen on).  
2.  Ylöspäin seuraavaan tilausmäärään.  
3.  Ylöspäin seuraavaan tilauskerrannaisen. (Jos asetukset ovat virheelliset, tämä voi vahingoittaa enimmäistilausmäärä.)  
  
## <a name="order-tracking-links-during-planning"></a>Tilauksen seurantalinkit suunnittelun aikana  
Suunnittelun aikaiseen tilauksen seurantaan liittyen on tärkeää mainita, että suunnittelujärjestelmä järjestää uudelleen dynaamisesti luodut tilauksen seurantalinkit nimike/variantti/sijainti-yhdistelmille.  
  
Tälle on kaksi syytä:  
  
-   Suunnittelujärjestelmän täytyy pystyä osoittamaan ehdotuksensa oikeiksi; että kaikki kysyntä katetaan ja että toimitustilukset ovat tarpeettomia.  
-   Dynaamisesti luodut tilauksen seurantalinkit on täsmäytettävä uudelleen säännöllisesti.  
  
Ajan myötä dynaamisen tilauksen seurannan linkit ovat epätasapainossa, koska koko tilauksen seurantaverkko järjestetään uudelleen, kunnes kysyntä tai tarjonta suljetaan.  
  
Ennen tarjonnan ja kysynnän täsmäytystä ohjelma poistaa kaikki olemassa olevat tilauksen seurantalinkit. Kun kysyntä- tai tarjontatapahtuma on suljettu, täsmäytyksen aikana muodostetaan uudet tilauksen seurantalinkit kysynnän ja tarjonnan välille.  
  
> [!NOTE]  
>  Vaikka nimikettä ei ole asetettu dynaamiseen tilauksen seurantaan, suunnittelujärjestelmä luo täsmäytetyt tilauksen seurantalinkit yllä kuvatulla tavalla.  
  
## <a name="see-also"></a>Katso myös  
[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md)   
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)
