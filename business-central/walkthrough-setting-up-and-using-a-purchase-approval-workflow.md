---
title: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen
description: 'Tässä opastuksessa on kaikki vaiheet, jotka liittyvät ostojen hyväksymistyönkulun määrittämiseen ja käyttämiseen Business Centralissa.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/13/2022
ms.author: edupont
---
# Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen

Voit automatisoida uusien tai muuttuneiden tietueiden hyväksymisprosessin esimerkiksi asiakirjojen, kirjausrivien ja asiakaskorttien kohdalla luomalla työnkulkuihin hyväksymisvaiheet.

Ennen kuin luot hyväksymistyönkulkuja, määritä hyväksyjä ja varahyväksyjä jokaiselle hyväksyjäkäyttäjälle. Voit myös määrittää hyväksyjille rajat niille myynti -ja ostotietueille, joita he saavat hyväksyä. Hyväksymispyynnöt ja muut ilmoitukset voidaan lähettää sähköpostina tai sisäisenä muistiona. Voit määrittää kunkin hyväksyjäkäyttäjän asetuksiin myös milloin he saavat ilmoituksia.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)]in työnkulkutoiminnon lisäksi voit käyttää Power Automatea määrittämään tapahtumien työnkulkua [!INCLUDE[prod_short](includes/prod_short.md)]issa. Huomaa, että vaikka kyse on erillisistä työnkulkujärjestelmistä, jokainen Power Automatessa luotu työnkulkumalli lisätään työnkulkumallien luetteloon [!INCLUDE[prod_short](includes/prod_short.md)]issa. Lue lisätietoja kohdasta [Business Centralin käyttäminen automaattisessa työnkulussa](across-how-use-financials-data-source-flow.md).  

Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamista liiketoimintaprosessin tehtäviä. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita. Lisätietoja kohdassa [Työnkulku](across-workflow.md).  

## Tietoja tästä vaihekuvauksesta

Tässä vaihekuvauksessa kuvataan seuraavat tehtävät:  

- Hyväksyjäkäyttäjien määrittäminen  
- Hyväksyjäkäyttäjien ilmoitusten määrittäminen  
- Hyväksynnän työnkulun muokkaaminen ja ottaminen käyttöön  
- Hyväksynnän pyytäminen ostotilaukseen (nimellä Alicia)  
- Ilmoituksen vastaanottaminen ja sitten pyynnön hyväksyminen (nimellä Sean)  

## Taustatietoja

Sean on superkäyttäjänä CRONUSissa. Hän luo kaksi hyväksyjää. Yksi on Alicia, joka edustaa ostajaa. Toinen on hän itse edustaen Alician hyväksyjää. Sean antaa itselleen rajaton ostojen hyväksyntä oikeudet ja määrittää, että hän saa ilmoituksia sisäisenä muistiona mahdollisimman pian asian tapahtumasta. Lopuksi Sean luo pyydetyn hyväksynnän työnkulun kopioksi olemassa olevasta *Ostotilauksen hyväksymisen työnkulku* -mallista jättäen kaikki olemassa olevan tapahtuman ehdot ja vastausvaihtoehdot ennalleen ja sitten ottaa työnkulun käyttöön.  

Sean testaa hyväksyntätyönkulkua kirjautumalla [!INCLUDE[prod_short](includes/prod_short.md)]iin Aliciana ja pyytää ostotilauksen hyväksymistä. Sean sitten kirjautuu omalla tunnuksellaan, näkee huomautuksen hänen Roolikeskuksessa, seuraa linkkiä ostotilauksen hyväksymispyyntöön ja hyväksyy pyynnön.  

## Käyttäjät

