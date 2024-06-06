---
title: Asetuksien parhaat käytännöt – suunnitteluparametrit
description: Tässä aiheessa kuvataan parhaat käytännöt valittujen suunnitteluparametrikenttien määrittämiseen nimikekortin Suunnittelu-pikavälilehden avulla.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Asetukset - parhaat käytännöt: suunnitteluparametrit

**Suunnittelu**-pikavälilehti nimikkeen kortissa on yrityksen toimitusketjun keskus. Oikeiden suunnitteluparametrien määrittäminen on erittäin tärkeää kustannustehokkaan varastonhallinnan ja hyvän asiakaspalvelun vuoksi.  

 Seuraavassa taulukossa on parhaita käytäntöjä siitä, miten voit määrittää valitun suunnitteluparametrin kentät. Saat lisätietoja kentästä valitsemalla **Asetuskenttä**-sarakkeessa olevan linkin.  

|Kentän asetukset|Parhaat käytännöt|Kommentti|  
|-----------------|-------------------|-------------|  
|Uusintatilaustapa||Lisätietoja on ohjeaiheessa [Asetukset - parhaat käytännöt: uusintatilaustavat](setup-best-practices-reordering-policies.md).|  
|Varaa|Valitse **ei koskaan**, kun nimike suunnitellaan käyttämällä uusintatilauspistettä.<br /><br /> Valitse tuotannon **Ei koskaan** -kohta, kun haluat sallia suunnittelujärjestelmän kaikille kysynnöille.<br /><br /> Valitse **valinnainen** kohteille, jotka haluat ehkä varata ylimmän prioriteetin asiakkaille.<br /><br /> Valitse **Aina** muille yksilöllisille nimikkeille (muille kuin vakiotyyppisille nimikkeille), kuten sekalainen, jotka ovat tulevia, erityisvaatimuksia sisältäviä nimikkeitä.|Varaukset neutraloivat suunnittelun tarkoitusta, joka tasapainottaa kysyntää ja tarjontaa. Tämän vuoksi nimikkeitä, jotka on määritetty suunnittelussa, ei yleensä pidä varata.<br /><br /> Jos käyttäjä varaa varastomäärää tulevaa kysyntää varten, suunnittelun perusta häiriintyy ja uusintatilauspiste ei ehkä toimi oikein. Vaikka oletettu varastotaso on hyväksyttävä suhteessa uusintatilauspisteeseen, määrät eivät ehkä ole käytettävissä varauksen vuoksi.|  
|Puskuriaika|Määritä ottaen huomioon toimittajan joustavuuden.<br /><br /> Lyhyemmän ajanjakson avulla voit vähentää käyttöpääomaa välttämällä liiallista kalustoa, mutta se myös aiheuttaa enemmän toimenpiteitä aikataululle.|Jos toimittaja hyväksyy tilauksiin viime hetken muutoksia, käytä lyhyempää jaksoa, mutta valmistaudu suurempaan määrään uudelleenajoituksia. Jos toimittaja vaatii sitovan suunnittelun, pidennä jaksoa mahdollisimman paljon.<br /><br /> Lisätietoja **Puskutiaika**-kentästä on ohjeessa [Suunnittelun tiedot: suunnittelun parametrit](design-details-planning-parameters.md).|  
|Sisällytä varasto|Valitse aina, kun käytät uusintatilaustapaa Erä-erästä.|Älä valitse vain erityistilanteissa, esimerkiksi, kun varastonimikkeet eivät ole myytäviä.|  
|Toimitusajan varmistus|Valitse 1D tai 6D.<br /><br /> Määritä vähintään yhden päivän toimitusajan varmistus varmistaaksesi, että toimitukset ovat käytettävissä päivää ennen kuin niitä tarvitaan.<br /><br /> Jos kyseessä on uusi toimittaja, määritä aika normaalia pidemmäksi niin pitkäksi aikaa, kunnes toimittajan toimitussuorituskyky tunnetaan.<br /><br /> Määritä tuotannon kriittisille komponenteille pidemmät toimitusajan varmistukset.|Järjestelmän suunnittelema tarjonta, jolla vältetään varaston loppuminen, saapuu sinä päivänä, jona varasto loppuisi. Tämä voi olla useita tunteja myöhässä, jos esimerkiksi kysyntä tarvitaan aamulla ja tarjonta saapuu iltapäivällä. **Huomautus:**  **Toimitusajan varmistus** -kenttä käyttää peruskalenteria. 14 D ei välttämättä ole kahta viikkoa.|  
|Varmuusvaraston määrä|Käyttää nimikkeisiin, joissa on suuria vaihteluita.<br /><br /> Käytä tuotannon kriittisissä komponenteissa.<br /><br /> Käytä nimkikeisiin, joissa on huoltosopimukset.|Jos **Uusintatilauspiste**-kenttään ei ole määritetty arvoa, varmuusvaraston määrä toimii myös uusintatilauspisteenä.|  
|Erän koontijakso|Jos haluat vain muutamia suuria tilauksia ja hyväksyt varastoinnin, määritä pitkä erän koontijakso.<br /><br /> Jos haluat useita pieniä tilauksia ja mahdollisimman pienen varaston, määritä lyhyt erän koontijakso.|Erän koontijakso on yleensä pisin varastointiaika.|  
|Uusintatilauspiste|Perusta uusintatilauspiste nimikkeen kysynnän profiiliin.|Jos historiatiedot osoittavat, että nimikkeen keskimääräinen kysyntä seitsemän päivän toimitusajan aikana on 100 yksikköä, uudelleentilauspisteen vähimmäisarvoksi voidaan määrittää 100.<br /><br /> Tämä tarkoittaa, että kun varastotaso laskee "Vaiheet ongelman toistamiseen" -osassa alle 100 yksikköön, suunnittelujärjestelmä ehdottaa täydennystä, koska täydennys vie seitsemän päivää, ja varastotason on oltava riittävä, jotta se kattaa noiden seitsemän päivän aikana ilmenevän nimikkeiden kysynnän.|  
|Aikaväli|Jätä tyhjäksi, mikä tarkoittaa, että varastotaso tarkistetaan joka päivä.|Varastotason päivittäinen tarkistus varmistaa optimaalisen uudelleentilauksen suunnittelun. **Huomautus:**  Aikaväli 1V tarkoittaa sitä, että varastotaso saattaa olla alle uusintatilauspisteen yksi viikko ennen kuin toimitustilausta ehdotetaan.|  
|Pyöristystarkkuus|Jos kyseessä on kallis tuotanto, määritä arvoksi 0,00001.|Jätteen tai materiaalikulutuksen suuret pyöristysmäärät voivat aiheuttaa erittäin suuria varastokustannuksia. Siksi saattaa olla tarpeen määrittää pienin pyöristystarkkuus tämän mahdollisen kustannuksen minimoimiseksi.|  

> [!NOTE]  
> Nimikekorttien suunnitteluparametrien parhaita käytäntöjä sovelletaan myös SKU-korttien samoihin kenttiin.  
>
> Jos yritykset suunnittelevat kysyntää eri sijainneissa, on suositeltavaa määrittää jokaiselle sijainnille varastointiyksiköt ja luoda kaikki kysyntä **Sijainnin koodi** -kentän arvon avulla. Lisätietoja on kohdassa [Rakennetiedot: suunnitelman luominen sijaintien avulla tai ilman sijainteja](production-planning-with-without-locations.md).  

## Katso myös  
[Asetukset - parhaat käytännöt: toimitusten suunnittelu](setup-best-practices-supply-planning.md)  
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)  
[Monimutkaisten sovellusalueiden määrittäminen parhaiden käytäntöjen avulla](set-up-complex-application-areas-using-best-practices.md)  
[Rakennetiedot: suunnitelman luominen sijaintien avulla tai ilman sijainteja](production-planning-with-without-locations.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
