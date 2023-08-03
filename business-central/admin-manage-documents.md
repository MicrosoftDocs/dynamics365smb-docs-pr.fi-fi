---
title: Hallitse tallennustilaa poistamalla asiakirjoja tai pakkaamalla tietoja.
description: Opi käsittelemään historiallisten asiakirjojen kertymistä (ja vähentämään tietokantaan tallennettujen tietojen määrää) poistamalla tai pakkaamalla ne.
author: edupont04
ms.topic: conceptual
ms.search.form: '107, 9035, 9040'
ms.date: 09/14/2022
ms.author: edupont
---
# Hallitse tallennustilaa poistamalla asiakirjoja tai pakkaamalla tietoja.

Keskitetyn roolin, kuten sovelluksen järjestelmänvalvojan, on huolehdittava säännöllisesti siitä, että vanhat asiakirjat joko poistetaan tai tiivistetään.  

> [!TIP]
> Lisätietoja muista tavoista vähentää tietokantaan tallennettujen tietojen määrää on kehittäjien ja IT-ammattilaisten ohjeessa [Business Central -tietoantoihin tallennettujen tietojen vähentäminen](/dynamics365/business-central/dev-itpro/administration/database-reduce-data).

## Asiakirjojen poistaminen

Jossain tapauksissa voi olla tarpeen poistaa laskutettuja ostotilauksia. Et kuitenkaan voi poistaa niitä, ellet ole kokonaan laskuttanut ja vastaanottanut nimikkeitä ostotilauksissa. [!INCLUDE[prod_short](includes/prod_short.md)] auttaa tarkistamalla sen.

Ohjelma poistaa palautustilaukset tavallisesti sen jälkeen, kun ne on laskutettu. Kun kirjaat laskun, se siirretään **Kirjattu ostohyvityslasku** -sivulle. Jos kuitenkin olet valinnut **Palautustoimitus hyvityslaskutettaessa** -valintaruudun **Ostojen ja ostovelkojen asetukset** -sivulla, lasku siirretään **Kirjattu palautustoimitus** -sivulle. Voit poistaa asiakirjat **Poista laskutetut ostopal.til.** -eräajolla. Eräajo tarkistaa ennen poistamista, onko ostopalautustilaukset toimitettu ja laskutettu kokonaan.  

Puiteostotilauksia ei poisteta automaattisesti sen jälkeen, kun kaikki liittyvät ostotilaukset on käsitelty ja laskutettu. Sen sijaan ne voi poistaa **Poista lask. puiteostotilaukset** -eräajolla.  

Laskutetut huoltotilaukset poistetaan ohjelmasta automaattisesti sen jälkeen, kun ne on laskutettu kokonaan. Kun lasku on kirjattu, vastaava tapahtuma luodaan ja niitä voi tarkastella **Kirjatut huoltolaskut** -sivulla.  

Ohjelma ei poista huoltotilauksia automaattisesti, jos tilauksen kokonaismäärä on kirjattu **Huoltolasku**-sivulla eikä huoltotilauksessa. Tällaiset laskutetut tilaukset täytyy ehkä poistaa manuaalisesti suorittamalla **Poista laskutetut huoltotilaukset** -eräajo.  

## Pakkaa tiedot päivämäärätiivistyksen avulla

