---
title: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen
description: Voit automatisoida uusien tai muuttuneiden tietueiden hyväksymisprosessin esimerkiksi asiakirjojen, kirjausrivien ja asiakaskorttien kohdalla luomalla työnkulkuihin hyväksymisvaiheet. Ennen kuin luot hyväksymistyönkulkuja, määritä hyväksyjä ja varahyväksyjä jokaiselle hyväksyjäkäyttäjälle. Voit myös määrittää hyväksyjille rajat niille myynti -ja ostotietueille, joita he saavat hyväksyä. Hyväksymispyynnöt ja muut ilmoitukset voidaan lähettää sähköpostina tai sisäisenä muistiona. Kunkin hyväksyjäkäyttäjän asetuksiin voit määrittää myös milloin he saavat ilmoituksia.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/26/2021
ms.author: edupont
ms.openlocfilehash: 964e1dae3dc754198777c703a15c1ef0b6fe82a7
ms.sourcegitcommit: 6bce51954f17b80491e180f25d67ff18b1618a88
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/27/2021
ms.locfileid: "6110977"
---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen

Voit automatisoida uusien tai muuttuneiden tietueiden hyväksymisprosessin esimerkiksi asiakirjojen, kirjausrivien ja asiakaskorttien kohdalla luomalla työnkulkuihin hyväksymisvaiheet. Ennen kuin luot hyväksymistyönkulkuja, määritä hyväksyjä ja varahyväksyjä jokaiselle hyväksyjäkäyttäjälle. Voit myös määrittää hyväksyjille rajat niille myynti -ja ostotietueille, joita he saavat hyväksyä. Hyväksymispyynnöt ja muut ilmoitukset voidaan lähettää sähköpostina tai sisäisenä muistiona. Kunkin hyväksyjäkäyttäjän asetuksiin voit määrittää myös milloin he saavat ilmoituksia.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)]in työnkulkutoiminnon lisäksi voit käyttää Power Automatea määrittämään tapahtumien työnkulkua [!INCLUDE[prod_short](includes/prod_short.md)]issa. Huomaa, että vaikka kyse on erillisistä työnkulkujärjestelmistä, jokainen Power Automatessa luotu työnkulkumalli lisätään työnkulkumallien luetteloon [!INCLUDE[prod_short](includes/prod_short.md)]issa. Lisätietoja on kohdassa [Business Centralin käyttäminen automaattisessa työnkulussa](across-how-use-financials-data-source-flow.md).  

 Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamia liiketoimintaprosessin tehtäviä. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita. Lisätietoja on kohdassa [Työnkulku](across-workflow.md).  

## <a name="about-this-walkthrough"></a>Tietoja tästä vaihekuvauksesta

Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:  

- Hyväksyjäkäyttäjien määrittäminen  
- Hyväksyjäkäyttäjien ilmoitusten määrittäminen  
- Hyväksynnän työnkulun muokkaaminen ja ottaminen käyttöön  
- Hyväksynnän pyytäminen ostotilaukseen, nimellä Alicia  
- Ilmoituksen vastaanottaminen ja sitten pyynnön hyväksyminen, nimellä Sean  

## <a name="story"></a>Taustatietoja

Sean on superkäyttäjänä CRONUSissa. Hän luo kaksi hyväksyjää. Yksi on Alicia, joka edustaa ostajaa. Toinen on hän itse edustaen Alician hyväksyjää. Sean antaa itselleen rajaton ostojen hyväksyntä oikeudet ja määrittää, että hän saa ilmoituksia sisäisenä muistiona mahdollisimman pian asian tapahtumasta. Lopuksi Sean luon pyydetyn hyväksynnän työnkulun kopioksi olemassa olevasta ostotilauksen hyväksymisen työnkulusta jättäen kaikki olemassa olevan tapahtuman ehdot ja vastausvaihtoehdot ennalleen ja sitten ottaa työnkulun käyttöön.  

Sean testaa hyväksyntätyönkulkua kirjautumalla ensin [!INCLUDE[prod_short](includes/prod_short.md)]iin Aliciana ja pyytää ostotilauksen hyväksymistä. Sean sitten kirjautuu omalla tunnuksellaan, näkee huomautuksen hänen Roolikeskuksessa, seuraa linkkiä ostotilauksen hyväksymispyyntöön ja hyväksyy pyynnön.  

