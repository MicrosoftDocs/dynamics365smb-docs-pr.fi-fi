---
title: Työnkulkujen luominen tehtävien yhdistämista varten
description: Voit luoda työnkulkuja, jotka yhdistävät eri käyttäjien suorittamia liiketoimintaprosessin tehtäviä, ja sisällyttää järjestelmätehtäviä, esimerkiksi automaattisen kirjauksen, työnkulun osavaiheiksi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/30/2021
ms.author: edupont
ms.openlocfilehash: b4f6894c0d9c5a23445f70b2a50fcd677b17be66
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6438405"
---
# <a name="create-workflows-to-connect-business-process-tasks"></a>Työnkulkujen luominen liiketoimintaprosessin tehtävien yhdistämista varten

Voit luoda työnkulkuja, jotka yhdistävät eri käyttäjien suorittamia liiketoimintaprosessin tehtäviä. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita.  

Voit luoda **Työnkulku**-sivulla työnkulun mainitsemalla liittyvät toimet riveillä. Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta ja vastausvaihtoehdoista. Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita.  

Kun luot työnkulkuja, voit kopioida vaiheet aiemmin luoduista työnkuluista tai työnkulkumalleista. Työnkulkumallit ovat yleisen [!INCLUDE[prod_short](includes/prod_short.md)] -version työnkulkuja, joita ei voi muokata. Työnkulkumallien koodit, jotka Microsoft on lisännyt, sisältävät etuliitteen "MS-", kuten "MS-PIW". Lisätietoja on kohdassa [Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md).  

Jos liiketoimintaskenaario edellyttää työnkulun tapahtumia tai vastauksia, joita ei ole tuettu, Microsoft-kumppanin on toteutettava se luomalla laajennus, joka toteuttaa asiaankuuluvan työnkulkutapahtuman.  

> [!NOTE]  
> Kaikki työnkulun osavaiheiden ilmoitukset lähetetään työjonon kautta. Varmista, että työjono vastaa yrityksesi tarpeita. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).  

:::image type="content" source="media/Workflows/workflow-example.png" alt-text="Kuva työnkulun esimerkistä.":::

Työnkulku jakautuu kolmeen osaan:

1) **Kun - tapahtuma** Tässä valitaan käynnistin.
    Esimerkkejä käynnistimestä voivat olla:
    - Päätietojen tietuetta muutetaan
    - Päiväkirjaan luodaan rivi
    - saapuva asiakirja luodaan tai vapautetaan
    - Asiakirjan hyväksyntää pyydetään

2) **Ehto** **Ehdot** liittyvät tapahtumaan ja avautuvat suodattimien luomista varten, kun tapahtuma käynnistetään
3) **Sitten - vastaus** **Vastaukset** vastaavat siihen, mitkä työn seuraavat vaiheet ovat.

Molempien tapahtumatyyppien tapahtumat ovat järjestelmän määrittämiä. Uusien tapahtumien lisäämistä varten on kehitettävä laajennus.

## <a name="to-create-a-workflow"></a>Työnkulun luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulut** ja valitse sitten vastaava linkki.  
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

    1. Voit määrittää tapahtuman kentän muutoksen **Tapahtuman ehdot** -sivulla **Kenttä**-kentässä valitsemalla kentän, joka muuttuu.  
    2. **Operaattori** -kentässä, valitse joko **Pienentynyt**, **Suurentunut** tai **Muuttunut**.  
9. Määritä **Sitten - vastaus** -kentässä vastaus, joka seuraa, kun työnkulun tapahtuma toteutuu.  

     Kun valitset kentän, **Työnkulun vastaukset** -sivu avautuu. Voit valita tällä sivulla kaikki olemassa olevat työnkulun vastaukset ja määrittää vastausvaihtoehdot valitulle vastaukselle.  
