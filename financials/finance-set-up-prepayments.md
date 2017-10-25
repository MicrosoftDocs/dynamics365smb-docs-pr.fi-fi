---
title: "Ennakkomaksujen määrittäminen | Microsoft Docs"
description: "Ennakkomaksut ovat maksuja, jotka on laskutettu ja kirjattu myynti- tai ostoennakkomaksun tilaukseen ennen lopullista laskutusta. Esimerkiksi ennen tilattujen nimikkeiden valmistamista voidaan edellyttää talletuksen tekemistä, tai ennen nimikkeiden toimittamista asiakkaalle voidaan edellyttää maksun suorittamista. Ennakkomaksutoimintojen avulla voit laskuttaa ja kerätä asiakkailta edellytettyjä talletuksia tai suorittaa talletuksia toimittajille. Näin voit varmistaa, että kaikki maksut kohdistetaan laskuun."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 11aef4cb4b1d40568b63662239a26993782201a3
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-prepayments"></a>Toimintaohje: Ennakkomaksujen määrittäminen
Jos haluat, että asiakkaat lähettävät maksun ennen kuin toimitat heille tilauksen tai jos toimittaja haluaa maksun ennen kuin toimitus lähetetään sinulle, voit käyttää Ennakkomaksu-toimintoa. Voit laskuttaa ja periä toiminnolla asiakkailta edellytettäviä talletuksia tai suorittaa talletuksia toimittajille sekä varmistaa, että kaikki osamaksut kohdistetaan laskuun. Lisätietoja on kohdassa [Toimintaohje: Ennakkomaksulaskujen luominen](finance-how-to-create-prepayment-invoices.md).

Ennen kuin voit kirjata ennakkomaksulaskuja, sinun on määritettävä kirjaustilit pääkirjanpitoon sekä määritettävä numerosarjat ennakkomaksuasiakirjoille.  

Voit määrittää toimittajan tai asiakkaan ennakkomaksuna laskutettavan rivisumman prosenttiosuuden kaikille nimikkeille tai valituille nimikkeille. Kun olet saanut asetukset valmiiksi, voit luoda ennakkomaksulaskuja myynti- ja ostotilauksista. Voit käyttää kullekin myynti- tai ostoriville oletusprosenttiosuuksia tai voit muuttaa laskun summia tarpeen mukaan. Voit määrittää esimerkiksi koko tilauksen yhteissumman.  

Koska ennakkoon maksettu summa kuuluu ostajalle siihen asti, kunnes hän on vastaanottanut tavarat tai palvelut, sinun on määritettävä KP-tilit, joilla ennakkomaksusummia pidetään viimeisen laskun lähetykseen asti. Myynnin ennakkomaksut on tallennettava ostovelkatilille nimikkeiden toimitukseen asti. Oston ennakkomaksut on tallennettava käyttöomaisuustilille nimikkeiden vastaanottoon asti. Lisäksi on määritettävä erillinen kirjanpitotili jokaiselle ALV-tunnukselle.

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>Ennakkomaksutilien lisääminen yleisiin kirjausasetuksiin  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Yleiset kirjausasetukset** ja valitse sitten aiheeseen liittyvä linkki.
2. Täytä **Yleiset kirjausasetukset** -ikkunassa seuraavat kentät:  

    - **Myynnin ennakkomaksutili**  
    - **Ostojen ennakkomaksutili**  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>Ennakkomaksuasiakirjojen numerosarjojen määrittäminen  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntien ja myyntisaamisten asetukset** ja valitse sitten aiheeseen liittyvä linkki.
2. Täytä seuraavat kentät **Myyntien ja myyntisaamisten asetukset** -ikkunassa.  

   - **Kirjattujen ennakkomaksulaskujen nrot**
   - **Kirjattujen ennakkomaksun hyvityslaskujen nrot**

1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Ostojen ostovelkojen asetukset** ja valitse sitten aiheeseen liittyvä linkki.
2. Täytä **Ostojen ostovelkojen asetukset** -ikkunassa seuraavat kentät:

    - **Kirjattujen ennakkomaksulaskujen nrot**
    - **Kirjattujen ennakkomaksun hyvityslaskujen nrot**

> [!NOTE]  
>  Voit käyttää ennakkomaksuissa ja tavallisissa maksuissa samoja tai erilaisia numerosarjoja. Jos käytät erilaisia sarjoja, ne eivät saa olla päällekkäisiä, koska sarjoissa ei saa olla samoja numeroita.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Nimikkeiden, asiakkaiden ja toimittajien ennakkomaksuprosenttien määrittäminen  
Voit määrittää nimikkeelle oletusennakkomaksuprosentin kaikkia asiakkaita, tiettyä asiakasta tai asiakkaan hintaryhmää kohti.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Nimikkeet** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse ensin nimike ja sitten **Ennakkomaksuprosentit**-toiminto.  
3. Täytä tarvittavat kentät **Myynnin ennakkomaksuprosentit** -ikkunassa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Voit määrittää asiakkaalle tai toimittajalle yhden kaikkia nimikkeitä ja kaikentyyppisiä myyntirivejä koskevan oletusennakkomaksuprosentin. Voit antaa sen asiakkaan tai toimittajan kortissa.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Asiakkaat** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa asiakkaan kortti.
3. Täytä **Ennakkomaksuprosentti**-kenttä.
4. Toista vaiheet muiden asiakkaiden tai toimittajien kohdalla.  

### <a name="to-determine-which-prepayment-percentage-has-first-priority"></a>Etusijalla olevan ennakkomaksuprosentin määrittäminen  
Tilauksella voi olla ennakkomaksuprosentti myynnin tunnistetiedoissa ja toinen prosentti riveillä nimikkeitä varten. Järjestelmä hakee jokaiselle myyntiriville ennakkomaksuprosentin seuraavassa järjestyksessä ja käyttää ensimmäistä löytämäänsä oletusprosenttia:  
1. Sen asiakkaan ja rivin nimikkeen ennakkoprosentti, jolle tilaus on luotu.  
2. Sen rivin ja asiakkaan hintaryhmän nimikkeen ennakkomaksuprosentti, johon asiakas kuuluu.  
3. Kaikkien asiakkaiden rivin nimikkeen ennakkomaksuprosentti.  
4. Myynnin tai ostojen tunnistetietojen ennakkomaksuprosentti.  

Toisin sanoin asiakaskortin ennakkomaksuprosenttia käytetään vain, jos nimikkeelle ei ole määritetty ennakkomaksuprosenttia. Jos kuitenkin muutat **Ennakkomaksuprosentti**-kentän sisältöä myynnin tai oston tunnistetiedoissa rivien luomisen jälkeen, kaikkien rivien ennakkomaksuprosentti päivitetään. Tällöin tilauksen luonti kiinteällä ennakkomaksuprosentin kanssa on helppoa nimikkeille määritetystä prosentista huolimatta.

## <a name="see-also"></a>Katso myös  
[Ennakkomaksujen laskuttaminen](finance-invoice-prepayments.md)  
[Vaihekuvaus: Myynnin ennakkomaksujen määrittäminen ja laskuttaminen](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Rahoitus](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

