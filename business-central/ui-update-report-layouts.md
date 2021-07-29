---
title: Raporttiasettelun pitäminen ajan tasalla
description: Tietoja raportissa käytettävän mukautetun raporttiasettelun päivittämisestä, kun esimerkiksi raportin tietojoukkoon on tehty rakennemuutoksia.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 99b0f191bf9890683bb6cbb68f7baef0342f9737
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6445274"
---
# <a name="update-custom-report-layouts"></a>Päivitä mukautetut raporttiasettelut
Joskus saatat joutua päivittämään raportissa käytettyä mukautettua asettelua. Tämä vaaditaan, kun raportin tietojoukko on muuttunut, esimerkiksi asettelussa käytetty kenttä on poistettu raportin tietojoukosta. Raporttiasettelu on päivitettävä, jos saat virhesanoman, kun yrität tarkastella, tulostaa tai tallentaa raportin.  

Voit päivittää raporttiasettelun automaattisesti valitsemalla **Kyllä** raportin suorituksen aikana avautuvassa virhesanomassa. Voit päivittää tietyt raporttiasettelut tai kaikki mukautetut raporttiasettelut, joihin tietojoukon muutokset ovat saattaneet vaikuttaa, ennen raporttien suorittamista.  

Voit myös halutessasi testata päivitykset tekemättä vaadittuja muutoksia mukautettuihin raporttiasetteluihin. Tämän ansiosta voit nähdä, mitä muutoksia raporttiasetteluun tulee ja tunnistaa mahdolliset ongelmat. Testituloksista voi avata mukautetut raporttiasettelut suoraan muokattavaksi, jotta voit korjata mahdolliset ongelmat. Suosittelemme kuitenkin testaamaan raporttiasetteluiden päivitykset ennen päivitysten asentamista.  

Kaikkia raportin tietojoukon muutoksia ei voi päivittää automaattisesti raporttiasetteluihin. Jotkin muutokset edellyttävät raporttiasettelun manuaalista muokkaamista. Lisätietoja on ohjeaiheessa [Mukautettujen raporttiasetteluiden päivittämisen rajoitukset](ui-update-report-layouts.md#UpdateLimitations).  

## <a name="to-update-one-or-more-custom-report-layouts"></a>Vähintään yhden mukautetun raportin asettelun päivittäminen  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Raporttiasettelut** ja valitse sitten vastaava linkki.  

2.  Jos haluat päivittää tietyn raportin, valitse ensin asettelu luettelosta **Raporttiasettelut**-sivulla ja sitten **Päivitä asettelu** -toiminto. Jos sen sijaan haluat päivittää yrityksen kaikki mukautetut raporttiasettelut, valitse **Päivitä kaikki asettelut** -toiminto.  

Jos virheitä ei ilmene, päivitykset otetaan käyttöön raporttiasetteluissa. Jos virheitä esiintyy, järjestelmä näyttää viestin, joka sisältää virheet. Päivityksen jälkeen mukautettua raporttiasettelua on muokattava virheen korjaamiseksi. Lisätietoja on kohdassa [Virheiden korjaaminen](ui-update-report-layouts.md#FixErrors).  

## <a name="to-test-custom-report-layout-updates"></a>Mukautettujen raporttiasetteluiden päivitysten testaaminen  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Raporttiasetteluvalinta** ja valitse sitten vastaava linkki.  

2.  Valitse **Raporttiasetteluvalinta**-sivulla **Testiasettelun päivitykset** -toiminto.  

 Raporttiasettelujen muutokset testataan, mutta niitä ei käytetä varsinaisissa raporttiasetteluissa. **Raporttiasettelun päivitysloki** -sivu avautuu, ja siinä näytetään jokaiselle raporttiasettelulle tulevat päivitykset sekä niiden tila. Jos raporttiasettelulla on virheitä, voit avata raporttiasettelun suoraan viestistä muokkaamista varten. Lisätietoja on kohdassa [Virheiden korjaaminen](ui-update-report-layouts.md#FixErrors).  

##  <a name="limitations-of-the-custom-report-layout-update"></a><a name="UpdateLimitations"></a> Mukautettujen raporttiasetteluiden päivittämisen rajoitukset  
 Automaattinen päivitys voi tehdä monenlaisia muutoksia mukautettuihin raporttiasetteluihin, kuten jos asettelussa käytettävä kenttä on poistettu raportin tietojoukosta. Seuraavia muutoksia raportin tietojoukkoon automaattinen päivitys ei kuitenkaan käsittele.  

1.  Poistetut kentät, otsikot ja tietokohteet.  

2.  Monistaa kenttien nimet raporttiasettelussa sen jälkeen, kun kenttä on nimetty uudelleen tietojoukossa. Tämä tulisi käsitellä suunnitteluvirheenä.  

3.  Päivitystapaukset, joissa raporttiasettelun useammat toistot aiheuttavat useita uudelleennimeämistoimintoja samoille kentille, otsikoille tai tietonimikkeille.  

 Jos päivitysprosessi havaitsee jonkin näistä ongelmista, päivitystä ei voi ottaa käyttöön. Nämä ongelmat on korjattava manuaalisesti, esimerkiksi muokkaamalla raporttia käsin Wordissa tai ohjelmallisesti käyttämällä päivityksen codeuniteja.  

##  <a name="fixing-errors"></a><a name="FixErrors"></a> Virheiden korjaaminen  
 Jos virhesanoma tulee näkyviin raporttiasettelun päivityksen tai testauksen jälkeen, sinun on todennäköisesti muokattava raportin asettelua ongelman korjaamiseksi. Lue virhesanoma, jonka avulla voit selvittää ongelman syyn.  

 Yleisin ongelma ilmenee, kun asettelussa käytetty kenttä on poistettu raportin tietojoukosta. Tässä tapauksessa näet virhesanoman rivin, joka ilmoittaa, että nimike on poistettu. Jotta voit korjata tämän ongelman, sinun on muokattava asettelua ja poistettava kyseinen kenttä.  

 Lisätietoja on kohdassa [Raportin mukautetun asettelun luominen ja muokkaaminen](ui-how-create-custom-report-layout.md#ModifyCustomLayout).  

Kun muutat asettelua, yritä päivittää asettelu uudelleen.  

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös  
 [Raporttiasetteluiden hallinta](ui-manage-report-layouts.md)  
 [Raporttien, eräajojen ja XMLportien käsitteleminen](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]