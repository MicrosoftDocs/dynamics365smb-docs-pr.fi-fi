---
title: Nimikekulujen määrittäminen myynnille ja ostoille
description: 'Nimikekulujen määrittäminen silloin, kun tarvitaan varastonimikkeitä, jotka kuljettavat lisäkustannuksia, kuten rahdin ja fyysisen käsittelyn.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'transportation, added cost, landed cost'
ms.search.form: '5709, 5800, 5805, 5814'
ms.date: 07/19/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="use-item-charges-to-account-for-additional-trade-costs"></a>Kaupan lisäkustannusten huomioiminen nimikekulujen avulla

Voit varmistaa oikean arvostuksen liittämällä varastonimikkeisiin lisäkustannukset, kuten nimikkeiden ostamisessa ja myynnissä syntyvät rahti-, käsittely-, vakuutus- ja kuljetuskulut. Ostoissa ostetun nimikkeen kokonaiskustannukset koostuvat toimittajan ostohinnasta ja kaikista suorista lisänimikekuluista, jotka voidaan määritellä yksittäisiin vastaanottoihin tai palautustoimituksiin. Myynnissä Myytyjen nimikkeiden lähetyskulujen tietäminen voi olla yritykselle yhtä tärkeää kuin ostettujen nimikkeiden kokonaiskustannusten tietäminen.

Lisäkustannuksen varastoarvoon kirjaamisen lisäksi voit käyttää nimikekuluominaisuutta seuraavissa tehtävissä:

* Saapuneen nimikkeen kulun määrittäminen, jotta voidaan tehdä täsmällisiä päätöksiä jakeluverkon optimoimiseksi.
* Nimikkeen yksikkökulun tai yksikköhinnan erittely analyysia varten.
* Ostohyvitysten sisällyttäminen yksikkökustannukseen ja myyntihyvitysten yksikköhintaan.

Ennen kuin voit määrittää nimikekuluja, sinun täytyy määrittää nimikekulunumerot erityyppisille nimikekuluille. Numerot sisältävät sen, mille KP-tileille myyntiin, ostoon ja varaston muutoksiin liittyvät kustannukset kirjataan. Nimikekulunumero sisältää yleisen tuotteen kirjausryhmän, veroryhmäkoodin, tuotteen ALV-kirjausryhmän ja nimikekulun yhdistelmä. Kun syötät nimikekulunumeron osto- tai myyntiasiakirjaan, KP-tili haetaan. Haettu tili valitaan nimikekulujen numeron asetusten ja asiakirjan tietojen perusteella.

Nimikekulun voi määrittää sekä osto- että myyntiasiakirjoissa kahdella tavalla:

* Asiakirjassa, jossa on luettelo nimikkeistä, joihin nimikekulu liittyy. Tämä tehdään yleensä asiakirjoissa, joita ei ole vielä kokonaan kirjattu.
* Erillisessä laskussa linkittämällä nimikekulu linkitetään kirjattuun vastaanottoon tai lähetykseen, jossa on luettelo nimikkeistä, joihin nimikekulu liittyy.

> [!NOTE]  
> Voit määrittää nimikekulut myynneissä ja ostoissa tilauksiin, laskuihin ja hyvityslaskuihin. Seuraavat toimenpiteet kuvaavat, miten ostolaskujen nimikekuluja käsitellään. Vaiheet ovat samanlaiset kaikissa osto- ja myyntiasiakirjoissa.

## <a name="example"></a>Esimerkki

Tässä videossa näytetään, miten lisätoimituskuluja käsitellään osana varaston kustannuslaskentaa.
<br><br>  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4b0SB?rel=0]

## <a name="to-set-up-item-charge-numbers"></a>Nimikekulunumeroiden määrittäminen

Nimikekulunumeroita käytetään erottelemaan eri tyyppisiä nimikekuluja.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikekulut** ja valitse sitten vastaava linkki.
2. Luo uusi rivi valitsemalla **Nimikekulut**-sivulla **Uusi**-toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item"></a>Nimikekulun määrittäminen suoraan nimikkeen ostolaskuun

