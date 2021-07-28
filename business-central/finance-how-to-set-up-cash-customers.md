---
title: Käteisasiakkaiden määrittäminen
description: Tässä aiheessa kuvataan vaiheet, joita tarvitaan laskun määrittämiseen asiakasnumerolla käteisellä maksavia asiakkaita varten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 9462b7bb887b5c4d2dcc0f602d5cd0fe57ccc1fb
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6442083"
---
# <a name="set-up-cash-customers"></a>Käteisasiakkaiden määrittäminen
Laskua ei voi luoda ilman asiakasnumeroa. Näin on, vaikka teet käteismyynnin, eikä asiakastilille ole mitään tallennettavaa.  

## <a name="to-set-up-a-cash-customer"></a>Käteisasiakkaiden määrittäminen  
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakas** ja valitse sitten vastaava linkki.  
2.  Luo uusi **Asiakkaan** kortti. Lisätietoja on kohdassa [Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md).
3.  Valitse **Nro**-kenttään esimerkiksi **Käteismyynti**.  
4.  Syötä **Nimi**-kenttään esimerkiksi **Käteismyynti**.  
5.  Täytä **Laskutus**-pikavälilehden **Asiakkaan kirjausryhmä**- ja **Ylein. liiketoim. kirjausryhmä** -kentät.  

 Nyt asiakas on määritetty, ja se sisältää riittävästi tietoa laskutusta varten.  

> [!NOTE]  
>  Olet voinut valita kirjausryhmän, jota on käytetty myös kotimaisiin luottomyynteihin. Jos haluat ylläpitää erillistä tietoa käteismyynneistä esimerkiksi erityisellä myynti- tai myyntisaamistilillä, voit määrittää tätä varten ylimääräisen kirjausryhmän.  
>   
>  Myyntisaamistilille täytyy syöttää numero kirjausryhmää varten, vaikka tilin saldo on aina 0 laskun kirjaamisen jälkeen.  

## <a name="see-also"></a>Katso myös
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md)    
[Rahoitus](finance.md)  



[!INCLUDE[footer-include](includes/footer-banner.md)]