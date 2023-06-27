---
title: 'Toimintaohje: Myynnin ja ostojen ALV:n käsittely'
description: 'Tässä ohjeaiheessa kuvataan erilaisia tapoja käsitellä ALV:tä sekä manuaalisesti että automaattisten asetusten avulla, jotta voit noudattaa maakohtaisia säädöksiä.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, sales, purchases'
ms.search.form: '7, 118, 130, 142, 459, 460, 525'
ms.date: 06/16/2021
ms.author: bholtorf
---
# <a name="work-with-vat-on-sales-and-purchases" />Myynnin ja ostojen ALV:n käsitteleminen

Jos maasi tai alueesi edellyttää, että lasket ja raportoit arvonlisäveron (ALV) myynti- ja ostotransaktioista, voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)]in laskemaan ALV:n. Lisätietoja on kohdassa [Arvolisäveron laskelmien ja kirjausmenetelmien määrittäminen](finance-setup-vat.md).

Jotkin arvolisäveroon liittyvät tehtävät voidaan tehdä manuaalisesti. Kirjattu summa on ehkä oikaistava, jos havaitset, että toimittaja käyttää toista pyöristysmenetelmää.  

> [!TIP]
> Voit antaa [!INCLUDE[prod_short](includes/prod_short.md)]in tarkistaa ALV-rekisterinumerot ja muut yritystiedot, kun luot tai päivität asiakirjoja. Lisätietoja on ohje aiheessa [ALV-rekisterinumeroiden tarkistaminen](finance-how-validate-vat-registration-number.md).

## <a name="calculating-and-displaying-vat-amounts-on-sales-and-purchase-documents" />ALV-summien laskeminen ja näyttäminen myynti- ja ostoasiakirjoissa

Kun valitset nimikenumeron **Nro**-kentässä kenttä myynti- tai ostoasiakirjassa, [!INCLUDE[prod_short](includes/prod_short.md)] täyttää **Yksikköhinta**- ja **Rivisumma**-kentät. Yksikköhinta saadaan joko **Nimike**-kortista tai nimikkeelle ja asiakkaalle sallituista nimikehinnoista. [!INCLUDE[prod_short](includes/prod_short.md)] laskee rivisumman, kun lisäät määrän riville.  