## <a name="users"></a>Käyttäjät

Ennen käyttäjien ja heidän ilmoitustapansa hyväksyminen määrittämistä sinun on varmistettava, että [!INCLUDE[prod_short](includes/prod_short.md)]:ssä on kaksi käyttäjää: Toinen käyttäjä viittaa Aliciaa. Toinen käyttäjä, eli sinä itse, viittaa Seaniin. Katso lisätietoja kohdasta [Luo käyttäjiä lisenssien mukaan](ui-how-users-permissions.md).

### <a name="setting-up-approval-users"></a>Hyväksyjäkäyttäjien määrittäminen

Kun kirjautunut omana itsenäsi, määritä Alicia hyväksyjäkäyttäjäksi, jonka hyväksyjä sinä itse olet. Aseta hyväksyntäoikeutesi ja määritä, miten ja milloin sinulle ilmoitetaan hyväksymispyynnöt.  

#### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Määritä itsesi ja Alicia hyväksyjäkäyttäjiksi

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyväksynnän käyttäjäasetukset** ja valitse sitten liittyvä linkki.  
2. Valitse **Hyväksynnän käyttäjäasetukset** -sivulla **Uusi**-toiminto.  

    > [!NOTE]  
    >  Hyväksyjä täytyy määrittää ennen kuin voit määrittää käyttäjiä, jotka tarvitsevat tämän hyväksyjän hyväksynnän. Siksi sinun on määritettävä itsesi ennen kuin voit määrittää Alician.  

3. Voit määrittää kaksi hyväksyjäkäyttäjää täyttämällä kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Käyttäjätunnus|Hyväksyjän tunnus|Rajaton ostojen hyväksyntä|  
    |-------------|-----------------|---------------------------------|  
    |SINÄ||Valittu|  
    |ALICIA|SINÄ||  

### <a name="setting-up-notifications"></a>Ilmoitusten määrittäminen

Tässä vaihekuvauksessa käyttäjälle ilmoitetaan sisäisellä ilmoituksella hyväksyttävistä pyynnöistä. Hyväksymisilmoitus voidaan myös lähettää sähköpostitse, ja voit lisätä työnkulun vastausvaiheen, joka ilmoittaa lähettäjälle, kun pyyntö hyväksytään tai hylätään. Lisätietoja on kohdassa [Ilmoitusten vastaanoton ajankohdan ja tavan määrittäminen](across-how-to-specify-when-and-how-to-receive-notifications.md).

#### <a name="to-set-up-how-and-when-you-are-notified"></a>Voit määrittää, miten ja milloin saat ilmoituksen

1. Valitse **Hyväksynnän käyttäjäasetukset** -sivulla, valitse itsellesi rivi ja valitse sitten **Ilmoituksen asetukset** -toiminto.  
2. Valitse **Ilmoituksen asetukset** -sivun **Ilmoitustyyppi**-kentässä **Hyväksyntä**.  
3. Valitse **Ilmoitusmenetelmä**-kentässä **Huomautus**.  
4. Valitse **Ilmoituksen asetukset** -sivulla **Ilmoitusaikataulu**-toiminto.  
5. Valitse **Ilmoitusaikataulu**-sivun **Toistuminen**-kentässä **Heti**.  

## <a name="creating-the-approval-workflow"></a>Hyväksymisen työnkulun luominen

Luo ostotilauksen hyväksymisen työnkulku kopioimalla vaiheet **Ostotilauksen hyväksymistyönkulku** -työnkulkumallista. Jätä ennalleen nykyisen työnkulun vaiheet ja ota työnkulku käyttöön.  

