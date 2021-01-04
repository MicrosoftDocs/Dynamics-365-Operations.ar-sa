---
title: دفتر الأستاذ المتكامل
description: يوضح هذا الموضوع تكامل بيانات دفتر الأستاذ بين Finance and Operations وتطبيقات Dynamics 365 الأخرى باستخدام Dataverse.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f794d8306a3a752d811d7d84c0ed5f739f423cad
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681632"
---
# <a name="integrated-ledger"></a><span data-ttu-id="672d0-103">دفتر الأستاذ المتكامل</span><span class="sxs-lookup"><span data-stu-id="672d0-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="672d0-104">في تطبيق العمل، تقوم بيانات دفتر الأستاذ بتعريف الأساس الذي تم إعداده لكيفيه عمل أحدي الشركات.</span><span class="sxs-lookup"><span data-stu-id="672d0-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="672d0-105">علي سبيل المثال، تصف بيانات دفتر الأستاذ السنه المالية التي تتبعها الشركة، والعملات التي تتعامل فيها، والحسابات التي تستخدمها.</span><span class="sxs-lookup"><span data-stu-id="672d0-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="672d0-106">يصف هذا الموضوع تكامل البيانات المالية الرئيسية هذه.</span><span class="sxs-lookup"><span data-stu-id="672d0-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="672d0-107">القوالب</span><span class="sxs-lookup"><span data-stu-id="672d0-107">Templates</span></span>

<span data-ttu-id="672d0-108">تشمل بيانات دفتر الأستاذ مجموعة من مخططات الجداول المالية الرئيسية تعمل معًا أثناء تفاعل بيانات المورّد، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="672d0-108">Ledger data includes a collection of core financial table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="672d0-109">تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="672d0-109">Finance and Operations apps</span></span>      | <span data-ttu-id="672d0-110">تطبيق المستند إلى نموذج في Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="672d0-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="672d0-111">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="672d0-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="672d0-112">العملات</span><span class="sxs-lookup"><span data-stu-id="672d0-112">Currencies</span></span>                       | <span data-ttu-id="672d0-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="672d0-113">transactioncurrencies</span></span>            |
<span data-ttu-id="672d0-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="672d0-114">FiscalCalendar</span></span>                   | <span data-ttu-id="672d0-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="672d0-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="672d0-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="672d0-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="672d0-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="672d0-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="672d0-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="672d0-118">ExchRateType</span></span>                     | <span data-ttu-id="672d0-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="672d0-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="672d0-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="672d0-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="672d0-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="672d0-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="672d0-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="672d0-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="672d0-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="672d0-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="672d0-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="672d0-124">MainAccountCategory</span></span>              | <span data-ttu-id="672d0-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="672d0-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="672d0-126">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="672d0-126">MainAccount</span></span>                      | <span data-ttu-id="672d0-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="672d0-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="672d0-128">دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="672d0-128">Ledger</span></span>                           | <span data-ttu-id="672d0-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="672d0-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="672d0-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="672d0-130">ExchangeRates</span></span>                    | <span data-ttu-id="672d0-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="672d0-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="672d0-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="672d0-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="672d0-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="672d0-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="672d0-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="672d0-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="672d0-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="672d0-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="672d0-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="672d0-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="672d0-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="672d0-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="672d0-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="672d0-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="672d0-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="672d0-139">msdyn\_chartofaccounts</span></span>        |


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




