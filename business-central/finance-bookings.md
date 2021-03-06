---
title: Varausten laskuttaminen Business Central -sovelluksessa | Microsoft Docs
description: Lisätietoja Microsoft Bookingsista tehtävästä massalaskutuksesta Business Centralissa.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 06095fdb0fac291490eeef5a085264ea75581283
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5780855"
---
# <a name="bulk-invoicing-for-microsoft-bookings-in-prod_short"></a>Microsoft Bookingsin massalaskutus [!INCLUDE[prod_short](includes/prod_short.md)]issa
Voit tehdä tapaamisten massalaskutusta, jos yrityksesi käyttää Microsoft 365:n Bookings-sovellusta. [!INCLUDE[prod_short](includes/prod_short.md)]in **Laskuttamattomat varaukset** -sivulla esitetään luettelo yrityksen valmiista varauksista. Tällä sivulla voit valita nopeasti tapaamiset, jotka haluat laskuttaa ja joille haluat luoda luonnoslaskut tarjotuista palveluista.  

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