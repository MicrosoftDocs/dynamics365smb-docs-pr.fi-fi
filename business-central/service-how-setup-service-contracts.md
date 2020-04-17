---
title: Huoltosopimusten määrittäminen | Microsoft Docs
description: Lisätietoja huoltosopimusten määrittämisestä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: f5dc45e6cc46d0a6aa6a4e1415108f801aef3040
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195145"
---
# <a name="set-up-service-contracts"></a>Huoltosopimusten määrittäminen
Seuraavat on määritettävä, ennen kuin sopimuksia voi käyttää: 

* **Huoltosopimusryhmät** kerää yhteen toisiinsa jollain tavoin liittyvät huoltosopimukset.
* **Huoltosopimuksen tiliryhmiä** käytetään ryhmittelemään yhteen huoltosopimuksille luotujen huoltolaskujen huoltosopimustilit. Voit määrittää nämä ryhmät huoltosopimuksille.  
* **Sopimusmallit** määrittävät sopimusten asettelut sopimuksille, jotka sisältävät yleisimmin käytetyt huoltosopimusten tiedot. Kun luot huoltosopimustarjouksia, voit luoda ne käyttämällä malleja. Kun luot sopimustarjouksen, kentissä on automaattisesti mallikenttien sisältö.
* **Asiakasmallien** avulla voit luoda tarjouksia yhteyshenkilöille tai mahdollisille asiakkaille, joita ei ole rekisteröity asiakkaiksi [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.  

## <a name="to-set-up-a-service-contract-group"></a>Huoltosopimusryhmien määrittäminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huoltosopimusryhmät** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Valitse **Alennus vain sopimustil.** -valintaruutu, jos haluat, että sopimus- tai huoltoalennukset ovat voimassa vain sopimushuoltotilauksille, kuten ylläpidolle.  

## <a name="to-set-up-a-service-contract-account-group"></a>Huoltosopimusten tiliryhmien määrittäminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huoltosopimuksen tiliryhmät** ja valitse sitten liittyvä linkki.  
2. Luo uusi huoltosopimuksen tiliryhmä.   
3. Täytä **Koodi**- ja **Kuvaus**-kentät. Nämä kentät muodostavat huoltotiliryhmän kuvauksen.  
4. Täytä  **Ei ennak. maksettu sop. tili** -kenttä ja valitse muiden kuin ennakkoon maksettujen sopimusten tilin KP-tilinumero.  
5. Valitse **Ennak.maksetun sopimuksen tili** -kentässä ennakkoon maksettujen sopimusten tilin KP-tilinumero.  

## <a name="to-set-up-a-contract-template"></a>Sopimusmallien määrittäminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huoltosopimusmallit** ja valitse sitten liittyvä linkki.  
2. Luo uusi huoltosopimusmalli.  
3. Valitse **Nro**-kenttään sopimusmallin numero.  
  
     Vaihtoehtoisesti, jos olet määrittänyt sopimusmalleille numerosarjan **Huoltohallinnon asetukset** -sivulla, voit painaa Enter-painiketta, niin ohjelma lisää seuraavan saatavilla olevan sopimusmallin numeron. Täytä muut kentät tarpeen mukaan.  
  
4. Täytä **Lasku**-pikavälilehden **Huoltosop. tilir.koodi** -kenttään **laskutuskausi** ja muut tiedot. Täytä muut kentät tarpeen mukaan.  
5. Lisää sopimusalennukset valitsemalla **Huoltoalennukset**-toiminto.  

## <a name="to-set-up-a-customer-template"></a>Asiakasmallien määrittäminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakasmallit** ja valitse sitten liittyvä linkki.  
2. Luo uusi asiakasmallin kortti.  
3. Anna **Yleinen**-pikavälilehden **Koodi**- ja **Kuvaus**-kentissä asiakasmallin koodi ja kuvaus. 
4. Määritä hakuehdot täyttämällä muut kentät, kuten **Maa-/aluekoodi**, **Territorion koodi** ja **Kielikoodi**.  
5. Täytä **Yleinen liiketoim. kirjausryhmä**- ja **Asiakkaan kirjausryhmä** -kentät.  

## <a name="see-also"></a>Katso myös
[Huoltohallinnon määrittäminen](service-setup-service.md)