---
title: Määritä arvolisävero
description: Varmista, että lasket, kirjaat ja raportoit myynnin ja ostojen ALV:n oikein. Tämän oppaan käyttö on suositeltavaa ALV:tä määritettäessä.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.search.form: 10, 1877, 470, 471, 472
ms.date: 01/31/2022
ms.author: bholtorf
ms.openlocfilehash: 80264ff085ab9d88a2d6a32d8f0f1189b3622832
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2022
ms.locfileid: "8383669"
---
# <a name="set-up-calculations-and-posting-methods-for-value-added-tax"></a>Arvonlisäveron laskemisen ja kirjaustapojen määrittäminen

Kuluttajat ja yritykset maksavat arvonlisäveroa (ALV:tä), kun he ostavat tavaroita tai palveluja. ALV:n määrä voi vaihdella useiden tekijöiden mukaan. ALV määritetään [!INCLUDE[prod_short](includes/prod_short.md)]issa määrittämään prosentti, jolla verosummat lasketaan, seuraavien parametrien perusteella:

* Kenelle myydään  
* Keneltä ostetaan  
* Mitä myydään  
* Mitä ostetaan  

Voit määrittää ALV-laskelmat manuaalisesti, mutta se voi olla hankalaa ja aikaavievää. Voit helpottaa määritysten tekemistä **ALV-asetusten** ohjatun määrityksen avulla. Tämän oppaan käyttö on suositeltavaa ALV:tä määritettäessä.

> [!NOTE]  
> Voit käyttää opasta vain siinä tapauksessa, että olet luonut oman yrityksen etkä ole kirjannut ALV:n sisältäviä tapahtumia. Muussa tapauksessa on erittäin helppoa käyttää vahingossa eri ALV-prosentteja, mikä johtaisi virheellisiin ALV-raportteihin.  

Jos haluat määrittää ALV-laskelmat itse tai jos haluat lisätietoja kustakin vaiheesta, kukin vaihe käsitellään tässä ohjeaiheessa.  

[!INCLUDE [finance-vat](includes/finance-vat.md)]

## <a name="use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>Käytä ALV-asetusten ohjattua määritysopasta ALV:n määrityksessä (suositus)

Avustetun ALV-asetusten asennus oppaan käyttö on suositeltavaa määritettäessä ALV:tä [!INCLUDE[prod_short](includes/prod_short.md)]issa.

Avaa avustettu asennusopas seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Asetusten ohjattu määritys**.  
2. Valitse **Määritä ALV** ja suorita vaiheet.
3. Kun olet suorittanut avustetut asetukset, käy **ALV-kirjausten asetukset** -sivulla ja tarkista, onko sinun täytettävä lisää kenttiä paikallisen vaatimusten mukaan [!INCLUDE [prod_short](includes/prod_short.md)] -versiossasi. Lisätietoja on kohdassa [Paikalliset toiminnot Business Centralissa](about-localization.md)  

## <a name="set-up-vat-registration-numbers-for-your-country-or-region"></a>Määritä oman maan tai alueen ALV-rekisteröintinumerot

Voit auttaa varmistamaan, että annettavat ALV-rekisteröintinumerot ovat kelvollisia, määrittämällä niiden maiden tai alueiden ALV-rekisteröintinumeroiden muodot, joissa sinulla on liiketoimintaa. [!INCLUDE[prod_short](includes/prod_short.md)] näyttää virhesanoman, kun joku tekee virheen tai käyttää muotoa, jota ei hyväksytä maassa tai alueella.

ALV-rekisteröintinumeroiden määritysohjeet:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 2.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maat/alueet**.
2. Valitse ensin maa tai alue ja sitten **ALV-rekisteröintinron muodot** -toiminto.
3. Määritä muoto **Muodot**-kenttään antamalla vähintään yksi seuraavista merkeistä:  

* **#** - edellyttää yksimerkkistä lukua.  
* **@** - edellyttää kirjainta. Muodon kirjainkoolla ei ole merkitystä.  
* **?** Mikä tahansa merkki sallitaan.  

    > [!Tip]
    > Voit käyttää muita merkkejä, kunhan niitä käytetään maan tai alueen muodossa. Jos sinun on sisällytettävä esimerkiksi numeroiden välinen piste tai yhdysviiva, voit määrittää muodon seuraavasti: ##.####.### tai @@-###-###.  

