---
title: Business Central -sovelluksen sähköpostin määrittäminen | Microsoft Docs
description: Lisätietoja tavoista, joilla sähköpostiviestejä lähetetään ja vastaanotetaan Business Central -sovelluksessa SMTP-palvelimen kautta tai miten Office 365 -tilauksessa luotuja sähköpostipalvelimen asetuksia käytetään.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 12/17/2019
ms.author: sgroespe
ms.openlocfilehash: df0956167908c214385b40e3ccb2f20a10d4458b
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910830"
---
# <a name="set-up-email"></a>Määritä sähköposti
Jos haluat lähettää ja vastaanottaa sähköpostiviestejä [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssä, SMTP-sähköpostiasetukset-sivun kentät on täytettävä.

Sen sijaan että kirjoittaisit SMTP-palvelimen tiedot manuaalisesti, voit käyttää **Käytä Office 365 Server -asetuksia** -toimintoa, joka hakee nämä tiedot Office 365 -tilauksesta

Voit määrittää sähköpostin joko myöhemmin kuvattavalla tavalla manuaalisesti tai käyttää ohjattua **Sähköpostiasetukset**-määritystä. Lisätietoja on ohjeaiheessa [Valmistautuminen liiketoimintaan](ui-get-ready-business.md).  

## <a name="to-set-up-email"></a>Sähköpostin määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **SMTP-sähköpostin asetukset** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Jos käytössä on tili, jossa vaaditaan kaksimenetelmäinen todennus, **Salasana**-kenttään syötettävän arvon on oltava sama kuin Office 365 -tilauksessa käytettävä salasana. Salasanan tyypin on oltava **Sovelluksen salasana**. Lisätietoja on kohdassa [Kaksivaiheisen vahvistuksen sovellussalasanojen hallinta](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Vaihtoehtoisesti voit lisätä Office 365 -tilauksessa määritetyt tiedot valitsemalla **Käytä Office 365 Server -asetuksia** -toiminnon.
4. Kun kaikki kentät on täytetty oikein, valitse **Testisähköpostin asetukset** -toiminto.
5. Kun testi onnistuu, sulje sivu.

## <a name="using-a-substitute-sender-address-on-outbound-email-messages"></a>Korvaavan lähettäjän osoitteen käyttäminen lähtevissä sähköpostiviesteissä
Kaikki [!INCLUDE[d365fin](includes/d365fin_md.md)]in lähtevät sähköpostiviestit käyttävät SMTP-sähköpostin asetussivulla määritetyn tilin oletusosoitetta edellä kuvatulla tavalla. Voit kuitenkin muuttaa Exchange-palvelimen **Lähetä –**- tai **Lähetä puolesta** -toimintoja lähtevien viestin lähettäjän osoitteen muuttamiseen. [!INCLUDE[d365fin](includes/d365fin_md.md)] käyttää oletustiliä Exchange-todennuksessa mutta joko korvaa lähettäjän osoitteen määrittämälläsi osoitteella tai muuttaa sitä puolesta-tiedolla.

Seuraavassa on esimerkkejä tavoista, joilla Lähetä –- tai Lähetä puolesta -toimintoja käytetään [!INCLUDE[d365fin](includes/d365fin_md.md)]issa:

 * Kun asiakirjoja lähetetään osto- tai myyntitilauksina toimittajille tai asiakkaille, haluat ehkä, että ne näyttävät tulevan _noreply@yourcompanyname.com_-osoitteesta.
 * Kun työnkulku lähettää hyväksyntäpyynnön sähköpostitse käyttämällä pyytäjän sähköpostiosoitetta.

> [!Note]
> Lähettäjän osoitteiden korvaamiseen voidaan käyttää vain yhtä tiliä. Et siis voi käyttää yhtä korvaavaa osoitetta ostoprosesseissa ja toista myyntiprosesseissa.

### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>Korvaavan lähettäjän osoitteen määrittäminen kaikkiin lähteviin sähköpostiviesteihin
1. Etsi Office 365 -tilin **Exchangen hallintakeskuksessa** postilaatikko, jota käytetään korvaavana osoitteena, ja kopioi sitten osoite tai kirjoita se muistiin. Jos tarvitset uuden osoitteen luo uusi käyttäjä Microsoft 365 -hallintakeskuksessa ja määritä käyttäjälle postilaatikko.
2. Valitse [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **SMTP-sähköpostin asetukset** ja valitse sitten liittyvä linkki.
3. Lisää korvaava osoite **Lähetä –** -kenttään.
4. Kopioi **Käyttäjätunnus**-kentässä oleva osoite tai kirjoita se muistiin.
5. Etsi **Exchangen hallintakeskuksessa** postilaatikko, jota käytetään korvaavana osoitteena, ja anna sitten **Käyttäjätunnus**-kentän osoite **Lähetä –** -kenttään. Lisätietoja on aiheessa [Yksittäisten postilaatikoiden käyttöoikeuksien määrittäminen EAC-määrityksen avulla](/Exchange/recipients/mailbox-permissions?view=exchserver-2019#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>Korvaavan osoitteen käyttäminen hyväksymistyönkuluissa
1. Valitse [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **SMTP-sähköpostin asetukset** ja valitse sitten liittyvä linkki.
2. Kopioi **Käyttäjätunnus**-kentässä oleva osoite tai kirjoita se muistiin.
3. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyväksynnän käyttäjäasetukset** ja valitse sitten liittyvä linkki.
4. Etsi **Exchangen hallintakeskuksessa** kunkin **Hyväksynnän käyttäjäasetukset** -sivun luettelossa olevan käyttäjän postilaatikot ja anna **Lähetä –** -kenttään osoite, joka oli **SMTP-sähköpostin asetukset** -sivun **Käyttäjätunnus**-kentässä [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Lisätietoja on kohdassa [Vastaanottajien käyttöoikeuksien hallinta](/Exchange/recipients/mailbox-permissions?view=exchserver-2019).
5. Valitse [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **SMTP-sähköpostin asetukset** ja valitse sitten liittyvä linkki.
6. Ota korvaus käyttöön ottamalla käyttöön **Salli lähettäjän korvaaminen** -valitsin.

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] määrittää seuraavassa järjestyksessä, mikä osoite näytetään: <br><br> 1. **Hyväksynnän käyttäjäasetukset** -sivun **Sähköposti**-kentässä työnkulun viesteille määritetty osoite. <br> 2. **SMTP-sähköpostin asetukset** -sivun **Lähetä –** -kentässä määritetty osoite. <br> 3. **SMTP-sähköpostin asetukset** -sivun **Käyttäjätunnus**-kentässä määritetty osoite.


## <a name="see-also"></a>Katso myös

[Exchange Onlinen jaetut postilaatikot](/exchange/collaboration-exo/shared-mailboxes)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen yrityssähköpostina Outlookissa](admin-outlook.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in hakeminen mobiililaitteeseen](install-mobile-app.md)
