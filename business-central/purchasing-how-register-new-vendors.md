---
title: Uuden toimittajan rekisteröinti toimittajan kortin luonnin avulla (sisältää videon)
description: Opi luomaan toimittajakortti jotta voit rekisteröidä uuden toimittajan tai alihankkijan ja tallentaa toimittajakortteja malliksi.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.search.form: '26, 27, 34, 461, 786, 1379, 1385, 1386, 1628'
ms.date: 09/05/2022
ms.author: bholtorf
---
# <a name="register-new-vendors"></a>Uusien toimittajien rekisteröiminen

Toimittajat tarjoavat tuotteita, jotka myydään. Jokainen toimittaja, jolta ostat, täytyy rekisteröidä toimittajakortin kanssa.

Ennen kuin voit rekisteröidä uusia toimittajia, sinun on määritettävä ostokoodeja, joita valitaan toimittajien korttien täyttämisen yhteydessä. Kun kaikki tarvittavat päätiedot on luotu, voit lisätä toimittajalle ainutlaatuisia ominaisuuksia, kuten priorisoida toimittajan maksutarkoituksiin tai luetteloida toimittajan ja muiden toimittajien toimittamat tuotteet. Kokonaan erillinen toimittajia koskevien määritystehtävien joukko on alennuksia, hintoja ja maksutapoja koskevien sopimusten tallentaminen. Lisätietoja kohdassa [Oston määrittäminen](purchasing-setup-purchasing.md).

Toimittajan kortti sisältää tiedot, joita tarvitaan tuotteiden ostamiseksi kultakin toimittajalta. Lisätietoja on kohdissa [Ostojen kirjaaminen](purchasing-how-record-purchases.md) ja [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).
<br /><br />  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="adding-new-vendors"></a>Uusien toimittajien lisääminen

Voit lisätä uusia toimittajia manuaalisesti täyttämällä **Toimittajankortti**-sivun tai käyttämällä malleja, jotka sisältävät ennalta määritettyjä tietoja. Voit esimerkiksi luoda malleja erityyppisille toimittajaprofiileille. Mallien käyttäminen säästää aikaa uusien toimittajien lisäämisen aikana ja varmistaa, että tiedot ovat aina oikein.

> [!NOTE]  
> Jos eri toimittajatyypeille on olemassa toimittajamalleja, kun alat luoda uutta toimittajakorttia, näet sivun, josta voit valita sopivan mallin. Jos vain yksi toimittajamalli on olemassa, uudet toimittajan kortit käyttävät aina kyseistä mallia.

