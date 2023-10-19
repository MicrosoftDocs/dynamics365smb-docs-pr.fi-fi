---
title: Nimikkeiden tai nimikevarianttien estäminen myynnistä tai ostamisesta
description: Voit estää nimikkeiden ja nimikevarianttien syöttämisen myynti- tai ostoasiakirjojen riveille ja estää sen kirjaamiseen kaikissa tapahtumissa.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'item, variant, product'
ms.date: 08/22/2023
---
# <a name="block-items-or-item-variants-from-sales-or-purchasing"></a>Nimikkeiden tai nimikevarianttien estäminen myynnistä tai ostamisesta

Voit estää nimikkeen ja nimikevarianttien syöttämisen myynti- tai ostoasiakirjojen riveille ja estää sen kirjaamiseen tapahtumissa. Tämä on hyödyllistä esimerkiksi silloin, kun nimikkeellä on tunnettu vika. Jos joku valitsee myynti- tai ostoasiakirjassa estetyn nimikkeen tai variantin, viesti ilmoittaa heille, että nimike on suljettu.

Seuraava taulukko kuvaa, mitä tapahtuu, kun nimikkeet tai variantit on estetty.  

|Asetus|Kuvaus|  
|--------------------|------------|  
|**Myynti estetty**|Nimikettä tai varianttia ei voi valita myyntiasiakirjassa tai myynnin nimikepäiväkirjassa.|  
|**Osto estetty**|Et voi valita nimikettä tai varianttia ostoasiakirjassa, ostonimikepäiväkirjassa tai ostojen suunnitteluprosesseissa.|  
|**Suljettu**|Nimikettä tai varianttia ei voi sisällyttää transaktioita kirjatessa.|  

> [!NOTE]
> Estetyt nimikkeet voidaan palauttaa. Tämä tarkoittaa sitä, etteivät mitkään yllämainitut asetukset päde palautustilauksissa ja hyvitysmaksuissa.

Kun luot uusia asiakirjoja aiemmin luotujen asiakirjojen perusteella **Kopioi asiakirjasta** -toiminnolla, saat ilmoituksen, jos lähdeasiakirjan riveillä olevia nimikkeitä tai variantteja on estetty. Estetyt asiakirjarivit jätetään pois uudesta asiakirjasta, ja ilmoitus sisältää yhteenvedon kaikista lähdeasiakirjassa estetyistä asiakirjariveistä.

## <a name="to-block-an-item"></a>Nimikkeen estäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.  
2. Valitse nimike sen mukaan, mitä haluat tehdä, ja valitse sitten yksi tai useampi seuraavista valintaruuduista:
    * **Suljettu**
    * **Myynti estetty**
    * **Osto estetty**  

## <a name="to-block-an-item-variant"></a>Nimikevariantin estäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.  
2. Valitse nimike, jonka variantin haluat estää, valitse **Variantit** ja valitse sitten yksi tai useampi seuraavista valintaruutuista:  
    * **Suljettu**
    * **Myynti estetty**
    * **Osto estetty**

## <a name="see-also"></a>Katso myös

[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Varasto](inventory-manage-inventory.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
