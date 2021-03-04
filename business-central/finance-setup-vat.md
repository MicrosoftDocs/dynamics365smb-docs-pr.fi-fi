---
title: Tietoja arvonlisäveron määrittämisestä | Microsoft Docs
description: Varmista, että lasket, kirjaat ja raportoit myynnin ja ostojen ALV:n oikein.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: e0ce2d6c5a2d524cf150bc6e3b50f243fe42b4d9
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750328"
---
# <a name="set-up-value-added-tax"></a>Määritä arvolisävero

Kuluttajat ja yritykset maksavat arvonlisäveroa (ALV:tä), kun he ostavat tavaroita tai palveluja. ALV:n määrä voi vaihdella useiden tekijöiden mukaan. ALV määritetään [!INCLUDE[prod_short](includes/prod_short.md)]issa määrittämään prosentti, jolla verosummat lasketaan, seuraavien tekijöiden perusteella:

* Kenelle myydään  
* Keneltä ostetaan  
* Mitä myydään  
* Mitä ostetaan  

Voit määrittää ALV-laskelmat manuaalisesti, mutta se voi olla hankalaa ja aikaavievää. Voit helpottaa määritysten tekemistä **ALV-asetusten** ohjatun määrityksen avulla. Tämän oppaan käyttö on suositeltavaa ALV:tä määritettäessä.

> [!NOTE]  
> Voit käyttää opasta vain siinä tapauksessa, että olet luonut oman yrityksen etkä ole kirjannut ALV:n sisältäviä tapahtumia. Muussa tapauksessa on erittäin helppoa käyttää vahingossa eri ALV-prosentteja, mikä johtaisi virheellisiin ALV-raportteihin.  

Jos haluat määrittää ALV-laskelmat itse tai jos haluat lisätietoja kustakin vaiheesta, kukin vaihe käsitellään tässä ohjeaiheessa.

## <a name="to-use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>ALV-asetusten ohjatun määritysoppaan käyttäminen ALV:n määrityksessä (suositus)

Avustetun ALV-asetusten asennus oppaan käyttö on suositeltavaa määritettäessä ALV:tä [!INCLUDE[prod_short](includes/prod_short.md)]issa.

Avaa avustettu asennusopas seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asetusten ohjattu määritys**.  
2. Valitse **Määritä ALV** ja suorita vaiheet.
3. Kun olet suorittanut avustetut asetukset, käy **ALV-kirjausten asetukset** -sivulla ja tarkista, onko sinun täytettävä lisää kenttiä paikallisen vaatimusten mukaan [!INCLUDE [prod_short](includes/prod_short.md)] -versiossasi. Lisätietoja on kohdassa [Paikalliset toiminnot Business Centralissa](about-localization.md)  

## <a name="to-set-up-vat-registration-numbers-for-your-country-or-region"></a>Oman maan tai alueen ALV-rekisteröintinumeroiden määrittäminen

Voit auttaa varmistamaan, että annettavat ALV-rekisteröintinumerot ovat kelvollisia, määrittämällä niiden maiden tai alueiden ALV-rekisteröintinumeroiden muodot, joissa sinulla on liiketoimintaa. [!INCLUDE[prod_short](includes/prod_short.md)] näyttää virhesanoman, kun joku tekee virheen tai käyttää muotoa, jota ei hyväksytä maassa tai alueella.

ALV-rekisteröintinumeroiden määritysohjeet:

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maat/alueet**.
2. Valitse ensin maa tai alue ja sitten **ALV-rekisteröintinron muodot** -toiminto.
3. Määritä muoto **Muodot**-kenttään antamalla vähintään yksi seuraavista merkeistä:  

* **#** - edellyttää yksimerkkistä lukua.  
* **@** - edellyttää kirjainta. Kirjainkoolla ei ole merkitystä.  
* **?** Mikä tahansa merkki sallitaan.  

    > [!Tip]
    > Voit käyttää muita merkkejä, kunhan niitä käytetään maan tai alueen muodossa. Jos sinun on sisällytettävä esimerkiksi numeroiden välinen piste tai yhdysviiva, voit määrittää muodon seuraavasti: ##.####.### tai @@-###-###.  

## <a name="to-set-up-vat-business-posting-groups"></a>Liiketoiminnan ALV-kirjausryhmien luominen
Liiketoiminnan ALV-kirjausryhmien on vastattava niitä markkinoita, joilla teet kauppaa asiakkaiden ja toimittajien kanssa, ja niiden määritettävä ALV:n laskeminen ja kirjaaminen kullakin markkinalla. Esimerkkejä liiketoiminnan ALV-kirjausryhmistä: **Kotimaa** ja **Euroopan unioni (EU)**.  