10. Määritä **Valitun vastauksen vaihtoehdot** -pikavälilehdessä työnkulun vastauksen asetukset valitsemalla arvoja eri kenttiin, jotka näkyvät, seuraavasti:  

    1. Määritä työnkulun vastauksen asetukset, johon sisältyy ilmoitusten lähettäminen, täyttämällä kentät seuraavassa taulukossa kuvatulla tavalla.  

        |Kenttä|Kuvaus|  
        |-----|-----------|  
        |**Ilmoita lähettäjälle**|Määrittää, ilmoitetaanko hyväksymispyynnön vastaanottajan asemesta hyväksynnän pyytäjälle. Jos valitset valintaruudun, **Vastaanottajan käyttäjätunnus** -kenttä on poissa käytöstä, koska hyväksynnän pyytäjälle eli lähettäjälle ilmoitetaan sen sijaan. Työnkulun vastauksen nimi muuttuu vastaavasti nimeksi **Luo ilmoitus &lt;lähettäjälle&gt;**. Jos valintaruutua ei ole valittu, työnkulun vastauksen nimi on **Luo ilmoitus &lt;käyttäjälle&gt;**.
        |**Vastaanottajan käyttäjätunnus**|Määritä käyttäjä, jolle ilmoitus on lähetettävä. **Huomautus**: Tämä vaihtoehto on käytettävissä vain työnkulun vastauksissa, joissa on paikkamerkki kyseiselle käyttäjälle. Työnkulun vastaukset ilman paikkamerkkiä käyttäjille, ilmoituksen vastaanottaja määritetään yleensä hyväksyjäkäyttäjän asetuksissa.|  
        |**Ilmoitustapahtuman tyyppi**|Määrittää, käynnistääko työnkulun ilmoituksen tietueiden muutos, hyväksymispyyntö vai välitetyt erääntyvät tiedot.|
        |**Linkin kohdesivu**|Määritä toinen sivu, jonka ilmoituksen linkki avaa oletussivun sijaan. Huomaa, että sivulla on oltava sama lähdetaulukko kuin tietueella.|
        |**Mukautettu linkki**|Määritä sen linkin URL-osoite, joka lisätään ilmoitukseen sivulle vievän linkin lisäksi.|  

    2. Määritä työnkulun vastauksen asetukset, johon sisältyy hyväksymispyynnön luominen, täyttämällä kentät seuraavassa taulukossa kuvatulla tavalla.  

        |Kenttä|Description|  
        |-----|-----------|  
        |**Eräpäivän kaava**|Määritä, kuinka monen päivän kuluessa lähettämisestä hyväksyntäpyyntö on ratkaistava.|
        |**Delegoi seuraavan jälkeen:**|Määritä, milloin, jos ollenkaan, hyväksyntäpyyntö delegoidaan automaattisesti korvaajalle. Voit valita automaattisen delegoinnin yhden, kahden tai viiden päivän päähän hyväksynnän pyynnöstä.|
        |**Hyväksyjän tyyppi**|Määritä, kuka on hyväksyjä, käyttäen hyväksyntäkäyttäjien ja työnkulun käyttäjien määritystä. Kun kentän määritys on **Myyjä/ostaja**, asetus määrittää, että **Myyjän/ostajan koodi** -kenttään **Hyväksynnän käyttäjäasetukset** -sivulla määritetty käyttäjä määrittää hyväksyjän. Hyväksymispyyntötapahtumat luodaan sitten **Hyväksyjän rajatyyppi** -kentän arvon mukaan. Lisätietoja on kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-workflow-users.md).|
        |**Näytä vahvistussanoma**|Määritä, näytetäänkö vahvistussanoma käyttäjille, kun he pyytävät hyväksyntää.|
        |**Hyväksyjän rajatyyppi**|Määritä, kuinka hyväksyjien hyväksyntärajat vaikuttavat silloin, kun hyväksyjille luodaan hyväksyntäpyyntöjä. Hyväksytyllä hyväksyjällä tarkoitetaan hyväksyjää, jonka hyväksyntäraja on suurempi kuin pyynnön arvo. Seuraavat vaihtoehdot ovat käytössä: <ol><li>**Hyväksyjäketju** määrittää, että hyväksyntäpyynnöt luodaan kaikille pyytäjän hyväksyjille ensimmäiseen hyväksyttyyn hyväksyjään saakka.</li><li>**Suora hyväksyjä** määrittää, että hyväksyntäpyyntö luodaan vain pyytäjän lähimmälle hyväksyjälle hänen hyväksyntärajastaan riippumatta.</li><li>**Ensimmäinen hyväksytty hyväksyjä** määrittää, että hyväksyntäpyyntö luodaan vain pyytäjän ensimmäiselle hyväksytylle hyväksyjälle.</li></ol>|
    3. Määritä työnkulun vastauksen asetukset, johon sisältyy päiväkirjarivien luominen, täyttämällä kentät seuraavassa taulukossa kuvatulla tavalla.  

        |Kenttä|Description|  
        |-----|-----------|  
        |**Yleisen päiväkirjan mallin nimi**|Määritä päiväkirjan malliin nimi, josta määritetyt päiväkirjarivit luodaan.|  
        |**Yleisen päiväkirjan erän nimi**|Määritä päiväkirjan erän nimi, josta määritetyt päiväkirjarivit luodaan.|  

