---
title: Nimikkeen tekoälypohjaisen markkinointitekstin (esiversio) määrittäminen Copilotin avulla
description: 'Tässä artikkelissa kerrotaan, miten voit hankkia Business Centralin Copilot-kokeiluversion ja ottaa Copilot-ympäristön käyttöön'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/22/2023
ms.custom: bap-template
---

# <a name="configure-ai-powered-item-marketing-text-preview-with-copilot" />Nimikkeen tekoälypohjaisen markkinointitekstin (esiversio) määrittäminen Copilotin avulla

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Tässä artikkelissa kerrotaan, miten voit hallita mahdollisuutta luoda tekoälypohjaisen nimikkeen markkinointitekstin Copilotilla organisaatiollesi. Tehtävän suorittaa järjestelmänvalvoja. On olemassa kaksi vaatimusta, jotka sinun on täytettävä, jotta ominaisuus olisi käyttäjien käytettävissä:

- Ota käyttöön **Luo tekoälypohjaisia tuotekuvauksia Copilotin avulla** -ominaisuus.
- Hyväksy [Esiversion](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) ehdot ja [Microsoftin tietosuojalauseke](https://go.microsoft.com/fwlink/?LinkId=521839) organisaation puolesta.

Jos jompikumpi näistä vaatimuksista ei täyty, ominaisuus ei ole käytettävissä.

## <a name="prerequisites" />Vaatimukset

Käytössäsi on Copilot-käyttöön otettu Business Centralin [esiversio](ai-preview-getstarted.md). Copilot käyttöönoton tekee ylläpitäjä. Lisätietoja on kohdassa [Määritä nimikkeiden tekoälypohjaisten markkinointitekstien luominen Copilotilla](enable-ai.md).

## <a name="enable-or-disable-create-ai-powered-product-descriptions-with-copilot" />Ota käyttöön tai poista käytöstä Luo tekoälypohjaisia tuotekuvauksia Copilotin avulla -ominaisuus

1. Etsi ja avaa **toimintojen hallinta** -sivu Business Centralissa.
2. Määritä **Käytössä kohteelle** -sarakkeen **Ominaisuuksien esikatselu: Luo tekoälyllä toimivia tuotekuvauksia Copilot-ominaisuuden avulla** -sarakkeeksi **Kaikki käyttäjät**, jos haluat ottaa ominaisuuden käyttöön, tai **Ei mitään**, jos haluat poistaa sen käytöstä.

   Saat lisätietoja ominaisuuksien hallinnasta yleisesti siirtymällä [Ominaisuuksien hallintaan](/dynamics365/business-central/dev-itpro/administration/feature-management).

## <a name="consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users" />Kaikkien käyttäjien esiversion ja tietosuojaehtojen hyväksyminen tai hylkääminen

1. Etsi ja avaa Business Centralissa **tietosuojatietojen tila** -sivu.
2. Valitse **integrointinimi**-sarakkeessa **Azure openAI** ja lue sitten sinulle esitettävät käyttöehdot.
3. Valitse **Azure OpenAI** -rivillä **hyväksy kaikille** -valintaruutu, jos haluat hyväksyä tai **hylätä kaikille** valintaruudun valinnan.

## <a name="next-steps" />Seuraavat vaiheet

Kun olet ottanut ominaisuuden käyttöön ja hyväksynyt sen, voit kokeilla Copilotia Business Centralin nimikkeille. Siirry kohtaan [Markkinointitekstin lisääminen nimikkeille](item-marketing-text.md).  

## <a name="see-also" />Katso myös

[Tekoälypohjainen tuotteen markkinointiteksti Copilotin avulla -yleiskatsaus](ai-overview.md)  
[Luo markkinointiteksti nimikkeille käyttämällä Copilotia](item-marketing-text.md)  
[Nimikkeen tekoälypohjainen markkinointiteksti Copilotin avulla - UKK](ai-faq.md)  
