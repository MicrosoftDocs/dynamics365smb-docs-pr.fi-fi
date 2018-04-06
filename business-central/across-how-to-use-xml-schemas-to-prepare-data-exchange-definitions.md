---
title: XML-malleihin perustuvien XMLports-kohteiden luominen | Microsoft Docs
description: "Voit määrittää tiedonsiirtokehyksen XML-mallien avulla."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 860de16a7cf5f608b6b1739eb8a4900ebe6c8e11
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a>XML-mallien käyttäminen tietojenvaihtomääritysten valmisteluun
Voit ottaa XML-tiedostojen tietojen tuonnin ja viennin käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]in tiedonsiirtokehyksessä määrittämällä [!INCLUDE[d365fin](includes/d365fin_md.md)]in kanssa vaihdettavat tietoelementit XML-mallien avulla. Se tehdään **XML-mallin tarkastelutoiminto** -ikkunassa lataamalla XML-rakennetiedosto, valitsemalla sopivat tietoelementit ja käynnistämällä joko tietojen vaihdon määritys tai XMLport.  

 Kun olet määrittänyt XML-mallin perusteella sisällytettävät tietoelementit, voit luoda XMLport-objektin **Luo XMLport** -toiminnolla.  

 Voit myös käyttää **Luo tietojen vaihdon määritys** -toimintoa luodaksesi valittuihin tietoelementteihin perustuvan määrityksen, jonka sitten viimeistelet tietojen vaihtamiskehyksessä. Tällä tavoin **Kirjauksen tiedonsiirtomääritykset** -ikkunassa luodaan tietue. Jatka ikkunassa määrittämällä, mitkä tiedoston elementit ja mitkä [!INCLUDE[d365fin](includes/d365fin_md.md)]in kentät yhdistetään toisiinsa. Lisätietoja on kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).  

 Tämä ohjeaihe sisältää seuraavat menettelyt:  

-   XML-rakennetiedoston lataaminen  

-   Solmujen valitseminen ja tyhjentäminen XML-rakenteessa  

-   XML-rakenteeseen perustuvan tietojen vaihtamismäärityksen luominen  

-   XML-rakenteeseen perustuvan XMLportin luominen  

-   XMLportin tuominen Objektien suunnittelu -sovellukseen  

### <a name="to-load-an-xml-schema-file"></a>XML-rakennetiedoston lataaminen  

1.  Varmista, että sopiva XML-rakennetiedosto on saatavilla. Tiedostotunniste on .xsd.  

2.  Anna **Etsi**-ruudussa **XML-mallit** ja valitse sitten liittyvä linkki.  

3.  Valitse **Kotisivu**-välilehden **Uusi**-ryhmässä **Uusi**.  

4.  Täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Koodi**|Määritä koodi, jolla identifioit XML-kaavan.|  
    |**Kuvaus**|Määritä XML-kaavan kuvaus.|  

     **Kohdenimitila**-kenttä määrittää riville ladatun XML-mallitiedoston nimitilan (joka voi olla mikä tahansa).  

5.  Valitse **Kotisivu**-välilehden **Käsittely**-ryhmässä **Lataa malli** ja valitse sitten XML-mallin tiedosto.  

     Kun tiedosto on ladattu, rivin muihin kenttiin lisätään tiedoston tiedot ja **Malli on ladattu** -valintaruutu valitaan.  

    > [!NOTE]  
    >  Ladatun XML-rakenteen puu on oletusarvoisesti tiivistettynä. Solmun voi laajentaa **+**-painikkeella. Kaikki solmut voi laajentaa käyttämällä **Laajenna kaikki** -painiketta valintanauhasta.  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a>Solmujen valitseminen ja tyhjentäminen XML-rakenteessa  

1.  Anna **Etsi**-ruudussa **XML-mallin tarkastelutoiminto** ja valitse sitten liittyvä linkki.  

2.  Täytä otsikon kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**XML-mallin koodi**|Määritä vaiheessa 5 lataamasi XML-rakennetiedosto "XML-rakenteen lataaminen" -osiossa.|  
    |**Uuden XMLportin numero**|Määritä sen XMLporttien määrä, joka luodaan tästä XML-kaavasta, kun valitset **Luo XMLport** -ikkunassa.|  

     Rivit on nyt täytettä solmuilla, jotka edustavat kaikki XML-kaavan elementtejä. XML-mallin mukaan pakolliset elementtien solmut valitaan oletusarvoisesti.  

3.  Laajenna ensimmäisellä rivillä **Solmun nimi**-sarakkeessa **Asiakirja**-solmu ja laajenna sitten vähitellen alapuolella olevia solmuja, joita haluat tarkastella.  

     Vaihtoehtoisesti, napsauta solmua hiiren kakkospainikkeella ja valitse sitten **Laajenna kaikki**.  

