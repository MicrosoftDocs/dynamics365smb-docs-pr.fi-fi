---
title: Sähköisten asiakirjojen lähettäminen
description: Lisätietoja laskujen lähettämisestä sähköisesti.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d547f031d9d33c0d7cd5f8b20398fd7b6dbe0393
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382998"
---
# <a name="send-electronic-documents"></a>Sähköisten asiakirjojen lähettäminen

[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman yleinen versio tukee sähköisten laskujen ja hyvityslaskujen lähettämistä PEPPOL-muodossa. Suurimmat document exchange -palveluiden tarjoajat tukevat tätä muotoa. Document exchange -palveluiden tarjoaja välittää sähköisiä asiakirjoja liikekumppaneiden välillä. Käyttämällä tiedonsiirtokehystä voidaan tukea myös muita sähköisiä asiakirjamuotoja.  

 Document exchange -palvelu on esimääritetty [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman yleisessä versiossa, ja se on valmis määritettäväksi yrityksellesi. Lisätietoja on kohdassa [Document Exchange -palvelun määrittäminen](across-how-to-set-up-a-document-exchange-service.md). Joissakin tapauksissa sovellus on kuitenkin asennettava. Lisätietoja on kohdassa [Sähköinen laskutus – usein kysytyt kysymykset](faq-electronic-invoicing.yml).  

 Lähettääksesi myyntilaskun sähköisenä PEPPOL-tiedostona voit valita **Sähköinen asiakirja** -vaihtoehdon **Kirjaa ja lähetä** -valintaikkunassa. Voit määrittää myös asiakkaan oletuslähettämisprofiilin kyseisessä valintaikkunassa. Aluksi on määritettävä joitakin perustietoja, kuten yrityksen tiedot, asiakkaat, nimikkeet ja mittayksiköt. Näitä käytetään liiketoimintakumppanien ja nimikkeiden tunnistamiseen, kun kenttien tietoja muutetaan. Lisätietoja on kohdassa [Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen](across-how-to-set-up-electronic-document-sending-and-receiving.md).  

### <a name="to-send-an-electronic-sales-invoice"></a>Sähköisen myyntilaskun lähettäminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntilaskut** ja valitse sitten liittyvä linkki.  

2. Luo uusi myyntilasku.  

3. Kun myyntilasku on valmis laskutettavaksi, valitse **Kirjaa ja lähetä** -toiminto.  

     Jos asiakkaan oletuslähetysprofiili on **Sähköinen asiakirja**, se näkyy **Kirjaa ja lähetä vahvistus** -valintaikkunassa. Tällä tavalla sinun tarvitsee vain valita **Kyllä**-painike kirjataksesi ja lähettääksesi laskun sähköisesti valitussa muodossa.  

4. Valitse **Kirjaa ja lähetä vahvistus** -valintaikkunassa **Lähetä asiakirja vastaanottajalle** -kentän oikealla puolella oleva MuokkausApu-painike.  

5. Valitse **Lähetä asiakirja kohteeseen** -valintaikkunassa **Sähköinen asiakirja** -kentässä **Document Exchange -palvelun kautta**.  

6. Valitse **Muoto**-kentässä **PEPPOL**.  

7. Valitse **OK**-painike. **Kirjaa ja lähetä vahvistus** -valintaikkuna tulee näkyviin. **Sähköinen asiakirja (PEPPOL)** lisätään **Lähetä asiakirja kohteeseen** -kenttään.  

8. Valitse **Kyllä**-painike.  

     Myyntilasku kirjataan ja lähetetään asiakkaalle PEPPOL-muodossa.  

    > [!NOTE]  
    >  Voit myös lähettää kirjatun myyntilaskun sähköisenä asiakirjana. Menettely on sama kuin joka on kuvattu tässä aiheessa kirjaamattomille myyntiasiakirjoille. Valitse **Kirjattu myyntilasku** -sivun **Toimintoloki**-toiminto, kun haluat tarkastella sähköisen asiakirjan tilaa.  

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Myynnin laskutus](sales-how-invoice-sales.md)  
[Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md)  
[Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Document Exchange -palvelun määrittäminen](across-how-to-set-up-a-document-exchange-service.md)  
[Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md)  
[Sähköinen tiedonsiirto](across-data-exchange.md)  
[Sähköinen laskutus – usein kysytyt kysymykset](faq-electronic-invoicing.yml)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]