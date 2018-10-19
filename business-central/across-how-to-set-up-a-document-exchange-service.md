---
title: "Document Exchange -palvelun määrittäminen | Microsoft Docs"
description: "Ulkoista palveluntarjoajaa käytetään sähköisten asiakirjojen vaihtamiseen liikekumppaneiden kanssa."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: d785dfd1a9c3879fc0ddfc79c7c254adbc2ddb52
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

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

