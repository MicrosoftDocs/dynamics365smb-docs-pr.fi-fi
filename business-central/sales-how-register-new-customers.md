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
ms.search.form: 7, 21, 22, 33, 42, 43, 367, 368, 369, 512, 785, 1330, 1380, 1381, 1382, 1627, 2107, 7177, 9080, 9081, 9084, 9301, 9305
ms.date: 09/24/2021
ms.author: edupont
ms.openlocfilehash: 19430c43a0564dc1334d4bc9b314ef6a93e0b65c
ms.sourcegitcommit: a9e2aaee735870af566db68532cfa697347d68e0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752290"
---
# <a name="register-new-customers"></a>Uusien asiakkaiden rekisteröinti

Asiakkaat ovat tulonlähteesi. Jokainen asiakas, jolle myyt, on rekisteröitävä asiakaskorttina. Asiakkaan kortit sisältävät tietoja, jotka tarvitaan tuotteiden asiakkaalle myymistä varten. Lisätietoja on kohdissa [Myynnin laskutus](sales-how-invoice-sales.md) ja [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).  

Ennen kuin voit rekisteröidä uusia asiakkaita, sinun on määritettävä myyntikoodit, jotka voidaan valita asiakkaiden korttien täyttämisen yhteydessä. Lisätietoja on kohdassa [Myynnin määrittäminen](sales-setup-sales.md).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a>Uusien asiakkaiden lisääminen
Voit lisätä uusia asiakkaita manuaalisesti täyttämällä **Asiakaskortti**-sivun kentät tai käyttämällä malleja, jotka sisältävät ennalta määritettyjä tietoja. Voit esimerkiksi luoda malleja erityyppisille asiakasprofiileille. Mallien käyttäminen säästää aikaa uusien asiakkaiden lisäämisen aikana ja varmistaa, että tiedot ovat aina oikein. Jos luot malleja useammalle kuin yhdelle asiakastyypille, voit valita mallin, jota käytetään, kun lisäät asiakkaan. Jos luot vain yhden mallin, sitä käytetään kaikille uusille asiakkaille. Kun olet luonut mallin, voit kohdistaa sen yhteen tai useampaan valittuun asiakkaaseen käyttämällä **Käytä mallia** -toimintoa. Kun haluat luoda mallin, täytä tiedot, joita haluat käyttää uudelleen Asiakaskortti-sivulla, ja tallenna se mallina. Lisätietoja on osassa [Asiakaskortin tallentaminen mallina](sales-how-register-new-customers.md#to-save-the-customer-card-as-a-template).

> [!TIP]
> Voi olla hyödyllistä mukauttaa **Asiakasmalli**-sivua, kun luot mallin. Haluat ehkä esimerkiksi lisätä **Luottoraja**-kentän malliin. Lisätietoja on kohdassa [Työtilan mukauttaminen](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

Asiakkaan voi luoda myös yhteyshenkilöstä. Lisätietoja on kohdassa [Asiakkaan, toimittajan, työntekijän tai pankkitilin luominen yhteyshenkilöstä](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

### <a name="to-create-a-new-customer-card"></a>Uuden asiakkaan kortin luominen

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

**Hinnat ja alennukset** -toiminto tarjoaa vaihtoehtoja asiakkaan erikoishintojen tai -alennusten hallintaan, kun tilaus täyttää tietyt ehdot. Ehdot voivat olla esimerkiksi silloin, kun he ostavat tietyn nimikkeen, tilaavat vähimmäismäärän tai ostavat ennen päivämäärää, kuten kampanjan loppuessa. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).

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

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntien ja myyntisaamisten asetukset** ja valitse sitten vastaava linkki.

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
