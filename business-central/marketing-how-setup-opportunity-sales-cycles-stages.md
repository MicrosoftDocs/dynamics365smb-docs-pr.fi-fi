---
title: Mahdollisuuden myyntisyklien ja syklin vaiheiden määrittäminen| Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten myynnin vaiheet määritetään ensimmäisestä yhteysotosta sulkemiseen ja miten tällä tavoin luodaan myyntisykli, joka määritetään Business Central -sovelluksen mahdollisuuksille.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2019
ms.author: jswymer
ms.openlocfilehash: 9c49fced44fa6ed1802dcc546a116dae232a8058
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309074"
---
# <a name="set-up-opportunity-sales-cycles-and-cycle-stages"></a>Mahdollisuuden myyntisyklien ja syklin vaiheiden määrittäminen
Myyntisyklit ja myyntisyklin vaiheet on määritettävä ennen myyntimahdollisuuksien käyttöönottoa. Myyntisykli muodostuu vaiheista alkuperäisestä yhteydenotosta aina kaupantekoon asti. Jokaisella vaiheella on tietyt vaatimukset, jotka on täytettävä, esimerkiksi myyntitarjouksen vaatiminen ennen mahdollisuuden siirtämistä seuraavaan vaiheeseen. Voit myös määrittää, voiko vaiheen ohittaa. Voit määrittää tarvittavan määrän myyntisyklejä ja niille haluamasi määrän myyntisyklien vaiheita.

Mahdollisuuden myyntisyklien ottaminen käyttöön sisältää myyntisyklin määrittämisen, syklin eri vaiheiden määrittämisen ja syklin liittämisen mahdollisuuksiin. Liittyvän toiminnon tai tehtävien määrittäminen mahdollisuuteen voi olla myös osa myyntisyklin määrittämistä.

Tässä ohjeaiheessa kerrotaan, miten tehtävät ja toiminnot määritetään ja miten toiminnoille määritetään tehtäviä. Lisätietoja on kohdassa [Tehtäviä sisältävien toimintojen määrittäminen](marketing-how-setup-opportunity-sales-cycles-stages.md#to-set-up-activities-with-tasks).

## <a name="to-set-up-opportunity-sales-cycle-codes"></a>Mahdollisuuden myyntisyklin koodien määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntisyklit** ja valitse sitten liittyvä linkki. Kaikki olemassa olevat myyntisyklit sisältävä **Myyntisyklit**-sivu avautuu.
2. Valitse **Uusi**-toiminto ja täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Toista nämä vaiheet ja luo niin monta myyntijaksoa kuin haluat. Kun olet määrittänyt mahdollisuuden myyntikoodit, haluat ehkä määrittää kunkin syklin eri vaiheet.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Mahdollisuuden myyntisyklin vaiheiden määrittäminen
1. Valitse **Myyntisyklit**-sivulla mahdollisuuden myyntisykli, jolle haluat määrittää vaiheet. Valitse sitten **Vaiheet**-toiminto. **Myyntisyklin vaiheet** -sivu avautuu.
2. Valitse **Uusi**-toiminto, kun haluat syöttää myyntisykliin uuden vaiheen.

Toista nämä vaiheet ja määritä myyntisyklille niin monta vaihetta kuin haluat.

## <a name="to-assign-stage-cycles-to-opportunities"></a>Syklin vaiheiden määrittäminen mahdollisuuksille
Kun olet lisännyt mahdollisuuksien myyntisyklin, voit lisätä myyntimahdollisuuksia ja liittää mahdollisuuksiin vaiheen syklin määrittämällä **Myyntisyklin koodi** -kentän. Lisätietoja on kohdassa [Myyntimahdollisuuksien luominen](marketing-how-create-opportunities.md).

## <a name="to-set-up-activities-with-tasks"></a>Tehtäviä sisältävien toimintojen määrittäminen
Voit yhdistää toiminnoissa useita tehtäviä, kuten kutakin vaihetta koskeva tehtävän. Toiminnon tehtävät liittyvät toisiinsa päivämääräkaavan avulla. Voit määrittää toimintoja mahdollisuuksille, myyjille tai kontakteille.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimenpiteet** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto ja täytä tarvittavat kentät.
3. Täytä **Rivit**-pikavälilehdessä kentät, joilla määritetään vähintään yksi toiminnon tehtävä.

## <a name="to-assign-tasks-or-activities-of-tasks-to-opportunities"></a>Tehtävien tai tehtävätoimintojen määrittäminen mahdollisuuksiin
Kun ole määrittänyt tehtävän, voit määrittää sen myyntimahdollisuudelle ja siten toiminnon, jolle tehtävä kuuluu.

> [!NOTE]  
>   Tässä menettelyssä toimintotehtävät määritetään mahdollisuuksille. Tehtävät määritetään myyjille ja kontakteille vastaavasti.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Mahdollisuudet** ja valitse sitten liittyvä linkki.
2. Valitse ensin mahdollisuus ja sitten **Tehtävät**-toiminto.
3. Valitse **Tehtäväluettelo**-sivulla **Luo tehtävä** -toiminto.
4.  Täytä **Luo tehtävä** -sivulla tarvittavat kentät.

    Huomaa, että **Mahdollisuus**-kenttä on määritetty automaattisesti kyseiselle mahdollisuudelle.
5. Valitse **OK**-painike.
6. Valitse **Tehtäväluettelo**-sivulla ensin uusi tehtävä ja sitten **Määritä aktiviteetit** -toiminto.
7. Täytä **Määritä aktiviteetti** -sivulla tarvittavat kentät ja valitse sitten **OK**-painike.

## <a name="see-also"></a>Katso myös
[Myyntimahdollisuuksien käsitteleminen](marketing-processing-sales-opportunities.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
