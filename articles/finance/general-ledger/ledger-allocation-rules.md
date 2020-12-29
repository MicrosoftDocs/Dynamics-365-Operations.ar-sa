---
title: قواعد توزيع دفتر الأستاذ
description: توفر هذه المقالة معلومات حول قواعد توزيع دفتر الأستاذ. وهذ تصف المكونات المختلفة لقواعد التوزيع هذه وأساليب التوزيع التي يمكن استخدامها لها.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42896fc8b204df921f1e24797098472eca090d30
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439997"
---
# <a name="ledger-allocation-rules"></a><span data-ttu-id="e239e-104">قواعد توزيع دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="e239e-104">Ledger allocation rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e239e-105">توفر هذه المقالة معلومات حول قواعد توزيع دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="e239e-105">This article provides information about ledger allocation rules.</span></span> <span data-ttu-id="e239e-106">وهذ تصف المكونات المختلفة لقواعد التوزيع هذه وأساليب التوزيع التي يمكن استخدامها لها.</span><span class="sxs-lookup"><span data-stu-id="e239e-106">It describes the various components of these allocation rules and the allocation methods that can be used for them.</span></span>

<span data-ttu-id="e239e-107">يتم استخدام قواعد توزيع دفتر الأستاذ لحساب وإنشاء دفاتر يومية التوزيع وإدخالات الحسابات لتوزيع أرصدة دفتر الأستاذ أو المبالغ الثابتة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="e239e-107">Ledger allocation rules are used to automatically calculate and generate allocation journals and account entries for the allocation of ledger balances or fixed amounts.</span></span> <span data-ttu-id="e239e-108">وقد تكون طرق التوزيع متغيرة أو ثابتة.</span><span class="sxs-lookup"><span data-stu-id="e239e-108">Allocation methods can be variable or fixed.</span></span> <span data-ttu-id="e239e-109">ويمكن استخدام طرق التوزيع التالية لقواعد توزيع دفتر الأستاذ:</span><span class="sxs-lookup"><span data-stu-id="e239e-109">The following allocation methods can be used for ledger allocation rules:</span></span>

-   <span data-ttu-id="e239e-110">**الأساس** – تُستخدم هذه االطريقة المتغيرة عندما يعتمد التوزيع على رصيد دفتر الأستاذ الفعلي، استناداً إلى معايير عامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="e239e-110">**Basis** – This variable method is used when the allocation depends on the actual ledger balance, based on filter criteria.</span></span> <span data-ttu-id="e239e-111">فمثلاً، يُمكن توزيع نفقات الإعلانات وفقًا لمبيعات كل قسم بالنسبة إلى المبيعات الإدارية الإجمالية.</span><span class="sxs-lookup"><span data-stu-id="e239e-111">For example, advertising expenses can be allocated based on each department's sales in proportion to the total departmental sales.</span></span>
-   <span data-ttu-id="e239e-112">**النسبة المئوية الثابتة** و **الوزن الثابت** – في هذه الطرق، يتم تحديد الوزن أو النسبة المئوية للتوزيع مباشرةً للقاعدة.</span><span class="sxs-lookup"><span data-stu-id="e239e-112">**Fixed percentage** and **Fixed weight** – For these methods, the allocation percentage or weight is defined directly for the rule.</span></span> <span data-ttu-id="e239e-113">على سبيل المثال، يمكن توزيع نفقات الإعلان بحيث يتلقى القسم أ 70 في المائة من مصروفات الإعلانات ويتلقى القسم ب 30 في المائة.</span><span class="sxs-lookup"><span data-stu-id="e239e-113">For example, advertising expenses can be allocated so that Department A receives 70 percent of the advertising expense and Department B receives 30 percent.</span></span>
-   <span data-ttu-id="e239e-114">**بالتساوي** – توزع هذه الطريقة المبلغ بالتساوي على كل وجهة محددة.</span><span class="sxs-lookup"><span data-stu-id="e239e-114">**Equally** – This method distributes the amount equally to each defined destination.</span></span> <span data-ttu-id="e239e-115">على سبيل المثال، إذا تم تحديد وجهات للقسم أ وب، يمكن توزيع نفقات الإعلان بحيث يتلقى كلُّ من القسم أ والقسم ب 50 في المائة من مصروفات إعلانات.</span><span class="sxs-lookup"><span data-stu-id="e239e-115">For example, if destinations are defined for Department A and Department B, advertising expenses can be allocated so that both Department A and Department B receive 50 percent of the advertising expense.</span></span>

<span data-ttu-id="e239e-116">إذا تم استخدام الأساس كطريقة التوزيع لقاعدة توزيع، فعندئذٍ يجب عليك أيضًا تحديد قاعدة أساسية لتوزيع دفتر أستاذ منفصل.</span><span class="sxs-lookup"><span data-stu-id="e239e-116">If Basis is used as the allocation method for an allocation rule, you must also define separate ledger allocation basis rules.</span></span> <span data-ttu-id="e239e-117">وتتيح عملية "طلب توزيع العملية" للمستخدمين إمكانية معالجة قاعدة توزيع دفتر الأستاذ ومعاينة إدخالات دفتر يومية التوزيع الناتج قبل ترحيل أو حذف التوزيعات المحسوبة.</span><span class="sxs-lookup"><span data-stu-id="e239e-117">The "Process allocation request" process lets users process the ledger allocation rule and preview the resulting allocation journal entries before they either post or delete the calculated allocations.</span></span>

