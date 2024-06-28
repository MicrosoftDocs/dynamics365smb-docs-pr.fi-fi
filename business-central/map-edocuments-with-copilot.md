---
title: Sähköisten asiakirjojen yhdistäminen ostotilausriveille Copilotin avulla
description: Tietoja Copilotin käyttämisestä sähköisten asiakirjojen yhdistämiseen ostotilariveille.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 06/10/2024
ms.custom: bap-template
---

# Sähköisten asiakirjojen yhdistäminen ostotilausriveille Copilotin avulla (esiversio)

Hankintaprosessien digitalisoituessa Business Centralin sähköisten asiakirjojen ominaisuudella on merkittävä tehtävä toimittajan laskujen vastaanoton ja käsittelyn automatisoinnissa. Copilot voi auttaa tässä prosessissa parantamalla toimittajan laskujen yhdistämistä ja kohdistamista ostotilauksiin. Tämä avustus vähentää aikaa vieviä tehtäviä, jotka muuten sisältäisivät runsaasti hakuja, valintoja ja tieto syöttämistä. Toinen etu on se, että toimittajan laskut eivät liity ostotilauksiin täysin. Tällöin Copilotilla on hyvät positiot vastaavien ostotilausten yksilöimiseksi. Etenkin parannetuista kohdistusominaisuuksista on hyötyä pienille ja keskisuurille organisaatioille, jotka tarvitsevat tehokkaan asiakirjaseurannan ostotilausrivien osalta. Copilot on tekoälypohjainen avustaja, jonka käyttö edistää Business Central -käyttäjien luovuutta ja parantaa tuottavuutta.

