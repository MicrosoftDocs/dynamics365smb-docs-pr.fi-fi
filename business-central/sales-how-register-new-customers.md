---
title: Uusien asiakkaiden rekisteröiminen asiakkaan kortin luomisen avulla
description: Tässä ohjeaiheessa kerrotaan, miten asiakkaan kortti luodaan rekisteröimään tietoja kustakin uudesta asiakkaasta, jolle myyt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client, customer, credit
ms.date: 03/09/2021
ms.author: edupont
ms.openlocfilehash: d873c1546cebfccc6d2549b1de2b9d111589c553
ms.sourcegitcommit: 35f7e24c301926b39094aa64fe608afd04fdb8e1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573424"
---
# <a name="register-new-customers"></a>Uusien asiakkaiden rekisteröinti

Asiakkaat ovat tulonlähteesi. Jokainen asiakas, jolle myyt, on rekisteröitävä asiakaskorttina. Asiakkaan kortit sisältävät tietoja, jotka tarvitaan tuotteiden asiakkaalle myymistä varten. Lisätietoja on kohdissa [Myynnin laskutus](sales-how-invoice-sales.md) ja [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).  

Ennen kuin voit rekisteröidä uusia asiakkaita, sinun on määritettävä myyntikoodit, jotka voidaan valita asiakkaiden korttien täyttämisen yhteydessä. Lisätietoja on kohdassa [Myynnin määrittäminen](sales-setup-sales.md).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a>Uusien asiakkaiden lisääminen

Uusi asiakas rekisteröidään täyttämällä asiakaskortti. Eri asiakasprofiileille voi luoda mallit tai asiakkaat voidaan lisätä ilman malleja.  

> [!NOTE]  
> Jos eri asiakastyypeille on olemassa asiakasmalleja, sivu avautuu, kun luot uuden asiakkaan kortin, jossa voit valita haluamasi mallin. Jos vain yksi asiakasmalli on olemassa, uudet asiakaskortit käyttävät aina kyseistä mallia.  

### <a name="to-create-a-new-customer-card"></a>Uuden asiakkaan kortin luominen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.  
2. Valitse **Asiakkaat** -sivulla **Uusi**-toiminto.

    Jos vain yksi asiakasmalli on olemassa, uusi asiakkaan kortin avautuu. Osa kortin kentistä täytetty mallin tiedoilla.

    Jos on olemassa useita asiakasmalleja, näyttöön avautuu automaattisesti sivu, jossa voit valita asiakasmallin. Noudata tällaisessa tapauksessa kahta seuraavaa vaihetta.
3. Valitse **Valitse malli uudelle asiakkaalle** -sivulla malli, jota haluat käyttää uudessa asiakkaan kortissa.
4. Valitse **OK**-painike. Uuden asiakkaan kortti avautuu. Osa kortin kentistä on täytetty mallin tiedoilla.  
5. Voit täyttää asiakkaan kortin kenttiä tai muuttaa niitä tarvittaessa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**Myyntihinnat**-pikavälilehti sisältää erityiset hinnat tai alennukset, jotka haluat myöntää asiakkaalle, jos tietyt ehdot, kuten nimike, vähimmäistilausmäärä tai päättymispäivämäärä, täyttyvät. Kukin rivi edustaa erityistä hinnan alennusta tai rivialennusta. Kukin sarake vastaa ehtoa, joka takaa **Yksikköhinta**-kenttään kirjoitetun erikoishinnan tai **Rivialennus-%**-kenttään kirjoitetun rivialennuksen. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).

Asiakas on nyt rekisteröity, ja asiakkaan kortti on valmis käytettäväksi myyntiasiakirjoissa.

Jos haluat käyttää tätä asiakkaan korttia mallina, kun luot uusia asiakkaan kortteja, tallenna se mallina. Lisätietoja on seuraavassa osassa.  

### <a name="to-save-the-customer-card-as-a-template"></a>Asiakkaan kortin tallentaminen mallina

