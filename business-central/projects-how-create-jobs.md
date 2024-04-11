---
title: Projektin projektikortin luominen ja tehtävien määrittäminen
description: 'Uudelle projektille luodaan projektin tehtävät ja suunnittelurivit sisältävä projektikortti, mikä auttaa edistymisen ja budjettien hallinnassa.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.search.keywords: 'project management, task'
ms.search.form: '88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-projects"></a>Projektien luominen

Uuden projektin aloittamisen yhteydessä on luotava projektikortti sekä integroidut projektitehtävät ja projektin suunnittelurivit, jotka on jäsennetty kahteen kerrokseen.  

Ensimmäinen kerros koostuu projektitehtävistä. Projektikohtaisesti on luotava vähintään yksi projektitehtävä, koska kirjaukset viittaavat projektitehtävään. Kun projektissa on vähintään yksi projektitehtävä, voit määrittää projektin suunnittelurivejä ja kirjata projektin kulutuksen.

Toinen kerros koostuu projektin suunnitteluriveistä, jotka määrittävät yksityiskohtaisesti resurssien ja nimikkeiden käytön sekä erilaiset kirjanpidon kulut.

Kerroksen rakenteen avulla projekti voidaan jakaa projektin pieniksi tehtäviksi, jolloin budjetointiin, tarjouksiin ja rekisteröintiin saadaan tarkempia tietoja. Lisäksi sen avulla saadaan tietoja projektin etenemisestä. Voit seurata esimerkiksi sitä, miten olet saavuttanut määritetyt välitavoitteet tai oletko saavuttamassa budjettiin määritetyt tavoitteet.

> [!TIP]
> Käynnistä asetusten ohjattu määritys valitsemalla **Uusi projekti** -toiminto **Projektipäällikkö**-roolikeskuksessa. Ohjattu määritys ohjaa vaihe vaiheelta projektin ja integroitujen tehtävien ja suunnittelurivien luonnissa. Seuraavassa kerrotaan, miten vaiheet suoritetaan manuaalisesti. <!-- For an example of how to create a project manually, go to [Video: How to create a project in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).-->

## <a name="invoice-one-or-more-customers-for-project-tasks"></a>Projektitehtävien laskuttaminen yhdeltä tai usealta asiakkaalta

Joskus palvelua vastaanottava osapuoli eroaa laskun maksavasta osapuolesta. Ja joskus projektin tehtäviä on myös laskutettava useilta asiakkailta. Määritä **Projektikortti**-sivun **Tehtävän laskutustapa** -kentässä, laskutetaanko yhtä vai useaa asiakasta.

Jos palvelun vastaanottava asiakas myös maksaa laskun, valitse**Laskutusasiakas**- ja **Toimitusasiakas**-kentissä **Oletus (asiakas)** ja **Oletus (tilausasiakkaan osoite)**.

Jos laskutettavia asiakkaita on useita, palvelun vastaanottava asiakas ja laskutettava asiakas voidaan määrittää projektin kunkin tehtävän osalta. Voit antaa myös seuraavat tiedot:

* Valitse työn suorituspaikka asiakkaan toimitusasiakkaiden osoitteiden luettelosta.
* Lisää ulkoisten viitteiden tietoja yksinkertaistaaksesi projektia koskevaa viestintää.
* Korvaa projektin vakiotalousehdot.

## <a name="invoice-one-customer-for-multiple-project-tasks"></a>Useiden projektitehtävien laskuttaminen yhdeltä asiakkaalta

Laskutusprosessia voidaan yksinkertaistaa lähettämällä asiakkaalle yksi lasku, joka sisältää useita projekteja. Useiden projektien projektin suunnittelurivit lisätään kerralla myyntilaskuun. Tämä prosessi muistuttaa myyntilaskun luontia projektin suunnitteluriviltä ja arvon syöttämistä **Liitä myyntilaskun nroon** -kenttään.

Prosessin yleiskatsaus:

1. Luo uusi myyntilasku ja määritä arvo **Tilausasiakkaan nro** -kentässä. Täytä tarvittaessa myös **Laskutusasiakkaan nro**- ja **Valuuttakoodi**-kentät.
2. Valitse **Rivit**-pikavälilehdessä **Hae projektin suunnittelurivit** -toiminto. **Hae projektin suunnittelurivit** -sivulla on näkyvissä tilausasiakkaan projektien laskutettavat projektin suunnittelurivit, laskutusasiakas ja laskutusvaluutta, jos laskutettava määrä on suurempi kuin nolla. 
3. Valitse laskuun lisättävät rivit ja valitse sitten **OK**.

Toista nämä vaiheet, jos haluat lisätä toiseen projektin suunnittelurivijoukon. Lasku tai sen rivit voidaan myös poistaa ja aloittaa alusta.

> [!NOTE]
> Rajoitukset:
>
> * **Hae projektin suunnittelurivit** -toiminto ei ole saatavana myyntitilauksissa tai myyntitarjouksissa.
> * Suodatus ei ole mahdollista **Toimitusasiakkaan koodi**- tai **Yhteyshenkilön nro** -kentässä.

