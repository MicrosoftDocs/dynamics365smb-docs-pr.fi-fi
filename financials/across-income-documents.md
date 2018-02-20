---
title: "Saapuvien asiakirjojen käyttäminen| Microsoft Docs"
description: "Voit hallita saapuvia, ulkoisia yritysasiakirjoja, kuten maksukuitteja tai PDF-tiedostoja, hallita OCR-tehtäviä ja muuntaa tiedostoja sähköisiksi asiakirjoiksi ja tietueiksi Financialsissa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d38f1ed77ac3fac7c9283af6ea0f92479adbf89f
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="incoming-documents"></a>Saapuvat asiakirjat
Kaikkia liiketoimintatapahtumia ei tallenneta heti [!INCLUDE[d365fin](includes/d365fin_md.md)]iin. Ulkoinen liiketoiminta-asiakirja saattaa sen sijaan tulla yritykseesi sähköpostin liitteenä tai paperiversiona, jonka voit skannata tiedostoon. Tämä on tyypillistä ostoille, joissa saapuvat asiakirjatiedostot edustavat kulujen maksukuitteja tai pieniä ostoja.

Ulkoinen OCR (Optical Character Recognition) -palvelu voi muodostaa sähköisiä asiakirjoja saapuvia asiakirjoja vastaavista PDF- tai kuvatiedostoista, ja ne voidaan sitten muuntaa [!INCLUDE[d365fin](includes/d365fin_md.md)]issa asiakirjatietueiksi.

**Saapuvat asiakirjat** -ikkunassa voit käyttää erilaisia toimintoja, joilla voit tarkistaa kulutositteita, hallita OCR-tehtäviä ja muuntaa saapuvia asiakirjatiedostoja manuaalisesti tai automaattisesti sekä siirtää niistä tietoja asiakirjoihin tai kirjanpitoriveille. Ulkoisia tiedostoja voi liittää missä tahansa prosessin vaiheessa myös kirjattuihin asiakirjoihin ja muodostuviin toimittaja-, asiakas- ja pääkirjamerkintöihin.

Saapuvien asiakirjojen käsittely voi muodostua seuraavista pääaktiviteeteista:

* Tallenna ulkoiset asiakirjat [!INCLUDE[d365fin](includes/d365fin_md.md)]iin luomalla rivejä **Saapuvat asiakirjat** -ikkunassa toisella seuraavista tavoista:
  * Manuaalisesti käyttämällä yksinkertaista tietokoneen tai puhelimen toimintoja jollakin seuraavista tavoista:
    * Käytä **Luo tiedostosta** -painiketta ja täytä tarvittavat kentät **Saapuva asiakirja** -ikkunassa. Tiedosto liitetään automaattisesti.  
    * Käytä **Uusi**-painiketta ja täytä tarvittavat kentät **Saapuva asiakirja** -ikkunassa. Liitä tämän jälkeen tiedosto manuaalisesti.
    * Käytä tablet tai puhelin ja luo **Luo kamerasta** painikkeen avulla uusi saapuva asiakirja ja sitten lähetä kuva OCR-palveluun, esimerkiksi.
  * Automaattinen tallennus tapahtuu vastaanottamalla asiakirja OCR-palvelusta sähköisenä asiakirjana sen jälkeen, kun olet lähettänyt liittyvän PDF- tai kuvatiedoston sähköpostitse OCR-palveluun. **Rahoituksellisia tietoja** -pikavälilehden tiedot täytetään automaattisesti **Saapuva asiakirja** -ikkunassa.
* Muunna PDF- tai kuvatiedostot OCR-palvelussa sähköisiksi asiakirjoiksi, jotka voidaan muuntaa [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakirjatietueiksi.
* Luo saapuville asiakirjatietueille uusia asiakirjoja tai yleisen päiväkirjan rivejä syöttämällä tiedot samalla kun luet ne saapuvista asiakirjatiedostoista.
* Liitä saapuvia asiakirjatiedostoja missä tahansa tilassa oleviin osto- ja myyntiasiakirjoihin (myös kirjauksesta muodostuviin toimittaja-, asiakas- ja pääkirjamerkintöihin).
* Tarkastele saapuvia asiakirjatietueita ja niiden liitteitä mistä tahansa osto- tai myyntiasiakirjasta. **Tilikartta**-ikkunasta voit myös etsiä kaikki pääkirjamerkinnät, joilla ei ole saapuvia asiakirjatietueita.

| Toiminta | Katso |
| --- | --- |
| Määritä Saapuvat asiakirjat -ominaisuus ja OCR-palvelu. |[Määritä saapuvat asiakirjat](across-how-setup-income-documents.md) |
| Luo saapuvan asiakirjan tietueet, liitä tiedostot, käytä OCR:ää muuntamaan PDF-tiedostot sähköisiksi asiakirjoiksi, muunna sähköiset asiakirjat asiakirjatietueiksi, valvo kirjattujen myynti- ja ostoasiakirjojen saapuvia asiakirjatietueita. |[Saapuvien asiakirjojen käsitteleminen](across-process-income-documents.md) |

## <a name="see-also"></a>Katso myös
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