Käytä koodeja, jotka on helppo muistaa ja jotka kuvaavat liiketoiminnan kirjausryhmää, kuten **EU**, **Muu kuin EU** tai **Kotimaa**. Koodin tulee olla yksilöivä. Voit määrittää niin monta koodia kuin haluat, mutta koodin on oltava yksilöivä eli sama koodi ei voi olla samassa taulukossa kahdesti.

Liiketoiminnan ALV-kirjausryhmä määritetään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-yrityskirjausryhmä** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät.

Liiketoiminnan ALV-kirjausryhmien oletusarvot luodaan linkittämällä ne liiketoiminnan kirjausryhmiin. [!INCLUDE[prod_short](includes/prod_short.md)] määrittää automaattisesti liiketoiminnan ALV-kirjausryhmän koodin, kun määrität liiketoiminnan kirjausryhmän asiakkaaseen, toimittajaan tai pääkirjanpidon tiliin.

## <a name="to-set-up-vat-product-posting-groups"></a>Tuotteen ALV-kirjausryhmien luominen
Tuotteen ALV-kirjausryhmät vastaavat nimikkeitä tai resursseja, joita ostat tai myyt, ja määrittävät ALV:n laskennan ja kirjaamisen ostettavan tai myytävän nimikkeen tai resurssin mukaan.  
Olisi hyvä käyttää koodeja, jotka on helppo muistaa ja joissa on viittaus ALV-prosenttiin, kuten **EI-ALV** tai **Nolla**, **ALV10** tai **Alennettu**, jos ALV on 10 %, ja **ALV25** tai **Vakio**, jos ALV on 25 %.

Liiketoiminnan ALV-kirjausryhmä määritetään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-tuotekirjausryhmät** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät.

## <a name="to-combine-vat-posting-groups-in-vat-posting-setups"></a>ALV-kirjausryhmien yhdistäminen ALV-kirjausasetuksissa
[!INCLUDE[prod_short](includes/prod_short.md)] laskee myynnin ja ostojen ALV-summat ALV-kirjausryhmien perusteella. Nämä ryhmät puolestaan ovat yhdistelmä liiketoiminnan ja tuotteen ALV-kirjausryhmiä. Voit määrittää kullekin yhdistelmälle ALV-prosentin, ALV-laskennan tyypin sekä myyntiin, ostoihin ja vastakirjaukseen liittyvien ALV-kirjausten pääkirjanpidon tilit. Voit määrittää myös, lasketaanko ALV uudelleen, kun maksualennusta käytetään tai vastaanotetaan.  

Voit määrittää niin monta yhdistelmää kuin haluat. Jos haluat ryhmitellä ALV-kirjausasetusten yhdistelmät, joissa on samanlaiset määritteet, voit määrittää **ALV-tunnuksen** kullekin ryhmälle ja liittää tunnuksen ryhmän jäsenille.

ALV-kirjausasetukset yhdistetään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-kirjauksien asetukset** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät.

## <a name="to-assign-vat-posting-groups-by-default-to-multiple-entities"></a>ALV-kirjausryhmien määrittäminen oletusarvoisesti useille objekteille
Jos haluat käyttää samoja ALV-kirjausryhmiä useissa objekteissa, voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)]in tekemään niin oletusarvoisesti. Määrityksen voi tehdä kahdella tavalla:

* Voit määrittää liiketoiminnan ALV-kirjausryhmät yleisiin liiketoiminnan kirjausryhmiin tai asiakas- tai toimittajamalleihin.
* Voit määrittää tuotteen ALV-kirjausryhmät yleisiin tuotteen kirjausryhmiin.  

Liiketoiminnan tai tuotteen ALV-kirjausryhmä määritetään, kun valitse asiakkaan, toimittajan, nimikkeen tai resurssin liiketoiminnan tai tuotteen kirjausryhmän.

## <a name="assigning-vat-posting-groups-to-accounts-customers-vendors-items-and-resources"></a>ALV-kirjausryhmien määrittäminen yksittäisille tileille, asiakkaille, toimittajille, nimikkeille ja resursseille
Seuraavissa osissa käsitellään ALV-kirjausryhmien määrittämistä yksittäisille objekteille.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>ALV-kirjausryhmien määrittäminen yksittäisille pääkirjanpidon tileille
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten liittyvä linkki.  
2. Avaa valitun tilin **KP-tilin** kortti.  
3. Valitse **Kirjaus**-pikavälilehden **Yleinen kirjaustyyppi** -kentässä joko **Myynti** tai **Osto**.  
5. Valitse myynti- tai ostotilillä käytettävät ALV-kirjausryhmät.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Liiketoiminnan ALV-kirjausryhmien määrittäminen asiakkaille ja toimittajille  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakas** tai **Toimittaja** ja valitse sitten liittyvä linkki.  
2. Laajenna **Laskutus**-pikavälilehti **Asiakas**- tai **Toimittaja**-kortissa.  
3. Valitse liiketoiminnan ALV-kirjausryhmä.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Tuotteen ALV-kirjausryhmien määritetään yksittäisille nimikkeille ja resursseille  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimike** tai **Resurssi** ja valitse sitten liittyvä linkki.  
2. Tee jompikumpi seuraavista toimista:  

