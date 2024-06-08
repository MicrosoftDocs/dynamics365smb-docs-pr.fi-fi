---
title: Näytettävien saapuvien asiakirjojen määrittäminen
description: 'Voit muuttaa saapuvien asiakirjojen, kuten sähköisten laskujen oletusnäkymää parantaaksesi käsiteltyjen ja käsittelemättömien tietojen yleisnäkymää.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="manage-many-incoming-document-records"></a>Useiden saapuvien asiakirjatietueiden hallinta

Kun luot tai käsittelet saapuvia asiakirjatietueita, **Saapuvat asiakirjat** -sivun sisältämien rivien määrä voi kasvaa niin paljon, että yleiskuvauksen tarkasteleminen ei enää ole mahdollista. Tämän vuoksi voit määrittää saapuvien asiakirjatietueiden tilaksi *Käsitelty*, kun haluat poistaa ne oletusnäkymästä. Kun valitset **Näytä kaikki** -toiminnon, näkyvillä ovat sekä käsitellyt että käsittelemättömät tietueet.

> [!NOTE]  
> Et voi muokata tietoja, liittää tiedostoja tai suorittaa prosesseja niille saapuville asiakirjatietueille, joiden tilaksi on määritetty *Käsitelty*. Niiden tilaksi on ensin määritettävä *Käsittelemätön*.

**Käsitelty**-valintaruutu valitaan automaattisesti niille saapuville asiakirjatietueille, jotka on käsitelty. Valintaruudun voi valita tai valinnan voi poistaa myös manuaalisesti. Liiketoimintaprosessista riippuen saapuva asiakirjatietue voidaan käsitellä silloin, kun sille luodaan liittyvä asiakirja, tai tiedoston liittämisen yhteydessä.

> [!NOTE]  
> Kun avaat **Saapuvat asiakirjat** -sivun, jonka Roolikeskuksessa on **Omat saapuvat asiakirjat** -toiminto, oletusarvoisesti näytetään vain käsittelemättömät saapuvat asiakirjatietueet. Sitä kutsutaan tässä ohjeaiheessa "oletusnäkymäksi".

## <a name="to-remove-incoming-document-records-from-the-default-view"></a>Saapuvien asiakirjatietueiden poistaminen oletusnäkymästä

1. Valitse **Saapuvat asiakirjat** -sivulla saapuvista asiakirjatietueista vähintään yksi oletusnäkymästä poistettava rivi.
2. Valitse **Määritä tilaksi Käsitelty** -toiminto.

    Saapuvat asiakirjatietueet poistetaan oletusnäkymästä ja rivien **Käsitelty**-valintaruutu valitaan.

> [!NOTE]  
> Voit tehdä tämän toiminnon yksittäiselle tietueelle **Saapuvan asiakirjan kortti** -sivulla.

## <a name="to-view-all-incoming-document-records"></a>Saapuvien asiakirjatietueiden tarkasteleminen

1. Valitse **Saapuvat asiakirjat** -sivulla **Näytä kaikki** -toiminto.

Näkyvissä ovat kaikki saapuvat asiakirjatietueet, eli myös ne tietueet, joiden **Käsitelty**-valintaruutua ei ole valittu.

## <a name="to-add-incoming-document-records-to-the-default-view"></a>Saapuvien asiakirjatietueiden lisääminen oletusnäkymään

1. Valitse **Saapuvat asiakirjat** -sivulla **Näytä kaikki** -toiminto.
2. Valitse saapuvista asiakirjatietueista vähintään yksi rivi, jonka haluat näkyvän oletusnäkymässä.
3. Valitse **Määritä tilaksi Käsittelemätön** -toiminto.  

> [!NOTE]  
> Voit tehdä tämän toiminnon yksittäiselle tietueelle **Saapuvan asiakirjan kortti** -sivulla.

## <a name="see-also"></a>Katso myös
  
[Saapuvien asiakirja tietueiden luonti](across-how-create-income-document-records.md)
[Saapuvien asiakirjatietueiden luominen suoraan asiakirjoista ja tapahtumista](across-how-connect-disconnect-income-document-records.md)
[Saapuvat asiakirjat](across-income-documents.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
