---
title: Mahdollisuuden myyntisyklien ja syklin vaiheiden määrittäminen
description: 'Tässä ohjeaiheessa kerrotaan, miten myynnin vaiheet määritetään ensimmäisestä yhteysotosta sulkemiseen ja miten tällä tavoin luodaan myyntisykli, joka määritetään Business Central -sovelluksen mahdollisuuksille.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'relationship, prospect'
ms.search.forms: '5122, 5121, 5120, 5175, 5119, 5098, 5096'
ms.date: 05/27/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Mahdollisuuden myyntisyklien ja syklin vaiheiden määrittäminen

Myyntisyklit ja myyntisyklin vaiheet on määritettävä ennen kuin voit ottaa myyntimahdollisuudet käyttöön. Myyntisykli muodostuu vaiheista alkuperäisestä yhteydenotosta aina kaupantekoon asti. Määrität kullekin vaiheelle vaatimukset, jotka on täytettävä, esimerkiksi myyntitarjouksen vaatiminen ennen mahdollisuuden siirtämistä seuraavaan vaiheeseen. Voit myös määrittää, voiko vaiheen ohittaa. Voit määrittää niin monta myyntisykliä kuin tarvitset. Voit määrittää myyntisykille niin monta myyntisyklin vaihetta kuin on tarpeen.

Mahdollisuuden myyntisyklien käyttöä varten sinun on määritettävä myyntisyklit ja sen eri vaiheet ja sitten liitettävä sykli mahdollisuuksiin. Liittyvän toiminnon tai tehtävien määrittäminen mahdollisuuteen voi olla myös osa myyntisyklin määrittämistä.

Tässä artikkelissa kerrotaan myös, miten tehtävät ja toiminnot määritetään ja miten toiminnoille määritetään tehtäviä. Lisätietoja on kohdassa [Tehtäviä sisältävien toimintojen määrittäminen](marketing-how-setup-opportunity-sales-cycles-stages.md#to-set-up-activities-with-tasks).

## Mahdollisuuden myyntisyklin koodien määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntisyklit** ja valitse sitten vastaava linkki. Kaikki olemassa olevat myyntisyklit sisältävä **Myyntisyklit**-sivu avautuu.
2. Valitse **Uusi**-toiminto ja täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Toista nämä vaiheet ja luo niin monta myyntijaksoa kuin haluat. Kun olet määrittänyt mahdollisuuden myyntikoodit, haluat ehkä määrittää kunkin syklin eri vaiheet.

## Mahdollisuuden myyntisyklin vaiheiden määrittäminen

1. Valitse **Myyntisyklit**-sivulla mahdollisuuden myyntisykli, jolle haluat määrittää vaiheet. Valitse sitten **Vaiheet**-toiminto. **Myyntisyklin vaiheet** -sivu avautuu.
2. Valitse **Uusi**-toiminto, kun haluat syöttää myyntisykliin uuden vaiheen.

Toista nämä vaiheet ja määritä myyntisyklille niin monta vaihetta kuin haluat.

## Syklin vaiheiden määrittäminen mahdollisuuksille

Kun olet lisännyt mahdollisuuksien myyntisyklin, voit lisätä myyntimahdollisuuksia ja liittää mahdollisuuksiin vaiheen syklin määrittämällä **Myyntisyklin koodi** -kentän. Lisätietoja on kohdassa [Myyntimahdollisuuksien luominen](marketing-how-create-opportunities.md).

## Tehtäviä sisältävien toimintojen määrittäminen

Voit yhdistää toiminnoissa useita tehtäviä, kuten tehtäviä, joista jokainen edustaa vaihetta. Toiminnon tehtävät liittyvät toisiinsa päivämääräkaavan avulla. Voit määrittää toimintoja mahdollisuuksille, myyjille tai kontakteille.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Aktiviteetit** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto ja täytä tarvittavat kentät. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3. Täytä **Rivit**-pikavälilehdessä kentät, joilla määritetään vähintään yksi toiminnon tehtävä.

## Tehtävien tai tehtävätoimintojen määrittäminen mahdollisuuksiin

Kun ole määrittänyt tehtävän, voit määrittää sen myyntimahdollisuudelle ja siten toiminnon, jolle tehtävä kuuluu.

> [!NOTE]
> Et voi luoda *Kokous*-tyypin tehtäviä [!INCLUDE [prod_short](includes/prod_short.md)] onlinessa. Tämä ominaisuus vaatii paikallisen ympäristön käyttöoikeuksia.

Seuraavassa menettelyssä toimintotehtävät määritetään mahdollisuuksille. Tehtävät määritetään myyjille ja kontakteille vastaavasti.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Mahdollisuudet** ja valitse sitten vastaava linkki.
2. Valitse ensin mahdollisuus ja sitten **Tehtävät**-toiminto.
3. Valitse **Tehtäväluettelo**-sivulla **Luo tehtävä** -toiminto.
4. Täytä **Luo tehtävä** -sivulla tarvittavat kentät. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

    > [!TIP]
    > Kuten näet **Mahdollisuus**-kentässä, tehtävä on määritetty automaattisesti asianmukaiselle mahdollisuudelle.
5. Valitse **OK**-painike.
6. Valitse **Tehtäväluettelo**-sivulla ensin uusi tehtävä ja sitten **Määritä aktiviteetit** -toiminto.
7. Täytä **Määritä aktiviteetti** -sivulla tarvittavat kentät ja valitse sitten **OK**-painike.

## Katso myös

[Myyntimahdollisuuksien käsitteleminen](marketing-processing-sales-opportunities.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]