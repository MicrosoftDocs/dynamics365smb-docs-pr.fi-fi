---
title: Rakennetiedot – Pääkirjanpidon tilit | Microsoft Docs
description: 'Kun varasto ja kapasiteettitapahtumat täsmäytetään pääkirjanpidon kanssa, liittyvät arvotapahtumat kirjataan pääkirjanpidon eri tileille.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
---
# <a name="design-details-accounts-in-the-general-ledger"></a>Rakennetiedot: pääkirjanpidon tilit
Kun varasto ja kapasiteettitapahtumat täsmäytetään pääkirjanpidon kanssa, liittyvät arvotapahtumat kirjataan pääkirjanpidon eri tileille. Lisätietoja on kohdassa [Rakennetiedot: täsmäytys pääkirjanpidon kanssa](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="from-the-inventory-ledger"></a>Inventointitapahtumista
Seuraavassa taulukossa esitetään suhde eri varastoarvojen kirjausten ja pääkirjan tilien ja balansoitavien tilien välillä.  

|**Nimiketapahtuman tyyppi**|**Arvotapahtuman tyyppi**|**Vaihtelutyyppi**|**Oletettu kustannus**|**Tili**|**Vastatili**|  
|--------------------------------|--------------------------|-----------------------|-----------------------|-----------------|---------------------------|  
|Osto|Välitön kustannus||Kyllä|Varasto (väliaik.)|Varaston kertymätili (väliaik)|  
|Osto|Välitön kustannus||Ei|Vaihto-omaisuus|Kohdistettu välitön kustannus|  
|Osto|Välillinen kustannus||Ei|Vaihto-omaisuus|Kohdistettu yleiskust.|  
|Osto|Vaihtelu|Osto|Ei|Vaihto-omaisuus|Ostovaihtelu|  
|Osto|Uudelleenarvostus||Ei|Vaihto-omaisuus|Varastonmuutos|  
|Osto|Pyöristäminen||Ei|Vaihto-omaisuus|Varastonmuutos|  
|Myynti|Välitön kustannus||Kyllä|Varasto (väliaik.)|M.t.kust. (väliaik.)|  
|Myynti|Välitön kustannus||Ei|Vaihto-omaisuus|MTK|  
|Myynti|Uudelleenarvostus||Ei|Vaihto-omaisuus|Varastonmuutos|  
|Myynti|Pyöristäminen||Ei|Vaihto-omaisuus|Varastonmuutos|  
|Posit. muutos,Negat. muutos, Var.siirto|Välitön kustannus||Ei|Vaihto-omaisuus|Varastonmuutos|  
|Posit. muutos,Negat. muutos, Var.siirto|Uudelleenarvostus||Ei|Vaihto-omaisuus|Varastonmuutos|  
|Posit. muutos,Negat. muutos, Var.siirto|Pyöristäminen||Ei|Vaihto-omaisuus|Varastonmuutos|  
|(Tuotanto) Kulutus|Välitön kustannus||Ei|Vaihto-omaisuus|KET|  
|(Tuotanto) Kulutus|Uudelleenarvostus||Ei|Vaihto-omaisuus|Varastonmuutos|  
|(Tuotanto) Kulutus|Pyöristäminen||Ei|Vaihto-omaisuus|Varastonmuutos|  
|Kokoonpanon kulutus|Välitön kustannus||Ei|Vaihto-omaisuus|Varastonmuutos|  
|Kokoonpanon kulutus|Välitön kustannus||Ei|Kohdistettu välitön kustannus|Varastonmuutos|  
|Kokoonpanon kulutus|Välillinen kustannus||Ei|Kohdistettu yleiskust.|Varastonmuutos|  
|(Tuotannon) tuotos|Välitön kustannus||Kyllä|Varasto (väliaik.)|KET|  
|(Tuotannon) tuotos|Välitön kustannus||Ei|Vaihto-omaisuus|KET|  
|(Tuotannon) tuotos|Välillinen kustannus||Ei|Vaihto-omaisuus|Kohdistettu yleiskust.|  
|(Tuotannon) tuotos|Vaihtelu|Materiaali|Ei|Vaihto-omaisuus|Materiaalin vaihtelu|  
|(Tuotannon) tuotos|Vaihtelu|Kapasiteetti|Ei|Vaihto-omaisuus|Kapasit. vaihtelu|  
|(Tuotannon) tuotos|Vaihtelu|Alihankinta|Ei|Vaihto-omaisuus|Alihankkijavaihtelu|  
|(Tuotannon) tuotos|Vaihtelu|Kapasiteetin yleiskustannus|Ei|Vaihto-omaisuus|Kapasit. yleisvaihtelu|  
|(Tuotannon) tuotos|Vaihtelu|Tuotannon yleiskustannus|Ei|Vaihto-omaisuus|Valm. yleisvaihtelu|  
|(Tuotannon) tuotos|Uudelleenarvostus||Ei|Vaihto-omaisuus|Varastonmuutos|  
|(Tuotannon) tuotos|Pyöristäminen||Ei|Vaihto-omaisuus|Varastonmuutos|  
|Kokoonpanon tuotos|Välitön kustannus||Ei|Vaihto-omaisuus|Varastonmuutos|  
|Kokoonpanon tuotos|Uudelleenarvostus||Ei|Vaihto-omaisuus|Varastonmuutos|  
|Kokoonpanon tuotos|Välillinen kustannus||Ei|Vaihto-omaisuus|Kohdistettu yleiskust.|  
|Kokoonpanon tuotos|Vaihtelu|Materiaali|Ei|Vaihto-omaisuus|Materiaalin vaihtelu|  
|Kokoonpanon tuotos|Vaihtelu|Kapasiteetti|Ei|Vaihto-omaisuus|Kapasit. vaihtelu|  
|Kokoonpanon tuotos|Vaihtelu|Kapasiteetin yleiskustannus|Ei|Vaihto-omaisuus|Kapasit. yleisvaihtelu|  
|Kokoonpanon tuotos|Vaihtelu|Tuotannon yleiskustannus|Ei|Vaihto-omaisuus|Valm. yleisvaihtelu|  
|Kokoonpanon tuotos|Pyöristäminen||Ei|Vaihto-omaisuus|Varastonmuutos|  

## <a name="from-the-capacity-ledger"></a>Kapasiteettikirjauksista
 Seuraavassa taulukossa esitetään suhde eri kapasiteettiarvojen kirjausten ja pääkirjan tilien ja balansoitavien tilien välillä. Kapasiteettitapahtumat edustavat kulutettua työaikaa kokoonpano- tai tuotantotyössä.  

|**Työn tyyppi**|**Kapasiteettitapahtuman tyyppi**|**Arvotapahtuman tyyppi**|**Tili**|**Vastatili**|  
|-------------------|------------------------------------|--------------------------|-----------------|---------------------------|  
|Kokoonpano|Resurssi|Välitön kustannus|Kohdistettu välitön kustannus|Varastonmuutos|  
|Kokoonpano|Resurssi|Välillinen kustannus|Kohdistettu yleiskust.|Varastonmuutos|  
|Tuotanto|Kuormitusryhmä/tuotantosolu|Välitön kustannus|KET tili|Kohdistettu välitön kustannus|  
|Tuotanto|Kuormitusryhmä/tuotantosolu|Välillinen kustannus|KET tili|Kohdistettu yleiskust.|  

## <a name="assembly-costs-are-always-actual"></a>Kokoonpanokustannukset ovat aina todellisia
 Kuten yllä olevassa taulukossa on esitetty, kirjauksia ei esitetä väliaikaisilla tileillä. Tämä johtuu siitä, että KET:n konsepti ei ole käytössä kokoonpanon tuotoksen kirjauksessa, toisin kuin tuotannon tuotoksen kirjaus. Kokoonpanokustannukset kirjataan vain todellisina kustannuksina, eikä koskaan oletettuina kustannuksina.  

 Katso lisätietoja kohdasta [Rakennetiedot: kokoonpanotilauksen kirjaus](design-details-assembly-order-posting.md).  

## <a name="calculating-the-amount-to-post-to-the-general-ledger"></a>Lasketaan pääkirjanpitoon kirjattavaa summaa
 Seuraavia kenttiä **Arvotapahtuma**-taulukossa käytetään laskemaan arvioitu kustannussumma, joka on tiliöity pääkirjaan:  

-   Kustannussumma (todellinen)  
-   KP:oon kirjattu kustannus  
-   Kustannussumma (oletettu)  
-   Olet. kust. kirjattu KP:oon  

Seuraavassa taulukossa esitetään, kuinka pääkirjaan tiliöitävät summat lasketaan kahdelle eri kustannustyypille.  

|Kustannustyyppi|Laskenta|  
|---------------|-----------------|  
|Todellinen kustannus|Kustannussumma (todellinen) – KP-kirjattu kustannus|  
|Oletettu kustannus|Kustannussumma (oletettu) – Olet. kust. kirjattu KP:oon|  

## <a name="see-also"></a>Katso myös
 [Rakennetiedot: varaston arvostus](design-details-inventory-costing.md)   
 [Rakennetiedot: varaston kirjaus](design-details-inventory-posting.md)   
 [Rakennetiedot: Oletetun kustannuksen kirjaus](design-details-expected-cost-posting.md)  
 [Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
 [Rahoitus](finance.md)  
 [Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
