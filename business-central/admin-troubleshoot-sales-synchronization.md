---
title: Synkronointivirheiden vianmääritys
description: 'Tämä aihe sisältää ohjeita synkronointivirheiden tunnistamista, määrittämistä ja ratkaisemista varten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/14/2021
ms.author: bholtorf
---
# <a name="troubleshooting-synchronization-errors"></a><a name="troubleshooting-synchronization-errors"></a>Synkronointivirheiden vianmääritys


Sovellusten [!INCLUDE[prod_short](includes/prod_short.md)] ja [!INCLUDE[prod_short](includes/cds_long_md.md)] integrointi sisältää useita vaiheita, ja joskus tapahtuu virheitä. Tässä ohjeaiheessa kerrotaan yleisimpiä virheitä ja annetaan vinkkejä niiden korjaamiseen.

Virheet johtuvat usein siitä, että käyttäjä on tehnyt jotain yhdistetyille tietueille tai integroinnin määrittämisessä on tapahtunut virhe. Jos virheet ovat tapahtuneet yhdistettyjen tietueiden vuoksi, käyttäjät voivat ratkaista ne itse. Nämä virheet johtuvat esimerkiksi siitä, että poistat tietoja yhdestä liiketoimintasovelluksesta, mutta et molemmista, ja synkronoit tämän jälkeen. Lisätietoja on kohdassa [Synkronoinnin tilan näyttäminen](admin-how-to-view-synchronization-status.md).

Integroinnin määrittämiseen liittyvät virheet vaativat yleensä järjestelmänvalvojan toimia. Voit tarkastella näitä virheitä **Integroinnin synkronointivirheet** -sivulla. 

Seuraavassa taulukossa on esimerkkejä tyypillisistä ongelmista:  

|Ongelma  |Ratkaisu  |
|---------|---------|
|Integroinnin käyttäjille määritetyt käyttöoikeudet ja roolit ovat virheellisiä. | Virheen lähde on [!INCLUDE[prod_short](includes/cds_long_md.md)], ja siinä on usein seuraava teksti: Pääkäyttäjästä (ID=\<user id>, type=8) puuttuu oikeus \<privilegeName>. Tämä virhe tapahtuu, koska integroinnin käyttäjältä puuttuu oikeus, joka sallii entiteetin käytön. Yleensä tämä virhe tapahtuu mukautettuja entiteettejä synkronoitaessa tai jos [!INCLUDE[prod_short](includes/cds_long_md.md)]en on asennettu sovellus, joka tarvitsee oikeuden muiden [!INCLUDE[prod_short](includes/cds_long_md.md)]-entiteettien käyttämiseen. Tämä virhe ratkaistaan määrittämällä oikeus integroinnin käyttäjälle [!INCLUDE[prod_short](includes/cds_long_md.md)]ssä.<br><br> Integroinnin käyttäjän nimi löytyy **Dataverse-yhteyden asetukset** -sivulla. Virhesanoma sisältää oikeuden nimen, mikä voi auttaa tunnistamaan entiteetin, jonka käyttöön tarvitaan oikeus. Lisää puuttuva oikeus kirjautumalla [!INCLUDE[prod_short](includes/cds_long_md.md)]en järjestelmänvalvojan tilillä ja muokkaamalla integroinnin käyttäjälle määritettyä käyttöoikeusroolia. Lisätietoja on kohdassa [Käyttöoikeuksien hallinta luomalla käyttöoikeusrooli tai muokkaamalla sitä](/power-platform/admin/create-edit-security-role). |
|Olet yhdistämässä tietuetta, joka käyttää toista yhdistämätöntä tietuetta. Esimerkiksi asiakas, jonka valuuttaa ei ole yhdistetty, tai nimike, jonka mittayksikköä ei ole yhdistetty. | Riippuvainen tietue, kuten valuutta tai mittayksikkö on yhdistettävä ensin, ja sen jälkeen yhdistämistä voidaan kokeilla uudelleen. |

Seuraavat Integroinnin synkronointivirheet -sivun työkalut auttavat ratkaisemaan näitä ongelmia manuaalisesti.  

* **Lähde**- ja **Kohde**-kentät voivat sisältää linkkejä riviin, josta virhe löytyi. Tutki virhettä napsauttamalla linkkiä.  
* **Poista yli 7 päivää vanhat tapahtumat**- ja **Poista kaikki tapahtumat** -toiminnot tyhjentävät luettelon. Näitä toimintoja käytetään yleensä sen jälkeen, kun useisiin tietueisiin vaikuttavan virheen syy on selvitetty. Mieti kuitenkin tarkasti, kun teet sen. Nämä toiminnot saattavat poistaa virheitä, jotka vielä vaikuttavat toimintaan.
* **Näytä virheen kutsupino** -toiminto näyttää tiedot, jotka voivat auttaa tunnistamaan virheen syyn. Jos virhettä ei voi ratkaista itse ja päätät lähettää tukipyynnön, sisällytä tiedot tukipyyntöön.

## <a name="see-also"></a><a name="see-also"></a>Katso myös
[Integrointi Microsoft Dataversein kanssa](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Microsoft Dataverse -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md)  
[Yhteyden määrittäminen Microsoft Dataverse -sovellukseen](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Tietueiden yhdistäminen ja synkronoiminen manuaalisesti](admin-how-to-couple-and-synchronize-records-manually.md)  
[Synkronoinnin tilan näyttäminen](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
