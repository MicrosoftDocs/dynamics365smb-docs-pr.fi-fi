---
title: Päätietojen synkronoinnin hallinta
description: Tietoja päätietojen synkronoinnin hallinnasta
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---
# <a name="manage-master-data-synchronization" />Päätietojen synkronoinnin hallinta

Kun olet määrittänyt päätietojen synkronoinnin ja synkronoinnin ensimmäisen kerran, valittujen taulukoiden tietueet yhdistetään ja jokaiselle taulukolle luodaan toistuva työjonotapahtuma. Työjonotapahtumat synkronoivat automaattisesti tytäryritysten tiedot, kun joku tekee muutoksen lähdeyrityksessä. Muussa tapauksessa sinun ei tarvitse tehdä mitään.

> [!NOTE]
> Työjonotapahtumat ajoitetaan oletusarvoisesti joka minuutti, etkä voi muuttaa aikataulua.

Joskus asiat menevät kuitenkin pieleen, ja voi olla tilanteita, joita sinun täytyy hallita tai tutkia. Jos esimerkiksi ihmiset muuttavat samaa tietuetta sekä lähdeyrityksessä että tytäryrityksessä, synkronointi epäonnistuu, että voit määrittää oikean muutoksen. Lähdeyritys voi myös asentaa laajennuksen, joka muuttaa jommankumman taulukon rakennetta lisäämällä kentän tai kaksi synkronointia. Jos haluat synkronoida tytäryritysten uudet kentät, sinun täytyy asentaa samat laajennukset ja päivittää taulukkomallit niiden asetuksissa.

Tässä artikkelissa kuvataan työkalut, joita voit käyttää synkronoinnin sujuvuuden säilyttämiseksi.

## <a name="investigate-the-status-of-synchronization" />Synkronoinnin tilan tarkasteleminen

**Synkronointitaulukot**-sivulla on kaksi toimintoa, joiden avulla voit seurata synkronointia:

* **Integroinnin synkronointityöt**
* **Työjonon tapahtumat**

Toiminnot kuvaillaan seuraavassa taulukossa.

|Sivu  |Kuvaus  |
|---------|---------|
|**Integroinnin synkronointityöt**     | Avaa **Integroinnin synkronointityöt** -sivu, jossa voit selvittää, mitä tapahtui aina, kun työjonotapahtuma suoritettiin. Jos haluat lisätietoja lisättyjen uusien tietueiden yksityiskohdista tai selvittää, miksi tietuetta ei voitu synkronoida, valitse luvut **Lisätyt**- tai **Epäonnistuneet**-sarakkeista. Tämän sivun avulla voit myös poistaa vanhoja tietueita, joita et välttämättä tarvitse. Lisätietoja sijaintien tyhjentämisestä on kohdassa [Vanhojen merkintöjen poistaminen](#clean-up-old-entries).        |
|**Työjonon tapahtumat**     | Tarkastele tietoja työjonomerkinnästä, joka synkronoi valitun taulukon tiedot. Käytä tätä sivua esimerkiksi työjonotapahtuman tilan hallintaan, lisätietoja työjonon tapahtumista on kohdassa [Työjonojen käyttäminen tehtävien ajoituksessa](admin-job-queues-schedule-tasks.md).     |

> [!NOTE]
> Jos huomaat **synkronoinnin integrointityöt** -sivulla virheen, jota et pysty ratkaisemaan itse, on hyödyllistä antaa virheilmoitus ja kutsupinotiedot, jos otat yhteyttä kumppaniin tai Microsoftiin.

## <a name="synchronize-modified-records" />Synkronoi muokatut tietueet

Jos muutat taulukon tai kentän asetusta tytäryrityksessä, synkronointi täytyy päivittää. Jos esimerkiksi päätät valita **Korvaa paikallinen muutos** -valintaruudun kentässä, jotta lähdeyrityksen tiedot voivat korvata paikalliset muutokset. Voit päivittää synkronoinnin käyttämällä **Synkronoi muokatut tietueet** -toimintoa **Synkronointitaulukot**-sivulla.

## <a name="update-table-schemas" />Päivitä taulukkomallit

Jos lähdeyritys muuttaa taulukkoa esimerkiksi lisäämällä synkronoitavan kentän, tytäryritysten on päivitettävä kenttien yhdistämismääritykset. Käytä **Synkronointi kentät** -sivulla **Päivitä kentät** -toimintoa. 

## <a name="enable-or-disable-couplings-between-records" />Tietueiden välisten liitosten ottaminen käyttöön tai poistaminen käytöstä

Voit käynnistää tai pysäyttää tiettyjen taulukon tietueiden yhdistämisen valitsemalla **Synkronointikentät**-sivulla kentät ja käyttämällä sitten joko **Ota käyttöön**- tai **Poista käytöstä** -toimintoa. 

> [!TIP]
> Nopea tapa ottaa useita kenttiä käyttöön tai poistaa ne käytöstä samanaikaisesti on valita ne luettelosta ja käyttää sitten joko **Ota käyttöön**- tai **Poista käytöstä** -toimintoa.

## <a name="adding-extensions" />Laajennusten lisääminen

Jos lähdeyritys asentaa uuden laajennuksen, myös tytäryrityksen täytyy asentaa se, jos se haluaa synkronoida tietoja. Tytäryritys voi lisätä taulukot laajennuksesta luetteloon **Synkronointikentät**-sivun **Päivitä kentät** -toiminnon avulla.

> [!NOTE]
> Jotkin taulukot saavat tietoja liittyvistä taulukoista. Jos lisäät tunnisteen, joka ei sisällä toisiinsa liittyviä taulukoita, näiden taulukoiden kentät eivät ole käytettävissä. Varmista, että olet lisännyt kaikki liittyvät taulukot.

## <a name="clean-up-old-entries" />Siivoa vanhat tapahtumat

Ajan mittaan synkronointilokin tapahtumien lukumäärä muuttuu isoksi, joten sinun kannattaa vähän siivota tarpeettomien merkintöjen poistamiseksi. Jotta vanhojen merkintöjen poistaminen olisi helpompaa, **integroinnin synkronointityöt** -sivulla on seuraavat toiminnot:

* **Poista yli 7 päivää vanhat tapahtumat**
* **Poista kaikki tapahtumat**

<!--
## <a name="recreate-a-deleted-job-queue-entry" />Recreate a deleted job queue entry

If the recurring job queue entry is deleted for a table, you can quickly recreate it. On the **Synchronization Tables** page, choose the **Use Default Synchronization Setup** action.
-->

## <a name="see-also" />Katso myös

[Päätietojen synkronointiin valmistautuminen](admin-set-up-data-sync.md)