## <a name="set-up-vat-business-posting-groups"></a>Liiketoiminnan ALV-kirjausryhmien määrittäminen

Liiketoiminnan ALV-kirjausryhmien on vastattava niitä markkinoita, joilla teet kauppaa asiakkaiden ja toimittajien kanssa, ja niiden määritettävä ALV:n laskeminen ja kirjaaminen kullakin markkinalla. Esimerkkejä liiketoiminnan ALV-kirjausryhmistä: **Kotimaa** ja **Euroopan unioni (EU)**.  

Käytä koodeja, jotka on helppo muistaa ja jotka kuvaavat liiketoiminnan kirjausryhmää, kuten **EU**, **Muu kuin EU** tai **Kotimaa**. Koodin tulee olla yksilöivä. Voit määrittää niin monta koodia kuin haluat, mutta koodin on oltava yksilöivä eli sama koodi ei voi olla samassa taulukossa kahdesti.

Liiketoiminnan ALV-kirjausryhmä määritetään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Liiketoim. ALV-kirjausryhmä** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät.

Liiketoiminnan ALV-kirjausryhmien oletusarvot luodaan linkittämällä ne liiketoiminnan kirjausryhmiin. [!INCLUDE[prod_short](includes/prod_short.md)] määrittää automaattisesti liiketoiminnan ALV-kirjausryhmän koodin, kun määrität liiketoiminnan kirjausryhmän asiakkaaseen, toimittajaan tai pääkirjanpidon tiliin.

## <a name="set-up-vat-product-posting-groups"></a>Tuotteen ALV-kirjausryhmien määrittäminen

Tuotteen ALV-kirjausryhmät vastaavat nimikkeitä tai resursseja, joita ostat tai myyt, ja määrittävät ALV:n laskennan ja kirjaamisen ostettavan tai myytävän nimikkeen tai resurssin mukaan.  
Olisi hyvä käyttää koodeja, jotka on helppo muistaa ja joissa on viittaus ALV-prosenttiin, kuten **EI-ALV** tai **Nolla**, **ALV10** tai **Alennettu**, jos ALV on 10 %, ja **ALV25** tai **Vakio**, jos ALV on 25 %.

Liiketoiminnan ALV-kirjausryhmä määritetään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotteen ALV-kirjausryhmät** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>ALV-kirjausryhmien yhdistäminen ALV-kirjausasetuksissa

[!INCLUDE[prod_short](includes/prod_short.md)] laskee myynnin ja ostojen ALV-summat ALV-kirjausryhmien perusteella. Nämä ryhmät puolestaan ovat yhdistelmä liiketoiminnan ja tuotteen ALV-kirjausryhmiä. Voit määrittää kullekin yhdistelmälle ALV-prosentin, ALV-laskennan tyypin sekä myyntiin, ostoihin ja vastakirjaukseen liittyvien ALV-kirjausten pääkirjanpidon tilit. Voit määrittää myös, lasketaanko ALV uudelleen, kun maksualennusta käytetään tai vastaanotetaan.  

Voit määrittää niin monta yhdistelmää kuin haluat. Jos haluat ryhmitellä ALV-kirjausasetusten yhdistelmät, joissa on samanlaiset määritteet, voit määrittää **ALV-tunnuksen** kullekin ryhmälle ja liittää tunnuksen ryhmän jäsenille.

ALV-kirjausasetukset yhdistetään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 5.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-kirjausten asetukset** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät.

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>ALV-kirjausryhmien määrittäminen oletusarvoisesti useille objekteille

Jos haluat käyttää samoja ALV-kirjausryhmiä useissa objekteissa, voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)]in tekemään niin oletusarvoisesti. Määrityksen voi tehdä kahdella tavalla:

* Voit määrittää liiketoiminnan ALV-kirjausryhmät yleisiin liiketoiminnan kirjausryhmiin tai asiakas- tai toimittajamalleihin.
* Voit määrittää tuotteen ALV-kirjausryhmät yleisiin tuotteen kirjausryhmiin.  