1. Valitse **Asiakkaan kortti** -sivulla **Tallenna mallina** -toiminto. **Asiakasmalli**-sivu avautuu ja näyttää asiakaskortin mallina.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voit käyttää dimensioita malleina valitsemalla **Dimensiot**-toiminnon. **Dimensiomallit**-sivu avautuu. Se sisältää kaikki asiakkaalle määritetyt dimensiokoodit.
4. Muokkaa tai syötä dimensiokoodit, joita käytetään mallin avulla luotuihin uusiin asiakkaan kortteihin.  
5. Kun olet määrittänyt uuden asiakasmallin, valitse **OK**-painike.

Asiakasmalli lisätään asiakasmallien luetteloon niin, että sen avulla voit luoda uusia asiakkaiden kortteja.

## <a name="deleting-customer-cards"></a>Asiakaskorttien poistaminen

Jos olet kirjannut asiakkaalle tapahtuman, et voi poistaa korttia, koska nimiketapahtumia voi tarvita valvontaan. Voit poistaa asiakaskortin, jossa on tapahtumakirjauksia ottamalla yhteyttä Microsoft-kumppaniisi koodin avulla.  

## <a name="managing-credit-limits"></a>Luottorajojen hallinta

Luottoraja-, saldosumma- ja maksuehto-ominaisuudet mahdollistavat sen, että [!INCLUDE [prod_short](includes/prod_short.md)] antaa luottovaroituksen ja erääntynyt saldo -varoituksen tullessasi myyntitilaukseen.  Lisäksi muistutusehto- ja viivästyskuluehto-ominaisuuksien ansiosta voit laskuttaa korkoja ja/tai lisämaksuja.  

Asiakaskortin **Luottoraja**-kentässä määritetään enimmäissumma, jonka sallit asiakkaan ylittää maksusaldon ennen varoitusten antamista. Kun sitten syötät tietoja päiväkirjoihin, tarjouksiin, tilauksiin ja laskuihin, [!INCLUDE [prod_short](includes/prod_short.md)] testaa myynnin tunnistetiedot ja yksittäiset myyntirivit ja tarkistaa, onko luottoraja ylitetty.

Vaikka luottoraja on ylitetty, silti voidaan kirjata. Jos kenttä on jätetty tyhjäksi, tällä asiakkaalla ei ole luottorajaa.  

Voit valita, ettet saa varoitusta siitä, että asiakkaan luottoraja on ylitetty, ja voit määrittää, minkä tyyppisiä varoituksia haluat nähdä.

### <a name="to-specify-credit-limit-warnings"></a>Luottorajavaroitusten määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntien ja myyntisaamisten asetukset** ja valitse sitten liittyvä linkki.

2. Valitse **Yleiset**-pikavälilehden **Luottovaroitukset**-kentässä haluamasi vaihtoehdot seuraavassa taulukossa kuvatulla tavalla:

    |Asetus| Kuvaus|
    |------|------------|
    |**Molemmat varoitukset**| Kun käytät tätä vaihtoehtoa, ohjelma tarkastaa sekä **Luottoraja**- että **Erääntyvä saldo**-kentät asiakaskortista ja antaa varoituksen, jos asiakas on ylittänyt luottorajansa, ja jos asiakkaalla on erääntynyt saldo.|
    |**Luottoraja**|Asiakaskortin **Luottoraja**-kentän arvoa verrataan asiakkaan saldoon, ja näyttöön tulee varoitus, jos asiakkaan saldo ylittää kentän arvon.|
    |**Erääntynyt saldo**|**Erääntynyt saldo** -kenttä asiakkaan kortilla on valittuna ja jos asiakkaalla on erääntyneitä saldoja, näytetään varoitus.|
    |**Ei varoitusta**|Asiakkaan tilasta ei näytetä varoituksia.|

## <a name="see-also"></a>Katso myös

[Maksutapojen määrittäminen](finance-payment-methods.md)  
[Tietueiden kaksoiskappaleiden yhdistäminen](sales-how-merge-duplicate-records.md)  
[Numerosarjojen luominen](ui-create-number-series.md)  
[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]