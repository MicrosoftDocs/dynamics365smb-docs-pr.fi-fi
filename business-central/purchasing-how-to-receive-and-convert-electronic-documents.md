---
title: Sähköisten asiakirjojen vastaanottaminen ja muuntaminen
description: 'Tämä aihe kuvailee, miten voit vastaanottaa sähköisiä asiakirjoja suoraan kauppakumppaneilta tai OCR-palvelusta.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '189, 190, 191'
ms.date: 06/23/2021
ms.author: bholtorf
---
# Sähköisten asiakirjojen vastaanottaminen ja muuntaminen

> [!NOTE]
> Tämän artikkelin sisältö koskee vain Dynamics 365 Business Centralin niitä versioita, jotka on julkaistu ennen vuoden 2023 2. julkaisuaaltoa. Vuoden 2023 2. julkaisuaalto sisältää sähköisten asiakirjojen uudet toiminnot. Lisätietoja on kohdassa [Sähköisten asiakirjojen määrittäminen](finance-how-setup-edocuments.md). 


[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman yleinen versio tukee sähköisten laskujen ja hyvityslaskujen vastaanottamista PEPPOL-muodossa. Suurimmat document exchange -palveluiden tarjoajat tukevat tätä muotoa. Jotta voisit saada laskun toimittajalta sähköisenä PEPPOL-asiakirjana, asiakirja on muunnettava Saapuvat asiakirjat -sivulla [!INCLUDE[prod_short](includes/prod_short.md)]in ostolaskuksi tai päiväkirjan riviksi.

Kauppakumppaneiden sähköisten asiakirjojen suoran vastaanottamisen lisäksi voit saada sähköisiä asiakirjoja OCR-palvelusta, joka on muuntanut PDF- tai kuvatiedostoja sähköisiksi asiakirjoiksi.  

Ennen kuin voit vastaanottaa sähköisiä asiakirjoja Document Exchange -palvelun avulla, sinun on määritettävä perustietoja, kuten yritystiedot, toimittajat, nimikkeet ja mittayksiköt. Niiden avulla tunnistetaan liikekumppaneja ja nimikkeitä, kun saapuvassa asiakirjatiedostossa olevien elementtien tiedot muunnetaan [!INCLUDE[prod_short](includes/prod_short.md)]in kentiksi. Lisätietoja on kohdassa [Document Exchange -palvelun määrittäminen](across-how-to-set-up-a-document-exchange-service.md).  

Ennen kuin voit vastaanottaa sähköisiä asiakirjoja OCR-palvelun kautta, määritä ja ota käyttöön ennalta määritetty palveluyhteys. Lisätietoja on kohdassa [Saapuvien asiakirjojen määrittäminen](across-how-setup-income-documents.md).  

Sähköisten asiakirjojen saapuvan ja lähtevän liikenteen [!INCLUDE[prod_short](includes/prod_short.md)]:ssa hallitsee työjono-ominaisuus. Ennen kuin voit vastaanottaa sähköisiä asiakirjoja, on aloitettava asianmukainen työjono.  

Sähköisten asiakirjojen muuntaminen voit käynnistää joko manuaalisesti tässä proseduurissa kuvatulla tavalla tai voit ottaa työnkulun muuntamaan sähköiset asiakirjat automaattisesti niiden saapuessa. Yleinen [!INCLUDE[prod_short](includes/prod_short.md)] -versio sisältää työnkulkumallin, *Saapuvasta sähköisestä OCR:n kautta avoimen ostolaskun työnkulkuun*, joka on valmis kopioitavaksi työnkuluun ja otettavaksi käyttöön. Lisätietoja on kohdassa [Työnkulku](across-workflow.md).  

> [!NOTE]  
> Kun muunnat OCR-palvelusta vastaanotettuja sähköisiä asiakirjoja tai päiväkirjarivejä [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa, monta lähdeasiakirjan riviä yhdistetään yhdelle riville. Yhden rivin tyypiksi tulee KP-tili, ja **Kuvaus**- ja (KP-tilin) **Nro**-kentät ovat tyhjiä. **Summa**-kentän arvo on sama kuin kaikkien lähdeasiakirjan rivien kokonaissumma ilman ALV:tä.  
>
> Varmistaaksesi, että **Kuvaus** ja **Nro**-kentät on täytetty, voit valita **Linkitä teksti tiliin** -painikkeen **Saapuvat asiakirjat** -sivulla määrittääksesi, että tietty laskun teksti yhdistetään aina tiettyyn debet- tai kredit-tiliin pääkirjanpidossa. Jatkossa toimittajan tai asiakkaan sähköisestä asiakirjasta luotujen asiakirjan tai päiväkirjan rivien **Kuvaus**-kenttä täytetään kyseisellä tekstillä ja kyseisin tilin KP-tilin **Nro**-kentällä .  
>
> KP-tiliin yhdistämisen sijasta voit myös yhdistää pankkitiliin. Tämä on käytännöllistä esimerkiksi sähköisille asiakirjoille, jotka on jo maksettu, johon haluat luoda yleisen päiväkirjarivin, joka on valmis kirjattavajsu pankkitilille.  

Seuraavassa kuvataan, miten toimittajan lasku vastaanotetaan ja muunnetaan ostolaskuksi [!INCLUDE[prod_short](includes/prod_short.md)]:ssa. Menettely on sama, kun muunnat toimittajalaskun päiväkirjan riville.  

### Sähköisen laskun vastaanottaminen ja muuntaminen ostolaskuksi

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Saapuvat asiakirjat** ja valitse sitten vastaava linkki.  

2. Valitse rivi sille saapuvalle asiakirjatietueelle, joka edustaa uutta saapuvaa sähköistä laskua, ja valitse sitten **Muokkaa**-toiminto.  

    Aiheeseen liittyvä XML-tiedosto liitetään **Saapuvan asiakirjan kortti** -sivulla, ja useimmat sen kentät on esitäytetty sähköisen laskun tiedoilla. Lisätietoja on kohdassa [Saapuvien asiakirjatietueiden luominen](across-how-create-income-document-records.md).  

3. Valitse **Tiedonsiirron tyyppi** -kentässä **PEPPOL-lasku** tai **OCR-lasku** sähköisen asiakirjan lähteen mukaan.  

4. Toimittajalaskun tekstin liittäminen tiettyyn debet-tiliin tehdään valitsemalla **Toiminnot**-välilehden **Yleinen**-ryhmässä **Linkitä teksti tiliin** ja täyttämällä sitten **Tekstin yhdistäminen tiliin** -sivun tiedot.  

5. Valitse **Luo tiedosto** -toiminto.  

    [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa luodaan ostolasku, joka perustuu sähköisen asiakirjan tietoihin.  

    Yleensä vääriin tai puuttuviin perustietoihin liittyvät virheet näkyvät [!INCLUDE[prod_short](includes/prod_short.md)]in **Virhesanomat**-pikalomakkeessa.  

## Katso myös

[Ostovelkojen hallinta](payables-manage-payables.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Sähköinen tiedonsiirto](across-data-exchange.md)   
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
