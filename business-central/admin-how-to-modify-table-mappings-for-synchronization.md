---
title: Synkronoitavissa olevien taulukoiden ja kenttien yhdistämismääritys
description: Tietoja taulujen ja kenttien yhdistämistietojen synkronoinnista Business Centralin ja Microsoft Dataversen välillä.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 08/07/2024
ms.custom: bap-template
ms.search.keywords: 'sales, crm, integration, sync, synchronize, table mapping'
ms.service: dynamics-365-business-central
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>Synkronoitavissa olevien taulukoiden ja kenttien yhdistämismääritys

Tietojen synkronointi [!INCLUDE[prod_short](includes/prod_short.md)]in taulukoiden ja kenttien yhdistämiseen [!INCLUDE[prod_short](includes/cds_long_md.md)]n taulukoihin ja sarakkeisiin, jotta sovellukset voivat vaihtaa tietoja. Yhdistäminen tapahtuu integrointitaulujen avulla.

## <a name="mapping-integration-tables"></a>Integrointitaulujen yhdistämismääritys

Integrointitaulu on [!INCLUDE[prod_short](includes/prod_short.md)] -tietokannassa, joka edustaa taulukkoa, kuten tiliä, [!INCLUDE[cds_long_md](includes/cds_long_md.md)]ssa. integrointitaulut sisältävät kenttiä, jotka vastaavat sarakkeita [!INCLUDE[cds_long_md](includes/cds_long_md.md)] -taulukossa. Esimerkiksi Tilin integrointi -taulu muodostaa yhteyden Tilit-taulukkoon [!INCLUDE[cds_short_md](includes/cds_long_md.md)]ssa. Jokaista [!INCLUDE[cds_short_md](includes/cds_short_md.md)]in taulukkoa kohden, jonka haluat synkronoida [!INCLUDE[prod_short](includes/prod_short.md)]ssa olevien tietojen kanssa, on oltava integraatiotaulun yhdistämismääritys.

Kun luot yhteyden sovellusten välille, [!INCLUDE[prod_short](includes/prod_short.md)] määrittää joitakin oletusarvoisia yhdistämismäärityksiä. Halutessasi voit myös muuttaa taulujen yhdistämismäärityksiä. Lisätietoja on kohdassa [Synkronoinnin vakiotaulukoiden yhdistämismääritys](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization). Jos olet muuttanut oletusmäärityksiä ja haluat peruuttaa tekemäsi muutokset, valitse **Integrointitaulukon yhdistämismääritykset** -sivulla **Käytä oletussynkronointiasetuksia**.

