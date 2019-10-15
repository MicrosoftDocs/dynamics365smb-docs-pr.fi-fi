---
title: Maksujen täsmäytys Envestnet Yodlee Bank Feeds -laajennuksella | Microsoft Docs
description: Tässä ohjeaiheessa käsitellään pankkitilit linkittävästä Envestnet Yodlee Bank Feeds -laajennuksesta, joka nopeuttaa maksujen täsmäyttämistä.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: d79ef7c076ec3a529aeb0c679b8b61658ef65af5
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315346"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a>Envestnet Yodlee Bank Feeds -laajennus
Envestnet Yodlee Bank Feeds -palvelun avulla voit täsmäyttää pankkitileille tehdyt maksut nopeasti linkittämällä järjestelmän pankkitilin verkkopankkitiliin. Tämä tarkoittaa sitä, että viimeisin tiliote syötetään automaattisesti tai manuaalisesti täsmäytyskirjauskansioon. Sen avulla varmistetaan, että käsittelet aina viimeisimpiä maksuja, sekä minimoidaan virheen mahdollisuus.

Envestnet Yodlee Bank Feeds -palvelua tuetaan vain Yhdysvalloissa ja Kanadassa.

> [!NOTE]
> Tätä toimintoa tuetaan vain Business Centralin verkkoversiossa. Jos haluat käyttää tätä toimintoa paikallisesti, sinun on hankittava yhteistili Envestnet Yodleelta.<br /><br />

> [!IMPORTANT]
> Uuden eurooppalaisen maksupalveludirektiivin vuoksi (PSD2), 4.9.2019 jälkeen tiliotteita ei voi enää tuoda automaattisesti [!INCLUDE[d365fin](includes/d365fin_md.md)] brittiläisistä pankeista. Tutkimme mahdollisuutta ottaa tämä ominaisuus uudelleen käyttöön tulevaisuudessa.

Envestnet Yodlee Bank Feeds -palvelun edut:

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
