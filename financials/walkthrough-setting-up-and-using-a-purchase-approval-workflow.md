---
title: "Vaihekuvaus – ostojen hyväksyntätyönkulun määrittäminen ja käyttäminen | Microsoft Docs"
description: "Voit automatisoida uusien tai muuttuneiden tietueiden hyväksymisprosessin esimerkiksi asiakirjojen, kirjausrivien ja asiakaskorttien kohdalla luomalla työnkulkuihin hyväksymisvaiheet. Ennen kuin luot hyväksymistyönkulkuja, määritä hyväksyjä ja varahyväksyjä jokaiselle hyväksyjäkäyttäjälle. Voit myös määrittää hyväksyjille rajat niille myynti -ja ostotietueille, joita he saavat hyväksyä. Hyväksymispyynnöt ja muut ilmoitukset voidaan lähettää sähköpostina tai sisäisenä muistiona. Kunkin hyväksyjäkäyttäjän asetuksiin voit määrittää myös milloin he saavat ilmoituksia."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: a49e50213f808fb72b43dfa22a34833b306ef12d
ms.openlocfilehash: 7ce4b45d740e50bba8256e72fcf43c70ea85922c
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen
Voit automatisoida uusien tai muuttuneiden tietueiden hyväksymisprosessin esimerkiksi asiakirjojen, kirjausrivien ja asiakaskorttien kohdalla luomalla työnkulkuihin hyväksymisvaiheet. Ennen kuin luot hyväksymistyönkulkuja, määritä hyväksyjä ja varahyväksyjä jokaiselle hyväksyjäkäyttäjälle. Voit myös määrittää hyväksyjille rajat niille myynti -ja ostotietueille, joita he saavat hyväksyä. Hyväksymispyynnöt ja muut ilmoitukset voidaan lähettää sähköpostina tai sisäisenä muistiona. Voit määrittää kunkin hyväksyjäkäyttäjän asetuksiin myös milloin he saavat ilmoituksia.  

 Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamista liiketoimintaprosessin tehtäviä. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita. Lisätietoja on kohdassa [Työnkulku](across-workflow.md).  

## <a name="about-this-walkthrough"></a>Tietoja tästä vaihekuvauksesta  
Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:  

-   Hyväksyjäkäyttäjien määrittäminen (mukaan lukien käyttäjän määrittäminen Windowsissa ja [!INCLUDE[d365fin](includes/d365fin_md.md)]issa).  
-   Hyväksyjäkäyttäjien ilmoitusten määrittäminen.  
-   Hyväksynnän työnkulun muokkaaminen ja ottaminen käyttöön.  
-   Ilmoituksia lähettävän työjonon aloittaminen.  
-   Pyytää hyväksynnän ostotilaukseen, Alicia.  
-   Ilmoituksen vastaanottaminen ja sitten hyväksyminen, Sean.  

## <a name="prerequisites"></a>Vaatimukset  
Tarvitse tämän vaihekuvauksen loppuun viemiseen CRONUS Finland Oy -esittely-yrityksen.

## <a name="story"></a>Taustatietoja  
CRONUS-superkäyttäjä Sean on omalla tietokoneellaan.  

Hän luo kaksi hyväksyjää. Yksi on Alicia, joka edustaa ostajaa. Toinen on hän itse edustaen Alician hyväksyjää. Sean antaa itselleen rajaton ostojen hyväksyntä oikeudet ja määrittää, että hän saa ilmoituksia sisäisenä muistiona mahdollisimman pian asian tapahtumasta. Lopuksi Sean luon pyydetyn hyväksynnän työnkulun kopioksi olemassa olevasta ostotilauksen hyväksymisen työnkulusta jättäen kaikki olemassa olevan tapahtuman ehdot ja vastausvaihtoehdot ennalleen ja sitten ottaa työnkulun käyttöön.  

Sean testaa hyväksyntätyönkulkua kirjautumalla ensin [!INCLUDE[d365fin](includes/d365fin_md.md)]iin Aliciana ja pyytää ostotilauksen hyväksymistä. Sean sitten kirjautuu omalla tunnuksellaan, näkee huomautuksen hänen Roolikeskuksessa, seuraa linkkiä ostotilauksen hyväksymispyyntöön ja hyväksyy pyynnön.  

