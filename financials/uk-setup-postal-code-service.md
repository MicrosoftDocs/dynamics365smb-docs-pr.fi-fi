---
title: "Toimintaohje: Ison-Britannian postinumeroiden GetAddress.io-laajennuksen määrittäminen | Microsoft Docs"
description: "Ohjeaiheessa kerrotaan yleisistä toiminnoista, joilla käsittelet tietoja Financialsissa. Kyse voi olla esimerkiksi arvojen antamisesta, tietojen lajittelusta ja näkymien vaihtamisesta."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: getaddress.io, postcodes, extension
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c5a99f7a90b2f832bba3eb088d0faa7514c14708
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-set-up-the-getaddressio-uk-postcodes-extension"></a>Toimintaohje: Ison-Britannian postinumeroiden GetAddress.io-laajennuksen määrittäminen
Laajennuksen avulla on helppo antaa isobritannialaisten objektien, kuten asiakkaiden, kontaktien, työntekijöiden, toimittajien ja pankkitilien, osoitteita. 

Ison-Britannian GetAddress.io-laajennus etsii isobritannialaisia postinumeroita getAddress-ohjelmistorajapinnan avulla. Jos haluat käyttää laajennusta, tarvitset tilauksen ja getAddress-ohjelmistorajapinnan API-avaimen. Niiden saaminen on helppoa ja autamme sinua niiden hankkimisessa, kun määrität Ison-Britannian postiosoitteiden GetAddress.io-laajennuksen. Tilaukset perustuvat käyttöön tai kutsuihin, niin kuin niihin joskus viitataan. Kutsu tapahtuu tässä tapauksessa, kun [!INCLUDE[d365fin](includes/d365fin_md.md)] näyttää postinumeron osoitteiden luettelon. Valitse tarpeitasi parhaiten vastaava tilaus sen mukaan, kuinka usein lisäät osoitteita. Jos valitsit sivulla vain **Hae API-avain** -kohdan, käytät **maksutonta** tilausta, joka sallii 20 osoitteen lisäämisen päivässä ja joka on voimassa 30 päivää. 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a>Ison-Britannian postinumeroiden GetAddress.io-laajennuksen määrittäminen 
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Palvelun yhteydet** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Palvelun yhteydet** -ikkunassa **Ison-Britannian postinumeropalvelu**.
3. Valitse **Postinumeropalvelun määritys** -sivulla **Poistettu käytöstä**.
4. Valitse **Postinumeropalvelun valinta** -ikkunassa **GetAddress.io**.
5. Valitse **GetAddress.io-määritys**-ikkunassa **Hae API-avain**, joka avaa **Tilaukset**-sivun getAddress-ohjelmointirajapinnan sivustossa.  

    > [!NOTE]  
>   Ponnahdusikkunoiden avaaminen on ehkä sallittava selaimessa.
6. Osta tilaus tai valitse pelkkä **Hae API-avain** ja anna sähköpostiosoitteesi.
7. Avaa getAddress.io-sähköposti ja kopioi API-avain. Avain on **API-avaimesi**-otsikon alla.
8. Liitä API-avain **GetAddress.io-määritys**-ikkunassa **API-avain**-kenttään ja valitse **OK**.
9. Tarkista **Palvelun yhteydet** -sivulla, että **Osoitepalvelu**-kentässä on **GetAddress.io**. Jos osoite on kentässä, palvelu on otettu käyttöön.

## <a name="see-also"></a>Katso myös
[Ison-Britannian postinumeroiden GetAddress.io](ui-extensions-getaddressio.md)
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
