---
title: Hyväksymistyönkulkujen käyttäminen
description: 'Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät liiketoimintaprosessin tehtäviä, kuten automaattisen kirjaamisen tai uusien tietueiden hyväksynnän pyytämisen ja myöntämisen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '1500, 1501, 1503, 1504, 1505'
ms.date: 09/13/2022
ms.author: bholtorf
---
# Hyväksymistyönkulkujen käyttäminen

Työnkulku on tehtäväsarja, joka käynnistyy toiminnon, ehdon tai säännön seurauksena. Työnkulut toteutetaan yleensä liiketoimintalogiikan integroimiseksi organisaatioon, esimerkkeinä tehtävien erottelu, prosessien yhdistäminen tai parhaiden käytäntöjen soveltaminen.

Työnkulut voidaan suunnitella luomaan tietuekentän muutoksen hyväksymispyyntöjä säilyttäen samalla vanhat tiedot siltä varalta, että pyyntöä ei hyväksytä. Uusi arvo otetaan käyttöön vasta, kun viimeinen pyyntö on hyväksytty.

Liiketoimintalogiikka voi olla seuraavien hyväksyminen:

- Uudet päätiedot, kuten pääkirjanpito (KP) -tilit, asiakkaat, toimittajat tai nimikkeet.
- Muutokset aiemmin luotujen tietueiden kenttiin, jotka sisältävät luottamuksellista tietoa, kuten **Toimittajan pankkitilin nro** tai **Asiakkaan luottoraja**.
- Muutokset aiemmin luotujen tietueiden kenttiin, jotka sisältävät liiketoiminnan kannalta kriittisiä tietoja, kuten **Nimikkeen myyntihinnat**.
- Uudet käyttäjät tai muutokset käyttöoikeuksiin.
- Ostoasiakirjat.
- Myyntiasiakirjat.
- Saapuvat asiakirjat.
- Talouden päiväkirjat ennen kirjausta.

Seuraava kuva on esimerkki työnkulusta, jossa on käyttäjän käynnistämä peräkkäinen hyväksyntä. Työnkulun käynnistyttyä ensimmäiselle hyväksyjälle luodaan hyväksymispyyntö.  

![Kuva työnkulusta, jossa on peräkkäinen hyväksyntä.](media/Workflows/approval-flow.png)

Yllä olevassa kuvassa näkyy, kuinka ensimmäisen hyväksyjän on hyväksyttävä pyyntö ennen kuin se lähetetään seuraavalle hyväksyjälle. Jos ensimmäinen hyväksyjä ei hyväksy pyyntöä, pyyntö ei koskaan siirry seuraavalle.

Työnkulun ensimmäisestä käynnistämisestä alkanut reitti voi vaihdella hyväksynnän luonteen mukaan.  

Seuraavassa kuvassa on käyttäjän käynnistämä rinnakkaishyväksyntä. Rinnakkainen hyväksyntä tarkoittaa sitä, että kaikille hyväksyjille lähetetään hyväksymispyyntö samanaikaisesti.  

![Kuva työnkulusta, jossa on rinnakkaishyväksyntä.](media/Workflows/approval-flow-2.png)

Työnkulku ei kuitenkaan ole päättynyt, ennen kuin kaikki pyynnöt on hyväksytty, kuten seuraava kuva esittää:  

![Kuva hylätystä työnkulusta, jossa on rinnakkaishyväksyntä.](media/Workflows/approval-flow-3.png)

> [!NOTE]  
> Jos työnkulussa on useita hyväksyjiä, kaikkien hyväksyjien on hyväksyttävä jokainen vaihe, ennen kuin työnkulku voi siirtyä seuraavaan tapahtumaan. Vain yhden hyväksyjän hyväksyntä ei siirrä työnkulkua eteenpäin.

Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamista liiketoimintaprosessin tehtäviä. On myös mahdollista luoda sama työnkulku useammin kuin kerran. Jokaisen työnkulun voi käynnistää käyttämällä erilaisia käynnistimiä. Tämä on hyödyllistä, jos yhden osaston hyväksyntäpyynnön on hyväksyttävä yksi hyväksyjä, kun taas muiden osastojen pyynnöt on hyväksyttävä eri hyväksyjällä. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita.  

Ennen kuin voit aloittaa työnkulkujen käyttämisen, sinun on määritettävä työnkulun käyttäjät, luotava työnkulut, (tehtävä mahdolliset koodin mukautukset), ja määritettävä miten käyttäjät saavat ilmoituksia. Lisätietoja kohdassa [Työnkulkujen määrittäminen](across-set-up-workflows.md).

> [!NOTE]  
> Tavalliset työnkulun osavaiheet liittyvät käyttäjiin, jotka pyytävät hyväksyntää tehtäville, ja hyväksyjiin, jotka hyväksyvät tai hylkäävät pyynnöt. Tämän vuoksi monet työnkulkuihin liittyvät ohjeaiheet liittyvät hyväksyntään.  

 Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin artikkeleihin.  

| **Tehtävä** | **Katso** |
|--|--|
| Määritä hyväksyntätyönkulku alkamaan, kun ensimmäinen merkitsevä tapahtuma toteutuu. | [Hyväksymistyönkulkujen ottaminen käyttöön](across-how-to-enable-workflows.md) |
| Pyydä tehtävän hyväksyntää, ja hyväksyjänä voit hyväksyä, hylätä tai delegoida hyväksyntöjä sekä lähettää tai tarkastella hyväksyntäilmoituksia. | [Toimintaohje: Hyväksyntätyönkulkujen käyttäminen](across-how-use-approval-workflows.md) |
| Luo työnkulun vaiheet, jotka rajoittavat tiettyjen tietuetyyppien käyttöä ennen kuin tietty tapahtuma tapahtuu, esimerkiksi, tietueen hyväksyntä. | [Tietueen käytön rajoittaminen ja salliminen](across-how-to-restrict-and-allow-usage-of-a-record.md) |
| Tarkastele **Valmis**-tilassa olevia työnkulun osavaiheita. | [Arkistoitujen työnkulun osavaiheen ilmentymien tarkasteleminen](across-how-to-view-archived-workflow-step-instances.md) |
| Poista hyväksyntätyönkulku, joka ei ole enää käytössä. | [Hyväksymistyönkulkujen poistaminen](across-how-to-delete-workflows.md) |

## Katso myös

[Hyväksymistyönkulkujen määrittäminen](across-set-up-workflows.md)  
[Työnkulku](across-workflow.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