4.  Valitse **Kotisivu**-välilehden **Näytä**-ryhmässä yksi seuraavista toiminnoista muuttaaksesi mitkä solmut näytetään.  

    |**Toiminto**|Kuvaus|  
    |----------------|---------------------------------------|  
    |**Näytä kaikki**|Kaikki solmut ovat näkyvissä.|  
    |**Piilota ei-pakollinen**|Ainoastaan XML-rakenteen perusteella pakollisia elementtejä esittävät solmut näytetään. Näiden solmujen merkintänä on yleensä **1** **MinOccurs**-kentässä.<br /><br /> Käännä näkymä valitsemalla **Näytä kaikki**.|  
    |**Piilota ei-valittu**|Vain solmut, joissa **Valittu**-valintaruutu on valittuna näytetään.<br /><br /> Käännä näkymä valitsemalla **Näytä kaikki**.|  

5.  Valitse **Kotisivu**-välilehden **Hallinta**-ryhmässä **Muokkaa**.  

6.  Määritä **Valittu**-valintaruutu jokaiselle solmulle, jonka elementin haluat olevan tuettuna liittyvän SEPA-pankkitiedoston tiedonsiirtomäärityksessä.  

    > [!NOTE]  
    >  Kun valitset pakollisen alisolmun, kaikki sen pääsolmut valitaan myös.  

7.  Voit valita uudelleen kaikki solmut, jotka kuvaavat XML-mallin mukaan pakollisia elementtejä valitsemalla **Valitse kaikki pakolliset elementit** -toiminto.  

8.  Poista kaikki valinnat valitsemalla **Poista kaikkien valinta** -toiminto.  

     **Valinta**-kenttä määrittää, että solmulla on vähintään kaksi sisarussolmua, jotka toimivat vaihtoehtoina.  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a>XML-rakenteeseen perustuvan tietojen vaihtamismäärityksen luominen  

1.  Anna **Etsi**-ruudussa **XML-mallit** ja valitse sitten liittyvä linkki.  

2.  Valitse oikea XML-rakenne ja sitten **Koti**-välilehden **Prosessi**-ryhmästä **Avaa XML-rakenteen tarkastelu**.  

3.  Varmista, että tarvittavat solmut ovat valittuina. Lisätietoja on ohjeen kohdassa "Solmujen valitseminen ja tyhjentäminen XML-rakenteessa".  

4.  Valitse **XML-mallin tarkastelutoiminto** -ikkunan **Kotisivu**-välilehden **Käsittely**-ryhmässä **Luo tiedonsiirtomääritys**.  

 Tiedonsiirtomääritys luodaan **Kirjauksen tiedonsiirtomääritykset** -ikkunassa, jossa sen voi viimeistellä määrittämällä, mitkä tiedoston elementit ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in kentät yhdistetään toisiinsa. Lisätietoja on kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).  

> [!NOTE]  
>  Voit käyttää myös **Kirjauksen tiedonsiirtomääritykset** -ikkunan **Hae tiedostorakenne** -toimintoa. Tämä ikkuna täyttää **Sarakkeen määritykset** -pikavälilehden valmiiksi **XML-mallin tarkastelutoiminto** -ikkunan toiminnoilla.  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a>XML-rakenteeseen perustuvan XMLportin luominen  

1.  Anna **Etsi**-ruudussa **XML-mallit** ja valitse sitten liittyvä linkki.  

2.  Valitse soveltuva XML-rakenne ja sitten **Kotisivun**-välilehden **Käsittely**-ryhmässä **Avaa XML-mallin tarkastelutoiminto**.  

3.  Määritä **Uuden XMLportin numero** -kentässä numero, joka annetaan uudelle XMLport-objektille luonnin yhteydessä.  

4.  Varmista, että tarvittavat solmut ovat valittuina. Lisätietoja on ohjeen kohdassa "Solmujen valitseminen ja tyhjentäminen XML-rakenteessa".  

5.  Valitse **Kotisivu**-välilehdellä **Käsittely**-ryhmässä **Luo XMLport** ja tallenna objekti sitten .txt-tiedostona oikeaan paikkaan.  

6. Tuo uusi XMLport [!INCLUDE[d365fin](includes/d365fin_md.md)]in kehitysympäristöön ja käännä se.

## <a name="see-also"></a>Katso myös  
[Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md)   
[Maksujen vienti pankkitiedostoon](payables-how-export-payments-bank-file.md)   
[Maksujen kerääminen SEPA-suoraveloituksena](finance-collect-payments-with-sepa-direct-debit.md)   
[Tietoja tiedonsiirtokehyksestä](across-about-the-data-exchange-framework.md)

