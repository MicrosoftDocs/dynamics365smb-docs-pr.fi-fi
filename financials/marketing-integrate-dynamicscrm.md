---
title: Asiakassuhteiden hallinta Dynamics 365 for Salesin avulla Dynamics 365 for Financialsissa | Microsoft Docs
description: "Jos käytät Dynamics 365 for Salesia asiakassuhteissa, voit käyttää Dynamics 365 for Financialsia tilausten käsittelyyn ja talousasioissa. Tällä tavoin saavutetaan saumaton integrointi liidistä tuottoon."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 03/05/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: c0291cc316b49e1f1f4f2196745914daca158f61
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017

---
# <a name="managing-your-customer-relationships-using-dynamics-365-for-sales-from-inside-dynamics-365-for-financials"></a>Asiakassuhteiden hallinta Dynamics 365 for Salesin avulla Dynamics 365 for Financialsissa
Jos käytät Dynamics 365 for Salesia asiakassuhteissa, voit käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]ia tilausten käsittelyyn ja talousasioissa. Tällä tavoin saavutetaan saumaton integrointi liidistä tuottoon.

Kun sovellus on määritetty integroitumaan Dynamics 365 for Salesiin, voit käyttää Sales-tietoja [!INCLUDE[d365fin](includes/d365fin_md.md)]ista ja toisin päin tietyissä tilanteissa. Tämän integroinnin ansiosta voit käsitellä ja synkronoida molemmille palveluille yhteisiä tietotyyppejä, kuten asiakkaita, kontakteja ja myyntitietoja, sekä pitää tiedot ajan tasalla molemmissa palveluissa.  

**Huomautus**: [!INCLUDE[d365fin](includes/d365fin_md.md)]in nykyisessä versiossa Dynamics 365 for Salesia kutsutaan Dynamics CRM:ksi. Yksinkertaisuuden vuoksi tässä artikkelissa käytetään jatkossa [!INCLUDE[d365fin](includes/d365fin_md.md)]issa käytössä olevia termejä.  

Esimerkiksi myyjä voi käyttää Dynamics CRM:ssä [!INCLUDE[d365fin](includes/d365fin_md.md)]in hinnastoja myyntitilauksen luonnissa. Kun he lisäävät nimikkeen Dynamics CRM:n myyntitilausriville, he näkevät myös nimikkeen varastotason (saatavuuden) [!INCLUDE[d365fin](includes/d365fin_md.md)]ista. Nämä tiedot on julkaistu avustetun **Dynamics CRM -yhteyden määritys** -asennusoppaan osana.  

**Huomautus**: Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)]-kokemuksen mukauttaminen](ui-experiences.md).  

