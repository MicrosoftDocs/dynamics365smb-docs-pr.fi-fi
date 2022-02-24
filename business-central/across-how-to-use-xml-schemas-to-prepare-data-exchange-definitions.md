---
title: XML-malleihin perustuvien XMLports-kohteiden luominen | Microsoft Docs
description: Voit määrittää tiedonsiirtokehyksen XML-mallien avulla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 60b1e7ad420e805e27ad27d8aa7c66fb1274e7b5
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187993"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a>XML-mallien käyttäminen tietojenvaihtomääritysten valmisteluun
Voit ottaa XML-tiedostojen tietojen tuonnin ja viennin käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]in tiedonsiirtokehyksessä määrittämällä [!INCLUDE[d365fin](includes/d365fin_md.md)]in kanssa vaihdettavat tietoelementit XML-mallien avulla. Se tehdään **XML-mallin tarkastelutoiminto** -sivulla lataamalla XML-rakennetiedosto, valitsemalla sopivat tietoelementit ja käynnistämällä joko tietojen vaihdon määritys tai XMLport.  

 Kun olet määrittänyt XML-mallin perusteella sisällytettävät tietoelementit, voit luoda XMLport-objektin **Luo XMLport** -toiminnolla.  

 Voit myös käyttää **Luo tietojen vaihdon määritys** -toimintoa luodaksesi valittuihin tietoelementteihin perustuvan määrityksen, jonka sitten viimeistelet tietojen vaihtamiskehyksessä. Tällä tavoin **Kirjauksen tiedonsiirtomääritykset** -sivulla luodaan tietue. Jatka sivulla määrittämällä, mitkä tiedoston elementit ja mitkä [!INCLUDE[d365fin](includes/d365fin_md.md)]in kentät yhdistetään toisiinsa. Lisätietoja on kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).  

 Tämä ohjeaihe sisältää seuraavat menettelyt:  

-   XML-rakennetiedoston lataaminen  

-   Solmujen valitseminen ja tyhjentäminen XML-rakenteessa  

-   XML-rakenteeseen perustuvan tietojen vaihtamismäärityksen luominen  

-   XML-rakenteeseen perustuvan XMLportin luominen  

-   XMLportin tuominen objektien suunnitteluohjelmaan  

### <a name="to-load-an-xml-schema-file"></a>XML-rakennetiedoston lataaminen  

1.  Varmista, että sopiva XML-rakennetiedosto on saatavilla. Tiedostotunniste on .xsd.  

2.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **XML-mallit** ja valitse sitten liittyvä linkki.  

3.  Valitse **Uusi**-toiminto.  

4.  Täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Koodi**|Määritä koodi, jolla identifioit XML-kaavan.|  
    |**Kuvaus**|Määritä XML-kaavan kuvaus.|  

     **Kohdenimitila**-kenttä määrittää riville ladatun XML-mallitiedoston nimitilan (joka voi olla mikä tahansa).  

5.  Valitse **Lataa malli** -toiminto ja valitse XML-mallitiedosto.  

     Kun tiedosto on ladattu, rivin muihin kenttiin lisätään tiedoston tiedot ja **Malli on ladattu** -valintaruutu valitaan.  

    > [!NOTE]  
    >  Ladatun XML-rakenteen puu on oletusarvoisesti tiivistettynä. Solmun voi laajentaa **+**-painikkeella. Kaikki solmut voi laajentaa käyttämällä **Laajenna kaikki** -painiketta valintanauhasta.  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a>Solmujen valitseminen ja tyhjentäminen XML-rakenteessa  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **XML-mallin tarkastelutoiminto** ja valitse sitten liittyvä linkki.  

2.  Täytä otsikon kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**XML-mallin koodi**|Määritä vaiheessa 5 lataamasi XML-rakennetiedosto "XML-rakenteen lataaminen" -osiossa.|  
    |**Uuden XMLportin numero**|Määritä niiden XMLporttien määrä, jotka luodaan tästä XML-kaavasta, kun valitset **Luo XMLport** -toiminnon.|  

     Rivit on nyt täytettä solmuilla, jotka edustavat kaikki XML-kaavan elementtejä. XML-mallin mukaan pakolliset elementtien solmut valitaan oletusarvoisesti.  

