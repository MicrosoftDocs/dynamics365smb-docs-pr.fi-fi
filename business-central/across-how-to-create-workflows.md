---
title: Työnkulkujen luominen | Microsoft Docs
description: Voit luoda työnkulkuja, jotka yhdistävät eri käyttäjien suorittamia liiketoimintaprosessin tehtäviä. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0db0e2e6705a7d2fd1907227996d8c258dcbc554
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754790"
---
# <a name="create-workflows"></a>Työnkulkujen luominen
Voit luoda työnkulkuja, jotka yhdistävät eri käyttäjien suorittamia liiketoimintaprosessin tehtäviä. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita.  

Voit luoda **Työnkulku**-sivulla työnkulun mainitsemalla liittyvät toimet riveillä. Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta ja vastausvaihtoehdoista. Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita.  

Kun luot työnkulkuja, voit kopioida vaiheet aiemmin luoduista työnkuluista tai työnkulkumalleista. Työnkulkumallit ovat yleisen [!INCLUDE[prod_short](includes/prod_short.md)] -version työnkulkuja, joita ei voi muokata. Työnkulkumallien koodit, jotka Microsoft on lisännyt, sisältävät etuliitteen "MS-", kuten "MS-PIW". Lisätietoja on kohdassa [Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md).  

Jos liiketoimintaskenaario edellyttää työnkulun tapahtumia tai vastauksia, joita ei ole tuettu, Microsoft-kumppanin on toteutettava se mukauttamalla sovelluksen koodia.  

> [!NOTE]  
>  Kaikki työnkulun osavaiheiden ilmoitukset lähetetään työjonon kautta. Varmista, että asennuksen työjono on määritetty käsittelemään työnkulun ilmoituksia ja **Käynnistä automaattisesti NAS:stä** -valintaruutu on valittuna. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).  

## <a name="to-create-a-workflow"></a>Työnkulun luominen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvake, syötä **Työnkulut** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi**-toiminto. **Työnkulku**-sivu avautuu.  
3. Anna **Koodi**-kentässä enintään 20 merkkiä pitkä työnkulun tunniste.  
4. Voit luoda työnkulun työnkulkumallista valitsemalla **Työnkulut**-sivulla **Luo työnkulku mallista** -toiminnon. Lisätietoja on kohdassa [Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md).  
5. Syötä **Kuvaus**-kenttään työnkulun kuvaus.  
6. Määritä **Luokka**-kentässä, mihin luokkaan työnkulku kuuluu.  
7. Määritä **Kun - tapahtuma** -kentässä tapahtuma, jonka on tapahduttava, jotta työnkulun vaihe käynnistyy.  

    Kun valitset kentän, **Työnkulkutapahtumat**-sivu avautuu. Valinta tehdään tällä sivulla kaikista olemassa olevista työnkulun tapahtumista.  
8. Määritä **Ehto**-kentässä vähintään yksi ehto, jonka on toteuduttava, ennen kuin **Kun - tapahtuma**-kentän tapahtuma voi tapahtua.  

    Kun valitset kentän, **Tapahtuman ehdot** -sivu avautuu, jossa voit valita suodatinten luettelosta kentät, jotka liittyvät ehtoina kyseiseen tapahtumaan. Voit lisätä uusia suodatuskenttiä, joita haluat käyttää tapahtuman ehtoina. Voit määrittää tapahtuman ehtosuodattimet aivan kuin asetat suodattimet raportin pyyntösivuilla.  

    Jos työnkulun tapahtuma on muutos tietyssä tietueen kentässä, myös **tapahtuma edellytykset** -sivu avautuu, jossa voit valita kentän ja muutoksen tyyppi.  

    1.  Voit määrittää tapahtuman kentän muutoksen **Tapahtuman ehdot** -sivulla **Kenttä**-kentässä valitsemalla kentän, joka muuttuu.  
    2.  **Operaattori** -kentässä, valitse joko **Pienentynyt**, **Suurentunut** tai **Muuttunut**.  
