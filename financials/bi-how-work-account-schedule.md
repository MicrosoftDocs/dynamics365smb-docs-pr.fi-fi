---
title: "KP-raporttimallien kanssa työskentely| Microsoft Docs"
description: "Kuvailee, miten KP-raporttimalleja voidaan käyttää erilaisten näkymien ja raporttien luomiseen taloushallinnon suorituskykytietojen analysointia varten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7b28d3ec6f4a52c5229d2e121ff1fe8ed847eeb7
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-account-schedules"></a>KP-raporttimallien käyttäminen
Saat KP-raporttimallien avulla tietoja tilikarttaan sisältyvistä kirjanpitotiedoista. KP-raporttimallit analysoivat kirjanpitotilien lukuja ja vertaavat pääkirjanpidon tapahtumia pääkirjanpidon budjettitapahtumiin. Tulokset näkyvät roolikeskuksen kaavioissa, kuten kassavirtakaaviossa.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää käyttövalmiita KP-raporttimalleja. Voit myös määrittää itse verrattavat luvut määrittämällä omat rivit ja sarakkeet. Voit esimerkiksi luoda KP-raporttimalleja katteen laskemista varten erilaisille dimensioille, kuten osastoille tai asiakasryhmille. Voit luoda niin monta mukautettua rahoituslaskelmaa kuin haluat.  

KP-raporttimallien määrittäminen vaatii tilikartan taloustietojen ymmärtämistä. Voit esimerkiksi tarkastella pääkirjanpidon tapahtumia budjettitapahtumien prosenttiosuuksina. Tämä edellyttää, että budjetit on luotu. Lisätietoja on kohdassa [KP-budjettien luominen](finance-how-create-budgets.md).

## <a name="account-categories-and-account-schedules"></a>Tililuokat ja KP-raporttimallit
Tililuokkien avulla voit muuttaa rahoituslaskelmien asettelua. Kun olet määrittänyt tililuokat **KP-tilin luokat** -ikkunassa ja valinnut **Luo KP-raporttimallit** -toiminnon, tärkeimpien rahoituslaskelmien perustana olevat KP-raporttimallit päivitetään. Kun seuraavan kerran suoritat jonkin näistä raporteista, uudet kokonaissummat ja korvaustapahtumat lisätään muutosten perusteella. Lisätietoja on kohdassa [Pääkirjanpito ja tilikartta](finance-general-ledger.md).  

## <a name="to-create-new-account-schedules"></a>Uuden KP-raporttimallin luominen  
 KP-raporttimallien käyttäminen kirjanpitotilien lukujen analysoimista varten tai pääkirjanpidon tapahtumien vertaamiseksi pääkirjanpidon budjettitapahtumiin. Voit esimerkiksi tarkastella KP-tapahtumien prosenttiosuuksia budjettitapahtumista.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KP-raporttimallit** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **KP-raporttimallien nimet** -ikkunassa **Uusi**-toiminto ja luo uusi KP-raporttimallin nimi.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Valitse **Muokkaa KP-raporttimallia** -toiminto.
5. Täytä **KP-raporttimalli** -ikkunan kentät tarpeesi mukaan.  

    Kun olet luonut uuden KP-raporttimallin ja määrittänyt rivit sinun täytyy määrittää sarakkeet. Voit joko määrittää ne manuaalisesti tai liittää ennalta määrätyn sarakeasettelun KP-raporttimalliisi.
6. Valitse **Muokkaa sarakeasetuksia** -toiminto.
7. Täytä **Sarakeasettelu**-ikkunan kentät tarpeesi mukaan.

> [!NOTE]  
>   Jos KP-raporttimallin sarakeasettelun oletusarvoa ei määritetty, sarakkeet on määritettävä manuaalisesti.   

### <a name="to-create-a-column-that-calculates-percentages"></a>Prosenttilukuja laskevan sarakkeen luominen  
Joskus haluat ehkä sisällyttää KP-raporttimalliin sarakkeen, joka laskee prosenttiluvut kokonaissummasta. Jos esimerkiksi eri rivit jakavat myynnin dimensioittain, voit lisätä sarakkeen, joka ilmoittaa kunkin rivin prosenttiosuuden kokonaissummasta.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KP-raporttimallit** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **KP-raporttimallien nimet** -ikkunassa KP-raporttimalli.  
3. Valitse **Muokkaa KP-raporttimallia** -toiminto, jos haluat määrittää KP-raporttimallin rivin, joka laskee prosenttilukujen perustana olevan kokonaissumman.  
4. Lisää KP-raporttimalli-ikkunaan rivi välittömästi ensimmäisen sellaisen rivin yläpuolelle, jolla haluat näyttää prosenttiluvun.  
5. Täytä rivin kentät seuraavasti: valitse **Summaustyyppi**-kenttään **Määritä prosentin perusta**. Anna **Yhteensä**-kentässä kaava, jonka laskemaan kokonaissummaan prosenttiarvo perustuu. Jos esimerkiksi rivi 11 sisältää kokonaismyynnin, syötä **11**.  
6. Valitse **Muokkaa sarakeasetuksia** -toiminto, kun haluat määrittää sarakkeen.  
7. Täytä rivin kentät seuraavasti: valitse **Saraketyyppi**-kenttään **Kaava**. Anna **Kaava**-kenttään sen summan kaava, jolle haluat laskea prosentin, ja sen perää %-merkki. Jos esimerkiksi sarake N sisältää nettomuutoksen, syötä **N %**.  
8. Toista vaiheet 4-7 kullekin riviryhmälle, jonka haluat jakaa prosenttiluvun mukaan.

## <a name="to-set-up-account-schedules-with-overviews"></a>KP-raporttimallien määrittäminen käyttäen yleiskuvauksia  
KP-raporttimallin käyttäminen pääkirjanpidon lukuja ja pääkirjanpidon budjettilukuja vertaavan laskelman luomiseksi.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KP-raporttimallit** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **KP-raporttimallien nimet** -ikkunassa KP-raporttimalli.  
3. Valitse **Muokkaa KP-raporttimallia** -toiminto  
4. Valitse **KP-raporttimalli** -ikkunan **Nimi**-kentässä haluamasi KP-raporttimallin nimi.
5. Valitse **Syötä tilit** -toiminto.  
6. Valitse tilit, joita haluat ilmoitukseesi ja valitse sitten **OK**-painike.

    Tilit on nyt lisätty KP-raporttimalliin. Halutessasi voit myös muuttaa sarakeasettelua.  
7. Valitse **Yleiskuvaus**-toiminto.  
8. Valitse **Dimensiosuodattimet**-pikavälilehti ja määritä Budjettisuodatus-kentässä haluamasi suodattimen nimi.  
9. Valitse **OK**-painike.  

Nyt voit kopioida ja liittää budjettierittelyn laskentataulukkoon.

## <a name="see-also"></a>Katso myös
[Business Intelligence](bi.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

