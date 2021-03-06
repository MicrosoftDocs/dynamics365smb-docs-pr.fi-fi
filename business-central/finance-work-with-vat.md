---
title: Myynnin ja ostojen ALV:n käsittely | Microsoft Docs
description: Tässä ohjeaiheessa käsitellään, miten ALV-laskelmat koskevat kaikkia myynti- ja ostotapahtumia, kuten EU-maissa ja EU:n alueella kirjatun ALV:n oikaisua. Tässä ohjeaiheessa kerrotaan, miten se tehdään.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, sales, purchases,
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: ec880df940816b68a9b6f8a82098985471720984
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781554"
---
# <a name="work-with-vat-on-sales-and-purchases"></a>Myynnin ja ostojen ALV:n käsitteleminen
Jos maasi tai alueesi edellyttää arvonlisäveron (ALV:n) laskemista myynti- ja ostotapahtumille siten, että voit ilmoittaa summat veroviranomaiselle, voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)]in laskemaan ALV:n automaattisesti myynti- ja ostoasiakirjoissa. Lisätietoja on kohdassa [Arvolisäveron laskelmien ja kirjausmenetelmien määrittäminen](finance-setup-vat.md).

Jotkin arvolisäveroon liittyvät tehtävät voidaan tehdä manuaalisesti. Kirjattu summa on ehkä oikaistava, jos havaitset, että toimittaja käyttää toista pyöristysmenetelmää.  

> [!TIP]
> Voit antaa [!INCLUDE[prod_short](includes/prod_short.md)]in tarkistaa ALV-rekisterinumerot ja muut yritystiedot, kun luot tai päivität asiakirjoja. Lisätietoja on ohje aiheessa [ALV-rekisterinumeroiden tarkistaminen](finance-how-validate-vat-registration-number.md).

## <a name="calculating-and-displaying-vat-amounts-in-sales-and-purchase-documents"></a>ALV-summien laskeminen ja näyttäminen myynti- ja ostoasiakirjoissa  
Voit laskea ja näyttää myynti- ja ostoasiakirjojen ALV-summat eri tavoin kulloisenkin asiakas- tai toimittajatyypin mukaan. Voit myös korvata tietylle tapahtumalle lasketun ALV-summan toimittajan laskemalla ALV-summalla.  

### <a name="unit-price-and-line-amount-includingexcluding-vat-on-sales-documents"></a>Myyntiasiakirjojen yksikköhinta ja rivisumma, joka sisältää ALV:n tai ei sisällä sitä  
Kun valitset nimikenumeron **Nro**-kentässä myyntiasiakirjassa, [!INCLUDE[prod_short](includes/prod_short.md)] täyttää **Yksikköhinta**-kentän. Yksikköhinta saadaan joko **Nimike**-kortista tai nimikkeelle ja asiakkaalle sallituista nimikehinnoista. [!INCLUDE[prod_short](includes/prod_short.md)] laskee **rivisumman**, kun lisäät määrän riville.  

Jos myyt kuluttajille, haluat ehkä sisällyttää ALV:n myyntiasiakirjoihin. Valitse sitä varten asiakirjassa **Hinnat sisältävät ALV:n** -valintaruudun.  

### <a name="including-or-excluding-vat-on-prices"></a>ALV:n sisällyttäminen hintoihin ja jättäminen pois
Jos **Hinnat sisältävät ALV:n** -valintaruutu valintaan myyntiasiakirjassa, **Yksikköhinta**- ja **Rivisumma**-kentät päivitetään sisältämään ALV, mikä näkyy myös kenttien nimissä. ALV ei sisälly näihin kenttiin oletusarvoisesti.  

Jos kenttää ei valita, sovellus täyttää **Yksikköhinta**- ja **Rivisummat**-kentät ilman ALV:tä, mikä näkyy kenttien nimissä.  

