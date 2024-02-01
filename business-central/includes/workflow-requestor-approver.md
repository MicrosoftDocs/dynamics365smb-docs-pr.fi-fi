---
author: brentholtorf
ms.topic: include
ms.date: 05/30/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Kun määrität käyttäjiä hyväksynnän työnkulkuihin, on tärkeää, että sama käyttäjä ei ole työnkulun käyttäjäryhmässä sekä pyytäjä että hyväksyjä. Kun käyttäjä on sekä pyytäjä että hyväksyjä, hyväksynnät toimivat heille seuraavasti:

* Heidän pyyntönsä hyväksytään aina automaattisesti.
* Jos hyväksyjiä on useita, vain ne hyväksyjät, joilla on suurempi järjestysnumero työnkulun käyttäjäryhmässä, voivat muuttaa pyynnön tilaksi Hyväksytty. Hyväksyjät, joilla on pienempi järjestysnumero, voivat hyväksyä pyyntöjä, mutta heidän hyväksyntänsä ei vaikuta pyynnön tilaan.