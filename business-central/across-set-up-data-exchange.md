---
title: Tiedonsiirron määrittäminen | Microsoft Docs
description: Määritä Business Centralin tiedonsiirtokehys.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: e0074d3e3a1869a8f377c6ff3d8faad97f781077
ms.sourcegitcommit: d0dc5e5c46b932899e2a9c7183959d0ff37738d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076633"
---
# <a name="setting-up-data-exchange"></a>Tiedonsiirron määrittäminen
Ennen kuin voit lähettää ja vastaanottaa sähköisiä asiakirjoja tai tuoda ja viedä pankkitiedostoja, sinun on määritettävä tiedonsiirtokehys tiedostojen käsittelemistä varten. Lisäksi sinun täytyy määrittää liittyvät alueet, kuten asiakkaat, joille lähetät sähköiset laskut tai AMC Banking 365 -perusteet, jos käytät pankkitiedostojen muuntamiseen ulkoista palveluntarjoajaa. Lisätietoja on kohdassa [Sähköinen tiedonsiirto](across-data-exchange.md).  

 Kun [!INCLUDE[d365fin](includes/d365fin_md.md)] on määritetty vaihtamaan tietoja ulkoisten tiedostojen kanssa, käyttäjät voivat käyttää määritystä yleisissä liiketoimintatehtävissä, kuten sähköisten asiakirjojen lähettämisessä ja vastaanottamisessa sekä pankkitiedostojen tuonnissa ja viennissä.  

 Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.  

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Määritä valmiiksi määritetty document exchange -palvelu sallimaan lähettää ja vastaanottaa sähköisiä asiakirjoja [!INCLUDE[d365fin](includes/d365fin_md.md)]:n kanssa.|[Document Exchange -palvelun määrittäminen](across-how-to-set-up-a-document-exchange-service.md)|  
|Määritä valmiiksi määritetty OCR-palvelu muuntamaan PDF- tai kuvatiedostot sähköisiksi asiakirjoiksi, jotka voidaan muuntaa [!INCLUDE[d365fin](includes/d365fin_md.md)]in tiedoston tietueiksi.|[Saapuvien asiakirjojen määrittäminen](across-how-setup-income-documents.md)|  
|Määritä yksi tai kaksi esimääritettyä palvelua käyttämään päivitettyjä valuuttakursseja, jotta saat uusimmat valuutanvaihtokurssit järjestelmään **Valuutat**-sivulle.|[Valuutan vaihtokurssien päivittäminen](finance-how-update-currencies.md)|  
|Määritä joitakin perustietoja, kuten yrityksen tiedot, asiakkaat, toimittajat, nimikkeet ja mittayksiköt, jotka liittyvät tietojen yhdistämiseen [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.|[Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Määritä pankkitili, myyjä ja maksuloki SEPA-tilisiirrolle.|[Määritä SEPA-tilisiirto](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#setting-up-sepa-credit-transfer)|  
|Valmistele pankkitilimuodot, maksutavat ja asiakkaan SEPA-suoraveloitussopimukset.|[Maksujen kerääminen SEPA-suoraveloitusperintänä](finance-collect-payments-with-sepa-direct-debit.md)|  
|Määritä käyttäjätunnistus ja AMC Banking 365 peruslaajennuksen tarjoajan URL, joka vaaditaan, jotta pankkitiedostot voidaan muuttaa pankkisi vaatimaan muotoon.|[AMC Banking 365 -perusteiden laajennuksen käyttäminen](ui-extensions-amc-banking.md)|  
|Määritä ja ota käyttöön ulkoinen palvelu, jonka avulla voit tuoda pankin tiliotteet suoraan pankkisyötteinä.|[Pankin tiliotepalvelun määrittäminen](bank-how-setup-bank-statement-service.md)|  
|Kun tiliotepalvelu on otettu käyttöön, linkitä pankkitilit [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.|[Pankkitilien määrittäminen](bank-how-setup-bank-accounts.md)|  
|Valmistele datatiedoston tai tietovirran uuden tietojenvaihtomäärityksen luonti käyttämällä tiedoston XML-rakennetta. Se esitäyttää **Sarakkeen määritykset** -pikalomakkeen **Kirjauksen tiedonsiirtomääritykset** -sivulla.|[XML-mallien käyttäminen tietojenvaihtomääritysten valmisteluun](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Määritä tietojen vaihtokehys, jotta käyttäjät voivat vastaanottaa ja lähettää tietoja uudessa ostoasiakirjamuodossa, tuoda uuden pankkitiedoston tai vaihtaa muita tietoja.|[Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md)|  

## <a name="see-also"></a>Katso myös  
[Sähköinen tiedonsiirto](across-data-exchange.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  
