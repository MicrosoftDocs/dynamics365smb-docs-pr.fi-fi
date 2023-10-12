---
title: Microsoft Dataverse -sovelluksen käyttäminen
description: 'Johdatus siihen, miten Microsoft Dataversen ja sen komponentit voi integroida ja miten niitä voi käyttää yhteyden muodostamiseksi muihin Dynamics 365 -sovelluksiin.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 06/28/2023
ms.custom: bap-template
---

# Microsoft Dataverse-integrointi

Yrityssovelluksissa käytetään usein tietoja useista lähteistä. [!INCLUDE[prod_short](includes/cds_long_md.md)] yhdistää tiedot yhdeksi logiikkajoukoksi, jonka avulla on helppo yhdistää [!INCLUDE[prod_short](includes/prod_short.md)] muihin Dynamics 365 -sovelluksiin. Yhdistettävä sovellus voi olla esimerkiksi [!INCLUDE[crm_md](includes/crm_md.md)] tai oma sovellus, joka perustuu [!INCLUDE[prod_short](includes/cds_long_md.md)]-sovellukseen. Lisätietoja [!INCLUDE[prod_short](includes/cds_long_md.md)]sta on kohdassa [Mikä on Dataverse?](/powerapps/maker/common-data-service/data-platform-intro).

Seuraavat ohjeet käsittelevät [!INCLUDE[prod_short](includes/cds_long_md.md)]in ja [!INCLUDE[prod_short](includes/prod_short.md)]in integrointia.

> [!Note]  
> Näiden tehtävien suorittaminen vaatii **Järjestelmänvalvoja** käyttöoikeusroolin [!INCLUDE[prod_short](includes/cds_long_md.md)]ssa ja [!INCLUDE[prod_short](includes/prod_short.md)]ssa  

1. Määritä [!INCLUDE[prod_short](includes/cds_long_md.md)]in käyttöoikeudet niille [!INCLUDE[prod_short](includes/prod_short.md)]in käyttäjille, jotka käyttävät integroituja sovelluksia.