11. Määritä osavaiheen sijainti työnkulussa sisentämällä **Kun**-kentässä olevan tapahtuman nimi **Suurenna sisennystä**- ja **Pienennä sisennystä** -painikkeilla.  

    1. Osoita, että vaihe on seuraava työnkulun järjestyksessä sisentämällä sen nimi edellisen vaiheen alle.  
    2. Osoita, että vaihe on yksi useammasta vaihtoehtoisesta vaiheesta, joka voi riippua sille asetetusta ehdosta asettamalla sen sisennys muiden vaihtoehtoisten vaiheiden tasolle. Aseta nämä vaihtoehtoiset vaiheet tärkeysjärjestykseen sijoittamalla tärkein ensimmäiseksi.  

    > [!NOTE]  
    >  Voit muuttaa ainoastaan sellaisen vaiheen sisennystä, jolla ei ole seuraavia vaiheita.  

12. Toista vaiheet 7–11, lisätäksesi työnkulun vaiheita joko ennen tai jälkeen juuri luomaasi vaihetta.  
13. Valitse **Käytössä**-valintaruutu määrittämään, että työnkulku alkaa heti ensimmäisen vaiheen **Aloituskohta**-tyyppisen tapahtuman toteuduttua. Lisätietoja on kohdassa [Työnkulkujen käyttäminen](across-use-workflows.md).  

> [!NOTE]  
> Älä ota työnkulkua käyttöön, ennen kuin olet varma, että työnkulku on valmis ja siihen liittyvät osavaiheet voi aloittaa.  

> [!TIP]  
> Jos haluat nähdä työnkuluissa käytettävien taulukoiden väliset suhteet, valitse ![Kerro-ominaisuuden avaava hehkulamppu.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake ja syötä sitten **Työnkulku – Taulukon suhteet**.  

## <a name="example-of-creating-a-new-workflow-using-existing-events"></a>Esimerkki uuden työnkulun luomisesta aiemmin luotujen tapahtumien avulla

Seuraavassa esimerkissä tehdään uusi työnkulku, joka hyväksyy muutokset aiemmin luodun toimittajan nimeen:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulut** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto. **Työnkulku**-sivu avautuu.
3. Täytä työnkulkuosan kentät seuraavassa taulukossa kuvatulla tavalla.

    |Kenttä  |Arvo  |
    |---------|---------|
    |**Koodi**|**VENDAPN-01**|
    |**Kuvaus**|**Toimittajan nimen muutoksen hyväksyntä** |
    |**Luokka**|**OSTO**|

4. Voit luoda ensimmäisen työnkulun osavaiheen seuraavasti.

    1. Määritä **Kun - tapahtuma** -kentässä *Toimittajatietue muutetaan*.  
    2. Valitse **Ehto**-kentässä sana **Aina** ja valitse sitten **Tapahtuman ehdot** -sivulla **Lisää ehto, kun kentän arvo muuttuu** -linkki ja valitse sitten *Nimi*-kenttä.  

      Tämän vaiheen tulos on se, että ehto näkyy muodossa *Nimi muutetaan*.  
    3. Valitse **Sitten - vastaus** -kentässä **Valitse vastaus** -linkki ja valitse **Työnkulun vastaukset** -sivun **Valitse vastaus** -kentässä *Palauta <Field> kentän arvo tietueessa ja tallenna muutos* -vastaus ja määritä sitten **Valitun vastauksen asetukset** -osassa *Nimi*-kenttä.  
    4. Valitse **Lisää vastauksia** -linkki ja lisää sitten merkintä *Luo tietueelle hyväksyntäpyyntö käyttäen hyväksyjätyyppejä <%1> ja <%2>.* -vastaukselle.  
    5. Vaihda uuden vastauksen **Valitun vastauksen asetukset** -osassa **Hyväksyjätyyppi**-kenttä vaihtoehtoon *Työnkulun käyttäjäryhmä* ja määritä sitten **Työnkulun käyttäjäryhmä** -kentässä asiaankuuluva käyttäjäryhmä.  

    Lisätietoja on kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md).  
    6. Lisää kolmas vastaus: *Lähetä tietueen hyväksymispyyntö ja luo ilmoitus.*  
    7. Lisää neljäs vastaus nimellä *Näytä sanoma "%1"* ja määritä sitten **Valitun vastauksen asetukset** -osan sanomakentässä **Hyväksymispyyntö on lähetetty**.  
    8. Valitse OK-painike palataksesi työnkulun osavaiheeseen.  

