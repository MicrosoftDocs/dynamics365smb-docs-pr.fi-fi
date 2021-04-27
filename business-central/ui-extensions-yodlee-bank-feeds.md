---
title: Maksujen täsmäytys Envestnet Yodlee Bank Feeds -laajennuksella
description: Tässä ohjeaiheessa käsitellään pankkitilit linkittävästä Envestnet Yodlee Bank Feeds -laajennuksesta, joka nopeuttaa maksujen täsmäyttämistä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9bdbcc208429bba15e30bc56cc8a4477312c1cdd
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771233"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a>Envestnet Yodlee Bank Feeds -laajennus

Envestnet Yodlee Bank Feeds -palvelun avulla voit täsmäyttää pankkitileille tehdyt maksut nopeasti linkittämällä järjestelmän pankkitilin verkkopankkitiliin. Tämä tarkoittaa sitä, että viimeisin tiliote syötetään automaattisesti tai manuaalisesti täsmäytyskirjauskansioon. Sen avulla varmistetaan, että käsittelet aina viimeisimpiä maksuja, sekä minimoidaan virheen mahdollisuus.

Envestnet Yodlee Bank Feeds -palvelua tuetaan vain Yhdysvalloissa ja Kanadassa.

> [!NOTE]
> Envestnet Yodlee Bank Feeds -palvelua tuetaan vain Business Central -sovelluksen online-versiossa. Jos haluat käyttää tätä toimintoa paikallisesti, sinun on hankittava yhteistili Envestnet Yodleelta.<br /><br />
> Envestnet Yodlee Bank Feeds -palvelua tuetaan vain Yhdysvalloissa ja Kanadassa.
> Vain näissä maissa sijaitsevia pankkeja tuetaan, vaikka muiden maiden pankit voivat näkyä Envestnet Yodlee Bank Feeds -pankin valintaikkunassa [!INCLUDE[prod_short](includes/prod_short.md)]:ssa.

> [!IMPORTANT]
> Uuden eurooppalaisen maksupalveludirektiivin vuoksi (PSD2), 4.9.2019 jälkeen tiliotteita ei voi enää tuoda automaattisesti [!INCLUDE[prod_short](includes/prod_short.md)] brittiläisistä pankeista. Tutkimme mahdollisuutta ottaa tämä ominaisuus uudelleen käyttöön tulevaisuudessa.

Envestnet Yodlee Bank Feeds -palvelun edut:

* poistaa manuaalisyöttämisen tarpeen
* parantaa tehokkuutta ja tarkkuutta maksujen täsmäytyksen aikana
* tukee suuria määriä pankkeja
* tarjoaa pankkitapahtumien päivitetyt tiedot [!INCLUDE[prod_short](includes/prod_short.md)]issa
* tukee manuaalisia ja automaattisia pankkisyötteitä
* mahdollistaa maksujen täsmäytyksen ulkoistamisen kirjanpitäjälle, koska tiliotteet ovat käytettävissä.

## <a name="available-bank-feeds"></a>Käytettävissä olevat pankkisyötteet
Voit tarkistaa, tuetaanko pankkia määrittämällä ja muodostamalla yhteyden Envestnet Yodlee Bank Feeds -palveluun. Pankki näkyy luettelossa, jos sitä tukee Envestnet Yodlee.

Lisätietoja on kohdassa [Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md).

## <a name="see-also"></a>Katso myös
[[!INCLUDE[prod_short](includes/prod_short.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)    
[Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]