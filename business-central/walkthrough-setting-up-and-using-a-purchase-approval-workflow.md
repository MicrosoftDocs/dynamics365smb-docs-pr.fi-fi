---
title: "Ostojen hyväksyntätyönkulun määrittäminen ja käyttäminen | Microsoft Docs"
description: "Voit automatisoida uusien tai muuttuneiden tietueiden hyväksymisprosessin esimerkiksi asiakirjojen, kirjausrivien ja asiakaskorttien kohdalla luomalla työnkulkuihin hyväksymisvaiheet. Ennen kuin luot hyväksymistyönkulkuja, määritä hyväksyjä ja varahyväksyjä jokaiselle hyväksyjäkäyttäjälle. Voit myös määrittää hyväksyjille rajat niille myynti -ja ostotietueille, joita he saavat hyväksyä. Hyväksymispyynnöt ja muut ilmoitukset voidaan lähettää sähköpostina tai sisäisenä muistiona. Kunkin hyväksyjäkäyttäjän asetuksiin voit määrittää myös milloin he saavat ilmoituksia."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/08/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: d7af9edc0620a61f6e3f114feff3a831e91add57
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen
Voit automatisoida uusien tai muuttuneiden tietueiden hyväksymisprosessin esimerkiksi asiakirjojen, kirjausrivien ja asiakaskorttien kohdalla luomalla työnkulkuihin hyväksymisvaiheet. Ennen kuin luot hyväksymistyönkulkuja, määritä hyväksyjä ja varahyväksyjä jokaiselle hyväksyjäkäyttäjälle. Voit myös määrittää hyväksyjille rajat niille myynti -ja ostotietueille, joita he saavat hyväksyä. Hyväksymispyynnöt ja muut ilmoitukset voidaan lähettää sähköpostina tai sisäisenä muistiona. Voit määrittää kunkin hyväksyjäkäyttäjän asetuksiin myös milloin he saavat ilmoituksia.

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_md.md)]in työnkulkutoiminnon lisäksi voit integroida Microsoft Flow'n määrittämään tapahtumien työnkulkua [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Huomaa, että vaikka kyse on erillisistä työnkulkujärjestelmistä, jokainen Microsoft Flow'ssa luotu Flow-malli lisätään työnkulkumallien luetteloon [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Lisätietoja on kohdassa [Business Centralin käyttäminen automaattisessa työnkulussa](across-how-use-financials-data-source-flow.md).   

 Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamia liiketoimintaprosessin tehtäviä. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita. Lisätietoja on kohdassa [Työnkulku](across-workflow.md).  

## <a name="about-this-walkthrough"></a>Tietoja tästä vaihekuvauksesta  
Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:  

-   Hyväksyjäkäyttäjien määrittäminen.  
-   Hyväksyjäkäyttäjien ilmoitusten määrittäminen.  
-   Hyväksynnän työnkulun muokkaaminen ja ottaminen käyttöön.  
-   Pyytää hyväksynnän ostotilaukseen, Alicia.  
-   Ilmoituksen vastaanottaminen ja sitten hyväksyminen, Sean.  

## <a name="prerequisites"></a>Vaatimukset  
Tarvitse tämän vaihekuvauksen loppuun viemiseen CRONUS Finland Oy -esittely-yrityksen.

## <a name="story"></a>Taustatietoja  
Sean on CRONUS-superkäyttäjä. Hän luo kaksi hyväksyjää. Yksi on Alicia, joka edustaa ostajaa. Toinen on hän itse edustaen Alician hyväksyjää. Sean antaa itselleen rajaton ostojen hyväksyntä oikeudet ja määrittää, että hän saa ilmoituksia sisäisenä muistiona mahdollisimman pian asian tapahtumasta. Lopuksi Sean luon pyydetyn hyväksynnän työnkulun kopioksi olemassa olevasta ostotilauksen hyväksymisen työnkulusta jättäen kaikki olemassa olevan tapahtuman ehdot ja vastausvaihtoehdot ennalleen ja sitten ottaa työnkulun käyttöön.  

Sean testaa hyväksyntätyönkulkua kirjautumalla ensin [!INCLUDE[d365fin](includes/d365fin_md.md)]iin Aliciana ja pyytää ostotilauksen hyväksymistä. Sean sitten kirjautuu omalla tunnuksellaan, näkee huomautuksen hänen Roolikeskuksessa, seuraa linkkiä ostotilauksen hyväksymispyyntöön ja hyväksyy pyynnön.  

## <a name="setting-up-sample-data"></a>Esimerkkitietojen määrittäminen
Ennen käyttäjien ja heidän ilmoitustapansa hyväksyminen määrittämistä sinun on varmistettava, että [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssä on kaksi käyttäjää: Toinen käyttäjä viittaa Aliciaa. Toinen käyttäjä, eli sinä itse, viittaa Seaniin. Lisätietoja on kohdassa [Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md).

### <a name="setting-up-approval-users"></a>Hyväksyjäkäyttäjien määrittäminen  
Kun kirjautunut omana itsenäsi, määritä Alicia hyväksyjäkäyttäjäksi, jonka hyväksyjä sinä itse olet. Aseta hyväksyntäoikeutesi ja määritä, miten ja milloin sinulle ilmoitetaan hyväksymispyynnöt.  

#### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Määritä itsesi ja Alicia hyväksyjäkäyttäjiksi  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Hyväksynnän käyttäjäasetukset** ja valitse sitten liittyvä linkki.  
2.  Valitse **Hyväksynnän käyttäjäasetukset** -sivulla **Uusi**-toiminto.  

    > [!NOTE]  
    >  Hyväksyjä täytyy määrittää ennen kuin voit määrittää käyttäjiä, jotka tarvitsevat tämän hyväksyjän hyväksynnän. Siksi sinun on määritettävä itsesi ennen kuin voit määrittää Alician.  

3.  Voit määrittää kaksi hyväksyjäkäyttäjää täyttämällä kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Käyttäjätunnus|Hyväksyjän tunnus|Rajaton ostojen hyväksyntä|  
    |-------------|-----------------|---------------------------------|  
    |SINÄ||Valittu|  
    |ALICIA|SINÄ||  

### <a name="setting-up-notifications"></a>Ilmoitusten määrittäminen  
Tässä vaihekuvauksessa käyttäjälle ilmoitetaan sisäisellä ilmoituksella hyväksyttävistä pyynnöistä. Hyväksyntäilmoitus voidaan lähettää myös sähköpostitse. Lisätietoja on kohdassa [Ilmoitusten vastaanoton ajankohdan ja tavan määrittäminen](across-how-to-specify-when-and-how-to-receive-notifications.md). 

#### <a name="to-set-up-how-and-when-you-are-notified"></a>Voit määrittää, miten ja milloin saat ilmoituksen  
1.  Valitse **Hyväksynnän käyttäjäasetukset** -sivulla, valitse itsellesi rivi ja valitse sitten **Ilmoituksen asetukset** -toiminto.  
2.  Valitse **Ilmoituksen asetukset** -sivun **Ilmoitustyyppi**-kentässä **Hyväksyntä**.  
3.  Valitse **Ilmoitusmenetelmä**-kentässä **Huomautus**.  
6.  Valitse **Ilmoituksen asetukset** -sivulla **Ilmoitusaikataulu**-toiminto.  
7.  Valitse **Ilmoitusaikataulu**-sivun **Esiintymä**-kentässä **Heti**.  
8. Valitse **OK**-painike.  

## <a name="creating-the-approval-workflow"></a>Hyväksymisen työnkulun luominen  
 Luo ostotilauksen hyväksymisen työnkulku kopioimalla vaiheet ostotilauksen hyväksymisen työnkulun mallista. Jätä ennalleen nykyisen työnkulun vaiheet ja ota työnkulku käyttöön.  

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Ostotilauksen hyväksymisen työnkulun luominen ja lähettäminen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Työnkulut** ja valitse sitten liittyvä linkki.  
2.  Valitse **Työnkulut**-sivulla **Luo työnkulku mallista** -toiminto.  
3.  Valitse **Työnkulkumallit**-sivulla työnkulkumalli Ostotilauksen hyväksymistyönkulku ja valitse sitten **OK**.  

    Uuden työnkulun avautuvalla **Työnkulku**-sivulla on kaikki valitun mallin tiedot. **Koodi**-kentän arvoon liitetään -01, joka osoittaa, että kyseessä on ensimmäinen Ostotilauksen hyväksymistyönkulku -mallista luotu työnkulku.  
5.  Valitse **Työnkulku**-sivun otsikossa **Käytössä**-valintaruutu.  

## <a name="using-the-approval-workflow"></a>Hyväksymisen työnkulun käyttäminen  
Käytä uutta ostotilauksen hyväksymistyönkulkua kirjautumalla ensin [!INCLUDE[d365fin](includes/d365fin_md.md)]iin Aliciana ja pyydä ostotilauksen hyväksyntää. Kirjaudu sitten sisään itsenäsi, katso muistio Roolikeskuksessa, seuraa linkkiä hyväksymispyyntöön ja Hyväksy pyyntö.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Pyydä hyväksyntä ostotilaukseen, Aliciana  
1. Kirjaudu sisään Aliciana.
2.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten liittyvä linkki.  
3.  Valitse ensin avoimen ostotilauksen 104001 rivi ja sitten **Muokkaa**-toiminto.  
4.  Valitse **Ostotilaus**-sivulla **Lähetä hyväksymispyyntö** -toiminto.  

Huomaa, että arvo **Tila**-kentässä on nyt **Odottaa hyväksyntää**.  

### <a name="to-approve-the-purchase-order-as-sean"></a>Hyväksy ostotilaus, Seanina  
1. Kirjaudu sisään Seanina.
2.  Etsi roolikeskuksen **Omat ilmoitukset** -sivulla Alician lähettämä uusi huomautus.  
3.  Kun huomautus näkyy **Omat ilmoitukset** -sivulla, valitse **Hyväksymistapahtuma: XX, XX** -arvo **Sivu**-kentässä. **Hyväksyttävät pyynnöt** -sivu avautuu siten, että Alician ostotilauspyyntö näkyy korostettuna.  
4.  Valitse **Hyväksyttävät pyynnöt** -sivulla **Hyväksy**-toiminto.  

    Arvoksi **Tila**-kentässä Alician ostotilauksessa tulee **Vapautettu**.  

Olet nyt määrittänyt ja testannut yksinkertaisen hyväksymisen työnkulun, joka perustuu ostotilauksen hyväksymisen työnkulun kahteen ensimmäiseen vaiheeseen. Voit helposti laajentaa tämän työnkulun kirjaamaan Alician ostotilauksen automaattisesti, kun Sean hyväksyy sen. Voidaksesi tehdä tämän, sinun on otettava käyttöön Ostolaskun työnkulku, johon vapautetun ostolaskun vastaus kirjataan. Ensin sinun täytyy muuttaa työnkulun ensimmäisessä vaiheessa tapahtuman ehto (osto)**laskusta** **tilaukseksi**.  

[!INCLUDE[d365fin](includes/d365fin_md.md)]in yleinen versio sisältää lukuisia työnkulkumalleja sovelluskoodin tukemiin tilanteisiin. Useimmat näistä ovat hyväksynnän työnkulkuun.  

Työnkulun variaatiot määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita. Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).  

Jos liiketoimintaskenaario edellyttää työnkulun tapahtumaa tai vastausta, joka ei tueta, Microsoftin kumppanin on toteutettava se mukauttamalla sovelluksen koodia. Lisätietoja on kehittäjien ja IT-ammattilaisten ohjeen kohdassa [Vaihekuvaus: Uusien työnkulun tapahtumien ja vastausten määrittäminen](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses).  

## <a name="see-also"></a>Katso myös  
[Hyväksynnän käyttäjien määrittäminen](across-how-to-set-up-approval-users.md)   
[Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md)   
[Työnkulkujen luominen](across-how-to-create-workflows.md)   
[Hyväksymistyönkulkujen käyttäminen](across-how-use-approval-workflows.md)   
[Työnkulku](across-workflow.md)  
[Business Central -sovelluksen käyttäminen automaattisessa työnkulussa](across-how-use-financials-data-source-flow.md)

