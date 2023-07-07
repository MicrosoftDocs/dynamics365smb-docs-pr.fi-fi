---
title: Asiakkaiden hallinta Dynamics 365 Salesin avulla (sisältää videon) | Microsoft Docs
description: Voit käyttää Dynamics 365 Salesia Business Centralissa, jolloin saavutetaan liidistä tuottoon -prosessin saumaton integrointi ja synkronointi.
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map, Sales
ms.search.forms: 9980, 5341, 5349, 5330, 1817, 5342, 5337, 5336, 5331, 5343, 5334, 5346, 5348, 5329, 5380, 5353, 5381, 5351, 5333, 5360, 5373, 5371, 5340, 5345, 5362, 1313, 5361, 1876, 5339, 5338, 5335, 5332, 6250
ms.date: 09/16/2022
ms.author: bholtorf
ms.openlocfilehash: 46055056fc17b4997b5e49ccefe8cd104bef0a6d
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585862"
---
# <a name="use-dynamics-365-sales-from-business-central"></a>Dynamics 365 Salesin käyttäminen Business Centralissa
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

Päivittää myyntitilauksen otsikkojen kentät, kuten Viimeisin toimituspvm tai Pyydetty toimituspvm. Kentät on yhdistetty **MYYNTITILAUS-TILAUS**-integrointitaulukon yhdistämismääritys -kohtaan. Ne synkronoidaan säännöllisesti [!INCLUDE[crm_md](includes/crm_md.md)]-sovellukseen. Prosessit, kuten myyntitilauksen vapauttaminen, lähettäminen ja laskuttaminen, kirjataan myyntitilauksen aikajanalle [!INCLUDE[crm_md](includes/crm_md.md)]issa. Lisätietoja on kohdassa [Aktiviteettisyötteiden esittely](/dynamics365/sales-enterprise/manage-activities). Jos haluat ottaa käyttöön [!INCLUDE[crm_md](includes/crm_md.md)] -ohjelman tilausten kirjauksen ja aktiviteetit, katso lisätietoja [Muistiinpanot-ohjausobjektin määrittäminen mukautetun entiteetin julkaisuja koskevien tietojen käyttämiseksi](/dynamics365/customerengagement/on-premises/customize/notes-control-legacy) Customer Engagement -dokumentaatiossa. Tämä artikkeli viittaa Customer Engagement on-premisesiin, mutta vaiheet ovat samat online-versiolle. <!--The /dynamics365/sales-enterprise/developer/introduction-activity-feeds link was broken. Should this actually point to /dynamics365/sales-enterprise/manage-activities-->

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

## <a name="handling-sales-prices"></a>Myyntihintojen käsitteleminen
> [!NOTE]
> Vuoden 2020 julkaisuaallossa 2 julkaisimme virtaviivaiset prosessit hintojen ja alennusten määritykseen ja hallintaan. Jos olet uusi asiakas, joka käyttää kyseistä versiota, käytät uutta käyttökokemusta. Jos olet jo asiakas, uuden käyttöokemuksen käyttö riippuu siitä, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuden päivityksen **ominaisuuksien hallinnassa**. Lisätietoja on kohdassa [Tulevien ominaisuuksien ottaminen käyttöön etuajassa](/dynamics365/business-central/dev-itpro/administration/feature-management).

Prosessin viimeistelyvaiheet ovat erilaiset sen mukaan, onko järjestelmänvalvoja ottanut käyttöön uuden myyntihinnoittelukokemuksen vai ei. 

> [!NOTE]
> Jos vakiohinnan synkronointi ei toimi, suosittelemme integroinnin mukautusominaisuuksien käyttämistä. Lisätietoja on kohdassa [Microsoft Dataverse -palvelun avulla integroimisen mukauttaminen](/dynamics365/business-central/dev-itpro/administration/administration-custom-cds-integration).

#### [Nykyinen kokemus](#tab/current-experience/)
Nykyisessä hinnoittelukokemuksessa [!INCLUDE[prod_short](includes/prod_short.md)] synkronoi myyntihinnan, joka: 

* Kohdistetaan kaikkiin asiakkaisiin. Oletusmyyntihinnastot luodaan nimikkeiden **Nimikekortti**-sivun **Yksikköhinta**-kentän hinnan mukaan.
* Kohdista tiettyyn asiakkaan hintaryhmään. Esimerkiksi vähittäismyynti-tai tukkuasiakkaiden myyntihinnat. Voit synkronoida hinnat asiakkaan hintaryhmän perusteella seuraavasti:

    1. Yhdistä nimikkeet, joiden hinnat asiakkaan hintaryhmä määrittää.
    2. Yhdistä asiakkaan hintaryhmä **Asiakkaan hintaryhmät**-sivulla valitsemalla **Liittyvät**, sitten **Dynamics 365 Sales**, **Yhdistäminen** ja lopuksi **Määritä yhdistäminen**. Yhdistäminen luo aktiivisen hinnaston tuotteelle [!INCLUDE[prod_short](includes/prod_short.md)] samalla nimellä kuin asiakkaan hintaryhmä tuotteella [!INCLUDE[crm_md](includes/crm_md.md)]. Kaikki ne nimikkeet synkronoidaan automaattisesti, joiden asiakkaan hintaryhmä määrittää hinnan.

:::image type="content" source="media/customer-price-group.png" alt-text="Asiakkaan hintaryhmä -sivu.":::

#### [Uusi kokemus](#tab/new-experience/)  

Uusi hinnoittelukokemus synkronoi hinnastot, jotka täyttävät seuraavat ehdot:

* **Salli oletusarvojen päivittäminen** on poistettu käytöstä.
* HIntatyyppi on Myynti.
* Summatyyppi on Hinta.
* Rivin tuotetyypin on oltava Nimike tai Resurssi. 
* Vähimmäismäärää ei ole määritetty.

[!INCLUDE[prod_short](includes/prod_short.md)] synkronoi myyntihinnat, jotka koskevat kaikkia asiakkaita.. Oletusmyyntihinnastot luodaan nimikkeiden **Nimikekortti**-sivun **Yksikköhinta**-kentän hinnan mukaan.

Voit synkronoida hinnastot valitsemalla **Myyntihinnasto**-sivulla **Liittyvät**, **Dynamics 365 Sales**, **Yhdistäminen** ja lopuksi **Määritä yhdistäminen**. 

:::image type="content" source="media/sales-price-list.png" alt-text="Myyntihinnasto-sivu.":::

---


## <a name="see-also"></a>Katso myös
[Dynamics 365 Sales -integrointi](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Liikesuhteiden hallinta](marketing-relationship-management.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md)    
[Salesin ja myyntikeskuksen yleiskuvaus](/dynamics365/customer-engagement/sales-enterprise/overview)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
