---
title: Pankin viitetiedostojen määrittäminen
description: Elektronisten maksujen käsittelyä varten on ensin määritettävä pankin viitetiedostot, joiden avulla määritetään, miten maksutiedot tuodaan tai viedään.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0d073b4785fe20ecb369a21f7ce5f282dd82fa76
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920170"
---
# <a name="set-up-bank-reference-files"></a>Pankin viitetiedostojen määrittäminen
Elektronisten maksujen käsittelyä varten on ensin määritettävä pankin viitetiedostot, joiden avulla määritetään, miten maksutiedot tuodaan tai viedään.  

## <a name="to-set-up-a-bank-reference-file"></a>Pankin viitetiedoston määrittäminen  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Pankin viitetiedoston asetukset** ja valitse sitten liittyvä linkki.  
2.  Täytä **Yleinen**-pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Ei.**|Määrittää pankkitilin koodin.|  
    |**Kohdistettujen hyvityslaskujen tiedot**|Kun valitset tämän, laskuihin kohdistetut hyvitykset näkyvät maksun vastaanottajan tiliotteessa.|  

3.  Täytä **Ulkomaan maksut** -pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]