2. Määritä [!INCLUDE[prod_short](includes/cds_long_md.md)] -yhteys. Lisätietoja on kohdassa [Yhteyden muodostaminen Dataverse -sovellukseen](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Synkronoi tiedot sovellusten välillä. Lisätietoja on kohdassa [Business Centralin ja Dataversein synkronointi](admin-synchronizing-business-central-and-sales.md). 

## Aloita [!INCLUDE[prod_short](includes/cds_long_md.md)]in käyttö

Jos haluat aloittaa [!INCLUDE[prod_short](includes/cds_long_md.md)]n käyttämisen, tarvitset Microsoft Power Apps -tilin. Jos sinulla ei vielä ole Power Apps -tiliä, saat ilmaisen tilin käymällä osoitteessa [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) ja valitsemalla **Aloita ilmaiseksi** -linkin. Lisätietoja [!INCLUDE[prod_short](includes/cds_long_md.md)]n käyttämisen aloittamisesta on [Dataversen käytön aloittaminen](/training/modules/get-started-with-powerapps-common-data-service/) -moduulissa Microsoftin koulutuksissa.

## Kaksisuuntainen tai yksisuuntainen tietojen synkronointi

Voit määrittää integroinnin synkronoimaan tiedot joko Dynamics 365 -liiketoimintasovelluksesta toiseen tai molempiin suuntiin reaaliaikaisesti [!INCLUDE[prod_short](includes/cds_long_md.md)]n avulla. Jos esimerkiksi integroit sovelluksen [!INCLUDE[prod_short](includes/prod_short.md)] sovelluksen [!INCLUDE[crm_md](includes/crm_md.md)] kanssa, myyjä voi luoda myyntitilauksen sovelluksessa [!INCLUDE[crm_md](includes/crm_md.md)]. Tämän jälkeen tilaus synkronoidaan sovellukseen [!INCLUDE[prod_short](includes/prod_short.md)]. Vastaavasti [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksessa myyjä voi tarkistaa nimikkeen saatavuuden [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen tilauksessa. 

## Vakioentiteetit ja mukautetut entiteetit

[!INCLUDE[prod_short](includes/cds_long_md.md)] tallentaa tiedot turvallisesti taulukkojoukkoihin. Ne ovat samanlaisia joukkoja kuin taulukon tallentamat tiedot tietokannassa. [!INCLUDE[prod_short](includes/cds_long_md.md)] sisältää tavalliset skenaariot kattavien vakiotaulukoiden perusjoukon. Voit luoda myös organisaatiokohtaisia mukautettuja taulukoita. [!INCLUDE[prod_short](includes/prod_short.md)]:ssä voit tarkastella vakiotaulukoita ja mukautettuja taulukoita, jotka synkronoidaan Integrointitaulukon yhdistämismääritykset -sivulla.

## Tietoja Business Central -perusintegrointiratkaisusta

Perusintegraatioratkaisu on integroinnin avainosa. Ratkaisu lisää vaaditut roolit ja käyttöoikeustasot integroinnin käyttäjätileille ja luo taulukot, jotka tarvitaan [!INCLUDE[prod_short](includes/prod_short.md)] -yrityksen yhdistämisessä liiketoimintayksikköön [!INCLUDE[prod_short](includes/cds_long_md.md)] -sovelluksessa. 

Oletusarvoisesti **[!INCLUDE[prod_short](includes/cds_long_md.md)]n yhteyden määrityksen** asetusten ohjattu määritysopas tuo ratkaisun. Tämän vuoksi asennusopas käyttää määrittämääsi järjestelmänvalvojan käyttäjätiliä. Tämän tilin on oltava [!INCLUDE[prod_short](includes/cds_long_md.md)]n hyväksytty käyttäjä, jolla on seuraava käyttöoikeusrooli:

* järjestelmänvalvoja  

Lisätietoja käyttäjätileistä on seuraavissa artikkeleissa:

* [[!INCLUDE[prod_short](includes/cds_long_md.md)] -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md) 
* [Luo käyttäjät Microsoft Dynamics 365 (online) -sovelluksessa ja määritä käyttöoikeusroolit](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) 

Järjestelmänvalvojan tiliä käytetään vain kerran asennuksen aikana kokoonpanon muutosten takia, jotka perusintegrointiratkaisu tekee [!INCLUDE[prod_short](includes/cds_long_md.md)]ssa. Kun ratkaisu on tuotu, tiliä ei enää tarvita. Integrointi jatkaa integrointia varten automaattisesti luodun käyttäjätilin käyttämistä.

[!INCLUDE[prod_short](includes/cds_long_md.md)]:n mukauttamisen lisäksi ratkaisu luo integrointia varten myös seuraavat roolit [!INCLUDE[prod_short](includes/cds_long_md.md)]:ssä:

* **Integroinnin järjestelmänvalvoja** – Antaa käyttäjille mahdollisuuden [!INCLUDE[prod_short](includes/prod_short.md)]in ja [!INCLUDE[prod_short](includes/cds_long_md.md)]in välisen yhteyden hallintaan. Yleensä tämä rooli määritetään vain käyttäjätilille, joka on luotu automaattisesti synkronointia varten.  
* **Integroinnin käyttäjä** – Antaa käyttäjille mahdollisuuden käyttää synkronoituja tietoja. Yleensä tämä rooli liitetään seuraaville käyttäjätileille:

  * käyttäjätilit, jotka luodaan automaattisesti synkronointia varten
  * muut käyttäjät, jotka tarvitsevat synkronoitujen tietojen käyttöoikeuden.

Lisätietoja kustakin roolista, kuten käyttöoikeuksista ja käyttöoikeustasoista, on kohdassa [[!INCLUDE[prod_short](includes/cds_long_md.md)]-integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md).

Luo yhteyden muodostamisen aikana integrointitaulukon yhdistämismääritykset, joita tarvitaan tietojen synkronoimiseen. [!INCLUDE[prod_short](includes/cds_long_md.md)]n entiteetit yhdistetään taulukoihin ja taulukkokenttiin [!INCLUDE [prod_short](includes/prod_short.md)]issa integrointitaulukoiden kautta. Lisätietoja yhdistämismäärityksistä on kohdassa [Synkronoinnin vakioentiteetin yhdistämismääritys](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## Erojen käsitteleminen paikallisina valuuttoina ja perustapahtumavaluuttoina

Voit muodostaa yhteyden [!INCLUDE[prod_short](includes/cds_long_md.md)]-ympäristöön, jonka perusvaluutta on eri kuin paikallinen valuutta [!INCLUDE[prod_short](includes/prod_short.md)]issa. Voit muodostaa yhteyden [!INCLUDE[prod_short](includes/prod_short.md)]iin **Dataverse-yhteyden asetukset** -sivulla tai käyttämällä **Dataversen yhteyden määrityksen** ohjattua määritysopasta.

Voit muodostaa yhteyden varmistettuasi, että perustapahtumavaluutan määrityksessä [!INCLUDE[prod_short](includes/cds_long_md.md)]issa on annettu valuutta, joka on määritetty **Valuutat**-sivulla [!INCLUDE [prod_short](includes/prod_short.md)]issa ja valuutalle on määritetty vähintään yksi valuuttakurssi **Valuutan vaihtokurssit** -sivulla.

Esimerkki: Olet muodostamassa yhteyttä [!INCLUDE[prod_short](includes/cds_long_md.md)]sta niin, että paikalliseksi valuutaksi on määritetty euro (EUR) [!INCLUDE[prod_short](includes/cds_long_md.md)]-ympäristön **Pääkirjanpidon asetukset** -sivun mukaan. Siellä perustapahtumavaluutaksi on määritetty Yhdysvaltain dollari (USD). **Valuutat**-sivulla [!INCLUDE [prod_short](includes/prod_short.md)]issa on oltava valittuna USD ja soveltuva vaihtokurssi. 

Kun yhteys [!INCLUDE[prod_short](includes/cds_long_md.md)]en, [!INCLUDE [prod_short](includes/prod_short.md)] lisää sen paikallisen valuutan **Valuutta**-entiteettiin [!INCLUDE[prod_short](includes/cds_long_md.md)]ssa yhdessä **Valuutan vaihtokurssit** -sivun **Valuuttakerroin**-kentän vaihtokurssin kanssa.

Valuutan synkronointi on yksisuuntaista [!INCLUDE [prod_short](includes/prod_short.md)]ista [!INCLUDE [!INCLUDE[prod_short](includes/cds_long_md.md)]en. Rahamääräiset summat muunnetaan ja synkronoidaan seuraavasti:

* [!INCLUDE[prod_short](includes/cds_long_md.md)]n perusvaluutan summat muunnetaan [!INCLUDE [prod_short](includes/prod_short.md)]in paikalliseksi valuutaksi [!INCLUDE [prod_short](includes/prod_short.md)]ista synkronoidun uusimman vaihtokurssin perusteella.
* [!INCLUDE [prod_short](includes/prod_short.md)]in paikallisen valuutan summat synkronoidaan [!INCLUDE [prod_short](includes/prod_short.md)]in paikallisen valuutan kanssa jonakin muuna valuuttana (ei perusvaluuttana) [!INCLUDE[prod_short](includes/cds_long_md.md)]ssa.

## Katso myös

[Tietojen omistusmallit](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
