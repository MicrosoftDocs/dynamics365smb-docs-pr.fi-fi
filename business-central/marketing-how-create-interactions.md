---
title: Vuorovaikutusten luominen yhteyshenkilöille ja segmenteille
description: 'Tässä ohjeaiheessa kerrotaan, miten vuorovaikutukset luodaan Business Central -sovelluksessa asiakkaiden ja segmenttien kanssa käydylle viestinnälle.'
author: brentholtorf
ms.author: bholtorf
ms.topic: conceptual
ms.reviewer: bholtorf
ms.date: 12/13/2023
ms.custom: bap-template
ms.search.keywords: 'relationship, prospect'
ms.search.forms: '5077, 5078, 5074, 5076, 5186, 5075, 5079'
ms.service: dynamics-365-business-central
---
# <a name="create-interactions-on-contacts-and-segments"></a>Vuorovaikutusten luominen yhteyshenkilöille ja segmenteille

Voit luoda vuorovaikutuksia, joiden avulla voit seurata yhteydenpitoa, jota sinulla on yhden kontaktin kanssa tai jossa on useita kontakteja segmenteissäsi. Vuorovaikutusten luonnin helpottamiseksi [!INCLUDE [prod_short](includes/prod_short.md)] tarjoaa **Luo vuorovaikutus** -asetusten ohjatun määrityksen. Oppaasta on apua, kun halutaan tallentaa tärkeitä vuorovaikutustietoja.

Ennen vuorovaikutusten luomista sinun täytyy kuitenkin määrittää vuorovaikutusmallit. Lisätietoja vuorovaikutusmalleista on [Vuorovaikutusmallien määrittäminen](marketing-interactions.md) -kohdassa.

## <a name="to-create-an-interaction-with-a-contact"></a>Vuorovaikutuksen luominen yhteyshenkilön kanssa

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yhteyshenkilöt**, **Myyjä** tai **Vuorovaikutuslokitapahtuma** ja valitse liittyvä linkki.
2. Valitse **Luo vuorovaikutus** -toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Jos sinun täytyy lopettaa ennen vuorovaikutuksen päättymistä, voit valita **Peruuta** ja määrittää, haluatko tallentaa asetukset, jotta voit jatkaa myöhemmin. Jos haluat lisätietoja lykätyistä vuorovaikutuksista, siirry [Lykätyn vuorovaikutuksen viimeistely](#to-finish-setting-up-a-postponed-interaction) -kohtaan.

## <a name="to-create-an-interaction-on-a-segment"></a>Vuorovaikutusten luominen segmentille

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Segmentit** ja valitse sitten vastaava linkki.
2. Valitse **Luo vuorovaikutus** -toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Sen jälkeen kun olet liittänyt vuorovaikutuksen segmenttiin, **Segmentti**-sivulla on useita muita toimenpiteitä:
>
> * Mukauta jokaisen segmentin kontaktin vuorovaikutusta esimerkiksi valitsemalla riveillä toinen vuorovaikutusmalli.  
>* Kirjaa segmentti ja vuorovaikutukset lokiin valitsemalla **Loki**-toiminto, joka avaa **Lokin segmentti** -sivun.
> * Jos haluat luoda uuden segmentin, joka sisältää samat kontaktit, valitse **Luo seurantasegmentti** -valintaruutu. Tämä asetus edellyttää, että segmenteille on määritetty numerosarja **Kontaktienhallinnan asetukset** -sivulla.

Vuorovaikutus tallennetaan kullekin kontaktille **Vuorovaikutuslokitapahtuma**-taulukon segmentissä. Tämän jälkeen segmentti kirjataan lokiin. Lokiin kirjatut segmentit löytyvät **Lokiin kirjattu segmentti** -sivulta.

## <a name="to-finish-setting-up-a-postponed-interaction"></a>Lykätyn vuorovaikutuksen viimeistely

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Lykätyt vuorovaikutukset** ja valitse sitten vastaava linkki.
2. Valitse lopetettava vuorovaikutus ja valitse sitten **Jatka**-toiminto.

## <a name="see-also"></a>Katso myös

[Vuorovaikutusten tallentaminen](marketing-interactions.md)  
[Kontaktien hallinta](marketing-contacts.md)  
[Myyntimahdollisuuksien hallinta](marketing-manage-sales-opportunities.md)  
[Business Centralin käyttäminen](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
