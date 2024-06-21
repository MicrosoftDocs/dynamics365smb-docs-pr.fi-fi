---
title: Business Centralin tarkastussivut
description: Lähennä sivun rakennetta ja tietolähdettä koskeviin tietoihin sivun tarkastustoiminnolla. Sivun tarkastustoiminto sopii hyvin tietoja koskevien ongelmien vianmääritykseen.
ms.topic: conceptual
author: jswymer
ms.author: jswymer
ms.date: 09/15/2023
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# Business Centralin tarkastussivut

Saat sivun tarkastustoiminnolla tietoja sivusta sekä merkityksellisiä tietoja sivun rakenteesta, elementeistä, joista sivu koostuu, ja sivulla näkyvien tietojen lähteestä. Sivun tarkastus on suunniteltu järjestelmänvalvojille, tehokäyttäjille, tukihenkilöstölle ja kehittäjille. Sen sopii erityisesti sivun taustalla olevaan tietomalliin tutustumiseen ja vianmääritykseen. Jos sivulla on esimerkiksi ongelma, saat sivun tarkastustoiminnolla tietoja, jotka voit välittää järjestelmänvalvojalle ja tukihenkilöstölle.

> [!NOTE]  
> [!INCLUDE [prod_short](includes/prod_short.md)] vuoden 2023 2. julkaisuaallossa voi aloittaa Visual Studio Coden WWW-asiakasohjelmassa sivun tarkistuksen avulla laajennuksen lähdekoodin tutkimista ja virheenkorjausta varten. Lisätietoja on Business Centralin kehittäjien ja IT-ammattilaisten ohjeen kohdassa [Visual Studio Coden virheenkorjaus suoraan WWW-asiakasohjelmassa](/dynamics365/business-central/dev-itpro/developer/devenv-troubleshoot-vscode-webclient).

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]

## Sivun tarkastuksen käyttäminen

Sivun tarkistus aloitetaan **Ohje ja tuki** -sivulla. Valitse ensin kysymysmerkki oikeassa yläkulmassa, sitten **Ohje ja tuki** ja lopuksi **Tarkasta sivut ja tiedot**. Vaihtoehtoisesti voit käyttää näppäinyhdistelmää <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>F1</kbd>.

**Sivun tarkastus** -ruutu avautuu sivulle. Kun ruutu avautuu ensimmäisen kerran, siinä pääsivukohteeseen liittyviä tietoja.

Siirrä kohdistus näppäimillä tai osoitinlaitteella sivun eri elementteihin. Kun valitset pääsivulla tietoruudun tai osan, raja korostaa täsmällisen alueen ja **Sivun tarkastus** -ruudussa on tietoja valitusta elementistä. Esimerkiksi edellisessä kuvassa on tietoja **Myyntitilaus**-sivun luettelo-osasta. Kun siirryt sovelluksessa muille sivulle, **Sivun tarkastus** -ruutu päivittyy automaattisesti sen sivun tiedoilla, johon olet siirtynyt.

Lisätietoja sivun tarkastuksessa näytettävistä tiedoista on Business Centralin kehittäjien IT-ammattilaisten ohjeen kohdassa [Sivun tarkastaminen ja vianmääritys](/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages).

Jos odottamasi tiedot eivät näy **Sivun tarkastus** -ruudussa, käyttöoikeutesi eivät luultavasti ole riittävät. Tätä käsitellään seuraavassa osassa.

## Sivun tarkastustietojen käyttöoikeuksien hallinta

Voit hallita järjestelmänvalvojana **Sivun tarkastus** -ruudussa näytettävien tietojen käyttöoikeuksia määrittämällä käyttäjien käyttöoikeudet. Voit antaa käyttäjälle kaikkien tietojen käyttöoikeudet antamalla hänelle **Toteuta**-käyttöoikeus **Järjestelmä**-kohteessa **5330**. Voit myöntää tämän käyttöoikeuden käyttämällä käyttöoikeuksien joukkoa (kuten **D365-vianmääritys**) tai käyttäjäryhmää (kuten **D365-vianmääritys**). Lisätietoja käyttöoikeuksista on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).

Käyttäjät, joilla ei ole myönnetty käyttöoikeuksia **järjestelmäkohteessa 5330**, voivat silti käyttää **Sivun tarkastus** -ruutua. He näkevät kuitenkin vain **Sivu**- ja **Taulukko**-kentät. Käyttäjät voivat sitten välittää näiden kenttien perustiedot tukitiimilleen.

## Katso myös

[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
