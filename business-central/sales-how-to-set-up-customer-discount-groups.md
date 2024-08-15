---
title: Asiakkaan alennusryhmien määrittäminen
description: Tietoja asiakasalennusryhmien määrittämisestä ja myyntirivialennusten luomisesta näille ryhmille.
author: brentholtorf
ms.service: dynamics-365-business-central
ms.topic: article
ms.date: 07/05/2024
ms.author: bholtorf
ms.reviewer: bholtorf
---
# <a name="set-up-customer-discount-groups"></a>Asiakkaan alennusryhmien määrittäminen

Voit määrittää myyntirivialennuksia asiakasryhmälle sen sijaan, että soveltaisit niitä yksitellen.

**Asiakasalennusryhmät** ovat samanlaisia [kuin asiakashintaryhmät](sales-how-to-set-up-customer-price-groups.md), mutta niitä voi yhdistää nimikealennusryhmien kanssa. Rivialennukset määritetään nopeasti monille nimikkeille valituille asiakkaille.

## <a name="create-sales-line-discounts-for-a-customer-group"></a>Myyntirivialennusten luonti asiakasryhmälle

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakasalennusryhmät** ja valitse sitten vastaava linkki.
2. Valitse **Asiakasalennusryhmät**-sivulla **Uusi** luodaksesi uuden alennusryhmän, anna sille nimi **Koodi**-sarakkeessa ja lisää kuvaus.
3. Valitse **Myynnin rivialennukset -** toiminto.
4. Täytä **Myyntikoodi**-sarake edellisellä sivulla luodulla alennusryhmällä.
5. Täytä rivien kentät **Tyypillä** (nimike tai nimikealennusryhmä), **Koodilla**, **Mittayksikön koodilla** ja **Rivialennus-%:lla**.
6. Jos asiakasryhmän täytyy ostaa vähimmäismäärä saadakseen sovitun alennuksen, täytä **Vähimmäismäärä**-kenttä.
7. Syötä tarvittaessa alennusryhmän **Aloituspvm** ja **Lopetuspvm**.
8. Tarvittaessa voit myös määrittää **Valuuttakoodin** tai **Varianttikoodin**, kun olet [mukauttanut sarakkeita](ui-personalization-user.md).

Toista vaiheet 4–8 kunkin sellaisen nimikkeen tai nimikealennusryhmän osalta, jolle haluat luoda myyntirivialennuksen.

## <a name="assign-a-customer-to-a-discount-group"></a>Lisää asiakas alennusryhmään

Sen jälkeen kun olet määrittänyt asiakkaan alennusryhmät, voit syöttää asiakkaan alennusryhmän koodit asiakkaan Kortit.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Avaa sen asiakkaan **asiakaskortti**, jonka haluat liittää asiakasalennusryhmään.
3. Valitse **Laskutus**-pikavälilehden **Asiakkaan alennusryhmä** -kentässä ryhmäkoodi.

## <a name="see-also"></a>Katso myös

[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Erikoismyyntihintojen ja -alennusten kirjaaminen](sales-how-record-sales-price-discount-payment-agreements.md)  
[Asiakashintaryhmien määrittäminen](sales-how-to-set-up-customer-price-groups.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
