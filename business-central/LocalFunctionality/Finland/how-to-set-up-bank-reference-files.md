---
title: Pankin viitetiedostojen määrittäminen (FI)
description: Elektronisten maksujen käsittelyä varten suomalaisessa versiossa on ensin määritettävä pankin viitetiedostot, joiden avulla määritetään, miten maksutiedot tuodaan tai viedään.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 32000000, 32000001, 32000002, 32000004, 32000005, 32000006
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bba3d461cb9b11a3a1bd2c71376e98c9e71814f4
ms.sourcegitcommit: c05806689d289d101bd558696199cefbd989473e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2022
ms.locfileid: "8115023"
---
# <a name="set-up-bank-reference-files-in-the-finnish-version"></a>Pankin viitetiedostojen määrittäminen suomalaisessa versiossa
Elektronisten maksujen käsittelyä varten on ensin määritettävä pankin viitetiedostot, joiden avulla määritetään, miten maksutiedot tuodaan tai viedään.  

## <a name="to-set-up-a-bank-reference-file"></a>Pankin viitetiedoston määrittäminen  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankin viitetiedoston asetukset** ja valitse sitten vastaava linkki.  
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