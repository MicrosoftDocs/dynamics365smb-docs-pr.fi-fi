---
title: Asiakkaiden myynnin estäminen
description: Voit tarvittaessa estää asiakasta sisältymästä myyntiasiakirjoihin ja muihin myyntitapahtumiin.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 07/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="block-customers"></a>Asiakkaiden estäminen
Voit sulkea asiakkaan esimerkiksi maksukyvyttömyyden takia, jolloin asiakasta ei voi lisätä myyntiasiakirjoihin tai jotta asiakkaalle ei voi kirjata transaktioita.

Asiakkaan estämisen lisäksi voit määrittää estoon asiakkaan myyntisaatavat yhdessä muistutusten kanssa. Lisätietoja on kohdassa [Avointen saldojen perintä](receivables-collect-outstanding-balances.md).   

Seuraavassa taulukossa kuvaillaan eri asiakkaiden estoasetukset.  

|Asetus|Kuvaus|  
|--------------------|------------|  
|**Tyhjä**|Tapahtumat ovat sallittuja tälle asiakkaalle.|
|**Toimitus**|Tälle asiakkaalle ei voi luoda uusia tilauksia ja toimituksia. Aiemmin luodut toimitukset, joita ei ole vielä laskutettu, saa laskuttaa.|  
|**Lasku**|Tälle asiakkaalle ei voi luoda uusia tilauksia, toimituksia ja laskuja. Aiemmin luotuja toimituksia, joita ei ole vielä laskutettu, ei voi laskuttaa. Voit edelleen lähettää asiakkaalle muistutuksia ja viivästyskulujen laskuja.|  
|**Kaikki**|Yksikään tapahtuma ei ole sallittu tälle asiakkaalle, eivät myöskään maksut.|  

## <a name="to-block-a-customer"></a>Asiakkaan estäminen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Valitse asiakas ja valitse sitten **Muokkaa**-toiminto.
3. Valitse**Estetty**-kentässä, mitä haluat estää, kuten yllä olevassa taulukossa on kuvattu.

## <a name="see-also"></a>Katso myös
[Uusien asiakkaiden rekisteröiminen](sales-how-register-new-customers.md)  
[Avointen saldojen perintä](receivables-collect-outstanding-balances.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