> [!IMPORTANT]
> - Tämä on tuotantovalmis esiversio tuotanto- ja eristysympäristöihin maakohtaisissa lokalisoinneissa<!-- with the exception of Canada -->.
> - Tuotantovalmista esiversiota koskevat ominaisuuksien lisäkäyttöehdot. Lisätietoja: [Dynamics 365:n esiversion lisäkäyttöehdot](https://go.microsoft.com/fwlink/?linkid=2189520)
> - Tekoälyn luoma sisältö voi olla virheellistä.

**Sähköisten asiakirjojen** sovelluksen ensimmäisessä julkaisussa otettiin käyttöön koko myyntiprosessin sähköisiä asiakirjoja koskevia perusskenaarioita. Vastaanotettujen asiakirjojen käsittelyssä tarvitaan kuitenkin parannuksia ja automatisointia erityisesti ostoprosessien yhteydessä. Copilot tarkentaa sähköisten asiakirjojen hallintaa ostoprosessissa etenkin ostotilausten osalta. Sähköinen asiakirjakehys mahdollistaa kullekin toimittajalle luotavan ostoasiakirjan tyypin määrittämisen, kun toimittajilta vastaanotetaan sähköisiä laskuja. Aiemmin ainoa vaihtoehto oli luoda ostolasku joko asiakirjana tai KP-päiväkirjana.

Business Centralissa aiemmin luotua ostotilausta voidaan nyt päivittää sähköisessä laskussa saaduilla tiedoilla.

## Käytettävissä olevat kielet

[!INCLUDE[e-docs-matching-language-support](includes/e-docs-matching-language-support.md)]

## Copilotin aktivoiminen  

Jos et aktivoinut **Sähköisen asiakirjan kohdistusavustaja** -Copilotia, se on tehtävä manuaalisesti. Ota **Sähköisen asiakirjan kohdistusavustaja** käyttöön noudattamalla näitä seuraavia vaiheita: 

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Copilot- ja tekoälyominaisuudet** ja valitse sitten liittyvä linkki. 
2. Valitse ominaisuuksien luettelossa **Sähköisen asiakirjan kohdistusavustaja** ja muuta tilaksi **Aktiivinen**.  

Voit aloittaa Copilotin käytön heti, kun olet aktivoinut sen. 

## Ostotilausten tunnistaminen

Ensimmäiseksi tunnistetaan automaattisesti kohdistettavat ostotilaukset. Jos **toimittajasi** on määrittänyt **Vastaanota e-asiakirjalle** -kentän käyttämään **ostotilauksia**, niin kun sähköinen asiakirja on luotu [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa (manuaalisesti tai ulkoisesta päätepisteestä), [!INCLUDE[prod_short](includes/prod_short.md)] se tekee seuraavaa:

1. Jos kyseisen toimittajan **ostotilaus** on olemassa ja vastaanotetussa **Sähköinen asiakirja** -tiedostossa on *ostotilausnumero*, [!INCLUDE[prod_short](includes/prod_short.md)] linkittää tämän **Sähköisen asiakirjan** automaattisesti määritettyyn **ostotilaukseen**. Tämän **sähköisen asiakirjan** **asiakirjan tila** on **käsittelyssä**, ja **Palvelun tila** -alisivun **sähköisen asiakirjan tila** on **Asiakirja linkitetty**.  
Linkki näkyy kyseisen **E-asiakirjan** **Asiakirja**-kentässä. Jos sinun täytyy muuttaa linkitetty **ostotilaus** automaattisesti, voit tehdä sen käyttämällä **Päivitä ostotilauslinkki** -toimintoa ja valita manuaalisesti yhden toimittajan olemassa olevista ostotilauksista. Voit tehdä sen vain, ennen kuin vastaat **E-asiakirjan** ja **ostotilauksen** välisiä rivejä.  
2. Jos **Ostotilaus** tälle tietylle toimittajalle *on olemassa, mutta vastaanotetussa **Sähköinen asiakirja** -tiedostossa ei ole ostotilausnumeroa*, jos latasit tämän asiakirjan manuaalisesti, [!INCLUDE[prod_short](includes/prod_short.md)] antaa sinun valita jonkin olemassa olevista ostotilauksista avaamalla **Ostotilaukset**-luettelon tilauksista, jotka olet saanut toimittajilta, jotka sisältävät vain **Sähköisen asiakirjan**. Valitse haluamasi **Ostotilaus** ja valitse **OK**. Jos et ole valinnut oikeaa **ostotilausta** tai sait **E-asiakirjan** automaattisesti ulkoisesta päätepisteestä **työjonon** avulla, uutta **e-asiakirjaa** ei linkitetä minkään ostoasiakirjan kanssa, ja **asiakirjan tilaksi** tulee **Virhe** ja **Huollon tila** -alasivun **sähköisen asiakirjan tilaksi** **tuodun asiakirjan käsittelyvirhe**. Kun haluat lopettaa linkittämisen **ostotilaukseen**, valitse **Päivitä ostotilauslinkki** -toiminto ja valitse yksi tämän toimittajan ostotilauksista.  

## Rivien yhdistäminen

Copilot auttaa kohdistamaan sähköisen laskun rivit ja ostotilauksen rivit automaattisesti, minkä lisäksi se mahdollistaa kohdistuksia parantavan älykkään lisäkohdistuksen.

Kun ne on kohdistettu ja yhdistetty, [!INCLUDE [prod_short](includes/prod_short.md)] päivittää kohdistetun ostotilauksen soveltuvilla vastaanotetuilla tiedoilla. Tämä varmistaa, että tilausriveillä vastaanotetaan oikeat määrät.

Voit liittää vastaanotetut sähköiset asiakirjat ostotilausten riveihin kahdesta eri paikasta, **sähköiset asiakirjat**-sivulta tai **Ostotilaus**-sivulta. Helpoin tapa paikallistaa jo linkitetyt **ostotilaukset** on käyttää **Linkitetyt ostotilaukset** -ruutua osana **E-asiakirjan toimenpiteitä**. Kaikki ei-linkitetyt asiakirjat löytyvät **odottavat ostojen e-laskut** -ruudusta, jossa on luettelo tarkasteltavissa olevista **E-asiakirjoista**.  

> [!NOTE]
> Näitä kahta ruutua koskevat **e-asiakirjatoiminnot** ovat seuraavissa Roolikeskuksissa: **Liiketoimintapäällikön arviointi**, **Liiketoimintapäällikkö**, **Kirjanpitäjä**, **Varastopäällikkö** ja **Toimitus ja vastaanotto**.

Kun haluat suorittaa vastaavuuden ostotilauksesta, valitse **Liitä sähköisen asiakirjan rivit** -toiminto, joka on olemassa sekä ostotilaus- että ostotilausluettelon sivuilla. Mutta jos haluat suorittaa vastaavuuden **sähköiset asiakirjat** -sivulta, valitse **Täsmäytä ostotilaus** -toiminto tältä sivulta. Voit jatkaa täsmäyttämistä, seuraa alla olevia ohjeita:

1. Valitse linkitetyille asiakirjoille **Liitä e-asiakirjarivit**- tai **Täsmäytä ostotilaus** -toiminto.  
2. Voit huomata, että **Sähköisen asiakirjan täsmäytystilausrivit, joissa on Copilot** toimivat ja taustalla on **Ostotilauksen täsmäytys** -sivu. Tämä tarkoittaa, että sama prosessi tapahtuu, mutta **Copilotin** automaattisella tuella, joka suorittaa täsmäytysprosessin sinun sijastasi. 
3. Muutaman sekunnin kuluttua **E-asiakirjan vastaavuustilausrivit Copilotin kanssa** ehdottaa rivejä, joiden vastaavuuksien lisätiedot ovat: 

    1. Voit etsiä seuraavat tiedot kehotteen otsikosta:   

    |Kentän nimi |Kuvaus |
    |--------|-----------------|
    |Kohdistettu automaattisesti | Määrittää automaattisesti ehdotettujen kohdistusten määrän. Tämä perustuu merkkijonovertailuun, ja jos kuvaus on vähintään 80 %:n päällekkäinen, järjestelmä vastaa näitä kuvauksia automaattisesti käyttämättä Copilot-ominaisuuksia. |
    |Copilotin kohdistamat | Määrittää Copilotin ehdottamien osumien määrän käyttäen sekä merkkijonoa että semanttista vertailua. |
    |Sähköisen asiakirjan nro | Määrittää linkitetyn sähköisen asiakirjan numeron. |
    |Laskun summa yhteensä ilman ALV:tä | Määrittää laskun kokonaissumman ilman arvonlisäveroa. |
    |Kohdistettu summa yhteensä ALV:n kanssa | Määrittää kohdistetun summan ilman ALV:tä. |
    
    2. Jos kaikki rivit täsmäävät, oikeassa yläkulmassa näkyy vihreä teksti: **Kaikki rivit (100 %) vastaavat toisiaan. Tarkista vastaavuusehdotukset**.  
    3. Voit etsiä seuraavat tiedot **Täsmäytetyt ehdotukset** -riveiltä:  

    |Kentän nimi |Kuvaus |
    |--------|-----------------|
    |Sähköisen asiakirjan rivinro | Määrittää E-asiakirjan rivinumeron (joka tulee alkuperäisestä e-asiakirjatiedostosta). |
    |Sähköisen asiakirjan rivin kuvaus | Määrittää E-asiakirjan rivikuvauksen (joka tulee alkuperäisestä e-asiakirjatiedostosta). |
    |Kohdistettu määrä | Määrittää määrän, joka kohdistetaan ostotilausriviin. |
    |Ehdotus | Määrittää tekoälyn ehdottaman toimen, ja nämä ehdotetut toimenpiteet liittyvät ostotilausrivien vastaavuuksien täsmäytykseen. |

    4. Kaikki täysin ehdotetut ja toisiaan vastaavat rivit on merkitty vihreällä värillä. Jos on olemassa ongelma, esimerkiksi eri hinta, mutta sallitun hintavälin sisällä, tämä rivi on merkitty keltaisella värillä. Jos kuvauskenttien välillä on samankaltaisuutta, mutta hintaero on suurempi kuin sallittu, rivi on merkitty punaisella värillä.
    5. Jos et ole tyytyväinen joihinkin ehdotuksiin, voit poistaa ne **Poista rivi** -toiminnolla.  
    6. Jos haluat nähdä ehdotuksen täsmäytykset, voit avata **E-asiakirjan vastaavuustiedot** -sivun valitsemalla linkin **Ehdotus**-sarakkeesta. 
    7. **E-asiakirjan vastaavuuksien tiedot** -sivulla voit vertailla **E-asiakirjan** ja **ostotilauksen** tietoja varmistaaksesi ehdotetun vastaavuuden ennen sen vahvistamista. 
    8. Sulje sivu tarkistuksen jälkeen.   

4. Jos et ole tyytyväinen useimpiin ehdotuksiin tai et halua käyttää **Täsmäytä e-asiakirjan tilausrivit Copilotin avulla** -ominaisuutta, valitse **Hylkää se**, ja voit jatkaa [manuaalista täsmäytystä](finance-how-use-edocuments-purchase.md) edellä selitetyllä tavalla.  
5. Jos haluat säilyttää ehdotukset, valitse **Säilytä se** -painike, niin järjestelmä tallentaa kaikki **Copilotin** tekemät ehdotukset.  
6. [!INCLUDE[prod_short](includes/prod_short.md)] sulkee Copilotin kehotteen ja **Ostotilausten täsmäytys** -sivun rivit merkitään vihreiksi, koska ne on jo täsmäytetty.  
7. Tästä lähtien voit jatkaa työskentelyä manuaalisen täsmäytyksen tekemisessä, mikä tarkoittaa, että voit poistaa osumat, manuaaliset täsmäytykset, nollata täsmäytyksen tai jos et halua tehdä muutoksia, valitse **Käytä ostotilaukseen** -toiminto ja jatka työskentelyä **Ostotilauksen** kanssa. 

> [!NOTE]
> Voit mysö valita **Ostotilausten täsmäytys** -sivun uudelleen **Täsmäytä Copilotin avulla** -toiminnon, ohjelma kysyy kuitenkin, haluatko korvata olemassa olevat vastaavuudet, koska kaikki rivit on jo täsmäytetty.  

> [!NOTE]
> Hinnan/kustannuksen analysointi, ja saatavilla oleva määrätarkistus on osa esikäsittelytoimintoa. 

## Katso myös

[Sähköisten asiakirjojen yleiskuvaus](finance-edocuments-overview.md)    
[Sähköisten asiakirjojen käyttö myynnissä](finance-how-use-edocuments.md)    
[Sähköisten asiakirjojen käyttö ostoissa](finance-how-use-edocuments-purchase.md)   
[Copilot- ja tekoälyominaisuuksien vianmääritys](ai-copilot-troubleshooting.md)    
[Vastuullisen tekoälyn usein kysyttyjä kysymyksiä pankkitäsmäytysavustajasta](faqs-bank-reconciliation.md)    
