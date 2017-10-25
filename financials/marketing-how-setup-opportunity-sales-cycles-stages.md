---
title: "Mahdollisuuden myyntisyklien ja syklin vaiheiden määrittäminen| Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten myynnin vaiheet määritetään ensimmäisestä yhteysotosta sulkemiseen ja miten tällä tavoin luodaan myyntisykli, joka määritetään Financialsin mahdollisuuksille."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 29f9caa8f01fe8e4cfd0f65cc290d82a49fb36bb
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-opportunity-sales-cycles-and-cycle-stages"></a>Toimintaohje: Mahdollisuuden myyntisyklien ja syklin vaiheiden määrittäminen
Myyntisyklit ja myyntisyklin vaiheet on määritettävä ennen myyntimahdollisuuksien käyttöönottoa. Myyntisykli muodostuu vaiheista alkuperäisestä yhteydenotosta aina kaupantekoon asti. Jokaisella vaiheella on tietyt vaatimukset, jotka on täytettävä, esimerkiksi myyntitarjouksen vaatiminen ennen mahdollisuuden siirtämistä seuraavaan vaiheeseen. Voit myös määrittää, voiko vaiheen ohittaa. Voit määrittää tarvittavan määrän myyntisyklejä ja niille haluamasi määrän myyntisyklien vaiheita.

Mahdollisuuden myyntisyklien ottaminen käyttöön sisältää myyntisyklin määrittämisen, syklin eri vaiheiden määrittämisen ja syklin liittämisen mahdollisuuksiin. Liittyvän toiminnon tai tehtävien määrittäminen mahdollisuuteen voi olla myös osa myyntisyklin määrittämistä.

Tässä ohjeaiheessa kerrotaan, miten tehtävät ja toiminnot määritetään ja miten toiminnoille määritetään tehtäviä. Lisätietoja on kohdassa Tehtäviä sisältävien toimintojen määrittäminen.

## <a name="to-set-up-opportunity-sales-cycle-codes"></a>Mahdollisuuden myyntisyklin koodien määrittäminen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntisyklit** ja valitse sitten aiheeseen liittyvä linkki. Kaikki olemassa olevat myyntisyklit sisältävä **Myyntisyklit**-ikkuna avautuu.
2. Valitse **Uusi**-toiminto ja täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Toista nämä vaiheet ja luo niin monta myyntijaksoa kuin haluat. Kun olet määrittänyt mahdollisuuden myyntikoodit, haluat ehkä määrittää kunkin syklin eri vaiheet.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Mahdollisuuden myyntisyklin vaiheiden määrittäminen
1. Valitse **Myyntisyklit**-ikkunassa mahdollisuuden myyntisykli, jolle haluat määrittää vaiheet. Valitse sitten **Vaiheet**-toiminto. **Myyntisyklin vaiheet** -ikkuna avautuu.
2. Valitse **Uusi**-toiminto, kun haluat syöttää myyntisykliin uuden vaiheen.

Toista nämä vaiheet ja määritä myyntisyklille niin monta vaihetta kuin haluat.

## <a name="to-assign-stage-cycles-to-opportunities"></a>Syklin vaiheiden määrittäminen mahdollisuuksille
Kun olet lisännyt mahdollisuuksien myyntisyklin, voit lisätä myyntimahdollisuuksia ja liittää mahdollisuuksiin vaiheen syklin määrittämällä **Myyntisyklin koodi** -kentän. Lisätietoja on kohdassa [Toimintaohje: Myyntimahdollisuuksien luominen](marketing-how-create-opportunities.md).

## <a name="to-set-up-activities-with-tasks"></a>Tehtäviä sisältävien toimintojen määrittäminen
Voit yhdistää toiminnoissa useita tehtäviä, kuten kutakin vaihetta koskeva tehtävän. Toiminnon tehtävät liittyvät toisiinsa päivämääräkaavan avulla. Voit määrittää toimintoja mahdollisuuksille, myyjille tai kontakteille.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntisyklit** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Uusi**-toiminto ja täytä tarvittavat kentät.
3. Täytä **Rivit**-pikavälilehdessä kentät, joilla määritetään vähintään yksi toiminnon tehtävä.

## <a name="to-assign-tasks-or-activities-of-tasks-to-opportunities"></a>Tehtävien tai tehtävätoimintojen määrittäminen mahdollisuuksiin
Kun ole määrittänyt tehtävän, voit määrittää sen myyntimahdollisuudelle ja siten toiminnon, jolle tehtävä kuuluu.

> [!NOTE]  
>   Tässä menettelyssä toimintotehtävät määritetään mahdollisuuksille. Tehtävät määritetään myyjille ja kontakteille vastaavasti.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Mahdollisuudet** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse ensin mahdollisuus ja sitten **Tehtävät**-toiminto.
3. Valitse **Tehtäväluettelo**-ikkunassa **Luo tehtävä** -toiminto.
4.  Täytä **Luo tehtävä** -ikkunassa tarvittavat kentät.

    Huomaa, että **Mahdollisuus**-kenttä on määritetty automaattisesti kyseiselle mahdollisuudelle.
5. Valitse **OK**-painike.
6. Valitse **Tehtäväluettelo**-ikkunassa ensin uusi tehtävä ja sitten **Määritä aktiviteetit** -toiminto.
7. Täytä **Määritä aktiviteetti** -ikkunassa tarvittavat kentät ja valitse sitten **OK**-painike.

## <a name="see-also"></a>Katso myös
[Myyntimahdollisuuksien käsitteleminen](marketing-processing-sales-opportunities.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

