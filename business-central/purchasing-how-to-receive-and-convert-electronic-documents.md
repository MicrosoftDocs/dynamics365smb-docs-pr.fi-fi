---
title: Sähköisten asiakirjojen vastaanottaminen ja muuntaminen | Microsoft Docs
description: Voit vastaanottaa sähköisiä asiakirjoja suoraan kauppakumppaneilta tai OCR-palvelusta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: e9543d9fc361f2948907bc0e84d37dd870139cd8
ms.sourcegitcommit: 319023e53627dbe8e68643908aacc6fd594a4957
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/04/2019
ms.locfileid: "2553864"
---
# <a name="receive-and-convert-electronic-documents"></a>Sähköisten asiakirjojen vastaanottaminen ja muuntaminen
[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman yleinen versio tukee sähköisten laskujen ja hyvityslaskujen vastaanottamista PEPPOL-muodossa. Suurimmat document exchange -palveluiden tarjoajat tukevat tätä muotoa. Jotta voisit saada laskun toimittajalta sähköisenä PEPPOL-asiakirjana, asiakirja on muunnettava Saapuvat asiakirjat -sivulla [!INCLUDE[d365fin](includes/d365fin_md.md)]in ostolaskuksi tai päiväkirjan riviksi.

 Kauppakumppaneiden sähköisten asiakirjojen suoran vastaanottamisen lisäksi voit saada sähköisiä asiakirjoja OCR-palvelusta, joka on muuntanut PDF- tai kuvatiedostoja sähköisiksi asiakirjoiksi.  

 Ennen kuin voit vastaanottaa sähköisiä asiakirjoja Document Exchange -palvelun avulla, sinun on määritettävä perustietoja, kuten yritystiedot, toimittajat, nimikkeet ja mittayksiköt. Niiden avulla tunnistetaan liikekumppaneja ja nimikkeitä, kun saapuvassa asiakirjatiedostossa olevien elementtien tiedot muunnetaan [!INCLUDE[d365fin](includes/d365fin_md.md)]in kentiksi. Lisätietoja on kohdassa [Document Exchange -palvelun määrittäminen](across-how-to-set-up-a-document-exchange-service.md).  

 Ennen kuin voit vastaanottaa sähköisiä asiakirjoja OCR-palvelun kautta, määritä ja ota käyttöön ennalta määritetty palveluyhteys. Lisätietoja on kohdassa [Saapuvien asiakirjojen määrittäminen](across-how-setup-income-documents.md).  

 Sähköisten asiakirjojen saapuvan ja lähtevän liikenteen [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa hallitsee työjono-ominaisuus. Ennen kuin voit vastaanottaa sähköisiä asiakirjoja, on aloitettava asianmukainen työjono.  

 Sähköisten asiakirjojen muuntaminen voit käynnistää joko manuaalisesti tässä proseduurissa kuvatulla tavalla tai voit ottaa työnkulun muuntamaan sähköiset asiakirjat automaattisesti niiden saapuessa. Yleinen [!INCLUDE[d365fin](includes/d365fin_md.md)] -versio sisältää työnkulkumallin, *Saapuvasta sähköisestä OCR:n kautta avoimen ostolaskun työnkulkuun*, joka on valmis kopioitavaksi työnkuluun ja otettavaksi käyttöön. Lisätietoja on kohdassa [Työnkulku](across-workflow.md).  

> [!NOTE]  
>  Kun muunnat OCR-palvelusta vastaanotettuja sähköisiä asiakirjoja tai päiväkirjarivejä [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa, monta lähdeasiakirjan riviä yhdistetään yhdelle riville. Yhden rivin tyypiksi tulee KP-tili, ja **Kuvaus**- ja (KP-tilin) **Nro**-kentät ovat tyhjiä. **Summa**-kentän arvo on sama kuin kaikkien lähdeasiakirjan rivien kokonaissumma ilman ALV:tä.  
>   
>  Varmistaaksesi, että **Kuvaus** ja **Nro**-kentät on täytetty, voit valita **Linkitä teksti tiliin** -painikkeen **Saapuvat asiakirjat** -sivulla määrittääksesi, että tietty laskun teksti yhdistetään aina tiettyyn debet- tai kredit-tiliin pääkirjanpidossa. Jatkossa toimittajan tai asiakkaan sähköisestä asiakirjasta luotujen asiakirjan tai päiväkirjan rivien **Kuvaus**-kenttä täytetään kyseisellä tekstillä ja kyseisin tilin KP-tilin **Nro**-kentällä .  
>   
>  KP-tiliin yhdistämisen sijasta voit myös yhdistää pankkitiliin. Tämä on käytännöllistä esimerkiksi sähköisille asiakirjoille, jotka on jo maksettu, johon haluat luoda yleisen päiväkirjarivin, joka on valmis kirjattavajsu pankkitilille.  

 Seuraavassa kuvataan, miten toimittajan lasku vastaanotetaan ja muunnetaan ostolaskuksi [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa. Menettely on sama, kun muunnat toimittajalaskun päiväkirjan riville.  

### <a name="to-receive-and-convert-an-electronic-invoice-to-a-purchase-invoice"></a>Sähköisen laskun vastaanottaminen ja muuntaminen ostolaskuksi  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Saapuvat asiakirjat** ja valitse sitten liittyvä linkki.  

2.  Valitse rivi sille saapuvalle asiakirjatietueelle, joka edustaa uutta saapuvaa sähköistä laskua, ja valitse sitten **Muokkaa**-toiminto.  

     Aiheeseen liittyvä XML-tiedosto liitetään **Saapuvan asiakirjan kortti** -sivulla, ja useimmat sen kentät on esitäytetty sähköisen laskun tiedoilla. Lisätietoja on kohdassa [Saapuvien asiakirjatietueiden luominen](across-how-create-income-document-records.md).  

3.  Valitse **Tiedonsiirron tyyppi** -kentässä **PEPPOL-lasku** tai **OCR-lasku** sähköisen asiakirjan lähteen mukaan.  

4.  Toimittajalaskun tekstin liittäminen tiettyyn debet-tiliin tehdään valitsemalla **Toiminnot**-välilehden **Yleinen**-ryhmässä **Linkitä teksti tiliin** ja täyttämällä sitten **Tekstin yhdistäminen tiliin** -sivun tiedot.  

5.  Valitse **Luo tiedosto** -toiminto.  

     [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa luodaan ostolasku, joka perustuu sähköisen asiakirjan tietoihin.  

     Yleensä vääriin tai puuttuviin perustietoihin liittyvät virheet näkyvät [!INCLUDE[d365fin](includes/d365fin_md.md)]in **Virhesanomat**-pikalomakkeessa.  

## <a name="see-also"></a>Katso myös  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Sähköinen tiedonsiirto](across-data-exchange.md)   
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  