## <a name="to-create-a-project-card"></a>Projektikortin luominen

Ensin luodaan projektikortti, jonka jälkeen sille luodaan projektitehtävä ja projektin suunnittelurivit.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projekti** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto ja täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Projektin perustana voi käyttää toisen projektin tietoja valitsemalla **Kopioi projekti** -toiminto, täyttämällä tarvittavat kentät ja valitsemalla sitten **OK**-painikkeen.

> [!NOTE]  
> Jos projektissa käytetään aikaraportteja, myös vastuussa oleva henkilö on määritettävä. Tämä henkilö voi hyväksyä projektiin liitettyjen työntekijätehtävien tuntiraportit. Lisätietoja on kohdassa [Aikaraporttien määrittäminen](projects-how-setup-time-sheets.md).

Voit halutessasi merkitä projektin toimintoja estetyiksi **Estetty**-kentän avulla Seuraavassa taulukossa kuvataan tämän kentän vaihtoehtojen vaikutukset.

|Asetus  |Kuvaus  |
|---------|---------|
|Tyhjä |Kaikki toimenpiteet ovat sallittuja.|
|Kirjaus    |Vaikka suunnittelurivejä voidaan käsitellä, projektin kirjaus on estetty. Jos valitset tämän vaihtoehdon, projektin käyttöä tai myyntiä ei voi kirjata.|
|Kaikki  |Kaikki toimenpiteet ovat suljettuja.|

## <a name="to-create-tasks-for-a-project"></a>Tehtävien luonti projektiin

Projektin luonnin keskeinen osa on määrittää siihen liittyvät tehtävät. Voit määrittää tehtäviä luomalla yhden rivin tehtävää kohti **Projektikortti**-sivun **Tehtävät**-pikavälilehdessä. Jokaisella projektilla on oltava vähintään yksi tehtävä.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projekti** ja valitse sitten vastaava linkki.
2. Avaa soveltuvan projektin projektikortti.
3. Täytä **Tehtävät**-pikavälilehden uuden rivin kentät tarvittaessa.
4. Tehtäviä voidaan sisentää hierarkian luontia varten valitsemalla **Tehtävät**-toiminto ja valitsemalla sitten **Sisennä projektitehtävät** -toiminto.
5. Toista vaiheet 3 ja 4 kaikille projektissa tarvittaville tehtäville.
6. Projektitehtäville voidaan määrittää tietoja muista projektitehtävistä valitsemalla **Kopioi projektitehtävät kohteesta** -toiminto, täyttämällä tarvittavat kentät ja valitsemalla sitten **OK**-painikkeen.

## <a name="to-create-planning-lines-for-a-project"></a>Projektin suunnittelurivien luominen

Uusia projektitehtäviä voidaan tarkentaa projektin suunnitteluriveillä. Suunnittelurivi voi sieppaa tiedot, joita halutaan seurata projektissa. Seurata voidaan esimerkiksi projektin tarvitsemia resursseja tai nimikkeitä. Käytettävissä on esimerkiksi tehtävä, jolla asiakas saadaan hyväksymään projekti. Tehtävä liitetään nimikkeiden suunnitteluriveihin, esimerkiksi asiakastapaamiseen tai resurssin liittämiseen.  

Projektin suunnittelurivin tyyppi voi olla jokin seuraavista tyypeistä.  

| Tyyppi | Kuvaus |
| --- | --- |
| **Budjetti** |Projektin käytön ja kustannusten arviointi, yleensä Aika ja materiaali -tyyppisessä projektissa. Tämän tyyppisiä suunnittelurivejä ei voi laskuttaa. |
| **Laskutettava** |Asiakkaan arviolaskutus, yleensä kiinteähintainen projekti. |
| **Sekä budjetti että laskutettava** |Budjetoitu käyttö on sama kuin laskutettava käyttö. |

> [!NOTE]
> Kustannustiedot täytetään automaattisesti projektin suunnittelurivien tietojen lisäyksen aikana. Esimerkiksi resurssien ja nimikkeiden kustannus, hinta ja alennus perustuvat resurssin ja nimikkeen tietoihin.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projekti** ja valitse sitten vastaava linkki.
2. Avaa sopiva projektikortti.
3. Valitse projektitehtävä, jonka **Projektitehtävän tyyppi** -kentän arvo on **Kirjaus**. Valitse sitten **Projektin suunnittelurivit** -toiminto.  
4. Täytä **Projektin suunnittelurivit** -sivulla tarvittavat kentät uudella rivillä.
5. Toista vaiheet 3 ja 4 kaikille projektitehtävässä tarvittaville suunnitteluriveille.

## <a name="see-also"></a>Katso myös

[Projektien hallinta](projects-manage-projects.md)  
[Video: Projektin luonti Dynamics 365 Business Centralissa](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Taloushallinto](finance.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
