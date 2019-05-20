---
title: Myynnin ja ostojen ALV:n käsittely | Microsoft Docs
description: Tässä ohjeaiheessa käsitellään, miten ALV-laskelmat koskevat kaikkia myynti- ja ostotapahtumia, kuten EU-maissa ja EU:n alueella kirjatun ALV:n oikaisua. Tässä ohjeaiheessa kerrotaan, miten se tehdään.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, sales, purchases,
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 1665985ba00b291469146536a69a0dcfe9dec85a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238898"
---
# <a name="work-with-vat-on-sales-and-purchases"></a>Myynnin ja ostojen ALV:n käsitteleminen
Jos maasi tai alueesi edellyttää arvonlisäveron (ALV:n) laskemista myynti- ja ostotapahtumille siten, että voit ilmoittaa summat veroviranomaiselle, voit määrittää [!INCLUDE[d365fin](includes/d365fin_md.md)]in laskemaan ALV:n automaattisesti myynti- ja ostoasiakirjoissa. Lisätietoja on kohdassa [Arvolisäveron laskelmien ja kirjausmenetelmien määrittäminen](finance-setup-vat.md).

Jotkin arvolisäveroon liittyvät tehtävät voidaan tehdä manuaalisesti. Kirjattu summa on ehkä oikaistava, jos havaitset, että toimittaja käyttää toista pyöristysmenetelmää.

## <a name="calculating-and-displaying-vat-amounts-in-sales-and-purchase-documents"></a>ALV-summien laskeminen ja näyttäminen myynti- ja ostoasiakirjoissa  
Voit laskea ja näyttää myynti- ja ostoasiakirjojen ALV-summat eri tavoin kulloisenkin asiakas- tai toimittajatyypin mukaan. Voit myös korvata tietylle tapahtumalle lasketun ALV-summan toimittajan laskemalla ALV-summalla.  

### <a name="unit-price-and-line-amount-includingexcluding-vat-on-sales-documents"></a>Myyntiasiakirjojen yksikköhinta ja rivisumma, joka sisältää ALV:n tai ei sisällä sitä  
Kun valitset nimikenumeron **Nro**-kentässä myyntiasiakirjassa, [!INCLUDE[d365fin](includes/d365fin_md.md)] täyttää **Yksikköhinta**-kentän. Yksikköhinta saadaan joko **Nimike**-kortista tai nimikkeelle ja asiakkaalle sallituista nimikehinnoista. [!INCLUDE[d365fin](includes/d365fin_md.md)] laskee **rivisumman**, kun lisäät määrän riville.  

Jos myyt kuluttajille, haluat ehkä sisällyttää ALV:n myyntiasiakirjoihin. Valitse sitä varten asiakirjassa **Hinnat sisältävät ALV:n** -valintaruudun.  

### <a name="including-or-excluding-vat-on-prices"></a>ALV:n sisällyttäminen hintoihin ja jättäminen pois
Jos **Hinnat sisältävät ALV:n** -valintaruutu valintaan myyntiasiakirjassa, **Yksikköhinta**- ja **Rivisumma**-kentät päivitetään sisältämään ALV, mikä näkyy myös kenttien nimissä. ALV ei sisälly näihin kenttiin oletusarvoisesti.  

Jos kenttää ei valita, ohjelma täyttää **Yksikköhinta**- ja **Rivisummat**-kentät ilman ALV:tä, mikä näkyy kenttien nimissä.  

Voit määrittää **Hinnat sisältävät ALV:n** -valinnan oletusarvoksi kaikille tietyn asiakkaan myyntiasiakirjoille **asiakkaan** kortin **Hinnat sisältävät ALV:n** -kentässä. Voit myös määrittää, sisältävätkö nimikehinnat ALV:n. Normaalisti nimikkeen kortin sisältämät nimikehinnat eivät sisällä ALV:tä. Ohjelma määrittää **nimikkeen** kortin **Hinnat sisältävät ALV:n** -kentän perusteella yksikköhinnan myyntiasiakirjoja varten.  

