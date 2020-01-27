---
title: دفتر الأستاذ المتكامل
description: يوضح هذا الموضوع تكامل بيانات دفتر الأستاذ بين Finance and Operations وتطبيقات Dynamics 365 الأخرى باستخدام Common Data Service.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 4a0a8f2f52cf9a73efc3557b63793201a7a3f8b8
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853872"
---
# <a name="integrated-ledger"></a>دفتر الأستاذ المتكامل

[!include [banner](../includes/banner.md)]

في تطبيق العمل، تقوم بيانات دفتر الأستاذ بتعريف الأساس الذي تم اعداده لكيفيه عمل أحدي الشركات. علي سبيل المثال، تصف بيانات دفتر الأستاذ السنه المالية التي تتبعها الشركة، والعملات التي تتعامل فيها، والحسابات التي تستخدمها. يصف هذا الموضوع تكامل البيانات المالية الرئيسية هذه.

## <a name="templates"></a>القوالب

تشمل بيانات دفتر الأستاذ مجموعة من مخططات الكيانات المالية الرئيسية تعمل معًا أثناء تفاعل بيانات المورّد، كما هو موضح في الجدول التالي.

تطبيقات Finance and Operations      | تطبيقات Dynamics 365 الأخرى
---------------------------------|---------------------------------
العملات                       | transactioncurrencies
FiscalCalendar                   | msdyn\_fiscalcalendars
FiscalCalendarYear               | msdyn\_fiscalcalendaryears
ExchRateType                     | msdyn\_exchangeratetypes
ExchangeRateCurrencyPair         | msdyn\_currencyexchangeratepairs
FiscalPeriodEntity               | msdyn\_fiscalcalendarperiods
MainAccountCategory              | msdyn\_mainaccountcategory
الحساب الرئيسي                      | msdyn\_mainaccounts
دفتر الأستاذ                           | msdyn\_ledgers
ExchangeRates                    | msdyn\_currencyexchangerates
FinancialCalendarPeriod          | msdyn\_fiscalcalendarperiods
DimensionAttributeEntity         | msdyn\_dimensionattributes.md
DimensionIntegrationFormatEntity | msdyn\_financialdimensionformats.md
LedgerChartOfAccounts            | msdyn\_chartofaccounts.md


[!include [banner](../includes/dual-write-symbols.md)]

[!include [Currency](dual-write/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](dual-write/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](dual-write/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](dual-write/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](dual-write/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Ledger fiscal periods](dual-write/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Main account category](dual-write/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](dual-write/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](dual-write/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](dual-write/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](dual-write/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](dual-write/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](dual-write/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](dual-write/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




