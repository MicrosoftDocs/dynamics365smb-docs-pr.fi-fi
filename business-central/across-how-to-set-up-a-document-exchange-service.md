---
title: Document Exchange -palvelun määrittäminen | Microsoft Docs
description: Ulkoista palveluntarjoajaa käytetään sähköisten asiakirjojen vaihtamiseen liikekumppaneiden kanssa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 82ccc7bc9fc9aa09c9b403f9d5a31bfa25355e3e
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188226"
---
# <a name="set-up-a-document-exchange-service"></a>Document Exchange -palvelun määrittäminen
Ulkoista palveluntarjoajaa käytetään sähköisten asiakirjojen vaihtamiseen liikekumppaneiden kanssa. Lisätietoja on kohdassa [Sähköinen tiedonsiirto](across-data-exchange.md).  

## <a name="to-set-up-a-document-exchange-service"></a>Document Exchange -palvelun määrittäminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Document Exchange -palvelun asetukset** ja valitse sitten liittyvä linkki.  
2. Täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Käyttäjäagentti**|Anna teksti, jolla voidaan tunnistaa yrityksesi asiakirjan vaihtoprosesseissa.|  
    |**Document Exchange -palvelun vuokraajatunnus**|Anna vuokraaja document exchange -palvelussa, joka edustaa yritystäsi. Document exchange -palvelun tarjoaja tarjoaa tämän.|  
    |**Käytössä**|Määritä, onko palvelu käytössä. **Huomautus:** heti, kun palvelu otetaan käyttöön, ainakin kaksi työjonon tapahtumaa luodaan käsittelemään sähköisten asiakirjojen liikenne sisään ja ulos [!INCLUDE[d365fin](includes/d365fin_md.md)]:sta. Kun palvelu poistetaan käytöstä, työjonon tapahtumat poistetaan.|  
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