Voit pakata tietoja [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa niin, että säästät tilaa tietokannassa&mdash;joka [!INCLUDE [prod_short](includes/prod_short.md)] onlinessa voi jopa säästää rahaa. Tiivistys perustuu päivämääriin ja toimintoihin, yhdistää useita vanhoja tapahtumia yhdeksi uudeksi tapahtumaksi.

Voit tiivistää tapahtumat, jotka täyttävät kaikki seuraavat olosuhteet:

* Ne ovat suljetuilta tilikausilta.
* **Avoin**-kentän arvoksi asetetaan **Ei**.
* Ne ovat ainakin viisi vuotta vanhoja. Jos haluat pakata alle viisi vuotta vanhoja tietoja, ota yhteyttä Microsoft-kumppaniisi.

Joten esimerkiksi aiempien tilikausien toimittajatapahtumat voidaan tiivistää siten, että jokaista tiliä ja jokaista kuukautta kohti on vain yksi kredit- ja yksi debet-tapahtuma. Uuden tapahtuman summa on kaikkien tiivistettyjen tapahtumien summa. Määritetty päivämäärä on tiivistettävän ajanjakson aloituspäivämäärä, esimerkiksi kuukauden ensimmäinen päivä (jos tapahtumat on tiivistetty kuukauden mukaan). Tiivistyksen jälkeen voit yhä nähdä jokaisen tilin nettomuutoksen edellisen tilikauden osalta.

Päivämäärätiivistyksen tuloksena syntyvien tapahtumien määrä perustuu siihen, kuinka monta suodatinta asetat, mitkä kentät yhdistetään ja minkä jakson pituuden valitset. Tapahtumia syntyy aina vähintään yksi. Kun eräajo on päättynyt, tulos näkyy **Tiivistysrekisterit**-sivulla.

Voit pakata seuraavan tyyppisiä tietoja eräajojen avulla.

* Talouden tapahtumat – pääkirjanpito (KP) -tapahtumat, arvonlisävero (ALV) -tapahtumat, pankkitilitapahtumat, KP-budjettitapahtumat, asiakastapahtumat, toimittajatapahtumat.
* Fyysisen varaston tapahtumat
* Resurssitapahtumat
* Nimikkeiden budjettitapahtumat
* Käyttöomaisuustapahtumat, KO:n ylläpitotapahtumat ja KO-vakuutustapahtumat.

Kun määrität tiivistyksen ehtoja, voit säilyttää tiettyjen kenttien sisällön käyttämällä **Säilytä kentän sisältö** -kohdan alla olevia vaihtoehtoja. Käytettävissä olevat kentät määräytyvät pakattavan tiedon mukaan.

> [!NOTE]
> Ennen kuin voit suorittaa päivämäärätiivistyksen, analyysinäkymien on oltava ajan tasalla. Lisätietoja on [Analyysinäkymän päivittäminen](bi-how-analyze-data-dimension.md#update-an-analysis-view) -osassa.

Tiivistyksen jälkeen seuraavien kenttien sisältö säilytetään aina: **Kirjauspvm**, **Toimittajanro**, **Asiakirjan tyyppi**, **Valuutan koodi**, **Kirjausryhmä**, **Summa**, **Jäljellä oleva summa**, **Alkuperäinen summa (PVA)**, **Jäljellä oleva summa (PVA)**, **Summa (PVA)**, **Osto (PVA)**, **Laskualennus (PVA)**, **Annettu maksualennus (PVA)** ja **Maksualennus mahdollinen**.

## Tiivistettyjen tapahtumien kirjaaminen

Tiivistetyt tapahtumat kirjataan hieman eri tavalla kuin vakiokirjaukset. Tämä vähentää tiivistyksen avulla luotujen uusien pääkirjanpidon tapahtumien määrää, ja se on erityisen tärkeää, kun pidät yllä tietoja, kuten dimensioita ja asiakirjanumeroita. Päivämäärätiivistys luo uusia tapahtumia seuraavasti:

* **Pääkirjanpidon tapahtumat** -sivulla tiivistetyille tapahtumille luodaan uusia tapahtumia. **Kuvaus**-kenttä sisältää **Tiivistetty**-päivämäärän niin, että tiivistetyt tapahtumat on helppo yksilöidä. 
* Kirjanpitosivuilla, kuten **Asiakastapahtumat**-sivulla, luodaan yksi tai useampia uusia tapahtumia. 

Kirjausprosessi luo numerosarjojen aukkoja **Pääkirjanpidon tapahtumat** -sivulla oleville tapahtumille. Nämä numerot on määritelty vain kirjanpitosivujen tapahtumille. Tapahtumiin liitetty numeroalue on saatavilla **KP-rekisteri**-sivun **Tapahtumasta nro**- ja **Tapahtumaan nro** -kentistä. 

> [!NOTE]
> Kun olet suorittanut päivämäärien tiivistyksen, kaikki kirjanpidon tilit on lukittu. Tämä tarkoittaa, että et voi esimerkiksi peruuttaa toimittajan tai pankkikirjan merkintöjä millekään tilille, johon pakkaaminen vaikuttaa.

Päivämäärätiivistyksen tuloksena syntyvien tapahtumien määrä perustuu siihen, kuinka monta suodatinta asetat, mitkä kentät yhdistetään ja minkä jakson pituuden valitset. Tapahtumia syntyy aina vähintään yksi.

> [!WARNING]
> Tiivistys poistaa tapahtumia, joten aina ennen kuin aloitat eräajon, tee varmuuskopio tietokannasta.

### Suorita Pvmtiivistys

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Tietojen hallinta**, valitse sitten aiheeseen liittyvä linkki.
2. Tee jompikumpi seuraavista toimista:
    * Jos haluat käyttää avustettua opasta asentaaksesi päivämäärätiivistyksen vähintään yhdelle tietotyypille, valitse **Tietojen hallinnan opas**.
    * Jos haluat määrittää tiivistyksen yksittäiselle tietotyypille, valitse **Tietojen tiivistys**, **Tiivistä tapahtumat**, valitse sitten tiivistettävät tiedot.

   > [!NOTE]
   > Voit pakata vain yli viisi vuotta vanhoja tietoja. Jos haluat pakata alle viisi vuotta vanhoja tietoja, ota yhteyttä Microsoft-kumppaniisi.

## Katso myös

[Hallinta](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