> [!TIP]
> Vaihtoehtoisesti voit lisätä työnkulun vastausvaiheen, joka ilmoittaa lähettäjälle, kun heidän pyyntönsä on hyväksytty tai hylätty. Lisätietoja on kohdassa [Ilmoitusten vastaanoton ajankohdan ja tavan määrittäminen](across-how-to-specify-when-and-how-to-receive-notifications.md).

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Ostotilauksen hyväksymisen työnkulun luominen ja lähettäminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulut** ja valitse sitten liittyvä linkki.  
2. Valitse **Työnkulut**-sivulla **Toiminnot**, valitse **Uusi** ja valitse sitten **Uusi työnkulku mallista** -toiminto.  
3. Valitse **Työnkulkumallit** sivulla työnkulkumalli nimeltä **Ostotilauksen hyväksymistyönkulku**.  

    Uuden työnkulun avautuvalla **Työnkulku**-sivulla on kaikki valitun mallin tiedot. **Koodi**-kentän arvoon liitetään *-01*, joka osoittaa, että kyseessä on ensimmäinen **Ostotilauksen hyväksymistyönkulku** -mallista luotu työnkulku.  
4. Valitse **Työnkulku**-sivun otsikossa **Käytössä**-valintaruutu.  

## <a name="using-the-approval-workflow"></a>Hyväksymisen työnkulun käyttäminen

Käytä uutta ostotilauksen hyväksymistyönkulkua kirjautumalla ensin [!INCLUDE[prod_short](includes/prod_short.md)]iin Aliciana ja pyydä ostotilauksen hyväksyntää. Kirjaudu sitten sisään itsenäsi, katso muistio Roolikeskuksessa, seuraa linkkiä hyväksymispyyntöön ja Hyväksy pyyntö.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Pyydä hyväksyntä ostotilaukseen, Aliciana

1. Kirjaudu sisään Aliciana.
2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Ostotilaukset** ja valitse sitten liittyvä linkki.  
3. Valitse rivi avataksesi myyntitilauksen 106001.  
4. Valitse **Ostotilaus** -sivulla **Toiminnot**, valitse **Pyydä hyväksyntä** ja valitse sitten **Lähetä hyväksymispyyntö** -toiminto.  

Huomaa, että arvo **Tila**-kentässä on nyt **Odottaa hyväksyntää**.  

### <a name="to-approve-the-purchase-order-as-sean"></a>Hyväksy ostotilaus, Seanina

1. Kirjaudu sisään Seanina.
2. Valitse roolikeskuksen **Itsepalvelu**-alueesta **Hyväksymispyynnöt**-ruutu.
3. Valitse **Hyväksymispyyntö**-sivulta Alician ostotilausrivi ja valitse sitten **Hyväksy**-toiminto.  

Arvoksi **Tila**-kentässä Alician ostotilauksessa tulee **Vapautettu**.  

Olet nyt määrittänyt ja testannut yksinkertaisen hyväksymisen työnkulun, joka perustuu ostotilauksen hyväksymisen työnkulun kahteen ensimmäiseen vaiheeseen. Voit helposti laajentaa tämän työnkulun kirjaamaan Alician ostotilauksen automaattisesti, kun Sean hyväksyy sen. Voidaksesi tehdä tämän, sinun on otettava käyttöön Ostolaskun työnkulku, johon vapautetun ostolaskun vastaus kirjataan. Ensin sinun täytyy muuttaa työnkulun ensimmäisessä vaiheessa tapahtuman ehto (osto)**laskusta** **tilaukseksi**.  

[!INCLUDE[prod_short](includes/prod_short.md)]in yleinen versio sisältää lukuisia työnkulkumalleja sovelluskoodin tukemiin tilanteisiin. Useimmat näistä ovat hyväksynnän työnkulkuun.  

Työnkulun variaatiot määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita. Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).  

Jos liiketoimintaskenaario edellyttää työnkulun tapahtumaa tai vastausta, joka ei ole tuettu, Microsoft-kumppanin on toteutettava se koodin avulla tai määrittämällä työnkulku Power Automaten avulla. Lisätietoja on kehittäjän ohjeiden kohdassa [[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen automaattisessa työnkulussa](across-how-use-financials-data-source-flow.md) tai [AL-tapahtumat](/dynamics365/business-central/dev-itpro/developer/devenv-events-in-al).

## <a name="see-also"></a>Katso myös

[Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md)  
[Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md)  
[Työnkulkujen luominen](across-how-to-create-workflows.md)  
[Hyväksymistyönkulkujen käyttäminen](across-how-use-approval-workflows.md)  
[Työnkulku](across-workflow.md)  
[Business Central -sovelluksen käyttäminen automaattisessa työnkulussa](across-how-use-financials-data-source-flow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]