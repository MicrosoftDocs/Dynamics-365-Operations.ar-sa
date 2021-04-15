---
title: إعداد كيان قانوني لعملية التوحيد.
description: أثناء عملية التوحيد، يتم جمع الحركات من مجموعات متعددة من الكيان القانون داخل مجموعة واحدة من حسابات الكيان القانوني. يوضح هذا الموضوع كيفية إعداد كيان قانوني لعملية التوحيد.
author: jinniew
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 6f718bef3b1b07d3bb03dbf6acbf1cdf58aa7b8a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815466"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a><span data-ttu-id="3f1ed-104">إعداد كيان قانوني لعملية التوحيد.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-104">Prepare a legal entity for the consolidation process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f1ed-105">أثناء عملية التوحيد، يتم جمع الحركات من مجموعات متعددة من الكيان القانون داخل مجموعة واحدة من حسابات الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-105">During a consolidation, you gather transactions from several sets of legal entity accounts into a single set of legal entity accounts.</span></span> <span data-ttu-id="3f1ed-106">يوضح هذا الموضوع كيفية إعداد كيان قانوني لعملية التوحيد.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-106">This topic explains how to prepare a legal entity for a consolidation.</span></span>

> [!NOTE]
> <span data-ttu-id="3f1ed-107">ونوصي باستخدام Management Reporter لـ Microsoft Dynamics 365 Finance لدمج النتائج المالية للكيانات القانونية المتعددة بتنسيق موحد.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-107">We recommend that you use Management Reporter for Microsoft Dynamics 365 Finance to combine the financial results for multiple legal entities in a consolidated format.</span></span> <span data-ttu-id="3f1ed-108">يتيح لك Management Reporter إنشاء تقارير مالية موحدة عبر الكيانات القانونية، واستخدام Excel لاستيراد بيانات التوحيد من المصادر الأخرى، وترجمة المبالغ إلى أي عدد من العملات التي يتم بها إعداد تقارير بدون الحاجة إلى تشغيل عملية التوحيد في Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-108">Management Reporter lets you create consolidated financial reports across legal entities, use Excel to import consolidation data from other sources, and translate amounts into any number of reporting currencies without having to run the consolidation process in Dynamics 365 Finance.</span></span>

<span data-ttu-id="3f1ed-109">يمكنك طباعة تقارير، مثل البيانات المالية، من الكيان القانوني الموحد.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-109">You can print reports, such as financial statements, from the consolidated legal entity.</span></span> <span data-ttu-id="3f1ed-110">ومع ذلك، لا يمكنك استخدام الكيان القانوني الموحد للحركات اليومية.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-110">However, you can't use the consolidated legal entity for daily transactions.</span></span>

<span data-ttu-id="3f1ed-111">يمكنك دمج البيانات من الكيانات القانونية التي تستخدم قواعد بيانات مختلفة عن الكيان القانوني الموحد.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-111">You can consolidate data from legal entities that use different databases than the consolidated legal entity.</span></span> <span data-ttu-id="3f1ed-112">يشار إلى عملية التوحيد هذه على أنها *توحيد مستورد*.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-112">This consolidation process is referred to as an *import consolidation*.</span></span> <span data-ttu-id="3f1ed-113">بدلاً من ذلك، يمكن للكيانات القانونية استخدام نفس قاعدة البيانات ككيان قانوني موحد.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-113">Alternatively, the legal entities can use the same database as the consolidated legal entity.</span></span> <span data-ttu-id="3f1ed-114">يشار إلى عملية التوحيد هذه على أنها *توحيد عبر الإنترنت*.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-114">This consolidation process is referred to as an *online consolidation*.</span></span>

<span data-ttu-id="3f1ed-115">يجمع الكيان القانوني الموحد النتائج والأرصدة الخاصة بالشركات التابعة.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-115">The consolidated legal entity collects the results and balances of the subsidiaries.</span></span> <span data-ttu-id="3f1ed-116">لإعداد كيان قانوني موحد لعملية التوحيد، يجب اتباع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-116">To prepare a consolidated legal entity for a consolidation, follow these steps.</span></span>