## <a name="setting-up-the-sample-data"></a>Esimerkkitietojen määrittäminen  
Sinun on luotava paikalliseen tietokoneeseen ja [!INCLUDE[d365fin](includes/d365fin_md.md)]iin uusi Alicia-käyttäjä, jonka valitset myöhemmin hyväksyjäkäyttäjäksi. Oma käyttäjätilisi edustaa Seania.  

### <a name="to-add-alicia-as-a-user-on-the-local-computer"></a>Voit lisätä Alisian käyttäjäksi paikalliseen tietokoneeseen  

1.  Valitse **Käynnistä** **Hae ohjelmista ja tiedostoista** -ruudussa, anna **Muokkaa paikallisia käyttäjiä ja ryhmiä**, ja valitse sitten aiheeseen liittyvä linkki.  
2.  Avaa **Käyttäjät**-kansio.  
3.  Valitse **Toiminnot**-välilehdessä **Uusi käyttäjä**.  
4.  Kirjoita **Käyttäjänimi**-kenttään Alicia.  
5.  Kirjoita **Salasana**- ja **Vahvista salasana** -kenttiin kelvollinen salasana.  
6.  Sinun täytyy tyhjentää **Käyttäjän on vaihdettava salasana seuraavan sisäänkirjautumisen yhteydessä** -valintaruutu.  
7.  Sulje **Paikalliset käyttäjät ja ryhmät** -ikkuna.  

### <a name="to-add-alicia-as-a-user-in-included365finincludesd365finmdmd"></a>Alicia lisääminen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin käyttäjänä  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Käyttäjät** ja valitse sitten liittyvä linkki.  
2.  Valitse **Windows-käyttäjät** -ikkunan **Koti**-välilehden **Uusi**-ryhmässä **Uusi**.  
3.  Anna -**Käyttäjän kortti** -ikkunan **Käyttäjänimi**-kenttään Alicia.  
4.  Valitse **Windows-käyttäjänimi**-kentässä AssistEdit.  
5.  Kirjoita **Valitse käyttäjä tai ryhmä** -ikkunassa **Kirjoita valittavien kohteitten nimet** -kenttään Alicia ja valitse sitten **Tarkista nimet** -painike.  
6.  Kun [TIETOKONEEN NIMI]ALICIA näkyy kentässä, valitse **OK**.  
7.  Valitse **Käyttöoikeuksien joukot**-pikavälilehdessä **Käyttöoikeuksien joukko** -kentässä **SUPER**.  
8.  Valitse **Yritys**-kentässä **CRONUS International Ltd.**  
9. Valitse **OK**-painike.  

## <a name="setting-up-approval-users"></a>Hyväksyjäkäyttäjien määrittäminen  
Käyttämällä Windows-käyttäjää, joka on juuri luotu, määritä Alicia hyväksyjäkäyttäjäksi, jonka hyväksyjä olet itse. Aseta hyväksyntäoikeutesi ja määritä, miten ja milloin sinulle ilmoitetaan hyväksymispyynnöt.  

### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Määritä itsesi ja Alicia hyväksyjäkäyttäjiksi  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "") -kuvake, kirjoita **Hyväksynnän käyttäjäasetukset** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Hyväksynnän käyttäjäasetukset** -ikkunan **Koti**-välilehden **Uusi**-ryhmässä **Uusi**.  

    > [!NOTE]  
    >  Hyväksyjä täytyy määrittää ennen kuin voit määrittää käyttäjiä, jotka tarvitsevat tämän hyväksyjän hyväksynnän. Siksi sinun on määritettävä itsesi ennen kuin voit määrittää Alician.  

3.  Voit määrittää kaksi hyväksyjäkäyttäjää täyttämällä kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Käyttäjätunnus|Hyväksyjän tunnus|Rajaton ostojen hyväksyntä|  
    |-------------|-----------------|---------------------------------|  
    |[TIETOKONEEN NIMI][SINÄ]||Valittu|  
    |[TIETOKONEEN NIMI]ALICIA|[TIETOKONEEN NIMI][SINÄ]||  

## <a name="setting-up-notifications"></a>Ilmoitusten määrittäminen  
Määritä, miten ja milloin ilmoitetaan hyväksymispyynnöt.  

