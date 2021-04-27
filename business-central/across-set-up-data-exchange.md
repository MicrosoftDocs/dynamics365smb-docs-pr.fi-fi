---
title: Tiedonsiirron määrittäminen | Microsoft Docs
description: Määritä Business Centralin tiedonsiirtokehys.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 70672fcab8c2614de58bd152288ba3543fe6955a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787080"
---
# <a name="setting-up-data-exchange"></a>Tiedonsiirron määrittäminen
Ennen kuin voit lähettää ja vastaanottaa sähköisiä asiakirjoja tai tuoda ja viedä pankkitiedostoja, sinun on määritettävä tiedonsiirtokehys tiedostojen käsittelemistä varten. Lisäksi sinun on määritettävä liittyvät alueet, kuten asiakkaat, joille lähetät sähköiset laskut, tai AMC Banking 365 Fundamentals -laajennuksen, jos käytät pankkitiedostojen muuntamiseen ulkoista palveluntarjoajaa. Lisätietoja on kohdassa [Sähköinen tiedonsiirto](across-data-exchange.md).  

 Kun [!INCLUDE[prod_short](includes/prod_short.md)] on määritetty vaihtamaan tietoja ulkoisten tiedostojen kanssa, käyttäjät voivat käyttää määritystä yleisissä liiketoimintatehtävissä, kuten sähköisten asiakirjojen lähettämisessä ja vastaanottamisessa sekä pankkitiedostojen tuonnissa ja viennissä.  

 Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.  

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Määritä valmiiksi määritetty document exchange -palvelu sallimaan lähettää ja vastaanottaa sähköisiä asiakirjoja [!INCLUDE[prod_short](includes/prod_short.md)]:n kanssa.|[Document Exchange -palvelun määrittäminen](across-how-to-set-up-a-document-exchange-service.md)|  
|Määritä valmiiksi määritetty OCR-palvelu muuntamaan PDF- tai kuvatiedostot sähköisiksi asiakirjoiksi, jotka voidaan muuntaa [!INCLUDE[prod_short](includes/prod_short.md)]in tiedoston tietueiksi.|[Saapuvien asiakirjojen määrittäminen](across-how-setup-income-documents.md)|  
|Määritä yksi tai kaksi esimääritettyä palvelua käyttämään päivitettyjä valuuttakursseja, jotta saat uusimmat valuutanvaihtokurssit järjestelmään **Valuutat**-sivulle.|[Valuutan vaihtokurssien päivittäminen](finance-how-update-currencies.md)|  
|Määritä joitakin perustietoja, kuten yrityksen tiedot, asiakkaat, toimittajat, nimikkeet ja mittayksiköt, jotka liittyvät tietojen yhdistämiseen [!INCLUDE[prod_short](includes/prod_short.md)]issa.|[Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Määritä pankkitili, myyjä ja maksuloki SEPA-tilisiirrolle.|[SEPA-hyvityksen siirron määrittäminen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#setting-up-sepa-credit-transfer)|  
|Valmistele pankkitilimuodot, maksutavat ja asiakkaan SEPA-suoraveloitussopimukset.|[Maksujen kerääminen SEPA-suoraveloitusperintänä.](finance-collect-payments-with-sepa-direct-debit.md)|  
|Määritä käyttäjätunnistus ja AMC Banking 365 Fundamentals -laajennuspalvelun URL-osoite, joka vaaditaan, jotta pankkitiedostot voidaan muuttaa pankkisi vaatimaan muotoon.|[AMC Banking 365 Fundamentals -laajennuksen käyttäminen](ui-extensions-amc-banking.md)|  
|Määritä ja ota käyttöön ulkoinen palvelu, jonka avulla voit tuoda pankin tiliotteet suoraan pankkisyötteinä.|[Pankin tiliotepalvelun määrittäminen](bank-how-setup-bank-statement-service.md)|  
|Kun tiliotepalvelu on otettu käyttöön, linkitä pankkitilit [!INCLUDE[prod_short](includes/prod_short.md)]issa.|[Pankkitilien määrittäminen](bank-how-setup-bank-accounts.md)|  
|Valmistele datatiedoston tai tietovirran uuden tietojenvaihtomäärityksen luonti käyttämällä tiedoston XML-rakennetta. Se esitäyttää **Sarakkeen määritykset** -pikalomakkeen **Kirjauksen tiedonsiirtomääritykset** -sivulla.|[XML-mallien käyttäminen tietojenvaihtomääritysten valmisteluun](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Määritä tietojen vaihtokehys, jotta käyttäjät voivat vastaanottaa ja lähettää tietoja uudessa ostoasiakirjamuodossa, tuoda uuden pankkitiedoston tai vaihtaa muita tietoja.|[Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md)|  

## <a name="see-also"></a>Katso myös  
[Sähköinen tiedonsiirto](across-data-exchange.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]