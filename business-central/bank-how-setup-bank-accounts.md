---
title: Pankkitilien määrittäminen (sisältää videon)
description: Tietoja pankkitilien käytöstä Business Centralissa ja summien täsmäyttämisestä pankin kanssa.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'Yodlee, feed, stream'
ms.search.form: '370, 371, 372, 373, 375, 423, 424, 425, 426, 1240, 1280'
ms.date: 08/03/2023
ms.custom: bap-template
---
# <a name="set-up-bank-accounts"></a>Pankkitilien määrittäminen

[!INCLUDE[prod_short](includes/prod_short.md)] seuraa pankkitapahtumia pankkitilien avulla. Tilit voidaan määrittää käyttämään paikallista valuuttaa tai ulkomaan valuuttaa. Kun olet määrittänyt pankkitilit, voit myös käyttää Sekin tulostus -vaihtoehtoa. Pankkitilit sisältävät lisätoimintoja maksujen [täsmäytystä](receivables-apply-payments-auto-reconcile-bank-accounts.md), [pankkitäsmäytystä](bank-how-reconcile-bank-accounts-separately.md) sekä pankkitiedostojen tuontia ja vientiä varten. Pankkitilit voidaan sisällyttää myös yleisten päiväkirjojen tapahtumiin. Kukin pankkitili linkitetään tilikartassa olevaan tiliin määritetyn pankkitilin kirjausryhmän kautta. Pankkitilin käyttö maksutapahtumassa luo automaattisesti tapahtuman sekä pankkitilille että yhdistetylle pääkirjanpitotilille (KP).  

Pankkitilit toimivat eri tavalla sen mukaan, onko valuuttakoodi määritetty:

- Jos valuuttakoodi on tyhjä

  Kaikki pankkitilin tapahtumat ovat nykyisen yrityksen paikallisena valuuttana (PVA). Jos tilille tehdään tapahtuma toisena valuuttana, summat kirjataan tilille PVA:na asianmukaisen valuutan vaihtokurssin perusteella. Kaikki tältä tililtä myönnetyt sekit on annettava PVA:na. Jos pankkitiliä käytetään kirjauskansiossa, päiväkirjan rivi perii automaattisesti tyhjän valuuttakoodin.  
  
- Valuuttakoodi on määritetty

  Kaikkien tälle tilille tehtyjen tapahtumien ja siltä tehtyjen shekkien on oltava siinä valuutassa, joka tilillä on määritetty.

Voit säästää tietojen syöttämiseen käytettävän ajan tekemällä pankkitilistä tilille määritetyn valuutan oletustilin. Jos teet näin, tili liitetään myynti- ja huoltoasiakirjoihin, jotka käyttävät valuuttaa. Kun haluat tehdä tilistä myynti- ja huoltoasiakirjojen oletustilin, Ota **Pankkitilin kortti** -sivulla käyttöön **Käytä oletusvaluuttana** -valitsin. Voit tarvittaessa valita eri tilin, kun käsittelet asiakirjaa.

