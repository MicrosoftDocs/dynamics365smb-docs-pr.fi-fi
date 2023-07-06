---
title: Asiakasalennusryhmien määrittäminen
description: Tietoja asiakasalennusryhmien määrittämisestä ja myyntirivialennusten luomisesta näille ryhmille.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 06/08/2022
ms.author: a-reishima
---
# <a name="set-up-customer-discount-groups"></a><a name="set-up-customer-discount-groups"></a><a name="set-up-customer-discount-groups"></a>Asiakasalennusryhmien määrittäminen

Voit määrittää myyntirivialennuksia asiakasryhmälle sen sijaan, että soveltaisit niitä yksitellen.

**Asiakasalennusryhmät** toimivat samalla tavalla kuin [asiakashintaryhmät](sales-how-to-set-up-customer-price-groups.md), mutta ne voidaan yhdistää nimikealennusryhmiin useiden nimikkeiden rivialennusten nopeaksi määrittämiseksi valituille asiakkaille.

## <a name="create-sales-line-discounts-for-a-customer-group"></a><a name="create-sales-line-discounts-for-a-customer-group"></a><a name="create-sales-line-discounts-for-a-customer-group"></a>Myyntirivialennusten luonti asiakasryhmälle

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakasalennusryhmät** ja valitse sitten vastaava linkki.
2. Valitse **Asiakasalennusryhmät**-sivulla **Uusi** luodaksesi uuden alennusryhmän, anna sille nimi **Koodi**-sarakkeessa ja lisää kuvaus.
3. Valitse **Siirry**-toiminto ja valitse **Myyntirivialennukset**.
4. Täytä **Myyntikoodi**-sarake edellisellä sivulla luodulla alennusryhmällä.
5. Täytä rivien kentät **Tyypillä** (nimike tai nimikealennusryhmä), **Koodilla**, **Mittayksikön koodilla** ja **Rivialennus-%:lla**.
6. Jos asiakasryhmän täytyy ostaa vähimmäismäärä saadakseen sovitun alennuksen, täytä **Vähimmäismäärä**-kenttä.
7. Syötä tarvittaessa alennusryhmän **Aloituspvm** ja **Lopetuspvm**.
8. Tarvittaessa voit myös määrittää **Valuuttakoodin** tai **Varianttikoodin**, kun olet [mukauttanut sarakkeita](ui-personalization-user.md).

Toista vaiheet 4–8 kunkin sellaisen nimikkeen tai nimikealennusryhmän osalta, jolle haluat luoda myyntirivialennuksen.

## <a name="assign-a-customer-to-a-discount-group"></a><a name="assign-a-customer-to-a-discount-group"></a><a name="assign-a-customer-to-a-discount-group"></a>Lisää asiakas alennusryhmään

Sen jälkeen, kun olet määrittänyt asiakasalennusryhmät, voit syöttää asiakkaan alennusryhmäkoodit asiakaskortteihin.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Avaa sen asiakkaan **asiakaskortti**, jonka haluat liittää asiakasalennusryhmään.
3. Valitse **Laskutus**-pikavälilehden **Asiakkaan alennusryhmä** -kentässä ryhmäkoodi.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Katso myös

[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Erikoismyyntihintojen ja -alennusten kirjaaminen](sales-how-record-sales-price-discount-payment-agreements.md)  
[Asiakashintaryhmien määrittäminen](sales-how-to-set-up-customer-price-groups.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
