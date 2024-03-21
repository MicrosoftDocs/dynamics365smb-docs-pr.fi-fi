---
title: Asiakashintaryhmien määrittäminen
description: Tietoja asiakashintaryhmien määrittämisestä ja myyntihintojen luomisesta näille ryhmille.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customer price groups, discounts, sales prices'
ms.date: 09/30/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Asiakashintaryhmien määrittäminen
  
Myyntihinnat voidaan tehdä riippuviksi asiakasryhmistä, joille myydään. Näitä kutsutaan asiakashintaryhmiksi.

Ennen kuin asiakkaan hintaryhmiä määritetään, tulee päättää, kuinka monta ryhmää haluat ja ketkä asiakkaat kuuluvat mihinkin ryhmään.  

## Myyntihintojen luominen asiakasryhmälle  

Kun olet hyväksynyt hinnat, jotka ryhmä asiakkaita maksaa tietyistä nimikkeistä, hyväksyminen rekisteröidään yksittäisten nimikkeiden osalta **Myyntihinnat**-sivun riveille.

### Myyntihintojen luominen asiakasryhmälle

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakashintaryhmät** ja valitse sitten vastaava linkki.  

2. Valitse asiakashintaryhmän rivi. Jos riviä ei ole vielä olemassa, voit luoda uuden rivin. Luo uusi entiteetti valitsemalla **Uusi** ja anna sille nimi.  
    
    Tarkista valitulle riville seuraavien kenttien sisällöt: **Salli rivialennus**, **Salli laskualennus**, **Hinta sisältää ALV:n**ja **Veron liiket. kirj.ryhmä (hinta)**. 
  
3. Valitse **SIirry**-toiminto ja valitse **Myyntihinnat**. **Myyntihinnat**-sivu aukeaa. **Myynnin tyyppi** -kenttään täytetään **Asiakashintaryhmä**.  
  
4. Täytä **Myyntikoodi**-kenttään edellisellä sivulla valitsemasi myyntikoodi.  
  
5. Täytä rivien kenttiin **Nimikenro**, **Mittayksikön koodi** ja hyväksytty **Yksikköhinta**. Voit myös asettaa näkyviin **Varianttikoodi**-sarakkeen ja määritellä **Varianttikoodin**, jos nimikkeestä on useita variantteja.  
  
6. Jos asiakasryhmän täytyy ostaa vähimmäismäärällä saadakseen sovitun hinnan, täytä **Vähimmäismäärä**-kenttä.  

7. Syötä tarvittaessa hintasopimuksen **Aloituspvm** ja **Lopetuspvm**.  
  
8. Voit myös määrittää **valuuttakoodin** tarvittaessa.

Toista työvaiheet 4–8 kunkin nimikkeen osalta, joille haluat luoda Myyntihinnan.

## Asiakkaan hintaryhmäkoodien syöttäminen asiakaskortteihin  

Sen jälkeen, kun olet määrittänyt asiakashintaryhmät, voit syöttää asiakkaan hintaryhmäkoodit asiakaskortteihin.

### Asiakkaan hintaryhmäkoodien syöttäminen asiakaskorttiin  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.  

2. Avaa sen asiakkaan **asiakaskortti**, jonka haluat liittää asiakashintaryhmään.  

3. Valitse **Laskutus**-pikavälilehden **Asiakkaan hintaryhmä** -kentässä **Asiakashintaryhmä**-koodi.  


## Katso myös

[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Erikoismyyntihintojen ja -alennusten kirjaaminen](sales-how-record-sales-price-discount-payment-agreements.md)  
[Asiakasalennusryhmien määrittäminen](sales-how-to-set-up-customer-discount-groups.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
