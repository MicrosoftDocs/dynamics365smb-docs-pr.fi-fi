---
title: "Pankkitilien määrittäminen| Microsoft Docs"
description: "Voit täsmäyttää pankkitilit Financialsissa pankin tiliotteiden avulla."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: f46e95e24ef39a93bc93cfda1b9c575b07273566
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-bank-accounts"></a>Toimittajan pankkitilien määrittäminen
[!INCLUDE[d365fin](includes/d365fin_md.md)] seuraa pankkitapahtumia pankkitilien avulla. Tilit voidaan määrittää käyttämään paikallista valuuttaa tai ulkomaan valuuttaa. Kun olet määrittänyt pankkitilit, voit myös käyttää Sekin tulostus -vaihtoehtoa.

## <a name="to-set-up-bank-accounts"></a>Pankkitilien määrittäminen
1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Pankkitilit** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Pankkitilit**-ikkunassa **Uusi**-toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Pankkitilin määrittäminen pankkitiedostojen tuontia tai vientiä varten
**Pankkitilin kortti** -ikkunan **Siirto**-pikavälilehden kentät liittyvät pankkisyötteiden ja -tiedostojen tuontiin ja vientiin. Lisätietoja on kohdassa [Toimintaohje: Pankkitietojen muuntopalvelun määrittäminen](bank-how-setup-bank-data-conversion-service.md) ja [Toimintaohje: Envestnet Yodlee -pankkisyötepalvelun määrittäminen](bank-how-setup-bank-statement-service.md).

1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Pankkitilit** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa sen pankkitilin kortti, josta viet tai johon tuot pankkitiedostot.
3. Täytä **Siirto**-pikavälilehdessä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Eri tiedostojen vientipalvelut ja niiden tiedostomuodot edellyttävät erilaisia asetuksia **Pankkitilin kortti** -ikkunassa. Saat ilmoituksen virheellisistä tai puuttuvista asetusarvoista, kun yrität viedä tiedoston. Lue huolellisesti kenttien lyhyet kuvaukset tai katso lisätietoja liittyvien toimenpiteiden ohjeaiheista. Esimerkiksi maksutiedoston vienti pohjoisamerikkalaiseen sähköiseen rahansiirtoon (EFT-toiminto) edellyttää, että sekä **Viimeinen maksuosoitusehdotusnumero**- että **Siirtonro**-kenttä on täytetty. Lisätietoja on kohdassa [Toimintaohje: Maksujen vieminen pankkitiedostoon](payables-how-export-payments-bank-file.md).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Toimittajan pankkitilien määrittäminen pankkitiedostojen vientiä varten
**Toimittajan pankkitilin kortti** -ikkunan **Siirto**-pikavälilehden kentät liittyvät pankkisyötteiden ja -tiedostojen vientiin. Lisätietoja on kohdassa [Toimintaohje: Pankkitietojen muuntopalvelun määrittäminen](bank-how-setup-bank-data-conversion-service.md) ja [Toimintaohje: Maksujen vienti pankkitiedostoon](payables-how-export-payments-bank-file.md).

1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Toimittajat** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa sen toimittajan kortti, jonka pankkitiliin viet maksujen pankkitiedostot.
3. Valitse **Pankkitilit**-toiminto.
3. Täytä tarvittaessa **Toimittajan pankkitilin kortti** -ikkunan **Siirto**-pikavälilehden kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Katso myös
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Pankkitilien hallinta](bank-manage-bank-accounts.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

