---
title: Maksutapojen määrittäminen
description: 'Voit määrittää myynti- ja ostolaskuille maksutavan, kuten sekin, pankkisiirron, käteisen tai PayPal-maksun.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'check, bank transfer, cash, PayPal'
ms.search.form: '427,'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# <a name="set-up-payment-methods"></a>Maksutapojen määrittäminen

Maksutavat määrittävät, miten asiakkaiden halutaan ensisijaisesti maksavan ja miten haluat maksaa toimittajille. Maksutapa voi olla asiakas- tai toimittajakohtainen, Tyypillisiä maksutapoja ovat esimerkiksi **pankki**, **käteinen**, **sekki** tai **tili**.

Kun maksutapa määritetään asiakkaille ja toimittajille, heille luotavissa myynti- ja ostoasiakirjoissa käytetään aina samaa maksutapaa. Voit tarvittaessa muuttaa maksutapaa myynti- tai ostoasiakirjassa. Voit tehdä näin esimerkiksi tilanteessa, jossa haluat maksaa tietyn ostolaskun käteisenä sekin sijaan. Toimittajalle määritetty oletusmaksutapa ei muutu.

Myynti- ja ostoasiakirjoissa käytetään samaa maksutapaa. Jos maksutavaksi on määritetty _käteinen_, sitä käytetään maksuja maksettaessa ja niitä vastaanotettaessa. [!INCLUDE[prod_short](includes/prod_short.md)] tietää, että odotat myyntilaskua luodessasi vastaanottavasi maksun ja päin vastoin ostolaskuja luotaessa.

Palautusten hyvityslaskut ovat kuitenkin poikkeuksia, sillä rahavirrat kulkevat vastakkaisiin suuntiin eli sinulta asiakkaalle ja toimittajalta sinulle. Tämän vuoksi hyvityslaskuille ei määritetä oletusmaksutapaa. On kuitenkin olemassa vaihtoehtoinen menetelmä. Voit määrittää asiakkaalle tai toimittajalle maksuehdot. Vaikka **Laske maksualen. hyvityslask.** -kenttää ei ole tarkoitettu tähän kiertotapaan, tämän valintaruudun valitseminen **Maksuehdot**-sivulla lisää oletusmaksutavan hyvityslaskua luotaessa. <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## <a name="to-set-up-a-payment-method"></a>Maksutapojen määrittäminen

[!INCLUDE[prod_short](includes/prod_short.md)] sisältää muutamia yritysten usein käyttämiä maksutapoja. Voit kuitenkin lisätä niitä tarvittavan määrän.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksutavat** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Vaihtoehtoisesti voit lisätä maksuehdot maksutapaan. Lisätietoja on ohjeaiheessa [Maksuehtojen määrittäminen](finance-payment-terms.md).  

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a>Maksutavan määrittely asiakkaalle tai toimittajalle

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakas** tai **Toimittaja** ja valitse sitten vastaava linkki.
2. Valitse **Maksutavan koodi** -kentässä menetelmä, jota käytetään oletusarvoisesti asiakkaalle tai toimittajalle.

## <a name="see-also"></a>Katso myös

[Uusien asiakkaiden rekisteröiminen](sales-how-register-new-customers.md)  
[Maksuehtojen määrittäminen](finance-payment-terms.md)  
[Taloushallinto](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