5. Lisää seuraavalle riville uusi työnkulun osavaihe *Hyväksymispyyntö on hyväksytty.* -tapahtumalle.  

    1. Määritä **Kun - tapahtuma** -kenttään *Hyväksymispyyntö on hyväksytty*.  
    2. Valitse rivivalikko ja valitse sitten **Suurenna sisennystä**.  
    3. Valitse **Ehto** -kentässä sana **Aina** ja määritä sitten **Odottavat hyväksynnät** -kentässä *0*.  

      Tämän vaiheen tulos on se, että ehto näkyy muodossa *Odottavat hyväksynnät:0*, mikä osoittaa, että tämä on viimeinen hyväksyjä.  
    4. Valitse **Sitten - vastaus** -kentässä **Valitse vastaus** -linkki ja valitse sitten **Työnkulun vastaukset** -sivun **Valitse vastaus** -kentässä *Lähetä tietueen hyväksymispyyntö ja luo ilmoitus* -vastaus.  
    5. Valitse OK-painike.  
6. Lisää seuraavalle riville toinen työnkulun osavaihe *Hyväksymispyyntö on hyväksytty* -tapahtumalle.  

    1. Määritä **Kun - tapahtuma** -kenttään *Hyväksymispyyntö on hyväksytty*.
    2. Valitse **Ehto** -kentässä sana **Aina** ja määritä sitten **Odottavat hyväksynnät** -kentässä *>0*.  

      Tämän vaiheen tulos on se, että ehto näkyy muodossa *Odottavat hyväksynnät:>0*, mikä osoittaa, että tämä *ei* ole viimeinen hyväksyjä.  
    3. Valitse **Sitten - vastaus** -kentässä **Valitse vastaus** -linkki ja valitse sitten **Työnkulun vastaukset** -sivun **Valitse vastaus** -kentässä *Lähetä tietueen hyväksymispyyntö ja luo ilmoitus* -vastaus.  
    4. Valitse OK-painike.  
7. Lisää seuraavalle riville työnkulun osavaihe *Hyväksymispyyntö on hylätty* -tapahtumalle.  

    1. Määritä **Kun - tapahtuma** -kenttään *Hyväksymispyyntö on hylätty*.  
    2. Jätä **Ehto**-kentässä arvoksi *Aina*.  
    3. Valitse **Sitten - vastaus** -kentässä **Valitse vastaus** -linkki ja valitse sitten **Työnkulun vastaukset** -sivun **Valitse vastaus** -kentässä *Hylkää uudet arvot* -vastaus.  
    4. Valitse **Lisää vastauksia** -linkki ja lisää sitten merkintä *Hylkää tietueen hyväksymispyyntö ja luo ilmoitus* -vastaukselle
    5. Valitse OK-painike.  
8. Lisää seuraavalle riville toinen työnkulun osavaihe *Hyväksymispyyntö on hylätty* -tapahtumalle.  

    1. Määritä **Kun - tapahtuma** -kenttään *Hyväksymispyyntö on hylätty*.  
    2. Jätä **Ehto**-kentässä arvoksi *Aina*.  
    3. Valitse **Sitten - vastaus** -kentässä **Valitse vastaus** -linkki ja valitse sitten **Työnkulun vastaukset** -sivun **Valitse vastaus** -kentässä *Lähetä tietueen hyväksymispyyntö ja luo ilmoitus* -vastaus.  
    4. Valitse OK-painike.  
9. Jos haluat ottaa työnkulun käyttöön, valitse **Käytössä**-kenttä.  

Seuraavissa kuvissa on yleiskuvaus tämän menettelyn tuloksesta.  

:::image type="content" source="media/Workflows/workflow-example-2.png" alt-text="Kuva toimittajan nimen hyväksyntä -työnkulusta.":::

Seuraavaksi työnkulku on testattava avaamalla aiemmin luotu toimittaja ja vaihtamalla sen nimi. Varmista, että toimittajan nimen muuttamisen yhteydessä tehdään hyväksymispyyntö.

## <a name="see-also"></a>Katso myös

[Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md)  
[Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md)  
[Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md)  
[Arkistoitujen työnkulun osavaiheen ilmentymien tarkasteleminen](across-how-to-view-archived-workflow-step-instances.md)  
[Työnkulkujen poistaminen](across-how-to-delete-workflows.md)  
[Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Työnkulkujen määrittäminen](across-set-up-workflows.md)  
[Työnkulkujen käyttäminen](across-use-workflows.md)  
[Työnkulku](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