Voit määrittää **Hinnat sisältävät ALV:n** -valinnan oletusarvoksi kaikille tietyn asiakkaan myyntiasiakirjoille **asiakkaan** kortin **Hinnat sisältävät ALV:n** -kentässä. Voit myös määrittää, sisältävätkö nimikehinnat ALV:n. Normaalisti nimikkeen kortin sisältämät nimikehinnat eivät sisällä ALV:tä. Sovellus määrittää **Nimike**-kortin **Hinnat sisältävät ALV:n** -kentän perusteella yksikköhinnan myyntiasiakirjoja varten.  

Seuraavassa taulukossa on yleiskuvaus sovelluksen tavasta laskea yksikköhinnat myyntiasiakirjoja varten silloin, kun hintoja ei ole määritetty **Myyntihinnat**-sivulla:  

|**Hinta sisältää ALV:n -kenttä nimikkeen kortissa**|**Hinnat sisältävät ALV:n -kenttä myyntiotsikossa**|**Suoritettava toiminto**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Ei valintamerkkiä|Ei valintamerkkiä|Nimikkeen kortin **Yksikköhinta** kopioidaan myyntirivien **Yksikköhinta Ilman ALV** -kenttään.|  
|Ei valintamerkkiä|Valintamerkki|Sovellus laskee yksikkökohtaisen ALV-summan ja lisää sen nimikekortin **Yksikköhinta**-kenttään. Tämä yksikköhinnan kokonaissumma lisätään sitten myyntirivien **Yksikköhinta Sis. ALV** -kenttään.|  
|Valintamerkki|Ei valintamerkkiä|Sovellus laskee nimikekortin **Yksikköhinnan** Liiketoim. ALV-kirjryh. (Hinta) ja Tuotteen ALV-kirjausryhmä -yhdistelmään liittyvän ALV-%:n avulla. Nimikkeen kortin **Yksikköhinta** lisätään sitten ALV-summalla vähennettynä myyntirivien **Yksikköhinta Ilman ALV** -kenttään.|  
|Valintamerkki|Valintamerkki|Nimikkeen kortin **Yksikköhinta** kopioidaan myyntirivien **Yksikköhinta Sis. ALV** -kenttään.|

## <a name="correcting-vat-amounts-manually-in-sales-and-purchase-documents"></a>Myynti- ja ostoasiakirjojen ALV-summien oikaisu manuaalisesti  
Voit oikaista kirjattuja ALV-tapahtumia. Näin voit muuttaa myynnin tai oston ALV-kokonaissummaa muuttamatta ALV-perustetta. Sinun ei ehkä tarvitse tehdä sitä, jos saat esimerkiksi toimittajalta laskun, jossa ALV on laskettu väärin.  

Vaikka olet ehkä määrittänyt vähintään yhden yhdistelmän tuonnin ALV:n käsittelyä varten, sinun on määritettävä vähintään yksi tuotteen ALV-kirjausryhmä. Voit antaa sille nimeksi esimerkiksi **KORJAUS**, kun sitä käytetään korjaamista varten, jos et voi käyttää samaa pääkirjanpidon tiliä **Ostojen ALV-tili** -kentässä ALV:in kirjausasetusten rivillä. Lisätietoja on kohdassa [Arvolisäveron laskelmien ja kirjausmenetelmien määrittäminen](finance-setup-vat.md).

Jos maksualennus on laskettu ALV:n sisältävän laskusumman perusteella, ALV-summan maksualennusosa peruutetaan, kun maksualennus annetaan. Huomaa, että **Muutos maksualennusten osalta** -kenttä tulee aktivoida sekä pääkirjanpidon asetuksissa (yleisesti) että ALV-kirjausasetuksissa (erityisille liiketoiminnan ALV-kirjausryhmien ja tuotteen ALV-kirjausryhmien yhdistelmille).  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-sales-documents"></a>Järjestelmän määrittäminen myyntiasiakirjojen manuaalisille ALV-tapahtumille
Seuraavaksi käsitellään manuaalisten ALV-muutosten ottamista käyttöön myyntiasiakirjoissa. **Ostojen ja ostovelkojen asetukset** -sivun vaiheet ovat samankaltaiset.

