---
title: "Ison-Britannian postinumeroiden GetAddress.io-laajennuksen määrittäminen| Microsoft Docs"
description: "Artikkelissa käsitellään, miten postinumeropalvelu asennetaan ja määritetään tuomaan isobritannialaisia osoitteita"
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/16/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 29b3b551e3ea8e8dfd52a3846332eec47f9346ce
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="set-up-the-getaddressio-uk-postcodes-extension"></a>Ison-Britannian postinumeroiden GetAddress.io-laajennuksen määrittäminen
Laajennuksen avulla on helppo antaa isobritannialaisten objektien, kuten asiakkaiden, kontaktien, työntekijöiden, toimittajien ja pankkitilien, osoitteita. 

Ison-Britannian GetAddress.io-laajennus etsii isobritannialaisia postinumeroita getAddress-ohjelmistorajapinnan avulla. Jos haluat käyttää laajennusta, tarvitset tilauksen ja getAddress-ohjelmistorajapinnan API-avaimen. Niiden saaminen on helppoa ja autamme sinua niiden hankkimisessa, kun määrität Ison-Britannian postiosoitteiden GetAddress.io-laajennuksen. Tilaukset perustuvat käyttöön tai kutsuihin, niin kuin niihin joskus viitataan. Kutsu tapahtuu tässä tapauksessa, kun [!INCLUDE[d365fin](includes/d365fin_md.md)] näyttää postinumeron osoitteiden luettelon. Valitse tarpeitasi parhaiten vastaava tilaus sen mukaan, kuinka usein lisäät osoitteita. Jos valitsit sivulla vain **Hae API-avain** -kohdan, käytät **maksutonta** tilausta, joka sallii 20 osoitteen lisäämisen päivässä ja joka on voimassa 30 päivää. 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a>Ison-Britannian postinumeroiden GetAddress.io-laajennuksen määrittäminen 
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Palvelun yhteydet** ja valitse sitten liittyvä linkki.  
2. Valitse **Palvelun yhteydet** -ikkunassa **Ison-Britannian postinumeropalvelu**.
3. Valitse **Postinumeropalvelun määritys** -sivulla **Poistettu käytöstä**.
4. Valitse **Postinumeropalvelun valinta** -ikkunassa **GetAddress.io**.
5. Valitse **GetAddress.io-määritys**-ikkunassa **Hae API-avain**, joka avaa **Tilaukset**-sivun getAddress-ohjelmointirajapinnan sivustossa.  

    **Huomautus**: Ponnahdusikkunoiden avaaminen on ehkä sallittava selaimessa.
6. Osta tilaus tai valitse pelkkä **Hae API-avain** ja anna sähköpostiosoitteesi.
7. Avaa getAddress.io-sähköposti ja kopioi API-avain. Avain on **API-avaimesi**-otsikon alla.
8. Liitä API-avain **GetAddress.io-määritys**-ikkunassa **API-avain**-kenttään ja valitse **OK**.
9. Tarkista **Palvelun yhteydet** -sivulla, että **Osoitepalvelu**-kentässä on **GetAddress.io**. Jos osoite on kentässä, palvelu on otettu käyttöön.

## <a name="see-also"></a>Katso myös
[Ison-Britannian postinumerot GetAddress.io](ui-extensions-getaddressio.md) [[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennuksilla](ui-extensions.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)