> [!Note]
> Jos käytössä on [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -versio, integrointitaulun yhdistämismääritykset tallennetaan taulun 5335 integrointitaulukon yhdistämismäärityksiin, jossa voit tarkastella ja muokata yhdistämismäärityksiä. Monimutkaiset yhdistämismääritykset ja synkronoinnin säännöt on määritetty codeunitissa 5341.

> [!TIP]
> Kun kytkettyjä tietueita muutetaan, [!INCLUDE [prod_short](includes/prod_short.md)] synkronoi tiedot automaattisesti Dataversen kanssa. Automaattinen synkronointi on useimmissa tapauksissa hyvä. Usein tehtävät muutokset suuriin taulukon yhdistettyjen tietueiden määriin voivat kuitenkin hidastaa tietojen synkronointia.
>
> Jotta suorituskyky ei hidastuisi, voit ottaa käyttöön tai poistaa käytöstä tapahtumapohjaisen tietojen synkronoinnin mihin tahansa taulukkoon **integrointi taulukon yhdistämiset** -sivulla. Oletusarvon mukaan tapahtumiin perustuva synkronointi on käytössä, joten aiemmin luodut integroinnit eivät muutu. Järjestelmänvalvoja voi ottaa sen käyttöön tai poistaa sen käytöstä tiettyjen taulukoiden osalta.

### <a name="add-table-and-field-mappings-to-existing-integration-tables"></a>Taulukon ja kentän linkitysten lisääminen aiemmin luotuihin integrointitaulukoihin

 **Linkitys** integrointitaulukko sivun Uusi taulukon yhdistämismääritys -toiminnon avulla voit lisätä uusia taulukoiden linkitystoimintoja integrointitaulukoihin. Toiminto käynnistää **Luo uusia integrointikartoituksia** -avustetun asetusoppaan, jonka avulla voit määrittää uusia integrointitaulukko ja kenttien määritykset.

Oppaassa [!INCLUDE [prod_short](includes/prod_short.md)] voit linkittää taulukoita aiemmin luotujen integrointitaulukoiden kanssa Dataverse. Voit myös määrittää Dataverse taulukon yksilöivän tunnuksen kohdassa **integrointitaulukko Yksilöllinen tunnus -kentän nimi** ja **integrointitaulukko Muokattu kentän nimellä**, jotta tietojen synkronointi toimisi.

> [!NOTE]
> Taulukon sarakkeen haussa näkyvät kaikki [!INCLUDE [prod_short](includes/prod_short.md)] taulukot, myös mukautettuja taulukoita, joita ei ole vielä linkity. Se sulkee pois integrointitaulukko määritykset -sivulla jo olevat tiedot. integrointitaulukko-sarakkeen haussa näkyvät vain Dataverse taulukot (AL-hakutaulukot), jotka ovat osa out-of-the-box -integrointeja. Lisätaulukoiden tai mukautettujen Dataverse taulukoiden lisääminen edellyttää kehittäjän apua, kun luot ja otat ne käyttöön laajennuksen kautta.

Lisätoiminto avaa taulukon yhdistämismääritys lisäasetuksia, joita voi määrittää. Lisäosassa **Taulukon** suodatus **-** kentän avulla voit määrittää suodattimia. [!INCLUDE [prod_short](includes/prod_short.md)]  **Käytä tietojen integrointitaulukko suodatus** -kenttää Dataverse , jotta tiedot voidaan synkronoida yhdessä Taulukon config -taulukon asetusasetusten määritysmallin koodien **kanssa. Mallin koodi** ja **Laskutoimitt. määritykset Koodi** puuttuvien tietojen ennakkoon, kun uusi tieto tulee kummastakin kohdistuksesta.

Oppaasta on myös hyötyä uusien yhdistämismääritys sisällytettävien kenttien määrittämisessä. Voit yhdistää Kentän nimi [!INCLUDE [prod_short](includes/prod_short.md)] -sarakkeen **kentän** nimen Integrointikentän nimi Dataverse -sarakkeeseen **.**  Voit myös määrittää **Suunnan**, sen, onko kentässä aina sama arvo Vakio-sarakkeessa **·**, ja onko kenttien yhdistämismääritys käytettävä tarkistuksia tai muutoksia.

> [!NOTE]
> Virheiden **vähentämiseksi integrointitaulukko Kenttä-sarakkeen** suodattimet käytettävissä olevien kenttien luetteloon. Jos haluat linkittää kenttiä, joita suodattimet eivät sisällä, tarvitset kehittäjän apua.
>
> * Kenttien on oltava käytössä.
> * Et voi käyttää opasta FlowField- ja FlowFilter-kenttien linkittämiseen.
> * Voit linkittää vain kenttiä, jotka ovat tyyppiä BigInteger, totuusarvo, Koodi, Pvm, PvmFormula, PvmAika, Desimaali, Kesto, GUID, Kokonaisluku, Vaihtoehto ja Teksti.

> [!TIP]
> Voit myös lisätä uusia kenttien linkitysmahdollisuuksia olemassa oleviin integrointitaulukko linkitykset Integrointikenttien linkitys -luettelosivun avulla **. Voit käyttää kenttiä valitsemalla** Kentät **·**  integrointitaulukko Linkitys-sivulta **.** 
>
> Valitse **yksinkertaisesti Uusi kenttä yhdistämismääritys**  aukaisen Luo uudet integrointimääritykset **-avusteisen** asetusoppaan yhdistämismääritys vaihe kenttä ja jatka sitten tässä artikkelissa kuvatulla tavalla.

Aiemmin luotuun taulukon yhdistämismääritys lisättävät uudet kenttien linkitykset ovat poissa käytöstä -tilassa. Voit ottaa ne käyttöön myöhemmin valitsemalla **Muokkaa luetteloa** .

### <a name="synchronization-rules"></a>Synkronointisäännöt

Integrointitaulun yhdistämismääritys sisältää myös sääntöjä, jotka ohjaavat sitä, miten integroinnin synkronointityöt synkronoivat [!INCLUDE[prod_short](includes/prod_short.md)] -taulun tietueet [!INCLUDE[prod_short](includes/cds_long_md.md)] -taulun kanssa. Esimerkkejä myynnin integrointia koskevista säännöistä on [synkronointisäännöissä](#synchronization-rules).

### <a name="strategies-for-auto-resolving-conflicts"></a>Strategiat konfliktien automaattista ratkaisemista varten

Tietoristiriitoja voi ilmetä helposti, kun yrityssovellukset vaihtavat tietoja jatkuvasti. Joku voi esimerkiksi poistaa tai muuttaa jommankumman sovelluksen tai molempien sovellusten rivejä. Jos haluat vähentää manuaalisesti ratkaistavien ristiriitojen määrää, voit määrittää ratkaisustrategioita ja [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelma voi ratkaista ristiriidat automaattisesti strategioiden sääntöjen mukaan.

Integrointitaulukon yhdistämisiin kuuluvat säännöt, jotka ohjaavat synkronoinnin töiden synkronointitietueita. Voit määrittää **integrointitaulukon linkitys** -sivun **Ratkaise poistoristiriidat**- ja **Ratkaise päivitysristiriidat** -sarakkeiden avulla, miten [!INCLUDE[prod_short](includes/prod_short.md)] ratkaisee ristiriidat, jotka tapahtuvat, koska tietueita poistettiin yhden tai toisen yrityssovelluksen taulukoissa tai päivitetään molemmissa. 

**Ratkaise poistoristiriidat** -sarakkeessa voit valita haluatko, että [!INCLUDE[prod_short](includes/prod_short.md)] palauttaa poistetut tietueet automaattisesti, poistaa tietueiden välisen kytkennän tai ei tee mitään. Jos et tee mitään, sinun täytyy ratkaista ristiriidat manuaalisesti. 

**Ratkaise päivitysristiriidat** -sarakkeessa voit valita, jos haluat, että [!INCLUDE[prod_short](includes/prod_short.md)] lähettää automaattisesti tietojen päivityksen integrointitaulukkoon, kun lähetät tietoja [!INCLUDE[prod_short](includes/cds_long_md.md)] -ohjelmaan, tai saada tietojen päivityksen integrointitaulukosta, kun tietoja haetaan [!INCLUDE[prod_short](includes/cds_long_md.md)] -ohjelmasta, tai ei tee mitään. Jos et tee mitään, sinun täytyy ratkaista ristiriidat manuaalisesti.

Kun olet määrittänyt strategian, voit ratkaista ristiriidat automaattisesti yrityksen **Tietojen synkronointivirheet** -sivulta **Yritä uudelleen** -toiminnon avulla.

## <a name="mapping-integration-fields"></a>Integraatiokenttien yhdistäminen

Yhdistämistaulut ovat vasta ensimmäinen vaihe. Sinun täytyy myös yhdistää taulujen kentät. Integrointikenttien yhdistämismääritykset linkittävät [!INCLUDE[prod_short](includes/prod_short.md)]taulujen kentät vastaaviin sarakkeisiin [!INCLUDE[prod_short](includes/cds_long_md.md)]ssä ja määrittävät, synkronoidaanko kunkin taulun tiedot. Vakiomuotoinen taulunyhdistämismääritys, jonka [!INCLUDE[prod_short](includes/prod_short.md)] tarjoaa, sisältää kenttien yhdistämismääritykset, mutta voit halutessasi muuttaa niitä. Lisätietoja on kohdassa [Taulukoiden yhdistämismääritysten tarkasteleminen](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-table-mappings).

> [!Note]
> Jos käytössä on paikallinen versio [!INCLUDE[prod_short](includes/prod_short.md)]sta, integrointikenttien yhdistämismääritykset on määritelty taulun 5336 integrointikenttien yhdistämismäärityksessä.

Voit yhdistää kentät manuaalisesti tai voit automatisoida prosessin yhdistämällä useita kenttiä samaan aikaan niiden arvojen vastaavuuskriteerien perusteella. Lisätietoja on kohdassa [Usean tietueen yhdistäminen kentän arvon täsmäytyksen perusteella](admin-how-to-couple-and-synchronize-records-manually.md).

### <a name="handle-differences-in-field-values"></a>Kenttien arvojen erojen käsitteleminen

Joskus kenttien arvot, jotka haluat yhdistää, ovat erilaisia. Esimerkiksi [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksessa Yhdysvaltojen kielikoodi on U.S., mutta [!INCLUDE[prod_short](includes/prod_short.md)]:ssä se on US. Tämä tarkoittaa, että arvo on muunnettava, kun tietoja synkronoidaan. Tämä tapahtuu muutossäännöillä, jotka määrität kentille. Muunnossäännöt määritetään **Integrointitaulukon yhdistämismääritykset** -sivulla valitsemalla **Yhdistämismääritys** ja sitten **Kentät**. Ennalta määritetyt säännöt ovat käytettävissä, mutta voit myös luoda omia sääntöjä. Lisätietoja on kohdassa [Muunnossäännöt](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

### <a name="handle-missing-option-values"></a>Puuttuvien asetusarvojen käsitteleminen

[!INCLUDE[prod_short](includes/cds_long_md.md)] sisältää asetusjoukkokentät, joissa on **Asetus**-tyyppiä oleviin [!INCLUDE[prod_short](includes/prod_short.md)] -sarakkeisiin yhdistettävät arvot automaattista synkronointia varten. Synkronoinnin aikana muut kuin yhdistetyt asetukset ohitetaan ja puuttuvat asetukset liitetään liittyvään [!INCLUDE[prod_short](includes/prod_short.md)] -tauluun ja lisätään **CDS-asetuksen yhdistäminen** -järjestelmätauluun myöhemmin tapahtuvaa manuaalista käsittelemistä varten. Voit esimerkiksi lisätä puuttuvat asetukset tuotteeseen ja päivittää sitten yhdistämismäärityksen. Lisätietoja on kohdassa [Puuttuvien asetusarvojen käsitteleminen](admin-cds-missing-option-values.md).

## <a name="couple-records"></a>Yhdistä tietueet

Kytkentä linkittää rivit kohteessa [!INCLUDE[prod_short](includes/cds_long_md.md)] tietueisiin kohteessa [!INCLUDE[prod_short](includes/prod_short.md)]. Esimerkiksi tilit kohteessa [!INCLUDE[prod_short](includes/cds_long_md.md)] yhdistetään tyypillisesti asiakkaisiin kohteessa [!INCLUDE[prod_short](includes/prod_short.md)]. Kytkentätietueet tarjoavat seuraavat edut:

* Se tekee synkronoinnin mahdolliseksi.
* Käyttäjät voivat avata tietueita tai rivejä yhdessä yrityssovelluksessa toisesta. Tämän edellytyksenä on, että sovellukset on jo integroitu.

Kytkennät voidaan määrittää automaattisesti synkronoinnin töiden avulla tai manuaalisesti muokkaamalla tietuetta kohteessa [!INCLUDE[prod_short](includes/prod_short.md)]. Lisätietoja on kohdassa [Tietojen synkronoiminen kohteessa [!INCLUDE[prod_short](includes/prod_short.md)] ja [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md) ja [Tietueiden kytkeminen ja synkronointi manuaalisesti](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)i.

## <a name="filter-records-and-rows"></a>Suodata tietueet ja rivit

Jos et halua synkronoida kaikkia tietyn [!INCLUDE[prod_short](includes/cds_long_md.md)] -taulukon tai [!INCLUDE[prod_short](includes/prod_short.md)] -taulukon rivejä, voit määrittää suodattimia rajoittamaan synkronoitavia tietoja. Suodattimet määritetään **Integrointitaulukon yhdistämismääritykset** -sivulla.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Integroinnin yhdistämistaulukot** ja valitse sitten liittyvä linkki.
2. Voit suodattaa [!INCLUDE[prod_short](includes/prod_short.md)]in tietueita määrittämällä **Taulukkosuodatus**-kentän.  
3. Voit suodattaa [!INCLUDE[prod_short](includes/cds_long_md.md)]in rivejä määrittämällä **Integrointitaulukon suodatus** -kentän.  

## <a name="create-new-records"></a>Luo uusia tietueita

Oletusarvoisesti vain yhdistetyt [!INCLUDE[prod_short](includes/prod_short.md)]in ja [!INCLUDE[prod_short](includes/cds_long_md.md)]in rivit synkronoidaan integroinnin synkronointitöissä. Voit määrittää taulukon yhdistämismäärityksiä siten, että uudet tietueet tai rivit luodaan kohteeseen (kuten [!INCLUDE[prod_short](includes/prod_short.md)]iin) kullekin lähteen (kuten [!INCLUDE[prod_short](includes/cds_long_md.md)]) riville, jota ei ole vielä yhdistetty.  

Esimerkiksi MYYJÄT - Dynamics 365 Sales -synkronointityö käyttää taulukon yhdistämismääritystä MYYJÄT. Synkronointityö kopioi tiedot [!INCLUDE[prod_short](includes/cds_long_md.md)]in käyttäjistä [!INCLUDE[prod_short](includes/prod_short.md)]in myyjiin. Jos määrität yhdistämismääritykset luomaan uusia tietueita, jokaiselle [!INCLUDE[prod_short](includes/cds_long_md.md)]in käyttäjälle, jota ei vielä ole yhdistetty [!INCLUDE[prod_short](includes/prod_short.md)]in myyjään, luodaan uusi myyjärivi [!INCLUDE[prod_short](includes/prod_short.md)]issa.  

### <a name="to-create-new-records-during-synchronization"></a>Uusien tietueiden luominen synkronoinnin aikana

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Integroinnin yhdistämistaulukot** ja valitse sitten liittyvä linkki.
2. Poista luettelossa taulukon yhdistämismäärityksessä **Synkronoi vain yhdistetyt tietueet** -kentän arvo.  

## <a name="use-configuration-templates-on-table-mappings"></a>Määritysmallien käyttäminen taulukon yhdistämismäärityksissä

Määritysmallit voidaan määrittää taulumäärityksiin käyttämään uusia tietueita tai rivejä, jotka on luotu [!INCLUDE[prod_short](includes/prod_short.md)]issa tai [!INCLUDE[prod_short](includes/cds_long_md.md)]issa. Voit määrittää kuhunkin taulukon yhdistämismääritykseen määritysmallin käytettäväksi uusissa [!INCLUDE[prod_short](includes/prod_short.md)]in tietueissa ja toisen mallin käytettäväksi uusissa [!INCLUDE[prod_short](includes/cds_long_md.md)]in riveissä.  

Jos asennat oletussynkronointimäärityksen, kaksi määritysmallia luodaan useimmiten automaattisesti ja käytetään [!INCLUDE[prod_short](includes/prod_short.md)] -asiakkaiden ja [!INCLUDE[crm_md](includes/crm_md.md)] -tilien taulukon yhdistämismäärityksiin: **CDSCUST** ja **CDSACCOUNT**.  

* **CDSCUST** luo ja synkronoi uusia asiakkaita [!INCLUDE[prod_short](includes/prod_short.md)]ssa [!INCLUDE[crm_md](includes/crm_md.md)] tilien perusteella.  

     Luo tämä malli kopioimalla asiakkaille aiemmin luotu määritysmalli. **CDSCUST** luodaan vain, jos aiemmin luotu määritysmalli on olemassa ja mallin **Valuuttakoodi**-kenttä on tyhjä. Jos määritysmallin jossain kentässä on arvo, kyseistä arvoa käytetään [!INCLUDE[prod_short](includes/cds_long_md.md)]in tilin sarakkeessa määritetyn arvon sijasta. Jos esimerkiksi [!INCLUDE[prod_short](includes/cds_long_md.md)] -tilin **Maa/alue**-sarakkeessa on *Yhdysvallat* ja määritysmallin **Maa/alue**-kentässä on **Yhdistynyt kuningaskunta**, sitten **Yhdistynyt kuningaskunta** on myös [!INCLUDE[prod_short](includes/prod_short.md)]in asiakkaan **Maa/alue**-arvo.  

* **CDSACCOUNT** luo ja synkronoi uusia käyttäjätilejä [!INCLUDE[prod_short](includes/cds_long_md.md)]ssa [!INCLUDE[prod_short](includes/prod_short.md)] tilin perusteella.  

### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Määritysmallien määrittäminen taulukon yhdistämismäärityksessä

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Integroinnin yhdistämistaulukot** ja valitse sitten liittyvä linkki.
2. Valitse luettelossa taulukon yhdistämismääritystapahtuman **Taulukon määritysmallin koodi** -kentässä [!INCLUDE[prod_short](includes/prod_short.md)]in uusissa tietueissa käytettävä määritysmalli.  
3. Määritä määritysmallille **Integrointitaulukon määritysmallin koodi** -kenttä, jota käytetään [!INCLUDE[prod_short](includes/cds_long_md.md)]in uusissa tietueissa.

## <a name="see-also"></a>Katso myös

[Tietoja Dynamics 365 Business Centralin ja [!INCLUDE[prod_short](includes/cds_long_md.md)]in integroinnista](admin-prepare-dynamics-365-for-sales-for-integration.md )  
[Business Centralin ja [!INCLUDE[prod_short](includes/cds_long_md.md)]in synkronointi](admin-synchronizing-business-central-and-sales.md)  
[Ajoitettu synkronointi](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
