---
title: Varausten laskuttaminen Business Centralissa
description: Tässä ohjeaiheessa kerrotaan, miten joukkolaskutus voidaan suorittaa Microsoft Bookingsista Business Centralissa.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.search.form: 1638, 6702, 6704
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: c0abb4d4389dd3896f1aceedb42d51aca0e61000
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8139571"
---
# <a name="bulk-invoicing-for-microsoft-bookings-in-prod_short"></a>Microsoft Bookingsin massalaskutus [!INCLUDE[prod_short](includes/prod_short.md)]issa

Voit käyttää tapaamisten massalaskutusta, jos yrityksesi käyttää Microsoft 365:n Bookings-sovellusta. [!INCLUDE[prod_short](includes/prod_short.md)]in **Laskuttamattomat varaukset** -sivulla esitetään luettelo yrityksen valmiista varauksista. Tällä sivulla voit valita nopeasti tapaamiset, jotka haluat laskuttaa ja joille haluat luoda luonnoslaskut tarjotuista palveluista.  

## <a name="connect-to-bookings"></a>Yhdistäminen Bookings-sovellukseen

Jos haluat yhdistää oman [!INCLUDE[prod_short](includes/prod_short.md)]in Bookingsiin, sinun on määritettävä Bookings-yritys, Bookingsiin synkronoitavat tiedot, synkronointiväli ja käytettävät mallit. Voit määrittää nämä tiedot **Bookings-synkronoinnin asetukset** -sivulla, jonka voit avata **Exchangen synkronointiasetukset** -sivulta, jonka löydät [Hakutoiminnon](ui-search.md) avulla.  

Jos esimerkiksi haluat synkronoida asiakkaat Bookingsin ja [!INCLUDE[prod_short](includes/prod_short.md)]in välillä, sinun on määritettävä oletusmalli, jota käytetään uusien asiakkaiden lisäämiseen [!INCLUDE[prod_short](includes/prod_short.md)]iin Bookings-yrityksesi asiakkaiden perusteella.  

> [!NOTE]
> Bookings-sovellus on suunniteltu yksittäisten asiakkaiden eikä yritysten tapaamisten varaamiseen. Synkronointi [!INCLUDE[prod_short](includes/prod_short.md)]in kanssa synkronoikin tämän vuoksi vain asiakaskontaktit, joiden tyyppi on Henkilö. Kontaktin synkronointia varten tarvitaan sähköpostiosoite.  

Jos vastaavasti haluat synkronoida palvelunimikkeet Bookingsin ja [!INCLUDE[prod_short](includes/prod_short.md)]in välillä, sinun on määritettävä oletusmalli, jota käytetään uusien palvelunimikkeiden lisäämiseen [!INCLUDE[prod_short](includes/prod_short.md)]iin Bookings-yrityksen palvelujen perusteella.  

> [!NOTE]
> Vain *Palvelu*-tyyppiset nimikkeet synkronoidaan Bookingsin ja [!INCLUDE[prod_short](includes/prod_short.md)]in välillä. **Määritysmallit**-sivulla nimikkeen synkronointia varten määritetyn mallin tyypiksi on määritetty *Palvelu*.

## <a name="invoice-appointments"></a>Laskuta tapaamiset

Kun on aika lähettää laskut valmiista varauksista, voit siirtyä **Laskuttamattomat varaukset** -sivulle. Luettelon pituus riippuu tietojen synkronointiaikataulusta. Voit luoda laskut kaikille luettelon varauksille tai yhdelle varaukselle kerrallaan. Voit valita luettelosta useita tapahtumia ja laskuttaa ainoastaan ne.  

Bookings-tapaamisten laskuttamisen tuki on yksinkertaisempi kuin myyntitarjousten, -tilausten ja -laskujen kanssa työskentelyn täysi työnkulku. Lisätietoja on kohdassa [Myynnin laskutus](sales-how-invoice-sales.md). Voit myydä palveluitasi [!INCLUDE[prod_short](includes/prod_short.md)]in avulla tai käyttää Bookingsia, yrityksesi tarpeista riippuen.  

## <a name="see-also"></a>Katso myös

[Rahoitus](finance.md)  
[Myynnin laskutus](sales-how-invoice-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/business/scheduling-and-booking-app)  


[!INCLUDE[footer-include](includes/footer-banner.md)]