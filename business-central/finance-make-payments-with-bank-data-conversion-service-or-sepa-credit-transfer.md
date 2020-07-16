---
title: Maksujen suorittaminen AMC Banking 365 Fundamentals -laajennuksen tai SEPA-tilisiirron avulla | Microsoft Docs
description: Käsittele maksut toimittajille viemällä tiedoston yhdessä maksutietojen kanssa päiväkirjan riveiltä.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/07/2020
ms.author: bholtorf
ms.openlocfilehash: dbee0561f2baa52484df1fbebf8e4875dd3f7245
ms.sourcegitcommit: 8b2f02dd5189c46ecff33c07223ed62b36842d34
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2020
ms.locfileid: "3542715"
---
# <a name="make-payments-with-the-amc-banking-365-fundamentals-extension-or-sepa-credit-transfer"></a>Maksujen suorittaminen AMC Banking 365 Fundamentals -laajennuksen tai SEPA-tilisiirron avulla

Voit käsitellä **Maksupäiväkirja**-sivulla maksut toimittajille viemällä tiedoston yhdessä maksutietojen kanssa päiväkirjan riveiltä. Voit sitten ladata tiedoston verkkopankkiin, jossa liittyvät rahansiirrot käsitellään. [!INCLUDE[d365fin](includes/d365fin_md.md)] tukee SEPA-hyvitysten siirtomuotoa, mutta maa- tai aluekohtaisesti voi olla käytettävissä muita sähköisiä maksumuotoja.

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_md.md)]in yleisessä versiossa asetetaan ja yhdistetään yleiset palvelut pankkitietojen muuntamiseen mihin tahansa pankkisi vaatimaan muotoon. Pohjoisamerikkalaisessa versioissa maksutiedostot voidaan lähettää samalla palvelulla sähköisenä rahansiirtona, joskin prosessi on hieman erilainen. Lisätietoja on kohdan [Maksujen vienti pankkitiedostoon](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file) vaiheessa 6.  

 Kun haluat ottaa SEPA-hyvityksen siirrot käyttöön, määritä ensin pankkitili, toimittaja ja yleinen päiväkirja, johon maksupäiväkirja perustuu. Tämän jälkeen maksut valmistellaan toimittajia varten automaattisesti täyttämällä erääntyneet maksut ja määritetyt kirjauspäivämäärät **Maksupäiväkirja**-sivulle.  

> [!NOTE]  
> Kun olet varmistanut, että pankki on käsitellyt maksut onnistuneesti, voit jatkaa maksupäiväkirjan rivien kirjaamista.  

## <a name="setting-up-the-amc-banking-365-fundamentals-extension"></a>AMC Banking 365 Fundamentals -laajennuksen määrittäminen

Voit aktivoida AMC Banking 365 Fundamentals -laajennuksen, jolla voi muuntaa minkä tahansa pankin tiliotteen tuotavaan muotoon, tai voit muuttaa viedyt maksutiedostot pankin edellyttämään muotoon. Lisätietoja on kohdassa [AMC Banking 365 Fundamentals -laajennuksen käyttäminen](ui-extensions-amc-banking.md).

## <a name="setting-up-sepa-credit-transfer"></a>SEPA-hyvityksen siirron määrittäminen

Voit viedä maksuja **Maksupäiväkirja**-sivulta tiedostoon siirrettäväksi verkkopankkiisi liittyvien tilisiirtojen käsittelemiseksi. [!INCLUDE[d365fin](includes/d365fin_md.md)] tukee SEPA-hyvitysten siirtomuotoa, mutta maa- tai aluekohtaisesti voi olla käytettävissä muita sähköisiä maksumuotoja.  

Jos haluat ottaa käyttöön sellaisten pankkitiedostomuotojen viennin, joita [!INCLUDE[d365fin](includes/d365fin_md.md)] ei tue suoraan, voit määrittää tiedonsiirtomäärityksen tiedonsiirtokehyksen avulla. Lisätietoja on kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).  

Ennen kuin voit käsitellä maksun sähköisesti viemällä maksutiedostot SEPA-hyvityksen siirto -muodossa, sinun on suoritettava seuraavat asetukset:  

* Määritä kyseinen pankkitilin käsittelemään SEPA-hyvityksen siirtomuoto  
* Määritä toimittajan kortit, jotta voit käsitellä maksut viemällä tiedostot SEPA-hyvityksen siirtomuotoon  
* Määritä liittyvä yleisen päiväkirja erä ottamaan käyttöön maksujen vienti **Maksupäiväkirja**-sivulta  
* Yhdistä vähintään yhden maksutyypin tiedonsiirtomääritys liittyvään maksutapaan  

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a>Pankkitilin määrittäminen SEPA-hyvityksen siirtoa varten

