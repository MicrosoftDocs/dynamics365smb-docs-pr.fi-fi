---
title: Huoltojen laskujen ja hyvityslaskujen luominen
description: Tietoja huollon laskujen ja hyvityslaskujen luomisesta.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Huolto- ja hyvityslaskujen luominen

Huoltotilausten laskuttamisen helppous on yksi [!INCLUDE[prod_short](includes/prod_short.md)]:n tärkeimmistä ominaisuuksista. [!INCLUDE[prod_short](includes/prod_short.md)] voidaan määrittää siten, että huoltoteknikko voi luoda laskun kentällä, vaikka palvelua ei olisikaan liitetty sopimukseen tai tilaukseen. Vaihtoehtoisesti voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman niin, että laskutat huoltosopimukset jaksoittain. Kunkin sopimuksen laskutusjakso määrää, kuinka usein sopimus laskutetaan.

## Useiden huoltosopimusten laskuttaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luo huoltosopimuslaskuja** ja valitse sitten vastaava linkki.  
2. Määritä käytettävät suodattimet.  
3. Anna **Kirjauspvm**-kenttään päivämäärä, jota haluat käyttää huoltolaskujen kirjauspäivämääränä.  
4. Anna **Lasku pvm:ään asti** -kenttään päivämäärä, johon asti haluat laskuttaa sopimuksia. Eräajoon sisällytetään sopimukset, joiden seuraava laskutuspäivämäärä on ennen tätä päivämäärää.  
5. Valitse **Toiminto**-kentässä **Luo laskut**.  
6. Luo huoltolaskut valitsemalla **OK**.  
  
Huoltosopimus voidaan laskuttaa myös suoraan **Huoltosopimus**-sivulta, jos sopimuksen seuraava laskutuspäivämäärä on aikaisempi kuin käsittelypäivämäärä.

## Huoltosopimuksen laskuttaminen Huoltosopimus -ikkunassa   

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltosopimukset** ja valitse sitten vastaava linkki.  
2. Valitse laskutettava huoltosopimus ja avaa sopimuksen kortti.  
3. Valitse **Luo huoltolasku** -toiminto. 
4. Luo huoltolaskut valitsemalla **Kyllä**.  
  
  > [!NOTE]  
  > Et voi luoda huoltosopimuksen huoltolaskuja, kun **Muuta tilaa** -kentän arvoksi on määritetty **Avoin**.  

## Kulutuksen kirjaaminen huoltotilauksesta  

Seuraavaksi kuvataan, miten asiakkaalta veloitettava huollon osa määritetään.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotilaukset** ja valitse sitten vastaava linkki.  
2. Valitse laskutettava huoltotilaus ja avaa tilauksen kortti.  
3. Valitse **Huoltorivit**-toiminto.  
4. Etsi tarvittavat tapahtumat ja määritä sitten **Laskutettava määrä** -kentässä määrät, jotka veloitat asiakkaalta.  
  
   > [!NOTE]  
   > Voit laskuttaa asiakasta rekisteröidystä palvelusta joko kokonaan tai osissa. Jos asiakkaalle halutaan lähettää lasku koko summasta, **Laskutettava määrä**- ja **Määrä**-kentän arvon on oltava sama. Voit lähettää koko laskun yhdessä koko lähetyksen kanssa ja voit kirjata täyden laskun jo aiemmin kirjatulle koko toimitukselle, jota ei ole laskutettu eikä käytetty.  
   >  
   > Voit määrittää laskun määrän kahdella eri tavalla, kun kirjaat osittaisen laskun. Jos aiot kirjata huollon **Toimitus ja lasku**-vaihtoehdon kanssa, **Laskutettava määrä** -kentän arvon on oltava sama kuin **Toimitettava määrä** -kentän arvo. Jos haluat laskuttaa aiemmin kirjatun toimituksen, laskun määrä ei saa olla suurempi kuin **Toimitettu määrä** -kentän arvo.  
  
5. Valitse ensin **Kirjaa** ja sitten joko **Lasku** tai **Toimitus ja lasku**. Lisätietoja on kohdassa [Kirjaaminen huollonhallinnassa](service-service-posting.md).  
  
 Valittu huoltorivi kirjataan. Voit kirjata useita huoltorivejä samanaikaisesti valitsemalla ensin ne kaikki ja sitten **Kirjaus**. Jos teet näin, varmista, että kaikkien kirjattavien rivien tarvittavat tiedot on täytetty.  
  
 Kun kirjaat tilauksen ilman **Lasku**-valintaa, ohjelma luo kirjatun huoltolaskun sekä vastaavat tapahtumat ja päivittää tilauksen huoltorivien kentät. Lisäksi aiemmin kirjatut toimitusasiakirjat päivitetään laskutetuilla määrillä. Jos valitset **Toimitus ja lasku** -kirjausvalinnan, ohjelma luo myös kirjatun toimituksen.

## Huoltolaskun luominen manuaalisesti  