## <a name="setting-up-the-connection"></a>Yhteyden määrittäminen
Voit käynnistää aloitussivulta avustetun **Dynamics CRM -yhteyden määritys** -asennusoppaan helpottamaan yhteyden määritystä. Kun yhteys on muodostettu, Dynamics CRM:n tietueet on yhdistetty saumattomasti [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueisiin.  

**Huomautus**: Seuraavassa selitetään avustettu asennus, mutta voit suorittaa samat tehtävät manuaalisesti **CRM-yhteyden määritys** -ikkunassa.

Voit valita avustetussa asennusoppaassa, mitkä tiedot synkronoidaan palvelujen välillä. Voit myös määrittää, että haluat tuoda nykyisen Dynamics CRM -ratkaisun. Siinä tapauksessa on määritettävä hallinnollinen käyttäjätili.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Käyttäjätilin määrittäminen ratkaisun tuontia varten
Asennusopas käyttää hallinnollista tiliä nykyisen Dynamics CRM -ratkaisun tuontiin. Tämän tilin on oltava Dynamics CRM:n oikea käyttäjä, jolla on seuraavat käyttöoikeusroolit:

* järjestelmänvalvoja  
* ratkaisun mukauttaja.  

Lisätietoja on TechNetin artikkelissa [Käyttäjien luominen ja Microsoft Dynamics 365 (online) -käyttöoikeusroolien määrittäminen](https://technet.microsoft.com/library/jj191623.aspx) ja kohdassa [Toimintaohje: Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md).  

Tätä tiliä käytetään vain asennuksen aikana. Kun ratkaisu on tuotu [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, tiliä ei enää tarvita.

### <a name="setting-up-the-user-account-for-synchronization"></a>Synkronoinnin käyttäjätilin määrittäminen
Integraatiota varten tarvitaan jaettu käyttäjätili. Niinpä sinun onkin luotava Office 365 -tilauksessa erillinen käyttäjä, jota käytetään kahden palvelun välillä tapahtumaan synkronointiin. Tämän tilin on oltava jo kelvollinen Dynamics CRM -käyttäjä, mutta tilille ei tarvitse määrittää käyttöoikeusrooleja, koska asennusopas tekee sen puolestasi. Tämä käyttäjätili on määritettävä asennusoppaassa ainakin kerran sen perusteella, kuinka laajan synkronoinnin haluat ottaa käyttöön. Lisätietoja on TechNetin artikkelissa [Käyttäjien luominen ja Microsoft Dynamics 365 (online) -käyttöoikeusroolien määrittäminen](https://technet.microsoft.com/library/jj191623.aspx).

Jos otat käyttöön *tuotteen saatavuuden*, integrointiin käytettävällä käyttäjätilillä on oltava verkkopalvelun käyttöoikeusavain. Se on kaksivaiheinen toiminto. Sinun on valittava kyseisen tilin [!INCLUDE[d365fin](includes/d365fin_md.md)]-sivulla **Muuta verkkopalvelun käyttöoikeusavainta** -painike ja määritettävä CRM-yhteyden asennusoppaassa kyseinen käyttäjä OData-verkkopalvelun käyttäjäksi.

Jos otat käyttöön *myyntitilauksen integroinnin*, sinun on määritettävä tämän synkronoinnin käsittelevä käyttäjä. Se voi olla joko integrointikäyttäjä tai jokin muu käyttäjätili.

### <a name="coupling-records"></a>Tietueiden yhdistäminen
Voit valita avustetussa asennusoppaassa mitä kahden palvelun välillä synkronoidaan. Voit määrittää myöhemmin myös tietyn tyyppisten tietojen synkronoinnin. Tätä kutsutaan *yhdistämiseksi* ja tässä osassa kerrotaan, mitä seikkoja on kannattaa ottaa huomioon.

Jos haluat nähdä Dynamics CRM -tilit [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakkaina, kaksi tietuetyyppiä on yhdistettävä. Se on aika yksinkertaista: avaa **Asiakasluettelo**-ikkuna [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, jonka valintanauhan toiminnolla nämä tiedot voi yhdistää Dynamics CRM:n kanssa. Voit sitten määrittää, mitä Dynamics CRM -tilejä tietyt [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakkaat vastaavat.

Tietyillä alueilla toimintoa varten on ensin yhdistettävä tietyt tietojoukot ennen muita tietojoukkoja. Lisätietoja on seuraavassa luettelossa:

* Asiakkaat ja tilit  
  * Myyjät on yhdistettävä ensin Dynamics CRM -käyttäjien kanssa  
* Nimikkeet ja resurssit  
  * Mittayksiköt on yhdistettävä ensin Dynamics CRM -yksikköryhmien kanssa  
* Nimikkeiden ja resurssien hinnat  
  * Asiakkaan hintaryhmät on yhdistettävä ensin Dynamics CRM:n hintoihin  

**Huomautus**: Jos hinnoissa käytetään ulkomaan valuuttaa, varmista, että valuutat yhdistetään Dynamics CRM:n tapahtumavaluuttoihin.

Dynamics CRM:n myyntitilaukset tarvitsevat lisätietoja, kuten asiakkaita, mittayksiköitä, valuuttoja, asiakkaan hintaryhmiä, nimikkeitä ja/tai resursseja. Dynamics CRM:n myyntitilausten saumaton käyttö edellyttää, että asiakkaat, mittayksikkö, asiakkaan hintaryhmät, nimikkeet ja/tai resurssit yhdistetään ensin.

### <a name="synchronizing-records-fully"></a>Tietueiden täysi synkronointi
Valitse avustetun asennusoppaan lopussa **Suorita täysi synkronointi** -toiminto. Tämä toiminto aloittaa kaikkien [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueiden synkronoinnin kaikkien yhdistetyn Dynamics CRM -ratkaisun liittyvien tietueiden synkronoinnin. Valitse **Täyden CRM-synkronoinnin tarkistus** -ikkunassa **Aloita**-toiminto. Synkronointi aloittaa sitten töiden suorittamisen riippuvuuksien mukaisesti. Esimerkiksi valuuttatietueet synkronoidaan ennen asiakastietueita. Täysi synkronointi voi kestää kauan, joten se tapahtuu taustalla, jotta voit jatkaa [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöä.

Voit tarkistaa täyden synkronoinnin yksittäisten töiden etenemistä, porautua alaspäin **Työjonon tapahtuman tila**-, **Integrointitaulukkoon – projektin tila**- tai **Integrointitaulukosta – projektin tila** -kentissä **Täyden CRM-synkronoinnin tarkistus** -ikkunassa.

Saat **CRM-yhteyden määritys** -ikkunassa koska tahansa tietoja täydestä synkronoinnista. Täältä voit avata myös **Integrointitaulukon yhdistämismääritykset** -ikkunan, jossa on tietoja synkronoitavista Financialsin ja Dynamics CRM -ratkaisun taulukoista.

## <a name="see-also"></a>Katso myös
[Kontaktienhallinta](marketing-relationship-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  
[Oman [!INCLUDE[d365fin](includes/d365fin_md.md)]-kokemuksen mukauttaminen](ui-experiences.md)  
[Toimintaohje: Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md)    
[Organisaation ja käyttäjien perehdyttäminen Dynamics 365 (online) -ratkaisuun](https://www.microsoft.com/en-US/Dynamics/crm-customer-center/onboard-your-organization-and-users-to-dynamics-365-online.aspx)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
