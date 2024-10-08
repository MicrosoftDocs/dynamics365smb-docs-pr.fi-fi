---
title: Huoltonimikkeiden huoltotilausten vaihekuvaus
description: 'Tässä artikkelissa käsitellään useita perusprosesseja, joihin liittyy huoltotilauksia ja nimikkeitä.'
author: andreipa
ms.author: andreipa
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="walkthrough-of-service-orders-for-service-items"></a>Huoltonimikkeiden huoltotilausten vaihekuvaus

Tässä vaihekuvauksessa kuvataan useita ydinprosesseja:

- Luo tapauskohtainen huoltotilaus ja rekisteröi nimikkeen korjaus
- Anna asiakkaalle korjausaikaa varten lainanimike
- Kirjaa ja laskuta huoltotilaus
    
## <a name="creating-a-service-order"></a>Huoltotilauksen luominen

### <a name="scenario"></a>Skenaario

Huoltopäällikkö Charles luo huoltotilauksen korjausskenaariota varten ja lainaa lainatavaran asiakkaalle korjausaikaa varten.

### <a name="steps"></a>Vaiheet

1. Luo huoltotilaus manuaalisesti nimikkeelle, joka on korjattava.
   1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotilaukset**
   2. Valitse **Uusi**-toiminto.
   3. Syötä **10000** kohtaan asiakasnumero kenttä
   4. Valitse **Huoltotilauksen tyyppi** -kentässä **KORJAUS**.
   5. Valitse riveillä **Nimikkeen nro** -kohtaan **S-100**.
2. Vaihtoehtoisesti
   1. Tarkista mahdolliset ratkaisut valitsemalla Rivitoiminto **Vianetsintä**.
   2. Valitse Rivi-toiminto **Vika-/ratkaisukoodien suhteet**
   3. Valitse **oirekoodiksi** *MELU*
   4. Valitse *5-2 Kova ääni haudutuksen aikana* **vikakoodiksi** ja sulje sivu. Vikakoodi, ratkaisukoodit päivitetään riveillä.
3. Lainaa vaihtotavaraa nimikkeen korjauksen aikana
   1. Valitse riveillä Nimikkeen nro -kohtaan **L.TAVARA1** Vahvista lainatavaran liikkeeseenlasku valitsemalla **Kyllä** lainatavaran lainaamiseksi. 
   2. Valitse Funktiot-toiminto **Hae vakiohuoltokoodit**, valitse huoltoryhmään liittyvä vakiokoodi ja valitse **Ok**.
   
### <a name="results"></a>Tulokset

- Nimikkeelle luodaan huoltotilaus
- Huoltotilauksen huoltoasiakirjalokissa näkyvät lainatavaran aktiviteetit.
- Lainatavaralla on lainaustapahtuma, joka kuvastaa lainausta.
   

## <a name="register-performed-work-mark-loaner-as-returned"></a>Rekisteröi suoritetun työn, merkitsee lainatavaran palautetuksi.

### <a name="scenario-1"></a>Skenaario

Huoltoteknikko merkitsee lainatavaran palautetuksi, rekisteröi suoritetun työn.

### <a name="steps-1"></a>Vaiheet

1. Etsi huoltotehtävä ja rekisteröi aika 
   1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotehtävät** ja valitse sitten vastaava linkki.
   2. Etsi huoltotilaus, jolle aika määritetään.
   3. Valitse **Nimikkeen työkirja** -toiminto.
   4. Lisää seuraavat tiedot

    |Tyyppi|Nro|Määrä|
    |----|---|--------|  
    |Vaihtoehto|SER102|2|

   4. Valitse **Korjaustilakoodi**-kentässä *VALMIS*
    
2. Merkitse lainatavara palautetuksi
   1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Lainatavarat** ja valitse sitten vastaava linkki.
   2. Etsi lainatavara, jonka haluat merkitä palautetuksi.
   3. Valitse **Vastaanota**-toiminto 
   4. Vahvista lainatavaran palautus valitsemalla **Kyllä** lainatavaran palauttamiseksi.
      
### <a name="results-1"></a>Tulokset

- Huoltotilauksen **huoltoasiakirjalokissa** näkyvät lainatavaran aktiviteetit.
- Lainatavaralla on lainaustapahtuma, joka kuvastaa vastaanottoa.


### <a name="scenario-2"></a>Skenaario

Huoltopäällikkö Charles kirjaa valmiin huoltotilauksen.

1. Etsi huoltotilaus 
   1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotilaukset** ja valitse sitten vastaava linkki.
   2. Etsi kirjattava huoltotilaus.

2. Kirjaa lasku huoltotilauksessa
   1. Suorita huoltotilaus loppuun valitsemalla **Kirjaa**-toiminto, valitse **Toimitus ja lasku** -toiminto ja valitse sitten **OK**.
   2. Vahvista kirjatun laskun avaaminen valitsemalla **Kyllä**. 
### <a name="results-2"></a>Tulokset

- **Kirjattu huoltolasku** luodaan.
- Nimikkeeseen ja resurssiin liittyvät **huoltotapahtumat** luodaan

## <a name="see-also"></a>Katso myös
[Huoltonimikkeiden huoltosopimusten vaihekuvaus](service-contract-flow.md)  
[Palvelu](../../service-service.md)
