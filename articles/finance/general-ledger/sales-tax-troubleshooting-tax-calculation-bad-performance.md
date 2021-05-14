---
title: يؤثر أداء حساب الضريبة على المعاملات
description: يوفر هذا الموضوع معلومات استكشاف الأخطاء وإصلاحها المرتبطة بأداء حساب الضريبة وتاثيرها علي الحركات.
author: shtao
manager: beya
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7ff9d9b80172c3b337737b1cd53b4c56d1befe57
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947593"
---
# <a name="tax-calculation-performance-affects-transactions"></a><span data-ttu-id="3c34b-103">يؤثر أداء حساب الضريبة على المعاملات</span><span class="sxs-lookup"><span data-stu-id="3c34b-103">Tax calculation performance affects transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c34b-104">في بعض الأحيان تتاثر الحركة بمشكلات الأداء التي يواجهها حساب الضريبة.</span><span class="sxs-lookup"><span data-stu-id="3c34b-104">Sometimes, a transaction is affected by performance issues that tax calculation is having.</span></span> <span data-ttu-id="3c34b-105">لاستكشاف هذه المشكلة وإصلاحها، اتبع الخطوات الواردة في الأقسام التالية عند الضرورة.</span><span class="sxs-lookup"><span data-stu-id="3c34b-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="review-the-transaction-line-count"></a><span data-ttu-id="3c34b-106">راجع عدد بنود الحركة</span><span class="sxs-lookup"><span data-stu-id="3c34b-106">Review the transaction line count</span></span>

<span data-ttu-id="3c34b-107">حدد ما إذا كانت الحركة تحتوي علي عدد كبير من البنود (علي سبيل المثال، أكثر من مئات).</span><span class="sxs-lookup"><span data-stu-id="3c34b-107">Determine whether the transaction has a large number of lines (for example, more than several hundred).</span></span> <span data-ttu-id="3c34b-108">وإذا لم يكن موجودا، فقم بالانتقال إلى القسم التالي.</span><span class="sxs-lookup"><span data-stu-id="3c34b-108">If it doesn't, move on to the next section.</span></span> <span data-ttu-id="3c34b-109">إذا كان للحركة عده بنود مئات، قم بتاخير حساب الضريبة.</span><span class="sxs-lookup"><span data-stu-id="3c34b-109">If the transaction does have several hundred lines, delay the tax calculation.</span></span> <span data-ttu-id="3c34b-110">لمزيد من المعلومات، راجع [تمكين حساب الضريبة المؤجلة على دفاتر اليومية](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="3c34b-110">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span> 

<span data-ttu-id="3c34b-111">بعد ذلك، يمكنك تحديد ما إذا كان سيتم استيفاء اي من الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="3c34b-111">Next, you can determine whether any of the following conditions are met:</span></span>