1. Syötä **Etsi**-ruudussa **Pankkitilit** ja valitse sitten vastaava linkki.  
2. Avaa sen pankkitilin kortti, josta viet maksutiedostot SEPA-hyvitys siirtomuodossa.  
3. Valitse **Siirto**-välilehden **Maksun vientimuoto** -kentässä **SEPACT**.  
4. Valitse **Yleiset**-pikavälilehden **Hyvityksen siirtoviestinrot** -kentässä numerosarja, josta numerot määritetään SEPA-tilisiirtotapahtumiin.  
5. Varmista, että **IBAN**-kenttä on täytetty.  

    > [!NOTE]  
    > **Valuuttakoodi**-kentän asetuksena on oltava **EUR**, koska SEPA-hyvityksen siirrot voidaan tehdä vain euroina.  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a>Toimittajan kortin määrittäminen SEPA-hyvityksen siirtoa varten

1. Syötä **Etsi**-ruudussa **Toimittajat** ja valitse sitten vastaava linkki.  
2. Avaa sen toimittajan kortti, josta maksat sähköisesti viemällä maksutiedostot SEPA-hyvitys siirtomuodossa.  
3. Valitse **Maksu**-pikavälilehden **Maksutavan koodi** -kentässä **PANKKI**.  
4. Valitse **Ensisijainen pankkitili** -kentässä pankki, johon rahat siirretään, kun ne käsitellään verkkopankissasi.  

     **Ensisijainen pankkitili** -kentän arvo kopioidaan **Maksupäiväkirja**-sivun **Vastaanottajan pankkitili** -kenttään.  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a>Maksupäiväkirjan määrittäminen maksutiedostojen vientiä varten

1. Anna **Haku**-ruudussa **Maksupäiväkirjat** ja valitse sitten vastaava linkki.  
2. Avaa maksupäiväkirja, jota käytät maksujen käsittelyyn viemällä tiedostot SEPA-hyvitys siirtomuodossa.  
3. Valitse **Erän nimi** -kentässä avattavan\- luettelon painike.  
4. Valitse **Yleisen päiväkirjan erät** -sivulla **Muokkaa luetteloa** -toiminto.  
5. Valitse sen maksupäiväkirjan rivillä, jonka avulla viet maksut, **Salli maksun vienti** -valintaruutu.  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a>Vähintään yhden maksutyypin tiedonsiirtomäärityksen yhdistäminen liittyvään maksutapaan

1. Anna **Haku**-ruudussa **Maksutavat** ja valitse sitten vastaava linkki.  
2. Valitse **Maksutavat**-sivulla ensin maksutapa, jolla maksut viedään, ja sitten **Maksun vientirivin määritys** -kenttä.  
3. Valitse **Maksun vientirivin määritykset** -sivulla koodi, jonka määritit **Rivimääritykset**-pikavälilehden **Koodi**-kentässä ohjeaiheen [Tiedonsiirtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md) Tiedoston rivien ja sarakkeiden muotoilun kuvaaminen -kohdan vaiheessa 4.  

Suoraveloitusvaltakirja lisätään automaattisesti **Suoraveloitusvaltakirjan tunnus** -kenttään, kun luot myyntilaskun vaiheessa 2 valitulle asiakkaalle. Lisätietoja on kohdassa [Toistuvien myynti- ja ostorivien luominen](sales-how-work-standard-lines.md).  

## <a name="preparing-the-payment-journal"></a>Maksupäiväkirjan valmistelu

Täytä maksupäiväkirja toimittajiin kohdistuvilla erääntyvillä maksuriveillä ja vaihtoehdolla lisätä kirjauspäivämäärät perustuen liittyvien ostoasiakirjojen eräpäivään. Lisätietoja on kohdassa [Ostovelkojen hallinta](payables-manage-payables.md).

## <a name="exporting-payments-to-a-bank-file"></a>Maksujen vienti pankkitiedostoon

Kun olet valmis suorittamaan maksut toimittajille tai hyvitykset työntekijöille, voit viedä tiedoston ja päiväkirjan rivien maksutiedot **Maksupäiväkirja**-sivulla. Voit sitten ladata tiedoston pankkiin kyseisten rahansiirtojen käsittelyä varten.