3.  Laajenna ensimmäisellä rivillä **Solmun nimi**-sarakkeessa **Asiakirja**-solmu ja laajenna sitten vähitellen alapuolella olevia solmuja, joita haluat tarkastella.  

     Vaihtoehtoisesti, napsauta solmua hiiren kakkospainikkeella ja valitse sitten **Laajenna kaikki**.  

4.  Valitse yksi seuraavista toiminnoista muuttaaksesi mitkä solmut näytetään.  

    |**Toiminto**|Kuvaus|  
    |----------------|---------------------------------------|  
    |**Näytä kaikki**|Kaikki solmut ovat näkyvissä.|  
    |**Piilota ei-pakollinen**|Ainoastaan XML-rakenteen perusteella pakollisia elementtejä esittävät solmut näytetään. Näiden solmujen merkintänä on yleensä **1** **MinOccurs**-kentässä.<br /><br /> Käännä näkymä valitsemalla **Näytä kaikki**.|  
    |**Piilota ei-valittu**|Vain solmut, joissa **Valittu**-valintaruutu on valittuna näytetään.<br /><br /> Käännä näkymä valitsemalla **Näytä kaikki**.|  

5.  Valitse **Muokkaa** -toiminto.  

6.  Määritä **Valittu**-valintaruutu jokaiselle solmulle, jonka elementin haluat olevan tuettuna liittyvän SEPA-pankkitiedoston tiedonsiirtomäärityksessä.  

    > [!NOTE]  
    >  Kun valitset pakollisen alisolmun, kaikki sen pääsolmut valitaan myös.  

7.  Voit valita uudelleen kaikki solmut, jotka kuvaavat XML-mallin mukaan pakollisia elementtejä valitsemalla **Valitse kaikki pakolliset elementit** -toiminto.  

8.  Poista kaikki valinnat valitsemalla **Poista kaikkien valinta** -toiminto.  

     **Valinta**-kenttä määrittää, että solmulla on vähintään kaksi sisarussolmua, jotka toimivat vaihtoehtoina.  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a>XML-rakenteeseen perustuvan tietojen vaihtamismäärityksen luominen  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **XML-mallit** ja valitse sitten liittyvä linkki.  

2.  Valitse sopiva XML-malli ja valitse sitten **Avaa XML-mallin tarkastelutoiminto** -toiminto.  

3.  Varmista, että tarvittavat solmut ovat valittuina. Lisätietoja on ohjeen kohdassa "Solmujen valitseminen ja tyhjentäminen XML-rakenteessa".  

4.  Valitse **XML-mallin tarkastelutoiminto** -sivulla **Luo tiedonsiirtomääritys** -toiminto.  

 Tiedonsiirtomääritys luodaan **Kirjauksen tiedonsiirtomääritykset** -sivulla, jossa sen voi viimeistellä määrittämällä, mitkä tiedoston elementit ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in kentät yhdistetään toisiinsa. Lisätietoja on kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).  

> [!NOTE]  
>  Voit käyttää myös **Kirjauksen tiedonsiirtomääritykset** -sivun **Hae tiedostorakenne** -toimintoa. Tämä sivu täyttää **Sarakkeen määritykset** -pikavälilehden valmiiksi **XML-mallin tarkastelutoiminto** -sivun toiminnoilla.  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a>XML-rakenteeseen perustuvan XMLportin luominen  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **XML-mallit** ja valitse sitten liittyvä linkki.  

2.  Valitse sopiva XML-malli ja valitse sitten **Avaa XML-mallin tarkastelutoiminto** -toiminto.  

3.  Määritä **Uuden XMLportin numero** -kentässä numero, joka annetaan uudelle XMLport-objektille luonnin yhteydessä.  

4.  Varmista, että tarvittavat solmut ovat valittuina. Lisätietoja on ohjeen kohdassa "Solmujen valitseminen ja tyhjentäminen XML-rakenteessa".  

5.  Valitse Luo **Luo XMLport** -toiminto ja tallenna objekti sitten .txt-tiedostona oikeaan paikkaan.  

6. Tuo uusi XMLport [!INCLUDE[d365fin](includes/d365fin_md.md)]in kehitysympäristöön ja käännä se.

## <a name="see-also"></a>Katso myös  
[Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md)   
[Maksujen vienti pankkitiedostoon](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)   
[Maksujen kerääminen SEPA-suoraveloitusperintänä](finance-collect-payments-with-sepa-direct-debit.md)   
[Tietoja tiedonvaihto-kehyksestä](across-about-the-data-exchange-framework.md)
