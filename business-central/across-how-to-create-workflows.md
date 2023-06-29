---
title: Hyväksyntätyönkulkujen luominen tehtävien yhdistämistä varten
description: 'Lue lisää siitä, miten voit luoda työnkulkuja, jotka yhdistävät eri ihmisten suorittamia tehtäviä liiketoimintaprosesseissa.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
---
# <a name="create-workflows-to-connect-tasks-in-business-processes"></a><a name="create-workflows-to-connect-tasks-in-business-processes"></a>Työnkulkujen luominen liiketoimintaprosessin yhdistämistehtäviä varten

Voit luoda työnkulkuja, jotka yhdistävät eri käyttäjien suorittamia tehtäviä liiketoimintaprosesseissa. Voit sisällyttää mukaan järjestelmätehtäviä (kuten automaattinen kirjaus) työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita.  

Voit luoda **Työnkulku**-sivulla työnkulun mainitsemalla toimet riveillä. Jokainen vaihe koostuu käynnistimestä ja vastauksesta:

* Tapahtuma, joka määrittää työnkulun aloitusehdot.
* Työnkulun vastaus, joka määrittää työnkulun.

[!INCLUDE[workflow](includes/workflow.md)]

Kun luot työnkulkuja, voit kopioida vaiheet aiemmin luoduista työnkuluista tai työnkulkumalleista. Työnkulun mallit ovat ei-muokattavissa olevia työnkulkuja, joita [!INCLUDE[prod_short](includes/prod_short.md)] tarjoaa. Työnkulkumallien tunnisteet, jotka sisältävät etuliitteen "MS-", kuten "MS-PIW". Lisätietoja kohdassa [Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md).  

> [!NOTE]  
> Kaikki työnkulun osavaiheiden ilmoitukset lähetetään työjonon kautta. Varmista, että työjono vastaa yrityksesi tarpeita. Lue lisätietoja kohdasta [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).  

:::image type="content" source="media/Workflows/workflow-example.png" alt-text="Kuva työnkulun esimerkistä.":::

Työnkulku jakautuu kolmeen osaan:

1. **Kun - tapahtuma**  
   Tässä valitaan käynnistin.  
   Esimerkkejä käynnistimestä:
   * Päätietojen tietuetta muutetaan
   * Päiväkirjaan luodaan rivi
   * Saapuva asiakirja luodaan tai vapautetaan
   * Asiakirjan hyväksyntää pyydetään
2. **Ehto**  
   **Ehdot** liittyvät tapahtumaan ja mahdollistavat suodattimien luomisen sen päättämiseksi, miten työnkulku jatkuu.
3. **Sitten - vastaus**  
   **Vastaukset** määrittävät työnkulun seuraavat vaiheet.

Tapahtumien ja vastausten vaihtoehdot ovat järjestelmän määrittämiä. Jos haluat lisätä uusia vaihtoehtoja, sinun on kehitettävä laajennus.

## <a name="to-create-a-workflow"></a><a name="to-create-a-workflow"></a>Työnkulun luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulut**, valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto. **Työnkulku**-sivu avautuu.  
3. Anna **Koodi**-kentässä enintään 20 merkkiä pitkä työnkulun tunniste.  
4. Voit luoda työnkulun työnkulkumallista valitsemalla **Työnkulut**-sivulla **Uusi työnkulku mallista** -toiminnon. Lisätietoja kohdassa [Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md).  
5. Syötä **Kuvaus**-kenttään työnkulun kuvaus.  
6. Määritä **Luokka**-kentässä, mihin luokkaan työnkulku kuuluu.  
7. Määritä **Kun - tapahtuma** -kentässä tapahtuma, jonka on tapahduttava, jotta työnkulun vaihe käynnistyy.  

   Kun valitset kentän, **Työnkulkutapahtumat**-sivu näyttää kaikki käytettävissä olevat työnkulun tapahtumat.  