1. <span data-ttu-id="3f1ed-117">انتقل إلى **دفتر الأستاذ العام \> الإعداد \> المؤسسات \> الكيانات القانونية**.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-117">Go to **General ledger \> Setup \> Organization \> Legal entities**.</span></span>
2. <span data-ttu-id="3f1ed-118">حدد **جديد** لإنشاء الكيان القانوني الذي سيكون الكيان القانوني الموحد.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-118">Select **New** to create the legal entity that will be the consolidated legal entity.</span></span>
3. <span data-ttu-id="3f1ed-119">حدد خانة الاختيار **استخدام لعملية التوحيد المالي**، ثم أدخل المعلومات حول الكيان القانوني الموحد.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-119">Select the **Use for financial consolidation process** check box, and then enter information about the consolidated legal entity.</span></span> <span data-ttu-id="3f1ed-120">تأكد من أن هذه المعلومات هي كما تريد أن تظهر في البيانات المالية للكيان القانوني الموحد.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-120">Be sure to enter this information exactly as you want it to appear on financial statements for the consolidated legal entity.</span></span>
4. <span data-ttu-id="3f1ed-121">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-121">Close the page.</span></span>
5. <span data-ttu-id="3f1ed-122">حدد الكيان القانوني الموحد في الحقل الموجود في الركن الأيمن العلوي من الصفحة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-122">Select the consolidated legal entity in the field in the upper-right corner of the page, and then select **OK**.</span></span>
6. <span data-ttu-id="3f1ed-123">انتقل إلى **دفتر الأستاذ العام \> الإعداد \> دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-123">Go to **General ledger \> Setup \> Ledger**.</span></span>
7. <span data-ttu-id="3f1ed-124">حدد مخطط الحسابات والتقويم المالي وعملة المحاسبة وعملة تقارير الاختيارية ونوع سعر الصرف الافتراضي للكيان القانوني الموحد.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-124">Select the chart of accounts, the fiscal calendar, the accounting currency, an optional reporting currency, and the default type of exchange rate for the consolidated legal entity.</span></span> 
8. <span data-ttu-id="3f1ed-125">اذهب إلى **دفتر الأستاذ العام \> الإعداد \> العملة \> أسعار صرف العملات**.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-125">Go to **General ledger \> Setup \> Currency \> Currency exchange rates**.</span></span>
9. <span data-ttu-id="3f1ed-126">قم بإعداد أسعار الصرف الحالية في الفترات المناسبة لعملات الكيانات القانونية التابعة.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-126">Set up currency exchange rates in relevant periods for the currencies of the subsidiary legal entities.</span></span>
10. <span data-ttu-id="3f1ed-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-127">Close the page.</span></span>
11. <span data-ttu-id="3f1ed-128">إذا كان الكيان القانوني الموحد شركات تابعة تستخدم عملات أجنبية، فاتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-128">If the consolidated legal entity has subsidiaries that use foreign currencies, follow these steps:</span></span>

    1. <span data-ttu-id="3f1ed-129">انتقل إلى **دفتر الأستاذ العام \> الإعداد \> الترحيل \> حسابات الحركات التلقائية**.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-129">Go to **General ledger \> Setup \> Posting \> Accounts for automatic transactions**.</span></span>
    2. <span data-ttu-id="3f1ed-130">في الحقل **نوع الترحيل**، حدد حسابًا مناسبًا:</span><span class="sxs-lookup"><span data-stu-id="3f1ed-130">In the **Posting type** field, select an appropriate account:</span></span>

        - <span data-ttu-id="3f1ed-131">إذا كان للكيان القانوني فروع خارجية مستقلة ماليًا أو تشغيليًا عن الكيان القانوني الأصلي، فحدد حسابا مناسبا لنوع الترحيل **حساب الأرباح والخسائر لفروق التوحيد**.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-131">If the legal entity has foreign subsidiaries that are financially or operationally interdependent with the parent legal entity, select an appropriate account for the **Profit and loss account for consolidation differences** posting type.</span></span>
        - <span data-ttu-id="3f1ed-132">إذا كنت تقوم بتوحيد شركة فرعية مستقلة ماليًا وتشغيليًا عن الكيان القانوني الأصلي أو كيان قانوني الذي يحتوي على نتائج العديد من الشركات الفرعية المستقلة ماليًا وتشغيليًا عن الكيان القانوني الأصلي، وإذا كنت تستخدم أساليب ترجمة لدمج البيانات، فحدد حسابًا مناسبًا لنوع الترحيل **حساب الرصيد لفروق التوحيد**.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-132">If you're consolidating a subsidiary that is financially and operationally independent of the parent legal entity, or a legal entity that contains the results of several subsidiaries that are financially and operationally independent of the parent legal entity, and if you're using translation methods to consolidate the data, select an appropriate account for the **Balance account for consolidation differences** posting type.</span></span>

    3. <span data-ttu-id="3f1ed-133">في الحقل **الحساب الرئيسي**، حدد الحسابات الرئيسية التي يجب استخدامها لعمليات تسوية إعادة تقييم العملة الأجنبية.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-133">In the **Main account** field, select the main accounts that should be used for foreign currency revaluation adjustments.</span></span>
    4. <span data-ttu-id="3f1ed-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-134">Close the page.</span></span>

    <span data-ttu-id="3f1ed-135">إذا قمت بإنشاء الكيان القانوني الموحد في أول الفترة، فيمكنك إعادة تقييم بتعديل مبالغ العملة الأجنبية وفقًا لتغير سعر الصرف أثناء فترة التوحيد.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-135">If you create the consolidated legal entity early in a period, you can revalue foreign currency amounts as exchange rates change during the consolidation period.</span></span>

<span data-ttu-id="3f1ed-136">الكيان القانوني الموحد جاهز الآن للوظيفة الدورية **توحيد**.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-136">The consolidated legal entity is now set up for the **Consolidate** periodic job.</span></span> <span data-ttu-id="3f1ed-137">يمكنك إجراء توحيد الاستيراد أو التوحيد عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-137">You can do either an import consolidation or an online consolidation.</span></span>

- <span data-ttu-id="3f1ed-138">لإجراء توحيد الاستيراد، انتقل إلى **دفتر الأستاذ العام \> دوري \> توحيد \> توحيد \[الاستيراد من\]**.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-138">To do an import consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Import from\]**.</span></span>
- <span data-ttu-id="3f1ed-139">لإجراء توحيد عبر الإنترنت، انتقل إلى **دفتر الأستاذ العام \> دوري \> توحيد \> توحيد \[عبر الإنترنت\]**.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-139">To do an online consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Online\]**.</span></span>

> [!NOTE]
> <span data-ttu-id="3f1ed-140">قبل تشغيل التوحيد، يجب عليك تجهيز الكيانات القانونية التابعة لعملية التوحيد.</span><span class="sxs-lookup"><span data-stu-id="3f1ed-140">Before you can process the consolidation, you must prepare the subsidiary legal entities for consolidation.</span></span> <span data-ttu-id="3f1ed-141">لمزيد من المعلومات، راجع [إعداد الكيان القانوني التابع للتوحيد](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="3f1ed-141">For more information, see [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]