---
title: Suoratoimitusten tekeminen (sisältää videon)
description: Tässä artikkelissa kerrotaan, miten ostotilaukseen linkitetty myyntitilaus luodaan. Näin toimitus voidaan tehdä suoraan toimittajalta asiakkaalle.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0ca22eaadb8ba4054ce22782881b487cab6bd5c4
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8521778"
---
# <a name="make-drop-shipments"></a>Suoratoimitusten tekeminen

Suoratoimitus on nimikkeen toimitus yhdeltä toimittajistasi suoraan yhdelle asiakkaistasi.

Kun myyntilaus on merkitty suoratoimitusta varten ja luot ostotilauksen, jossa asiakas määritetään **Toimitusasiakas**-kenttään, **Asiakkaan osoite**, voit linkittää kaksi asiakirjaa ja ohjata toimittajan lähettämään tilaus suoraan asiakkaalle.
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Myyntitilauksen luominen suoratoimitusta varten

Voit valmistella suoratoimituksen luomalla nimikkeelle myyntitilauksen. Myyntirivillä tulee määrittää, että myynti vaatii suoratoimituksen.

1. Luo nimikkeelle myyntitilaus. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).
2. Valitse suoratoimituksen myyntitilauksen rivillä **Suoratoimitus**-valintaruutu. Käytä **Valitse sarakkeita** -toiminto, jos kenttä ei ole näkyvissä. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>Ostotilauksen luominen suoratoimitukselle

Voit valmistella suoran toimituksen määrittämällä ostotilaukseen, että se täytyy toimittaa asiakkaalle, ei itsellesi.

1. Luo ostotilaus. Älä täytä riveillä olevia kenttiä. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).
2. Valitse **Toimitusasiakas**-kentässä **Asiakkaan osoite**.
3. Valitse **Asiakas**-kenttään asiakas, jolle myydään.
4. Valitse **Suoratoimitukset**-toiminto ja valitse sitten **Hae myyntitilaus** -toiminto.
5. Valitse **Myyntiluettelo**-sivulla myyntitilaus, jota valmisteltiin kohdassa [Myyntitilauksen luominen suoratoimitusta varten](#to-create-a-sales-order-for-drop-shipment).
6. Valitse **OK**-painike.

Myyntitilauksen rivin tiedot lisätään ostotilauksen riville/riveille.

Voit ohjeistaa toimittajaa toimittamaan nimikkeet asiakkaalle esimerkiksi lähettämällä ostotilauksen PDF-tiedostona. Jos toimittaja antaa seurantanumeron tai vastaavan tiedon, voit tallentaa kyseisen tiedon ostotilausriville tyyppiä *Kommentti*.  

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a>Useiden ostotilausten luominen suoratoimituksille

Voit myös käyttää hankintatyökirjaa luodaksesi ostotilauksen toimittajalle. Hankintatyökirjan käyttämisen etuna on se, että se voi luoda ostotilauksia kaikille avoimille suoratoimituksille, joten sinun ei tarvitse luoda jokaista erikseen.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hankintalistat** ja valitse sitten liittyvä linkki.
2. Valitse **Suoratoimitukset**-toiminto ja valitse sitten **Hae myyntitilaus** -toiminto.
3. Valitse **OK**-painike.
4. Tarkista ostotilausrivit ja valitse **Toimittajan nro** -kentässä toimittaja, joka toimittaa vaadittuja tavaroita. 
5. Valitse **Toteuta toimenpideviesti** -toiminto, jos haluat muuntaa tarkistetut rivit ostotilaukseksi.

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>Myyntitilauksesta linkitetyn ostotilauksen tarkasteleminen

* Valitse suoratoimituksen myyntitilauksen rivi ja valitse sitten **Tilaa**-toiminto. Valitse **Suoratoimitus**-toiminto ja valitse sitten **Ostotilaus**-toiminto.

## <a name="to-post-a-drop-shipment"></a>Kirjaa suoratoimitus

Kun toimittaja toimittaa nimikkeet, voit kirjata myyntitilauksen toimitetuksi. Voit kirjata myös ostotilauksen, mutta vain **Vastaanotto**-vaihtoehdon kanssa niin kauan, kunnes myyntitilaus on laskutettu.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.
2. Avaa myyntitilaus, joka luotiin kohdassa [Myyntitilauksen luominen suoratoimitukselle](#to-create-a-sales-order-for-drop-shipment).
3. Määritä **Toimitettava määrä** -kentässä toimitettava tilausmäärä, joka voi olla koko tai osittainen tilausmäärä.
4. Valitse **Kirjaa**- tai **Kirjaa ja lähetä** -toiminto.
5. Valitse **Toimitus**-vaihtoehto, kun haluat laskuttaa myöhemmin, tai **Toimitus ja lasku** -vaihtoehto, kun haluat laskuttaa heti.

## <a name="see-also"></a>Katso myös

[Erikoistilausten luominen](sales-how-to-create-special-orders.md)  
[Nimikkeiden ostaminen myyntiin](purchasing-how-purchase-products-sale.md)  
[Tuotteiden myyminen](sales-how-sell-products.md)  
[Ostojen kirjaus](purchasing-how-record-purchases.md)  
[Myynti](sales-manage-sales.md)  
[Varasto](inventory-manage-inventory.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]