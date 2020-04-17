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
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: b9926ced6827354c438445f0618db5a525b080d2
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196733"
---
# <a name="using-dynamics-365-sales-from-business-central"></a>Dynamics 365 Salesin käyttäminen Business Centralissa
Jos käytät Dynamics 365 Salesia asiakassuhteissa, saat käyttöösi saumattoman integroinnin liidistä tuottoon käyttämällä [!INCLUDE[d365fin](includes/d365fin_md.md)]ia taustatehtäviin, kuten tilausten käsittelyyn, varastonhallintaan ja talousasioihin.

Ennen kuin voit käyttää integrointiominaisuuksia, [!INCLUDE[crm_md](includes/crm_md.md)]-järjestelmänvalvojan on määritettävä yhteys ja käyttäjät. Lisätietoja on kohdassa [Dynamics 365 Sales -integrointi](admin-prepare-dynamics-365-for-sales-for-integration.md).

> [!NOTE]
> Seuraavat ohjeet käsittelevät [!INCLUDE[crm_md](includes/crm_md.md)]in ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in verkkoversioiden integrointiprosessia. Lisätietoja paikallisesta määrityksestä on kohdassa [Paikallisen Dynamics 365 Salesin integroinnin valmistelu](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Integroimalla sovellukset voit käyttää Salesissa [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietoja ja joissakin tapauksissa myös päinvastoin. Voit käsitellä ja synkronoida molemmille palveluille yhteisiä tietoja, kuten asiakkaita, yhteyshenkilöitä ja myyntitietoja, ja pitää tiedot ajan tasalla molemmissa palveluissa.  

Esimerkiksi [!INCLUDE[crm_md](includes/crm_md.md)]-myyjä voi käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]:n hinnastoja myyntitilausta luodessaan. Kun myyjä lisää nimikkeen [!INCLUDE[crm_md](includes/crm_md.md)]:n myyntitilausriville, hän näkee nimikkeen varastomäärän (saatavuuden) [!INCLUDE[d365fin](includes/d365fin_md.md)]:stä.

Vastaavasti tilausten käsittelijät [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssä voivat käsitellä myyntitilauksia, jotka on siirretty automaattisesti tai manuaalisesti [!INCLUDE[crm_md](includes/crm_md.md)]:stä. He voivat esimerkiksi luoda ja kirjata sellaisten nimikkeiden tai resurssien myyntitilausrivejä, jotka vietiin [!INCLUDE[crm_md](includes/crm_md.md)]-sovelluksesta käsin lisättyinä tuotteina. Lisätietoja on kohdassa [Myyntitilauksen tietojen käsitteleminen](marketing-integrate-dynamicscrm.md#handling-sales-order-data)

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] integroituu vain [!INCLUDE[crm_md](includes/crm_md.md)]in kanssa. Muut Dynamics 365 -sovellukset, jotka muuttavat [!INCLUDE[crm_md](includes/crm_md.md)]:n vakiotyönkulkua tai tietomallia (kuten Project Service Automation), voivat katkaista [!INCLUDE[d365fin](includes/d365fin_md.md)]:n ja [!INCLUDE[crm_md](includes/crm_md.md)]:n integroinnin.

## <a name="coupling-records"></a>Tietueiden yhdistäminen
Voit valita synkronoitavat tiedot asetusten ohjatussa määrityksessä. Voit määrittää myöhemmin myös tiettyjen tietojen synkronoinnin. Tätä kutsutaan *yhdistämiseksi*. Voit esimerkiksi yhdistää tietyn [!INCLUDE[crm_md](includes/crm_md.md)]-tilin tiettyyn [!INCLUDE[d365fin](includes/d365fin_md.md)] -asiakkaaseen. Tässä osassa käsitellään seikkoja, jotka on otettava huomioon tietueiden yhdistämisessä.

Jos haluat nähdä [!INCLUDE[crm_md](includes/crm_md.md)]-tilit [!INCLUDE[d365fin](includes/d365fin_md.md)]:n asiakkaina, kaksi tietuetyyppiä on yhdistettävä. Se tehdään käyttämällä [!INCLUDE[d365fin](includes/d365fin_md.md)]in **Asiakkaat**-luettelosivun **Määritä yhdistäminen** -toimintoa. Määritä sitten, mitkä [!INCLUDE[d365fin](includes/d365fin_md.md)] -asiakkaat vastaavat tiettyjä [!INCLUDE[crm_md](includes/crm_md.md)]-tilejä.

Voit myös luoda (ja yhdistää) [!INCLUDE[crm_md](includes/crm_md.md)]-tilin esimerkiksi [!INCLUDE[d365fin](includes/d365fin_md.md)] -asiakastietueen avulla käyttämällä **Dynamics 365 Salesin tilin luominen** -kohtaa tai päinvastoin **Asiakkaan luominen [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssä** -kohtaa.

Kun määrität tietueiden välisen yhdistämisen, voit myös manuaalisesti pyytää, että nykyinen tietue, kuten asiakas, korvataan heti Salesin (tai [!INCLUDE[d365fin](includes/d365fin_md.md)]in) tilitiedoilla. Käytä siinä tapauksessa **Synkronoi nyt** -toimintoa. **Synkronoi nyt** -toiminto kysyy, korvataanko Sales- vai [!INCLUDE[d365fin](includes/d365fin_md.md)]-tietueen tiedot.

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
Asetusten ohjatun määritysoppaan lopussa voit valita **Suorita täysi synkronointi** -toiminnon ja aloittaa kaikkien [!INCLUDE[d365fin](includes/d365fin_md.md)] tietueiden synkronoinnin [!INCLUDE[crm_md](includes/crm_md.md)]:n liittyvien tietueiden kanssa. Valitse **Täyden Dynamics 365 Sales -synkronoinnin tarkistus** -sivulla **Aloita**-toiminto. Täysi synkronointi voi kestään jonkin aikaa, mutta voit jatkaa [!INCLUDE[d365fin](includes/d365fin_md.md)]:n käyttöä samalla, kun synkronointi tapahtuu taustalla.

Voit tarkistaa täyden synkronoinnin yksittäisten töiden etenemisen valitsemalla **Dynamics 365 Sales -sovelluksen täyden synkronoinnin tarkistus** -sivulla tietueen, jonka tiedot haluat tarkistaa. Voit päivittää tilan synkronoinnin aikana päivittämällä sivun.

Saat **Microsoft Dynamics 365 -yhteyden määritys** -sivulla koska tahansa tietoja täydestä synkronoinnista. Voit avata siellä myös **Integrointitaulukon yhdistämismääritykset** -sivun, jossa on tietoja synkronoitavista [!INCLUDE[d365fin](includes/d365fin_md.md)] in ja Salesin taulukoista.

## <a name="handling-sales-order-data"></a>Myyntitilauksen tietojen käsitteleminen
Salesin [!INCLUDE[crm_md](includes/crm_md.md)]iin lähetyt myyntitilaukset siirretään automaattisesti [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, jos valitset **Luo myyntitilaukset automaattisesti** -valintaruudun **Microsoft Dynamics 365 -yhteyden määrittäminen** -sivulla.
Vaihtoehtoisesti voi muuntaa [!INCLUDE[crm_md](includes/crm_md.md)]ista lähetyt myyntitilaukset manuaalisesti käyttämällä **Luo [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa** -toimintoa **Myyntitilaukset – Dynamics 365 for Sales** -sivulla.
Näissä myyntitilauksissa alkuperäisen tilauksen **Nimi**-kenttä siirretään ja yhdisetään myyntitilauksen **Ulkoisen asiakirjan numero** -kenttään [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa.

Tämä voi toimia myös, jos alkuperäinen myyntitilaus sisältää käsin lisättyjä tuotteita eli nimikkeitä tai resursseja, joita ei ole rekisteröity kumpaankaan sovellukseen. Tällöin tulee antaa **Käsin lisätyn tuotteen tyyppi**- ja **Käsin lisätyn tuotteen numero** -kentät **Myynnin ja myyntisaamisten asetukset** -sivulla. Tällöin ei-rekisteröity tuotemyynti yhdistetään talousanalyysissa tiettyyn nimike- tai resurssinumeroon.

Jos alkuperäisen myyntitilauksen nimikkeen kuvaus on hyvin pitkä, sitä varten [!INCLUDE[d365fin](includes/d365fin_md.md)]in myyntitilaukseen luodaan lisämyyntitilausrivi, jonka tyyppi on **Kommentti**.

Päivittää myyntitilauksen otsikkojen kentät, kuten Viimeisin toimituspvm tai Pyydetty toimituspvm. Kentät on yhdistetty SALESORDER-ORDER- **integrointitaulukon yhdistämismääritys** -kohtaan. Ne synkronoidaan säännöllisesti [!INCLUDE[crm_md](includes/crm_md.md)]-sovellukseen. Prosessit, kuten myyntitilauksen vapauttaminen ja myyntitilauksen lähettäminen tai laskuttaminen, kirjataan myyntitilauksen aikajanalle [!INCLUDE[crm_md](includes/crm_md.md)]issa. Lisätietoja on kohdassa [Aktiviteettisyötteiden esittely](/dynamics365/sales-enterprise/developer/introduction-activity-feeds). <!--The link is broken. Should this actually point to https://docs.microsoft.com/en-us/dynamics365/sales-enterprise/manage-activities-->

> [!NOTE]  
> Jaksoittainen synkronointi SALESORDER-ORDER -**integrointitaulukon yhdistämismäärityksenä** toimii vain, kun myyntitilauksen integrointi on otettu käyttöön. Lisätietoja on kohdassa [Sales-yhteyden määritykset -sivun yhteysasetukset](admin-prepare-dynamics-365-for-sales-for-integration.md). Vain [!INCLUDE[crm_md](includes/crm_md.md)]:n lähetetyistä myyntitilauksista luodut myyntitilaukset synkronoidaan. Lisätietoja on kohdassa [Myyntitilauksen käsittelyn integroinnin käyttöönotto](/dynamics365/sales-enterprise/developer/enable-sales-order-processing-integration).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098170]

## <a name="handling-sales-quotes-data"></a>Myyntitarjouksen tietojen käsitteleminen
[!INCLUDE[crm_md](includes/crm_md.md)]issa aktivoidut myyntitarjoukset siirretään [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, jos valitset **Käsittele myyntitarjoukset automaattisesti** -valintaruudun **Microsoft Dynamics 365 -yhteyden määrittäminen** -sivulla.
Vaihtoehtoisesti voit muuntaa [!INCLUDE[crm_md](includes/crm_md.md)]ista aktivoidut myyntitarjoukset manuaalisesti käyttämällä **Käsittele [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa** -toimintoa **Myyntitarjoukset – Dynamics 365 Sales** -sivulla.
Näissä myyntitarjouksissa alkuperäisen tarjouksen **Nimi**-kenttä siirretään ja yhdistetään myyntitilauksen **Ulkoisen asiakirjan numero** -kenttään [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Myös tarjouksen **Voimassaolo päättyy** -kenttä siirretään ja yhdistetään myyntitarjouksen **Tarjouksen voimassaolon päättymispäivä** -kenttään [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.  

Myyntitarjouksia muokataan useita kertoja viimeistelyn aikana. Myyntitarjousten manuaalinen ja automaattinen käsittely [!INCLUDE[d365fin](includes/d365fin_md.md)]issa varmistaa, että myyntitarjousten edelliset versiot arkistoidaan ennen uusien myyntitarjousten käsittelyä [!INCLUDE[crm_md](includes/crm_md.md)]ista.

## <a name="handling-posted-sales-invoices-customer-payments-and-statistics"></a>Kirjattujen myyntilaskujen, asiakkaiden maksujen ja tilastojen käsitteleminen
Kun myyntitilaus on täytetty, siitä luodaan lasku. Kun myyntitilaus luodaan, kirjattu myyntilasku voidaan siirtää [!INCLUDE[crm_md](includes/crm_md.md)]:ään, jos **Kirjattu myyntilasku** -sivun **Luo lasku [!INCLUDE[crm_md](includes/crm_md.md)]:ssä** -valintaruutu on valittu. Kirjatut laskut siirretään [!INCLUDE[crm_md](includes/crm_md.md)]:ään **Laskutettu**-tilassa.

Kun asiakasmaksu vastaanotetaan myyntilaskulle sovelluksessa [!INCLUDE[d365fin](includes/d365fin_md.md)], myyntilaskun tilaksi muutetaan **Maksettu** ja **Tilan syy** -kentän arvoksi määritetään **Osittainen**, jos lasku on maksettu osittain, tai **Kokonaan**, jos lasku on maksettu kokonaan, kun valitset **Päivitä tilin tiedot** -toiminnon [!INCLUDE[d365fin](includes/d365fin_md.md)] -asiakkaan sivulla. **Päivitä tilin tiedot** -toiminto päivittää myös arvot, kuten **Saldo**- ja **Kokonaismyynti**-kenttien arvot **[!INCLUDE[d365fin](includes/d365fin_md.md)] -tilin tiedot** -tietoruudussa [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksessa. Vaihtoehtoisesti voit käyttää ajastettuja töitä, asiakastilastoja ja POSTEDSALESINV-INV-kohdetta, jos nämä prosessit suoritetaan automaattisesti taustalla.

## <a name="see-also"></a>Katso myös
[Dynamics 365 Sales -integrointi](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Liikesuhteiden hallinta](marketing-relationship-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md)    
[Salesin ja myyntikeskuksen yleiskuvaus](/dynamics365/customer-engagement/sales-enterprise/overview)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
