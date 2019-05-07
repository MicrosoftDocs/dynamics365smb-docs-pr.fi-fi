---
title: Pankin viitetiedostojen määrittäminen
description: Elektronisten maksujen käsittelyä varten on ensin määritettävä pankin viitetiedostot, joiden avulla määritetään, miten maksutiedot tuodaan tai viedään.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6c94206b9260aff75fbc6d0bcae854737f40d67a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "932377"
---
# <a name="set-up-bank-reference-files"></a>Pankin viitetiedostojen määrittäminen
Elektronisten maksujen käsittelyä varten on ensin määritettävä pankin viitetiedostot, joiden avulla määritetään, miten maksutiedot tuodaan tai viedään.  

## <a name="to-set-up-a-bank-reference-file"></a>Pankin viitetiedoston määrittäminen  

1.  Valitse ![Etsi sivu tai raportti -kuvake](../../media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Pankin viitetiedoston asetukset** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Täytä **Yleinen**-pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Nro**|Määrittää pankkitilin koodin.|  
    |**Vie viitemaksut**|Anna vietävän maksutiedoston koko polku.|  
    |**Tuo viitemaksut**|Anna tuotavan maksutiedoston koko polku.|  
    |**Valuutan vaihtokurssitiedosto**|Anna valuutan vaihtokurssitiedoston koko polku.|  
    |**Kohdistettujen hyvityslaskujen tiedot**|Kun valitset tämän, laskuihin kohdistetut hyvitykset näkyvät maksun vastaanottajan tiliotteessa.|  

3.  Täytä **Ulkomaan maksut** -pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Vie ulkomaan maksut**|Anna ulkomaan pankkeihin vietävän maksutiedoston koko polku.|  
    |**Eräpäivän käsittely**|Määritä, miten eräpäivän käsittelyä käytetään ulkomaan maksuissa.<br /><br /> **Erä** – Kaikki tiedoston maksut saavat saman maksupäivämäärän.<br /><br /> -tai-<br /><br /> **Tapahtuma** – Jokainen tiedoston maksu saa tapahtumakohtaisen maksupäivämäärän. Kysy pankista lisätietoja tämän asetuksen käytöstä.|  
    |**Palvelumaksun oletuskoodi**|Valitse palvelumaksun oletuskoodi ulkomaan pankkeja varten.|  
    |**Oletusmaksutapa**|Valitse oletusmaksutapa ulkomaan pankkeja varten.|  
    |**Vaihtokurssin sopimusnro**|Anna vaihtokurssin sopimusnumero.|  
    |**Salli ulkomaan maksujen yhdistäminen**|Yhdistä kaikki yhdelle vastaanottajalle tietyn päivän aikana samalta pankkitililtä tehdyt ulkomaan maksut.|  

4.  Täytä **SEPA**-pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Pankin tunnus**|Anna SEPA-pankin tunnus. **Huomautus:** Tätä kenttää käytetään vain SEPA-standardissa pain.001.001.02.|  
    |**Tiedostonimi**|Anna SEPA-maksutiedoston koko polku. **Huomautus:** Tätä kenttää käytetään vain SEPA-standardissa pain.001.001.02.|  

    > [!IMPORTANT]  
    >  Voit viedä toimittajan maksut SEPA-standardin avulla, kun täytät **Maksun vientimuoto** -kentän **Pankkitilin kortti** -sivulla.  

5.  Valitse **OK**-painike.  

## <a name="see-also"></a>Katso myös  
 [Verkkopankkitoiminta Suomessa](electronic-banking-in-finland.md)   
 [Maksutiedostojen luominen](how-to-generate-payment-files.md)   
 [Maksualennusten ohittaminen](how-to-disregard-payment-discounts.md)
