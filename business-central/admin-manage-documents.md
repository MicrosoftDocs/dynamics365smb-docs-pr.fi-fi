---
title: Hallitse tallennustilaa poistamalla asiakirjoja tai pakkaamalla tietoja.
description: Opi käsittelemään historiallisten asiakirjojen kertymistä (ja vähentämään tietokantaan tallennettujen tietojen määrää) poistamalla tai pakkaamalla ne.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: 5263d4ba06cc7b2dc497efb6842a927704c31f35
ms.sourcegitcommit: 428ba6385cb27475e8803c2a8967daa22cfe8879
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/29/2021
ms.locfileid: "7724705"
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Hallitse tallennustilaa poistamalla asiakirjoja tai pakkaamalla tietoja.

Keskitetyn roolin, kuten sovelluksen järjestelmänvalvojan, on huolehdittava säännöllisesti siitä, että vanhat asiakirjat joko poistetaan tai tiivistetään.  

> [!TIP]
> Tietoja muista tavoista vähentää tietokantaan tallennettujen tietojen määrää on kehittäjien ja IT-ammattilaisten ohjeessa [Business Central -tietoantoihin tallennettujen tietojen vähentäminen](/dynamics365/business-central/dev-itpro/administration/database-reduce-data).

## <a name="delete-documents"></a>Asiakirjojen poistaminen

Jossain tapauksissa voi olla tarpeen poistaa laskutettuja ostotilauksia, joita ei ole poistettu. [!INCLUDE[prod_short](includes/prod_short.md)] tarkistaa, että poistetut ostotilaukset on laskutettu kokonaan. Tilauksia, joita ei ole kokonaan laskutettu ja vastaanotettu, ei voi poistaa.  

Ohjelma poistaa palautustilaukset tavallisesti sen jälkeen, kun ne on laskutettu. Kun kirjaat laskun, se siirretään **Kirjattu ostohyvityslasku** -sivulle. Jos kuitenkin olet valinnut **Palautustoimitus hyvityslaskutettaessa** -valintaruudun **Ostojen ja ostovelkojen asetukset** -sivulla, lasku siirretään sitten **Kirjattu palautustoimitus** -sivulle. Voit poistaa asiakirjat **Poista laskutetut ostopal.til.** -eräajolla. Eräajo tarkistaa ennen poistamista, onko ostopalautustilaukset toimitettu ja laskutettu kokonaan.  

Puiteostotilauksia ei poisteta sen jälkeen, kun kaikki liittyvät ostotilaukset on käsitelty ja laskutettu. Puitetilaukset voi poistaa **Poista lask. puiteostotilaukset** -eräajolla.  

Laskutetut huoltotilaukset poistetaan ohjelmasta automaattisesti sen jälkeen, kun ne on laskutettu kokonaan. Kun lasku on kirjattu, vastaava tapahtuma luodaan **Kirjatut huoltolaskut** -sivulla. Kirjattua asiakirjaa voi katsella **Kirjattu huoltolasku** -sivulla.  

Ohjelma ei poista huoltotilauksia automaattisesti, jos tilauksen kokonaismäärä on kirjattu **Huoltolasku**-sivulla eikä huoltotilauksessa. Tällöin sinun on ehkä poistettava laskutetut tilaukset, joita ei poistettu. Voit tehdä sen suorittamalla **Poista laskutetut huoltotilaukset** -eräajon.  

## <a name="compress-data-with-date-compression"></a>Pakkaa tiedot päivämäärätiivistyksen avulla