9. Määritä **Sitten - vastaus** -kentässä vastaus, joka seuraa, kun työnkulun tapahtuma toteutuu.  

     Kun valitset kentän, **Työnkulun vastaukset** -sivu avautuu. Voit valita tällä sivulla kaikki olemassa olevat työnkulun vastaukset ja määrittää vastausvaihtoehdot valitulle vastaukselle.  
10. Määritä **Valitun vastauksen vaihtoehdot** -pikavälilehdessä työnkulun vastauksen asetukset valitsemalla arvoja eri kenttiin, jotka näkyvät, seuraavasti:  

    1.  Määritä työnkulun vastauksen asetukset, johon sisältyy ilmoitusten lähettäminen, täyttämällä kentät seuraavassa taulukossa kuvatulla tavalla.  

        |Kenttä|Kuvaus|  
        |----------------------------------|---------------------------------------|  
        |**Ilmoita lähettäjälle**|Määrittää, ilmoitetaanko hyväksymispyynnön vastaanottajan asemesta hyväksynnän pyytäjälle. Jos valitset valintaruudun, **Vastaanottajan käyttäjätunnus** -kenttä on poissa käytöstä, koska hyväksynnän pyytäjälle eli lähettäjälle ilmoitetaan sen sijaan. Työnkulun vastauksen nimi muuttuu vastaavasti nimeksi **Luo ilmoitus &lt;lähettäjälle&gt;**. Jos valintaruutua ei ole valittu, työnkulun vastauksen nimi on **Luo ilmoitus &lt;käyttäjälle&gt;**.
        |**Vastaanottajan käyttäjätunnus**|Määritä käyttäjä, jolle ilmoitus on lähetettävä. Huomautus: Tämä vaihtoehto on käytettävissä vain työnkulun vastauksissa, joissa on paikkamerkki kyseiselle käyttäjälle. Työnkulun vastaukset ilman paikkamerkkiä käyttäjille, ilmoituksen vastaanottaja määritetään yleensä hyväksyjäkäyttäjän asetuksissa.|  
        |**Ilmoitustapahtuman tyyppi**|Määrittää, käynnistääko työnkulun ilmoituksen tietueiden muutos, hyväksymispyyntö vai välitetyt erääntyvät tiedot.|
        |**Linkin kohdesivu**|Määritä [!INCLUDE[prod_short](includes/prod_short.md)]issa toinen sivu, jonka ilmoituksen linkki avaa oletussivun sijaan.<br /><br />Huomaa, että sivulla on oltava sama lähdetaulukko kuin tietueella.|  
        |**Mukautettu linkki**|Määritä sen linkin URL-osoite, joka lisätään ilmoitukseen [!INCLUDE[prod_short](includes/prod_short.md)]in sivulle vievän linkin lisäksi.|  
    2.  Määritä työnkulun vastauksen asetukset, johon sisältyy hyväksymispyynnön luominen, täyttämällä kentät seuraavassa taulukossa kuvatulla tavalla.  

        |Kenttä|Description|  
        |----------------------------------|---------------------------------------|  
        |**Eräpäivän kaava**|Määritä, kuinka monen päivän kuluessa lähettämisestä hyväksyntäpyyntö on ratkaistava.|  
        |**Delegoi seuraavan jälkeen:**|Määritä, milloin, jos ollenkaan, hyväksyntäpyyntö delegoidaan automaattisesti korvaajalle. Voit valita automaattisen delegoinnin yhden, kahden tai viiden päivän päähän hyväksynnän pyynnöstä.|  
        |**Hyväksyjän tyyppi**|Määritä, kuka on hyväksyjä, käyttäen hyväksyntäkäyttäjien ja työnkulun käyttäjien määritystä.<br /><br /> Käytettävissä ovat seuraavat vaihtoehdot:<br /><br /> -   **Myyjä/ostaja** määrittää, että **Myyjän/ostajan koodi** -kenttään **Hyväksynnän käyttäjäasetukset** -sivulla määritetty käyttäjä määrittää hyväksyjän. Hyväksymispyyntötapahtumat luodaan sitten **Hyväksyjän rajatyyppi** -kentän arvon mukaan.<br />     Lisätietoja on kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-workflow-users.md).|  
        |**Näytä vahvistussanoma**|Määritä, näytetäänkö vahvistussanoma käyttäjille, kun he pyytävät hyväksyntää.|  
        |**Hyväksyjän rajatyyppi**|Määritä, kuinka hyväksyjien hyväksyntärajat vaikuttavat silloin, kun hyväksyjille luodaan hyväksyntäpyyntöjä. Hyväksytyllä hyväksyjällä tarkoitetaan hyväksyjää, jonka hyväksyntäraja on suurempi kuin pyynnön arvo.<br /><br /> Käytettävissä ovat seuraavat vaihtoehdot:<br /><br /> 1. **Hyväksyjäketju** määrittää, että hyväksyntäpyynnöt luodaan kaikille pyytäjän hyväksyjille ensimmäiseen hyväksyttyyn hyväksyjään saakka.<br />2. **Suora hyväksyjä** määrittää, että hyväksyntäpyyntö luodaan vain pyytäjän lähimmälle hyväksyjälle hänen hyväksyntärajastaan riippumatta.<br />3. **Ensimmäinen hyväksytty hyväksyjä** määrittää, että hyväksyntäpyyntö luodaan vain pyytäjän ensimmäiselle hyväksytylle hyväksyjälle.<br />|  
    3.  Määritä työnkulun vastauksen asetukset, johon sisältyy päiväkirjarivien luominen, täyttämällä kentät seuraavassa taulukossa kuvatulla tavalla.  

        |Kenttä|Description|  
        |----------------------------------|---------------------------------------|  
        |**Yleisen päiväkirjan mallin nimi**|Määritä päiväkirjan malliin nimi, josta määritetyt päiväkirjarivit luodaan.|  
        |**Yleisen päiväkirjan erän nimi**|Määritä päiväkirjan erän nimi, josta määritetyt päiväkirjarivit luodaan.|  

