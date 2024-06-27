---
title: Yhdistäminen ja synkronointi
description: 'Kun integrointitaulukon yhdistämismääritys synkronoidaan, yhdistettyjen Business Central- ja Dynamics 365 Sales -taulukoiden kaikkien tietueiden tiedot voidaan synkronoida.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'crm, sales, couple, decouple, synchronize'
ms.search.form: '6250,'
ms.service: dynamics-365-business-central
---

# <a name="couple-and-synchronize-records-between-dataverse-and-business-central"></a>Tietueiden yhdistäminen ja synkronoiminen Dataversen ja Business Centralin välillä

Tässä ohjeaiheessa kerrotaan, miten yksi tietue tai useita tietueita yhdistetään [!INCLUDE[prod_short](includes/prod_short.md)]:ssä Dataverse- tai [!INCLUDE[crm_md](includes/crm_md.md)]-tietueisiin. Tietueiden yhdistämisen ansiosta voit tarkastella Dataversein tietoja [!INCLUDE[prod_short](includes/prod_short.md)]ista ja päin vastoin. Yhdistäminen mahdollistaa myös tietojen synkronoinnin tietueiden välillä. Voit yhdistää aiemmin luotuja tietueita tai luoda ja yhdistää uusia tietueita.

> [!NOTE]
> Tietojen yhdistäminen ja synkronointi on käytettävissä vain, jos järjestelmänvalvoja on muodostanut yhteyden [!INCLUDE[prod_short](includes/prod_short.md)]:n ja Dataversen tai [!INCLUDE[crm_md](includes/crm_md.md)]:n välille. Asian voi tarkistaa nopeasti avaamalla **Asiakas**-kortin ja etsimällä **Määritä yhdistäminen** -toiminnon. Jos toiminto on käytettävissä, sovellukset on yhdistetty.

## <a name="video-example"></a>Esimerkkivideo

Tässä videossa näytetään tietojen kytkentä ja synkronointi osana [!INCLUDE[crm_md](includes/crm_md.md)] -ohjelman integrointia.

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Tietueen yhdistäminen

1. Avaa [!INCLUDE[prod_short](includes/prod_short.md)]issa sen tietueen kortti, jonka haluat yhdistää. Se voi olla esimerkiksi asiakkaan tai yhteyshenkilön kortti.  

    Voit myös avata luettelosivun ja valita tietueen, jonka haluat yhdistää.  

2. Valitse **Määritä yhdistäminen** -toiminto.  
3. Täytä kentät ja valitse **OK**.  

## <a name="to-synchronize-a-single-record"></a>Yhden tietueen synkronointi

1. Avaa [!INCLUDE[prod_short](includes/prod_short.md)]issa sen tietueen kortti, jonka haluat yhdistää. Se voi olla esimerkiksi asiakkaan tai yhteyshenkilön kortti.  
2. Valitse **Synkronoi nyt** -toiminto.  
3. Jos tietue voidaan synkronoida yhteen suuntaan, valitse vaihtoehto, joka määrittää suunnan tietojen päivitykselle ja valitse sitten **OK**.  

## <a name="to-synchronize-a-single-record-from-"></a>Yhden tietueen synkronointi [!INCLUDE[crm_md](includes/crm_md.md)]-sovelluksesta

1. Avaa [!INCLUDE[crm_md](includes/crm_md.md)]-sovelluksessa sen tietueen lomake, jonka haluat yhdistää. Se voi olla esimerkiksi tilikortin tai yhteyshenkilökortin lomake.  
2. Valitse **[!INCLUDE[prod_short](includes/prod_short.md)]** -toiminto valintanauhasta. Tietue avataan ja yhdistetään automaattisesti.

    > [!Note]
    > Voit synkronoida yhden tietueen [!INCLUDE[crm_md](includes/crm_md.md)]-sovelluksesta automaattisesti vain, kun **Synkronoi vain yhdistetyt tietueet** on poistettu käytöstä ja synkronoinnin suunnaksi on määritetty **Kaksisuuntainen** tai **Integrointitaulukosta** tietueen **Integrointitaulukon yhdistämismääritys** -sivulla. Lisätietoja on kohdassa [Taulukoiden ja kenttien yhdistäminen synkronointia varten](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).

## <a name="to-couple-multiple-records-using-match-based-coupling"></a>Voit yhdistää monta tietuetta vastaavuuspohjaisen yhdistämisen avulla.

