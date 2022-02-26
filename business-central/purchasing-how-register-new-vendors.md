---
title: Uuden toimittajan rekisteröinti toimittajan kortin luonnin avulla (sisältää videon)
description: Tässä aiheessa opit luomaan toimittajakortin, jotta voit rekisteröidä uuden toimittajan tai alihankkijan ja tallentaa toimittajakortteja malliksi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.search.form: 26, 27, 34, 461, 786, 1379, 1385, 1386, 1628
ms.date: 09/29/2021
ms.author: edupont
ms.openlocfilehash: 1cbdf85f08939aa05c013901239bbd390400f3e1
ms.sourcegitcommit: c05806689d289d101bd558696199cefbd989473e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2022
ms.locfileid: "8115500"
---
# <a name="register-new-vendors"></a>Uusien toimittajien rekisteröiminen

Toimittajat tarjoavat tuotteita, jotka myydään. Jokainen toimittaja, jolta ostat, täytyy rekisteröidä toimittajakorttina.

Ennen kuin voit rekisteröidä uusia toimittajia, sinun on määritettävä ostokoodeja, joita valitaan toimittajien korttien täyttämisen yhteydessä. Kun kaikki tarvittavat päätiedot on luotu, voit tehdä muita toimittajaa koskevia määrityksiä, kuten priorisoida toimittajan maksutilanteita varten sekä eritellä nimikkeitä, joita toimittaja ja muut toimittajat voivat toimittaa. Kokonaan erillinen toimittajia koskevien määritystehtävien joukko on alennuksia, hintoja ja maksutapoja koskevien sopimusten tallentaminen. Lisätietoja on kohdassa [Ostojen määrittäminen](purchasing-setup-purchasing.md).

Toimittajan kortti sisältää tiedot, joita tarvitaan tuotteiden ostamiseksi toimittajalta. Lisätietoja on kohdissa [Ostojen kirjaaminen](purchasing-how-record-purchases.md) ja [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).

> [!NOTE]  
> Jos eri toimittajan tyypeille on olemassa toimittajamalleja, sivu avautuu, kun luot uuden toimittajan kortin, jossa voit valita haluamasi mallin. Jos vain yksi toimittajamalli on olemassa, uudet toimittajan kortit käyttävät aina kyseistä mallia.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="adding-new-vendors"></a>Uusien toimittajien lisääminen
Voit lisätä uusia toimittajia manuaalisesti täyttämällä **Toimittajankortti**-sivun kentät tai käyttämällä malleja, jotka sisältävät ennalta määritettyjä tietoja. Voit esimerkiksi luoda malleja erityyppisille toimittajaprofiileille. Mallien käyttäminen säästää aikaa uusien toimittajien lisäämisen aikana ja varmistaa, että tiedot ovat aina oikein. Jos luot malleja useammalle kuin yhdelle toimittajatyypille, voit valita mallin, jota käytetään, kun lisäät toimittajan. Jos luot vain yhden mallin, sitä käytetään kaikille uusille toimittajille. Kun olet luonut mallin, voit kohdistaa sen yhteen tai useampaan valittuun toimittajaan käyttämällä **Käytä mallia** -toimintoa. Kun haluat luoda mallin, täytä tiedot, joita haluat käyttää uudelleen Toimittajan kortti -sivulla, ja tallenna se mallina. Lisätietoja on osassa [Toimittajakortti-sivun tallentaminen mallina](purchasing-how-register-new-vendors.md#to-save-the-vendor-card-as-a-template).

> [!TIP]
> Voi olla hyödyllistä mukauttaa **Toimittajamalli**-sivua, kun luot mallin. Voit esimerkiksi haluta lisätä kentän, joka ei vielä näy sivulla. Lisätietoja on kohdassa [Työtilan mukauttaminen](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

Toimittajan voi luoda myös yhteyshenkilöstä. Lisätietoja on kohdassa [Asiakkaan, toimittajan, työntekijän tai pankkitilin luominen yhteyshenkilöstä](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact). 

### <a name="to-create-a-new-vendor"></a>Uuden toimittajan luominen

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

> [!TIP]  
> Jos et tiedä laskutusosoitetta, jota käytetään kaikissa toimittajan laskuissa, älä täytä **Toimittajan nro** -kenttää. Valitse sen sijaan tavaran laskuttajan numeron sen jälkeen, kun olet määrittänyt ostotarjouksen, -tilauksen, -laskun otsikon.

Toimittaja on nyt rekisteröity, ja toimittajan kortti on valmis käytettäväksi ostoasiakirjoissa.

Jos haluat käyttää tätä toimittajan korttia mallina, kun luot uusia toimittajan kortteja, tallenna se toimittajamallina. Lisätietoja on osassa [Toimittajakortin tallentaminen mallina](#to-save-the-vendor-card-as-a-template).

### <a name="deleting-and-editing-vendor-information"></a>Toimittajan tietojen poistaminen ja muokkaaminen

Voit muokata toimittajakorttien tietoja milloin tahansa. Jos olet kirjannut toimittajalle tapahtuman, et voi kuitenkaan poistaa korttia, koska nimiketapahtumia voi tarvita valvontaan. Voit poistaa tapahtumia sisältäviä toimittajakortteja koodin avulla ottamalla yhteyttä Microsoft-kumppaniin.

> [!TIP]
> Voit muuttaa toimittajan pankkitilin IBAN-tunnusta ilman, että muutos vaikuttaa aikaisempiin tilisiirtorekisterin tapahtumiin. Kredit-siirron rekisteröintitapahtumat tallentavat vastaanottajan IBAN-tunnuksen ja vastaanottajan pankkitilinumeron, jotka määritettiin Toimittajan pankkitili- ja Vastaanottajan nimi -kentissä Toimittajakortti-sivulta, kun tapahtumat luotiin.


## <a name="to-save-the-vendor-card-as-a-template"></a>Toimittajan kortin tallentaminen mallina

1. Valitse **Toimittajakortti**-sivulla **Tallenna mallina** -toiminto. **Toimittajamalli**-sivu avautuu ja näyttää toimittajan kortin mallina.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voit käyttää dimensioita malleina valitsemalla **Dimensiot**-toiminnon. **Dimensiomallit**-sivu avautuu. Se sisältää kaikki toimittajalle määritetyt dimensiokoodit.
4. Muokkaa tai syötä dimensiokoodeja, joita käytetään mallin avulla luotuihin uusiin toimittajan kortteihin.
5. Kun olet määrittänyt uuden toimittajamallin, valitse **OK**-painike.  
   Toimittajamalli lisätään toimittajamallien luetteloon niin, että sen avulla voit luoda uusia toimittajan kortteja.

## <a name="see-also"></a>Katso myös

[Tietueiden kaksoiskappaleiden yhdistäminen](sales-how-merge-duplicate-records.md)  
[Numerosarjojen luominen](ui-create-number-series.md)  
[Osto](purchasing-manage-purchasing.md)  
[Ostojen kirjaus](purchasing-how-record-purchases.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]