Pankkitili on oleellinen osa [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaa ja sillä on rooli monissa muissa ominaisuuksissa. Seuraavassa kuvassa näkyvät tärkeimmät suhteet:

![Kuva pankkitilien suhteista.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

Tämä tarkoittaa, että pankkitilin luominen asettaa sen saataville kaikissa yllä mainituissa paikoissa. Lisäksi se peilataan asiaankuuluvalle KP-tilille ja **Yrityksen tiedot** -sivulle.

Pankkitiliä seurataan yleensä päivittäin, jotta mahdolliset uudet maksut asiakkailta rekisteröidään mahdollisimman nopeasti. Tämä auttaa varmistamaan, että asiakkaan todellinen tila näkyy [!INCLUDE[prod_short](includes/prod_short.md)] -kentässä. Tämän ansiosta myyjät, kirjanpitäjät ja muut työntekijät voivat käyttää asianmukaisimpia ja ajan tasalla olevia tietoja, jolloin he eivät tee tarpeettomia puheluja asiakkaalle erääntyneistä laskuista tai toimitusten viivästyksistä.  

![Kuva pankkimaksusta.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

Toinen tehtävä on tuoda toimittajan valuuttamaksut ja toteutuneet valuuttakurssit, jotta varmistetaan, että toimittajien todellinen tila on ajan tasalla. [Maksun täsmäytys](receivables-apply-payments-auto-reconcile-bank-accounts.md) -toiminto on helpoin tapa tehdä se. **Maksujen täsmäytyskirjauskansiossa** voit tuoda pankkitapahtumia suoraan verkkopankkisovelluksesta ja kirjata ne enemmän tai vähemmän automaattisesti. Päiväkirja tunnistaa ja kirjaa automaattisesti seuraavaa:  

- Suoraveloitusmaksut asiakkailta  
- Asiakasmaksut yksittäisistä laskuista  
- Kokonaissummamaksut asiakkailta  
- Asiakasmaksut ulkomaan valuutoissa  
- Toimittajamaksut  
- Toimittajamaksut ulkomaan valuutoissa  
- Toistuvat toimittajamaksut ja tilaukset  
- Pankkikulut ja -korot  

Maksujen täsmäytys säästää merkittävästi aikaa saapuvien ja lähtevien maksujen kirjaamisessa. Pankkitilin tapahtumia [!INCLUDE[prod_short](includes/prod_short.md)]issa ei kuitenkaan pidetä 100-prosenttisen oikeina, ennen kuin suoritat pankkitäsmäytyksen.  

Pankkitäsmäytyksellä varmistat, että pankkitili [!INCLUDE[prod_short](includes/prod_short.md)]issa vastaa pankin ulkoista tiliä.  

 ![Kuva pankkitilien täsmäytyksestä.](media/Set-Up-Bank-Accounts/BankReconciliation.png)

Yllä olevassa kuvassa vasemmanpuoleisin puoli edustaa pankkitiliä [!INCLUDE[prod_short](includes/prod_short.md)]issa ja oikeimmanpuoleisin puoli edustaa pankista verkkopankkisovelluksen kautta tuotuja tapahtumia. Keskellä olevassa kaaviossa näkyvät tapahtumat molemmilta puolilta, eli pankkitäsmäytys.

[!INCLUDE[prod_short](includes/prod_short.md)] -pankkitilin useimpien tapahtumien tulisi olla fyysisen pankin tiedossa. Poikkeuksiin kuuluu muutamia tapauksia:  

- [!INCLUDE[prod_short](includes/prod_short.md)]iin kirjatut korjaukset  
- Myönnetyt sekit, joita ei ole vielä lunastettu 
- Toimittajan maksut, joita pankki ei ole vielä hyväksynyt  

Pankin fyysisen tilin tapahtumat, joita ei ole tunnistettu maksujen täsmäytyskirjauskansiossa, kuten seuraavat:  

- Uudet toimittajatilaukset  
- Asiakasmaksut ilman kuvausta
- Pankin korko
- Pankkikulut
- Luottokorttimaksuja ei ole vielä raportoitu

Mitä parempia yhdistämistietoja teet maksujen täsmäytyskirjauskansiossa, sitä enemmän tapahtumia kirjataan automaattisesti ja sitä helpompaa kausittainen pankkitäsmäytys on.

Katso alla olevasta videosta perusvaiheet pankkitilin määrittämiseksi [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa.

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

> [!WARNING]
> Jotkin kentät voivat sisältää luottamuksellisia tietoja, kuten kentät **Pankkikonttorin nro**, **Pankkitilin numero**, **SWIFT-koodi** ja **IBAN-koodi**. Lue lisää kohdasta [Valvo arkaluontoisia kenttiä](across-log-changes.md#monitor-sensitive-fields).

## <a name="to-set-up-bank-accounts"></a>Pankkitilien määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit**, valitse sitten vastaava linkki.
2. Valitse **Pankkitilit**-sivulla **Uusi**-toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Esimerkki voisi olla **Pankkitilin kirjausryhmä** -kenttä, joka yhdistää pankkitilin taseen taustalla olevaan KP-tiliin. Lisätietoja kohdassa [Kirjausryhmien määrittäminen](finance-posting-groups.md).

> [!TIP]
> Jotkin kentät on piilotettu, kunnes valitset **Näytä lisää** -toiminnon, koska niitä käytetään harvoin. Toiset on lisättävä mukauttamisen avulla. Lue lisää kohdasta [Työtilan mukauttaminen](ui-personalization-user.md).

Voit luoda yrityksellesi niin monta pankkitiliä kuin tarvitset. Kullekin pankkitilille on määritettävä tiedot, jotka tekevät pankkitilistä yksilöllisesti tunnistettavan. Nämä tiedot sisältävät pankin maantieteellisen osoitteen, erityyppisten tapahtumien numerosarjat (kuten suoraveloitukset ja tilisiirrot), valuutan, jossa arvot määritetään sekä tiedot, joita käytetään tiliotteiden tuomiseen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
<!--
The following table explains key fields.

|Field|Description|  
|---------------------------------|---------------------------------------|  
|**General FastTab**||
|No.|Specifies the number of the bank account, according to the specified number series. If the number series allow manual numbering, any alphanumeric code up to 20 characters can be used.|
|Name|The Name of the bank holding the account.|
|Bank Branch No.|Typically used to identify the bank branch in domestic payments, it's very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Account No.|Typically used to identify the bank account number in domestic payments, it's very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Balance|Shows the bank account balance in the account currency.|
|Balance (LCY)|Shows the bank account balance in the local currency (LCY).|
|Our Contact Code|Specifies a code to identify the employee responsible for this bank account. The employee must be created in the **Salesperson/Purchaser** table.|
|Blocked|Specifies the related record is blocked from being posted in transactions, for example the account is obsolete after a bank change.|
|SEPA Direct Debit Exp. Format|Specifies the single euro payments area (SEPA) format of the bank file to be exported when you choose **Create Direct Debit File** on the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Credit Transfer Msg. Nos.|Specifies the number series for bank instruction messages created with the export file you create from the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Direct Debit Msg. Nos.|Specifies the number series to be used on the direct debit file you export for a direct debit collection entry on the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Creditor No.|Specifies your company as the creditor in connection with payment collection from customers using SEPA direct debit. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Bank Clearing Standard|The national bank names register used for the sender bank account.|
|Bank Clearing Code|Specifies the code for bank clearing required according to the format standard you selected in the **Bank Clearing Standard** field. The bank clearing code can be used as an alternative to SWIFT and IBAN to identify your bank as the sender of a bank transfer.|
|Last Date Modified|Date of the latest modification of the bank account.|
|**Payment Matching**||
|Disable Automatic Payment Matching|Specifies whether or not to disable automatic payment matching after importing bank transactions for this bank account. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Payment Match Tolerance**||
|Match Tolerance Type|Specifies the tolerance the automatic payment application function will use to apply the *Amount Incl. Tolerance Matched* rule for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Match Tolerance Value|Specifies if the automatic payment application function will apply the *Amount Incl. Tolerance Matched* rule by percentage or amount. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Hidden Fields**||
|Search Name|Specifies an alternate name you can use to search for the record in question when you can't remember the value in the **Name** field.|
|Min. Balance|Specifies a minimum balance for the bank account. This field is for information purposes only.|
|Positive Pay Export Code|Specifies a code for the data exchange definition managing the export of positive-pay files. Learn more at [Export Positive Pay Files](finance-how-positive-pay.md).|
|**Communication FastTab**||
|Address|The address of the bank branch.|
|Address 2|An additional address field for the bank branch.|
|Post Code|The post code of the bank branch.|
|City|The city of the bank branch.|
|Country/Region Code|The country/region code of the bank branch.|
|Phone No.|The phone number of the bank branch.|
|Mobile Phone No.|The mobile phone number of the bank branch.|
|Contact|The main contact in the bank branch. Additional contacts can be created in the **Contacts** module.|
|Fax No.|The fax number of the bank branch.|
|Email|The email address of the bank branch.|
|Home Page|The home page address of the bank branch website.|
|**Posting FastTab**||
|Currency Code|Specifies the relevant currency code for the bank account. Applying a currency code to a bank account limits all transactions to only using the applied currency code. Leaving the currency code blank allows transactions in all currencies, however, the amount will eventually be converted to the LCY using the applied currency rate. Checks issued from this account follow the same rules.|
|Last Check No.|The number of the latest check issued from this account.|
|Transit No.|Specifies a bank identification number of your own choice.|
|Last Statement No.|The number of the latest bank reconciliation posted to this account. Learn more at [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Last Payment Statement No.|The number of the latest payment reconciliation posted to this account. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Last Bank Statement|The ending balance of the last bank statement. Learn more at [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Bank Acc. Posting Group|Specifies a code for the bank account's posting group. The **Bank Acc. Posting Group** connects the bank account to the G/L account in the balance sheet.|
|**Transfer**||
|Transit No.|Specifies a bank identification number of your own choice.|
|SWIFT Code|Specifies the international bank identifier (SWIFT) code of the bank in which you have account. The SWIFT code is very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|IBAN|Specifies the bank account's international bank account number (IBAN). The IBAN code is very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Statement Import Format|Specifies the format of the bank statement file imported into this bank account. This format is used in both the payment reconciliation journals and bank account reconciliations.|
|Payment Export Format|Specifies the format of the bank file that is exported when you choose **Export Payments to File** on the **Payment Journal** page.|
-->

## <a name="to-enter-an-opening-balance"></a>Alkusaldon syöttäminen

Voit täyttää **Saldo**-kenttään alkusaldon, kun pankkitilitapahtuma ja kyseinen summa on kirjattu. Voit tehdä tämän suorittamalla pankkitilin täsmäytyksen. Lisätietoja on kohdassa [Pankkitilien täsmäyttäminen](bank-how-reconcile-bank-accounts-separately.md).  
>
> Vaihtoehtoisesti voit ottaa käyttöön alkusaldon osana yleistietojen luontia uusissa yrityksissä käyttämällä asetusten ohjattua **Siirrä yritystiedot** -määritysopasta. Lue lisätietoja kohdasta [Valmistautuminen liiketoimintaan](ui-get-ready-business.md).  

> [!IMPORTANT]
> Älä kirjaa alkusaldoa suoraan pääkirjanpitoon. Jos KP-tilillä on kirjauksia, jotka on kirjattu siihen suoraan, et yleensä pysty täsmäyttämään pankkitiliä. Valuuttamääräisten pankkitilien kohdalla tällainen käytäntö johtaa erojen kertymiseen, kun kirjaat lisää pankkitilin täsmäytyksiä. Usein pankin avaussaldo kirjataan suoraan pankkitilille, ja summa päätyy KP-tiliin. Voit vaihtoehtoisesti kumota sen myöhemmin sellaisen KP-tilin osalta, jota käytät pääkirjanpidon avaussaldon tasapainottamista varten. Molemmissa tapauksissa sinun on tasapainotettava mahdolliset suorat kirjaukset KP-tiliin ennen ensimmäisen pankkitäsmäytyksen aloittamista&mdash;erityisesti silloin, kun pankkitili käyttää ulkomaan valuuttaa.

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Pankkitilin määrittäminen pankkitiedostojen tuontia tai vientiä varten

**Pankkitilin kortti** -sivun **Siirto**-pikavälilehden kentät liittyvät pankkisyötteiden ja -tiedostojen tuontiin ja vientiin. Lue lisätietoja on kohdissa [AMC Banking 365 Fundamentals -laajennuksen käyttäminen](ui-extensions-amc-banking.md) ja [Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 2.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit**, valitse sitten vastaava linkki.
2. Avaa sen pankkitilin kortti, josta viet tai johon tuot pankkitiedostot.
3. Täytä **Siirto**-pikavälilehdessä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Eri tiedostojen vientipalvelut ja niiden tiedostomuodot edellyttävät erilaisia asetuksia **Pankkitilin kortti** -sivulla. Saat ilmoituksen virheellisistä tai puuttuvista asetusarvoista, kun yrität viedä tiedoston. Lue huolellisesti kenttien lyhyet kuvaukset tai katso lisätietoja liittyvien toimenpiteiden ohjeaiheista. Esimerkiksi maksutiedoston vienti pohjoisamerikkalaiseen sähköiseen rahansiirtoon (EFT-toiminto) edellyttää, että sekä **Viimeinen maksuosoitusehdotusnumero**- että **Siirtonro**-kentät täytetään. Lue lisätietoja kohdasta [Maksujen vieminen pankkitiedostoon](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Pankkitilin **Siirto**-pikavälivälilehden kentät palvelevat eri tarkoituksia sen mukaan, onko maksu saapuva vai lähtevä.

Alla oleva kuva näyttää saapuvien maksujen reitin (kuvauksen numerot vastaavat kuvassa olevia numeroita):

:::row:::
    :::column:::

1. Tapahtumat viedään pankkitililtä joko ihmisen luettavissa olevassa .csv-muodossa tai pankin omassa muodossa.
2. *Tiedonsiirtomääritys* yhdistää tiedoston tiedot kenttiin [!INCLUDE[prod_short](includes/prod_short.md)]issa. Lisätietoja kohdassa [Tietojen vaihdon määrittäminen](across-set-up-data-exchange.md)
3. *Tietojen vienti- ja tuontiasetukset* määrittävät viennin tai tuonnin, ja ne linkittyvät tiedonsiirtomääritykseen.
4. *Tiliotteiden tuontimuoto* linkittää tuontiasetukset pankkitiliin.
5. Maksut tuodaan joko **maksujen täsmäytyskirjauskansio**- tai **pankkitilin täsmäytys** -sivun kautta.

  :::column-end:::
  :::column:::

        ![Kuva pankista pankkitileille saaduista maksuista.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)

  :::column-end:::
:::row-end:::

Saapuvat maksut tuodaan aina **maksujen täsmäytyskirjauskansio** -sivun kautta tai suoraan **pankkitilin täsmäytys** -sivulle. Sitä vastoin lähtevät maksut voivat olla peräisin mistä tahansa maksupäiväkirjasta. Ainoa edellytys on, että **Salli maksun vienti** -kenttä on valittuna asiaankuuluvassa maksupäiväkirjaerässä.

Alla oleva kuva näyttää lähtevien maksujen reitin (kuvauksen numerot vastaavat kuvassa olevia numeroita):

:::row:::
    :::column:::

6. Tapahtumat, jotka täytetään maksupäiväkirjaan, joka on valmisteltu maksujen tiedostoon viemistä varten.
7. *Tiliotteiden tuontimuoto* linkittää tuontiasetukset pankkitiliin.
8. *Tietojen vienti- ja tuontiasetukset* määrittävät viennin tai tuonnin, ja ne linkittyvät tiedonsiirtomääritykseen.
9. *Tiedonsiirtomääritys* yhdistää tiedoston tiedot kenttiin [!INCLUDE[prod_short](includes/prod_short.md)]issa. Lisätietoja kohdassa [Tietojen vaihdon määrittäminen](across-set-up-data-exchange.md)
10. Maksut viedään maksupäiväkirjasta ja tuodaan pankkitilille.

  :::column-end:::
  :::column:::

        ![Kuva pankkitileiltä tehdyistä maksuista, jotka on lähetetty pankille.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)

  :::column-end:::
:::row-end:::

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Toimittajan pankkitilien määrittäminen pankkitiedostojen vientiä varten

**Toimittajan pankkitilin kortti** -sivun **Siirto**-pikavälilehden kentät liittyvät pankkisyötteiden ja -tiedostojen vientiin. Lisätietoja on kohdassa [AMC Banking 365 Fundamentals -laajennuksen käyttäminen](ui-extensions-amc-banking.md) ja [Maksujen vieminen pankkitiedostoon](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

[!INCLUDE[purchase-vendor-bank-account](includes/purchase-vendor-bank-account.md)]

## <a name="changing-your-bank-account"></a>Pankkitilin vaihtaminen

Käyttääksesi yrityksessäsi toista pankkitiliä, sinun on luotava uusi pankkitili [!INCLUDE[prod_short](includes/prod_short.md)]issa. Suosittelemme, ettet vain korvaa tällä hetkellä käyttämäsi tilin tietoja, koska se voi aiheuttaa virheellisiä tietoja. Esimerkiksi avaussaldosi voi olla virheellinen tai pankkisyöte saattaa lakata toimimasta oikein. On tärkeää, että pidät nykyiset ja uudet tilit erillään.

Kun olet luonut uuden pankkitilin, luo myös uusi pankin kirjausryhmä ja määritä se uudelle pääkirjanpitotilille. Voit käyttää aiemmin luotua pankin kirjausryhmää uudelleen, ja pankkitapahtumat kirjataan samoille pääkirjanpitotileille kuin tapahtumat muilta pankkitileiltä, jotka jakavat pankin kirjausryhmän. Suosittelemme kuitenkin, että luot uuden pankin kirjausryhmän ja pääkirjanpitotilin, jotta täsmäytys on helpompaa.

> [!NOTE]
> Muista, että avointen myyntilaskujen pankkitilitiedot näkyvät edelleen alkuperäisellä pankkitilillä. Näin ollen maksut todennäköisesti kirjataan edelleen kyseiselle tilille. Suosittelemme, että pidät molemmat tilit aktiivisina jonkin aikaa muutoksen jälkeen.

Jos haluat tarkastella käteistilejäsi tarkemmin taloudellisessa raportoinnissa, käytä **Alkusumma**- ja **Loppusumma**-tilejä tilikartassasi, **Summausväli**-rivejä taloudellisissa raporteissa tai KP-tililuokkia. Lisätietoja on kohdassa [Liiketoimintatiedot ja Financial Reporting](bi.md).

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/cash-management-dynamics-365-business-central/)

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
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