Tavallisesti kun kirjaat huoltotilauksen **Lasku**- tai **Toimitus ja lasku** -valinnan kanssa, ohjelma luo automaattisesti kirjatun huoltolaskun. Silti on ehkä luotava lasku, jota ei ole linkitetty huoltosopimukseen tai huoltotilaukseen. Työvaiheessa kerrotaan, miten lasku luodaan, samalla kun asiakas vastaanottaa huollon.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltolaskut** ja valitse sitten vastaava linkki.  
2. Luo uusi huoltolasku.  
3. Syötä **Nro** -kentässä.  
  
    > [!NOTE]  
    >  Jos taas olet määrittänyt huoltolaskuille numerosarjan **Huoltohallinnon asetukset** -sivulla, voit valita seuraavan saatavilla olevan laskunumeron **Enter**-näppäimellä.  
  
4. Syötä **Asiakasnro** -kentässä asiakkaan tunnus. Valitse asiamukainen asiakas luettelosta.  
  
    Ohjelma täyttää automaattisesti asiakkaaseen liittyvät kentät tiedoilla **Asiakas**-kortilta.  
  
5. Syötä päivämäärä **Kirjauspvm.**-kenttään. Tämä kenttä näkyy kirjatuissa tapahtumissa. Tämä kenttä näyttää nykyisen työpäivämäärän, mutta sitä voidaan muuttaa.  
6. Syötä **Asiakirjan pvm** -päivämäärä, joka näkyy tulostetussa laskussa ja jonka lasketaan eräpäivä.  
7. Täytä laskun huoltorivit. Rekisteröi huollossa käytetyt nimikkeet, resurssit ja/tai kustannukset täyttämällä **Tyyppi**-, **Nro**- ja **Määrä**-kenttä.

## Voit luoda laskun, joka yhdistää kirjatut toimitusrivit yhdestä tai useammasta huoltotilauksesta 

Voit luoda huoltolaskun huollolle, joka on jo toimitettu (huoltotilauksista) mutta jota ei ole vielä laskutettu tai kulutettu. Ohjelma mahdollistaa tietyn asiakkaan laskurivien täyttämisen automaattisesti valituilla kirjatuilla toimitusriveillä.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltolaskut** ja valitse sitten vastaava linkki.  
2. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
3. Luo laskurivit toimituille huolloille, jota ei ole laskutettu. Vaihtoehtoisesti voit lisätä kirjatut toimitusrivit laskuun **Hae toimitusrivit** -toiminnolla.  
4. Kirjaa huoltolasku.  
  
 Kirjattu huoltolasku ja vastaavat tapahtumat luodaan. Aiemmin kirjatut toimitusasiakirjat päivitetään laskutetuilla määrillä ja lähdetilausten huoltorivien määrillä.  

## Uuden huollon hyvityslaskun luominen  

Huollon hyvityslaskuasiakirjaan käytetään tavallisesti, kun asiakas palauttaa nimikkeen. Niitä voidaan käyttää kuitenkin myös asiakashyvityksenä tai virheellisen laskun korjaamiseen.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huollon hyvityslaskut** ja valitse sitten vastaava linkki.  
2. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Käsittelypäivämäärä näkyy **Kirjauspvm**- ja **Asiakirjapvm**-kentissä. Voit muuttaa sitä tarvittaessa.    
4. Syötä hyvityslaskun riveille tietoja nimikkeistä, jotka on palautettu tai poistettu tai asiakkaalle annettavasta korvauksesta.  

## Huoltolaskujen virheiden korjaaminen

Huoltolaskuja, joihin on liitetty huoltotapahtumia, voidaan poistaa. Niinpä huoltolaskujen virheet voidaan korjata tai niihin voidaan tehdä muutoksia juuttumatta tai tietoja menettämättä. Jos esimerkiksi tuotteen kirjausryhmä määrittäminen KP-tiliin on unohtunut, se voidaan lisätä myöhemmin ja luoda huoltolaskun uudelleen.

Huoltolasku poistetaan :::image type="content" source="media/copilot-delete-trash-can.png" alt-text="Poistotoiminon kuvake":::-toiminnolla. 

Huoltolaskun poistamisella on seuraavat seuraukset:

* Korjaava huoltotapahtuma kirjataan
* Sopimuksen laskutuspäivämäärä ja -jakso palautetaan, mikä mahdollistaa laskun luomisen uudelleen.

> [!NOTE]
> Vaikka useita laskuja voidaan palauttaa, se on tehtävä järjestyksessä viimeisimmästä laskusta alkaen.
>
> Huoltolaskua ei voi poistaa, jos sen tietoja, kuten laskutuskautta tai **Ennakkoon maksettu** -vaihtopainikkeen asentoa, muutettiin liittyvässä huoltosopimuksessa. Laskut on muistettava poistaa ennen asetusten muuttamista huoltosopimuksessa.

## Katso myös

[Huoltolaskujen kirjaaminen](service-how-to-post-service-orders.md)  
[Huoltohallinnon määrittäminen](service-setup-service.md)  
[Huollon kirjaaminen](service-service-posting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]