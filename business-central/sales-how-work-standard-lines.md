---
title: Vakiomalliset toistuvat myyntirivit
description: Voit määrittää usein käytettäviä ostorivejä. Voit sitten lisätä ne ostoasiakirjoihin ja täyttää tällä tavoin vakiotiedot nopeasti.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'trade, sell, replenishment'
ms.search.form: 172
ms.date: 02/14/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="create-recurring-sales"></a>Toistuvan myynnin luominen

Jos sinun on usein luotava samankaltaisia tietoja sisältäviä myyntirivejä, voit määrittää vakiorivejä ja lisätä ne sitten toistuviin myyntiasiakirjoihin, kuten toistuviin täydennystilauksiin.  

## <a name="set-up-recurring-sales-lines"></a>Toistuvien myyntirivien määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toistuvat myyntirivit** ja valitse sitten vastaava linkki.  
2. Valitse **Toistuvat myyntirivit** -sivulla **Uusi**-toiminto.  
3. Täytä **Yleiset**-pikavälilehdessä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Kirjoita **Rivit**-pikavälilehden kenttiin esitiedot, jotka sopivat toistuvina riveinä myyntiasiakirjoissa käytettäviksi vakioriveiksi.  

> [!NOTE]
> Toistuvilla myyntiriveillä ei voi määrittää hintoja, koska esimerkiksi hinnat ja alennukset lasketaan varsinaisissa myyntiasiakirjoissa toistuvien myyntirivien lisäämisen jälkeen.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## <a name="assign-recurring-sales-lines-to-a-customer"></a>Toistuvien myyntirivien määrittäminen asiakkaalle

Määritä asiakkaalle vähintään yksi toistuva myyntirivi, jotta näitä rivejä voidaan liittää kyseisen asiakkaan myyntiasiakirjoihin.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Avaa soveltuvan asiakkaan kortti.
3. Valitse **Toistuvat myyntirivit** -toiminto.
4. Valitse **Toistuvat myyntirivit** -sivulla niiden toistuvien myyntirivien koodit, joita haluat lisätä asiakkaan myyntiasiakirjoihin.
5. Täytä muut kentät ja määritä, milloin, miten ja missä toistuvia myyntirivejä käytetään.  

    Jos aiot käyttää toistuvien myyntirivien joukkoa yhdessä **Luo toistuvia myyntilaskuja** -erätyön avulla, käytä **Voimassaolon alkamispäivämäärä**- ja **Voimassaolon päättymispäivämäärä** -kenttiä rajoittamaan sitä, kun toistuvia myyntirivejä käytetään laskujen luomiseen. Lisätietoja on kohdassa [Useiden myyntilaskujen luonti vakiomyyntikoodien perusteella](sales-how-work-standard-lines.md#create-multiple-sales-invoices-based-on-recurring-sales-lines).

    Voit myös määrittää suoraveloitusmaksumenetelmän ja suoraveloitusvaltakirjan. Laskut, jotka luodaan **Luo toistuvia myyntilaskuja** -eräajolla, sisältävät tietoja, jotka vaaditaan maksun perimiseen SEPA-suoraveloituksella. Lisätietoja on ohjeaiheessa [Maksujen kerääminen SEPA-suoraveloitusperintänä](finance-collect-payments-with-sepa-direct-debit.md).

6. Voit valita neljässä kentässä, miten rivejä lisätään neljään asiakirjatyyppiin valitsemalla jonkin seuraavista asetuksista:

|Asetus|Kuvaus|
|------|-----------|
|**Manuaalinen**|Asiakkaalla olevat toistuvat myyntirivit on valittava ja lisättävä manuaalisesti.|
|**Automaattinen**|Jos asiakkaalla on useita toistuvia myyntirivejä, saat ilmoituksen siitä, mistä voidaan valita lisättävä rivi. Jos toistuvia myyntirivejä on vain yksi, se lisätään automaattisesti.<br /><br />Tämä toimii vain, jos uusi asiakirja luotiin asiakirjaluettelosta esimerkiksi valitsemalla **Uusi**-toiminto **Myyntitilaukset**-sivulla. Se ei toimi, jos asiakirja luotiin esimerkiksi asiakaskortista.|
|**Kysy aina**|Ilmoitus avautuu ja kaikki aiemmin luodut toistuvat myyntirivit näytetään. Voit sitten valita niistä yhden.

## <a name="insert-recurring-sales-lines-on-a-sales-invoice"></a>Toistuvien myyntirivien lisääminen myyntilaskuun

Jos asiakkaalla on toistuvia myyntirivejä, voit lisätä tai antaa muiden lisätä niitä kaikenlaisiin myyntiasiakirjoihin, kuten myyntilaskuun. Jos olet aktivoinut **Kysy aina** -asetukset määrittäessäsi toistuvia myyntirivejä asiakkaille, saat ilmoituksen, jos toistuvia myyntirivejä on.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntilaskut** ja valitse sitten vastaava linkki.
2. Avaa myyntilasku, johon haluat lisätä vähintään yhden vakiomyyntirivin.
3. Valitse **Nouda toistuvat myyntirivit** -toiminto.
4. Valitse **Toistuvat myyntirivit** -sivun **Koodi**-kentässä hakupainike ja valitse sitten vakiomyyntirivijoukko.
5. Lisää vakiomyyntirivit laskuun valitsemalla **OK**. Voit sitten käyttää näitä rivejä sellaisenaan tai muokata rivien tietoja.

## <a name="create-multiple-sales-invoices-based-on-recurring-sales-lines"></a>Useiden myyntilaskujen luonti toistuvien myyntirivien perusteella

Voit luoda **Luo toistuvia myyntilaskuja** -eräajolla myyntilaskuja asiakkaille määritettyjen vakiomyyntirivien mukaan siten, että niiden kirjauspäivämäärät ovat vakiomyyntiriveille määritetyllä voimassaolon päivämäärävälillä.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luo toistuvia myyntilaskuja** ja valitse sitten vastaava linkki.
2. Täytä **Luo toistuvia myyntilaskuja** -sivulla tarvittavat kentät.
3. Anna **Koodi**-suodatinkentässä sille asiakkaalle määritetty vakiomyyntirivien koodi, jolle haluat luoda myyntilaskuja.
4. Valitse **OK**-painike.

Myyntilaskut luodaan asiakkaille, joilla on määrätty asiakkaan vakiomyyntikoodi ja jotkut määritetyt suoraveloitustiedot kirjaamista varten määrättynä päivämääränä.

## <a name="see-also"></a>Katso myös

[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Toistuvien ostorivien luominen](purchasing-how-work-recurring-purchase-lines.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