Seuraavassa taulukossa on yleiskuva siitä, kuinka ohjelma laskee yksikköhinnat myyntiasiakirjoja varten silloin, kun hintoja ei ole määritetty **Myyntihinnat**-sivulla:  

|**Hinta sisältää ALV:n -kenttä nimikkeen kortissa**|**Hinnat sisältävät ALV:n -kenttä myyntiotsikossa**|**Suoritettava toiminto**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Ei valintamerkkiä|Ei valintamerkkiä|Nimikkeen kortin **Yksikköhinta** kopioidaan myyntirivien **Yksikköhinta Ilman ALV** -kenttään.|  
|Ei valintamerkkiä|Valintamerkki|Ohjelma laskee yksikkökohtaisen ALV-summan ja lisää sen nimikkeen kortin **Yksikköhinta**-kenttään. Tämä yksikköhinnan kokonaissumma lisätään sitten myyntirivien **Yksikköhinta Sis. ALV** -kenttään.|  
|Valintamerkki|Ei valintamerkkiä|Ohjelma laskee nimikkeen kortin **Yksikköhinnan** Liiketoim. ALV-kirjryh. (Hinta) ja Tuotteen ALV-kirjausryhmä -yhdistelmään liittyvän ALV-%:n avulla. Nimikkeen kortin **Yksikköhinta** lisätään sitten ALV-summalla vähennettynä myyntirivien **Yksikköhinta Ilman ALV** -kenttään.|  
|Valintamerkki|Valintamerkki|Nimikkeen kortin **Yksikköhinta** kopioidaan myyntirivien **Yksikköhinta Sis. ALV** -kenttään.|

## <a name="correcting-vat-amounts-manually-in-sales-and-purchase-documents"></a>Myynti- ja ostoasiakirjojen ALV-summien oikaisu manuaalisesti  
Voit oikaista kirjattuja ALV-tapahtumia. Näin voit muuttaa myynnin tai oston ALV-kokonaissummaa muuttamatta ALV-perustetta. Sinun ei ehkä tarvitse tehdä sitä, jos saat esimerkiksi toimittajalta laskun, jossa ALV on laskettu väärin.  

Vaikka olet ehkä määrittänyt vähintään yhden yhdistelmän tuonnin ALV:n käsittelyä varten, sinun on määritettävä vähintään yksi tuotteen ALV-kirjausryhmä. Voit antaa sille nimeksi esimerkiksi **KORJAUS**, kun sitä käytetään korjaamista varten, jos et voi käyttää samaa pääkirjanpidon tiliä **Ostojen ALV-tili** -kentässä ALV:in kirjausasetusten rivillä. Lisätietoja on kohdassa [Arvolisäveron laskelmien ja kirjausmenetelmien määrittäminen](finance-setup-vat.md).

Jos maksualennus on laskettu ALV:n sisältävän laskusumman perusteella, ALV-summan maksualennusosa peruutetaan, kun maksualennus annetaan. Huomaa, että **Muutos maksualennusten osalta** -kenttä tulee aktivoida sekä pääkirjanpidon asetuksissa (yleisesti) että ALV-kirjausasetuksissa (erityisille liiketoiminnan ALV-kirjausryhmien ja tuotteen ALV-kirjausryhmien yhdistelmille).  

#### <a name="to-manually-enter-vat-in-sales-documents"></a>Jos haluat lisätä ALV-summat manuaalisesti, tee seuraavat toimet  
1. Määritä **Pääkirjanpidon asetukset** -sivulla ohjelman laskeman summan ja manuaalisen summan **Maksimi sallittu ALV-ero**.  
2. Lisää **Myyntien ja myyntisaamisten asetukset** -sivulla valintamerkki **Salli ALV-ero** -kenttään.  