Liiketoiminnan tai tuotteen ALV-kirjausryhmä määritetään, kun valitse asiakkaan, toimittajan, nimikkeen tai resurssin liiketoiminnan tai tuotteen kirjausryhmän.

## <a name="assign-vat-posting-groups-to-accounts-customers-vendors-items-and-resources"></a>Määritä ALV-kirjausryhmät yksittäisille tileille, asiakkaille, toimittajille, nimikkeille ja resursseille

Seuraavissa osissa käsitellään ALV-kirjausryhmien määrittämistä yksittäisille objekteille.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>ALV-kirjausryhmien määrittäminen yksittäisille pääkirjanpidon tileille

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 6.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten vastaava linkki.  
2. Avaa valitun tilin **KP-tilin** kortti.  
3. Valitse **Kirjaus**-pikavälilehden **Yleinen kirjaustyyppi** -kentässä joko **Myynti** tai **Osto**.  
4. Valitse myynti- tai ostotilillä käytettävät ALV-kirjausryhmät.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Liiketoiminnan ALV-kirjausryhmien määrittäminen asiakkaille ja toimittajille

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 7.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakas** tai **Toimittaja** ja valitse sitten vastaava linkki.  
2. Laajenna **Laskutus**-pikavälilehti **Asiakas**- tai **Toimittaja**-kortissa.  
3. Valitse liiketoiminnan ALV-kirjausryhmä.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Tuotteen ALV-kirjausryhmien määritetään yksittäisille nimikkeille ja resursseille

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 8.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimike** tai **Resurssi** ja valitse sitten vastaava linkki.  
2. Tee jompikumpi seuraavista toimista:  

    * Laajenna **Nimike**-kortin **Hinta ja kirjaus** -pikavälilehti ja valitse sitten **Näytä lisää**. **Tuotteen ALV-kirjausryhmä** -kenttä avautuu.  
    * Laajenna **Resurssi**-kortissa **Laskutus**-pikavälilehti.  
3. Valitse tuotteen ALV-kirjausryhmä.  

## <a name="set-up-clauses-to-explain-vat-exemption-or-non-standard-vat-rates"></a>Määritä lausekkeet ALV-vapautuksen tai poikkeavien ALV-prosenttien selittämiseksi

Määritä ALV-lause kuvaamaan tietoja käytettävästä ALV-tyypistä. Tietoja voidaan vaatia hallituksen asetuksella. Kun olet määrittänyt ALV-lauseen ja liittänyt sen ALV-kirjausasetukseen, ALV-lause näkyy kaikissa tulostetuissa myyntiasiakirjoissa, jotka käyttävät ALV-kirjausten asetusryhmää.

Voit tarvittaessa määrittää myös, miten ALV-lauseet käännetään muille kielille. Kun luot ja tulostat ALV-tunnuksen sisältävän myyntiasiakirjan, asiakirja sisältää käännetyn ALV-lauseen. Asiakaskortissa määritetty kielikoodi määrittää käytetyn kielen.

Kun poikkeavia ALV-prosentteja käytetään erityyppisissä asiakirjoissa, kuten laskuissa tai hyvityslaskuissa, yritysten on yleensä sisällytettävä vapautusteksti (ALV-lauseke), jossa ilmoitetaan, miksi alennettu ALV tai nolla-ALV on laskettu. Voit määrittää eri ALV-lausekkeita, jotka sisällytetään liiketoiminta-asiakirjoihin asiakirja tyypin mukaan, esimerkiksi laskun tai hyvityslaskun mukaan. Tämä tehdään **ALV-lausekkeet asiakirjatyypin mukaan** -sivulla.

Voit muokata tai poistaa ALV-lauseen, ja muutokset näkyvät luodussa raportissa. [!INCLUDE[prod_short](includes/prod_short.md)] ei kuitenkaan säilytä muutoshistoriaa. Raportissa ALV-lauseen kuvaukset tulostetaan ja näytetään raportin kaikille riveille ALV-summan ja ALV-perusteen summan rinnalla. Jos ALV-lausetta ei ole määritetty millekään myyntiasiakirjan riville, koko osa jätetään pois raporttia tulostettaessa.

