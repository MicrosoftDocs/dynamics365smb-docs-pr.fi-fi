---
title: Toiminta vastuupaikkojen kanssa
description: 'Vastuupaikat hallintokeskuksina auttavat yrityksiä määrittämällä käyttäjäkohtaiset näkymät myynti- ja ostoasiakirjoista, jotka liittyvät yksinomaan tiettyyn vastuukeskukseen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.forms: '5714, 5715'
ms.date: 05/16/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="work-with-responsibility-centers"></a>Vastuupaikkojen käsitteleminen

Vastuupaikat mahdollistavat hallintakeskusten käsittelemisen. Vastuupaikka voi olla kustannuspaikka, kannattavuuspaikka, sijoituspaikka tai muu yrityksen määrittämä hallintapaikka. Vastuupaikkoja ovat esimerkiksi myyntitoimistot, usean sijainnin osto-osastot sekä tehtaan suunnittelutoimistot. Yritykset voivat esimerkiksi määrittää käyttäjäkohtaiset näkymät tiettyyn vastuupaikkaan liittyville osto- ja myyntiasiakirjoille.  

Useiden sijaintien käyttäminen yhdessä vastuupaikan kanssa mahdollistaa yritystoimintojaan hallinnan joustavasti ja optimaalisesti.

Useat sijainnit mahdollistavat sen, että yritykset voivat hallita varastoaan useissa sijainneissa yhden tietokannan avulla. Tämän rakeen kaksi tärkeintä konseptia ovat sijainnit ja varastointiyksiköt. Sijainti on paikka, joka käsittelee nimikkeiden fyysistä sijoittelua ja määriä. Konsepti on niin laaja, että se kattaa esimerkiksi voimalat tai tuotantolaitokset ja jakelukeskukset, varastot, näyttelytilat ja huoltoajoneuvot. Varastointiyksikkö on tietyssä sijainnissa oleva nimike ja/tai variantti. Varastointiyksiköiden avulla useissa paikoissa toimivat yritykset voivat lisätä täydennystietoja, osoitteita ja taloudellisia kirjaustietoja sijaintitasolla. Tämän seurauksena ne voivat täydentää saman nimikkeen variantteja kunkin sijainnin ja tilausnimikkeiden osalta sijaintikohtaisten täydennystietojen perusteella.  

## <a name="to-set-up-a-responsibility-center"></a>Vastuupaikkojen luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vastuupaikat** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Jos käytät vastuupaikkoja yrityksesi hallinnoimisessa, voi olla hyödyllistä määrittää vastuupaikalle oletusarvo.
4. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yrityksen tiedot** ja valitse sitten vastaava linkki.
5. Lisää **vastuupaikan koodi Toimitus-pikavälilehden**  **Vastuupaikka-kenttään** .

Tätä koodia käytetään kaikissa osto-, myynti- ja huoltoasiakirjoissa, jos käyttäjällä, asiakkaalla tai toimittajalla ei ole oletusvastuupaikkaa. Voit antaa kaikissa myynti-, osto- tai huoltoasiakirjassa jonkin muun kuin oletusvastuupaikan.

> [!NOTE]  
> Kun syötät asiakirjaan vastuupaikan koodin, se vaikuttaa asiakirjan osoitteeseen, dimensioihin ja hintoihin.  

## <a name="to-assign-responsibility-centers-to-users"></a>Vastuupaikkojen liittäminen käyttäjiin

Voit määrittää käyttäjät siten, että [!INCLUDE [prod_short](includes/prod_short.md)] hakee vain kyseiseen aihealueeseen liittyvät asiakirjat. Käyttäjät on liitetty yhteen vastuupaikkaan, ja he työskentelevät vain sen vastuupaikan tiettyihin sovellusalueisiin liittyvien asiakirjojen parissa.  

Määritä tämä määrittämällä vastuupaikat käyttäjille kolmella toiminta-alueella: ostoissa, myynnissä ja huoltohallinnossa.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjän määritys** ja valitse sitten vastaava linkki.  
2. Valitse **Käyttäjäasetukset**-sivulla se käyttäjä, johon haluat liittää vastuupaikan. Jos käyttäjä ei ole luettelossa, sinun täytyy syöttää käyttäjätunnus **Käyttäjätunnus**-kenttään.  
3. Anna **Myynnin vastuupaikan suodatus** -kentässä vastuupaikka, jossa käyttäjällä on myynteihin liittyviä tehtäviä.  
4. Anna **Ostovastuupaikan suodatus** -kentässä vastuupaikka, jossa käyttäjällä on ostoihin liittyviä tehtäviä.  
5. Anna **Huollon vastuupaikan suodatus** -kentässä vastuupaikka, jossa käyttäjällä on huoltohallintoon liittyviä tehtäviä.  

> [!NOTE]  
> Käyttäjät voivat tarkastella vain omaan vastuukeskukseensa liittyviä kirjattuja asiakirjoja. He voivat kuitenkin tarkastella kaikkia kirjapintotapahtuma ja siirtyä muihin kirjattuihin asiakirjoihin kirjanpitotapahtumista.

## <a name="see-also"></a>Katso myös

[Varaston määrittäminen](inventory-setup-inventory.md)    
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)    
[Vaihto-omaisuus](inventory-manage-inventory.md)    
[Varastoinninhallinnan yleiskatsaus](design-details-warehouse-management.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    
[Laskun kirjauskäytännön määrittäminen käyttäjille](admin-setup-invoice-posting-policy.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