#### <a name="to-adjust-vat-for-a-sales-document"></a>Myyntiasiakirjan ALV:n muuttaminen:  
1. Avaa käsiteltävä myyntitilaus.  
2. Valitse **Tilastot**-toiminto.  
3. Valitse **Laskutus**-pikavälilehti.  

    > [!NOTE]  
    >  Riveillä näkyy laskun ALV-kokonaissumma ALV-tunnuksen mukaan ryhmiteltynä. Voit manuaalisesti muuttaa **ALV-summa**-kentän summaa kunkin ALV-tunnuksen rivillä. Kun muokkaat **ALV-summa**-kenttää, ohjelma tarkistaa, ettei ALV:tä ole muutettu enempää kuin määrittämäsi suurimman sallitun eron verran. Jos ero on suurempi kuin **Maksimi sallittu ALV-ero**, näyttöön tulee varoitus, joka ilmoittaa suurimmasta sallitusta erosta. Et voi jatkaa, ennen kuin määrä muutetaan asetettujen rajojen sallimaksi. Valitse **OK** ja lisää uusi **ALV-summa**, joka on sallitun vaihteluvälin sisällä. Jos ALV-ero on sama tai pienempi kuin suurin sallittu ero, ALV jaetaan suhteellisesti asiakirjan sellaisten rivien kanssa, joilla on sama ALV-tunnus.  

## <a name="calculating-vat-manually-using-journals"></a>ALV:n laskeminen manuaalisesti päiväkirjojen avulla  
Voit oikaista ALV-summia myös at yleisessä päiväkirjassa sekä myynti- ja ostopäiväkirjoissa. Näin on ehkä toimittava esimerkiksi silloin, kun lisäät päiväkirjaan toimittajan laskun ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in laskema ALV-summa eroaa toimittajan laskun ALV-summasta.  

#### <a name="before-you-manually-enter-vat-on-a-general-journal"></a>Ennen kuin syötät manuaalisesti ALV:n yleisen päiväkirjaan  
1. Määritä **Pääkirjanpidon asetukset** -sivulla ohjelman laskeman summan ja manuaalisen summan **Maksimi sallittu ALV-ero**.  
2. Valitse **Yleisen päiväkirjan mallit** -sivulla käsiteltävän päiväkirjan **Salli ALV-ero** -valintaruutu.  

#### <a name="before-you-manually-enter-vat-on-sales-and-purchase-journals"></a>Ennen kuin voit manuaalisesti lisätä ALV:n myynti- ja ostopäiväkirjoihin, sinun on tehtävä seuraavat toimet:  
1. Valitse **Ostojen ja ostovelkojen asetukset** -sivulla **Salli ALV-ero** -valintaruutu.  
2. Kun olet tehnyt edellä kuvatut asetukset, voit oikaista yleisen päiväkirjan rivin **ALV-summa**-kentän tai myynti- tai ostopäiväkirjan rivin **Vastatilin ALV-summa** -kentän. [!INCLUDE[d365fin](includes/d365fin_md.md)] tarkistaa, että ero ei ole suurempi kuin määritetty enimmäisarvo.  

    > [!NOTE]  
    > Jos ero on suurempi, avautuva varoitus ilmoittaa suurimman sallitun eron. Jatkaminen edellyttää summan oikaisua. Valitse ensin **OK** ja annan sitten summa, joka on sallitun vaihteluvälin sisällä. Jos ALV-ero on sama tai pienempi kuin suurin sallittu ero, [!INCLUDE[d365fin](includes/d365fin_md.md)] näyttää eron **ALV-ero**-kentässä.  

## <a name="to-post-import-vat-with-purchase-invoices"></a>Tuonnin ALV:n kirjaaminen ostolaskuissa
Tuontia koskevan ALV-laskun voi kirjata ostolaskulla yleisen päiväkirjan asemesta.  

