---
title: Ostotarjouksen luominen tarjouksen pyytämistä varten
description: 'Ohjeaiheessa käsitellään, miten luodaan myyntitarjous- tai tarjouspyyntö kirjaamaan asiakkaalle tehty tarjous tuotteiden myynnistä tietyin ehdoin.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: rfq
ms.search.form: '49, 97, 9306, 9346'
ms.date: 03/14/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="request-quotes"></a>Tarjousten pyytäminen

Ostotarjousta voidaan käyttää ostotilauksen alustavana luonnoksena, joka voidaan muuttaa ostolaskuksi.

## <a name="create-a-purchase-quote"></a>Luo uusi ostotarjous

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotarjoukset**, valitse sitten vastaava linkki.
2. Luo uusi asiakirja samalla tavalla kuin tekisit ostotilauksen. Lisätietoja on kohdassa [Tietueiden ostot](purchasing-how-record-purchases.md).

## <a name="convert-a-purchase-quote-to-a-purchase-order"></a>Ostotarjousten muuttaminen ostotilauksiksi

Kun olet hyväksynyt toimittajan tarjouksen, voit käsitellä oston muuntamalla tarjouksen tilaukseksi.

1. Avaa ostotarjous, jonka haluat muuntaa ja valitse sitten **Tee tilaus** -toiminto.

Ostotarjous poistetaan tietokannasta. Ostotarjouksen tietojen perusteella luodaan ostotilaus, jonka avulla voit käsitellä oston ja kirjata ostolaskun. Ostotilauksen että ostolaskun **Tarjouksen nro** -kentässä näet ostotarjouksen numeron, josta ne on tehty.

> [!NOTE]
> Ostotarjousta ei voi muuntaa suoraan ostolaskuksi, kuten myyntitarjouksissa on mahdollista. Lisätietoja ostolaskun luomisesta on kohdassa [Kirjaa ostot ostolaskuilla](purchasing-how-record-purchases.md).

## <a name="see-also"></a>Katso myös

[Osto](purchasing-manage-purchasing.md)  
[Ostojen määrittäminen](purchasing-setup-purchasing.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