### <a name="to-set-up-how-and-when-you-are-notified"></a>Voit määrittää, miten ja milloin saat ilmoituksen  
1.  Valitse **Hyväksynnän käyttäjäasetukset** -ikkunassa rivi itseäsi varten ja valitse sitten **Koti** -välilehdessä **Prosessi**-ryhmässä **Ilmoituksen asetukset**.  
2.  Anna **Ilmoituksen asetukset** -ikkunan **Ilmoitustyyppi**-kentässä **Hyväksyntä**.  
3.  Valitse **Ilmoitusmallin koodi** -kenttä ja sitten **Lisäasetukset**-painike.  
4.  Valitse **Ilmoitusmallit**-ikkunan **Kotisivu**-välilehden **Hallinta**-ryhmässä **Muokkaa luetteloa**.  
5.  Anna HYVÄKSYNTÄ-mallin rivillä **Ilmoitusmenetelmä**-kenttään **Huomautus**.  
6.  Valitse **OK**-painike.  
7.  Valitse **Ilmoituksen asetukset** -ikkunan **Kotisivu**-välilehden **Käsittely**-ryhmässä **Ilmoitusaikataulu**.  
8.  Valitse **Ilmoitusaikataulu**-ikkunan **Esiintymä**-kentässä **Heti**.  
9. Valitse **OK**-painike.  

## <a name="creating-the-approval-workflow"></a>Hyväksymisen työnkulun luominen  
 Luo ostotilauksen hyväksymisen työnkulku kopioimalla vaiheet ostotilauksen hyväksymisen työnkulun mallista. Jätä ennalleen nykyisen työnkulun vaiheet ja ota työnkulku käyttöön.  

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Ostotilauksen hyväksymisen työnkulun luominen ja lähettäminen  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Työnkulut** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Työnkulut**-ikkunan **Toiminnot**-välilehden **Yleiset**-ryhmässä **Luo työnkulku mallista**.  
3.  Valitse **Toiminnot**-välilehden **Yleiset**-ryhmässä **Luo työnkulku mallista**. **Työnkulkumallit**-ikkuna avautuu.  
4.  Valitse työnkulkumalli nimeltä Ostotilauksen hyväksymistyönkulku ja valitse sitten **OK**.  

    Uuden työnkulun avautuvassa **Työnkulku**-ikkunassa on kaikki valitun mallin tiedot. **Koodi**-kentän arvoon liitetään -01, joka osoittaa, että kyseessä on ensimmäinen Ostotilauksen hyväksymistyönkulku -mallista luotu työnkulku.  
5.  Valitse **Työnkulku**-ikkunan otsikossa **Käytössä**-valintaruutu.  

## <a name="starting-a-notification-job-queue"></a>Ilmoitusten työjonon käynnistys  
Varmista, että järjestelmäsi työjono on määritetty käsittelemään työnkulun ilmoituksia.  

### <a name="to-start-the-notify-job-queue"></a>Käynnistä ILMOITA-työjono  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Työjonot** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Työjonot**-ikkunassa ILMOITA-työjonon rivi ja valitse sitten **Kotisivu**-välilehden **Käsittely**-ryhmässä **Käynnistä työjono**.  

## <a name="using-the-approval-workflow"></a>Hyväksymisen työnkulun käyttäminen  
Käytä uutta ostotilauksen hyväksymistyönkulkua kirjautumalla ensin [!INCLUDE[d365fin](includes/d365fin_md.md)]iin Aliciana ja pyydä ostotilauksen hyväksyntää. Kirjaudu sitten sisään itsenäsi, katso muistio Roolikeskuksessa, seuraa linkkiä hyväksymispyyntöön ja Hyväksy pyyntö.  

Voit kirjautua [!INCLUDE[d365fin](includes/d365fin_md.md)]iin eri käyttäjänä **Suorita toisena käyttäjänä** -toiminnolla.  

### <a name="to-log-into-included365finincludesd365finmdmd-as-alicia"></a>Kirjautuminen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin Aliciana  

1.  Paina [!INCLUDE[d365fin](includes/d365fin_md.md)]-verkkoasiakasohjelmassa selaimen verkkosivun käynnistyspainiketta VAIHTO-näppäimellä ja hiiren kakkospainikkeella ja valitse sitten **Suorita toisena käyttäjänä**.  

    Paina [!INCLUDE[d365fin](includes/d365fin_md.md)]in Windows-asiakasohjelmassa ohjelman käynnistyspainiketta VAIHTO-näppäimellä ja hiiren kakkospainikkeella ja valitse sitten **Suorita toisena käyttäjänä**.  

