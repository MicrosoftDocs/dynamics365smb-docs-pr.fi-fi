---
title: Pankkitilien määrittäminen| Microsoft Docs
description: Voit täsmäyttää pankkitilit pankin tiliotteiden avulla.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 27e3dd32fc1bf79dffdf1b7f33d1ea86a3f598e3
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307631"
---
# <a name="set-up-bank-accounts"></a>Pankkitilien määrittäminen
[!INCLUDE[d365fin](includes/d365fin_md.md)] seuraa pankkitapahtumia pankkitilien avulla. Tilit voidaan määrittää käyttämään paikallista valuuttaa tai ulkomaan valuuttaa. Kun olet määrittänyt pankkitilit, voit myös käyttää Sekin tulostus -vaihtoehtoa.

## <a name="to-set-up-bank-accounts"></a>Pankkitilien määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten liittyvä linkki.
2. Valitse **Pankkitilit**-sivulla **Uusi**-toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Voit täyttää **Saldo**-kenttään alkusaldo, kun pankkitilitapahtuma ja kyseinen summa on kirjattu. Voit tehdä tämän suorittamalla pankkitilin täsmäytyksen. Lisätietoja on kohdassa [Pankkitilien täsmäyttäminen erikseen](bank-how-reconcile-bank-accounts-separately.md). Vaihtoehtoisesti voit ottaa käyttöön alkusaldon osana yleistietojen luontia uusissa yrityksissä käyttämällä ohjattua **Siirrä yritystiedot** -asetusten määritystä. Lisätietoja on kohdassa [Käytön aloittaminen](product-get-started.md).

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Pankkitilin määrittäminen pankkitiedostojen tuontia tai vientiä varten
**Pankkitilin kortti** -sivun **Siirto**-pikavälilehden kentät liittyvät pankkisyötteiden ja -tiedostojen tuontiin ja vientiin. Lisätietoja on kohdissa [Pankkitietojen muuntopalvelun määrittäminen](bank-how-setup-bank-data-conversion-service.md) ja [Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten liittyvä linkki.
2. Avaa sen pankkitilin kortti, josta viet tai johon tuot pankkitiedostot.
3. Täytä **Siirto**-pikavälilehdessä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Eri tiedostojen vientipalvelut ja niiden tiedostomuodot edellyttävät erilaisia asetuksia **Pankkitilin kortti** -sivulla. Saat ilmoituksen virheellisistä tai puuttuvista asetusarvoista, kun yrität viedä tiedoston. Lue huolellisesti kenttien lyhyet kuvaukset tai katso lisätietoja liittyvien toimenpiteiden ohjeaiheista. Esimerkiksi maksutiedoston vienti pohjoisamerikkalaiseen sähköiseen rahansiirtoon (EFT-toiminto) edellyttää, että sekä **Viimeinen maksuosoitusehdotusnumero**- että **Siirtonro**-kenttä on täytetty. Lisätietoja on kohdassa [Maksujen vieminen pankkitiedostoon](payables-how-export-payments-bank-file.md).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Toimittajan pankkitilien määrittäminen pankkitiedostojen vientiä varten
**Toimittajan pankkitilin kortti** -sivun **Siirto**-pikavälilehden kentät liittyvät pankkisyötteiden ja -tiedostojen vientiin. Lisätietoja on kohdissa [Pankkitietojen muuntopalvelun määrittäminen](bank-how-setup-bank-data-conversion-service.md) ja [Maksujen vienti pankkitiedostoon](payables-how-export-payments-bank-file.md).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajat** ja valitse sitten liittyvä linkki.
2. Avaa sen toimittajan kortti, jonka pankkitiliin viet maksujen pankkitiedostot.
3. Valitse **Pankkitilit**-toiminto.
3. Täytä tarvittaessa **Toimittajan pankkitilin kortti** -sivun **Siirto**-pikavälilehden kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Katso myös
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Kirjausryhmien määrittäminen](finance-posting-groups.md)  
[Pankkitilien hallinta](bank-manage-bank-accounts.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