* Laajenna **Nimike**-kortin **Hinta ja kirjaus** -pikavälilehti ja valitse sitten **Näytä lisää**. **Tuotteen ALV-kirjausryhmä** -kenttä avautuu.  
* Laajenna **Resurssi**-kortissa **Laskutus**-pikavälilehti.  
3. Valitse tuotteen ALV-kirjausryhmä.  

## <a name="setting-up-clauses-to-explain-vat-exemption-or-non-standard-vat-rates"></a>Lausekkeiden määrittäminen ALV-vapautuksen tai poikkeavien ALV-prosenttien selittämiseksi
Määritä ALV-lause kuvaamaan tietoja käytettävästä ALV-tyypistä. Tietoja voidaan vaatia hallituksen asetuksella. Kun olet määrittänyt ALV-lauseen ja liittänyt sen ALV-kirjausasetukseen, ALV-lause näkyy kaikissa tulostetuissa myyntiasiakirjoissa, jotka käyttävät ALV-kirjausten asetusryhmää.

Voit tarvittaessa määrittää myös, miten ALV-lauseet käännetään muille kielille. Kun luot ja tulostat ALV-tunnuksen sisältävän myyntiasiakirjan, asiakirja sisältää käännetyn ALV-lauseen. Asiakaskortissa määritetty kielikoodi määrittää käytetyn kielen.

Kun poikkeavia ALV-prosentteja käytetään erityyppisissä asiakirjoissa, kuten laskuissa tai hyvityslaskuissa, yritysten on yleensä sisällytettävä vapautusteksti (ALV-lauseke), jossa ilmoitetaan, miksi alennettu ALV tai nolla-ALV on laskettu. Voit määrittää eri ALV-lausekkeita, jotka sisällytetään liiketoiminta-asiakirjoihin asiakirja tyypin mukaan, esimerkiksi laskun tai hyvityslaskun mukaan. Tämä tehdään **ALV-lausekkeet asiakirjatyypin mukaan** -sivulla.

Voit muokata tai poistaa ALV-lauseen, ja muutokset näkyvät luodussa raportissa. [!INCLUDE[prod_short](includes/prod_short.md)] ei kuitenkaan säilytä muutoshistoriaa. Raportissa ALV-lauseen kuvaukset tulostetaan ja näytetään raportin kaikille riveille ALV-summan ja ALV-perusteen summan rinnalla. Jos ALV-lausetta ei ole määritetty millekään myyntiasiakirjan riville, koko osa jätetään pois raporttia tulostettaessa.

### <a name="to-set-up-vat-clauses"></a>ALV-lauseiden määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-lausekkeet** ja valitse sitten liittyvä linkki.  
2. Luo **ALV-lauseet**-sivulla uusi rivi.  
3. Kirjoita lauseen tunnus **Koodi**-kenttään. Lause määritetään tällä koodilla ALV-kirjausryhmiin.  
4. Kirjoita **Kuvaus**-kenttään ALV-vapautusteksti, jonka haluat näkyvän asiakirjoissa, joihin ALV voi sisältyä. Voit tarvittaessa kirjoittaa lisätekstin **Kuvaus 2** -kenttään. Teksti näkyy uusilla tiedostoriveillä.
5. Valitse **Kuvaus asiakirjatyypin mukaan** -toiminto.
6. Määritä **ALV-lausekkeille asiakirjatyyppi** -sivulla kentät, jotka sisältävät sen ALV-vapautustekstin, jonka asiakirjatyypin haluat näyttää.  
7. Valinnainen: ALV-lauseen voi määrittää ALV-kirjausryhmään heti valitsemalla ensin **Asetukset** ja sitten lauseen. Jos halua odottaa, voit määrittää lauseen myöhemmin **ALV-kirjausten asetukset** -sivulla.  
8. Valinnainen: Valitsemalla **Käännökset** toiminnon voit määrittää, miten ALV-lause käännetään.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>ALV-lauseen määrittäminen ALV-kirjausryhmään
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-kirjauksien asetukset** ja valitse sitten liittyvä linkki.  
2. Valitse **ALV-lause**-sarakkeessa lause, jota käytetään kussakin ALV-kirjauksen asetuksissa, joihin sitä sovelletaan.  

### <a name="to-specify-translations-for-vat-clauses"></a>ALV-lauseiden käännösten määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-lausekkeet** ja valitse sitten liittyvä linkki.  
2. Valitse **Käännökset**-toiminto.  
3. Valitse **Kielikoodi**-kentässä kieli, jolle käännetään.  
4. Kirjoita kuvausten käännökset **Kuvaus**- ja **Kuvaus 2** -kenttiin. Tämä teksti näkyy käännetyissä ALV-raporttiasiakirjoissa.  