Ennen käyttäjien ja heidän ilmoitustapansa hyväksyminen määrittämistä sinun on varmistettava, että nuo käyttäjät ovat [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa: Toinen käyttäjä viittaa Aliciaan. Toinen käyttäjä, eli sinä itse, viittaa Seaniin. Lue lisätietoja kohdasta [Luo käyttäjät käyttöoikeuksien mukaan](ui-how-users-permissions.md).

### Hyväksyjäkäyttäjien määrittäminen

Kun kirjautunut omana itsenäsi, määritä Alicia hyväksyjäkäyttäjäksi, jonka hyväksyjä sinä itse olet. Aseta hyväksyntäoikeutesi ja määritä, miten ja milloin sinulle ilmoitetaan hyväksymispyynnöt.  

#### Määritä itsesi ja Alicia hyväksyjäkäyttäjiksi

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyväksynnän käyttäjäasetukset** ja valitse sitten vastaava linkki.  
2. Valitse **Hyväksynnän käyttäjäasetukset** -sivulla **Uusi**-toiminto.  

    > [!NOTE]  
    >  Hyväksyjä täytyy määrittää ennen kuin voit määrittää käyttäjiä, jotka tarvitsevat tämän hyväksyjän hyväksynnän. Tämä tarkoittaa sitä, että sinun on määritettävä itsesi ennen kuin voit määrittää Alician.  

3. Voit määrittää kaksi hyväksyjäkäyttäjää täyttämällä kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Käyttäjätunnus|Hyväksyjän tunnus|Rajaton ostojen hyväksyntä|  
    |-------|-----------|---------------------------|  
    |SINÄ||Valittu|
    |ALICIA|SINÄ||

### Ilmoitusten määrittäminen

Tässä vaihekuvauksessa käyttäjälle ilmoitetaan sisäisellä ilmoituksella hyväksyttävistä pyynnöistä. Hyväksymisilmoituksia voidaan myös lähettää sähköpostitse, ja voit lisätä työnkulun vastausvaiheen, joka ilmoittaa lähettäjälle, kun pyyntö hyväksytään tai hylätään. Lue lisätietoja kohdasta [Työnkulkuilmoitusten vastaanoton ajankohdan ja tavan määrittäminen](across-how-to-specify-when-and-how-to-receive-notifications.md).

#### Voit määrittää, miten ja milloin saat ilmoituksen

1. Valitse **Hyväksynnän käyttäjäasetukset** -sivulla, valitse itsellesi rivi ja valitse sitten **Ilmoituksen asetukset** -toiminto.  
2. Valitse **Ilmoituksen asetukset** -sivun **Ilmoitustyyppi**-kentässä **Hyväksyntä**.  
3. Valitse **Ilmoitusmenetelmä**-kentässä **Huomautus**.  
4. Valitse **Ilmoituksen asetukset** -sivulla **Ilmoitusaikataulu**-toiminto.  
5. Valitse **Ilmoitusaikataulu**-sivun **Toistuminen**-kentässä **Heti**.  

## Hyväksymistyönkulun luominen

Luo ostotilauksen hyväksymisen työnkulku kopioimalla vaiheet **Ostotilauksen hyväksymistyönkulku** -mallista. Jätä ennalleen nykyisen työnkulun vaiheet ja ota työnkulku käyttöön.  

> [!TIP]
> Vaihtoehtoisesti voit lisätä työnkulun vastausvaiheen, joka ilmoittaa lähettäjälle, kun heidän pyyntönsä on hyväksytty tai hylätty. Lue lisätietoja kohdasta [Työnkulkuilmoitusten vastaanoton ajankohdan ja tavan määrittäminen](across-how-to-specify-when-and-how-to-receive-notifications.md).

### Ostotilauksen hyväksymisen työnkulun luominen ja lähettäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulut**, valitse sitten vastaava linkki.  
2. Valitse **Työnkulut**-sivulla **Toiminnot**, valitse **Uusi** ja valitse sitten **Uusi työnkulku mallista** -toiminto.  
3. Valitse **Työnkulkumallit** sivulla työnkulkumalli nimeltä **Ostotilauksen hyväksymistyönkulku**.  

   Uuden työnkulun avautuvalla **Työnkulku**-sivulla on kaikki valitun mallin tiedot. **Koodi**-kentän arvoon liitetään *-01*, joka osoittaa, että kyseessä on ensimmäinen **Ostotilauksen hyväksymistyönkulku** -mallista luotu työnkulku.  
4. Kytke **Työnkulku**-sivun otsikossa **Käytössä**-valitsin päälle.  

## Hyväksymistyönkulun käyttäminen

Käytä uutta ostotilauksen hyväksymistyönkulkua kirjautumalla ensin [!INCLUDE[prod_short](includes/prod_short.md)]iin Aliciana ja pyydä ostotilauksen hyväksyntää. Kirjaudu sitten sisään itsenäsi, katso muistio Roolikeskuksessa, seuraa linkkiä hyväksymispyyntöön ja sitten hyväksy pyyntö.  

### Pyydä hyväksyntä ostotilaukseen, Aliciana

1. Kirjaudu sisään Aliciana.
2. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ostotilaukset**, valitse sitten vastaava linkki.  
3. Avaa *Myyntitilaus 106001* valitsemalla rivi.  
4. Valitse **Ostotilaus** -sivulla **Toiminnot**, valitse **Pyydä hyväksyntä** ja valitse sitten **Lähetä hyväksymispyyntö** -toiminto.  

Huomaa, että arvo **Tila**-kentässä on nyt **Odottaa hyväksyntää**.  

### Hyväksy ostotilaus, Seanina

1. Kirjaudu sisään Seanina.
2. Valitse roolikeskuksen **Itsepalvelu**-alueesta **Hyväksymispyynnöt**.
3. Valitse **Hyväksymispyyntö**-sivulta Alician ostotilausrivi, valitse sitten **Hyväksy**-toiminto.  

Arvoksi **Tila**-kentässä Alician ostotilauksessa tulee **Vapautettu**.  

Olet nyt määrittänyt ja testannut yksinkertaisen hyväksymisen työnkulun, joka perustuu **ostotilauksen hyväksymisen työnkulun** kahteen ensimmäiseen vaiheeseen. Voit helposti laajentaa tämän työnkulun kirjaamaan Alician ostotilauksen automaattisesti, kun Sean hyväksyy sen. Voidaksesi tehdä tämän, sinun on otettava käyttöön **Ostolaskun työnkulku**, johon vapautetun ostolaskun vastaus kirjataan. Ensin sinun täytyy muuttaa työnkulun ensimmäisessä vaiheessa tapahtuman ehto (osto)**laskusta** **tilaukseksi**.  

[!INCLUDE[prod_short](includes/prod_short.md)]in yleinen versio sisältää lukuisia työnkulkumalleja sovelluskoodin tukemiin tilanteisiin. Useimmat näistä malleista ovat hyväksynnän työnkulkuihin.  

Työnkulun variaatiot määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita. Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).  

[!INCLUDE[workflow](includes/workflow.md)]

## Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/use-approval-workflows/)

## Katso myös

[Hyväksyjäkäyttäjien määrittäminen](across-how-to-set-up-approval-users.md)  
[Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md)  
[Luo hyväksymistyönkulut](across-how-to-create-workflows.md)  
[Hyväksymistyönkulkujen käyttäminen](across-how-use-approval-workflows.md)  
[Työnkulku](across-workflow.md)  
[Business Centralin käyttäminen automaattisessa työnkulussa](across-how-use-financials-data-source-flow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
