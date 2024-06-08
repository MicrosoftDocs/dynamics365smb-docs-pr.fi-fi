---
title: Toimitusten yhdistäminen yhteen laskuun | Microsoft Docs
description: 'Jos haluat laskuttaa useamman kuin yhden toimituksen kerralla, voit käyttää koontilasku-ominaisuutta.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 03/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Toimitusten yhdistäminen yhteen laskuun

Jos haluat laskuttaa useamman kuin yhden toimituksen kerralla, voit käyttää koontilasku-ominaisuutta.  

Ennen kuin koontilaskun voi luoda, samalle asiakkaalle täytyy kirjata useita myyntitoimituksia samassa valuutassa. Toimintoa voi siis käyttää, kun vähintään kaksi myyntitilausta luodaan ja kirjataan toimitetuiksi, mutta ei laskutetuiksi. 

## Yhdistä manuaalisesti toimitukset yhteen laskuun

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntilaskut** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto. Lisätietoja on kohdassa [Myynnin laskutus](sales-how-invoice-sales.md).
3. Valitse **Tilausasiakkaan nro** asiakas, jolle toimitettujen nimikkeiden lasku lähetetään.  
4. Valitse **Rivit**-pikavälilehdessä **Hae toimitusrivit** -toiminto.  
5. Valitse laskuun sisällytettävä toimitusrivi:  

    - Voit lisätä kaikki rivit valitsemalla kaikki rivit ja valitsemalla sitten **OK**.  
    - Voit lisätä kaikki rivit valitsemalla kaikki rivit ja valitsemalla sitten **OK**. Voit käyttää Ctrl-näppäintä valitsemaan useita ei-perättäisiä rivejä.  

    Jos valitsit virheellisen rivin tai haluat aloittaa alusta, voit poistaa laskun rivit ja suorittaa **Hae toimitusrivit** -toiminnon uudelleen.  
7. Kirjaa lasku valitsemalla **Kirjaa**-toiminto.  

> [!TIP]  
> Jos olet toimittanut tilauksia, joissa **tilausasiakkaan nro** on eri kuin **Laskutus asiakkaan nro**, näitä rivejä ei näytetä **Hae toimitusrivit** -raportissa. Lisää **Tilausasiakas**-kenttä sivulle räätälöinnin avulla ja poista suodatin. Nyt voit lisätä toimitusrivejä laskuun riippumatta **tilausasiakkaan nro** -kentän arvosta niin kauan kuin **Laskutus asiakkaan nro** toimitusrivit vastaavat myyntilaskun arvoa.  

## Yhdistä automaattisesti toimitukset yhteen laskuun

[!INCLUDE[prod_short](includes/prod_short.md)] valitsee vain ne myyntitilaukset, joissa on valittu **koontilasku**. 

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tee koontilasku** ja valitse sitten vastaava linkki. Eräajon pyynnön sivu aukeaa.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Valitse **Kirjaa laskut** -valintaruutu.  
4. Valitse **OK**-painike.  

> [!NOTE]  
>  Huomaa, että laskut on kirjattava manuaalisesti, jos eräajon **Kirjaa laskut** -valintaruutua ei ole valittu.  

## Avoimen myyntitilauksen poistaminen koontilaskun kirjauksen jälkeen

Kun koontilasku on tehty ja kirjattu, laskutetuille riveille luodaan kirjattu myyntilasku. Alkuperäisen puitemyyntitilauksen tai myyntitilauksen **Laskutettu määrä** -kenttä päivitetään laskutetun määrän perusteella.  

Kun laskutat toimitukset näin, säilyvät tilaukset, joista toimitukset kirjattiin, vaikka ne olisi toimitettu ja laskutettu täysin.   

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poista laskutetut myyntitilaukset** ja valitse sitten linkki.  
2. Määritä **Numero** -kenttään , mitkä myyntitilaukset poistetaan.  
3. Valitse **OK**-painike.  

Voit myös poistaa manuaalisesti yksittäiset myyntitilaukset.  

Toista vaiheet 1–3 muissa käsiteltävissä asiakirjoissa, kuten puitemyyntitilauksissa.

## Katso myös

[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
