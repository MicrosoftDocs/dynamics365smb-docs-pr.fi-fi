---
title: Asiakkaiden hallinta Dynamics 365 for Salesissa| Microsoft Docs
description: "Voit tehdä Business Central -sovelluksessa tietojen yhdistämismäärityksen Dynamics 365 for Salesilla, jolloin saavutetaan liidistä tuottoon -prosessin saumaton integrointi ja synkronointi."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 057db7c39834c7be0fb93589e4fc58d740dd259c
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="managing-customers-and-sales-created-in-dynamics-365-for-sales"></a>Dynamics 365 for Sales -sovelluksessa luotujen asiakkaiden ja myynnin hallinta
Jos käytät Dynamics 365 for Sales -sovellusta (Sales) asiakassuhteissa, voit käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellusta tilausten käsittelyyn ja talousasioissa. Tällä tavoin saavutetaan saumaton integrointi liidistä tuottoon.

Kun sovellus on määritetty integroitavaksi Sales-sovelluksen kanssa, voit käyttää Sales-sovelluksen tietoja [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksesta ja toisin päin tietyissä tilanteissa. Tämän integroinnin ansiosta voit käsitellä ja synkronoida molemmille palveluille yhteisiä tietotyyppejä, kuten asiakkaita, kontakteja ja myyntitietoja, sekä pitää tiedot ajan tasalla molemmissa palveluissa.  

Esimerkiksi myyjä voi käyttää Sales-sovelluksessa [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen hinnastoja myyntitilauksen luonnissa. Kun he lisäävät nimikkeen Sales-sovelluksen myyntitilausriville, he näkevät myös nimikkeen varastotason (saatavuuden) [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksesta.

Ja päinvastoin, [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen tilausten käsittelijät voivat käsitellä Sales-sovelluksesta automaattisesti tai manuaalisesti siirrettyjä myyntitilausten erityisominaisuuksia. Erityisominaisuudet voivat olla esimerkiksi sallittujen myyntitilausrivien automaattinen luominen ja kirjaaminen Sales-sovellukseen käsin lisättyinä tuotteina syötetyille nimikkeille tai resursseille. Lisätietoja on Erityisten myyntitilausten tietojen käsittelminen -osassa.

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] integroituu vain Dynamics 365 for Sales -sovellukseen. Dynamics 365:n muut sovellukset tai ratkaisut, jotka muuttavat Sales-sovelluksen vakiotyönkulkua tai tietomallia (kuten Project Service Automation), voivat katkaista [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja Sales-sovelluksen integroinnin.

## <a name="standard-sales-entity-mapping-for-synchronization"></a>Synkronoinnin Myynti-entiteetin yhdistämismääritys
Myynti-entiteetit, kuten tilit, integroidaan vastaavien [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietuetyyppien, kuten asiakkaiden, kanssa. Voit käyttää Sales-sovelluksen tietoja sen jälkeen, kun [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietueiden ja Myynti-entiteettitietueiden väliset yhdistämismääritykset (eli yhdistämiset) on määritetty. Voit määrittää yhdistämisen esimerkiksi tietyn [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen asiakkaan ja vastaavan Sales-sovelluksen tilin välille.

Seuraava taulukko sisältää [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietuetyyppien luettelon (taulukot) ja vastaavat Myynti-entiteetit, jotka voidaan synkronoida heti käyttöönoton jälkeen.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|Myynti|Synkronoinnin suunta|Oletussuodatin|
|-------------------------------------------|-----|-------------------------|--------------|
|Myyjä/Ostaja|Käyttäjä|Sales -> Business Central|Sales-sovelluksen kontaktin suodatin: **Tila** on **Ei**, **Lisensoitu käyttäjä** on **Kyllä**, Integroinnin käyttäjä -tila on **Ei**|
|Asiakas|Tili|Business Central -> Sales ja Sales -> Business Central|Sales-sovelluksen tilin suodatin: **Suhteen tyyppi** on **Asiakas** ja **Tila** on **Aktiivinen**.|
|Kontakti|Kontakti|Business Central -> Sales ja Sales -> Business Central|Business Central -kontaktin suodatin: **Tyyppi** on **Henkilö** ja kontakti on liitetty yritykseen. Sales-sovelluksen kontaktin suodatin: Kontakti on liitetty yritykseen ja pääyrityksen tyyppi on **Tili**|
|Valuutta|Tapahtumavaluutta|Business Central -> Sales| |
|Mittayksikkö|Yksikköryhmä|Business Central -> Sales| |
|Vaihtoehto|Tuote|Business Central -> Sales ja Sales -> Business Central|Sales-sovelluksen kontaktin suodatin: **Tuotteen tyyppi** on **Myyntivarasto**|
|Resurssi|Tuote|Business Central -> Sales ja Sales -> Business Central|Sales-sovelluksen kontaktin suodatin: **Tuotteen tyyppi** on **Palvelut**|
|Asiakkaan hintaryhmä|Hinnasto|Business Central -> Sales| |
|Myyntihinta|Tuotehinnasto|Business Central -> Sales|Business Central -kontaktin suodatin: **Myyntikoodi** ei ole tyhjä, **Myynnin tyyppi** on **Asiakkaan hintaryhmä**|
|Mahdollisuus|Mahdollisuus|Business Central -> Sales ja Sales -> Business Central| |
|Myyntilaskun otsikko|Lasku|Business Central -> Sales| |
|Myyntilaskurivi|Laskutustuote|Business Central -> Sales| |

Taulukon 5335 (**Integrointitaulukon yhdistämismääritys**) taulukon määritystapahtumat määrittävät synkronoitavat Myynti-entiteetit ja [!INCLUDE[d365fin](includes/d365fin_md.md)] -taulukot. Voit tarkastella yhdistämismäärityksiä ja määrittää suodattimia sivulla 5335 (**Integrointitaulukon yhdistämismääritykset**). Taulukon 5336 (**Integrointikentän yhdistämismääritys**) kentän määritystapahtumat ja lisämäärityksen logiikka määrittävät [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietueiden kenttien ja Myynti-entiteettien kenttien väliset yhdistämismääritykset.

### <a name="field-mapping-for-the-sales-account-option"></a>Kentän yhdistämismääritys myyntitilin asetusta varten
[!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen kolme taulukkoa yhdistetään **Tili**-entiteetin asetuskenttien kanssa.   

Taulukon tietueet, joita ei ole linkitetty Sales-sovelluksen asetuksiin, ohitetaan synkronoinnin aikana. Tällöin Sales-sovelluksen **Asetus**-kenttä on tyhjä.

Seuraava taulukko näyttää **Tili**-entiteetin **Asetus**-kentän Business Central -taulukkojen yhdistämismääritykset.

|Sivupöytä|Sales-sovelluksen Tili-entiteetin asetuskenttä|
|----------------------|-------------------------------------------|
|Maksuehdot|Maksuehdot|
|Toimitusehto|Osoite 1: Kuljetusehdot|
|Kuljetusliike|Osoite 1: Toimitustapa|

### <a name="synchronization-rules"></a>Synkronointisäännöt
Seuraavassa taulukossa esitetään säännöt, jotka ohjaavat Business Central -taulukoiden ja Myynti-entiteettien synkronointia.

> [!NOTE]  
> Sales-yhteyden tilin suorittamia Sales-sovelluksen tietojen muutoksia ei oteta huomioon. Muutoksia ei synkronoida. Tämän vuoksi on suositeltavaa, että muutoksia ei tehdä Sales-yhteyden tilin avulla.

|Sivupöytä|Sääntö|
|-----|----|
|Asiakkaat|Ennen kuin asiakas voidaan synkronoida, asiakkaalle määritetyn myyjän on oltava kytkettynä Sales-sovelluksen käyttäjään. Varmista, että synkronoit myyjät ja Sales-sovelluksen käyttäjät, ennen kuin synkronoit asiakkaat ja Sales-sovelluksen tilit, kun ASIAKKAAT - Dynamics 365 for Sales -synkronointityö suoritetaan ja se määritetään uusien tietueiden luomista varten. <br /> <br />ASIAKKAAT – Dynamics 365 for Sales -synkronointityö synkronoi vain ne Sales-sovelluksen tilit, joiden suhteen tyyppi on Asiakas.|
|Kontaktit|Vain ne Sales-sovelluksen kontaktit, jotka on määritetty tiliin, luodaan Business Centralissa. Myyjän koodin arvo määrittää yhdistetyn entiteetin omistajan Sales-sovelluksessa.|
|Valuutat|Valuutat kytketään tapahtumavaluuttoihin Sales-sovelluksessa ISO-koodien perusteella. Vain valuuttoja, joilla on standardi ISO-koodi, kytketään ja synkronoidaan tapahtumanvaluuttojen kanssa.|
|Mittayksiköt|Mittayksiköt synkronoidaan yksikköryhmien kanssa Sales-sovelluksessa. Yksikköryhmälle voi määrittää vain yhden mittayksikön.|
|Nimikkeet|Kun myyntituotteisiin synkronoidaan nimikkeitä, Business Central luo automaattisesti Sales-sovelluksen hinnaston. Synkronointivirheitä välttämiseksi Älä muokkaa tämän hinnaston manuaalisesti.|
|Myyjät|Myyjät yhdistetään järjestelmäkäyttäjiin Sales-sovelluksessa. Käyttäjä on otettava käyttöön ja hänellä on oltava käyttöoikeus. Käyttäjä ei voi olla integroinnin käyttäjä. Huomaa, että tämä taulukko tulee synkronoida ensimmäiseksi, koska sitä käytetään asiakkaiden, kontaktien, mahdollisuuksien ja myyntilaskujen kanssa.|
|Resurssit|Resurssit synkronoidaan niiden myyntituotteiden kanssa, joiden tyyppi on Palvelu.|
|Asiakashintaryhmät|Asiakkaan hintaryhmät synkronoidaan myyntihinnastojen kanssa.|
|Myyntihinnat|Myyntihintojen myyntityyppi on Asiakkaan hintaryhmä. Niiden määritetty myyntikoodi synkronoidaan myyntihinnaston rivien kanssa.|
|Mahdollisuudet|Mahdollisuudet synkronoidaan myyntimahdollisuuksien kanssa. Myyjän koodin arvo määrittää yhdistetyn entiteetin omistajan Sales-sovelluksessa.|
|Kirjatut myyntilaskut|Kirjatut myyntilaskut synkronoidaan myyntilaskujen kanssa. Ennen laskun synkronointia kannattaa synkronoida kaikki muut entiteetit, jotka voivat vaikuttaa laskuun. Niitä voivat olla esimerkiksi myyjät ja hinnastot. Laskun otsikossa oleva myyjän koodin arvo määrittää yhdistetyn entiteetin omistajan Sales-sovelluksessa.|

## <a name="setting-up-the-connection"></a>Yhteyden määrittäminen
Voit käynnistää aloitussivulta asetusten ohjatun **Microsoft Dynamics 365 -yhteyden määrittäminen** -määrittämisen, joka auttaa yhteyden määrittämisessä. Kun yhteys on muodostettu, Sales-sovelluksen tietueet on yhdistetty saumattomasti [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen tietueisiin.  

> [!NOTE]  
>   Seuraavaksi käsitellään asetusten ohjattua määritystä. Voit halutessasi suorittaa samat tehtävät manuaalisesti **Sales-yhteyden määritys** -ikkunassa.

Voit valita avustetussa asennusoppaassa, mitkä tiedot synkronoidaan palvelujen välillä. Voit myös määrittää, että haluat tuoda nykyisen Sales-ratkaisun. Siinä tapauksessa on määritettävä hallinnollinen käyttäjätili.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Käyttäjätilin määrittäminen ratkaisun tuontia varten
Asennusopas käyttää hallinnollista tiliä nykyisen Sales-ratkaisun tuonnissa. Tämän tilin on oltava Sales-sovelluksen oikea käyttäjä, jolla on seuraavat käyttöoikeusroolit:

* järjestelmänvalvoja  
* ratkaisun mukauttaja.  

Lisätietoja on artikkelissa [Käyttäjien luominen ja Microsoft Dynamics 365 (online) -käyttöoikeusroolien määrittäminen](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) ja kohdassa [Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md).  

Tätä tiliä käytetään vain asennuksen aikana. Kun ratkaisu on tuotu [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, tiliä ei enää tarvita.

### <a name="setting-up-the-user-account-for-synchronization"></a>Synkronoinnin käyttäjätilin määrittäminen
Integraatiota varten tarvitaan jaettu käyttäjätili. Niinpä sinun on luotava Office 365 -tilauksessa erillinen käyttäjä, jota käytetään kahden palvelun välillä tapahtumaan synkronointiin. Tämän tilin on oltava jo kelvollinen Sales-sovelluksen käyttäjä, mutta tilille ei tarvitse määrittää käyttöoikeusrooleja, koska asennusopas tekee sen puolestasi. Tämä käyttäjätili on määritettävä asennusoppaassa ainakin kerran sen perusteella, kuinka laajan synkronoinnin haluat ottaa käyttöön. Lisätietoja on artikkelissa [Käyttäjien luominen ja Microsoft Dynamics 365 (online) -käyttöoikeusroolien määrittäminen](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles).

Jos otat käyttöön *tuotteen saatavuuden*, integrointiin käytettävällä käyttäjätilillä on oltava verkkopalvelun käyttöoikeusavain. Se on kaksivaiheinen toiminto. Sinun on valittava kyseisen tilin [!INCLUDE[d365fin](includes/d365fin_md.md)]-sivulla **Muuta verkkopalvelun käyttöoikeusavainta** -painike ja määritettävä Sales-yhteyden asennusoppaassa kyseinen käyttäjä OData-verkkopalvelun käyttäjäksi.

Jos otat käyttöön *myyntitilauksen integroinnin*, sinun on määritettävä tämän synkronoinnin käsittelevä käyttäjä. Se voi olla joko integrointikäyttäjä tai jokin muu käyttäjätili.

### <a name="coupling-records"></a>Tietueiden yhdistäminen
Voit valita avustetussa asennusoppaassa mitä kahden palvelun välillä synkronoidaan. Voit määrittää myöhemmin myös tietyn tyyppisten tietojen synkronoinnin. Tätä kutsutaan *yhdistämiseksi* ja tässä osassa kerrotaan, mitä seikkoja on kannattaa ottaa huomioon.

Jos haluat nähdä Sales-tilit [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen asiakkaina, kaksi tietuetyyppiä on yhdistettävä. Se on melko yksinkertaista: avaa **Asiakasluettelo**-ikkuna [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa, jonka valintanauhan toiminnolla nämä tiedot voi yhdistää Sales-sovelluksen kanssa. Voit sitten määrittää, mitä Sales-tilejä tietyt [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen asiakkaat vastaavat.

Tietyillä alueilla toimintoa varten on ensin yhdistettävä tietyt tietojoukot ennen muita tietojoukkoja. Lisätietoja on seuraavassa luettelossa:

* Asiakkaat ja tilit  
  * Myyjät on yhdistettävä ensin Sales-sovelluksen käyttäjien kanssa  
* Nimikkeet ja resurssit  
  * Mittayksiköt on yhdistettävä ensin Sales-sovelluksen yksikköryhmien kanssa  
* Nimikkeiden ja resurssien hinnat  
  * Asiakkaan hintaryhmät on yhdistettävä ensin Sales-sovelluksen hintoihin  

> [!NOTE]  
>   Jos hinnoissa käytetään ulkomaan valuuttaa, varmista, että valuutat yhdistetään Sales-sovelluksen tapahtumavaluuttoihin.

Sales-sovelluksen myyntitilaukset tarvitsevat lisätietoja, kuten asiakkaita, mittayksiköitä, valuuttoja, asiakkaan hintaryhmiä, nimikkeitä ja/tai resursseja. Myyntitilausten saumaton integraatio edellyttää, että asiakkaat, mittayksikkö, asiakkaan hintaryhmät, nimikkeet ja/tai resurssit yhdistetään ensin.

### <a name="synchronizing-records-fully"></a>Tietueiden täysi synkronointi
Valitse avustetun asennusoppaan lopussa **Suorita täysi synkronointi** -toiminto. Tämä toiminto aloittaa kaikkien [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen tietueiden synkronoinnin kaikkien yhdistetyn Sales-ratkaisun liittyvien tietueiden synkronoinnin. Valitse **Täyden CRM-synkronoinnin tarkistus** -ikkunassa **Aloita**-toiminto. Synkronointi aloittaa sitten töiden suorittamisen riippuvuuksien mukaisesti. Esimerkiksi valuuttatietueet synkronoidaan ennen asiakastietueita. Täysi synkronointi voi kestää kauan, joten se tapahtuu taustalla, jotta voit jatkaa [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöä.

Voit tarkistaa täyden synkronoinnin yksittäisten töiden etenemistä, porautua alaspäin **Työjonon tapahtuman tila**-, **Integrointitaulukkoon – projektin tila**- tai **Integrointitaulukosta – projektin tila** -kentissä **Täyden CRM-synkronoinnin tarkistus** -ikkunassa.

**Microsoft Dynamics 365 -yhteyden määritys** -ikkunasta voi katsoa koska tahansa tietoja täydestä synkronoinnista. Voit avata sieltä myös **Integrointitaulukon yhdistämismääritykset** -ikkunan, jossa on tietoja synkronoitavista [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen ja yhdistetyn Sales-ratkaisun taulukoista.

## <a name="handling-special-sales-order-data"></a>Erityisen myyntitilauksen tietojen käsitteleminen
Sales-sovelluksen myyntitilaukset siirretään automaattisesti [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellukseen, jos valitset **Luo myyntitilaukset automaattisesti** -valintaruudun **Microsoft Dynamics 365 -yhteyden määrittäminen** -ikkunassa. Näissä myyntitilauksissa alkuperäisen tilauksen **Nimi**-kenttä siirretään ja yhdisetään myyntitilauksen **Ulkoisen asiakirjan numero** -kenttään [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa.

Tämä voi toimia myös, jos alkuperäinen myyntitilaus sisältää käsin lisättyjä tuotteita eli nimikkeitä tai resursseja, joita ei ole rekisteröity kumpaankaan tuotteeseen. Tällöin tulee antaa **Käsin lisätyn tuotteen tyyppi**- ja **Käsin lisätyn tuotteen numero** -kentät **Myynnin ja myyntisaamisten asetukset** -ikkunassa. Tällöin ei-rekisteröity tuotemyynti yhdistetään talousanalyysissa tiettyyn nimike-/resurssinumeroon.

Jos alkuperäisen myyntitilauksen kuvaus on hyvin pitkä, sitä varten luodaan [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen myyntitilaukseen lisämyyntitilausrivi, jonka tyyppi on Kommentti.

## <a name="see-also"></a>Katso myös
[Kontaktienhallinta](marketing-relationship-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md)    
[Organisaation ja käyttäjien perehdyttäminen Dynamics 365 (online) -ratkaisuun](/dynamics365/customer-engagement/admin/onboard-your-organization-and-users-to-dynamics-365-online)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