Voit pakata tietoja [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa niin, että säästät tilaa tietokannassa, joka [!INCLUDE [prod_short](includes/prod_short.md)] onlinessa voi jopa säästää rahaa. Tiivistys perustuu päivämääriin ja yhdistää useita vanhoja tapahtumia yhdeksi uudeksi tapahtumaksi. 

Voit tiivistää tapahtumat seuraavissa olosuhteissa:

* Ne ovat suljetuilta tilikausilta.
* **Avoin**-kentän arvoksi asetetaan **Ei**. 
* Ne ovat ainakin viisi vuotta vanhoja. Jos haluat pakata alle viisi vuotta vanhoja tietoja, ota yhteyttä Microsoft-kumppaniisi.

Esimerkiksi aiempien tilikausien toimittajatapahtumat voidaan tiivistää siten, että jokaista tiliä ja jokaista kuukautta kohti on vain yksi kredit- ja yksi debet-tapahtuma. Uuden tapahtuman summa on kaikkien tiivistettyjen tapahtumien summa. Määritetty päivämäärä on tiivistettävän ajanjakson aloituspäivämäärä, esimerkiksi kuukauden ensimmäinen päivä (jos tapahtumat on tiivistetty kuukauden mukaan). Tiivistyksen jälkeen voit yhä nähdä jokaisen tilin nettomuutoksen edellisen tilikauden osalta.

Päivämäärätiivistyksen tuloksena syntyvien tapahtumien määrä perustuu siihen, kuinka monta suodatinta asetat, mitkä kentät yhdistetään ja minkä jakson pituuden valitset. Tapahtumia syntyy aina vähintään yksi. Kun eräajo on päättynyt, tulos näkyy **Tiivistysrekisterit**-sivulla.

Voit pakata seuraavan tyyppisiä tietoja eräajojen avulla. Kullekin tietotyypille on eräajo.

* Talouden tapahtumat – KP-tapahtumat, ALV-tapahtumat, pankkitilitapahtumat, KP-budjettitapahtumat, asiakastapahtumat, toimittajatapahtumat.
* Fyysisen varaston tapahtumat 
* Resurssitapahtumat
* Nimikkeiden budjettitapahtumat
* Käyttöomaisuus – käyttöomaisuustapahtumat, KO:n ylläpitotapahtumat, KO-vakuutustapahtumat.

Kun määrität tiivistyksen ehtoja, voit käyttää **Säilytä kentän sisältö** -kohdan alla olevia vaihtoehtoja säilyttääksesi tiettyjen kenttien sisällön. Käytettävissä olevat kentät määräytyvät pakattavan tiedon mukaan.

> [!NOTE]
> Ennen kuin voit suorittaa päivämäärätiivistyksen, analyysinäkymien on oltava ajan tasalla. Lisätietoja on kohdassa [Analyysinäkymän päivittäminen](bi-how-analyze-data-dimension.md#to-update-an-analysis-view).

Tiivistyksen jälkeen seuraavien kenttien sisältö säilytetään aina: **Kirjauspvm**, **Toimittajanro**, **Asiakirjan tyyppi**, **Valuutan koodi**, **Kirjausryhmä**, **Summa**, **Jäljellä oleva summa**, **Alkuperäinen summa (PVA)**, **Jäljellä oleva summa (PVA)**, **Summa (PVA)**, **Osto (PVA)**, **Laskualennus (PVA)**, **Annettu maksualennus (PVA)** ja **Maksualennus mahdollinen**.

## <a name="posting-compressed-entries"></a>Tiivistettyjen tapahtumien kirjaaminen
Tiivistetyt tapahtumat kirjataan hieman eri tavalla kuin vakiokirjaukset. Tämä vähentää tiivistyksen avulla luotujen uusien pääkirjanpidon tapahtumien määrää, ja se on erityisen tärkeää, kun pidät yllä tietoja, kuten dimensioita ja asiakirjanumeroita. Päivämäärätiivistys luo uusia tapahtumia seuraavasti:
* **Pääkirjanpidon tapahtumat** -sivulla uusille tapahtumille luodaan uusia tapahtuma numeroita tiivistetyistä tapahtumista. **Kuvaus**-kenttä sisältää **Tiivistetty**-päivämäärän niin, että tiivistetyt tapahtumat on helppo yksilöidä. 
* Kirjanpitosivuilla, kuten **Asiakastapahtumat**-sivulla, luodaan yksi tai useampia tapahtumia uusien tapahtumanumeroiden avulla. 

Kirjausprosessi luo numerosarjojen aukkoja **Pääkirjanpidon tapahtumat** -sivulla oleville tapahtumille. Nämä numerot on määritelty vain kirjanpitosivujen tapahtumille. Tapahtumiin liitetty numeroalue on saatavilla **KP-rekisteri**-sivun **Tapahtumasta nro**- ja **Tapahtumaan nro** -kentistä. 

> [!NOTE]
> Kun olet suorittanut päivämäärien tiivistyksen, kaikki kirjanpidon tilit on lukittu. Et voi esimerkiksi poistaa toimittaja- tai pankkitapahtumien kohdistamista millekään tilille sen kauden osalta, jonka ajalta päivämäärät tiivistetään.

Päivämäärätiivistyksen tuloksena syntyvien tapahtumien määrä perustuu siihen, kuinka monta suodatinta asetat, mitkä kentät yhdistetään ja minkä jakson pituuden valitset. Tapahtumia syntyy aina vähintään yksi. 

> [!WARNING]
> Tiivistys poistaa tapahtumia, joten aina ennen kuin aloitat eräajon, tee varmuuskopio tietokannasta.

### <a name="to-run-a-date-compression"></a>Suorita Pvmtiivistys
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Tietojen hallinta** ja valitse sitten aiheeseen liittyvä linkki.
2. Tee jompikumpi seuraavista toimista:
    * Jos haluat käyttää avustettua asennusopasta asentaaksesi päivämäärätiivistyksen vähintään yhdelle tietotyypille, valitse **Tietojen hallinnan opas**.
    * Jos haluat määrittää tiivistyksen yksittäiselle tietotyypille, valitse **Pvmtiivistys**, **Tiivistä tapahtumat** ja valitse sitten tiivistettävät tiedot.

   > [!NOTE]
   > Voit pakata vain yli viisi vuotta vanhoja tietoja. Jos haluat pakata alle viisi vuotta vanhoja tietoja, ota yhteyttä Microsoft-kumppaniisi.

## <a name="see-also"></a>Katso myös

[Hallinta](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]