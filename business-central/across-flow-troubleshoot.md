---
title: Automaattisten työnkulkujen vianmääritys
description: 'Opettele tekemään vianmääritys Business Centralin ja Power Automaten väliselle yhteydelle, kun rakennat automaattista työnkulkua.'
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions, Power Automate,'
ms.date: 12/13/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
---

# <a name="troubleshoot-your--automated-workflows"></a>[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman automaattisten työnkulkujen vianmääritys

Kun muodostat yhteyden [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan Power Automaten avulla automaattisten työnkulkujen luomiseksi, saatat törmätä virheviesteihin. Tässä artikkelissa on ratkaisuehdotuksia usein toistuviin ongelmiin.

## <a name="flow-doesnt-run-on-all-records-created-or-changed"></a>Työnkulku ei toimi kaikissa luoduissa tai muuttuvissa tietueissa

### <a name="problem"></a>Ongelma

Jos tapahtuma luo tai muuttaa useita tietueita, työnkulkua ei suoriteta joissakin tai kaikissa tietueissa.

### <a name="possible-cause"></a>Mahdollinen syy

Tällä hetkellä työnkulun käsittelemien tietueiden määrä on rajoitettu. Jos 30 sekunnin kuluessa luodaan tai muutetaan yli 1000 tietuetta, työnkulkua ei käynnistetä.

> [!NOTE]
> Kehittäjien osalta työnkulun käynnistys tehdään webhook-ilmoitusten avulla, ja tämä rajoitus johtuu tavasta, jolla Business Central -yhdistin käsittelee `collection`-ilmoituksia. Lisätietoja on kehittäjän ja järjestelmänvalvojan ohjeen kohdassa [Webhookien käyttö Dynamics 365 Business Centralissa](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows).

## <a name="the-response-from-the-business-central-service-is-too-large-error"></a>"Business Central -palvelun vastaus on liian suuri" -virhe

### <a name="problem-1"></a>Ongelma

Kun käytät tietueiden kanssa vuorovaikutuksessa olevaa toimintoa (kuten *Luo tietue (v3)* ja *Hae tietue (v3)*), Power Automate -näyttöön saattaa tulla tämän kaltainen virhe:

`The response from the Business Central service is too large`

### <a name="possible-cause-1"></a>Mahdollinen syy

Vaikka Business Central ei ole määrittänyt ohjelmointirajapintojen palauttamien tietueiden kokoa, Power Automaten Dynamics 365 Business Central -yhdistin voi käsitellä vain enintään 8 Mt:n tietueita.

Kaikki Microsoftin tarjoamat Business Centralin sovellusliittymät palauttavat tietueita tämän rajan puitteissa, mutta kumppanien tarjoamat sovellusliittymät eivät välttämättä. Jos näet virheen "Business Central -palvelun vastaus on liian suuri", ota yhteyttä käyttämäsi API-liittymän luoneeseen kumppaniin.

## <a name="entity-set-not-found-error"></a>"Entiteettijoukkoa ei löydy" -virhe

### <a name="problem-2"></a>Ongelma

Kun luot uuden Power Automate -työnkulun [!INCLUDE[prod_short](includes/prod_short.md)] -hyväksymiskäynnistimen avulla, esimerkiksi *Kun ostoasiakirjan hyväksyntää pyydetään*, näyttöön voi tulla tämän kaltainen virhesanoma:

`Entity set not found: \<name\>`

Paikkamerkki `\<name\>` on puuttuvan Web-palvelun palvelun nimi, kuten *workflowWebhookSubscriptions* tai *workflowPurchaseDocumentLines*.

### <a name="possible-cause-2"></a>Mahdollinen syy

Power Automaten käyttäminen hyväksyntiin edellyttää, että tietyt sivu- ja codeunit-objektit julkaistaan Web-palveluina. Oletusarvon mukaan useimmat tarvittavista objekteista julkaistaan Web-palveluina. Joissakin tapauksissa ympäristösi on ehkä mukautettu siten, että näitä objekteja ei enää julkaista.

### <a name="fix"></a>Korjaa

Siirry **Verkkopalvelut**-sivulle ja varmista, että seuraavat objektit on julkaistu Web-palveluina. Kaikille objekteille tulisi olla merkintä luettelossa , ja **Julkaistu**-valintaruutu valittuna.  

| Objektityyppi | Objektin tunnus | Objektin nimi | Palvelun nimi |
|--|--|--|--|
| Codeunit | 1544 | WorkflowWebhookSubscription | WorkflowActionResponse |
| Sivu | 6408 | workflowCustomers | workflowCustomers |
| Sivu | 6406 | workflowGenJournalBatches | workflowGenJournalBatches |
| Sivu | 6407 | workflowGenJournalLines | workflowGenJournalLines |
| Sivu | 6409 | workflowItems | workflowItems |
| Sivu | 6405 | Ostoasiakirjarivin entiteetti | workflowPurchaseDocumentLines |
| Sivu | 6404 | workflowPurchaseDocuments | workflowPurchaseDocuments |
| Sivu | 6403 | Myyntiasiakirjarivin entiteetti | workflowSalesDocumentLines |
| Sivu | 6402 | workflowSalesDocuments | workflowSalesDocuments |
| Sivu | 6410 | workflowVendors | workflowVendors |
| Sivu | 831 | workflowWebhookSubscriptions | workflowWebhookSubscriptions |

> [!NOTE]
> **Palvelun nimi** -arvon täytyy olla täsmälleen sama kuin taulukossa on esitetty. Älä muuta tai käännä palvelun nimeä.

Lue lisää verkkopalvelujen julkaisemisesta kohdasta [Verkkopalvelun julkaiseminen](across-how-publish-web-service.md).

## <a name="see-also"></a>Katso myös

[[!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen käyttäminen Power Automate -työnkuluissa](across-how-use-financials-data-source-flow.md)  
[Työnkulku](across-workflow.md)  
[Automaattisten työnkulkujen määrittäminen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Ota pikatyönkulut käyttöön](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  
[Power Automate -työnkulkujen hallinta](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
