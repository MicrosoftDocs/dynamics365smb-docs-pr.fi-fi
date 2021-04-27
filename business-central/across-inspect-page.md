---
title: Business Centralin tarkastussivut
description: Lähennä sivun rakennetta ja tietolähdettä koskeviin tietoihin sivun tarkastustoiminnolla. Sivun tarkastustoiminto sopii hyvin tietoja koskevien ongelmien vianmääritykseen.
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: conceptual
ms.service: dynamics365-business-central
author: jswymer
ms.author: jswymer
ms.date: 04/01/2021
ms.openlocfilehash: 09dba629e977707921129261ea2540cc223c15dc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784938"
---
# <a name="inspecting-pages-in-business-central"></a>Business Centralin tarkastussivut

Saat sivun tarkastustoiminnolla tietoja sivusta sekä merkityksellisiä tietoja sivun rakenteesta, elementeistä, joista sivu koostuu, ja sivulla näkyvien tietojen lähteestä. Sivun tarkastus on suunniteltu järjestelmänvalvojille, tehokäyttäjille, tukihenkilöstölle ja kehittäjille. Sen sopii erityisesti sivun taustalla olevaan tietomalliin tutustumiseen ja vianmääritykseen. Jos sivulla on esimerkiksi ongelma, saat sivun tarkastustoiminnolla tietoja, jotka voit välittää järjestelmänvalvojalle ja tukihenkilöstölle.

## <a name="working-with-page-inspection"></a>Sivun tarkastuksen käyttäminen

Sivun tarkistus aloitetaan **Ohje ja tuki** -sivulla. Valitse ensin kysymysmerkki oikeassa yläkulmassa, sitten **Ohje ja tuki** ja lopuksi **Tarkasta sivut ja tiedot**. Vaihtoehtoisesti voit käyttää pikanäppäintä **Ctrl+Alt+F1**.

**Sivun tarkastus** -ruutu avautuu sivulle. Seuraavassa kuvassa on **Myyntitilaus**-sivun **Sivun tarkastus** -ruutu.

![Sivun tarkastus](media/page-inspection-example.png)

Kun **Sivun tarkastus** -ruutu avautuu ensimmäisen kerran, siinä pääsivukohteeseen liittyviä tietoja.

Siirrä kohdistus näppäimillä tai osoitinlaitteella sivun eri elementteihin. Kun valitset pääsivulla tietoruudun tai osan, raja korostaa täsmällisen alueen ja **Sivun tarkastus** -ruudussa on tietoja valitusta elementistä. Esimerkiksi edellisessä kuvassa on tietoja **Myyntitilaus**-sivun luettelo-osasta. Kun siirryt sovelluksessa muille sivulle, **Sivun tarkastus** -ruutu päivittyy automaattisesti sen sivun tiedoilla, johon olet siirtynyt.

Lisätietoja sivun tarkastuksessa näytettävistä tiedoista on Business Centralin kehittäjien IT-ammattilaisten ohjeen kohdassa [Sivun tarkastaminen ja vianmääritys](/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages).

Jos odottamasi tiedot eivät näy **Sivun tarkastus** -ruudussa, käyttöoikeutesi eivät luultavasti ole riittävät. Tätä käsitellään seuraavassa osassa.

## <a name="controlling-access-to-page-inspection-details"></a>Sivun tarkastustietojen käyttöoikeuksien hallinta

Voit hallita järjestelmänvalvojana **Sivun tarkastus** -ruudussa näytettävien tietojen käyttöoikeuksia määrittämällä käyttäjien käyttöoikeudet. Voit antaa käyttäjälle kaikkien tietojen käyttöoikeudet antamalla hänelle **Toteuta**-käyttöoikeus **Järjestelmä**-kohteessa **5330**. Voit myöntää tämän käyttöoikeuden käyttämällä käyttöoikeuksien joukkoa (kuten **D365-vianmääritys**) tai käyttäjäryhmää (kuten **D365-vianmääritys**). Lisätietoja käyttöoikeuksista on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).

Käyttäjät, joilla ei ole myönnetty käyttöoikeuksia **järjestelmäkohteessa 5330**, voivat silti käyttää **Sivun tarkastus** -ruutua. He näkevät kuitenkin vain **Sivu**- ja **Taulukko**-kentät. Käyttäjät voivat sitten välittää näiden kenttien perustiedot tukitiimilleen.

## <a name="see-also"></a>Katso myös

[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]