8. Määritä **Ehto**-kentässä vähintään yksi ehto, jonka on toteuduttava, ennen kuin **Kun-tapahtuma**-kentän tapahtuma voi tapahtua.  

   Kun valitset kentän, **tapahtumaehdot**-sivulla on luettelo suodatuskentistä, jotka voivat olla tapahtuman ehdot. Voit halutessasi lisätä uusia suodatuskenttiä.  

   Jos työnkulun tapahtuma on muutos tietyssä tietueen kentässä, käytä **tapahtumaehdot**-sivua valitaksesi kentän ja muutoksen tyypin.  

   1. Voit määrittää tapahtuman kentän muutoksen **Tapahtuman ehdot** -sivulla **Kenttä**-kentässä valitsemalla kentän, joka muuttuu.  
   2. **Operaattori** -kentässä, valitse joko **Pienentynyt**, **Suurentunut** tai **Muuttunut**.  
9. Määritä **Sitten - vastaus** -kentässä vastaus, joka seuraa, kun työnkulun tapahtuma toteutuu.  

   Kun valitset kentän, **Työnkulun vastaukset**-sivu näyttää kaikki käytettävissä olevat työnkulun vastaukset ja vastausvaihtoehdot.  
10. Määritä **Valitun vastauksen vaihtoehdot** -pikavälilehdessä työnkulun vastauksen asetukset valitsemalla arvoja eri kenttiin, jotka näkyvät, seuraavasti:  

    1. Määritä työnkulun vastauksen asetukset, johon sisältyy ilmoitusten lähettäminen, täyttämällä kentät seuraavassa taulukossa kuvatulla tavalla.  

    > [!NOTE]
    > Kentät vaihtelevat valitun vastauksen mukaan.

       |Kenttä|Kuvaus|
       |-----|-----------|
       |**Ilmoita lähettäjälle**|Määrittää, ilmoitetaanko hyväksymispyynnön vastaanottajan asemesta hyväksynnän pyytäjälle. Jos valitset valintaruudun, **Vastaanottajan käyttäjätunnus** -kenttä on poissa käytöstä, koska hyväksynnän pyytäjälle eli lähettäjälle ilmoitetaan sen sijaan. Työnkulun vastauksen nimi muuttuu vastaavasti nimeksi **Luo ilmoitus &lt;lähettäjälle&gt;**. Jos valintaruutua ei ole valittu, työnkulun vastauksen nimi on **Luo ilmoitus &lt;käyttäjälle&gt;**.|
       |**Vastaanottajan käyttäjätunnus**|Määritä käyttäjä, jolle ilmoitus on lähetettävä. **Huomautus**: Tämä vaihtoehto on käytettävissä vain työnkulun vastauksissa, joissa on paikkamerkki kyseiselle käyttäjälle. Työnkulun vastaukset ilman paikkamerkkiä käyttäjille, ilmoituksen vastaanottaja määritetään yleensä **Hyväksyjäkäyttäjän asetuksissa**.|
       |**Ilmoitustapahtuman tyyppi**|Valitse työnkulun ilmoituksen käynnistin. Käynnistin voi olla tietueiden muutos, hyväksymispyyntö tai kulunut eräpäivä.|
       |**Linkin kohdesivu**|Valitse sivu, jonka ilmoituksen linkki avaa. Sivulla on oltava sama lähdetaulukko kuin tietueella.|
       |**Mukautettu linkki**|Määritä sen linkin URL-osoite, joka lisätään ilmoitukseen sivulle vievän linkin lisäksi.|

    2. Määritä työnkulun vastauksen asetukset, johon sisältyy hyväksymispyynnön luominen, täyttämällä kentät seuraavassa taulukossa kuvatulla tavalla.  

       |Kenttä|Kuvaus|  
       |-----|-----------|  
       |**Eräpäivän kaava**|Määrittää, monenko päivän aikana hyväksyjän on ratkaistava pyyntö. Jakso alkaa, kun pyyntö lähetetään.|
       |**Delegoi seuraavan jälkeen:**|Määritä, milloin, jos ollenkaan, hyväksyntäpyyntö delegoidaan automaattisesti korvaajalle. Voit valita automaattisen delegoinnin yhden, kahden tai viiden päivän päähän hyväksynnän pyynnöstä.|
       |**Hyväksyjän tyyppi**|Määritä, kuka on hyväksyjä, käyttäen hyväksyntäkäyttäjien ja työnkulun käyttäjien määritystä. Kun kentän määritys on **Myyjä/ostaja**, **Myyjän/ostajan koodi** -kenttään **Hyväksynnän käyttäjäasetukset** -sivulla määritetty käyttäjä määrittää hyväksyjän. Hyväksymispyyntötapahtumat luodaan sitten **Hyväksyjän rajatyyppi** -kentän arvon mukaan. Lisätietoja kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-workflow-users.md).|
       |**Näytä vahvistussanoma**|Määritä, näytetäänkö vahvistussanoma käyttäjille, kun käyttäjä pyytää hyväksyntää.|
       |**Hyväksyjän rajatyyppi**|Määrittele rajoitusten vaikutus hyväksyjille. Hyväksyjän hyväksymisrajan on oltava pyynnön arvon yläpuolella. Käytettävissä ovat seuraavat vaihtoehdot: <ol><li>**Hyväksyjäketju** määrittää, että hyväksyntäpyynnöt luodaan kaikille pyytäjän hyväksyjille ensimmäiseen hyväksyttyyn hyväksyjään saakka.</li><li>**Suora hyväksyjä** määrittää, että hyväksyntäpyyntö luodaan vain pyytäjän lähimmälle hyväksyjälle hänen hyväksyntärajastaan riippumatta.</li><li>**Ensimmäinen hyväksytty hyväksyjä** määrittää, että hyväksyntäpyyntö luodaan vain pyytäjän ensimmäiselle hyväksyjälle.</li><li>**Tietty hyväksyjä** määrittää, että ilmoitat **hyväksyjän tunnus** -kentässä valitulle käyttäjälle.</li></ol>|

    3. Määritä työnkulun vastauksen asetukset, johon sisältyy päiväkirjarivien luominen, täyttämällä kentät seuraavassa taulukossa kuvatulla tavalla.  

       |Kenttä|Kuvaus|  
       |-----|-----------|  
       |**Yleisen päiväkirjan mallin nimi**|Määritä päiväkirjan malliin nimi, josta määritetyt päiväkirjarivit luodaan.|  
       |**Yleisen päiväkirjan erän nimi**|Määritä päiväkirjan erän nimi, josta määritetyt päiväkirjarivit luodaan.|  

