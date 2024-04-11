---
title: Huoltohallintoprosessien määrittäminen
description: 'Tietoja sellaisten prosessien määrittämisestä, joilla voidaan varmistaa asiakkaiden tyytyväisyys palveluihin.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.search.keywords: 'service, number sequences, setup, warnings, fee, contracts, warranties'
ms.date: 02/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="configure-service-management-processes"></a>Huoltohallintoprosessien määrittäminen

Seuraavaksi käsitellään esimerkkejä asetuksista, joita voidaan käyttää huoltohallintoprosesseissa:  
  
* Jotkin eri prosessien yleisasetukset, kuten varoitukset, laskelmat huoltonimikkeiden seuraavasta huollosta, arvioinnin aloitusmaksu ja käytettävä vianmääritystaso.  
* Teknikon huoltoasiakirjoihin syöttäminen tietojen tyypit. Voit esimerkiksi pyytää heitä määrittämään tilauksen tyypin, työn aloitus- ja/tai päättymispäivämäärät sekä tehdyn työn tyyppi.  
* Joitakin vastausaikojen ja takuiden oletusasetukset. Niitä ovat huollon aloittamisen oletusvastausaika, osien ja työn takuun oletusprosentit sekä takuun kesto.  
* Sopimusten asetukset, kuten huoltosopimustilauksissa käytettävien päivien enimmäismäärä, sopimuksen peruutuksessa mahdollisesti käytettävät syykoodit, kuvausten vakiotekstit ja sopimuksen arvot.  
* Huoltoon liittyvissä asiakirjoissa ja nimikkeissä käytettävät numerosarjat.  

## <a name="to-enter-general-and-mandatory-settings"></a>Yleisten ja pakollisten asetusten antaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltohallinnon asetukset** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="set-up-service-invoice-posting-policies-for-users"></a>Käyttäjien huoltolaskun kirjauskäytäntöjen määrittäminen

Yrityksillä on usein yksilöllisiä lasku- ja toimitusprosesseja. Prosessit voivat vaihdella esimerkiksi yhdestä henkilöstä, joka kirjaa kaiken huoltotilaukseen, useisiin työntekijöihin, joista kukin käsittelee omaa sivuaan.

Kirjauskäytäntöjen avulla voidaan rajoittaa käyttäjien huoltolaskujen kirjaamista tai edellyttää heitä kirjaamaan laskut yhdessä liittyvän huoltotoimituksen kanssa. Kirjauskäytäntö määritetään valitsemalla **Käyttäjäasetukset**-sivun **Huoltolaskun kirjauskäytäntö** -kentässä jokin seuraavista vaihtoehdoista:

* **Sallittu** (oletus): säilytetään nykyinen toiminta, jossa voidaan valita kirjausvaihtoehto, kuten **Toimitus**, **Lasku** ja **Toimitus ja lasku**.
* **Kielletty**: Huoltolaskujen kirjaaminen estetään. [!INCLUDE [prod_short](includes/prod_short.md)] näyttämän vahvistusikkunan ainoa vaihtoehto on **Toimitus**.
* **Pakollinen**: Laskut voidaan kirjata yhdessä huoltotoimitusten kanssa. [!INCLUDE [prod_short](includes/prod_short.md)] näyttämän vahvistusikkunan ainoa vaihtoehto on **Toimitus ja Lasku**.

Tämä asetus vaikuttaa seuraaviin asiakirjoihin:

* Huoltotilaukset
* Fyysisen varaston toimitukset
* Huoltolaskut
* Huollon hyvityslaskut

Seuraavassa taulukossa käsitellään vaikutuksia eri asiakirjoihin.

|Asiakirja  |Salli<br>Näyttää useita vaihtoehtoja   |Kielletty<br>Vahvistusikkuna  |Pakollinen<br>Vahvistusvalintaikkuna  |
|---------|---------|---------|---------|
|Huoltotilaus     | * Toimitus<br>* Lasku<br>* Toimitus ja lasku<br>* Toimitus ja kulutus         |* Toimitus<br>* Toimitus ja kulutus  |Haluatko kirjata toimituksen ja laskun?         |
|Fyysisen varaston toimitus     |* Toimitus<br>* Toimitus ja lasku         |Haluatko kirjata toimituksen?         | Haluatko kirjata toimituksen ja laskun?        |
|Huoltolasku     | Haluatko kirjata laskun?         | Virhe: Ei voi kirjata.       |Haluatko kirjata laskun?         |
|Huoltohyvityslasku     | Haluatko kirjata hyvityslaskun?         | Virhe: Ei voi kirjata.        |Haluatko kirjata hyvityslaskun?         |

> [!NOTE]
> Kun kirjaat huoltolaskuja ja hyvityslaskuja, kirjausvaihtoehtoja ei ole. Asiakirjat kirjaavat aina fyysiset tapahtumat ja rahoitustapahtumat yhdessä. Huoltolaskuja ja hyvityslaskuja ei voi kirjata osittain.

## <a name="see-also"></a>Katso myös

[Vikojen raportoinnin määrittäminen](service-how-setup-fault-reporting.md)  
[Resurssin kohdistuksen määrittäminen](service-how-setup-resource-allocation.md)  
[Vakiohuoltokoodien määrittäminen](service-how-setup-service-coding.md)  
[Huollon lisäkustannusten määrittäminen](service-how-setup-service-costs-pricing.md)  
[Vianmäärityksen määrittäminen](service-how-setup-troubleshooting.md)  
[Huoltohallinto](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
