---
title: Pankkitilien määrittäminen (sisältää videon)
description: Tietoja pankkitilien käytöstä Business Centralissa ja summien täsmäyttämisestä pankin kanssa.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.search.form: 370, 371, 372, 373, 375, 423, 424, 425, 426, 1240, 1280
ms.date: 01/24/2022
ms.author: edupont
ms.openlocfilehash: 49ddd48a03c8abe9ea9b396bebc4328e2be30104
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8143736"
---
# <a name="set-up-bank-accounts"></a>Pankkitilien määrittäminen

[!INCLUDE[prod_short](includes/prod_short.md)] seuraa pankkitapahtumia pankkitilien avulla. Tilit voidaan määrittää käyttämään paikallista valuuttaa tai ulkomaan valuuttaa. Kun olet määrittänyt pankkitilit, voit myös käyttää Sekin tulostus -vaihtoehtoa. Pankkitilit sisältävät lisätoimintoja maksujen [täsmäytystä](receivables-apply-payments-auto-reconcile-bank-accounts.md), [pankkitäsmäytystä](bank-how-reconcile-bank-accounts-separately.md) sekä pankkitiedostojen tuontia ja vientiä varten. Pankkitilit voidaan sisällyttää myös yleisten päiväkirjojen tapahtumiin. Kukin pankkitili linkitetään tilikartassa olevaan tiliin määritetyn pankkitilin kirjausryhmän kautta. Pankkitilin käyttö maksutapahtumassa luo automaattisesti tapahtuman sekä pankkitilille että yhdistetylle KP-tilille.  

Pankkitilit toimivat eri tavalla sen mukaan, onko valuuttakoodi määritetty:

- Valuuttakoodi on tyhjä

  Kaikki pankkitilin tapahtumat ovat nykyisen yrityksen paikallisena valuuttana (PVA). Jos tilille tehdään tapahtuma toisena valuuttana, summat kirjataan tilille PVA:na asianmukaisen valuutan vaihtokurssin perusteella. Kaikki tältä tililtä myönnetyt sekit on annettava PVA:na. Jos pankkitiliä käytetään kirjauskansiossa, päiväkirjan rivi perii automaattisesti tyhjän valuuttakoodin.  
- Valuuttakoodi on määritetty

  Kaikkien tälle tilille tehtyjen tapahtumien on oltava siinä valuutassa, joka tilillä on määritetty. Kaikilla tältä tililtä annetuilla sekeillä on myös oltava tämä valuutta.  

Pankkitili on integroitu [!INCLUDE[prod_short](includes/prod_short.md)] -osa ja sillä on rooli monissa muissa ominaisuuksissa. Seuraavassa kuvassa näkyvät tärkeimmät suhteet:

