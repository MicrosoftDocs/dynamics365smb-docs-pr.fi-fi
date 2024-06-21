---
title: Sähköisten asiakirjojen lähettäminen
description: 'Lue, miten voit lähettää sähköisiä laskuja ja hyvityslaskuja PEPPOL-muodossa Business Centralin avulla.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Sähköisten asiakirjojen lähettäminen

> [!NOTE]
> Tämän artikkelin sisältö koskee vain Dynamics 365 Business Centralin niitä versioita, jotka on julkaistu ennen vuoden 2023 2. julkaisuaaltoa. Vuoden 2023 2. julkaisuaalto sisältää sähköisten asiakirjojen uudet toiminnot. Lisätietoja on kohdassa [Sähköisten asiakirjojen määrittäminen](finance-how-setup-edocuments.md).  

[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman yleinen versio tukee sähköisten laskujen ja hyvityslaskujen lähettämistä PEPPOL-muodossa. Suurimmat document exchange -palveluiden tarjoajat tukevat tätä muotoa. Document exchange -palveluiden tarjoaja välittää sähköisiä asiakirjoja liikekumppaneiden välillä. Käyttämällä tiedonsiirtokehystä voidaan tukea myös muita sähköisiä asiakirjamuotoja.  

 Document exchange -palvelu on esimääritetty [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman yleisessä versiossa, ja se on valmis määritettäväksi yrityksellesi. Lisätietoja on kohdassa [Document Exchange -palvelun määrittäminen](across-how-to-set-up-a-document-exchange-service.md). Joissakin tapauksissa sovellus on kuitenkin asennettava. Lisätietoja on kohdassa [Sähköinen laskutus – usein kysytyt kysymykset](faq-electronic-invoicing.yml).  

 Lähettääksesi myyntilaskun sähköisenä PEPPOL-tiedostona voit valita **Sähköinen asiakirja** -vaihtoehdon **Kirjaa ja lähetä** -valintaikkunassa. Voit määrittää myös asiakkaan oletuslähettämisprofiilin kyseisessä valintaikkunassa. Aluksi on määritettävä joitakin perustietoja, kuten yrityksen tiedot, asiakkaat, nimikkeet ja mittayksiköt. Näitä käytetään liiketoimintakumppanien ja nimikkeiden tunnistamiseen, kun kenttien tietoja muutetaan. Lisätietoja on kohdassa [Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen](across-how-to-set-up-electronic-document-sending-and-receiving.md).  

### Sähköisen myyntilaskun lähettäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntilaskut** ja valitse sitten vastaava linkki.  

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

## Katso myös

[Lasku – myynti](sales-how-invoice-sales.md)  
[Asiakirjan lähetyksen profiilien määrittäminen](sales-how-setup-document-send-profiles.md)  
[Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Document Exchange -palvelun määrittäminen](across-how-to-set-up-a-document-exchange-service.md)  
[Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md)  
[Sähköinen tiedonsiirto](across-data-exchange.md)  
[Sähköinen laskutus – usein kysytyt kysymykset](faq-electronic-invoicing.yml)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
