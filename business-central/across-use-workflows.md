---
title: Työnkulkujen käyttäminen
description: Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät liiketoimintaprosessin tehtäviä, kuten automaattisen kirjaamisen tai uusien tietueiden hyväksynnän pyytämisen ja myöntämisen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 51079e65deda165869d946b5efc11da85fb720e4
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6446517"
---
# <a name="using-workflows"></a>Työnkulkujen käyttäminen

Työnkulku on tehtäväsarja, joka käynnistyy toiminnon, ehdon tai säännön seurauksena. Työnkulut toteutetaan yleensä liiketoimintalogiikan integroimiseksi organisaatioon, esimerkkeinä tehtävien erottelu, prosessien yhdistäminen tai luottamuksen ja vastuualueiden lisääminen.  

Työnkulut on suunniteltu luomaan uuden arvon hyväksymispyyntöjä ja pitämään vanha arvo, jos pyyntöä ei hyväksytä. Uusi arvo otetaan käyttöön vasta, kun viimeinen pyyntö on hyväksytty.  

Liiketoimintalogiikka voi olla seuraavien hyväksyminen:

- Uudet päätiedot, kuten KP-tilit, asiakkaat, toimittajat tai nimikkeet
- Muutokset aiemmin luotujen tietueiden kenttiin, jotka sisältävät luottamuksellista tietoa, kuten **Toimittajan pankkitilin nro** tai **Asiakkaan luottoraja**
- Muutokset aiemmin luotujen tietueiden kenttiin, jotka sisältävät liiketoiminnan kannalta kriittisiä tietoja, kuten **Nimikkeen myyntihinnat**
- Uudet käyttäjät tai muutokset käyttöoikeuksiin
- Ostoasiakirjat
- Myyntiasiakirjat
- Saapuvat asiakirjat
- Talouden päiväkirjat ennen kirjausta

Seuraavassa kuvassa on esimerkki työnkulusta, jossa on käyttäjän käynnistämä peräkkäinen hyväksyntä. Työnkulun käynnistyttyä ensimmäiselle hyväksyjälle luodaan hyväksymispyyntö.  

![Kuva työnkulusta, jossa on peräkkäinen hyväksyntä.](media/Workflows/approval-flow.png)

Tässä esimerkissä ensimmäisen hyväksyjän on hyväksyttävä pyyntö ennen kuin pyyntö lähetetään seuraavalle hyväksyjälle. Jos ensimmäinen hyväksyjä ei hyväksy pyyntöä, pyyntö ei koskaan siirry seuraavalle hyväksyjälle.  

Työnkulun ensimmäisestä käynnistämisestä alkanut reitti voi vaihdella hyväksynnän luonteen mukaan.  

Seuraavassa kuvassa on käyttäjän käynnistämä rinnakkaishyväksyntä. Työnkulun käynnistyttyä kaikille hyväksyjille lähetetään hyväksymispyyntö samanaikaisesti.  

![Kuva työnkulusta, jossa on rinnakkaishyväksyntä.](media/Workflows/approval-flow-2.png)

Työnkulkua ei kuitenkaan hyväksytä, ennen kuin hyväksyjät ovat hyväksyneet kaikki pyynnöt, kuten seuraava kuva esittää:  

![Kuva hylätystä työnkulusta, jossa on rinnakkaishyväksyntä.](media/Workflows/approval-flow-3.png)

> [!NOTE]  
> Ei ole mahdollista luoda useita hyväksyjiä sisältävää työnkulkua ja odottaa, että koko työnkulku hyväksytään, kun ensimmäinen pyyntö on hyväksytty. Kaikki pyynnöt on hyväksyttävä, jotta työnkulku voidaan hyväksyä.

Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamista liiketoimintaprosessin tehtäviä. On myös mahdollista luoda sama työnkulku useammin kuin kerran. Jokainen tapahtuman käynnistämä työnkulku, jossa käytetään eri suodattimia. Tästä on hyötyä, jos yhden osaston hyväksymispyynnön on oltava yhden hyväksyjän hyväksymä, kun taas toisen hyväksyjän on hyväksyttävä muiden osastojen hyväksymispyynnöt. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita.  

 Ennen kuin voit aloittaa työnkulkujen käyttämisen, sinun on määritettävä työnkulun käyttäjät, luotava työnkulut ja tehtävä mahdolliset koodin mukautukset, ja määritettävä miten käyttäjät saavat ilmoituksia. Lisätietoja on kohdassa [Työnkulkujen määrittäminen](across-set-up-workflows.md).  

> [!NOTE]  
> Tavalliset työnkulun osavaiheet liittyvät käyttäjiin, jotka pyytävät hyväksyntää tehtäville, ja hyväksyjiin, jotka hyväksyvät tai hylkäävät pyynnöt. Tämän vuoksi monet työnkulkuihin liittyvät ohjeaiheet liittyvät hyväksyntään.  

 Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.  

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Määritä työnkulku alkamaan, kun ensimmäinen merkitsevä tapahtuma toteutuu.|[Työnkulkujen ottaminen käyttöön](across-how-to-enable-workflows.md)|  
|Pyydä tehtävän hyväksyntää, ja hyväksyjänä voit hyväksyä, hylätä tai delegoida hyväksyntöjä sekä lähettää tai tarkastella hyväksyntäilmoituksia.|[Hyväksymistyönkulkujen käyttäminen](across-how-use-approval-workflows.md)|  
|Luo työnkulun vaiheet, jotka rajoittavat tiettyjen tietuetyyppien käyttöä ennen kuin tietty tapahtuma tapahtuu, esimerkiksi, että tietue on hyväksytty.|[Tietueen käytön rajoittaminen ja salliminen](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|Tarkastele Valmis-tilassa olevia työnkulun osavaiheita.|[Arkistoitujen työnkulun osavaiheen ilmentymien tarkasteleminen](across-how-to-view-archived-workflow-step-instances.md)|  
|Poista työnkulku, joka ei ole enää käytössä.|[Työnkulkujen poistaminen](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a>Katso myös  
[Työnkulkujen määrittäminen](across-set-up-workflows.md)   
[Työnkulku](across-workflow.md)   
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]