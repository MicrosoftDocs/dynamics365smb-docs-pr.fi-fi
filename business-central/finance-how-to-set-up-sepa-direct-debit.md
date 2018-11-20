---
title: "SEPA-suoraveloituksen määrittäminen | Microsoft Docs"
description: "Tietoja SEPA-suoraveloituksen määrittämisestä Business Central -sovelluksessa."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0ba40eb247c1edb2b4d8c7437bf60790545799ee
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-sepa-direct-debit"></a>SEPA-suoraveloituksen määrittäminen
**Suoraveloitusperinnät** -ikkunasta voit viedä sähköiseen pankkiisi ohjeita, jotka ohjaavat pankkiasi suorittamaan suoraveloituksen asiakkaan pankkitililtä omalle pankkitilillesi. [!INCLUDE[d365fin](includes/d365fin_md.md)] tukee SEPA-suoraveloitusmuotoa, mutta maassasi tai alueellasi saattaa olla käytettävissä muita sähköisten maksujen muotoja.  

Jos haluat ottaa käyttöön sellaisten pankkitiedostomuotojen viennin, joita [!INCLUDE[d365fin](includes/d365fin_md.md)] ei tue sellaisenaan, voit määrittää tietojen siirtomäärityksen käyttämällä tiedonsiirtokehystä. Lisätietoja on kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).  

Ennen kuin voit käsitellä asiakkaan maksuja sähköisesti viemällä suoraveloitusohjeita SEPA Direct Debit -muodossa, sinun on suoritettava seuraavat määritysvaiheet.  

* Määritä sen pankkitiedoston vientimuoto, joka ohjaa pankkiasi suorittamaan suoraveloituksen asiakkaan pankkitililtä omalle pankkitilillesi.  
* Määritä asiakkaan maksutapa.  
* Määritä suoraveloitustoimeksianto, joka kuvaa asiakkaan kanssa tekemääsi sopimusta maksujen keräämisestä tietyllä sopimuskaudella.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a>SEPA-suoraveloituksen pankkitilin määrittäminen  
1. Syötä **Etsi**-ruudussa **Pankkitilit** ja valitse sitten vastaava linkki.  
2. Avaa pankkitili, jota haluat käyttää suoraveloitukseen.  
3. Valitse **Siirto**-pikavälilehden **SEPA-suoraveloituksen vientimuoto** -kentässä SEPA-suoraveloitusasetus.  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a>SEPA-suoraveloituksen asiakkaan maksutavan määrittäminen  
1. Anna **Haku**-ruudussa **Maksutavat** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Määritä maksutapa. Täytä suoraveloituskohtaiset kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Suoraveloitus**|Määrittää, käytetäänkö maksutapaa SEPA-suoraveloitusperintään.|  
    |**Suoraveloituksen maksuehtojen koodi**|Määritä maksuehdot, kuten ÄLÄ MAKSA, jotka näkyvät SEPA-suoraveloituksena maksettavissa myyntilaskuissa ilmoittamassa asiakkaalle, että maksu kerätään automaattisesti. Vaihtoehtoisesti tämän kentän voi jättää tyhjäksi.|  

    > [!NOTE]  
    >  Älä anna arvoa **Vastatilin nro** -kenttään.  

4. Valitse **OK**-painike **Maksutavat** -ikkunan sulkemiseksi.  
5. Syötä **Etsi**-ruudussa **Asiakkaat** ja valitse sitten vastaava linkki.  
6. Avaa asiakkaan kortti asiakkaalle, jolle haluat määrittää SEPA-suoraveloitusperinnän.  
7. Valitse **Maksutavan koodi** -kenttä ja sitten maksutavan koodi, jonka määritit vaiheessa 3.  
8. Toista vaiheet 6–7 kaikille asiakkaille, joille haluat määrittää SEPA-suoraveloitusperinnän.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a>Suoraveloitusvaltakirjan määrittäminen, joka vastaa asiakkaan sopimusta  
1. Syötä **Etsi**-ruudussa **Asiakkaat** ja valitse sitten vastaava linkki.  
2. Avaa asiakkaan kortti, jonka haluat määrittää SEPA-suoraveloituksille.  
3. Valitse **Pankkitilit**-toiminto.  
4. Valitse **Asiakkaan pankkitililuettelo** -ikkunassa asiakkaan pankkitili, jota käytät suoraveloitukseen ja valitse sitten **Koti**-välilehden **Käsittely**-ryhmässä **Suoraveloitusvaltakirja**.  
5. Täytä **Suoraveloitusvaltakirjat** -ikkunan kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Asiakkaan pankkitilin koodi**|Määrittää pankkitilin, josta suoraveloitusmaksut kerätään. Tämä kenttä täytetään automaattisesti.|  
    |**Voimassaolo alkaa**|Määritä päivämäärä, jolloin suoraveloitusvaltakirja alkaa.|  
    |**Voimassaolo päättyy**|Määritä päivämäärä, jolloin suoraveloitusvaltakirja päättyy.|  
    |**Allekirjoituspäivämäärä**|Määritä päivämäärä, jolloin asiakas allekirjoitti suoraveloitusvaltakirjan.|  
    |**Maksun tyyppi**|Määritä, koskeeko sopimus useita (**Toistuva**) tai yksittäisiä (**Kerta**) suoraveloitusperintöjä.|  
    |**Debetien odotettu määrä**|Määritä, kuinka monta suoraveloitusperintään sinulla on tarkoitus tehdä. Tämä kenttä on merkittävä vain, jos olet valinnut **Toistuva**-vaihtoehdon **Maksun tyyppi** -kentästä.|  
    |**Debet-laskuri**|Määrittää, kuinka monta suoraveloitusperintää on tehty tätä suoraveloitusvaltakirjaa käyttämällä. Tämä kenttä päivitetään automaattisesti.|  
    |**Suljettu**|Määrittää, kuinka monta suoraveloitusperintää ei voida tehdä tätä suoraveloitusvaltakirjaa käyttämällä.|  

6.  Toista vaiheet 1–5 kaikille asiakkaille, joille haluat määrittää SEPA-suoraveloitukset.  

 Suoraveloitusvaltakirja lisätään automaattisesti **Suoraveloitusvaltakirjan tunnus** -kenttään, kun luot myyntilaskun vaiheessa 2 valitulle asiakkaalle. Lisätietoja on kohdassa [Toistuvien myynti- ja ostorivien luominen](sales-how-work-standard-lines.md).  

## <a name="see-also"></a>Katso myös  
[Maksujen kerääminen SEPA-suoraveloitusperintänä](finance-collect-payments-with-sepa-direct-debit.md)  
[Tiedonsiirtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md)
[Toistuvien myynti- ja ostorivien luominen](sales-how-work-standard-lines.md)
[Sähköinen tiedonsiirto](across-data-exchange.md)

