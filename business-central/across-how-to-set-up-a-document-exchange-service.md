---
title: Document Exchange -palvelun määrittäminen
description: Ulkoista palveluntarjoajaa käytetään sähköisten asiakirjojen vaihtamiseen liikekumppaneiden kanssa käyttämällä "Document Exchange -palvelun asetukset" -määritystä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 357c48c6b7ed8e2d44316805bba04ff9236f0e9b
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436296"
---
# <a name="set-up-a-document-exchange-service"></a>Document Exchange -palvelun määrittäminen
Ulkoista palveluntarjoajaa käytetään sähköisten asiakirjojen vaihtamiseen liikekumppaneiden kanssa. Lisätietoja on kohdassa [Sähköinen tiedonsiirto](across-data-exchange.md).  

## <a name="to-set-up-a-document-exchange-service"></a>Document Exchange -palvelun määrittäminen  
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Document Exchange -palvelun asetukset** ja valitse sitten vastaava linkki.  
2. Täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Käyttäjäagentti**|Anna teksti, jolla voidaan tunnistaa yrityksesi asiakirjan vaihtoprosesseissa.|  
    |**Document Exchange -palvelun vuokraajatunnus**|Anna vuokraaja document exchange -palvelussa, joka edustaa yritystäsi. Document exchange -palvelun tarjoaja tarjoaa tämän.|  
    |**Käytössä**|Määritä, onko palvelu käytössä. **Huomautus:** heti, kun palvelu otetaan käyttöön, ainakin kaksi työjonon tapahtumaa luodaan käsittelemään sähköisten asiakirjojen liikenne sisään ja ulos [!INCLUDE[prod_short](includes/prod_short.md)]:sta. Kun palvelu poistetaan käytöstä, työjonon tapahtumat poistetaan.|  
    |**Rekisteröinnin URL-osoite**|Määritä verkkosivu, jossa document exchange -palvelu rekisteröidään.|  
    |**Palvelun URL-osoite**|Määritä sen document exchange -palvelun osoite, joka kutsutaan, kun lähetät ja vastaanotat sähköisiä asiakirjoja.|  
    |**Sisäänkirjautumisen osoite**|Määritä document exchange -palvelun kirjautumissivu, johon kirjoitat yrityksesi käyttäjänimen ja salasanan kirjautuessasi palveluun.|  
    |**Kuluttajan avain**|Anna kolmen osapuolen OAuth-avain kuluttaja-avaimelle. Document exchange -palvelun tarjoaja tarjoaa tämän.|  
    |**Kuluttajan salainen avain**|Anna piilokoodi, joka suojaa kuluttaja-avainta. Saat sen Document exchange -palveluntarjoajalta.|  
    |**Tunnus**|Anna kolmen osapuolen OAuth-avain tunnukselle. Saat sen Document exchange -palveluntarjoajalta.|  
    |**Tunnuksen salainen avain**|Anna piilokoodi, joka suojaa tunnusta. Saat sen Document exchange -palveluntarjoajalta.|  

    > [!NOTE]  
    > Sisäänkirjaustiedot salataan automaattisesti.

## <a name="see-also"></a>Katso myös  
[Tiedonsiirron määrittäminen](across-set-up-data-exchange.md)  
[Sähköinen tiedonsiirto](across-data-exchange.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]