AMC Banking 365 Fundamentals -laajennus on saatavana [!INCLUDE[d365fin](includes/d365fin_md.md)]in yleisessä versiossa. Pohjoisamerikkalaisessa versioissa maksutiedostot voidaan lähettää samalla laajennuksella sähköisenä rahansiirtona, joskin prosessi on hieman erilainen. Lisätietoja on kohdan [Maksujen vienti pankkitiedostoon](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file) vaiheessa 6.

> [!NOTE]  
> Määritä liittyvän pankkitilin sähköinen muoto ennen maksutiedostojen vientiä maksupäiväkirjasta ja ota AMC Banking 365 Fundamentals -laajennus käyttöön. Lisätietoja on kohdissa [Pankkitilin määrittäminen](bank-how-setup-bank-accounts.md) ja [AMC Banking 365 Fundamentals -laajennuksen käyttäminen](ui-extensions-amc-banking.md). Valitse myös **Salli maksun vienti** -valintaruutu **Yleisen päiväkirjan erät** -sivulla. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).  

Voit tarkastella maksupäiväkirjasta vietyjä maksutiedostoja **Hyvityksen siirron rekisterit** -sivulla. Voit myös viedä sivulla maksutiedostot uudelleen, jos tekniset virheet tai tiedostomuutokset vaativat sitä. Huomaa kuitenkin, että viedyt sähköiset rahansiirtotiedostot eivät näy tällä sivulla eikä niitä voi viedä uudelleen.  

### <a name="to-export-payments-to-a-bank-file"></a>Maksujen vienti pankkitiedostoon

Seuraavassa kuvataan, miten toimittajalle maksetaan sekillä. Vaiheet ovat samankaltaiset kuin hyvitettäessä asiakkaalle sekkimaksuna.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten liittyvä linkki.
2. Täytä maksupäiväkirjan rivit. Lisätietoja on ohjeaiheessa [Maksujen ja hyvitysten kirjaaminen](payables-how-post-payments-refunds.md).

    > [!NOTE]
    > Jos käytät sähköistä rahansiirtoa, sinun on valittava joko **Sähköinen maksu** tai **Sähköinen maksu – IAT** **Pankkimaksun tyyppi** -kentässä. Eri tiedostojen vientipalvelut ja niiden tiedostomuodot edellyttävät erilaisia asetuksia **Pankkitilin kortti**- ja **Toimittajan pankkitilin kortti** -sivuilla. Saat ilmoituksen virheellisistä tai puuttuvista asetusarvoista, kun yrität viedä tiedoston.
    >
    > EFT-ominaisuutta voi käyttää vain pankkitileille, jotka on määritetty paikallisena valuuttana. Sitä ei voi käyttää ulkomaan valuutalle, mikä ilmaistaan **Valuutan koodi** -kentässä olevalla arvolla. (Tyhjä kentän arvo tarkoittaa paikallista valuuttaa.)

3. Kun kaikki maksupäiväkirjan rivit ovat valmiit, valitse **Vie**-toiminto.
4. Täytä **Vie sähköiset maksut** -sivun kentät tarpeen mukaan.

    Virheilmoituksia näkyy **Maksutiedoston virheet** -tietoruudussa, jossa voit myös nähdä yksityiskohtaiset tiedot virheviestistä. Kaikki virheet on ratkaistava ennen maksutiedoston vientiä.

    > [!TIP]  
    > AMC Banking 365 Fundamentals -laajennusta käytettäessä yleinen virhesanoma ilmaisee, että pankkitilin numeron pituus ei täytä pankin vaatimuksia. Voit välttää tämän virheen tai ratkaista sen poistamalla **IBAN**-kentän **Pankkitilin kortti** -sivulla ja antamalla sitten pankkitilin numeron **Pankkitilin nro** -kentässä pankin edellyttämässä muodossa.

5. Määritä **Tallenna nimellä** -sivulla paikka, johon tiedosto viedään, ja valitse sitten **Tallenna**.

    > [!NOTE]  
    > Jos käytät sähköistä rahansiirtoa, tallenna saatava toimittajan maksusuorituslomake Word-asiakirjana tai valitse sen lähettäminen suoraan toimittajalle. Maksut on nyt lisätty **Luo sähköinen rahansiirtotiedosto** -sivulle, jossa voit luoda samanaikaisesti useita maksutilauksia, mikä säästää lähetyskustannuksia. Lisätietoja on seuraavissa vaiheissa:
6. Valitse **Maksupäiväkirja**-sivulla **Luo sähköinen rahansiirtotiedosto** -toiminto.

    **Luo sähköinen rahansiirtotiedosto** -sivulla kaikki sähköistä rahansiirtoa varten määritetyt maksut, jotka on viety maksupäiväkirjasta määritetylle pankkitilille mutta joita ei ole vielä muodostettu, on mainittu **Rivit**-pikavälilehdessä.
7. Vie kaikki sähköiset rahansiirtomaksut sisältävä tiedosto valitsemalla **Luo sähköinen rahansiirtotiedosto** -toiminto.
8. Määritä **Tallenna nimellä** -sivulla paikka, johon tiedosto viedään, ja valitse sitten **Tallenna**.

Pankin maksutiedosto viedään määrittämääsi sijaintiin ja voit jatkaa sen lataamista verkkopankkitilille ja suorittaa todelliset maksut. Voit sitten kirjata viedyn maksupäiväkirjan rivit.

### <a name="to-plan-when-to-post-exported-payments"></a>Vietyjen maksujen kirjaamisajankohdan suunnitteleminen

Jos et halua kirjata viedyn maksun maksupäiväkirjan riviä, koska esimerkiksi odotat pankin vahvistusta tapahtuman käsittelystä, voit poistaa päiväkirjan rivin. Kun luot myöhemmin maksupäiväkirjan rivin, jolla maksetaan jäljellä oleva laskun summa, **Viety summa yhteensä** -kenttä näyttää, kuinka paljon maksun summasta on jo viety. Lisäksi saat lisätietoja viedystä kokonaissummasta valitsemalla **Hyvityksen siirron rekisterimerkinnät** -painikkeen, joka avaa vietyjen maksutiedostojen tiedot.

Jos noudatat prosessia, jossa maksut kirjataan vasta sen jälkeen, kun pankin suorittamasta maksujen käsittelystä on saatu vahvistus, voit hallita tätä kahdella eri tavalla.

* Maksupäiväkirjan ehdotettujen maksurivien kohdalla voit lajitella joko **Viety maksutiedostoon** -sarakkeen tai **Viety summa yhteensä**-kentän mukaan ja sitten poistaa maksuehdotukset avoimilta laskuilta, jotka on jo maksettu ja joita et halua maksaa.
* Voit valita **Ehdota toimittajamaksuja** -sivulla, jossa määrität maksupäiväkirjaan lisättävät maksut, **Ohita viedyt maksut** -valintaruudun, jos et halua lisätä päiväkirjarivejä jo viedyille maksuille.

Saat lisätietoja viedyistä maksuista valitsemalla **Maksujen vientihistoria** -toiminnon.

### <a name="to-re-export-payments-to-a-bank-file"></a>Maksujen vieminen uudelleen pankkitiedostoon

Voit viedä maksutiedostot uudelleen **Hyvityksen siirron rekisterit** -sivulla. Ennen kuin poistat tai kirjaat maksupäiväkirjan rivejä, voit myös viedä maksutiedoston uudelleen **Maksupäiväkirja**-sivulla yksinkertaisesti viemällä sen uudelleen. Jos olet poistanut tai kirjannut maksupäiväkirjan rivit viennin jälkeen, voit viedä saman maksutiedoston uudelleen **Hyvityksen siirron rekisterit** -sivulla. Valitse rivi tilisiirtojen erälle, jonka haluat viedä uudelleen, ja käyttämällä sitten **Vie maksut uudelleen tiedostoon** -toimintoa.

> [!NOTE]  
> Viedyt sähköiset rahansiirtotiedostot eivät näy **Hyvityksen siirron rekisterit** -sivulla, eikä niitä voi viedä uudelleen.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyvityksen siirron rekisterit** ja valitse sitten liittyvä linkki.
2. Valitse ensin uudelleenvietävä maksun vienti ja sitten **Vie maksut uudelleen tiedostoon** -toiminto.

## <a name="posting-the-payments"></a>Maksujen kirjaaminen

Kirjaa maksut sen jälkeen, kun pankki on käsitellyt ne onnistuneesti. Lisätietoja on kohdassa [Maksujen suorittaminen](payables-make-payments.md).

## <a name="see-also"></a>Katso myös

[AMC Banking 365 Fundamentals -laajennuksen käyttäminen](ui-extensions-amc-banking.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[Maksujen kerääminen SEPA-suoraveloitusperintänä](finance-collect-payments-with-sepa-direct-debit.md)  
