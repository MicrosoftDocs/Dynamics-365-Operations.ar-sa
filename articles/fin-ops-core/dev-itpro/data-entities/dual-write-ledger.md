---
title: دفتر الأستاذ المتكامل
description: يوضح هذا الموضوع تكامل بيانات دفتر الأستاذ بين Finance and Operations وCustomer Engagement باستخدام Common Data Service.
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
ms.openlocfilehash: 43819e23b167663a51095546cab307e7d7c79a38
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771038"
---
## <a name="integrated-ledger"></a><span data-ttu-id="73f64-103">دفتر الأستاذ المتكامل</span><span class="sxs-lookup"><span data-stu-id="73f64-103">Integrated ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73f64-104">في تطبيق العمل، تقوم بيانات دفتر الأستاذ بتعريف الأساس الذي تم اعداده لكيفيه عمل أحدي الشركات.</span><span class="sxs-lookup"><span data-stu-id="73f64-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="73f64-105">علي سبيل المثال، تصف بيانات دفتر الأستاذ السنه المالية التي تتبعها الشركة، والعملات التي تتعامل فيها، والحسابات التي تستخدمها.</span><span class="sxs-lookup"><span data-stu-id="73f64-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="73f64-106">يصف هذا الموضوع تكامل البيانات المالية الرئيسية هذه.</span><span class="sxs-lookup"><span data-stu-id="73f64-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="73f64-107">القوالب</span><span class="sxs-lookup"><span data-stu-id="73f64-107">Templates</span></span>

<span data-ttu-id="73f64-108">تشمل بيانات دفتر الأستاذ مجموعة من مخططات الكيانات المالية الرئيسية تعمل معًا أثناء تفاعل بيانات المورّد، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="73f64-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="73f64-109">تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="73f64-109">Finance and Operations apps</span></span>      | <span data-ttu-id="73f64-110">تطبيقات Dynamics 365 الأخرى</span><span class="sxs-lookup"><span data-stu-id="73f64-110">Other Dynamics 365 apps</span></span>
---------------------------------|---------------------------------
<span data-ttu-id="73f64-111">العملات</span><span class="sxs-lookup"><span data-stu-id="73f64-111">Currencies</span></span>                       | <span data-ttu-id="73f64-112">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="73f64-112">transactioncurrencies</span></span>
<span data-ttu-id="73f64-113">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="73f64-113">FiscalCalendar</span></span>                   | <span data-ttu-id="73f64-114">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="73f64-114">msdyn\_fiscalcalendars</span></span>
<span data-ttu-id="73f64-115">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="73f64-115">FiscalCalendarYear</span></span>               | <span data-ttu-id="73f64-116">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="73f64-116">msdyn\_fiscalcalendaryears</span></span>
<span data-ttu-id="73f64-117">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="73f64-117">ExchRateType</span></span>                     | <span data-ttu-id="73f64-118">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="73f64-118">msdyn\_exchangeratetypes</span></span>
<span data-ttu-id="73f64-119">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="73f64-119">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="73f64-120">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="73f64-120">msdyn\_currencyexchangeratepairs</span></span>
<span data-ttu-id="73f64-121">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="73f64-121">FiscalPeriodEntity</span></span>               | <span data-ttu-id="73f64-122">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="73f64-122">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="73f64-123">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="73f64-123">MainAccountCategory</span></span>              | <span data-ttu-id="73f64-124">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="73f64-124">msdyn\_mainaccountcategory</span></span>
<span data-ttu-id="73f64-125">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="73f64-125">MainAccount</span></span>                      | <span data-ttu-id="73f64-126">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="73f64-126">msdyn\_mainaccounts</span></span>
<span data-ttu-id="73f64-127">دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="73f64-127">Ledger</span></span>                           | <span data-ttu-id="73f64-128">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="73f64-128">msdyn\_ledgers</span></span>
<span data-ttu-id="73f64-129">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="73f64-129">ExchangeRates</span></span>                    | <span data-ttu-id="73f64-130">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="73f64-130">msdyn\_currencyexchangerates</span></span>
<span data-ttu-id="73f64-131">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="73f64-131">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="73f64-132">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="73f64-132">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="73f64-133">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="73f64-133">DimensionAttributeEntity</span></span>         | <span data-ttu-id="73f64-134">msdyn\_dimensionattributes.md</span><span class="sxs-lookup"><span data-stu-id="73f64-134">msdyn\_dimensionattributes.md</span></span>
<span data-ttu-id="73f64-135">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="73f64-135">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="73f64-136">msdyn\_financialdimensionformats.md</span><span class="sxs-lookup"><span data-stu-id="73f64-136">msdyn\_financialdimensionformats.md</span></span>
<span data-ttu-id="73f64-137">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="73f64-137">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="73f64-138">msdyn\_chartofaccounts.md</span><span class="sxs-lookup"><span data-stu-id="73f64-138">msdyn\_chartofaccounts.md</span></span>


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