### <a name="to-set-up-vat-clauses"></a>ALV-lauseiden määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 9.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-lauseet** ja valitse sitten vastaava linkki.  
2. Luo **ALV-lauseet**-sivulla uusi rivi.  
3. Kirjoita lauseen tunnus **Koodi**-kenttään. Lause määritetään tällä koodilla ALV-kirjausryhmiin.  
4. Kirjoita **Kuvaus**-kenttään ALV-vapautusteksti, jonka haluat näkyvän asiakirjoissa, joihin ALV voi sisältyä. Voit tarvittaessa kirjoittaa lisätekstin **Kuvaus 2** -kenttään. Teksti näkyy uusilla tiedostoriveillä.
5. Valitse **Kuvaus asiakirjatyypin mukaan** -toiminto.
6. Määritä **ALV-lausekkeille asiakirjatyyppi** -sivulla kentät, jotka sisältävät sen ALV-vapautustekstin, jonka asiakirjatyypin haluat näyttää.  
7. Valinnainen: ALV-lauseen voi määrittää ALV-kirjausryhmään heti valitsemalla ensin **Asetukset** ja sitten lauseen. Jos halua odottaa, voit määrittää lauseen myöhemmin **ALV-kirjausten asetukset** -sivulla.  
8. Valinnainen: Valitsemalla **Käännökset** toiminnon voit määrittää, miten ALV-lause käännetään.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>ALV-lauseen määrittäminen ALV-kirjausryhmään

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 10.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-kirjausten asetukset** ja valitse sitten vastaava linkki.  
2. Valitse **ALV-lause**-sarakkeessa lause, jota käytetään kussakin ALV-kirjauksen asetuksissa, joihin sitä sovelletaan.  

### <a name="to-specify-translations-for-vat-clauses"></a>ALV-lauseiden käännösten määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 11.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-lauseet** ja valitse sitten vastaava linkki.  
2. Valitse **Käännökset**-toiminto.  
3. Valitse **Kielikoodi**-kentässä kieli, jolle käännetään.  
4. Kirjoita kuvausten käännökset **Kuvaus**- ja **Kuvaus 2** -kenttiin. Tämä teksti näkyy käännetyissä ALV-raporttiasiakirjoissa.  

## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>ALV-kirjausten asetukset luominen käsittelemään tuonnin ALV:tä

*Tuonnin ALV* -ominaisuudella kirjataan asiakirja, jossa koko summaa on ALV:tä. Tämä on tarpeellista, jos saat veroviranomaisilta laskun tuontitavaroiden arvonlisäverosta.  

Määritä tuonnin ALV:n koodit seuraavasti:  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 12.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotteen ALV-kirjausryhmät** ja valitse sitten vastaava linkki.  
2. Määritä Tuotteen ALV-kirjausryhmät -sivulla uusi tuotteen ALV-kirjausryhmä tuonnin ALV:tä varten.  
3. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 13.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-kirjausten asetukset** ja valitse sitten vastaava linkki.  
4. Luo ALV-kirjausten asetukset -sivulla uusi rivi tai käytä aiemmin luotua liiketoiminnan ALV-kirjausryhmää yhdessä tuonnin ALV:tä varten luodun uuden tuotteen ALV-kirjausryhmän kanssa.  
5. Valitse **ALV-laskennan tyyppi** -kentässä **Täysi ALV**.  
6. Anna **Ostojen ALV-tili** -kentässä se pääkirjanpidon tili, jota käytetään tuonnin ALV:n kirjaamiseen. Kaikki muut tilit ovat valinnaisia.  

## <a name="use-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>ALV-vastakirjauksen käyttäminen EU-maiden tai -alueiden välisessä kaupassa

Joiden yritysten on käytettävä ALV-vastakirjausta tehdessään kauppaa muiden yritysten kanssa. Sääntö koskee esimerkiksi EU:n maiden tai alueiden välisiä myyntejä ja ostoja.  

