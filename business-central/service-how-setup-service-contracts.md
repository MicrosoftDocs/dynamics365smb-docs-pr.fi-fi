---
title: Huoltosopimusten määrittäminen
description: Lue, miten voit määrittää huoltosopimuksia, joilla on vaaditut edellytykset, kuten huoltosopimusryhmät, sopimusmallit ja asiakasmallit.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 19e728ddf5394ad116cfc05eefecaec9d3e46871
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8132600"
---
# <a name="set-up-service-contracts"></a>Huoltosopimusten määrittäminen
Seuraavat on määritettävä, ennen kuin sopimuksia voi käyttää: 

* **Huoltosopimusryhmät** kerää yhteen toisiinsa jollain tavoin liittyvät huoltosopimukset.
* **Huoltosopimuksen tiliryhmiä** käytetään ryhmittelemään yhteen huoltosopimuksille luotujen huoltolaskujen huoltosopimustilit. Voit määrittää nämä ryhmät huoltosopimuksille.  
* **Sopimusmallit** määrittävät sopimusten asettelut sopimuksille, jotka sisältävät yleisimmin käytetyt huoltosopimusten tiedot. Kun luot huoltosopimustarjouksia, voit luoda ne käyttämällä malleja. Kun luot sopimustarjouksen, kentissä on automaattisesti mallikenttien sisältö.
* **Asiakasmallien** avulla voit luoda tarjouksia yhteyshenkilöille tai mahdollisille asiakkaille, joita ei ole rekisteröity asiakkaiksi [!INCLUDE[prod_short](includes/prod_short.md)]issa.  

## <a name="to-set-up-a-service-contract-group"></a>Huoltosopimusryhmien määrittäminen  
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltosopimusryhmät** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Valitse **Alennus vain sopimustil.** -valintaruutu, jos haluat, että sopimus- tai huoltoalennukset ovat voimassa vain sopimushuoltotilauksille, kuten ylläpidolle.  

## <a name="to-set-up-a-service-contract-account-group"></a>Huoltosopimusten tiliryhmien määrittäminen  
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltosopimuksen tiliryhmät** ja valitse sitten vastaava linkki.  
2. Luo uusi huoltosopimuksen tiliryhmä.   
3. Täytä **Koodi**- ja **Kuvaus**-kentät. Nämä kentät muodostavat huoltotiliryhmän kuvauksen.  
4. Täytä  **Ei ennak. maksettu sop. tili** -kenttä ja valitse muiden kuin ennakkoon maksettujen sopimusten tilin KP-tilinumero.  
5. Valitse **Ennak.maksetun sopimuksen tili** -kentässä ennakkoon maksettujen sopimusten tilin KP-tilinumero.  

## <a name="to-set-up-a-contract-template"></a>Sopimusmallien määrittäminen  
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltosopimusmallit** ja valitse sitten vastaava linkki.  
2. Luo uusi huoltosopimusmalli.  
3. Valitse **Nro**-kenttään sopimusmallin numero.  
  
     Vaihtoehtoisesti, jos olet määrittänyt sopimusmalleille numerosarjan **Huoltohallinnon asetukset** -sivulla, voit painaa Enter-painiketta, niin ohjelma lisää seuraavan saatavilla olevan sopimusmallin numeron. Täytä muut kentät tarpeen mukaan.  
  
4. Täytä **Lasku**-pikavälilehden **Huoltosop. tilir.koodi** -kenttään **laskutuskausi** ja muut tiedot. Täytä muut kentät tarpeen mukaan.  
5. Lisää sopimusalennukset valitsemalla **Huoltoalennukset**-toiminto.  

## <a name="to-set-up-a-customer-template"></a>Asiakasmallien määrittäminen  
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakasmallit** ja valitse sitten vastaava linkki.  
2. Luo uusi asiakasmallin kortti.  
3. Anna **Yleinen**-pikavälilehden **Koodi**- ja **Kuvaus**-kentissä asiakasmallin koodi ja kuvaus. 
4. Määritä hakuehdot täyttämällä muut kentät, kuten **Maa-/aluekoodi**, **Territorion koodi** ja **Kielikoodi**.  
5. Täytä **Yleinen liiketoim. kirjausryhmä**- ja **Asiakkaan kirjausryhmä** -kentät.  

## <a name="see-also"></a>Katso myös
[Huoltohallinnon määrittäminen](service-setup-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]