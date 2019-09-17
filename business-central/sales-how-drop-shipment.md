---
title: Ostotilauksen linkittäminen myyntitilaukseen suoratoimitusta varten | Microsoft Docs
description: Tässä artikkelissa kerrotaan, miten ostotilaukseen linkitetty myyntitilaus luodaan. Näin toimitus voidaan tehdä suoraan toimittajalta asiakkaalle.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 09/06/2019
ms.author: sgroespe
ms.openlocfilehash: 9555aabe515757b71426ddca2f90b37e561f96e2
ms.sourcegitcommit: d3035c32bb79b51179540787b98579ac0c528cc4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/06/2019
ms.locfileid: "1985812"
---
# <a name="make-drop-shipments"></a>Suoratoimitusten tekeminen
Suoratoimitus on nimikkeen toimitus yhdeltä toimittajistasi suoraan yhdelle asiakkaistasi.

Kun myyntilaus on merkitty suoratoimitusta varten ja luot ostotilauksen, jossa asiakas määritetään **Toimitusasiakas**-kenttään, **Asiakkaan osoite**, voit linkittää kaksi asiakirjaa ja ohjata toimittajan lähettämään tilaus suoraan asiakkaalle.

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Myyntitilauksen luominen suoratoimitusta varten
Voit valmistella suoratoimituksen luomalla nimikkeelle normaalisti myyntitilauksen. Myyntirivillä tulee kuitenkin määrittää, että myynti vaatii suoratoimituksen.

1. Luo nimikkeelle myyntitilaus. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).
2. Valitse suoratoimituksen myyntitilauksen rivillä **Suoratoimitus**-valintaruutu. Käytä **Valitse sarakkeita** -toiminto, jos kenttä ei ole näkyvissä. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>Ostotilauksen luominen suoratoimitukselle
Myytävän nimikkeen suoratoimitus valmistellaan luomalla ostotilaus normaalisti lukuun ottamatta sitä, että ostotilauksessa on määritettävä, että nimikkeet on toimitettava asiakkaalle, ei ostotilauksen tekijälle.

1. Luo ostotilaus. Älä täytä riveillä olevia kenttiä. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).
2. Valitse **Toimitusasiakas**-kentässä **Asiakkaan osoite**.
3. Valitse **Asiakas**-kenttään asiakas, jolle myydään.
3. Valitse **Suoratoimitukset**-toiminto ja valitse sitten **Hae myyntitilaus** -toiminto.
4. Valitse **Myyntiluettelo**-sivulla myyntitilaus, jota valmisteltiin kohdassa [Myyntitilauksen luominen suoratoimitusta varten](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).
5. Valitse **OK**-painike.

Myyntitilauksen rivin tiedot lisätään ostotilauksen riville/riveille.

Voit ohjeistaa toimittajaa toimittamaan nimikkeet asiakkaalle esimerkiksi lähettämällä ostotilauksen PDF-tiedostona.     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>Myyntitilauksesta linkitetyn ostotilauksen tarkasteleminen
* Valitse suoratoimituksen myyntitilauksen rivi ja valitse sitten **Tilaa**-toiminto. Valitse **Suoratoimitus**-toiminto ja valitse sitten **Ostotilaus**-toiminto.

## <a name="to-post-a-drop-shipment"></a>Kirjaa suoratoimitus
Kun toimittaja toimittaa nimikkeet, voit kirjata myyntitilauksen toimitetuksi. Voit kirjata myös ostotilauksen, mutta vain **Vastaanotto**-vaihtoehdon kanssa niin kauan, kunnes myyntitilaus on laskutettu.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Myyntitilaukset** ja valitse sitten liittyvä linkki.
2. Avaa kohdassa [Myyntitilauksen luominen suoratoimitukselle]() luomasi myyntitilaus.
3. Määritä **Toimitettava määrä** -kentässä toimitettava tilausmäärä, joka voi olla koko tai osittainen tilausmäärä.
4. Valitse **Kirjaa**- tai **Kirjaa ja lähetä** -toiminto.
5. Valitse **Toimitus**-vaihtoehto, kun haluat laskuttaa myöhemmin, tai **Toimitus ja lasku** -vaihtoehto, kun haluat laskuttaa heti.

## <a name="see-also"></a>Katso myös
[Erikoistilausten luominen](sales-how-to-create-special-orders.md)  
[Nimikkeiden ostaminen myyntiin](purchasing-how-purchase-products-sale.md)  
[Tuotteiden myyminen](sales-how-sell-products.md)  
[Ostojen kirjaus](purchasing-how-record-purchases.md)  
[Myynti](sales-manage-sales.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
