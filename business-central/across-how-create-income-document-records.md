---
title: Saapuvien asiakirjatietueiden luominen
description: 'Saapuvat asiakirjat -sivun eri toimintojen avulla voit tarkastella kulukuitteja, hallita OCR-tehtäviä, muuntaa saapuvia asiakirjatiedostoja ja liittää ulkoisia tiedostoja.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="create-incoming-document-records" />Saapuvien asiakirjatietueiden luominen

**Saapuvat asiakirjat** -sivulla voit käyttää erilaisia toimintoja, joilla voit tarkistaa kulutositteita, hallita OCR-tehtäviä ja muuntaa saapuvia asiakirjatiedostoja manuaalisesti tai automaattisesti sekä siirtää niistä tietoja asiakirjoihin tai kirjanpitoriveille. Ulkoisia tiedostoja voi liittää missä tahansa prosessin vaiheessa myös kirjattuihin asiakirjoihin ja muodostuviin toimittaja-, asiakas- ja pääkirjamerkintöihin.

Voit tallentaa ulkoisen asiakirjan [!INCLUDE[prod_short](includes/prod_short.md)]issa luomalla tai suorittamalla ensin saapuvan tiedostotietueen. Voit tehdä nämä tehtävät manuaalisesti tai ottaa valokuvan ulkoisesta asiakirjasta ja luoda saapuvan asiakirjatietueen, johon on liitetty kuvatiedosto.

Ennen kuin voit käyttää **Saapuvat asiakirjat** -ominaisuutta, sinun on tehtävä tarvittavat asetukset. Lisätietoja on kohdassa [Saapuvien asiakirjojen määrittäminen](across-how-setup-income-documents.md).

## <a name="approve-or-reject-an-incoming-document" />Saapuvan asiakirjan hyväksyminen tai hylkääminen

Jos olet määrittänyt **Saapuvat asiakirjat** -ominaisuuden edellyttämään asiakirjojen luomisen hyväksynnän, käyttäjien, joilla on tarvittavat oikeudet, on hyväksyttävä tietueet ennen niiden käsittelemistä. Lisätietoja on ohjeaiheessa [Saapuvien asiakirjatietueiden hyväksyjien määrittäminen](across-how-setup-income-documents.md#to-set-up-approvers-of-incoming-document-records).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Saapuvat asiakirjat** ja valitse sitten vastaava linkki.
2. Valitse rivi, jolla hyväksyttävä tai hylättävä asiakirja on, ja valitse sitten **Hyväksy**- tai **Hylkää**-toiminto.

Jos hyväksyt saapuvan asiakirjatietueen, saapuvan asiakirjan rivin **Vapautettu**-valintaruutu on valittuna. Esimerkiksi ostolaskujen luonnista vastaava henkilö voi nyt aloittaa tietueen käsittelemisen.

## <a name="create-an-incoming-document-record-by-taking-a-photo" />Saapuvien asiakirjatietueiden luominen valokuva ottamalla

> [!NOTE]  
> Seuraavat toimet koskevat vain [!INCLUDE[prod_short](includes/prod_short.md)]in tabletti- ja puhelinasiakasohjelmia.

1. Valitse roolikeskuksesta **luo saapuva asiakirja kamerasta** ruutu ja siirry sitten vaiheeseen 4.
2. Valitse vaihtoehtoisesti ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Saapuvat asiakirjat** ja valitse sitten vastaava linkki.
3. Valitse **Saapuvat asiakirjat** -sivulla **'Uusi** ja valitse sitten **Luo kamerasta**. Tabletin tai puhelimen kamera ativoituu.
4. Ota valokuva asiakirjasta, kuten tavaran vastaanotto, jonka haluat käsitellä saapuvana asiakirjana,ja valitse sitten **Käytä**.

    Luo uuden saapuvan asiakirjan tietueen ja liittää kuvan.

## <a name="attach-an-image-to-an-incoming-document-record-by-taking-a-photo" />Kuvan liittäminen saapuvien asiakirjatietueiden tietueeseen valokuva ottamalla

> [!NOTE]  
> Seuraavat toimet koskevat vain [!INCLUDE[prod_short](includes/prod_short.md)]in tabletti- ja puhelinasiakasohjelmia.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Saapuvat asiakirjat** ja valitse sitten vastaava linkki.
2. Avaa aiemmin luotu saapuvan asiakirjan tietue kortti.
3. Valitse asiakirjatietuesivulla **Käsittele** ja valitse sitten **Liitä kuva kamerasta**. Tabletin tai puhelimen kamera aktivoituu.
4. Ota valokuva asiakirjasta, kuten tavaran vastaanotto, jonka haluat käsitellä saapuvana asiakirjana,ja valitse sitten **Käytä**.

    Kuva liitetään saapuvan asiakirjan tietueeseen.

## <a name="create-an-incoming-document-record-manually" />Saapuvan asiakirjatietueen luominen manuaalisesti

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Saapuvat asiakirjat** ja valitse sitten vastaava linkki.
2. Valitse **Uusi** ja sitten **Luo tiedostosta** -toiminto.  
3. **Lisää tiedosto** -sivulla valitse tiedosto ja valitse sitten **Avaa**. Tiedosto liitetään automaattisesti.
4. Vaihtoehtoisesti voit valita **Uusi**-toiminnon.
5. Voit liittää tiedoston valitsemalla **Käsittele** ja sitten **Liitä tiedosto** -toiminnon.
6. Valitse **Lisää tiedosto** -sivulla tiedosto, joka vastaa kyseistä saapuvaa asiakirjaa, ja valitse sitten **Avaa**.
7. Täytä **Saapuva asiakirja** -sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-microsoft-trainingtrainingmodulesincoming-documents-dynamics--business-central" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also" />Katso myös

[Käytä OCR:ää PDF-ja kuvatiedostojen muuntamiseksi sähköisiksi asiakirjoiksi](across-how-use-ocr-pdf-images-files.md)
[Saapuvien asiakirjatietueiden luominen suoraan asiakirjoista ja tapahtumista](across-how-connect-disconnect-income-document-records.md)
[Sellaisten kirjattujen asiakirjojen etsiminen, joilla ei ole saapuvia asiakirjatietueita](across-how-find-posted-documents-without-income-document-records.md)
[Saapuvat asiakirjat](across-income-documents.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