## <a name="to-create-a-vat-posting-setup-to-handle-import-vat"></a>ALV-kirjausten asetusten luominen käsittelemään tuonnin ALV:tä
Tuonnin ALV -ominaisuudella kirjataan asiakirja, jossa koko summaa on ALV:tä. Tämä on tarpeellista, jos saat veroviranomaisilta laskun tuontitavaroiden arvonlisäverosta.  

Määritä tuonnin ALV:n koodit seuraavasti:  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-tuotekirjausryhmät** ja valitse sitten liittyvä linkki.  
2. Määritä Tuotteen ALV-kirjausryhmät -sivulla uusi tuotteen ALV-kirjausryhmä tuonnin ALV:tä varten.  
3. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-kirjauksien asetukset** ja valitse sitten liittyvä linkki.  
4. Luo ALV-kirjausten asetukset -sivulla uusi rivi tai käytä aiemmin luotua liiketoiminnan ALV-kirjausryhmää yhdessä tuonnin ALV:tä varten luodun uuden tuotteen ALV-kirjausryhmän kanssa.  
5. Valitse **ALV-laskennan tyyppi** -kentässä **Täysi ALV**.  
6. Anna **Ostojen ALV-tili** -kentässä se pääkirjanpidon tili, jota käytetään tuonnin ALV:n kirjaamiseen. Kaikki muut tilit ovat valinnaisia.  


## <a name="using-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>ALV-vastakirjaus EU-maiden tai -alueiden välisessä kaupassa
Joiden yritysten on käytettävä ALV-vastakirjausta tehdessään kauppaa muiden yritysten kanssa. Sääntö koskee esimerkiksi EU:n maiden tai alueiden välisiä myyntejä ja ostoja.  

> [!NOTE]  
> Tämä sääntö on voimassa, kun käydään kauppaa yritysten kanssa, jotka ovat ALV-velvollisia toisessa EU-maassa / toisella EU-alueella. Jos harjoitat liiketoimintaa suoraan muiden EU-maiden/alueiden kuluttajien kanssa, pyydä soveltuvat ALV-säännöt veroviranomaisilta.  

> [!TIP]  
> Voit tarkistaa EU:n ALV-rekisteröintinumeron vahvistuspalvelun avulla, onko yritys rekisteröity ALV-velvolliseksi toisessa EU-maassa. Palvelua voi käyttää maksutta [!INCLUDE[prod_short](includes/prod_short.md)]issa. Lisätietoja on tämän ohjeaiheen osassa _ALV-rekisteröintinumeroiden tarkistaminen_.

### <a name="sales-to-eu-countries-or-regions"></a>Myynti EU-maihin tai -alueille
ALV:tä ei lasketa myynneistä muiden EU-maiden/alueiden ALV-velvollisille yrityksille. Näiden EU-maihin/alueille tapahtuvien myyntien arvo on raportoitava erikseen ALV-ilmoituksessa.  

Laskeaksesi asianmukaisesti ALV:t myynneistä EU-maissa/-alueilla, sinun pitäisi:  

* Määritä myyntirivi, jossa on samat tiedot kuin ostoja varten. Jos olet jo määrittänyt rivejä EU-maista/alueilta tapahtuvia ostoja varten ALV-kirjausten asetukset -sivulla, voit käyttää näitä rivejä myös myynteihin.  
* Liitä liiketoiminnan ALV-kirjausryhmät asiakkaan kortin **Laskutus**-pikavälilehden **Liiketoiminnan ALV-kirjausryhmä** -kenttään kullekin EU-asiakkaalle. Asiakkaan ALV-rekisterinumero on myös lisättävä **Ulkomaankauppa**-pikavälilehden **ALV-rekisterinro**-kenttään.  

Kun kirjaat myynnin toisen EU-maan/alueen asiakkaalle, ohjelma laskee ALV-summan ja luo ALV-tapahtuman, jossa on tiedot ALV-vastakirjauksesta ja ALV-perusteesta (ALV-summan laskemiseen käytettävästä summasta). Yleisen päiväkirjan ALV-tileille ei kirjata tapahtumia.

## <a name="understanding-vat-rounding-for-documents"></a>ALV:n pyöristäminen asiakirjoja varten
Vielä kirjaamattomien asiakirjojen summat pyöristetään ja näytetään kirjattujen summien lopullista pyöristämistä vastaavalla tavalla. ALV lasketaan koko asiakirjalle, mikä tarkoittaa sitä, että laskettu ALV perustuu kaikkien rivien summaan, joilla on sama ALV-tunnus asiakirjassa.




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