---
title: "Sähköisten tiedostojen lähettäminen | Microsoft Docs"
description: "Lisätietoja laskujen lähettämisestä sähköisesti."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: eb9a20547c7eef346fa199eaa136211dcdd09dab
ms.contentlocale: fi-fi
ms.lasthandoff: 09/27/2017

---
# <a name="how-to-send-electronic-documents"></a>Toimintaohje: Sähköisten asiakirjojen lähettäminen
[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman yleinen versio tukee sähköisten laskujen ja hyvityslaskujen lähettämistä PEPPOL-muodossa. Suurimmat document exchange -palveluiden tarjoajat tukevat tätä muotoa. Document exchange -palveluiden tarjoaja välittää sähköisiä asiakirjoja liikekumppaneiden välillä. Käyttämällä tiedonsiirtokehystä voidaan tukea myös muita sähköisiä asiakirjamuotoja.  

 Document exchange -palvelu on esimääritetty [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman yleisessä versiossa, ja se on valmis määritettäväksi yrityksellesi. Lisätietoja on kohdassa [Toimintaohje: Document Exchange -palvelun määrittäminen](across-how-to-set-up-a-document-exchange-service.md).  

 Jos haluat lähettää myyntilaskun sähköisenä PEPPOL-asiakirjana, valitse **Sähköinen asiakirja** -vaihtoehto **Kirjaa ja lähetä** -valintaikkunassa. Samassa valintaikkunassa voit määrittää sähköisen lähettämisen asiakkaan asiakirjojen oletuslähetysprofiiliksi. Aluksi on määritettävä joitakin perustietoja, kuten yrityksen tiedot, asiakkaat, nimikkeet ja mittayksiköt. Näitä käytetään liiketoimintakumppanien ja nimikkeiden tunnistamiseen, kun kenttien tietoja muutetaan. Lisätietoja on kohdassa [Toimintaohje: Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen](across-how-to-set-up-electronic-document-sending-and-receiving.md).  

### <a name="to-send-an-electronic-sales-invoice"></a>Sähköisen myyntilaskun lähettäminen  

1.  Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, kirjoita **Myyntilaskut** ja valitse sitten aiheeseen liittyvä linkki.  

2.  Luo uusi myyntilasku.  

3.  Kun myyntilasku on laskutusvalmis, valitse **Toiminnot**-välilehden **Kirjaaminen**-ryhmästä **Kirjaa ja lähetä**.  

     Jos asiakkaan oletuslähetysprofiili on **Sähköinen asiakirja**, tieto näkyy **Kirjaa ja lähetä vahvistus** -valintaikkunassa. Lasku kirjataan ja lähetetään sähköisesti valitussa muodossa, kun valitset **Kyllä**-painikkeen.  

4.  Valitse **Kirjaa ja lähetä vahvistus** -valintaikkunassa **Lähetä asiakirja vastaanottajalle** -kentän oikealla puolella oleva MuokkausApu-painike.  

5.  Valitse **Lähetä asiakirja kohteeseen** -valintaikkunassa **Sähköinen asiakirja** -kentässä **Document Exchange -palvelun kautta**.  

6.  Valitse **Muoto**-kentässä **PEPPOL**.  

7.  Valitse **OK**-painike. **Kirjaa ja lähetä vahvistus** -valintaikkuna tulee näkyviin. **Sähköinen asiakirja (PEPPOL)** lisätään **Lähetä asiakirja kohteeseen** -kenttään.  

8.  Valitse **Kyllä**-painike.  

     Myyntilasku kirjataan ja lähetetään asiakkaalle sähköisenä asiakirjana PEPPOL-muodossa.  

    > [!NOTE]  
    >  Voit myös lähettää kirjatun myyntilaskun sähköisenä asiakirjana. Menettely on sama kuin joka on kuvattu tässä aiheessa kirjaamattomille myyntiasiakirjoille. **Kirjattu myyntilasku** -ikkunassa **Toiminnot** välilehdessä **Yleiset**-ryhmässä valitse **Toimintoloki**, kun haluat tarkastella sähköisen asiakirjan tilaa. Lisätietoja on myös kohdassa **Toimintoloki**  

## <a name="see-also"></a>Katso myös  
[Toimintaohje: Myynnin laskutus](sales-how-invoice-sales.md)  
[Toimintaohje: Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md)  
[Toimintaohje: Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Toimintaohje: Document Exchange -palvelun määrittäminen](across-how-to-set-up-a-document-exchange-service.md)  
[Toimintaohje: Tiedonsiirtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md)  
[Sähköinen tiedonsiirto](across-data-exchange.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  