![Kuva pankkitilien suhteista.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

Tämä tarkoittaa, että pankkitilin luominen asettaa sen saataville kaikissa yllä mainituissa paikoissa. Lisäksi se peilataan asiaankuuluvalle KP-tilille ja **Yrityksen tiedot** -sivulle.

Pankkitiliä seurataan yleensä päivittäin, jotta mahdolliset uudet maksut asiakkailta rekisteröidään mahdollisimman nopeasti. Tämä auttaa varmistamaan, että [!INCLUDE[prod_short](includes/prod_short.md)] näyttää asiakkaiden todellisen tilan, jotta myyjät, kirjanpitäjät ja muut työntekijät voivat käyttää asiaankuuluvia ja ajan tasalla olevia tietoja. Näin he välttävät tarpeettomat puhelut asiakkaalle erääntyneistä laskuista tai lähetysten viivästymisestä.  

![Kuva pankkimaksusta.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

Toinen tehtävä on tuoda toimittajan valuuttamaksut ja toteutuneet valuuttakurssit, jotta varmistetaan, että toimittajien todellinen tila on ajan tasalla. Helpoin tapa varmistaa, että pankkitili päivitetään, on käyttää [maksun täsmäytysominaisuutta](receivables-apply-payments-auto-reconcile-bank-accounts.md). **Maksujen täsmäytyskirjauskansiossa** voit tuoda pankkitapahtumia suoraan verkkopankkisovelluksesta ja kirjata ne enemmän tai vähemmän automaattisesti. Päiväkirja tunnistaa ja kirjaa automaattisesti seuraavaa:  

- Suoraveloitusmaksut asiakkailta  
- Asiakasmaksut yksittäisistä laskuista  
- Kokonaissummamaksut asiakkailta  
- Asiakasmaksut ulkomaan valuutoissa  
- Toimittajamaksut  
- Toimittajamaksut ulkomaan valuutoissa  
- Toistuvat toimittajamaksut ja tilaukset  
- Pankkikulut ja -korot  

Maksujen täsmäytys säästää valtavasti aikaa saapuvien ja lähtevien maksujen kirjaamisessa. Pankkitilin tapahtumia [!INCLUDE[prod_short](includes/prod_short.md)]issa ei kuitenkaan pidetä 100-prosenttisen oikeina, ennen kuin suoritat pankkitäsmäytyksen.  

Pankkitäsmäytyksellä varmistat, että pankkitili [!INCLUDE[prod_short](includes/prod_short.md)]issa vastaa pankin ulkoista tiliä.  

 ![Kuva pankkitilien täsmäytyksestä.](media/Set-Up-Bank-Accounts/BankReconciliation.png)

Yllä olevassa kuvassa vasen puoli edustaa pankkitiliä [!INCLUDE[prod_short](includes/prod_short.md)]issa ja oikea puoli edustaa pankista verkkopankkisovelluksen kautta tuotuja tapahtumia. Keskellä olevassa kaaviossa näkyvät tapahtumat molemmilta puolilta, eli pankkitäsmäytys.

[!INCLUDE[prod_short](includes/prod_short.md)] -pankkitilin useimpien tapahtumien tulisi olla fyysisen pankin tiedossa. Poikkeuksiin kuuluvat seuraavat tapaukset:  

- [!INCLUDE[prod_short](includes/prod_short.md)]iin kirjatut korjaukset  
- Myönnetyt sekit, joita ei ole vielä lunastettu  
- Toimittajan maksut, joita pankki ei ole hyväksynyt  

Pankin fyysisen tililn tuntemattomat tapahtumat, joita ei ole tunnistettu maksujen täsmäytyskirjauskansiossa, kuten seuraavat:  

- Uudet toimittajatilaukset  
- Asiakasmaksut ilman kuvausta
- Pankin korot
- Pankkikulut
- Luottokorttimaksut, joita ei ole vielä ilmoitettu

Mitä parempia yhdistämistietoja teet maksujen täsmäytyskirjauskansiossa, sitä enemmän tapahtumia kirjataan automaattisesti ja sitä helpompaa kausittainen pankkitäsmäytys on.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

<br><br>

> [!WARNING]
> Jotkin kentät voivat sisältää luottamuksellisia tietoja, kuten kentät **Pankkikonttorin nro**, **Pankkitilin numero**, **SWIFT-koodi** ja **IBAN-koodi**. Lisätietoja on kohdassa [Herkkien kenttien valvonta](across-log-changes.md#monitoring-sensitive-fields).

## <a name="to-set-up-bank-accounts"></a>Pankkitilien määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten vastaava linkki.
2. Valitse **Pankkitilit**-sivulla **Uusi**-toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Esimerkiksi **Pankkitilin kirjausryhmä** -kenttä yhdistää pankkitilin taseen taustalla olevaan KP-tiliin. Lisätietoja on kohdassa [Kirjausryhmien määrittäminen](finance-posting-groups.md).

> [!TIP]
> Jotkin kentät on piilotettu, kunnes valitset **Näytä lisää** -toiminnon, koska niitä käytetään harvoin. Toiset on lisättävä mukauttamisen avulla. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

Voit luoda yrityksellesi niin monta pankkitiliä kuin tarvitset. Kullekin pankkitilille on määritettävä tiedot, jotka tekevät pankkitilistä yksilöllisesti tunnistettavan. Nämä tiedot sisältävät pankin maantieteellisen osoitteen, erityyppisten tapahtumien numerosarjat (kuten suoraveloitukset ja tilisiirrot), valuutan, jossa arvot määritetään sekä tiedot, joita käytetään tiliotteiden tuomiseen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
<!--
The following table explains key fields.

|Field|Description|  
|---------------------------------|---------------------------------------|  
|**General FastTab**||
|No.|Specifies the number of the bank account, according to the specified number series. If the number series allow manual numbering, any alphanumeric code up to 20 characters can be used.|
|Name|The Name of the bank holding the bank account.|
|Bank Branch No.|The Bank Branch No. is usually used to identify the bank branch in domestic payments. The Bank Branch No. is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Account No.|Bank Account No. is usually used to identify the bank account no. in domestic payments. The Bank Account No. is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Balance|Shows the Balance of the bank account in the account currency.|
|Balance (LCY)|Shows the Balance of the bank account in the local currency (LCY).|
|Our Contact Code|Specifies a code to specify the employee who is responsible for this bank account. The employee must be created in the **Salesperson/Purchaser** table.|
|Blocked|Specifies that the related record is blocked from being posted in transactions, for example the account is obsolete after a bank change.|
|SEPA Direct Debit Exp. Format|Specifies the SEPA format of the bank file that will be exported when you choose the **Create Direct Debit File** button in the **Direct Debit Collect. Entries** window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Credit Transfer Msg. Nos.|Specifies the number series for bank instruction messages that are created with the export file that you create from the Direct Debit Collect. Entries window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Direct Debit Msg. Nos.|Specifies the number series that will be used on the direct debit file that you export for a direct-debit collection entry in the Direct Debit Collect. Entries window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Creditor No.|Specifies your company as the creditor in connection with payment collection from customers using SEPA Direct Debit. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Bank Clearing Standard|The national bank names register used for the sender bank account.|
|Bank Clearing Code|Specifies the code for bank clearing that is required according to the format standard that you selected in the Bank Clearing Standard field. The bank clearing code can be used as an alternative to SWIFT and IBAN to identify your bank as sender of a bank transfer.|
|Last Date Modified|Date of the latest modification of the bank account.|
|**Payment Matching**||
|Disable Automatic Payment Matching|Specifies whether to disable automatic payment matching after importing bank transactions for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Payment Match Tolerance**||
|Match Tolerance Type|Specifies by which tolerance the automatic payment application function will apply the Amount Incl. Tolerance Matched rule for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Match Tolerance Value|Specifies if the automatic payment application function will apply the Amount Incl. Tolerance Matched rule by Percentage or Amount. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Hidden Fields**||
|Search Name|Specifies an alternate name that you can use to search for the record in question when you cannot remember the value in the Name field.|
|Min. Balance|Specifies a minimum balance for the bank account. This field is for information purposes only.|
|Positive Pay Export Code|Specifies a code for the data exchange definition that manages the export of positive-pay files. Read more in [Export Positive Pay Files](finance-how-positive-pay.md).|
|**Communication FastTab**||
|Address|The address of the bank branch.|
|Address 2|An additional address field for the bank branch.|
|Post Code|The post code of the bank branch.|
|City|The city of the bank branch.|
|Country/Region Code|The Country/Region Code of the bank branch.|
|Phone No.|The Phone No. of the bank branch.|
|Mobile Phone No.|The Mobile Phone No. of the bank branch.|
|Contact|The main contact in the bank branch. Additional contacts can be created in the Contacts module.|
|Fax No.|The Fax No. of the bank branch.|
|Email|The Email of the bank branch.|
|Home Page|The Home Page of the bank branch.|
|**Posting FastTab**||
|Currency Code|Specifies the relevant currency code for the bank account. Applying a currency code to a bank account will limit all transactions to only use the applied currency code. Leaving the currency code blank will allow transactions in all currencies, however, the amount will be converted to the local currency (LCY) using the applied currency rate. Checks issued from this account will also follow the same rules.|
|Last Check No.|The number of the latest check issued from this account.|
|Transit No.|Specifies a bank identification number of your own choice.|
|Last Statement No.|The number of the latest bank reconciliation posted to this account. Read more in [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Last Payment Statement No.|The number of the latest payment reconciliation posted to this account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Last Bank Statement|The ending-balance of the last bank statement. Read more in [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Bank Acc. Posting Group|Specifies a code for the bank account posting group for the bank account. The Bank Acc. Posting Group connects the bank account to the G/L Account in the balance sheet.|
|**Transfer**||
|Transit No.|Specifies a bank identification number of your own choice.|
|SWIFT Code|Specifies the international bank identifier code (SWIFT) of the bank where you have the account. The SWIFT Code is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|IBAN|Specifies the bank account's international bank account number. The IBAN Code is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Statement Import Format|Specifies the format of the bank statement file that can be imported into this bank account. The format is being used in both the payment reconciliation journals and the bank account reconciliations.|
|Payment Export Format|Specifies the format of the bank file that will be exported when you choose the Export Payments to File button in the Payment Journal window.|
-->
> [!NOTE]
> Voit täyttää **Saldo**-kenttään alkusaldo, kun pankkitilitapahtuma ja kyseinen summa on kirjattu. Voit tehdä tämän suorittamalla pankkitilin täsmäytyksen. Lisätietoja on kohdassa [Pankkitilien täsmäyttäminen](bank-how-reconcile-bank-accounts-separately.md).  
>
> Vaihtoehtoisesti voit ottaa käyttöön alkusaldon osana yleistietojen luontia uusissa yrityksissä käyttämällä ohjattua **Siirrä yritystiedot** -asetusten määritystä. Lisätietoja on ohjeaiheessa [Valmistautuminen liiketoimintaan](ui-get-ready-business.md).  

> [!IMPORTANT]
> On tärkeää, että et kirjaa alkusaldoa suoraan pääkirjanpitoon. Jos KP-tilin kirjauksia kirjataan suoraan KP-tiliin, tuloksena on yleensä se, että et voi täsmäyttää pankkitiliä tai, jos kyseessä on ulkomaan valuutan pankkitili, tuloksena on eroja, jotka kertyvät ylimääräisiä pankkitäsmäytyksiä kirjatessa. Usein pankin avaussaldo kirjataan suoraan pankkitilille, ja summa päätyy KP-tiliin. Voit vaihtoehtoisesti kumota sen myöhemmin sellaisen nimetyn KP-tilin osalta, jota olet käyttänyt pääkirjanpidon avaussaldon tasapainottamista varten. Molemmissa tapauksissa sinun on tasapainotettava mahdolliset suorat kirjaukset KP-tiliin ennen ensimmäisen pankkitäsmäytyksen aloittamista ja erityisesti silloin, kun pankkitili käyttää ulkomaan valuuttaa.  

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Pankkitilin määrittäminen pankkitiedostojen tuontia tai vientiä varten

**Pankkitilin kortti** -sivun **Siirto**-pikavälilehden kentät liittyvät pankkisyötteiden ja -tiedostojen tuontiin ja vientiin. Lisätietoja on kohdissa [AMC Banking 365 Fundamentals -laajennuksen käyttäminen](ui-extensions-amc-banking.md) ja [Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten vastaava linkki.
2. Avaa sen pankkitilin kortti, josta viet tai johon tuot pankkitiedostot.
3. Täytä **Siirto**-pikavälilehdessä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Eri tiedostojen vientipalvelut ja niiden tiedostomuodot edellyttävät erilaisia asetuksia **Pankkitilin kortti** -sivulla. Saat ilmoituksen virheellisistä tai puuttuvista asetusarvoista, kun yrität viedä tiedoston. Lue huolellisesti kenttien lyhyet kuvaukset tai katso lisätietoja liittyvien toimenpiteiden ohjeaiheista. Esimerkiksi maksutiedoston vienti pohjoisamerikkalaiseen sähköiseen rahansiirtoon (EFT-toiminto) edellyttää, että sekä **Viimeinen maksuosoitusehdotusnumero**- että **Siirtonro**-kenttä on täytetty. Lisätietoja on kohdassa [Maksujen vieminen pankkitiedostoon](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Pankkitilin **Siirto**-pikavälivälilehden kentät palvelevat eri tarkoituksia sen mukaan, onko maksu saapuva vai lähtevä.

Kuvassa on saapuvien maksujen reitti:

:::row:::
    :::column:::
        1. Tapahtumat viedään pankkitililtä joko ihmisen luettavissa olevassa .csv-muodossa tai pankin omassa muodossa.
        <br><br>
2. *Tiedonsiirtomääritys* yhdistää tiedoston tiedot kenttiin [!INCLUDE[prod_short](includes/prod_short.md)]issa. Lisätietoja on kohdassa [Tietojenvaihdon määrittäminen](across-set-up-data-exchange.md).
<br><br>
3. *Tietojen vienti- ja tuontiasetukset* määrittävät viennin tai tuonnin, ja ne linkittyvät tiedonsiirtomääritykseen.
<br><br>
4. *Tiliotteiden tuontimuoto* linkittää tuontiasetukset pankkitiliin.
<br><br>
5. Maksut tuodaan joko **maksujen täsmäytyskirjauskansio**- tai **pankkitilin täsmäytys** -sivun kautta.
    :::column-end:::
    :::column:::
        ![Kuva pankista pankkitileille saaduista maksuista.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)
    :::column-end:::
:::row-end:::

Saapuvat maksut tuodaan aina **maksujen täsmäytyskirjauskansio** -sivun kautta tai suoraan **pankkitilin täsmäytys** -sivulle. Sitä vastoin lähtevät maksut voivat olla peräisin mistä tahansa maksupäiväkirjasta. Ainoa edellytys on, että **Salli maksun vienti** -kenttä on valittuna asiaankuuluvassa maksupäiväkirjaerässä.

Kuvassa on lähtevien maksujen reitti:

:::row:::
    :::column:::
        6. Tapahtumat, jotka on täytetty maksupäiväkirjaan, joka on valmisteltu maksujen tiedostoon viemistä varten.
        <br><br>
        7. *Tiliotteiden tuontimuoto* linkittää tuontiasetukset pankkitiliin
        <br><br>
        8. *Tietojen vienti- ja tuontiasetukset* määrittävät viennin tai tuonnin, ja ne linkittyvät tiedonsiirtomääritykseen.
        <br><br>
        9. *Tiedonsiirtomääritys* yhdistää tiedoston tiedot kenttiin [!INCLUDE[prod_short](includes/prod_short.md)]issa. Lisätietoja on kohdassa [Tietojenvaihdon määrittäminen](across-set-up-data-exchange.md).
        <br><br>
        10. Maksut viedään maksupäiväkirjasta ja tuodaan pankkitilille
    :::column-end:::
    :::column:::
        ![Kuva pankkitileiltä tehdyistä maksuista, jotka on lähetetty pankille.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)
    :::column-end:::
:::row-end:::

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Toimittajan pankkitilien määrittäminen pankkitiedostojen vientiä varten

**Toimittajan pankkitilin kortti** -sivun **Siirto**-pikavälilehden kentät liittyvät pankkisyötteiden ja -tiedostojen vientiin. [Lisätietoja on kohdassa AMC Banking 365 Fundamentals -laajennuksen käyttäminen](ui-extensions-amc-banking.md) ja [Maksujen vieminen pankkitiedostoon](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajat** ja valitse sitten vastaava linkki.
2. Avaa sen toimittajan kortti, jonka pankkitiliin viet maksujen pankkitiedostot.
3. Valitse **Pankkitilit**-toiminto.
4. Valitse **Toimittajan pankkitili** -luettelossa pankkitili tai lisää uusi pankkitili.  
5. Täytä tarvittaessa **Toimittajan pankkitilin kortti** -sivun **Siirto**-pikavälilehden kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!WARNING]
> Jotkin toimittajan pankkitilin kentät sisältävät luottamuksellisia tietoja, kuten kentät **Pankkikonttorin nro**, **Pankkitilin numero**, **SWIFT-koodi** ja **IBAN-koodi**. Lisätietoja on kohdassa [Herkkien kenttien valvonta](across-log-changes.md#monitoring-sensitive-fields).

## <a name="changing-your-bank-account"></a>Pankkitilin vaihtaminen

Jos haluat käyttää yrityksessäsi toista pankkitiliä, sinun on luotava uusi pankkitili [!INCLUDE[prod_short](includes/prod_short.md)]issa. Suosittelemme, ettet vain korvaa tällä hetkellä käyttämäsi tilin tietoja, koska se voi aiheuttaa virheellisiä tietoja. Esimerkiksi avaussaldosi voi olla virheellinen tai pankkisyöte saattaa lakata toimimasta oikein. On tärkeää, että pidät nykyiset ja uudet tilit erillään.

Kun olet luonut uuden pankkitilin, luo myös uusi pankin kirjausryhmä ja määritä se uudelle pääkirjanpitotilille. Voit käyttää aiemmin luotua pankin kirjausryhmää uudelleen, ja pankkitapahtumat kirjataan samoille pääkirjanpitotileille kuin tapahtumat muilta pankkitileiltä, jotka jakavat pankin kirjausryhmän. Suosittelemme kuitenkin, että luot uuden pankin kirjausryhmän ja pääkirjanpitotilin, jotta täsmäytys on helpompaa.

> [!NOTE]
> Muista, että avointen myyntilaskujen pankkitilitiedot näkyvät edelleen alkuperäisellä pankkitilillä. Näin ollen maksut todennäköisesti kirjataan edelleen kyseiselle tilille. Suosittelemme, että pidät molemmat tilit aktiivisina jonkin aikaa muutoksen jälkeen.

Jos haluat tarkastella käteistilejäsi tarkemmin taloudellisessa raportoinnissa, käytä **Alkusumma**- ja **Loppusumma**-tilejä tilikartassasi, **Summausväli**-rivejä KP-raporttimalleissa tai KP-tililuokkia. Lisätietoja on osassa [Liiketoimintatiedot ja Financial Reporting](bi.md).

## <a name="see-also"></a>Katso myös

[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Kirjausryhmien määrittäminen](finance-posting-groups.md)  
[Pankkitilien täsmäytys](bank-manage-bank-accounts.md)  
[Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md)  
[SEPA-suoraveloitus Business Centralissa](finance-collect-payments-with-sepa-direct-debit.md)  
[Pankkitilin määrittäminen SEPA-suoraveloitusta varten](finance-collect-payments-with-sepa-direct-debit.md#to-set-up-your-bank-account-for-sepa-direct-debit)  
[Pankkitilin määrittäminen SEPA-hyvityksen siirtoa varten](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-set-up-a-bank-account-for-sepa-credit-transfer)  
[Maksujen suorittaminen AMC Banking 365 Fundamentals -laajennuksen tai SEPA-tilisiirron avulla](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Maksun täsmäytys](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Pääkirjanpito ja aitoustodistus](finance-general-ledger.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