Jos tiedät nimikekulun nimikkeen ostolaskua kirjatessa, toimi seuraavasti.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten vastaava linkki.
2. Luo uusi ostolasku. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).
3. Varmista, että ostolasku on vähintään yksi rivi Nimike-tyyppinen rivi.
4. Valitse uuden rivin **Tyyppi**-kentässä **Kulu (nimike)**.
5. Syötä Määrä-kenttään **nimikekulun** yksiköt, josta olet laskutettu.
6. Anna **Välitön yksikkökustannus** -kentässä nimikekulun summa.
7. Täytä tarvittavat jäljellä olevat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Varsinainen määritys tehdään seuraavissa vaiheissa. **Määriteltävä määrä** -kentän arvo näkyy punaisella fontilla, kunnes nimikekulu on määritetty kokonaan.
8. Valitse **Rivit**-välilehdessä **Nimikekulujen määritys** toiminto.

    Avautuvassa **Nimikekulujen määritys** -sivulla näkyy yksi rivi kutakin ostolaskun Nimike-tyypin riviä. Voit määrittää nimikekululle vähintään yhdelle laskuriville käyttämällä toimintoa, joka määrittää ja jakaa sen puolestasi. Vaihtoehtoisesti voit täyttää **Määritettävä määrä** -kentän manuaalisesti. Seuraavissa vaiheissa kerrotaan, miten kuvataan, miten nimikekulujen määrityksen ehdotustoimintoa käytetään.

9. Valitse **Nimikekulun määritys** -sivulla **Ehdota nimikk. kulumääritystä** -toiminto.
10. Jos Nimike-tyyppisiä laskurivejä on useita, valitse yksi neljästä jakeluvaihtoehdosta.  

Jos nimikekulu on määritetty kokonaan, ostolaskun **Määriteltävä määrä** -kentän arvo on nolla.

Nimikekulu on nyt määritetty ostolaskuun. Kun kirjaat ostolaskun vastaanoton, nimikkeiden varastoarvot päivitetään nimikekulun kustannusten arvolla.  

## <a name="to-assign-an-item-charge-from-a-separate-invoice-to-the-purchase-invoice-for-the-item"></a>Nimikekulun määrittäminen erillisestä laskusta nimikkeen ostolaskuun

Jos vastaanotit nimikekulun laskun alkuperäisen laskun vastaanoton kirjaamisen jälkeen, toimi seuraavasti.

1. Toista kohdan [Nimikekulun määrittäminen suoraan nimikkeen ostolaskuun](payables-how-assign-item-charges.md#to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item) vaiheet 1–8.
2. Valitse **Nimikekulujen määritys** -sivulla **Hae vastaanoton rivit** -toiminto.
3. Valitse **Oston vast.otto rivit** -sivulla sen nimikkeen kirjattu oston vastaanotto, johon haluat määrittää nimikekulun, ja valitse sitten **OK**-painike.
4. Valitse **Ehdota nimikk. kulumääritystä** -toiminto.

Erillisen ostolaskun nimikekulu on nyt määritetty kirjatun oston vastaanoton nimikkeelle, joten nimikkeen varastoarvo päivitetään nimikekulun kustannuksella.

## <a name="handle-item-charges-for-partial-receipts"></a>Osittaisten vastaanottojen nimikekulujen käsitteleminen

Tutustutaan esimerkkiin siitä, miten nimikekuluja käsitellään osittaisen vastaanoton osalta.

Ostotilaus sisältää kolme riviä:

* Nimikkeille on kaksi riviä.
* Yhdelle riville kerätään nimikekuluja, jotka on kohdistettu nimikkeiden kesken summan mukaan.

Kun nimikkeet on toimitettu, huomaat, että jokin nimikkeistä puuttuu, joten et voi merkitä kyseistä riviä vastaanotetuksi. Voit vastaanottaa ja kirjata ostolaskun vain toiselle nimikkeelle ja käsitellä puuttuvaa nimikettä myöhemmin.

Voit käsitellä osittaisen vastaanoton nimikekustannuksia **Nimikekulujen määritys** -sivulla syöttämällä **0** **Käsiteltävä määrä** -kenttään puuttuvan kohteen rivillä. Kopioi sitten arvo **Käsiteltävä nimikekulumäärä** -kentästä **Laskutettava määrä** -kenttään ostotilausriveillä.

Kun olet valmis käsittelemään puuttuvan nimikkeen, päivitä **Käsiteltävä määrä** -kenttä ja kirjaa tilaus.

## <a name="see-also"></a>Katso myös

[Ostovelkojen hallinta](payables-manage-payables.md)  
[Ostojen kirjaaminen](purchasing-how-record-purchases.md)  
[Lasku – myynti](sales-how-invoice-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
