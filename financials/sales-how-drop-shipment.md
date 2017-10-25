---
title: Ostotilaukseen linkitetyn myyntitilauksen luominen suoratoimitusta varten | Microsoft Docs
description: "Tässä artikkelissa kerrotaan, miten ostotilaukseen linkitetty myyntitilaus luodaan. Näin toimitus voidaan tehdä suoraan toimittajalta asiakkaalle."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 990867cb428f860b1001177738d1a027f72485bc
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-make-drop-shipments"></a>Toimintaohje: Suoratoimitusten tekeminen
Suoratoimitus on nimikkeen toimitus yhdeltä toimittajistasi suoraan yhdelle asiakkaistasi.

Kun myyntitilaus merkitään suoratoimitusta varten, ja luot ostotilauksen, jossa asiakas määritetään **Tilausasiakkaan nro** -kentässä, voit linkittää nämä kaksi asiakirjaa ja ohjeistaa toimittajaa toimittamaan nimikkeet suoraan asiakkaalle.

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Myyntitilauksen luominen suoratoimitusta varten
Voit valmistella suoratoimituksen luomalla nimikkeelle normaalisti myyntitilauksen. Myyntirivillä tulee kuitenkin määrittää, että myynti vaatii suoratoimituksen.

1. Luo nimikkeelle myyntitilaus. Lisätietoja on kohdassa [Toimintaohje: Tuotteiden myyminen](sales-how-sell-products.md).
2. Valitse suoratoimituksen myyntitilauksen rivillä **Suoratoimitus**-valintaruutu. Käytä **Valitse sarakkeita** -toiminto, jos kenttä ei ole näkyvissä. Lisätietoja on ohjeaiheessa [Käyttäjän mukautus](ui-user-personalization.md).

> [!NOTE]  
>   Tämä toiminto edellyttää, että kokemukseksi on valittu **Suite**. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -kokemuksen mukauttaminen](ui-experiences.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>Ostotilauksen luominen suoratoimitukselle
Myytävän nimikkeen suoratoimitus valmistellaan luomalla ostotilaus normaalisti lukuun ottamatta sitä, että ostotilauksessa on määritettävä, että nimikkeet on toimitettava asiakkaalle, ei ostotilauksen tekijälle.

1. Luo ostotilaus. Älä täytä riveillä olevia kenttiä. Lisätietoja on kohdassa [Toimintaohje: Ostojen kirjaaminen](purchasing-how-record-purchases.md).
2. Valitse **Tilausasiakkaan nro** -kenttään asiakas, jolle myydään.
3. Valitse **Suoratoimitukset**-toiminto ja valitse sitten **Hae myyntitilaus** -toiminto.
4. Valitse **Myyntiluettelo**-ikkunassa myyntitilaus, jota valmisteltiin "Myyntitilauksen luominen suoratoimitusta varten" -osassa.
5. Valitse **OK**-painike.

Myyntitilauksen rivin tiedot lisätään ostotilauksen riville/riveille.

Voit ohjeistaa toimittajaa toimittamaan nimikkeet asiakkaalle esimerkiksi lähettämällä ostotilauksen PDF-tiedostona.     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>Myyntitilauksesta linkitetyn ostotilauksen tarkasteleminen
* Valitse suoratoimituksen myyntitilauksen rivi ja valitse sitten **Tilaa**-toiminto. Valitse **Suoratoimitus**-toiminto ja valitse sitten **Ostotilaus**-toiminto.

## <a name="to-post-a-drop-shipment"></a>Kirjaa suoratoimitus
Kun toimittaja toimittaa nimikkeet, voit kirjata myyntitilauksen toimitetuksi. Voit kirjata myös ostotilauksen, mutta vain **Vastaanotto**-vaihtoehdon kanssa niin kauan, kunnes myyntitilaus on laskutettu.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa "Myyntitilauksen luominen suoratoimitukselle" -osassa luomasi myyntitilaus.
3. Määritä **Toimitettava määrä** -kentässä toimitettava tilausmäärä, joka voi olla koko tai osittainen tilausmäärä.
4. Valitse **Kirjaa**- tai **Kirjaa ja lähetä** -toiminto.
5. Valitse **Toimitus**-vaihtoehto, kun haluat laskuttaa myöhemmin, tai **Toimitus ja lasku** -vaihtoehto, kun haluat laskuttaa heti.

## <a name="see-also"></a>Katso myös
[Toimintaohje: Erikoistilausten luominen](sales-how-to-create-special-orders.md)|  
[Toimintaohje: Tuotteiden myyminen](sales-how-sell-products.md)  
[Toimintaohje: Ostojen kirjaus](purchasing-how-record-purchases.md)  
[Myynti](sales-manage-sales.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