### <a name="to-set-up-purchasing-for-posting-import-vat-invoices"></a>Määritä ostaminen tuonnin ALV-laskujen kirjaukseen  
1. Määritä toimittajan kortti tuontiviranomaiselle, joka lähettää sinulle tuontia koskevan ALV-laskun. **Ylein. liiketoim. kirjausryhmä**- ja **Liiketoiminnan ALV-kirjausryhmä** -tiedot täytyy määrittää samalla tavalla kuin tuontia koskevan ALV:n KP-tili.  
2. Luo tuontia koskevalle ALV:lle **yleinen tuotteen kirjausryhmä** ja määritä asiaankuuluvalle **yleiselle tuotteen kirjausryhmälle** tuontia koskevan ALV:n **tuotteen ALV-oletuskirjausryhmä**.  
3. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten liittyvä linkki.  
4. Valitse tuonnin ALV-kirjanpidon tili ja valitse sitten **Koti**-välilehdellä **Hallinta**-ryhmässä **Muokkaa**.  
5. Valitse tuontia koskevalle ALV:lle **Kirjaus**-pikavälilehdessä ALV:n **Yleinen tuotteen kirjausryhmä** -asetukset. [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman täyttää **Tuotteen ALV-kirjausryhmä** -kentän automaattisesti.  
6. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleiset kirjausasetukset** ja valitse sitten liittyvä linkki.  
7. Luo ALV-viranomaisen **Ylein. liiketoim. kirjausryhmän** ja tuontia koskevan ALV:n **Yleinen tuotteen kirjausryhmän** yhdistelmä. Valitse **Ostotili**-kentässä tuontia koskevan ALV:n KP-tili tätä uutta yhdistelmää varten.  

### <a name="to-create-a-new-invoice-for-the-import-authority-vendor-once-you-have-completed-the-setup"></a>Kun olet tehnyt määritykset valmiiksi, luo uusi lasku tuontiviranomaiseksi määritetylle toimittajalle  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten liittyvä linkki.  
2. Luo uusi ostolasku.  
3. Valitse **Tavarantoimittajan nro** -kentässä tuontiviranomaiseksi määritetty toimittaja ja valitse **OK**.  
4. Valitse ostorivin **Tyyppi**-kentässä **KP-tili** ja **Nro**-kentässä tuonnin ALV:n KP-tili.  
5. Kirjoita **Määrä**-kenttään **1**.  
6. Määritä ALV-summa **Välitön yksikkökustannus ilman ALV:tä** -kenttään.  
7. Kirjaa lasku.  

## <a name="to-process-certificates-of-supply"></a>Tarjontasertifikaattien käsittely
Kun myyt tavaroita toisen EU-maan/alueen asiakkaalle, sinun on lähetettävä asiakkaalle tarjontasertifikaatti, joka asiakkaan täytyy allekirjoittaa ja palauttaa sinulle. Seuraavia toimenpiteitä käytetään myyntitoimitusten tarjontasertifikaattien käsittelyyn, mutta samat vaiheet koskevat nimikkeiden palvelutoimituksia ja palautustoimituksia toimittajille.  

### <a name="to-view-certificate-of-supply-details"></a>Tarjontasertifikaatin tietojen katseleminen.  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut myyntitoimitukset** ja valitse sitten liittyvä linkki.  
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
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut myyntitoimitukset** ja valitse sitten liittyvä linkki.  
2. Valitse haluamasi myyntitoimitus asiakkaalle toiseen EU-maahan tai toiselle EU-alueelle.  
3. Valitse **Tulosta tarjontasertifikaatti** -toiminto.  

    > [!NOTE]  
    >  Vaihtoehtoisesti voit tulostaa todistuksen **Tarjontasertifikaatti**-sivulla.  

4. Jotta voit sisällyttää tiedot sertifikaatin toimitusasiakirjan riveiltä, valitse **Tulosta rivitiedot** -valintaruutu.  
5. Valitse **Luo tarjontasertifikaatit, jos niitä ei ole luotu** -valintaruutu, jos haluat, että [!INCLUDE[d365fin](includes/d365fin_md.md)] luo sertifikaatit kirjatuille toimituksille, joilla ei niitä ole suorittamishetkellä. Kun valitset valintaruudun, kaikille niille kirjatuille toimituksille luodaan uudet sertifikaatit, joilla ei ole sertifikaatteja valitulla alueella.  
6. Suodatusasetukset ovat oletusarvon mukaan toimitusasiakirjalle, jonka olet valinnut. Täytä suodatintiedot valitaksesi tietty tarjontatodistus, jonka haluat tulostaa.  
7. Valitse **Tarjontasertifikaatti**-sivulla **Tulosta**-toiminto, jos haluat tulostaa raportin, tai **Esikatselu**-toiminto, jos haluat katsoa sitä näytössä.  

    > [!Note]  
    > Toimituksen **Tarjontasertifikaatin tila** -kenttä ja **Tulostettu**-kenttä päivitetään **Tarjontasertifikaatit**-sivulla.  

8. Lähetä tulostettu tarjontasertifikaatti asiakkaalle allekirjoitettavaksi.  

### <a name="to-update-the-status-of-a-certificate-of-supply-for-a-shipment"></a>Tilauksen tarjontasertifikaatin tilan päivittäminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut myyntitoimitukset** ja valitse sitten liittyvä linkki.  
2. Valitse haluamasi myyntitoimitus asiakkaalle toiseen EU-maahan tai toiselle EU-alueelle.  
3. Valitse **Tila**-kentässä asianmukainen vaihtoehto.  

   Jos asiakas on palauttanut allekirjoitetun tarjontatodistuksen, valitse **Vastaanotettu**. **Vast.ott. pvm**-kenttä päivitetään. Vastaanottopäivämääräkksi määritetään oletusarvon mukaan nykyinen käsittelypäivämäärä.  

   Voit muokata päivämäärän vastaamaan päivämäärää, jolloin vastaanotit asiakkaan allekirjoittaman tarjontasertifikaatin. Voit myös lisätä linkin allekirjoitettuun sertifikaattiin käyttämällä vakiomuotoista [!INCLUDE[d365fin](includes/d365fin_md.md)] -linkitystä.  

   Jos asiakas ei palauta allekirjoitettua tarjontatodistusta, valitse **Ei vastaanotettu**. Tämän jälkeen sinun on lähetettävä asiakkaalle uusi lasku, joka sisältää ALV:n, koska veroviranomainen ei hyväksy alkuperäistä laskua.  

Voit tarkastella sertifikaattiryhmiä aloittamalla **Tarjontasertifikaatit**-sivulta ja päivitä sitten avointen sertifikaattien tila, kun vastaanotat ne asiakkaalta. Tästä voi olla hyötyä, jos haluat etsiä kaikki tietyn tilan omaavat sertifikaatit, esimerkiksi **Pakollinen**, ja joille haluat päivittää tilaksi **Ei vastaanotettu**.  

### <a name="to-update-the-status-of-a-group-of-certificates-of-supply"></a>Tilauksen tarjontasertifikaattien ryhmän tilan päivittäminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tarjontasertifikaatit** ja valitse sitten liittyvä linkki.  
2. Suodata **Tila**-kenttä arvoon, jonka haluat luodaksesi luettelon sertifikaateista, joita haluat hallita.  
3. Päivitä tilan tiedot valitsemalla **Muokkaa luetteloa**.  
4. Valitse **Tila**-kentässä sopiva vaihtoehto.  

   Jos asiakas on palauttanut allekirjoitetun tarjontatodistuksen, valitse **Vastaanotettu**. **Vast.ott. pvm**-kenttä päivitetään. Vastaanottopäivämääräkksi määritetään oletusarvon mukaan nykyinen käsittelypäivämäärä.  

   Voit muokata päivämäärän vastaamaan päivämäärää, jolloin vastaanotit allekirjoitetun tarjontasertifikaatin. Voit myös lisätä linkin allekirjoitettuun sertifikaattiin käyttämällä [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakirjojen vakiolinkitystä.  

    > [!NOTE]  
    >  Et voi luoda uutta tarjontasertifikaattia **Tarjontasertifikaatit**-sivulla, kun siirryt siihen tällä menetelmällä. Voit luoda sertifikaatin toimitukselle, jota ei asetettu vaatimaan sitä avaamalla kirjatun myyntitoimituksen, ja käyttämällä yhtä kahdesta yllä kuvatusta toimenpiteestä:  
    >   
    > * Tarjontasertifikaatin luominen manuaalisesti  
    > * Tarjontasertifikaatin tulostaminen.

## <a name="see-also"></a>Katso myös  
[Arvonlisäveron laskemisen ja kirjaustapojen määrittäminen](finance-setup-vat.md)   
[Toimintaohje: ALV:n raportointi veroviranomaisille](finance-how-report-vat.md)   
