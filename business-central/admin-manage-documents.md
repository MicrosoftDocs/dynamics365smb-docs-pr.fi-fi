---
title: Hallitse tallennustilaa poistamalla asiakirjoja tai pakkaamalla tietoja.
description: Tietoja siitä, miten voit säilyttää historialliset tiedot pakkaamalla tapahtumia tai poistaa ne.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 05e5078253d63fac61039d26cc0d700e96c7d21a
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911278"
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Hallitse tallennustilaa poistamalla asiakirjoja tai pakkaamalla tietoja.

Keskitetyn roolin, kuten sovelluksen järjestelmänvalvojan, on huolehdittava säännöllisesti siitä, että vanhat asiakirjat joko poistetaan tai tiivistetään.  

## <a name="delete-documents"></a>Asiakirjojen poistaminen

Jossain tapauksissa voi olla tarpeen poistaa laskutettuja ostotilauksia, joita ei ole poistettu. [!INCLUDE[d365fin](includes/d365fin_md.md)] tarkistaa, että poistetut ostotilaukset on laskutettu kokonaan. Tilauksia, joita ei ole kokonaan laskutettu ja vastaanotettu, ei voi poistaa.  

Ohjelma poistaa palautustilaukset tavallisesti sen jälkeen, kun ne on laskutettu. Kun kirjaat laskun, se siirretään **Kirjattu ostohyvityslasku** -sivulle. Jos kuitenkin olet valinnut **Palautustoimitus hyvityslaskutettaessa** -valintaruudun **Ostojen ja ostovelkojen asetukset** -sivulla, lasku siirretään sitten **Kirjattu palautustoimitus** -sivulle. Voit poistaa asiakirjat **Poista laskutetut ostopal.til.** -eräajolla. Eräajo tarkistaa ennen poistamista, onko ostopalautustilaukset toimitettu ja laskutettu kokonaan.  

Puiteostotilauksia ei poisteta sen jälkeen, kun kaikki liittyvät ostotilaukset on käsitelty ja laskutettu. Puitetilaukset voi poistaa **Poista lask. puiteostotilaukset** -eräajolla.  

Laskutetut huoltotilaukset poistetaan ohjelmasta automaattisesti sen jälkeen, kun ne on laskutettu kokonaan. Kun lasku on kirjattu, vastaava tapahtuma luodaan **Kirjatut huoltolaskut** -sivulla. Kirjattua asiakirjaa voi katsella **Kirjattu huoltolasku** -sivulla.  

Ohjelma ei poista huoltotilauksia automaattisesti, jos tilauksen kokonaismäärä on kirjattu **Huoltolasku**-sivulla eikä huoltotilauksessa. Tällöin sinun on ehkä poistettava laskutetut tilaukset, joita ei poistettu. Voit tehdä sen suorittamalla **Poista laskutetut huoltotilaukset** -eräajon.  

## <a name="compress-data-with-date-compression"></a>Pakkaa tiedot päivämäärätiivistyksen avulla

