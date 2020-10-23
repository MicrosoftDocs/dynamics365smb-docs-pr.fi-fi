---
title: Saapuvien asiakirjojen käyttäminen| Microsoft Docs
description: Voit hallita saapuvia, ulkoisia yritysasiakirjoja, kuten maksukuitteja tai PDF-tiedostoja, hallita OCR-tehtäviä ja muuntaa tiedostoja sähköisiksi asiakirjoiksi ja tietueiksi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1b2ea6b02613f120cf96f330379bf9928aad4b17
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924726"
---
# <a name="incoming-documents"></a>Saapuvat asiakirjat

Kaikkia liiketoimintatapahtumia ei tallenneta heti [!INCLUDE[d365fin](includes/d365fin_md.md)]iin. Ulkoinen liiketoiminta-asiakirja saattaa sen sijaan tulla yritykseesi sähköpostin liitteenä tai paperiversiona, jonka voit skannata tiedostoon. Tämä on tyypillistä ostoille, joissa saapuvat asiakirjatiedostot edustavat kulujen maksukuitteja tai pieniä ostoja.

Ulkoinen OCR (Optical Character Recognition) -palvelu voi muodostaa sähköisiä asiakirjoja saapuvia asiakirjoja vastaavista PDF- tai kuvatiedostoista, ja ne voidaan sitten muuntaa [!INCLUDE[d365fin](includes/d365fin_md.md)]issa asiakirjatietueiksi. Valitse organisaatiolle ja/tai maalle/alueelle sopiva huoltopaketti. Voit myös luoda tapahtumia manuaalisesti edustamaan ulkoisia asiakirjoja.  

**Saapuvat asiakirjat** -sivulla voit käyttää erilaisia toimintoja, joilla voit tarkistaa kulutositteita, hallita OCR-tehtäviä ja muuntaa saapuvia asiakirjatiedostoja manuaalisesti tai automaattisesti sekä siirtää niistä tietoja asiakirjoihin tai kirjanpitoriveille. Ulkoisia tiedostoja voi liittää missä tahansa prosessin vaiheessa myös kirjattuihin asiakirjoihin ja muodostuviin toimittaja-, asiakas- ja pääkirjamerkintöihin.

Saapuvien asiakirjojen käsittely voi muodostua seuraavista pääaktiviteeteista:

* Tallenna ulkoiset asiakirjat [!INCLUDE[d365fin](includes/d365fin_md.md)]iin luomalla rivejä **Saapuvat asiakirjat** -sivulla toisella seuraavista tavoista:
  * Manuaalisesti käyttämällä yksinkertaista tietokoneen tai puhelimen toimintoja jollakin seuraavista tavoista:
    * Käytä **Luo tiedostosta** -painiketta ja täytä tarvittavat kentät **Saapuva asiakirja** -sivulla. Tiedosto liitetään automaattisesti.  
    * Käytä **Uusi**-painiketta ja täytä tarvittavat kentät **Saapuva asiakirja** -sivulla. Liitä tämän jälkeen tiedosto manuaalisesti.
    * Käytä tablet tai puhelin ja luo **Luo kamerasta** painikkeen avulla uusi saapuva asiakirja ja sitten lähetä kuva OCR-palveluun, esimerkiksi.
  * Automaattinen tallennus tapahtuu vastaanottamalla asiakirja OCR-palvelusta sähköisenä asiakirjana sen jälkeen, kun olet lähettänyt liittyvän PDF- tai kuvatiedoston sähköpostitse OCR-palveluun. **Rahoituksellisia tietoja** -pikavälilehden tiedot täytetään automaattisesti **Saapuva asiakirja** -sivulla.
* Muunna PDF- tai kuvatiedostot OCR-palvelussa sähköisiksi asiakirjoiksi, jotka voidaan muuntaa [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakirjatietueiksi.
* Luo saapuville asiakirjatietueille uusia asiakirjoja tai yleisen päiväkirjan rivejä syöttämällä tiedot samalla kun luet ne saapuvista asiakirjatiedostoista.
* Liitä saapuvia asiakirjatiedostoja missä tahansa tilassa oleviin osto- ja myyntiasiakirjoihin (myös kirjauksesta muodostuviin toimittaja-, asiakas- ja pääkirjamerkintöihin).
* Tarkastele saapuvia asiakirjatietueita ja niiden liitteitä mistä tahansa osto- tai myyntiasiakirjasta. **Tilikartta**-sivulta voi myös etsiä kaikki pääkirjamerkinnät, joilla ei ole saapuvia asiakirjatietueita.

| Vastaanottaja | Katso |
| --- | --- |
| Määritä Saapuvat asiakirjat -ominaisuus ja OCR-palvelu. |[Saapuvien asiakirjojen määrittäminen](across-how-setup-income-documents.md) |
| Luo saapuvan asiakirjan tietueet, liitä tiedostot, käytä OCR:ää muuntamaan PDF-tiedostot sähköisiksi asiakirjoiksi, muunna sähköiset asiakirjat asiakirjatietueiksi, valvo kirjattujen myynti- ja ostoasiakirjojen saapuvia asiakirjatietueita. |[Saapuvien asiakirjojen käsitteleminen](across-process-income-documents.md) |

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/incoming-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