1. Määritä **Pääkirjanpidon asetukset** -sivulla sovelluksen laskeman summan ja manuaalisen summan **Maksimi sallittu ALV-ero**.  
2. Lisää **Myyntien ja myyntisaamisten asetukset** -sivulla valintamerkki **Salli ALV-ero** -kenttään.  

### <a name="to-adjust-vat-for-a-sales-document"></a>Myyntiasiakirjan ALV:n muuttaminen:  
1. Avaa käsiteltävä myyntitilaus.  
2. Valitse **Tilastot**-toiminto.  
3. Valitse **Laskutus**-pikavälilehdessä arvo **Verorivien lukumäärä**-kentässä.
4. Muokkaa **ALV-summa**-kenttää.   

> [!NOTE]  
> Riveillä näkyy laskun ALV-kokonaissumma ALV-tunnuksen mukaan ryhmiteltynä. Voit manuaalisesti muuttaa **ALV-summa**-kentän summaa kunkin ALV-tunnuksen rivillä. Kun muokkaat **ALV-summa**-kenttää, sovellus tarkistaa, ettei ALV:tä ole muutettu enempää kuin määrittämäsi suurimman sallitun eron verran. Jos ero on suurempi kuin **Maksimi sallittu ALV-ero**, näyttöön tulee varoitus, joka ilmoittaa suurimmasta sallitusta erosta. Et voi jatkaa, ennen kuin määrä muutetaan asetettujen rajojen sallimaksi. Valitse **OK** ja lisää uusi **ALV-summa**, joka on sallitun vaihteluvälin sisällä. Jos ALV-ero on sama tai pienempi kuin suurin sallittu ero, ALV jaetaan suhteellisesti asiakirjan sellaisten rivien kanssa, joilla on sama ALV-tunnus.  

## <a name="calculating-vat-manually-using-journals"></a>ALV:n laskeminen manuaalisesti päiväkirjojen avulla  
Voit oikaista ALV-summia myös at yleisessä päiväkirjassa sekä myynti- ja ostopäiväkirjoissa. Näin on ehkä toimittava esimerkiksi silloin, kun lisäät päiväkirjaan toimittajan laskun ja [!INCLUDE[prod_short](includes/prod_short.md)]in laskema ALV-summa eroaa toimittajan laskun ALV-summasta.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-general-journals"></a>Järjestelmän määrittäminen yleisen päiväkirjan manuaalisille ALV-tapahtumille
Seuraavat vaiheet on tehtävä, ennen kuin ALV kirjataan manuaalisesti yleisessä päiväkirjassa.  

1. Määritä **Pääkirjanpidon asetukset** -sivulla sovelluksen laskeman summan ja manuaalisen summan **Maksimi sallittu ALV-ero**.  
2. Valitse **Yleisen päiväkirjan mallit** -sivulla käsiteltävän päiväkirjan **Salli ALV-ero** -valintaruutu.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-sales-and-purchase-journals"></a>Järjestelmän määrittäminen myynti- ja ostopäiväkirjojen manuaalisille ALV-tapahtumille
Seuraavat vaiheet on tehtävä, ennen kuin ALV kirjataan manuaalisesti myynti- tai ostopäiväkirjassa.

1. Valitse **Ostojen ja ostovelkojen asetukset** -sivulla **Salli ALV-ero** -valintaruutu.  
2. Toista vaihe 1 **Myyntien ja myyntisaamisten asetukset** -sivulla.
3. Kun olet tehnyt edellä kuvatut asetukset, voit oikaista yleisen päiväkirjan rivin **ALV-summa**-kentän tai myynti- tai ostopäiväkirjan rivin **Vastatilin ALV-summa** -kentän. [!INCLUDE[prod_short](includes/prod_short.md)] tarkistaa, että ero ei ole suurempi kuin määritetty enimmäisarvo.  

    > [!NOTE]  
    > Jos ero on suurempi, avautuva varoitus ilmoittaa suurimman sallitun eron. Jatkaminen edellyttää summan oikaisua. Valitse ensin **OK** ja annan sitten summa, joka on sallitun vaihteluvälin sisällä. Jos ALV-ero on sama tai pienempi kuin suurin sallittu ero, [!INCLUDE[prod_short](includes/prod_short.md)] näyttää eron **ALV-ero**-kentässä.  