Kun olet luonut mallin, voit kohdistaa sen yhteen tai useampaan valittuun toimittajaan käyttämällä **Käytä mallia** -toimintoa. Kun haluat luoda mallin, täytä tiedot, joita haluat käyttää uudelleen **Toimittajan kortti** -sivulla, ja tallenna se mallina. Lisätietoja on [Toimittajakortti-sivun tallentaminen mallina](purchasing-how-register-new-vendors.md#to-save-the-vendor-card-as-a-template) -osassa.

> [!TIP]
> Voi olla hyödyllistä mukauttaa **Toimittajamalli**-sivua, kun luot mallin. Jos esimerkiksi haluat lisätä kentän, joka ei vielä näy sivulla. Lue lisätietoja [Työtilan mukauttaminen](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner) -osassa.

Toimittajan voi luoda myös yhteyshenkilöstä. Lisätietoja on [Asiakkaan, toimittajan, työntekijän tai pankkitilin luominen yhteyshenkilöstä](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact) -osassa.

Maksusuorituksen saajien osoitteita käytetään, kun tulostetaan sekkejä toimittajille maksamista varten. Toimittajilla voi olla useita maksusuorituksen saajien osoitteita maksuja varten. Esimerkiksi toimittaja voi toimittaa nimikkeen tytäryhtiöstä, mutta haluaa saada maksun pääkonttorille. Sovelluksen [!INCLUDE [prod_short](includes/prod_short.md)] avulla voit määrittää useita postitusosoitteita jokaiselle toimittajalle. Voit myös valita oikean sijainnin maksujen lähettämistä varten laskuittain.

Voit määrittää maksusuorituksen saajien osoitteita Toimittajakortti-sivuilla ja ostotilausten ja laskujen Toimitus ja maksut -pikavälilehdessä. Kun luot maksupäiväkirjarivejä käyttämällä Maksa toimittajalle- tai Luo maksu -toimintoa Toimittajaluettelo- tai Toimittajakortti-sivulla tai maksupäiväkirjan Kohdista tapahtumat -toimintoa, toimittajatapahtuman maksusuorituksen saajan koodi määritetään. Voit korvata tämän arvon.

### <a name="to-create-a-new-vendor"></a>Uuden toimittajan luominen

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

> [!TIP]  
> Jos et tiedä laskutusosoitetta, jota käytetään kaikissa toimittajan laskuissa, älä täytä **Yleistä**-pikavälilehden **Nro**-kenttää. Valitse sen sijaan tavaran laskuttajan numeron sen jälkeen, kun olet määrittänyt ostotarjouksen, -tilauksen, -laskun otsikon.

Toimittaja on nyt rekisteröity, ja toimittajan kortti on valmis käytettäväksi ostoasiakirjoissa.

Jos haluat käyttää tätä toimittajan korttia mallina, kun luot uusia toimittajan kortteja, tallenna se toimittajamallina. Lisätietoja on [Toimittajakortin tallentaminen mallina](#to-save-the-vendor-card-as-a-template) -osassa.

### <a name="deleting-and-editing-vendor-information"></a>Toimittajan tietojen poistaminen ja muokkaaminen

Voit muokata toimittajakorttien tietoja milloin tahansa. Jos olet kirjannut toimittajalle tapahtuman, et voi kuitenkaan poistaa korttia, koska nimiketapahtumia voi tarvita valvontaan. Voit poistaa tapahtumia sisältäviä toimittajakortteja koodin avulla ottamalla yhteyttä Microsoft-kumppaniin.

> [!TIP]
> Voit muuttaa toimittajan kansainvälisen tilinumeron (IBAN) ilman, että muutos vaikuttaa aikaisempiin tilisiirtorekisterin tapahtumiin. Kredit-siirron rekisteröintitapahtumat tallentavat *vastaanottajan IBAN*-tunnuksen ja *vastaanottajan pankkitilinumeron*, jotka määritettiin **Toimittajan pankkitili**- ja **Vastaanottajan nimi** -kentissä **Toimittajakortti**-sivulta, kun tapahtumat luotiin.

> [!TIP]
> Voit lisätä vaihtoehtoisia osoitteita toimittajakortteihin valitsemalla **Tilausosoitteet**-toiminnon.

## <a name="to-save-the-vendor-card-as-a-template"></a>Toimittajan kortin tallentaminen mallina

1. Valitse **Toimittajakortti**-sivulla **Tallenna mallina** -toiminto. **Toimittajamalli**-sivu avautuu ja näyttää toimittajan kortin mallina.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voit käyttää dimensioita malleina valitsemalla **Dimensiot**-toiminnon. **Dimensiomallit**-sivu avautuu. Se sisältää kaikki toimittajalle määritetyt dimensiokoodit.
4. Muokkaa tai syötä dimensiokoodeja, joita käytetään mallin avulla luotuihin uusiin toimittajan kortteihin.
5. Kun olet määrittänyt uuden toimittajamallin, valitse **OK**.  
   Toimittajamalli lisätään toimittajamallien luetteloon niin, että sen avulla voit luoda uusia toimittajan kortteja.

## <a name="see-also"></a>Katso myös

[Tietueiden kaksoiskappaleiden yhdistäminen](sales-how-merge-duplicate-records.md)  
[Numerosarjojen luominen](ui-create-number-series.md)  
[Toimittajan pankkitilin määrittäminen](purchasing-how-set-up-vendors-bank-accounts.md)  
[Ostajien määrittäminen](purchasing-how-setup-purchasers.md)  
[Osto](purchasing-manage-purchasing.md)  
[Ostojen kirjaus](purchasing-how-record-purchases.md)  
[Sijaintien ja reittiohjeiden etsiminen online-karttojen avulla](across-online-maps.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
