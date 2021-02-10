---
title: Asiakkaiden hallinta Dynamics 365 Salesin avulla| Microsoft Docs
description: Voit tehdä Business Centralissa tietojen yhdistämismäärityksen Dynamics 365 Salesilla, jolloin saavutetaan liidistä tuottoon -prosessin saumaton integrointi ja synkronointi.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map, Sales
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 7234536ff432140b1606ffe685bb0225f4963612
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755315"
---
# <a name="using-dynamics-365-sales-from-business-central"></a>Dynamics 365 Salesin käyttäminen Business Centralissa
Jos käytät Dynamics 365 Salesia asiakassuhteissa, saat käyttöösi saumattoman integroinnin liidistä tuottoon käyttämällä [!INCLUDE[prod_short](includes/prod_short.md)]ia taustatehtäviin, kuten tilausten käsittelyyn, varastonhallintaan ja talousasioihin.

Ennen kuin voit käyttää integrointiominaisuuksia, [!INCLUDE[crm_md](includes/crm_md.md)]-järjestelmänvalvojan on määritettävä yhteys ja käyttäjät. Lisätietoja on kohdassa [Dynamics 365 Sales -integrointi](admin-prepare-dynamics-365-for-sales-for-integration.md).

> [!NOTE]
> Seuraavat ohjeet käsittelevät [!INCLUDE[crm_md](includes/crm_md.md)]in ja [!INCLUDE[prod_short](includes/prod_short.md)]in verkkoversioiden integrointiprosessia. Lisätietoja paikallisesta määrityksestä on kohdassa [Paikallisen Dynamics 365 Salesin integroinnin valmistelu](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Integroimalla sovellukset voit käyttää Salesissa [!INCLUDE[prod_short](includes/prod_short.md)]in tietoja ja joissakin tapauksissa myös päinvastoin. Voit käsitellä ja synkronoida molemmille palveluille yhteisiä tietoja, kuten asiakkaita, yhteyshenkilöitä ja myyntitietoja, ja pitää tiedot ajan tasalla molemmissa palveluissa.  

Esimerkiksi [!INCLUDE[crm_md](includes/crm_md.md)]-myyjä voi käyttää [!INCLUDE[prod_short](includes/prod_short.md)]:n hinnastoja myyntitilausta luodessaan. Kun myyjä lisää nimikkeen [!INCLUDE[crm_md](includes/crm_md.md)]:n myyntitilausriville, hän näkee nimikkeen varastomäärän (saatavuuden) [!INCLUDE[prod_short](includes/prod_short.md)]:stä.

Vastaavasti tilausten käsittelijät [!INCLUDE[prod_short](includes/prod_short.md)]:ssä voivat käsitellä myyntitilauksia, jotka on siirretty automaattisesti tai manuaalisesti [!INCLUDE[crm_md](includes/crm_md.md)]:stä. He voivat esimerkiksi luoda ja kirjata sellaisten nimikkeiden tai resurssien myyntitilausrivejä, jotka vietiin [!INCLUDE[crm_md](includes/crm_md.md)]-sovelluksesta käsin lisättyinä tuotteina. Lisätietoja on kohdassa [Myyntitilauksen tietojen käsitteleminen](marketing-integrate-dynamicscrm.md#handling-sales-order-data)

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] integroituu vain [!INCLUDE[crm_md](includes/crm_md.md)]in kanssa. Muut Dynamics 365 -sovellukset, jotka muuttavat [!INCLUDE[crm_md](includes/crm_md.md)]:n vakiotyönkulkua tai tietomallia (kuten Project Service Automation), voivat katkaista [!INCLUDE[prod_short](includes/prod_short.md)]:n ja [!INCLUDE[crm_md](includes/crm_md.md)]:n integroinnin.

## <a name="coupling-records"></a>Tietueiden yhdistäminen
Voit valita synkronoitavat tiedot asetusten ohjatussa määrityksessä. Voit määrittää myöhemmin myös tiettyjen tietojen synkronoinnin. Tätä kutsutaan *yhdistämiseksi*. Voit esimerkiksi yhdistää tietyn [!INCLUDE[crm_md](includes/crm_md.md)]-tilin tiettyyn [!INCLUDE[prod_short](includes/prod_short.md)] -asiakkaaseen. Tässä osassa käsitellään seikkoja, jotka on otettava huomioon tietueiden yhdistämisessä.

Jos haluat nähdä [!INCLUDE[crm_md](includes/crm_md.md)]-tilit [!INCLUDE[prod_short](includes/prod_short.md)]:n asiakkaina, kaksi tietuetyyppiä on yhdistettävä. Se tehdään käyttämällä [!INCLUDE[prod_short](includes/prod_short.md)]in **Asiakkaat**-luettelosivun **Määritä yhdistäminen** -toimintoa. Määritä sitten, mitkä [!INCLUDE[prod_short](includes/prod_short.md)] -asiakkaat vastaavat tiettyjä [!INCLUDE[crm_md](includes/crm_md.md)]-tilejä.

Voit myös luoda (ja yhdistää) [!INCLUDE[crm_md](includes/crm_md.md)]-tilin esimerkiksi [!INCLUDE[prod_short](includes/prod_short.md)] -asiakastietueen avulla käyttämällä **Dynamics 365 Salesin tilin luominen** -kohtaa tai päinvastoin **Asiakkaan luominen [!INCLUDE[prod_short](includes/prod_short.md)]:ssä** -kohtaa.

Kun määrität tietueiden välisen yhdistämisen, voit myös manuaalisesti pyytää, että nykyinen tietue, kuten asiakas, korvataan heti Salesin (tai [!INCLUDE[prod_short](includes/prod_short.md)]in) tilitiedoilla. Käytä siinä tapauksessa **Synkronoi nyt** -toimintoa. **Synkronoi nyt** -toiminto kysyy, korvataanko Sales- vai [!INCLUDE[prod_short](includes/prod_short.md)]-tietueen tiedot.

Joissakin tapauksissa tietyt tietojoukot on yhdistettävä ennen muita tietojoukkoja. Seuraavassa taulukossa on lisätietoja.

|Tiedot|Yhdistettävä ensin|
|-----|----|
|Asiakkaat ja tilit|Myyjät on yhdistettävä [!INCLUDE[crm_md](includes/crm_md.md)]-käyttäjien kanssa|
|Nimikkeet ja resurssit|Mittayksiköiden ja [!INCLUDE[crm_md](includes/crm_md.md)]-yksikköryhmien yhdistäminen|
|Nimikkeiden ja resurssien hinnat|Asiakkaan hintaryhmien yhdistäminen [!INCLUDE[crm_md](includes/crm_md.md)]-hintoihin|

> [!NOTE]  
> Jos hinnoissa käytetään ulkomaan valuuttaa tai asiakkaat käyttävät ulkomaan valuuttaa, varmista, että valuutat yhdistetään Salesin tapahtumavaluuttoihin.

[!INCLUDE[crm_md](includes/crm_md.md)]:n myyntitilaukset tarvitsevat lisätietoja, kuten asiakkaita, mittayksiköitä, valuuttoja, asiakkaan hintaryhmiä, nimikkeitä ja/tai resursseja. Myyntitilausten integraatio edellyttää, että asiakkaat, mittayksikkö, asiakkaan hintaryhmät, nimikkeet ja/tai resurssit yhdistetään.

## <a name="fully-synchronizing-records"></a>Tietueiden täysi synkronointi
Asetusten ohjatun määritysoppaan lopussa voit valita **Suorita täysi synkronointi** -toiminnon ja aloittaa kaikkien [!INCLUDE[prod_short](includes/prod_short.md)] tietueiden synkronoinnin [!INCLUDE[crm_md](includes/crm_md.md)]:n liittyvien tietueiden kanssa. Valitse **Täyden Dynamics 365 Sales -synkronoinnin tarkistus** -sivulla **Aloita**-toiminto. Täysi synkronointi voi kestään jonkin aikaa, mutta voit jatkaa [!INCLUDE[prod_short](includes/prod_short.md)]:n käyttöä samalla, kun synkronointi tapahtuu taustalla.

Voit tarkistaa täyden synkronoinnin yksittäisten töiden etenemisen valitsemalla **Dynamics 365 Sales -sovelluksen täyden synkronoinnin tarkistus** -sivulla tietueen, jonka tiedot haluat tarkistaa. Voit päivittää tilan synkronoinnin aikana päivittämällä sivun.

Saat **Microsoft Dynamics 365 -yhteyden määritys** -sivulla koska tahansa tietoja täydestä synkronoinnista. Voit avata siellä myös **Integrointitaulukon yhdistämismääritykset** -sivun, jossa on tietoja synkronoitavista [!INCLUDE[prod_short](includes/prod_short.md)] in ja Salesin taulukoista.

## <a name="handling-sales-order-data"></a>Myyntitilauksen tietojen käsitteleminen
Salesin [!INCLUDE[crm_md](includes/crm_md.md)]iin lähetyt myyntitilaukset siirretään automaattisesti [!INCLUDE[prod_short](includes/prod_short.md)]iin, jos valitset **Luo myyntitilaukset automaattisesti** -valintaruudun **Microsoft Dynamics 365 -yhteyden määrittäminen** -sivulla.
Vaihtoehtoisesti voi muuntaa [!INCLUDE[crm_md](includes/crm_md.md)]ista lähetyt myyntitilaukset manuaalisesti käyttämällä **Luo [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa** -toimintoa **Myyntitilaukset – Dynamics 365 for Sales** -sivulla.
Näissä myyntitilauksissa alkuperäisen tilauksen **Nimi**-kenttä siirretään ja yhdisetään myyntitilauksen **Ulkoisen asiakirjan numero** -kenttään [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa.

Tämä voi toimia myös, jos alkuperäinen myyntitilaus sisältää käsin lisättyjä tuotteita eli nimikkeitä tai resursseja, joita ei ole rekisteröity kumpaankaan sovellukseen. Tällöin tulee antaa **Käsin lisätyn tuotteen tyyppi**- ja **Käsin lisätyn tuotteen numero** -kentät **Myynnin ja myyntisaamisten asetukset** -sivulla. Tällöin ei-rekisteröityjen tuotteiden myynti yhdistetään tiettyyn nimike- tai resurssinumeroon.

> [!NOTE]
> Arvonmääritystä ei voi yhdistää nimikkeeseen tai resurssiin [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa, joka on liitetty tuotteeseen [!INCLUDE[crm_md](includes/crm_md.md)] -kohteessa. Jotta kirjoittaminen olisi mahdollista, on suositeltavaa luoda nimike tai resurssi erikseen tätä tarkoitusta varten, eikä se saa olla yhteydessä tuotteeseen [!INCLUDE[crm_md](includes/crm_md.md)] -ohjelmassa. 

Jos alkuperäisen myyntitilauksen nimikkeen kuvaus on hyvin pitkä, sitä varten [!INCLUDE[prod_short](includes/prod_short.md)]in myyntitilaukseen luodaan lisämyyntitilausrivi, jonka tyyppi on **Kommentti**.

Päivittää myyntitilauksen otsikkojen kentät, kuten Viimeisin toimituspvm tai Pyydetty toimituspvm. Kentät on yhdistetty **MYYNTITILAUS-TILAUS**-integrointitaulukon yhdistämismääritys -kohtaan. Ne synkronoidaan säännöllisesti [!INCLUDE[crm_md](includes/crm_md.md)]-sovellukseen. Prosessit, kuten myyntitilauksen vapauttaminen ja myyntitilauksen lähettäminen tai laskuttaminen, kirjataan myyntitilauksen aikajanalle [!INCLUDE[crm_md](includes/crm_md.md)]issa. Lisätietoja on kohdassa [Aktiviteettisyötteiden esittely](/dynamics365/sales-enterprise/manage-activities). <!--The /dynamics365/sales-enterprise/developer/introduction-activity-feeds link was broken. Should this actually point to /dynamics365/sales-enterprise/manage-activities-->

> [!NOTE]  
> Jaksoittainen synkronointi **MYYNTITILAUS-TILAUS**-integrointitaulukon yhdistämismäärityksenä toimii vain, kun myyntitilauksen integrointi on otettu käyttöön. Lisätietoja on kohdassa [Sales-yhteyden määritykset -sivun yhteysasetukset](admin-prepare-dynamics-365-for-sales-for-integration.md). Vain [!INCLUDE[crm_md](includes/crm_md.md)]:n lähetetyistä myyntitilauksista luodut myyntitilaukset synkronoidaan. Lisätietoja on kohdassa [Myyntitilauksen käsittelyn integroinnin käyttöönotto](/dynamics365/sales-enterprise/developer/enable-sales-order-processing-integration).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098170]

## <a name="handling-sales-quotes-data"></a>Myyntitarjouksen tietojen käsitteleminen
[!INCLUDE[crm_md](includes/crm_md.md)]issa aktivoidut myyntitarjoukset siirretään [!INCLUDE[prod_short](includes/prod_short.md)]iin, jos valitset **Käsittele myyntitarjoukset automaattisesti** -valintaruudun **Microsoft Dynamics 365 -yhteyden määrittäminen** -sivulla.
Vaihtoehtoisesti voit muuntaa [!INCLUDE[crm_md](includes/crm_md.md)]ista aktivoidut myyntitarjoukset manuaalisesti käyttämällä **Käsittele [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa** -toimintoa **Myyntitarjoukset – Dynamics 365 Sales** -sivulla.
Näissä myyntitarjouksissa alkuperäisen tarjouksen **Nimi**-kenttä siirretään ja yhdistetään myyntitilauksen **Ulkoisen asiakirjan numero** -kenttään [!INCLUDE[prod_short](includes/prod_short.md)]issa. Myös tarjouksen **Voimassaolo päättyy** -kenttä siirretään ja yhdistetään myyntitarjouksen **Tarjouksen voimassaolon päättymispäivä** -kenttään [!INCLUDE[prod_short](includes/prod_short.md)]issa.  

Myyntitarjouksia muokataan useita kertoja viimeistelyn aikana. Myyntitarjousten manuaalinen ja automaattinen käsittely [!INCLUDE[prod_short](includes/prod_short.md)]issa varmistaa, että myyntitarjousten edelliset versiot arkistoidaan ennen uusien myyntitarjousten käsittelyä [!INCLUDE[crm_md](includes/crm_md.md)]ista.

Kun valitset **Käsittely** [!INCLUDE[prod_short](includes/prod_short.md)]ssa tarjoukselle, jonka tila on **Voitettu**, myyntitilaus luodaan kohteessa [!INCLUDE[prod_short](includes/prod_short.md)] vain, jos vastaava myyntitilaus on lähetetty kohteesta [!INCLUDE[crm_md](includes/crm_md.md)]. Muussa tapauksessa tarjous vapautetaan vain [!INCLUDE[prod_short](includes/prod_short.md)]-ohjelmaan. Jos vastaava myyntitilaus lähetetään [!INCLUDE[crm_md](includes/crm_md.md)]-ohjelmaan myöhemmin ja myyntitilaus luodaan siitä, **Tarjousnumero** päivitetään myyntitilaukseen ja tarjous arkistoidaan.

## <a name="handling-posted-sales-invoices-customer-payments-and-statistics"></a>Kirjattujen myyntilaskujen, asiakkaiden maksujen ja tilastojen käsitteleminen
Kun myyntitilaus on täytetty, siitä luodaan lasku. Kun myyntitilaus luodaan, kirjattu myyntilasku voidaan siirtää [!INCLUDE[crm_md](includes/crm_md.md)]:ään, jos **Kirjattu myyntilasku** -sivun **Luo lasku [!INCLUDE[crm_md](includes/crm_md.md)]:ssä** -valintaruutu on valittu. Kirjatut laskut siirretään [!INCLUDE[crm_md](includes/crm_md.md)]:ään **Laskutettu**-tilassa.

Kun asiakasmaksu vastaanotetaan myyntilaskulle sovelluksessa [!INCLUDE[prod_short](includes/prod_short.md)], myyntilaskun tilaksi muutetaan **Maksettu** ja **Tilan syy** -kentän arvoksi määritetään **Osittainen**, jos lasku on maksettu osittain, tai **Kokonaan**, jos lasku on maksettu kokonaan, kun valitset **Päivitä tilin tiedot** -toiminnon [!INCLUDE[prod_short](includes/prod_short.md)] -asiakkaan sivulla. **Päivitä tilin tiedot** -toiminto päivittää myös arvot, kuten **Saldo**- ja **Kokonaismyynti**-kenttien arvot **[!INCLUDE[prod_short](includes/prod_short.md)] -tilin tiedot** -tietoruudussa [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksessa. Vaihtoehtoisesti voit käyttää ajastettuja töitä, asiakastilastoja ja POSTEDSALESINV-INV-kohdetta, jos nämä prosessit suoritetaan automaattisesti taustalla.

## <a name="see-also"></a>Katso myös
[Dynamics 365 Sales -integrointi](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Liikesuhteiden hallinta](marketing-relationship-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md)    
[Salesin ja myyntikeskuksen yleiskuvaus](/dynamics365/customer-engagement/sales-enterprise/overview)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
