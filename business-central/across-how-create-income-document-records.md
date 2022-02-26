---
title: Saapuvien asiakirjatietueiden luominen
description: Saapuvat asiakirjat -sivun eri toimintojen avulla voit tarkastella kulukuitteja, hallita OCR-tehtäviä, muuntaa saapuvia asiakirjatiedostoja ja liittää ulkoisia tiedostoja.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 130a41d23a6e28979fad1e4999a1f620eaf7affe
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437700"
---
# <a name="create-incoming-document-records"></a>Saapuvien asiakirjatietueiden luominen
**Saapuvat asiakirjat** -sivulla voit käyttää erilaisia toimintoja, joilla voit tarkistaa kulutositteita, hallita OCR-tehtäviä ja muuntaa saapuvia asiakirjatiedostoja manuaalisesti tai automaattisesti sekä siirtää niistä tietoja asiakirjoihin tai kirjanpitoriveille. Ulkoisia tiedostoja voi liittää missä tahansa prosessin vaiheessa myös kirjattuihin asiakirjoihin ja muodostuviin toimittaja-, asiakas- ja pääkirjamerkintöihin.

Voit tallentaa ulkoisen asiakirjan [!INCLUDE[prod_short](includes/prod_short.md)]issa luomalla tai suorittamalla ensin saapuvan tiedostotietueen. Voit tehdä tämän manuaalisesti tai ottaa valokuvan ulkoisesta asiakirjasta ja luoda sitten saapuva asiakirjatietue, johon on liitetty kuvatiedosto.

Ennen kuin voit käyttää Saapuvat asiakirjat -ominaisuutta, sinun on tehtävä tarvittavat asetukset. Lisätietoja on kohdassa [Saapuvien asiakirjojen määrittäminen](across-how-setup-income-documents.md).

## <a name="to-approve-or-reject-an-incoming-document"></a>Saapuvan asiakirjan hyväksyminen tai hylkääminen
Jos haluat, että käyttäjät voivat luoda laskuja tai yleisen päiväkirjan rivejä saapuvista asiakirjatietueista vasta, kun ne on hyväksytty, voit määrittää hyväksyjät, joiden on hyväksyttävä tietueet ennen niiden käsittelyä.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Saapuvat asiakirjat** ja valitse sitten vastaava linkki.
2. Valitse rivi, jolla hyväksyttävä tai hylättävä asiakirja on, ja valitse sitten **Hyväksy**- tai **Hylkää**-toiminto.

Jos hyväksyt saapuvan asiakirjatietueen, saapuvan asiakirjan rivin **Vapautettu**-valintaruutu on valittuna. Esimerkiksi ostolaskujen luonnista vastaava henkilö voi nyt aloittaa tietueen käsittelemisen.

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a>Saapuvien asiakirjatietueiden luominen valokuva ottamalla
> [!NOTE]  
>   Seuraavat toimet koskevat vain [!INCLUDE[prod_short](includes/prod_short.md)]in tabletti- ja puhelinasiakasohjelmia.

1. Valitse sovellusriviltä **luo saapuva asiakirja kamerasta** ruutu ja siirry sitten vaiheeseen 4.
2. Voit myös valita sovellusrivin, valita asetukset-painikkeen, valita **saapuvat asiakirjat**, ja valita sitten **kaikki**.
3. Valitse **Saapuvat asiakirjat** -sivulla ellipsipainike ja valitse sitten **Luo kamerasta**. Tabletin tai puhelimen kamera ativoituu.
4. Ota valokuva asiakirjasta, kuten tavaran vastaanotto, jonka haluat käsitellä saapuvana asiakirjana,ja valitse sitten **OK**.

    Luo uuden saapuvan asiakirjan tietueen ja liittää kuvan.

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a>Kuvan liittäminen saapuvien asiakirjatietueiden tietueeseen valokuva ottamalla
> [!NOTE]  
>   Seuraavat toimet koskevat vain [!INCLUDE[prod_short](includes/prod_short.md)]in tabletti- ja puhelinasiakasohjelmia.

1. Voit valita sovellusrivin, valita asetukset-painikkeen, valita **saapuvat asiakirjat**, ja valita sitten **kaikki**.
2. Avaa aiemmin luotu saapuvan asiakirjan tietue kortti.
3. Valitse **Saapuva asiakirja** -sivulla ellipsipainike ja valitse sitten **Liitä kuva kamerasta**. Tabletin tai puhelimen kamera ativoituu.
4. Ota valokuva asiakirjasta, kuten tavaran vastaanotto, jonka haluat käsitellä saapuvana asiakirjana,ja valitse sitten **OK**.

    Kuva liitetään saapuvan asiakirjan tietueeseen.

## <a name="to-create-an-incoming-document-record-manually"></a>Saapuvan asiakirjatietueen luominen manuaalisesti
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Saapuvat asiakirjat** ja valitse sitten vastaava linkki.
2. Valitse **Luo tiedostosta** -toiminto.  
3. **Lisää tiedosto** -sivulla valitse tiedosto ja valitse sitten **Avaa**. Tiedosto liitetään automaattisesti.
4. Vaihtoehtoisesti voit valita **Uusi**-toiminnon.
5. Voit liittää tiedoston valitsemalla **Liitä tiedosto** -toiminto.
6. Valitse **Lisää tiedosto** -sivulla tiedosto, joka vastaa kyseistä saapuvaa asiakirjaa, ja valitse sitten **Avaa**.
7. Täytä **Saapuva asiakirja** -sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Katso myös
[Saapuvien asiakirjojen käsitteleminen](across-process-income-documents.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]