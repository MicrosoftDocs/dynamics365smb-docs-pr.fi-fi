---
title: Vuorovaikutusten luominen kontakteille ja segmenteille| Microsoft Docs
description: "Tässä ohjeaiheessa kerrotaan, miten vuorovaikutukset luodaan Finance and Operations, Business editionissa asiakkaiden ja segmenttien kanssa käydylle viestinnälle. Kyse voi olla esimerkiksi suoramainonnasta."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/15/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 61ee0eaccea5bfb3511537d825b2a0cb8948dee8
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

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
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Segmentit** ja valita sitten aiheeseen liittyvän linkin.
2. Määritä, minkä vuorovaikutuksen haluat liittää segmenttiin, täyttämällä **Segmentti**-ikkunassa **Vuorovaikutus**-osan kentät.

    Kun olet liittänyt vuorovaikutuksen segmenttiin, voit tehdä jokaisen segmentin kontaktin vuorovaikutuksesta yksilöllisen, esimerkiksi valitsemalla toisen vuorovaikutusmallin **Segmentti**-ikkunan riveillä.  
3. Voit kirjata segmentin ja vuorovaikutukset lokiin valitsemalla **Loki**-toiminnon. **Lokin segmentti**-luetteloikkuna aukeaa.
4. Jos haluat luoda uuden segmentin, joka sisältää samat kontaktit, valitse **Luo seurantasegmentti** -valintaruutu. Jotta ohjelma luo seurantasegmentin, segmenttien numerosarja on määritettävä **Kontaktienhallinnan asetukset** -ikkunassa.

Vuorovaikutus tallennetaan kullekin kontaktille **Vuorovaikutuslokitapahtuma**-taulukon segmentissä. Tämän jälkeen segmentti kirjataan lokiin. Lokiin kirjatut segmentit löytyvät **Lokiin kirjattu segmentti** -ikkunasta.

Jos olet valinnut **Luo seurantasegmentti** -valintaruudun, ohjelma luo automaattisesti uuden segmentin, jossa on samat kontaktit kuin juuri lokiin kirjaamassasi segmentissä.

## <a name="see-also"></a>Katso myös
[Vuorovaikutusten tallentaminen](marketing-interactions.md)  
[Kontaktien hallinta](marketing-contacts.md)  
[Myyntimahdollisuuksien hallinta](marketing-manage-sales-opportunities.md)  
[Kontaktienhallinnan määrittäminen](marketing-setup-marketing.md)  
[Finance and Operations, Business editionin käyttäminen](ui-work-product.md)