> [!NOTE]  
> Tämä sääntö on voimassa, kun käydään kauppaa yritysten kanssa, jotka ovat ALV-velvollisia toisessa EU-maassa / toisella EU-alueella. Jos harjoitat liiketoimintaa suoraan muiden EU-maiden/alueiden kuluttajien kanssa, pyydä soveltuvat ALV-säännöt veroviranomaisilta.  

> [!TIP]  
> Voit tarkistaa EU:n ALV-rekisteröintinumeron vahvistuspalvelun avulla, onko yritys rekisteröity ALV-velvolliseksi toisessa EU-maassa. Palvelua voi käyttää maksutta [!INCLUDE[prod_short](includes/prod_short.md)]issa. Lisätietoja on ohje aiheessa [ALV-rekisterinumeroiden vahvistaminen](finance-how-validate-vat-registration-number.md).

### <a name="sales-to-eu-countries-or-regions"></a>Myynti EU-maihin tai -alueille

ALV:tä ei lasketa myynneistä muiden EU-maiden/alueiden ALV-velvollisille yrityksille. Näiden EU-maihin/alueille tapahtuvien myyntien arvo on raportoitava erikseen ALV-ilmoituksessa.  

Laskeaksesi asianmukaisesti ALV:t myynneistä EU-maissa/-alueilla, sinun pitäisi:  

* Määritä myyntirivi, jossa on samat tiedot kuin ostoja varten. Jos olet jo määrittänyt rivejä EU-maista/alueilta tapahtuvia ostoja varten ALV-kirjausten asetukset -sivulla, voit käyttää näitä rivejä myös myynteihin.  
* Liitä liiketoiminnan ALV-kirjausryhmät asiakkaan kortin **Laskutus**-pikavälilehden **Liiketoiminnan ALV-kirjausryhmä** -kenttään kullekin EU-asiakkaalle. Asiakkaan ALV-rekisterinumero on myös lisättävä **Ulkomaankauppa**-pikavälilehden **ALV-rekisterinro**-kenttään.  

Kun kirjaat myynnin toisen EU-maan/alueen asiakkaalle, ohjelma laskee ALV-summan ja luo ALV-tapahtuman, jossa on tiedot ALV-vastakirjauksesta ja ALV-perusteesta (ALV-summan laskemiseen käytettävästä summasta). Yleisen päiväkirjan ALV-tileille ei kirjata tapahtumia.

## <a name="vat-rounding-for-documents"></a>ALV:n pyöristäminen asiakirjoja varten

Vielä kirjaamattomien asiakirjojen summat pyöristetään ja näytetään kirjattujen summien lopullista pyöristämistä vastaavalla tavalla. ALV lasketaan koko asiakirjalle, mikä tarkoittaa sitä, että laskettu ALV perustuu kaikkien rivien summaan, joilla on sama ALV-tunnus asiakirjassa.  

## <a name="set-up-vat-reporting"></a>Määritä ALV-raportointi

Sinun on määritettävä tiedot siitä, mitä vaatimuksia maasi veroviranomaisella on ALV-raporttien lähettämisen suhteen. Seuraavissa vaiheissa kuvataan yleisimmin käytettävät tiedot. Maasi tai alueesi voi kuitenkin edellyttää muitakin vaiheita. Lisätietoja saat asianomaisesta artikkelista vasemman paneelin *Paikalliset toiminnot* -osasta.

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

## <a name="see-also"></a>Katso myös

[ALV-ilmoitusmallien ja ALV-ilmoitusten nimien määrittäminen](finance-how-setup-vat-statement.md)  
[Ei-realisoituneen arvonlisäveron määrittäminen](finance-setup-unrealized-vat.md)  
[ALV:n raportointi veroviranomaisille](finance-how-report-vat.md)  
[Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md)  
[ALV-kannan muutostyökalun käyttö](finance-how-use-vat-rate-change-tool.md)  
[ALV-rekisterinumeroiden tarkistaminen](finance-how-validate-vat-registration-number.md)  
[Business Centralin paikalliset toiminnot](about-localization.md)  

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)


[!INCLUDE[footer-include](includes/footer-banner.md)]
