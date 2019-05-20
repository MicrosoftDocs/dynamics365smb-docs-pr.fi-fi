---
title: Maksujen täsmäytys Envestnet Yodlee Bank Feeds -palvelun laajennuksella | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan pankkitilit linkittävästä Envestnet Yodlee Bank Feeds -palvelun laajennuksesta, joka nopeuttaa maksujen täsmäyttämistä.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 53ee8bb7ee798c473e1053ea8413be28f9185d1b
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1248201"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a>Envestnet Yodlee Bank Feeds -palvelun laajennus
Envestnet Yodlee Bank Feeds -palvelun avulla voit täsmäyttää pankkitileille tehdyt maksut nopeasti linkittämällä järjestelmän pankkitilin verkkopankkitiliin. Tämä tarkoittaa sitä, että viimeisin tiliote syötetään automaattisesti tai manuaalisesti täsmäytyskirjauskansioon. Sen avulla varmistetaan, että käsittelet aina viimeisimpiä maksuja, sekä minimoidaan virheen mahdollisuus.

> [!NOTE]
> Tätä toimintoa tuetaan vain Business Centralin verkkoversiossa. Jos haluat käyttää tätä toimintoa paikallisesti, sinun on hankittava yhteistili Envestnet Yodleelta.

Envestnet Yodlee Bank Feeds -palvelu tarjoaa seuraavat edut:

* poistaa manuaalisyöttämisen tarpeen
* parantaa tehokkuutta ja tarkkuutta maksujen täsmäytyksen aikana
* tukee suuria määriä pankkeja
* tarjoaa pankkitapahtumien päivitetyt tiedot [!INCLUDE[d365fin](includes/d365fin_md.md)]issa
* tukee manuaalisia ja automaattisia pankkisyötteitä
* mahdollistaa maksujen täsmäytyksen ulkoistamisen kirjanpitäjälle, koska tiliotteet ovat käytettävissä.

Lisätietoja on kohdassa [Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md).

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)    
[Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
