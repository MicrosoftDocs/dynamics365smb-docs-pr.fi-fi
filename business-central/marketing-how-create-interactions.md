---
title: Vuorovaikutusten luominen kontakteille ja segmenteille| Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten vuorovaikutukset luodaan Business Central -sovelluksessa asiakkaiden ja segmenttien kanssa käydylle viestinnälle. Kyse voi olla esimerkiksi suoramainonnasta.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 5536671877c2fa766f953fe6bc9a5af5d2861b3e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387947"
---
# <a name="create-interactions-on-contacts-and-segments"></a>Vuorovaikutusten luominen kontakteille ja segmenteille
Voit luoda vuorovaikutuksia, kun haluat tallentaa kaikki vuorovaikutukset ja kaiken yhteydenpidon (esimerkiksi postin), joita sinulla on kontaktiesi ja segmenttiesi kanssa.

Ennen vuorovaikutusten luomista sinun täytyy määrittää vuorovaikutusmallit. Lisätietoja on ohjeaiheessa [Vuorovaikutusmallien määrittäminen](marketing-interactions.md).

## <a name="to-create-an-interaction"></a>Integroinnin luominen
1. Avaa kontakti-, myyjä- tai vuorovaikutuslokitapahtuma.
2. Valitse **Luo vuorovaikutus** -toiminto.
3. Täytä kentät ja valitse **OK**-painike.

> [!NOTE]  
>   Jos haluat suorittaa toisen tehtävän ennen vuorovaikutuksen suorittamista, valitse **Peruuta** ja valitse sitten yhteydenpidon suorittaminen myöhemmin. Tällöin vuorovaikutusta lykätään.

## <a name="to-finish-and-delete-postponed-interactions"></a>Lykättyjen vuorovaikutusten lopettaminen ja poistaminen
1. Avaa kontakti-, myyjä- tai vuorovaikutuslokitapahtuma.
2. Valitse **Lykätyt vuorovaikutukset**.
3. Valitse lopetettava vuorovaikutus ja valitse sitten **Jatka**-toiminto.

## <a name="to-create-an-interaction-on-a-segment"></a>Vuorovaikutusten luominen segmentille
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Segmentit** ja valitse sitten liittyvä linkki.
2. Määritä, minkä vuorovaikutuksen haluat liittää segmenttiin, täyttämällä **Segmentti**-sivulla **Vuorovaikutus**-osan kentät.

    Kun olet liittänyt vuorovaikutuksen segmenttiin, voit tehdä jokaisen segmentin kontaktin vuorovaikutuksesta yksilöllisen, esimerkiksi valitsemalla toisen vuorovaikutusmallin **Segmentti**-sivun riveillä.  
3. Voit kirjata segmentin ja vuorovaikutukset lokiin valitsemalla **Loki**-toiminnon. **Lokin segmentti** -sivu avautuu.
4. Jos haluat luoda uuden segmentin, joka sisältää samat kontaktit, valitse **Luo seurantasegmentti** -valintaruutu. Jotta ohjelma luo seurantasegmentin, segmenttien numerosarja on määritettävä **Kontaktienhallinnan asetukset** -sivulla.

Vuorovaikutus tallennetaan kullekin kontaktille **Vuorovaikutuslokitapahtuma**-taulukon segmentissä. Tämän jälkeen segmentti kirjataan lokiin. Lokiin kirjatut segmentit löytyvät **Lokiin kirjattu segmentti** -sivulta.

Jos olet valinnut **Luo seurantasegmentti** -valintaruudun, ohjelma luo automaattisesti uuden segmentin, jossa on samat kontaktit kuin juuri lokiin kirjaamassasi segmentissä.

## <a name="see-also"></a>Katso myös
[Vuorovaikutusten tallentaminen](marketing-interactions.md)  
[Kontaktien hallinta](marketing-contacts.md)  
[Myyntimahdollisuuksien hallinta](marketing-manage-sales-opportunities.md)  
[Business Centralin käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]