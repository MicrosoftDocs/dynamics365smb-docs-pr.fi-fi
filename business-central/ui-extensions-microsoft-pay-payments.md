---
title: Microsoft Pay Standard| Microsoft Docs
description: Antaa tietoja Microsoft Pay -laajennuksesta
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a8811f6a05b380ce4e4b18b9caf28528a49b99d0
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386147"
---
# <a name="the-microsoft-pay-extension"></a>Microsoft Pay -laajennus

> [!IMPORTANT]
> Alkaen 8. helmikuuta 2020, Microsoft Pay -palvelun muutokset vaikuttavat Microsoft Pay -laajennukseen Microsoft [!INCLUDE[prod_short](includes/prod_long.md)]ssa. Muutosten vuoksi helmikuun 8. päivän jälkeen **Maksa nyt** -maksulinkit, joita Microsoft Pay -laajennus luo laskuille kohdassa [!INCLUDE[prod_short](includes/prod_short.md)], eivät avaa Microsoft Payta. Laajennusta käyttävien asiakkaiden on muutettava maksupalveluasetuksensa, jotta he voivat käyttää sen sijaan PayPal-laajennusta.<br /></br>
>
> Tammikuun 8. päivästä alkaen näytämme ilmoituksen kohteessa [!INCLUDE[prod_short](includes/prod_short.md)]. Ilmoitus sisältää linkin asetuksiin, joita sinun on muutettava, ja lisätietoja. Helmikuun 8. päivän jälkeen Microsoft Pay -laajennos ei ole enää saatavilla kohteessa [!INCLUDE[prod_short](includes/prod_short.md)].<br /></br>
>
> Muutokset vaikuttavat seuraaviin Business Centralin versioihin:
> - Microsoft Dynamics 365 Business Central lokakuu 2018
> - Microsoft Dynamics 365 Business Central huhtikuu 2019
> - Microsoft Dynamics 365 Business Central 2019 julkaisuaalto 2

Asiakkaat vaativat jatkuvasti yhä korkeatasoisempaa asiakaspalvelua sekä tuotteen laadun että toimituksen ja maksupalvelujen osalta. Voit parantaa asiakaspalvelun tasoa Microsoft Pay -palvelun avulla.

Microsoft Pay -laajennus lisää Microsoft Pay -linkin myyntiasiakirjoihin, joten asiakkaiden on helppo maksaa Microsoft Pay -palvelun avulla. Voit sitten voit lähettää asiakirjojat sähköpostitse, mikä parantaa asiakaspalvelua ja nopeuttaa asiakkaiden maksujen saapumista pankkitilille.

Microsoft Pay -laajennuksen edut:
- Asiakkaan maksut saapuvat nopeammin pankkitilille.
- asiakkailla on useita vaihtoehtoja maksaa laskut.
- Microsoft Pay on luotettava maksupalvelu, jota asiakkaat käyttävät mieluummin kuin antavat luottokorttitietonsa tuntemattomissa sivustoissa.
- Microsoft Payn avulla maksuja voi käsitellä useilla eri tavoilla. Niitä ovat esimerkiksi luottokorttikäsittely, kuten PayPal ja Stripe.
- Microsoft Pay -linkki voidaan upottaa jokaiseen lasku automaattisesti tai käyttäjä voi tehdä sen itse.
- Tämä toiminto on luotu laajennuksena, voit päättää itse, milloin se kannattaa ottaa käyttöön liiketoimintaprosesseissa tai kannattaako sen käyttö lainkaan.

Maksupalvelulaajennukset voi ottaa maksutta käyttöön [!INCLUDE[prod_short](includes/prod_short.md)]issa. Tiliä varten on kuitenkin otettava yhteys maksupalveluun. Lisätietoja on kohdassa [Asiakkaan maksujen ottaminen käyttöön maksupalvelujen kautta](sales-how-enable-payment-service-extensions.md).

## <a name="see-also"></a>Katso myös
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]