11. Määritä osavaiheen sijainti työnkulussa sisentämällä **Kun**-kentässä olevan tapahtuman nimi **Suurenna sisennystä**- ja **Pienennä sisennystä** -painikkeilla.  
    1.  Osoita, että vaihe on seuraava työnkulun järjestyksessä sisentämällä sen nimi edellisen vaiheen alle.  
    2.  Osoita, että vaihe on yksi useammasta vaihtoehtoisesta vaiheesta, joka voi riippua sille asetetusta ehdosta asettamalla sen sisennys muiden vaihtoehtoisten vaiheiden tasolle. Aseta nämä vaihtoehtoiset vaiheet tärkeysjärjestykseen sijoittamalla tärkein ensimmäiseksi.  

    > [!NOTE]  
    >  Voit muuttaa ainoastaan sellaisen vaiheen sisennystä, jolla ei ole seuraavia vaiheita.  

12. Toista vaiheet 7–11, lisätäksesi työnkulun vaiheita joko ennen tai jälkeen juuri luomaasi vaihetta.  
13. Valitse **Käytössä**-valintaruutu määrittämään, että työnkulku alkaa heti ensimmäisen vaiheen **Aloituskohta**-tyyppisen tapahtuman toteuduttua. Lisätietoja on kohdassa [Työnkulkujen käyttäminen](across-use-workflows.md).  

> [!NOTE]  
>  Älä ota työnkulkua käyttöön, ennen kuin olet varma, että työnkulku on valmis ja siihen liittyvät osavaiheet voi aloittaa.  

> [!TIP]  
>  Jos haluat nähdä työnkulussa käytettävien taulukoiden väliset suhteet, valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake ja syötä **Työnkulku - taulukon suhteet**.  

## <a name="see-also"></a>Katso myös  
[Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md)   
[Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md)   
[Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md)   
[Arkistoitujen työnkulun osavaiheen ilmentymien tarkasteleminen](across-how-to-view-archived-workflow-step-instances.md)   
[Työnkulkujen poistaminen](across-how-to-delete-workflows.md)   
[Vaihekuvaus: Ostojen hyväksyntätyönkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Työnkulkujen määrittäminen](across-set-up-workflows.md)   
[Työnkulkujen käyttäminen](across-use-workflows.md)   
[Työnkulku](across-workflow.md)      