2.  Anna**Windowsin suojaus** -ikkunassa [TIETOKONEEN NIMI]ALICIA ja tarvittava salasana.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Pyydä hyväksyntä ostotilaukseen, Aliciana  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Ostotilaukset** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse rivi, jossa on ostotilaus 104001. Valitse sitten **Koti**-välilehdessä **Hallinta**-ryhmässä **Muokkaa**.  
3.  Valitse **Ostotilaus**-ikkunan **Toiminnot**-välilehden **Hyväksyntä**-ryhmässä **Lähetä hyväksymispyyntö**.  

    Huomaa, että arvo **Tila**-kentässä on nyt **Odottaa hyväksyntää**.  

4.  Sulje [!INCLUDE[d365fin](includes/d365fin_md.md)].  

### <a name="to-approve-the-purchase-order-as-sean"></a>Hyväksy ostotilaus, Seanina  

1.  Avaa [!INCLUDE[d365fin](includes/d365fin_md.md)] tavalliseen tapaan. Ohjelma avautuu sinä käyttäjänä.  
2.  Katso Roolikeskuksessasi **Omat ilmoitukset** -ikkunassa uuden muistiinpano Alicialta.  

    > [!NOTE]  
    >  Vaikka ilmoituksen toistumiseksi on määritetty **heti**, huomautus saapuu noin minuutin kuluttua siitä kun Alicia lähettää hyväksymispyynnön. Tämä johtuu oletusarvoisesta työjono-ominaisuuden toistumistiheydestä.  

3.  Kun huomautus näkyy **Omat ilmoitukset** -ikkunassa, valitse **Hyväksymistapahtuma: XX, XX** -arvo **Sivu**-kentässä. **Hyväksyttävät pyynnöt** -ikkuna avautuu siten, että Alician ostotilauspyyntö näkyy korostettuna.  
4.  Valitse **Hyväksyttävät pyynnöt**-ikkunan **Kotisivu**-välilehden **Käsittely**-ryhmässä **Hyväksy**.  

    Arvoksi **Tila**-kentässä Alician ostotilauksessa tulee **Vapautettu**.  

Olet nyt määrittänyt ja testannut yksinkertaisen hyväksymisen työnkulun, joka perustuu ostotilauksen hyväksymisen työnkulun kahteen ensimmäiseen vaiheeseen. Voit helposti laajentaa tämän työnkulun kirjaamaan Alician ostotilauksen automaattisesti, kun Sean hyväksyy sen. Voidaksesi tehdä tämän, sinun on otettava käyttöön Ostolaskun työnkulku, johon vapautetun ostolaskun vastaus kirjataan. Ensin sinun täytyy muuttaa työnkulun ensimmäisessä vaiheessa tapahtuman ehto (osto)**laskusta** **tilaukseksi**.  

[!INCLUDE[d365fin](includes/d365fin_md.md)]in yleinen versio sisältää lukuisia työnkulkumalleja sovelluskoodin tukemiin tilanteisiin. Useimmat näistä ovat hyväksynnän työnkulkuun. Lisätietoja on kohdassa Työnkulkumallit.  

Työnkulun variaatiot määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita. Lisätietoja on kohdassa [Toimintaohje: Työnkulkujen luominen](across-how-to-create-workflows.md).  

Jos liiketoimintaskenaario edellyttää työnkulun tapahtumaa tai vastausta, joka ei tueta, Microsoftin kumppanin on toteutettava se mukauttamalla sovelluksen koodia. Lisätietoja on kehittäjien ja IT-ammattilaisten ohjeen kohdassa [Vaihekuvaus: Uusien työnkulun tapahtumien ja vastausten määrittäminen](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses).  

## <a name="see-also"></a>Katso myös  
[Toimintaohje: Hyväksyjäkäyttäjien määrittäminen](across-how-to-set-up-approval-users.md)   
[Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md)   
[Toimintaohje: Työnkulkujen luominen](across-how-to-create-workflows.md)   
[Toimintaohje: Hyväksyntätyönkulkujen käyttäminen](across-how-use-approval-workflows.md)   
[Työnkulku](across-workflow.md)