Jos haluat, että yksikköhinnat ja rivisummat sisältävät ALV:n (jos myyt esimerkiksi vähittäismyynnissä oleville kuluttajille), valitse asiakirjassa **Hinnat sisältävät ALV:n** -valintaruutu. Lisätietoja on kohdassa [ALV:n sisällyttäminen ja poissulkeminen hintoihin ja rivisummiin](#including-or-excluding-vat-in-prices-and-line-amounts). 

Voit laskea ja näyttää myynti- ja ostoasiakirjojen ALV-summat eri tavoin kulloisenkin asiakas- tai toimittajatyypin mukaan. Voit myös muuttaa tietylle tapahtumalle lasketun ALV-summan manuaalisesti, esimerkiksi siten, että toimittajan laskemaa ALV-summaa käytetään.

### <a name="including-or-excluding-vat-in-prices-and-line-amounts" />ALV:n sisällyttäminen hintoihin ja rivisummiin sekä sen poissulkeminen

Jos **Hinnat sisältävät ALV:n** -valintaruutu valitaan myyntiasiakirjassa, **Yksikköhinta**- ja **Rivisumma**-kentät sisältävät ALV:n. ALV ei sisälly näiden kenttien arvoihin oletusarvoisesti. Kenttien nimet kuvaavat, sisältyykö hintoihin ALV.  

Voit määrittää **Hinnat sisältävät ALV:n** -valinnan oletusarvoksi kaikille tietyn asiakkaan myyntiasiakirjoille **asiakkaan** kortin **Hinnat sisältävät ALV:n** -kentässä. Voit myös määrittää, sisältävätkö nimikehinnat ALV:n. Yleensä nimikekortin hinnat eivät sisällä ALV:tä. 

Seuraavassa taulukossa on yleiskuvaus sovelluksen tavasta laskea yksikköhinnat myyntiasiakirjoja varten silloin, kun hintoja ei ole määritetty **Myyntihinnat**-sivulla:  

|**Hinta sisältää ALV:n -kenttä nimikkeen kortissa**|**Hinnat sisältävät ALV:n -kenttä**|**Suoritettava toiminto**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Ei käytössä|Ei käytössä|Nimikkeen kortin **Yksikköhinta** kopioidaan myyntirivien **Yksikköhinta Ilman ALV** -kenttään.|  
|Ei käytössä|Käytössä|Sovellus laskee yksikkökohtaisen ALV-summan ja lisää sen nimikekortin **Yksikköhinta**-kenttään. Tämä yksikköhinnan kokonaissumma lisätään sitten myyntirivien **Yksikköhinta Sis. ALV** -kenttään.|  
|Käytössä|Ei käytössä|Sovellus laskee **nimikekortin** **Yksikköhinnan** Liiketoim. ALV-kirjryh. (Hinta) ja Tuotteen ALV-kirjausryhmä -yhdistelmään liittyvän ALV-prosentin avulla. Nimikkeen kortin **Yksikköhinta** lisätään sitten ALV-summalla vähennettynä myyntirivien **Yksikköhinta Ilman ALV** -kenttään. Lisätietoja on kohdassa [Liiketoiminnan ALV-kirjausryhmien ja asiakashintaryhmien käyttäminen](finance-work-with-vat.md#using-vat-business-posting-groups-and-customer-price-groups).|  
|Käytössä|Käytössä|Nimikkeen kortin **Yksikköhinta** kopioidaan myyntirivien **Yksikköhinta Sis. ALV** -kenttään.|

#### <a name="using-vat-business-posting-groups-and-customer-price-groups" />Liiketoiminnan ALV-kirjausryhmien ja asiakashintaryhmien käyttäminen

Jos haluat hintojen sisältävän ALV:n, voit käyttää liiketoiminnan ALV-kirjausryhmiä, kun haluat laskea summan ryhmän ALV-kirjausasetusten perusteella. Lisätietoja on kohdassa [Liiketoiminnan ALV-kirjausryhmien määrittäminen](finance-setup-vat.md#set-up-vat-business-posting-groups).

Sen mukaan, mitä haluat tehdä, voit liittää liiketoiminnan ALV-kirjausryhmän asiakkaille tai myyntiasiakirjoihin seuraavilla tavoilla:

* Jos haluat käyttää samaa ALV-prosenttia kaikille asiakkaille, voit valita ryhmän **Myynnin ja saamisten asetukset** -sivun **Liiketoiminnan ALV-kirjaus ryhmä (hinta)** -kentässä.
* Jos haluat käyttää jotain ALV-prosenttia tietylle asiakkaalle, voit valita ryhmän **Asiakaskortti** -sivun **Liiketoiminnan ALV-kirjaus ryhmä (hinta)** -kentässä. 
* Jos haluat käyttää jotain ALV-prosenttia tietylle asiakasryhmälle, voit valita ryhmän **Asiakashintaryhmä**-sivun **Liiketoiminnan ALV-kirjaus ryhmä (hinta)** -kentässä. Tämä on hyödyllistä esimerkiksi silloin, kun haluat, että hinta koskee kaikkia asiakkaita tietyllä maantieteellisellä alueella tai tietyllä toimialalla.
* Kaikissa myyntiasiakirjoissa **Liiketoiminnan ALV-kirjausryhmä** -kentässä. Ryhmälle määritettyä ALV-summaa käytetään vain asiakirjalle, jota parhaillaan käsittelet.

> [!NOTE]
> Jos et määrittele **Liiketoiminnan ALV-kirjaus ryhmä (hinta)** -kentässä ryhmää, ALV ei sisälly hintoihin.

#### <a name="examples" />Esimerkkejä

Sellaiset tekijät kuin maa tai alue, joissa myyt, tai toimialan tyyppi, voivat vaikuttaa ALV-summaan, joka sinun täytyy ottaa huomioon. Esimerkiksi ravintola voi veloittaa 6 %:n ALV:n aterioista, joita syödään omassa talossa, ja 17 %:n ALV:n noutoruuasta. Tämän saavuttamiseksi luodaan Liiketoiminnan ALV-kirjausryhmä (hinta) talossa ruokailua varten ja toinen noutoa varten.

## <a name="working-with-vat-date" />ALV-päivämäärän käyttäminen

### <a name="vat-date-in-documents" />ALV-päivämäärä asiakirjoissa

Kun luot uusia myynti- tai ostoasiakirjoja, **ALV-päivämäärä** perustuu **ALV-oletuspäivämäärä**-kenttään **Pääkirjanpidon asetukset** -sivulla. Tämä oletusarvo voi olla sama kuin **kirjauspäivämäärä** tai **asiakirjan päivämäärä**. Jos tarvitset eri ALV-päivämäärän, voit muuttaa arvon manuaalisesti **ALV-päivämäärä**-kentässä. Kun kirjaat asiakirjan, **ALV-päivämäärä**näkyy kirjattavassa asiakirjassa sekä ALV- ja KP-tapahtumissa.

> [!NOTE]
> Jos **ALV-päivämäärä** -kenttä ei ole käytettävissä asiakirjoissa tai päiväkirjoissa, **Älä käytä ALV-päivämäärä-toimintoa** on valittu **Pääkirjanpidon asetukset** -sivun **ALV-päivämäärän käyttö** -kentässä.  

> [!IMPORTANT]
> Jos **Hallitse ALV-jaksoa** -vaihtoehdoksi määritetään **Pääkirjanpidon asetukset** -sivulla **Estä kirjaaminen suljetulla jaksolla** tai **Estä kirjaaminen suljetulla jaksolla ja varoita vapautetusta jaksosta**, asiakirja tai päiväkirja voidaan kirjata vain, jos **ALV-päivämäärä**-kentän arvo ei ole suljetulla jaksolla **ALV-palautusjaksot** -kohdassa. Vaikka **ALV-palautusjaksot** -kohdan jakso olisi avoin, seurauksena voi olla varoitus, jonka perusteena on **ALV-palautuksen tila** ja **Hallitse ALV-jaksoa** -määritys.

> [!IMPORTANT]
> Tietyn päivämääräalueen **ALV-päivämäärän** kirjaus voidaan sallia tai estää käyttämällä **Pääkirjanpidon asetukset**- ja **Käyttäjäasetukset**-sivujen **Ensimm. sallittu kirjauspvm:**- ja **Viimeinen sallittu kirjauspvm:** -kenttiä.  

> [!NOTE]
> Jos **ALV-päivämäärä** jätetään tyhjäksi, [!INCLUDE [prod_short](includes/prod_short.md)] käyttää kirjatun tapahtuman **ALV-päivämääränä** **Pääkirjanpidon asetukset** -sivun **ALV-oletuspäivämäärä** -kohdan oletusmäärityksiä.  

### <a name="modifying-the-vat-date-in-posted-entries" />ALV-päivämäärän muokkaaminen kirjatuissa tapahtumissa

Kirjattujen asiakirjojen ALV-päivämäärää voidaan tarvittaessa muuttaa. Kirjattujen asiakirjojen **ALV-päivämäärä**-kentän päivämäärää muutetaan seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-tapahtumat** ja valitse sitten vastaava linkki. 
2. Etsi tapahtuma, jonka ALV-päivämäärä on virheellinen.  
3. Valitse **Muokkaa luetteloa** -toiminto ja syötä sitten oikea päivämäärä **ALV-päivämäärä**-kenttään.  
4. Kun sivu suljetaan, ALV-päivämäärä muuttuu liittyvässä **KP-tapahtumat**-kohdassa ja kirjatussa asiakirjassa.  

> [!NOTE]
> **ALV-tapahtumat**-kohdan **ALV-päivämäärä**-kenttää voidaan muuttaa vain, jos nykyinen päivämäärä ei ole suljetulla ALV-palautusjaksolla. Vaikka **ALV-palautusjaksot** -kentän jakso olisi avoin, seurauksena voi olla varoitus, jonka perusteena on **ALV-palautuksen tila**.  

> [!NOTE]
> Jos asiakirjassa on useita **ALV-tapahtumia**, vain yhden asiakirjaan liittyvän tapahtuman **ALV-päivämäärä**-kentän arvo tarvitsee muuttaa. [!INCLUDE[prod_short](includes/prod_short.md)] pitää tapahtumat johdonmukaisina muuttamalla automaattisesti ALV-päivämäärän tähän tapahtumiin liittyvissä ALV-tapahtumissa. [!INCLUDE [prod_short](includes/prod_short.md)] päivittää muiden taulukoiden (KP-tapahtumat ja asiakirjat) **ALV-päivämäärät** mutta vain tähän tapahtumaan liittyen.  

## <a name="correcting-vat-amounts-manually-on-sales-and-purchase-documents" />Myynti- ja ostoasiakirjojen ALV-summien oikaisu manuaalisesti

Voit tehdä muutoksia kirjattuihin ALV-tapahtumiin, jotta voit muuttaa ostojen ja myyntien ALV-kokonaissummia muuttamatta ALV-perustetta. Jos vastaanotat esimerkiksi toimittajalta laskun, jonka alv-summa on virheellinen.  

Vaikka olet ehkä määrittänyt vähintään yhden yhdistelmän tuonnin ALV:n käsittelyä varten, sinun on määritettävä vähintään yksi tuotteen ALV-kirjausryhmä. Voit antaa sille nimeksi esimerkiksi **KORJAUS**, kun sitä käytetään korjaamista varten, jos et voi käyttää samaa pääkirjanpidon tiliä **Ostojen ALV-tili** -kentässä ALV:in kirjausasetusten rivillä. Lisätietoja on kohdassa [Arvolisäveron laskelmien ja kirjausmenetelmien määrittäminen](finance-setup-vat.md).

Jos maksualennus on laskettu ALV:n sisältävän laskusumman perusteella, ALV-summan maksualennusosa peruutetaan, kun maksualennus annetaan. Huomaa, että **Muutos maksualennusten osalta** -kenttä tulee aktivoida sekä pääkirjanpidon asetuksissa (yleisesti) että ALV-kirjausasetuksissa (erityisille liiketoiminnan ALV-kirjausryhmien ja tuotteen ALV-kirjausryhmien yhdistelmille).  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-sales-documents" />Järjestelmän määrittäminen myyntiasiakirjojen manuaalisille ALV-tapahtumille
Seuraavaksi käsitellään manuaalisten ALV-muutosten ottamista käyttöön myyntiasiakirjoissa. **Ostojen ja ostovelkojen asetukset** -sivun vaiheet ovat samankaltaiset.

1. Määritä **Pääkirjanpidon asetukset** -sivulla sovelluksen laskeman summan ja manuaalisen summan **Maksimi sallittu ALV-ero**.  
2. Lisää **Myyntien ja myyntisaamisten asetukset** -sivulla valintamerkki **Salli ALV-ero** -kenttään.  

### <a name="to-adjust-vat-for-a-sales-document" />Myyntiasiakirjan ALV:n muuttaminen:

1. Avaa käsiteltävä myyntitilaus.  
2. Valitse **Tilastot**-toiminto.  
3. Valitse **Laskutus**-pikavälilehdessä arvo **Verorivien lukumäärä**-kentässä.
4. Muokkaa **ALV-summa**-kenttää.   

> [!NOTE]  
> Riveillä näkyy laskun ALV-kokonaissumma ALV-tunnuksen mukaan ryhmiteltynä. Voit manuaalisesti muuttaa **ALV-summa**-kentän summaa kunkin ALV-tunnuksen rivillä. Kun muokkaat **ALV-summa**-kenttää, sovellus tarkistaa, ettei ALV:tä ole muutettu enempää kuin määrittämäsi suurimman sallitun eron verran. Jos ero on suurempi kuin **Maksimi sallittu ALV-ero**, näyttöön tulee varoitus, joka ilmoittaa suurimmasta sallitusta erosta. Et voi jatkaa, ennen kuin määrä muutetaan asetettujen rajojen sallimaksi. Valitse **OK** ja lisää uusi **ALV-summa**, joka on sallitun vaihteluvälin sisällä. Jos ALV-ero on sama tai pienempi kuin suurin sallittu ero, ALV jaetaan suhteellisesti asiakirjan sellaisten rivien kanssa, joilla on sama ALV-tunnus.  

## <a name="calculating-vat-manually-using-journals" />ALV:n laskeminen manuaalisesti päiväkirjojen avulla
Voit oikaista ALV-summia myös at yleisessä päiväkirjassa sekä myynti- ja ostopäiväkirjoissa. Näin on ehkä toimittava esimerkiksi silloin, kun lisäät päiväkirjaan toimittajan laskun ja [!INCLUDE[prod_short](includes/prod_short.md)]in laskema ALV-summa eroaa toimittajan laskun ALV-summasta.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-general-journals" />Järjestelmän määrittäminen yleisen päiväkirjan manuaalisille ALV-tapahtumille
Seuraavat vaiheet on tehtävä, ennen kuin ALV kirjataan manuaalisesti yleisessä päiväkirjassa.  

1. Määritä **Pääkirjanpidon asetukset** -sivulla sovelluksen laskeman summan ja manuaalisen summan **Maksimi sallittu ALV-ero**.  
2. Valitse **Yleisen päiväkirjan mallit** -sivulla käsiteltävän päiväkirjan **Salli ALV-ero** -valintaruutu.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-sales-and-purchase-journals" />Järjestelmän määrittäminen myynti- ja ostopäiväkirjojen manuaalisille ALV-tapahtumille

Seuraavat vaiheet on tehtävä, ennen kuin ALV kirjataan manuaalisesti myynti- tai ostopäiväkirjassa.

1. Valitse **Ostojen ja ostovelkojen asetukset** -sivulla **Salli ALV-ero** -valintaruutu.  
2. Toista vaihe 1 **Myyntien ja myyntisaamisten asetukset** -sivulla.
3. Kun olet tehnyt edellä kuvatut asetukset, voit oikaista yleisen päiväkirjan rivin **ALV-summa**-kentän tai myynti- tai ostopäiväkirjan rivin **Vastatilin ALV-summa** -kentän. [!INCLUDE[prod_short](includes/prod_short.md)] tarkistaa, että ero ei ole suurempi kuin määritetty enimmäisarvo.  

> [!NOTE]  
> Jos ero on suurempi, avautuva varoitus ilmoittaa suurimman sallitun eron. Jatkaminen edellyttää summan oikaisua. Valitse ensin **OK** ja annan sitten summa, joka on sallitun vaihteluvälin sisällä. Jos ALV-ero on sama tai pienempi kuin suurin sallittu ero, [!INCLUDE[prod_short](includes/prod_short.md)] näyttää eron **ALV-ero**-kentässä.  

## <a name="posting-import-vat-with-purchase-invoices" />Tuonnin ALV:n kirjaaminen ostolaskuissa
Tuontia koskevan ALV-laskun voi kirjata ostolaskulla päiväkirjojen asemesta.  

### <a name="to-set-up-purchasing-for-posting-import-vat-invoices" />Määritä ostaminen tuonnin ALV-laskujen kirjaukseen

1. Määritä toimittajan kortti tuontiviranomaiselle, joka lähettää sinulle tuontia koskevan ALV-laskun. **Ylein. liiketoim. kirjausryhmä**- ja **Liiketoiminnan ALV-kirjausryhmä** -tiedot täytyy määrittää samalla tavalla kuin tuontia koskevan ALV:n KP-tili.  
2. Luo tuontia koskevalle ALV:lle **yleinen tuotteen kirjausryhmä** ja määritä asiaankuuluvalle **yleiselle tuotteen kirjausryhmälle** tuontia koskevan ALV:n **tuotteen ALV-oletuskirjausryhmä**.  
3. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten vastaava linkki.  
4. Valitse tuonnin ALV-pääkirjanpitotili ja valitse sitten **Muokkaa**-toiminto.  
5. Valitse tuontia koskevalle ALV:lle **Kirjaus**-pikavälilehdessä ALV:n **Yleinen tuotteen kirjausryhmä** -asetukset. [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman täyttää **Tuotteen ALV-kirjausryhmä** -kentän automaattisesti.  
6. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleiset kirjausasetukset** ja valitse sitten vastaava linkki.  
7. Luo ALV-viranomaisen **Ylein. liiketoim. kirjausryhmän** ja tuontia koskevan ALV:n **Yleinen tuotteen kirjausryhmän** yhdistelmä. Valitse **Ostotili**-kentässä tuontia koskevan ALV:n KP-tili tätä uutta yhdistelmää varten.  

### <a name="to-create-a-new-invoice-for-the-import-authority-vendor-once-you-have-completed-the-setup" />Kun olet tehnyt määritykset valmiiksi, luo uusi lasku tuontiviranomaiseksi määritetylle toimittajalle

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten vastaava linkki.  
2. Luo uusi ostolasku.  
3. Valitse **Tavarantoimittajan nro** -kentässä tuontiviranomaiseksi määritetty toimittaja ja valitse **OK**.  
4. Valitse ostorivin **Tyyppi**-kentässä **KP-tili** ja **Nro**-kentässä tuonnin ALV:n KP-tili.  
5. Kirjoita **Määrä**-kenttään **1**.  
6. Määritä ALV-summa **Välitön yksikkökustannus ilman ALV:tä** -kenttään.  
7. Kirjaa lasku.  

## <a name="processing-certificates-of-supply" />Tarjontasertifikaattien käsitteleminen

Kun myyt tavaroita toisen EU-maan/alueen asiakkaalle, sinun on lähetettävä asiakkaalle tarjontasertifikaatti, joka asiakkaan täytyy allekirjoittaa ja palauttaa sinulle. Seuraavia toimenpiteitä käytetään myyntitoimitusten tarjontasertifikaattien käsittelyyn, mutta samat vaiheet koskevat nimikkeiden palvelutoimituksia ja palautustoimituksia toimittajille.  

### <a name="to-view-certificate-of-supply-details" />Tarjontasertifikaatin tietojen katseleminen.
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut myyntitoimitukset** ja valitse sitten vastaava linkki.  
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

### <a name="to-print-a-certificate-of-supply" />Tarjontasertifikaatin tulostaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut myyntitoimitukset** ja valitse sitten vastaava linkki.  
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

### <a name="to-update-the-status-of-a-certificate-of-supply-for-a-shipment" />Tilauksen tarjontasertifikaatin tilan päivittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut myyntitoimitukset** ja valitse sitten vastaava linkki.  
2. Valitse haluamasi myyntitoimitus asiakkaalle toiseen EU-maahan tai toiselle EU-alueelle.  
3. Valitse **Tila**-kentässä asianmukainen vaihtoehto.  

   Jos asiakas on palauttanut allekirjoitetun tarjontatodistuksen, valitse **Vastaanotettu**. **Vast.ott. pvm**-kenttä päivitetään. Vastaanottopäivämääräkksi määritetään oletusarvon mukaan nykyinen käsittelypäivämäärä.  

   Voit muokata päivämäärän vastaamaan päivämäärää, jolloin vastaanotit asiakkaan allekirjoittaman tarjontasertifikaatin. Voit myös lisätä linkin allekirjoitettuun sertifikaattiin käyttämällä vakiomuotoista [!INCLUDE[prod_short](includes/prod_short.md)] -linkitystä.  

   Jos asiakas ei palauta allekirjoitettua tarjontatodistusta, valitse **Ei vastaanotettu**. Tämän jälkeen sinun on lähetettävä asiakkaalle uusi lasku, joka sisältää ALV:n, koska veroviranomainen ei hyväksy alkuperäistä laskua.  

Voit tarkastella sertifikaattiryhmiä aloittamalla **Tarjontasertifikaatit**-sivulta ja päivitä sitten avointen sertifikaattien tila, kun vastaanotat ne asiakkaalta. Tästä voi olla hyötyä, jos haluat etsiä kaikki tietyn tilan omaavat sertifikaatit, esimerkiksi **Pakollinen**, ja joille haluat päivittää tilaksi **Ei vastaanotettu**.  

### <a name="to-update-the-status-of-a-group-of-certificates-of-supply" />Tilauksen tarjontasertifikaattien ryhmän tilan päivittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tarjontasertifikaatit** ja valitse sitten vastaava linkki.  
2. Suodata **Tila**-kenttä arvoon, jonka haluat luodaksesi luettelon sertifikaateista, joita haluat hallita.  
3. Päivitä tilan tiedot valitsemalla **Muokkaa luetteloa**.  
4. Valitse **Tila**-kentässä sopiva vaihtoehto.  

   Jos asiakas on palauttanut allekirjoitetun tarjontatodistuksen, valitse **Vastaanotettu**. **Vast.ott. pvm**-kenttä päivitetään. Vastaanottopäivämääräkksi määritetään oletusarvon mukaan nykyinen käsittelypäivämäärä.  

   Voit muokata päivämäärän vastaamaan päivämäärää, jolloin vastaanotit allekirjoitetun tarjontasertifikaatin. Voit myös lisätä linkin allekirjoitettuun sertifikaattiin käyttämällä [!INCLUDE[prod_short](includes/prod_short.md)]in asiakirjojen vakiolinkitystä.  

> [!NOTE]
> Et voi luoda uutta tarjontasertifikaattia **Tarjontasertifikaatit**-sivulla, kun siirryt siihen tällä menetelmällä. Voit luoda sertifikaatin toimitukselle, jota ei asetettu vaatimaan sitä avaamalla kirjatun myyntitoimituksen, ja käyttämällä yhtä kahdesta yllä kuvatusta toimenpiteestä:  
>
> * Tarjontasertifikaatin luominen manuaalisesti  
> * Tarjontasertifikaatin tulostaminen.

## <a name="see-related-microsoft-training" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/paths/process-vat-dynamics-365-business-central/)

## <a name="see-also" />Katso myös

[Arvonlisäveron laskemisen ja kirjaustapojen määrittäminen](finance-setup-vat.md)  
[ALV:n raportointi veroviranomaisille](finance-how-report-vat.md)  
[ALV-rekisterinumeron vahvistaminen](finance-how-validate-vat-registration-number.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