11. Määritä osavaiheen sijainti työnkulussa sisentämällä **Kun**-kentässä olevan tapahtuman nimi **Suurenna sisennystä**- ja **Pienennä sisennystä** -painikkeilla.  

    1. Sisennä edellisen vaiheen nimen alla oleva tapahtuma osoittamaan, että kyseessä on seuraava vaihe.  
    2. Osoita, että vaihe on yksi useammasta vaihtoehtoisesta vaiheesta, joka voi riippua sille asetetusta ehdosta sisentämällä tapahtuman nimi vastaamaan muita vaihtoehtoisia vaiheita. Aseta nämä vaihtoehtoiset vaiheet tärkeysjärjestykseen sijoittamalla tärkein ensimmäiseksi.  

    > [!NOTE]  
    >  Voit muuttaa ainoastaan sellaisen vaiheen sisennystä, jolla ei ole seuraavia vaiheita.  

12. Toista vaiheet 7–11, lisätäksesi työnkulun vaiheita joko luomaasi vaihetta ennen tai jälkeen.  
13. Kytke **Käytössä**-valitsin päälle määrittääksesi, että työnkulku alkaa ensimmäisen vaiheen **Aloituskohta**-tyyppisen tapahtuman toteuduttua. Lisätietoja on kohdassa [Työnkulkujen käyttäminen](across-use-workflows.md).  