- <span data-ttu-id="3c34b-112">هناك حركات مستورده من ملفات كبيره.</span><span class="sxs-lookup"><span data-stu-id="3c34b-112">There are import transactions from large files.</span></span>
- <span data-ttu-id="3c34b-113">وتعالج جلسات العمل المتعددة نفس حساب ضريبة الحركة في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="3c34b-113">Multiple sessions process the same transaction tax calculation at the same time.</span></span>
- <span data-ttu-id="3c34b-114">تحتوي الحركة علي عده بنود، ويتم تحديث طرق العرض في الوقت الحقيقي.</span><span class="sxs-lookup"><span data-stu-id="3c34b-114">The transaction has multiple lines, and the views are updated in real time.</span></span> <span data-ttu-id="3c34b-115">على سبيل المثال، يتم تحديث حقل **مبلغ ضريبة المبيعات المحسوب** في صفحة **دفتر اليومية العام** في الوقت الفعلي عند تغيير حقول البند.</span><span class="sxs-lookup"><span data-stu-id="3c34b-115">For example, the **Calculated sales tax amount** field on the **General journal** page is updated in real time when a line's fields are changed.</span></span>

   <span data-ttu-id="3c34b-116">[![حساب حقل مبلغ ضريبة المبيعات في صفحة إيصال دفتر اليومية](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="3c34b-116">[![Calculated sales tax amount field on the Jounal voucher page](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span></span>

<span data-ttu-id="3c34b-117">في حاله استيفاء اي من هذه الشروط، قم بتاخير حساب الضريبة.</span><span class="sxs-lookup"><span data-stu-id="3c34b-117">If any of these conditions are met, delay the tax calculation.</span></span>

## <a name="review-the-call-stack"></a><span data-ttu-id="3c34b-118">مراجعه مكدس الاستدعاءات</span><span class="sxs-lookup"><span data-stu-id="3c34b-118">Review the call stack</span></span>

<span data-ttu-id="3c34b-119">قم بمراجعه مكدس الاستدعاءات لتحديد ما إذا كان سيتم استدعاء حساب الضريبة عده مرات.</span><span class="sxs-lookup"><span data-stu-id="3c34b-119">Review the call stack to determine whether tax calculation is called multiple times.</span></span> <span data-ttu-id="3c34b-120">وإذا لم يكن موجودا، فقم بالانتقال إلى القسم التالي.</span><span class="sxs-lookup"><span data-stu-id="3c34b-120">If it isn't, move on to the next section.</span></span> <span data-ttu-id="3c34b-121">إذا تم استدعاء مكدس الاستدعاءات عده مرات، اتبع هذه الخطوات للمساعدة في تقليل أوقات حساب الضريبة.</span><span class="sxs-lookup"><span data-stu-id="3c34b-121">If the call stack is called multiple times, follow these steps to help reduce the tax calculation times.</span></span>

1. <span data-ttu-id="3c34b-122">إذا كان دفتر اليومية يعتبر الحركة، فقم بتاخير حساب الضريبة.</span><span class="sxs-lookup"><span data-stu-id="3c34b-122">If the journal has considered the transaction, delay the tax calculation.</span></span> <span data-ttu-id="3c34b-123">لمزيد من المعلومات، راجع [تمكين حساب الضريبة المؤجلة على دفاتر اليومية](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="3c34b-123">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span>
2. <span data-ttu-id="3c34b-124">إذا كانت المعاملة عبارة عن أمر شراء، وكان إصدار التطبيق أحدث من 10.0.15، فيمكنك تأخير حساب الضريبة حتى الحساب النهائي عن طريق تمكين الطيران لـ **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span><span class="sxs-lookup"><span data-stu-id="3c34b-124">If the transaction is a purchase order, and the application version is later than 10.0.15, you can delay the tax calculation until the final calculation by enabling the flighting for **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span></span>

## <a name="review-the-call-stack-timeline"></a><span data-ttu-id="3c34b-125">مراجعه جدول زمني مكدس الاستدعاءات</span><span class="sxs-lookup"><span data-stu-id="3c34b-125">Review the call stack timeline</span></span>

<span data-ttu-id="3c34b-126">قم بمراجعه المخطط الزمني لمكدس الاستدعاءات لتحديد ما إذا كانت المشاكل التالية موجودة ام لا.</span><span class="sxs-lookup"><span data-stu-id="3c34b-126">Review the call stack timeline to determine whether the following issues exist.</span></span> <span data-ttu-id="3c34b-127">إذا فعلوا ذلك، قم بتمكين الطيران لـ **TaxUncommittedDoIsolateScopeFlighting** لحل المشكلة.</span><span class="sxs-lookup"><span data-stu-id="3c34b-127">If they do, enable the flighting for **TaxUncommittedDoIsolateScopeFlighting** to fix the issue.</span></span>

- <span data-ttu-id="3c34b-128">تؤدي الحركة إلى توقف النظام عن الاستجابة حتى تنتهي الجلسة.</span><span class="sxs-lookup"><span data-stu-id="3c34b-128">The transaction causes the system to stop responding until the session ends.</span></span> <span data-ttu-id="3c34b-129">التالي، لا يمكن للحركة ان تحسب نتيجة الضريبة.</span><span class="sxs-lookup"><span data-stu-id="3c34b-129">Therefore, the transaction can't calculate the tax result.</span></span> <span data-ttu-id="3c34b-130">يبين الرسم التوضيحي التالي مربع الرسالة "تم إنهاء الجلسة" والذي تتلقاه.</span><span class="sxs-lookup"><span data-stu-id="3c34b-130">The following illustration shows the "Session ended" message box that you receive.</span></span>

    <span data-ttu-id="3c34b-131">[![رسالة انتهاء جلسة العمل](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="3c34b-131">[![Session ended message](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span></span>

- <span data-ttu-id="3c34b-132">تستغرق أساليب **TaxUncommitted** وقت أطول من الطرق الأخرى.</span><span class="sxs-lookup"><span data-stu-id="3c34b-132">The **TaxUncommitted** methods take more time than other methods.</span></span> <span data-ttu-id="3c34b-133">على سبيل المثال، في الرسم التوضيحي التالي، فإن أسلوب **TaxUncommitted::updateTaxUncommitted()** تستغرق 43347.42 ثانية، لكن الطرق الأخرى تستغرق 0.09 ثانية.</span><span class="sxs-lookup"><span data-stu-id="3c34b-133">For example, in the following illustration, the **TaxUncommitted::updateTaxUncommitted()** method takes 43,347.42 seconds, but other methods take 0.09 seconds.</span></span>

    <span data-ttu-id="3c34b-134">[![مدد الأساليب](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="3c34b-134">[![Method durations](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span></span>

## <a name="customizing-and-calling-tax-calculation"></a><span data-ttu-id="3c34b-135">تخصيص واستدعاء حساب الضريبة</span><span class="sxs-lookup"><span data-stu-id="3c34b-135">Customizing and calling tax calculation</span></span>

<span data-ttu-id="3c34b-136">عند التخصيص، لا تستدعي حساب الضرائب في أسلوب **insert()** أو **update()** لكل بند.</span><span class="sxs-lookup"><span data-stu-id="3c34b-136">When you customize, don't call tax calculation at the **insert()** or **update()** method for each line.</span></span> <span data-ttu-id="3c34b-137">يجب استدعاء حساب الضريبة على مستوى الحركة.</span><span class="sxs-lookup"><span data-stu-id="3c34b-137">Tax calculation should be called at the transaction level.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="3c34b-138">حدد ما إذا كان التخصيص موجودًا</span><span class="sxs-lookup"><span data-stu-id="3c34b-138">Determine whether customization exists</span></span>

<span data-ttu-id="3c34b-139">إذا كنت قد أكملت الخطوات الواردة في الأقسام السابقة ولكنك لم تجد أي مشكلة، فحدد ما إذا كان التخصيص موجودًا أم لا.</span><span class="sxs-lookup"><span data-stu-id="3c34b-139">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="3c34b-140">في حاله عدم وجود تخصيص، قم بإنشاء طلب خدمه Microsoft لمزيد من الدعم.</span><span class="sxs-lookup"><span data-stu-id="3c34b-140">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