Määritä entiteetin (esimerkiksi asiakkaan tai kontaktin) synkronoitavat tiedot yhdistämällä tietueet vastaavuuksien perusteella. Tarkenna vastaavuuksia määrittämällä haun kirjainkoon merkitseväksi ja määrittämällä kullekin vastaavuudelle prioriteetin. Jos vastaavuutta ei löydy, voit myös määrittää, että haluat luoda entiteetin Dataversessa. Lisätietoja on kohdassa [Vastaavuuspohjaisen yhdistämisen mukauttaminen](admin-how-to-set-up-a-dynamics-crm-connection.md#customize-the-match-based-coupling).  

> [!NOTE]
> Vastaavuuteen perustuva yhdistämisprosessi ohittaa tietueet, jotka on jo täsmäytetty. Jos haluat sisällyttää tietueet, kun suoritat vastaavuuteen perustuvan yhdistämisen, poista tietueiden yhdistäminen ja yritä sitten uudelleen. Lisätietoja tietueiden irrottamisesta on kohdassa [Tietueiden irrottaminen](#uncoupling-records).

1. Avaa [!INCLUDE[prod_short](includes/prod_short.md)]issa tietueen luettelosivu, kuten asiakkaiden tai yhteyshenkilöiden luettelosivu.
2. Valitse **Vastaavuuspohjainen yhdistäminen** -toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-synchronize-multiple-records"></a>Useiden tietueiden synkronointi

1. Avaa [!INCLUDE[prod_short](includes/prod_short.md)]issa tietueen luettelosivu, kuten Asiakkaat- tai Yhteyshenkilöt-sivu.  
2. Valitse ensin synkronoitavat tietueet ja sitten **Synkronoi nyt** -toiminto.  
3. Jos tietueet voidaan synkronoida yhteen suuntaan, valitse vaihtoehto, joka määrittää suunnan tietojen päivitykselle ja valitse sitten **OK**.  

## <a name="bulk-insert-and-couple-records"></a>Tietueiden joukkolisäys ja -yhdistäminen

Jos sinulla on suuri määrä  Dataverse-entiteettejä, jotka vastaavat [!INCLUDE [prod_short](includes/prod_short.md)]-ohjelman tietueita, voit lisätä ja yhdistää niitä joukkotoimintona. Voit esimerkiksi haluta joukkolisätä ja -yhdistää tietueita, kun määrität synkronointia ensimmäistä kertaa.

Käytä **ohjattua tietojen tuomista** **Microsoft Power Platform -hallintakeskuksessa**.

Seuraavassa esimerkissä kuvataan, miten joukkolisätään ja -yhdistetään asiakkaita Dataverse-tilien kanssa. Käytä samaa prosessia muun tyyppisille entiteeteille, kuten toimittajille, nimikkeille ja resursseille.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Avaa asiakastiedot Excelissä valitsemalla **Avaa Excelissä** -toiminto. <!--Don't they need to choose the customers that they want to import to Dataverse?-->
3. Jos haluat yhdistää ja tuoda tietoja **Tili**-kohteeseen Dataversessa, katso ohjeet: [Tuo tietoja (kaikki tietuetyypit) useista lähteistä](/power-platform/admin/import-data-all-record-types).  

    Jos Tili-kohteella on **bcbi_companyid**-sarake, kun linkität tietosarakkeita, varmista, että tuonti määrittää jokaiselle tuodulle tietueelle asianmukaisen yritystunnuksen sarakkeessa. Voit etsiä yritystunnuksen [!INCLUDE [prod_short](includes/prod_short.md)] -ratkaisussa noudattamalla seuraavia vaiheita:

    1. Avaa **Integrointitaulukon yhdistämismääritykset** -sivu.
    2. Valitse **ASIAKAS**-yhdistämismääritys ja valitse sitten **Muokkaa luetteloa**.
    3. Vieritä oikealle ja valitse **Integrointitaulukon suodatus** -kentässä avustajamuokkauksen painike :::image type="icon" source="media/assist-edit-icon.png" border="false":::. Tämä näyttää asiakkaan yhdistämismäärityksen oletussuodattimen, ja siinä on yrityksen tunnus. Yritystunnus on arvon ensimmäinen osa. Kopioi vain kyseinen osa ja jätä nollat huomiotta. Seuraavassa esimerkissä korostetaan kopioitava osa.

    :::image type="content" source="media/dataverse-company-id-guid.png" alt-text="Näyttää yritystunnuksen osan, joka kopioidaan.":::

    > [!NOTE]
    > Kaikki Dataverse-entiteettien ja Business Central -tietueiden nimet eivät täsmää. Sen mukaan, mitä tuot, tarkista että seuraavissa sarakkeissa on seuraavat arvot tuomisen jälkeen:
    >
    >* Asiakkaille **CustomerTypeCode**-sarakkeen tulee sisältää **Asiakas**.
    >* Toimittajille **CustomerTypeCode**-sarakkeen tulee sisältää **Toimittaja**. 
    >* Nimikkeille **ProductTypeCode**-sarakkeen tulee sisältää **Myyntivarasto**.
    >* Resurssien osalta **ProductTypeCode**-sarakkeen tulee sisältää **Palvelu**.
 
4. Kun olet tuonut tiedot Dataverse-ympäristöön, [!INCLUDE [prod_short](includes/prod_short.md)]-ohjelmassa seuraa [Voit yhdistää monta tietuetta vastaavuuspohjaisen yhdistämisen avulla](#to-couple-multiple-records-using-match-based-coupling) -ohjeita ja yhdistä Dataverse-tietueet [!INCLUDE [prod_short](includes/prod_short.md)]-tietueiden kanssa. 

## <a name="uncoupling-records"></a>Tietueiden yhdistämisen poistaminen

Voit irrottaa yhden tai useamman tietueen luettelosivuilta tai **Yhdistettyjen tietojen synkronointivirheet** -sivulta valitsemalla yhden tai useamman rivin ja valitsemalla **Poista yhdistäminen**. Voit myös poistaa kaikki yhden tai useamman taulukon yhdistämismäärityksen yhdistämiset **Integrointitaulukon yhdistämismääritykset** -sivulla.

## <a name="see-also"></a>Katso myös

[Dynamics 365 Salesin käyttäminen Business Centralista](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