## <a name="components-of-ledger-allocation-rules"></a><span data-ttu-id="e239e-118">مكونات قواعد توزيع دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="e239e-118">Components of ledger allocation rules</span></span>
<span data-ttu-id="e239e-119">تشتمل كل قاعدة تخصيص على أربعة مكونات: عام ومصدر ووجهة ومقابل.</span><span class="sxs-lookup"><span data-stu-id="e239e-119">Each allocation rule has four components: general, source, destination, and offset.</span></span> <span data-ttu-id="e239e-120">ويُتطلب عنصر إضافي، قواعد أساسات توزيع دفتر الأستاذ، إذا تم استخدام الأساس باعتباره طريقة التوزيع.</span><span class="sxs-lookup"><span data-stu-id="e239e-120">An additional component, ledger allocation bases rules, is required if Basis is used as the allocation method.</span></span> <span data-ttu-id="e239e-121">ويقدم كل مكون من هذه المكونات جزءًا مهمًا من المعلومات المطلوبة لمعالجة عمليات التوزيع.</span><span class="sxs-lookup"><span data-stu-id="e239e-121">Each component provides a critical piece of the information that is required in order to process allocations.</span></span>

-   <span data-ttu-id="e239e-122">**عام** – هذا المكون هو الذي يقوم فيه المستخدم بتحديد الخيارات مثل  طريقة التوزيع وإعدادات القاعدة بين الشركات الشقيقة وما إذا كانت القاعدة نشطة أم لا.</span><span class="sxs-lookup"><span data-stu-id="e239e-122">**General** – This component is where the user specifies options such as the allocation method, intercompany rule settings, and whether the rule is active.</span></span>
-   <span data-ttu-id="e239e-123">**المصدر** -هذا المكون هو الذي يقوم فيه المستخدم بتحديد البيانات المصدر للتوزيع.</span><span class="sxs-lookup"><span data-stu-id="e239e-123">**Source** – This component is where the user specifies the source data for the allocation.</span></span> <span data-ttu-id="e239e-124">يمكن إسناد التوزيع إلى أرصدة دفتر الأستاذ (**مصدر البيانات** = **دفتر الأستاذ**) أو المبالغ الثابتة (**مصدر بيانات** = **القيمة الثابتة**).</span><span class="sxs-lookup"><span data-stu-id="e239e-124">Allocation can be based on ledger balances (**Data source** = **Ledger**) or fixed amounts (**Data source** = **Fixed value**).</span></span> <span data-ttu-id="e239e-125">وعند تعيين **مصدر بيانات** إلى **دفتر الأستاذ**، يجب تحديد معايير عامل التصفية المصدر لقاعدة توزيع دفتر الأستاذ (على سبيل المثال، نفقات الإعلان).</span><span class="sxs-lookup"><span data-stu-id="e239e-125">When **Data source** is set to **Ledger**, source filter criteria must be defined for the ledger allocation rule (for example, for the advertising expenses).</span></span>
-   <span data-ttu-id="e239e-126">**الوجهة** – يحدد هذا المكون الطريقة التي يجب بها توزيع نتيجة حساب التوزيع والمحاسبة عليها.</span><span class="sxs-lookup"><span data-stu-id="e239e-126">**Destination** – This component defines how the result of the allocation calculation should be distributed and accounted for.</span></span> <span data-ttu-id="e239e-127">على سبيل المثال، يمكن أن يكون هناك بند وجهة واحد لكل قسم.</span><span class="sxs-lookup"><span data-stu-id="e239e-127">For example, there can be one destination line for each department.</span></span>
-   <span data-ttu-id="e239e-128">**المقابل** – يحدد هذا المكون الطريقة التي يجب بها تحديد الأبعاد الحسابات الرئيسية للإدخالات المقابلة التي توازن بين إدخالات الوجهة.</span><span class="sxs-lookup"><span data-stu-id="e239e-128">**Offset** – This component defines how main accounts and dimensions should be determined for the offset entries that balance the destination entries.</span></span> <span data-ttu-id="e239e-129">وعادةً ما يتم استخدام الخيارات المحددة من قِبل المستخدم بدلاً من الحسابات والأبعاد المحددة في المصدر.</span><span class="sxs-lookup"><span data-stu-id="e239e-129">User-defined options are typically used instead of accounts and dimensions that are based on the source.</span></span> <span data-ttu-id="e239e-130">وعند تعيين **مصدر البيانات** إلى **قيمة ثابتة**، لا يمكن استخدام **مصدر** كخيار.</span><span class="sxs-lookup"><span data-stu-id="e239e-130">When **Data source** is set to **Fixed value**, **Source** can't be used as an option.</span></span>
-   <span data-ttu-id="e239e-131">**قواعد أساس توزيع دفتر الأستاذ** – تستخدم هذه القواعد معايير عامل التصفية المصدر الخاصة بها لتحديد أرصدة دفتر الأستاذ التي يجب استخدامها للتوزيع (على سبيل المثال، إيراد لكل قسم).</span><span class="sxs-lookup"><span data-stu-id="e239e-131">**Ledger allocation basis rules** – These rules use their own source filter criteria to determine which ledger balances should be used for allocation (for example, the revenue per department).</span></span> <span data-ttu-id="e239e-132">يمكن استخدام قاعدة أساس التوزيع مع العديد من قواعد التوزيع.</span><span class="sxs-lookup"><span data-stu-id="e239e-132">Each allocation basis rule can be used with multiple allocation rules.</span></span>




