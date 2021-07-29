---
title: Ennakkomaksujen määrittäminen
description: Tietoja siitä, miten Business Central määritetään niin, että ennakkomaksutoimintojen avulla voit laskuttaa ja kerätä asiakkailta talletuksia tai suorittaa talletuksia toimittajille.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keyword: prepayment
ms.date: 06/29/2021
ms.author: edupont
ms.openlocfilehash: a8b647e52457fc4bc2c7377ad6d4fb4f40d6dc58
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6446313"
---
# <a name="set-up-prepayments"></a>Ennakkomaksujen määrittäminen
Jos haluat, että asiakkaat lähettävät maksun ennen kuin toimitat heille tilauksen tai jos toimittaja haluaa maksun ennen kuin toimitus lähetetään sinulle, voit käyttää Ennakkomaksu-toimintoa. Ennakkomaksutoiminnon avulla voit laskuttaa ja periä toiminnolla asiakkailta edellytettäviä talletuksia tai suorittaa talletuksia toimittajille sekä varmistaa, että kaikki osamaksut kohdistetaan laskuun. Lisätietoja on kohdassa [Ennakkomaksulaskujen luominen](finance-how-to-create-prepayment-invoices.md).

Ennen kuin voit kirjata ennakkomaksulaskuja, sinun on määritettävä kirjaustilit pääkirjanpitoon sekä määritettävä numerosarjat ennakkomaksuasiakirjoille. Määritä myyntiin ja ostoon liittyville ennakkomaksuille tilit. Voit määrittää kirjaustilit, joita käytetään kaikille yleisiin liiketoiminnan kirjausryhmiin tai yleisiin tuotteen kirjausryhmiin liittyville ennakkomaksuille. Voit myös määrittää tietyille myynnin ja oston kirjausryhmille omat tilit. Tämä riippuu siitä, millaisia vaatimuksia yrityksellä on ennakkomaksujen seurantaa varten.  

Voit määrittää toimittajan tai asiakkaan ennakkomaksuna laskutettavan rivisumman prosenttiosuuden kaikille nimikkeille tai valituille nimikkeille. Kun olet saanut asetukset valmiiksi, voit luoda ennakkomaksulaskuja myynti- ja ostotilauksista. Voit käyttää kullekin myynti- tai ostoriville oletusprosenttiosuuksia tai voit muuttaa laskun summia tarpeen mukaan. Voit määrittää esimerkiksi koko tilauksen yhteissumman.  

> [!NOTE]
> 100 prosentin ennakkomaksua ei kannata käyttää seuraavissa tilanteissa:
> * Sijaintisi on Pohjois-Amerikassa. Verojen laskutavan vuoksi 100 prosentin ennakkomaksu voi aiheuttaa ongelmia ennakkomaksulaskuissa.
> * Kaikilla alueilla, jos maksualennus vähennetään manuaalisesti laskusta. 100 prosentin ennakkomaksua ei jätä automaattisesti summaa, josta alennus vähennetään. 

Koska ennakkoon maksettu summa kuuluu ostajalle siihen asti, kunnes hän on vastaanottanut tavarat tai palvelut, sinun on määritettävä KP-tilit, joilla ennakkomaksusummia pidetään viimeisen laskun lähetykseen asti. Myynnin ennakkomaksut on tallennettava ostovelkatilille nimikkeiden toimitukseen asti. Oston ennakkomaksut on tallennettava käyttöomaisuustilille nimikkeiden vastaanottoon asti. Lisäksi on määritettävä erillinen kirjanpitotili jokaiselle ALV-tunnukselle.  

[!INCLUDE[local-func-setup-link](includes/local-func-setup-link.md)]

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>Ennakkomaksutilien lisääminen yleisiin kirjausasetuksiin  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleiset kirjausasetukset** ja valitse sitten vastaava linkki.
2. Täytä **Yleiset kirjausasetukset** -sivulla seuraavat kentät:  

    - **Myynnin ennakkomaksutili**  
    - **Ostojen ennakkomaksutili**  

> [!TIP]
> Jos **Yleiset kirjausasetukset** -sivun kentät eivät ole näkyvissä, siirry sivulla oikealle sivun alaosassa olevan vaakavierityspalkin avulla.  

Jos et ole vielä määrittänyt ennakkomaksujen pääkirjanpitotilejä, voit avata sen **KP-tililuettelo**-sivun kyseisen tilin kentästä.  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>Ennakkomaksuasiakirjojen numerosarjojen määrittäminen  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntien ja myyntisaamisten asetukset** ja valitse sitten vastaava linkki.
2. Täytä seuraavat kentät **Myyntien ja myyntisaamisten asetukset** -sivulla.  

   - **Kirjattujen ennakkomaksulaskujen nrot**
   - **Kirjattujen ennakkomaksun hyvityslaskujen nrot**

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostojen ja maksettavien määritys** ja valitse sitten vastaava linkki.
2. Täytä **Ostojen ostovelkojen asetukset** -sivulla seuraavat kentät:

    - **Kirjattujen ennakkomaksulaskujen nrot**
    - **Kirjattujen ennakkomaksun hyvityslaskujen nrot**

> [!NOTE]  
> Voit käyttää ennakkomaksuissa ja tavallisissa maksuissa samoja tai erilaisia numerosarjoja. Jos käytät erilaisia sarjoja, ne eivät saa olla päällekkäisiä, koska sarjoissa ei saa olla samoja numeroita.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Nimikkeiden, asiakkaiden ja toimittajien ennakkomaksuprosenttien määrittäminen  
Voit määrittää nimikkeelle oletusennakkomaksuprosentin kaikkia asiakkaita, tiettyä asiakasta tai asiakkaan hintaryhmää kohti.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.
2. Valitse ensin nimike ja sitten **Ennakkomaksuprosentit**-toiminto.  
3. Täytä tarvittavat kentät **Myynnin ennakkomaksuprosentit** -sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Voit määrittää asiakkaalle tai toimittajalle yhden kaikkia nimikkeitä ja kaikentyyppisiä myyntirivejä koskevan oletusennakkomaksuprosentin. Voit antaa sen asiakkaan tai toimittajan kortissa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
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
[Ennakkomaksujen arvonlisäveron laskeminen Australiassa](LocalFunctionality/Australia/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Ennakkomaksujen arvonlisäveron laskeminen Uudessa-Seelannissa](LocalFunctionality/NewZealand/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Pääkirjanpito ja aitoustodistus](finance-general-ledger.md)  
[Rahoitus](finance.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]