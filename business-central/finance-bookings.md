---
title: Varausten laskuttaminen Business Central -sovelluksessa | Microsoft Docs
description: "Lisätietoja Microsoft Bookingsista tehtävästä massalaskutuksesta Business Central -sovelluksessa."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 01/07/2019
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: a98027c3ef3171491f84197897f93cbed4e288c2
ms.openlocfilehash: 65542f3855eff3a5ed117bff3247adbf05def6e2
ms.contentlocale: fi-fi
ms.lasthandoff: 01/07/2019

---
# <a name="bulk-invoicing-for-microsoft-bookings-in-included365finincludesd365finmdmd"></a>Microsoft Bookingsin massalaskutus [!INCLUDE[d365fin](includes/d365fin_md.md)]issa
Voit käyttää tapaamisten massalaskutusta, jos yrityksesi käyttää Office 365:n Bookings-sovellusta. [!INCLUDE[d365fin](includes/d365fin_md.md)]in **Laskuttamattomat varaukset** -sivulla esitetään luettelo yrityksen valmiista varauksista. Tällä sivulla voit valita nopeasti tapaamiset, jotka haluat laskuttaa ja joille haluat luoda luonnoslaskut tarjotuista palveluista.  

## <a name="connect-to-bookings"></a>Yhdistäminen Bookings-sovellukseen
Jos haluat yhdistää oman [!INCLUDE[d365fin](includes/d365fin_md.md)]in Bookingsiin, sinun on määritettävä Bookings-yritys, Bookingsiin synkronoitavat tiedot, synkronointiväli ja käytettävät mallit. Voit määrittää nämä tiedot **Bookings-synkronoinnin asetukset** -sivulla, jonka voit avata **Exchangen synkronointiasetukset** -sivulta, jonka löydät [Hakutoiminnon](ui-search.md) avulla.  

Jos esimerkiksi haluat synkronoida asiakkaat Bookingsin ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in välillä, sinun on määritettävä oletusmalli, jota käytetään uusien asiakkaiden lisäämiseen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin Bookings-yrityksesi asiakkaiden perusteella.  

> [!NOTE]
> Bookings-sovellus on suunniteltu yksittäisten asiakkaiden eikä yritysten tapaamisten varaamiseen. Synkronointi [!INCLUDE[d365fin](includes/d365fin_md.md)]in kanssa synkronoikin tämän vuoksi vain asiakaskontaktit, joiden tyyppi on Henkilö. Kontaktin synkronointia varten tarvitaan sähköpostiosoite.  

Jos vastaavasti haluat synkronoida palvelunimikkeet Bookingsin ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in välillä, sinun on määritettävä oletusmalli, jota käytetään uusien palvelunimikkeiden lisäämiseen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin Bookings-yrityksen palvelujen perusteella.  

> [!NOTE]
> Vain *Palvelu*-tyyppiset nimikkeet synkronoidaan Bookingsin ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in välillä. **Määritysmallit**-sivulla nimikkeen synkronointia varten määritetyn mallin tyypiksi on määritetty *Palvelu*.

## <a name="invoice-appointments"></a>Laskuta tapaamiset
Kun on aika lähettää laskut valmiista varauksista, voit siirtyä **Laskuttamattomat varaukset** -sivulle. Luettelon pituus riippuu tietojen synkronointiaikataulusta. Voit luoda laskut kaikille luettelon varauksille tai yhdelle varaukselle kerrallaan. Voit valita luettelosta useita tapahtumia ja laskuttaa ainoastaan ne.  

Bookings-tapaamisten laskuttamisen tuki on yksinkertaisempi kuin myyntitarjousten, -tilausten ja -laskujen kanssa työskentelyn täysi työnkulku. Lisätietoja on kohdassa [Myynnin laskutus](sales-how-invoice-sales.md). Voit myydä palveluitasi [!INCLUDE[d365fin](includes/d365fin_md.md)]in avulla tai käyttää Bookingsia, yrityksesi tarpeista riippuen.  

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[Myynnin laskutus](sales-how-invoice-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/en-us/business/scheduling-and-booking-app)  