> [!NOTE]  
> Älä ota työnkulkua käyttöön, ennen kuin olet varma, että se on valmis.  

> [!TIP]  
> Jos haluat tarkastella työnkuluissa käytettävien taulukoiden välisiä suhteita, valitse ![Kerro-ominaisuuden avaava hehkulamppu.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä sitten **Työnkulku – Taulukon suhteet**.  

## <a name="example-of-creating-a-new-workflow-using-existing-events"></a><a name="example-of-creating-a-new-workflow-using-existing-events"></a>Esimerkki uuden työnkulun luomisesta aiemmin luotujen tapahtumien avulla

Seuraavassa esimerkissä luodaan uusi työnkulku, joka hyväksyy muutoksen toimittajan nimeen:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulut**, valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto. **Työnkulku**-sivu avautuu.
3. Täytä työnkulkuosan kentät seuraavassa taulukossa kuvatulla tavalla.

    |Kenttä  |Arvo  |
    |---------|---------|
    |**Koodi**|**VENDAPN-01**|
    |**Kuvaus**|**Toimittajan nimen muutoksen hyväksyntä** |
    |**Luokka**|**OSTO**|

4. Tee seuraavalla tavalla luodaksesi ensimmäisen työnkulun osavaiheen.

    1. Määritä **Kun - tapahtuma** -kentässä *Toimittajatietue muutetaan*.  
    2. Valitse **Ehto**-kentässä sana **Aina**. Valitse sitten **Tapahtuman ehdot** -sivulla **Lisää ehto, kun kentän arvo muuttuu** -linkki ja valitse sitten **Nimi**-kenttä. Tämän vaiheen tulos on se, että ehto näkyy muodossa *Nimi muutetaan*.  
    3. Valitse **Sitten vastaus** -kentässä **Valitse vastaus** -linkki. Valitse sitten **Työnkulun vastaukset** -sivun **Valitse vastaus** -kentässä **Palauta tietueen \<Field\>-kentän arvo ja tallenna muutos** -vastaus. Määritä sitten **Nimi**-kenttä **Valitun vastauksen vaihtoehdot** -osassa.  
    4. Valitse **Lisää vastauksia** -linkki ja lisää sitten merkintä **Luo tietueelle hyväksyntäpyyntö käyttäen hyväksyjätyyppejä <%1> ja <%2>** -vastaukselle.  
    5. Vaihda uuden vastauksen **Valitun vastauksen asetukset** -osiossa **Hyväksyjän tyyppi** -kenttään **Työnkulun käyttäjäryhmä**. Määritä sitten käyttäjäryhmä **työnkulun käyttäjäryhmä** -kentässä. Lisätietoja kohdassa [Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md).  
    6. Lisää kolmas vastaus: **Lähetä tietueen hyväksymispyyntö ja luo ilmoitus**.  
    7. Lisää neljäs vastaus, **Näytä viesti "%1"**. Määritä sitten **Valitun vastauksen asetukset** -osion **Viesti**-kenttään **Hyväksymispyyntö on lähetetty**.  
    8. Valitse **OK** palataksesi työnkulun osavaiheeseen.  

5. Lisää seuraavalle riville uusi työnkulun osavaihe **Hyväksymispyyntö on hyväksytty** -tapahtumalle.

    1. Määritä **Kun - tapahtuma** -kenttään **Hyväksymispyyntö on hyväksytty**.  
    2. Valitse rivivalikko, valitse sitten **Suurenna sisennystä**.  
    3. Valitse **Ehto**-kentässä **Aina**. Määritä sitten **Odottavat hyväksynnät** -kentässä **0**. Ehto näkyy muodossa **Odottavat hyväksynnät:0**, mikä osoittaa, että pyyntö ei edellytä muita hyväksyjiä.  
    4. Valitse **Sitten vastaus** -kentässä **Valitse vastaus** -linkki. Valitse sitten **Työnkulun vastaukset** -sivun **Valitse vastaus** -kentässä **Lähetä tietueen hyväksymispyyntö ja luo ilmoitus** -vastaus.  
    5. Valitse **OK**.  
6. Lisää seuraavalle riville toinen työnkulun osavaihe **Hyväksymispyyntö on hyväksytty** -tapahtumalle.  

    1. Määritä **Kun - tapahtuma** -kenttään **Hyväksymispyyntö on hyväksytty**.
    2. Valitse **Ehto**-kentässä **Aina**. Määritä sitten **Odottavat hyväksynnät** -kentässä **>0**. Ehto näkyy muodossa **Odottavat hyväksynnät:>0**, mikä osoittaa, että tämä ei ole viimeinen hyväksyjä.  
    3. Valitse **Sitten vastaus** -kentässä **Valitse vastaus** -linkki. Valitse sitten **Työnkulun vastaukset** -sivun **Valitse vastaus** -kentässä **Lähetä tietueen hyväksymispyyntö ja luo ilmoitus** -vastaus.  
    4. Valitse **OK**.  
7. Lisää seuraavalle riville työnkulun osavaihe **Hyväksymispyyntö on delegoitu** -tapahtumalle.  

    1. Määritä **Kun-tapahtuma**-kenttään **Hyväksymispyyntö on delegoitu**.  
    2. Jätä **Ehto**-kentässä arvoksi **Aina**.  
    3. Valitse **Sitten vastaus** -kentässä **Valitse vastaus** -linkki. Valitse sitten **Työnkulun vastaukset** -sivun **Valitse vastaus** -kentässä **Lähetä tietueen hyväksymispyyntö ja luo ilmoitus** -vastaus.  
    4. Valitse **OK**.  
8. Lisää seuraavalle riville toinen työnkulun osavaihe **Hyväksymispyyntö on hylätty** -tapahtumalle.  

    1. Määritä **Kun - tapahtuma** -kenttään **Hyväksymispyyntö on hylätty**.  
    2. Jätä **Ehto**-kentässä arvoksi **Aina**.  
    3. Valitse **Sitten vastaus** -kentässä **Valitse vastaus** -linkki. Valitse sitten **Työnkulun vastaukset** -sivun **Valitse vastaus** - kentässä **Hylkää uudet arvot** -vastaus.  
    4. Valitse **Lisää vastauksia** -linkki, lisää sitten merkintä **Hylkää tietueen hyväksymispyyntö ja luo ilmoitus** -vastaukselle
    5. Valitse **OK**.  
9. Ota työnkulku käyttöön valitsemalla **Käytössä**-tilanvaihtonäppäin.  

Seuraavassa kuvassa on yleiskuvaus tämän menettelyn tuloksesta.  

:::image type="content" source="media/Workflows/workflow-example-2.png" alt-text="Kuva toimittajan nimen hyväksyntä -työnkulusta.":::

Testaa seuraavaksi työnkulku avaamalla aiemmin luotu toimittajakortti ja muuttamalla toimittajan nimeä. Varmista, että hyväksymispyyntö lähetetään toimittajan nimen muuttamisen jälkeen.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/create-workflows/)

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md)  
[Hyväksyjäkäyttäjien määrittäminen](across-how-to-set-up-approval-users.md)  
[Hyväksyntätyönkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md)  
[Arkistoitujen työnkulun osavaiheen ilmentymien tarkasteleminen](across-how-to-view-archived-workflow-step-instances.md)  
[Hyväksymistyönkulkujen poistaminen](across-how-to-delete-workflows.md)  
[Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Hyväksymistyönkulkujen määrittäminen](across-set-up-workflows.md)  
[Hyväksymistyönkulkujen käyttäminen](across-use-workflows.md)  
[Työnkulku](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