## <a name="posting-import-vat-with-purchase-invoices"></a>Tuonnin ALV:n kirjaaminen ostolaskuissa
Tuontia koskevan ALV-laskun voi kirjata ostolaskulla päiväkirjojen asemesta.  

### <a name="to-set-up-purchasing-for-posting-import-vat-invoices"></a>Määritä ostaminen tuonnin ALV-laskujen kirjaukseen  
1. Määritä toimittajan kortti tuontiviranomaiselle, joka lähettää sinulle tuontia koskevan ALV-laskun. **Ylein. liiketoim. kirjausryhmä**- ja **Liiketoiminnan ALV-kirjausryhmä** -tiedot täytyy määrittää samalla tavalla kuin tuontia koskevan ALV:n KP-tili.  
2. Luo tuontia koskevalle ALV:lle **yleinen tuotteen kirjausryhmä** ja määritä asiaankuuluvalle **yleiselle tuotteen kirjausryhmälle** tuontia koskevan ALV:n **tuotteen ALV-oletuskirjausryhmä**.  
3. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten liittyvä linkki.  
4. Valitse tuonnin ALV-pääkirjanpitotili ja valitse sitten **Muokkaa**-toiminto.  
5. Valitse tuontia koskevalle ALV:lle **Kirjaus**-pikavälilehdessä ALV:n **Yleinen tuotteen kirjausryhmä** -asetukset. [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman täyttää **Tuotteen ALV-kirjausryhmä** -kentän automaattisesti.  
6. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yleiset kirjausasetukset** ja valitse sitten liittyvä linkki.  
7. Luo ALV-viranomaisen **Ylein. liiketoim. kirjausryhmän** ja tuontia koskevan ALV:n **Yleinen tuotteen kirjausryhmän** yhdistelmä. Valitse **Ostotili**-kentässä tuontia koskevan ALV:n KP-tili tätä uutta yhdistelmää varten.  

### <a name="to-create-a-new-invoice-for-the-import-authority-vendor-once-you-have-completed-the-setup"></a>Kun olet tehnyt määritykset valmiiksi, luo uusi lasku tuontiviranomaiseksi määritetylle toimittajalle  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten liittyvä linkki.  
2. Luo uusi ostolasku.  
3. Valitse **Tavarantoimittajan nro** -kentässä tuontiviranomaiseksi määritetty toimittaja ja valitse **OK**.  
4. Valitse ostorivin **Tyyppi**-kentässä **KP-tili** ja **Nro**-kentässä tuonnin ALV:n KP-tili.  
5. Kirjoita **Määrä**-kenttään **1**.  
6. Määritä ALV-summa **Välitön yksikkökustannus ilman ALV:tä** -kenttään.  
7. Kirjaa lasku.  

## <a name="processing-certificates-of-supply"></a>Tarjontasertifikaattien käsitteleminen
Kun myyt tavaroita toisen EU-maan/alueen asiakkaalle, sinun on lähetettävä asiakkaalle tarjontasertifikaatti, joka asiakkaan täytyy allekirjoittaa ja palauttaa sinulle. Seuraavia toimenpiteitä käytetään myyntitoimitusten tarjontasertifikaattien käsittelyyn, mutta samat vaiheet koskevat nimikkeiden palvelutoimituksia ja palautustoimituksia toimittajille.  

### <a name="to-view-certificate-of-supply-details"></a>Tarjontasertifikaatin tietojen katseleminen.  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kirjatut myyntitoimitukset** ja valitse sitten liittyvä linkki.  
2. Valitse haluamasi myyntitoimitus asiakkaalle toiseen EU-maahan/alueelle.  
3. Valitse **Tarjontasertifikaatin tiedot**.  
4. Jos **Tarjontasertifikaatti**-valintaruutu on valittu asiakkaan ALV-kirjausryhmän asetuksissa, **Tila**-kentän arvoksi määritetään oletusarvoisesti **Tarvitaan**. Voit päivittää kentän osoittamaan, onko asiakas palauttanut sertifikaatin.  

    > [!Note]  
    >  Jos **Tarjontasertifikaatti vaaditaan**-valintaruutu ei ole valittuna ALV-kirjausryhmän asetuksissa, järjestelmä luo uuden tietueen ja **Tila**-kentälle asetetaan arvoksi **Ei sovellu**. Voit päivittää kentän vastaamaan oikeita tilatietoja. Tila voidaan muuttaa tarpeen mukaan manuaalisesti arvosta **Ei sovellu** arvoon **Pakollinen** ja arvosta **Pakollinen** arvoon **Ei sovellu**.  

   Sertifikaatti luodaan, kun päivität **Tila**-kentän arvoksi **Pakollinen**, **Vastaanotettu** tai **Ei vastaanotettu**.  

    > [!TIP]  
    >  Voit käyttää **Tarjontasertifikaatti**-sivua nähdäksesi kaikkien niiden kirjattujen toimitusten tilan, joille on luotu tarjontasertifikaatti.  

5. Valitse **Tulosta tarjontasertifikaatti**.  

    > [!Note]  
    >  Voit esikatsella tai tulostaa asiakirjan. Kun valitset **Tulostaa tarjontasertifikaatti** ja tulostat asiakirjan, järjestelmä valitsee **Tulostettu**-valintaruudun automaattisesti. Jos todistuksen tilaa ei ole jo määritetty, se päivitetään arvoon **Pakollinen**. Sisällytä tulostettu sertifikaatti tarvittaessa toimitukseen.  

### <a name="to-print-a-certificate-of-supply"></a>Tarjontasertifikaatin tulostaminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kirjatut myyntitoimitukset** ja valitse sitten liittyvä linkki.  
2. Valitse haluamasi myyntitoimitus asiakkaalle toiseen EU-maahan tai toiselle EU-alueelle.  
3. Valitse **Tulosta tarjontasertifikaatti** -toiminto.  

    > [!NOTE]  
    >  Vaihtoehtoisesti voit tulostaa todistuksen **Tarjontasertifikaatti**-sivulla.  

4. Jotta voit sisällyttää tiedot sertifikaatin toimitusasiakirjan riveiltä, valitse **Tulosta rivitiedot** -valintaruutu.  
5. Valitse **Luo tarjontasertifikaatit, jos niitä ei ole luotu** -valintaruutu, jos haluat, että [!INCLUDE[prod_short](includes/prod_short.md)] luo sertifikaatit kirjatuille toimituksille, joilla ei niitä ole suorittamishetkellä. Kun valitset valintaruudun, kaikille niille kirjatuille toimituksille luodaan uudet sertifikaatit, joilla ei ole sertifikaatteja valitulla alueella.  
6. Suodatusasetukset ovat oletusarvon mukaan toimitusasiakirjalle, jonka olet valinnut. Täytä suodatintiedot valitaksesi tietty tarjontatodistus, jonka haluat tulostaa.  
7. Valitse **Tarjontasertifikaatti**-sivulla **Tulosta**-toiminto, jos haluat tulostaa raportin, tai **Esikatselu**-toiminto, jos haluat katsoa sitä näytössä.  

    > [!Note]  
    > Toimituksen **Tarjontasertifikaatin tila** -kenttä ja **Tulostettu**-kenttä päivitetään **Tarjontasertifikaatit**-sivulla.  

8. Lähetä tulostettu tarjontasertifikaatti asiakkaalle allekirjoitettavaksi.  

### <a name="to-update-the-status-of-a-certificate-of-supply-for-a-shipment"></a>Tilauksen tarjontasertifikaatin tilan päivittäminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kirjatut myyntitoimitukset** ja valitse sitten liittyvä linkki.  
2. Valitse haluamasi myyntitoimitus asiakkaalle toiseen EU-maahan tai toiselle EU-alueelle.  
3. Valitse **Tila**-kentässä asianmukainen vaihtoehto.  

   Jos asiakas on palauttanut allekirjoitetun tarjontatodistuksen, valitse **Vastaanotettu**. **Vast.ott. pvm**-kenttä päivitetään. Vastaanottopäivämääräkksi määritetään oletusarvon mukaan nykyinen käsittelypäivämäärä.  

   Voit muokata päivämäärän vastaamaan päivämäärää, jolloin vastaanotit asiakkaan allekirjoittaman tarjontasertifikaatin. Voit myös lisätä linkin allekirjoitettuun sertifikaattiin käyttämällä vakiomuotoista [!INCLUDE[prod_short](includes/prod_short.md)] -linkitystä.  

   Jos asiakas ei palauta allekirjoitettua tarjontatodistusta, valitse **Ei vastaanotettu**. Tämän jälkeen sinun on lähetettävä asiakkaalle uusi lasku, joka sisältää ALV:n, koska veroviranomainen ei hyväksy alkuperäistä laskua.  

Voit tarkastella sertifikaattiryhmiä aloittamalla **Tarjontasertifikaatit**-sivulta ja päivitä sitten avointen sertifikaattien tila, kun vastaanotat ne asiakkaalta. Tästä voi olla hyötyä, jos haluat etsiä kaikki tietyn tilan omaavat sertifikaatit, esimerkiksi **Pakollinen**, ja joille haluat päivittää tilaksi **Ei vastaanotettu**.  

### <a name="to-update-the-status-of-a-group-of-certificates-of-supply"></a>Tilauksen tarjontasertifikaattien ryhmän tilan päivittäminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Tarjontasertifikaatit** ja valitse sitten liittyvä linkki.  
2. Suodata **Tila**-kenttä arvoon, jonka haluat luodaksesi luettelon sertifikaateista, joita haluat hallita.  
3. Päivitä tilan tiedot valitsemalla **Muokkaa luetteloa**.  
4. Valitse **Tila**-kentässä sopiva vaihtoehto.  

   Jos asiakas on palauttanut allekirjoitetun tarjontatodistuksen, valitse **Vastaanotettu**. **Vast.ott. pvm**-kenttä päivitetään. Vastaanottopäivämääräkksi määritetään oletusarvon mukaan nykyinen käsittelypäivämäärä.  

   Voit muokata päivämäärän vastaamaan päivämäärää, jolloin vastaanotit allekirjoitetun tarjontasertifikaatin. Voit myös lisätä linkin allekirjoitettuun sertifikaattiin käyttämällä [!INCLUDE[prod_short](includes/prod_short.md)]in asiakirjojen vakiolinkitystä.  

    > [!NOTE]  
    >  Et voi luoda uutta tarjontasertifikaattia **Tarjontasertifikaatit**-sivulla, kun siirryt siihen tällä menetelmällä. Voit luoda sertifikaatin toimitukselle, jota ei asetettu vaatimaan sitä avaamalla kirjatun myyntitoimituksen, ja käyttämällä yhtä kahdesta yllä kuvatusta toimenpiteestä:  
    >
    > * Tarjontasertifikaatin luominen manuaalisesti  
    > * Tarjontasertifikaatin tulostaminen.

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Arvonlisäveron laskemisen ja kirjaustapojen määrittäminen](finance-setup-vat.md)  
[ALV:n raportointi veroviranomaisille](finance-how-report-vat.md)  
[ALV-rekisterinumeron vahvistaminen](finance-how-validate-vat-registration-number.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