Voit pakata tietoja [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelmassa niin, että säästät tilaa tietokannassa, joka [!INCLUDE [prodshort](includes/prodshort.md)] onlinessa voi jopa säästää rahaa. Tiivistys perustuu päivämääriin ja yhdistää useita vanhoja tapahtumia yhdeksi uudeksi tapahtumaksi. Tapahtumia voi tiivistää vain suljetuilta tilikausilta, ja voit tiivistää vain sellaisia toimittajatapahtumia, joiden **Avoin**-kentän arvo on *Nro*.  

Esimerkiksi aiempien tilikausien toimittajatapahtumat voidaan tiivistää siten, että jokaista tiliä ja jokaista kuukautta kohti on vain yksi kredit- ja yksi debet-tapahtuma. Uuden tapahtuman summa on kaikkien tiivistettyjen tapahtumien summa. Määritetty päivämäärä on tiivistettävän ajanjakson aloituspäivämäärä, esimerkiksi kuukauden ensimmäinen päivä (jos tapahtumat on tiivistetty kuukauden mukaan). Tiivistyksen jälkeen voit yhä nähdä jokaisen tilin nettomuutoksen edellisen tilikauden osalta.

Päivämäärätiivistyksen tuloksena syntyvien tapahtumien määrä perustuu siihen, kuinka monta suodatinta asetat, mitkä kentät yhdistetään ja minkä jakson pituuden valitset. Tapahtumia syntyy aina vähintään yksi. Kun eräajo on päättynyt, tulos näkyy **Tiivistysrekisterit**-sivulla.

Voit pakata seuraavan tyyppisiä tietoja [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelmassa eräajojen avulla:

* Pankkitilitapahtumat

  Tiivistyksen jälkeen **Säilytä kentän sisältö** -toiminnon avulla voit myös säilyttää seuraavien kenttien sisällön: **Asiakirjan nro, Kontaktimme**, **Globaali dimensio 1 koodi** ja **Globaali dimensio 2 koodi**.
* Toimittajatapahtumat

  Tiivistyksen jälkeen seuraavien kenttien sisältö säilytetään aina: **Kirjauspvm**, **Toimittajanro**, **Asiakirjan tyyppi**, **Valuutan koodi**, **Kirjausryhmä**, **Summa**, **Jäljellä oleva summa**, **Alkuperäinen summa (PVA)**, **Jäljellä oleva summa (PVA)**, **Summa (PVA)**, **Osto (PVA)**, **Laskualennus (PVA)**, **Annettu maksualennus (PVA)** ja **Maksualennus mahdollinen**.

  **Säilytä kentän sisältö** -ominaisuuden avulla voidaan säilyttää myös seuraavien lisäkenttien sisältö: **Asiakirjan nro**, **Tavarantoimittajan nro**, **Ostokoodi**, **Globaali dimensio 1 koodi** ja **Globaali dimensio 2 koodi**.

<!--* General ledger entries
* Customer ledger entries-->
<!--* Fixed asset ledger entries
* G/L budget entries
* VAT entries

  After the compression the contents of the following fields are always retained: **Posting Date**, **Type**, **Closed**, **Gen. Bus. Posting Group**, **Gen. Prod. Posting Group**, **VAT Calculation Type**, **Base**, and **Amount**.

  With the **Retain Field Contents** facility, you can also retain the contents of the following additional fields: **Document No.**, **Bill-to/Pay-to No.**, **EU 3-Party Trade**, **Country/Region Code**, and **Internal Ref. No.**.
* Insurance ledger entries
* Maintenance ledger entries
* Resource ledger entries

  After the compression, the contents of the following fields are retained: **Posting Date**, **Resource No.**, **Resource Group No.**, **Entry Type**, **Quantity**, **Total Cost**, **Total Price**, and **Chargeable**.

  With the **Retain Field Contents** facility, you can also retain the contents of the following additional fields: **Document No.**, **Work Type Code**, **Job No.**, **Unit of Measure Code**, **Source Type**, **Source No.**. **Chargeable**, **
* Warehouse entries

  After the compression the contents of the following fields are always retained: **Registering Date**, **Location Code**, **Zone Code**, **Bin Code**, **Item No.**, **Quantity**, **Qty. (Base)**, **Bin Type Code**, **Entry Type**, **Variant Code**, **Qty. per Unit of Measure**, **Unit of Measure Code**, **Warranty Date**, **Expiration Date**, **Cubage**, and **Weight**.

  With the **Retain Field Contents** facility, you can also retain the contents of the **Serial No.** and **Lot No.** fields. -->

Päivämäärätiivistys-eräajon tuloksena syntyvien tapahtumien määrä perustuu siihen, kuinka monta suodatinta asetat, mitkä kentät yhdistetään ja minkä jakson pituuden valitset. Tapahtumia syntyy aina vähintään yksi. 

> [!WARNING]
> Tiivistys poistaa tapahtumia, joten aina ennen kuin aloitat eräajon, tee varmuuskopio tietokannasta.

Seuraava taulukko sisältää **Vaihtoehdot**-pikavälilehden kentät, jotka ovat käytettävissä kaikissa erätöissä. **Säilytä kentän sisältö** -osassa on lisäkenttiä.

|Kenttä  |Kuvaus  |
|-------|-------------|
|Aloituspvm     |Syötä ensimmäinen tiivistykseen sisällytettävä päivämäärä. Tiivistys vaikuttaa kaikkiin tapahtumiin tästä päivästä lähtien aina lopetuspäivämäärään asti.|
|Lopetuspvm     |Syötä viimeinen tiivistykseen sisällytettävä päivämäärä. Tiivistys vaikuttaa kaikkiin tapahtumiin aloituspäivämäärästä lähtien aina tähän päivään asti.|
|Jakson pituus |Valitse pituus jaksolle, jonka tapahtumat yhdistetään. Valitsemalla kentän näet vaihtoehdot. Jos olet valinnut jakson pituudeksi vaihtoehdon *Vuosineljännes*, *Kuukausi* tai *Viikko*, tiivistyksen kohteeksi tulevat vain ne tapahtumat, joilla on yhteinen kirjanpitojakso.|
|Säilytä kentän sisältö     |Lisää rasti ruutuihin, jos haluat säilyttää tiettyjen kenttien sisällön, vaikka tapahtumat tiivistetään. Mitä useamman kentän valitset, sitä yksityiskohtaisempia tiivistetyt tapahtumat ovat. Jos et valitse mitään näistä kentistä, eräajo luo yhden tapahtuman päivää, viikkoa tai muuta jaksoa kohti, riippuen jaksosta, jonka valitsit **Jakson pituus** -kentässä. |

## <a name="see-also"></a>Katso myös

[Hallinta](admin-setup-and-administration.md)  
