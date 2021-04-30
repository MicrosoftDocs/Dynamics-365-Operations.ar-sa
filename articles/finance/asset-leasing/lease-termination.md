---
title: اقتراح إنهاء عقد الإيجار
description: يوضح هذا الموضوع كيفية اقتراح إيجار للإنهاء.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseTerminateLeaseListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 6b32f9e8f80827e04269ac8cb6a4fbb5a13af8bc
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881098"
---
# <a name="propose-a-lease-for-termination"></a><span data-ttu-id="bd948-103">اقتراح إيجار للإنهاء</span><span class="sxs-lookup"><span data-stu-id="bd948-103">Propose a lease for termination</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="bd948-104">إذا تم إنهاء الإيجار مبكرًا، يمكن لعقد إيجار الأصل تسجيل إدخال دفتر يومية إنهاء لشطب التزامات الإيجار، وحق استخدام الأصل (ROU)، والإهلاك التراكمي، والحجز بالربح أو الخسارة.</span><span class="sxs-lookup"><span data-stu-id="bd948-104">If a lease is terminated early, Asset leasing can record a termination journal entry to write off the lease liability, right-of-use (ROU) asset, and accumulated depreciation, and book a gain or loss.</span></span> <span data-ttu-id="bd948-105">تقوم عملية الإنهاء المبكر بإنهاء عقد إيجار ودفاتر الإيجار المقترنة به.</span><span class="sxs-lookup"><span data-stu-id="bd948-105">The early termination process terminates a lease and its associated lease books.</span></span> <span data-ttu-id="bd948-106">ولا يتم إنهاء دفاتر الإيجار الفردية.</span><span class="sxs-lookup"><span data-stu-id="bd948-106">It doesn't terminate individual lease books.</span></span> <span data-ttu-id="bd948-107">يصف هذا الموضوع الوظيفة التي تتيح لك اقتراح عقد إيجار للإنهاء ومعالجة إدخال دفتر يومية إنهاء الإيجار.</span><span class="sxs-lookup"><span data-stu-id="bd948-107">This topic describes the functionality that lets you propose a lease for termination and process the lease termination journal entry.</span></span>

<span data-ttu-id="bd948-108">في حاله عدم تصنيف الإيجار كإيجار معاملة إيجار مؤجل وغير مرتبط بأصل ثابت، فإن إيجار الأصل ينشئ دفتر يومية الإنهاء التالي.</span><span class="sxs-lookup"><span data-stu-id="bd948-108">If a lease isn't classified as a deferred rent treatment lease and isn't associated with a fixed asset, Asset leasing produces the following termination journal entry.</span></span>

| <span data-ttu-id="bd948-109">الحركة</span><span class="sxs-lookup"><span data-stu-id="bd948-109">Transaction</span></span>                           | <span data-ttu-id="bd948-110">مدين</span><span class="sxs-lookup"><span data-stu-id="bd948-110">Debit (Dr.)</span></span> | <span data-ttu-id="bd948-111">دائن</span><span class="sxs-lookup"><span data-stu-id="bd948-111">Credit (Cr.)</span></span> |
|---------------------------------------|-------------|--------------|
| <span data-ttu-id="bd948-112">التزامات الإيجار المدينة</span><span class="sxs-lookup"><span data-stu-id="bd948-112">Dr. Lease liability</span></span>                   | <span data-ttu-id="bd948-113">X</span><span class="sxs-lookup"><span data-stu-id="bd948-113">X</span></span>           |              |
| <span data-ttu-id="bd948-114">مدين الإهلاك التراكمي</span><span class="sxs-lookup"><span data-stu-id="bd948-114">Dr. Accumulated depreciation</span></span>          | <span data-ttu-id="bd948-115">X</span><span class="sxs-lookup"><span data-stu-id="bd948-115">X</span></span>           |              |
| <span data-ttu-id="bd948-116">الربح/الخسارة المدينة عند تعديل عقد الإيجار</span><span class="sxs-lookup"><span data-stu-id="bd948-116">Dr. Gain (loss) on lease modification</span></span> | <span data-ttu-id="bd948-117">X</span><span class="sxs-lookup"><span data-stu-id="bd948-117">X</span></span>           |              |
| <span data-ttu-id="bd948-118">أصل الإيجار الدائن</span><span class="sxs-lookup"><span data-stu-id="bd948-118">Cr. Lease asset</span></span>                       |             | <span data-ttu-id="bd948-119">X</span><span class="sxs-lookup"><span data-stu-id="bd948-119">X</span></span>            |
| <span data-ttu-id="bd948-120">الربح/الخسارة الدائنة عند تعديل عقد الإيجار</span><span class="sxs-lookup"><span data-stu-id="bd948-120">Cr. Gain (loss) on lease modification</span></span> |             | <span data-ttu-id="bd948-121">X</span><span class="sxs-lookup"><span data-stu-id="bd948-121">X</span></span>            |

<span data-ttu-id="bd948-122">إذا تم تصنيف دفتر الإيجار كدفتر إيجار مؤجل، يقوم الإدخال بشطف رصيد الإيجار المؤجل قبل إنهاء العمل بحساب الأرباح أو الخسائر، كما هو موضح هنا.</span><span class="sxs-lookup"><span data-stu-id="bd948-122">If the lease book is classified as a deferred rent book, the entry writes off the balance of the deferred rent before the termination to the gain or loss account, as shown here.</span></span>

| <span data-ttu-id="bd948-123">الحركة</span><span class="sxs-lookup"><span data-stu-id="bd948-123">Transaction</span></span>                           | <span data-ttu-id="bd948-124">مدين</span><span class="sxs-lookup"><span data-stu-id="bd948-124">Debit (Dr.)</span></span> | <span data-ttu-id="bd948-125">دائن</span><span class="sxs-lookup"><span data-stu-id="bd948-125">Credit (Cr.)</span></span> | 
|---------------------------------------|-------------|--------------|
| <span data-ttu-id="bd948-126">الإيجار المؤجل المدين</span><span class="sxs-lookup"><span data-stu-id="bd948-126">Dr. Deferred rent</span></span>                     | <span data-ttu-id="bd948-127">X</span><span class="sxs-lookup"><span data-stu-id="bd948-127">X</span></span>           |              |
| <span data-ttu-id="bd948-128">الربح/الخسارة الدائنة عند تعديل عقد الإيجار</span><span class="sxs-lookup"><span data-stu-id="bd948-128">Cr. Gain (loss) on lease modification</span></span> |             | <span data-ttu-id="bd948-129">X</span><span class="sxs-lookup"><span data-stu-id="bd948-129">X</span></span>            |
| <span data-ttu-id="bd948-130">الإيجار المؤجل الدائن</span><span class="sxs-lookup"><span data-stu-id="bd948-130">Cr. Deferred rent</span></span>                     |             | <span data-ttu-id="bd948-131">X</span><span class="sxs-lookup"><span data-stu-id="bd948-131">X</span></span>            |
| <span data-ttu-id="bd948-132">الربح/الخسارة المدينة عند تعديل عقد الإيجار</span><span class="sxs-lookup"><span data-stu-id="bd948-132">Dr. Gain (loss) on lease modification</span></span> | <span data-ttu-id="bd948-133">X</span><span class="sxs-lookup"><span data-stu-id="bd948-133">X</span></span>           |              |

<span data-ttu-id="bd948-134">في حاله اتصال دفتر الإيجار بأصل ثابت، يتم حساب حق استخدام الأصل في الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="bd948-134">If the lease book is connected to a fixed asset, the ROU asset is accounted for in Fixed assets.</span></span> <span data-ttu-id="bd948-135">تتضمن هذه المحاسبة حساب عمليات الإنهاء المبكر.</span><span class="sxs-lookup"><span data-stu-id="bd948-135">This accounting includes the accounting for early terminations.</span></span> <span data-ttu-id="bd948-136">ينتج إيجار الأصول إدخال دفتر اليومية التالي لشطب التزامات الإيجار.</span><span class="sxs-lookup"><span data-stu-id="bd948-136">Asset leasing produces the following journal entry to write off the lease liability.</span></span>

| <span data-ttu-id="bd948-137">الحركة</span><span class="sxs-lookup"><span data-stu-id="bd948-137">Transaction</span></span>                           | <span data-ttu-id="bd948-138">مدين</span><span class="sxs-lookup"><span data-stu-id="bd948-138">Debit (Dr.)</span></span> | <span data-ttu-id="bd948-139">دائن</span><span class="sxs-lookup"><span data-stu-id="bd948-139">Credit (Cr.)</span></span> |
|---------------------------------------|-------------|--------------|
| <span data-ttu-id="bd948-140">التزامات الإيجار المدينة</span><span class="sxs-lookup"><span data-stu-id="bd948-140">Dr. Lease liability</span></span>                   | <span data-ttu-id="bd948-141">X</span><span class="sxs-lookup"><span data-stu-id="bd948-141">X</span></span>           |              |
| <span data-ttu-id="bd948-142">الربح/الخسارة الدائنة عند تعديل عقد الإيجار</span><span class="sxs-lookup"><span data-stu-id="bd948-142">Cr. Gain (loss) on lease modification</span></span> |             | <span data-ttu-id="bd948-143">X</span><span class="sxs-lookup"><span data-stu-id="bd948-143">X</span></span>            |

<span data-ttu-id="bd948-144">للحصول على معلومات حول الطريقة الصحيحة للتخلص من حق استخدام الأصل، راجع [التخلص من أصل ثابت كخردة](../fixed-assets/dispose-of-a-fixed-asset-as-scrap.md).</span><span class="sxs-lookup"><span data-stu-id="bd948-144">For information about the correct way to dispose of an ROU asset, see [Dispose of a fixed asset as scrap](../fixed-assets/dispose-of-a-fixed-asset-as-scrap.md).</span></span>

## <a name="propose-a-lease-for-termination"></a><span data-ttu-id="bd948-145">اقتراح إيجار للإنهاء</span><span class="sxs-lookup"><span data-stu-id="bd948-145">Propose a lease for termination</span></span>

1. <span data-ttu-id="bd948-146">انتقل إلى الإيجار الذي يجب إنهاؤه، ثم، في جزء الإجراء، حدد **اقتراح الإنهاء**.</span><span class="sxs-lookup"><span data-stu-id="bd948-146">Go to the lease that must be terminated, and then, on the Action Pane, select **Termination proposal**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bd948-147">يكون زر **اقتراح الإنهاء** غير متوفرفي حالة وجود أي إدخالات دفتر يومية غير مرحلة مقابل أي دفتر.</span><span class="sxs-lookup"><span data-stu-id="bd948-147">The **Termination proposal** button is unavailable if there are any unposted journal entries against any book.</span></span> <span data-ttu-id="bd948-148">قبل أن تتمكن من إنهاء الإيجار، يجب ترحيل أي إدخالات دفتر يومية تم إنشاؤها مقابل الإيجار أو حذفها.</span><span class="sxs-lookup"><span data-stu-id="bd948-148">Before you can terminate the lease, you must post or delete any journal entries that have been created against the lease.</span></span>

2. <span data-ttu-id="bd948-149">في مربع الحوار الذي يظهر، قم بتعيين حقول **تاريخ السريان** و **تاريخ الترحيل** لإدخال دفتر يومية الإنهاء.</span><span class="sxs-lookup"><span data-stu-id="bd948-149">In the dialog box that appears, set the **Effective date** and **Posting date** fields for the termination journal entry.</span></span>
3. <span data-ttu-id="bd948-150">حدد **اقتراح الإنهاء** لاقتراح الإيجار المراد إنهاؤه.</span><span class="sxs-lookup"><span data-stu-id="bd948-150">Select **Termination proposal** to propose the lease for termination.</span></span>
4. <span data-ttu-id="bd948-151">حدد **ترحيل إنهاء الإيجار** لترحيل إدخال دفتر يومية إنهاء الإيجار تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="bd948-151">Select **Post lease termination** to automatically post the lease termination journal entry.</span></span>
5. <span data-ttu-id="bd948-152">في صفحة **عمليات إنهاء الإيجار**، حدد معرف الإيجار للإيجار الذي تقترح إنهاؤه لعرض بنود الإنهاء.</span><span class="sxs-lookup"><span data-stu-id="bd948-152">On the **Lease terminations** page, select the lease ID of the lease that you proposed for termination to view the termination lines.</span></span> <span data-ttu-id="bd948-153">تعرض بنود الإنهاء قيم الحمل الخاصة بحق استخدام الأصل والتزامات الإيجار ووالإهلاك التراكمي والإيجار المؤجل (إذا كانت معمولا بها) والربح أو الخسارة التي يجب التعرف عليها في إنهاء الإيجار.</span><span class="sxs-lookup"><span data-stu-id="bd948-153">The termination lines show the carrying values of the ROU asset, lease liability, accumulated depreciation, deferred rent (if applicable), and gain or loss that must be recognized on the termination of the lease.</span></span>

<span data-ttu-id="bd948-154">الإيجار جاهز الآن للإنهاء.</span><span class="sxs-lookup"><span data-stu-id="bd948-154">The lease is now ready for termination.</span></span> <span data-ttu-id="bd948-155">تتغير قيمة حقل **حالة الإنهاء** لدفتر الإيجار إلى **جاهز للإنهاء**.</span><span class="sxs-lookup"><span data-stu-id="bd948-155">The value of the **Termination status** field for the lease book is changed to **Ready for termination**.</span></span> <span data-ttu-id="bd948-156">وفي هذه المرحلة، لا يمكن بعد الآن ترحيل إدخالات دفتر اليومية مقابل الإيجار، أو تعديلها أو إعاقتها.</span><span class="sxs-lookup"><span data-stu-id="bd948-156">At this point, you can no longer post journal entries against the lease, or adjust or impair it.</span></span> 

## <a name="process-leases-that-are-ready-for-termination"></a><span data-ttu-id="bd948-157">معالجه الإيجارات الجاهزة للإنهاء</span><span class="sxs-lookup"><span data-stu-id="bd948-157">Process leases that are ready for termination</span></span>

<span data-ttu-id="bd948-158">لمعالجه الإيجارات الجاهزة للإنهاء وترحيل إدخال دفتر يومية الإنهاء، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="bd948-158">To process leases that are ready for termination and post the termination journal entry, follow these steps.</span></span>

1. <span data-ttu-id="bd948-159">في الصفحة **عمليات إنهاء الإيجار**، حدد عقد الإيجار المراد معالجته، ثم حدد **إنهاء**.</span><span class="sxs-lookup"><span data-stu-id="bd948-159">On the **Lease terminations** page, select the lease to process, and then select **Terminate**.</span></span>
2. <span data-ttu-id="bd948-160">في مربع الحوار الذي يظهر، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bd948-160">In the dialog box that appears, select **OK**.</span></span>

<span data-ttu-id="bd948-161">يقوم النظام بترحيل إدخال دفتر يومية الإنهاء.</span><span class="sxs-lookup"><span data-stu-id="bd948-161">The system posts the termination journal entry.</span></span> <span data-ttu-id="bd948-162">يتم تعيين الحقل **حالة الإيجار** لدفتر الإيجار إلى **تم الإنهاء**، وتعيين حقل **حالة اقتراح الإنهاء** إلى **مكتملة**.</span><span class="sxs-lookup"><span data-stu-id="bd948-162">The **Lease status** field for the lease book is set to **Terminated**, and the **Termination proposal status** field is set to **Completed**.</span></span>

## <a name="reverse-a-lease-termination"></a><span data-ttu-id="bd948-163">إلغاء إنهاء الإيجار</span><span class="sxs-lookup"><span data-stu-id="bd948-163">Reverse a lease termination</span></span>

<span data-ttu-id="bd948-164">لإغاء إدخال دفتر يومية إنهاء الإيجار وفتح إيجار تم إنهاؤه، اتبع هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="bd948-164">To reverse a lease termination journal entry and open a terminated lease, follow this step.</span></span>

- <span data-ttu-id="bd948-165">في الصفحة **عمليات إنهاء الإيجار**، حدد عقد الإيجار المنتهي المراد إلغاؤه، ثم حدد **إلغاء الإنهاء**.</span><span class="sxs-lookup"><span data-stu-id="bd948-165">On the **Lease terminations** page, select the terminated lease to reverse, and then select **Reverse termination**.</span></span>

<span data-ttu-id="bd948-166">يقوم النظام بإلغاء إدخال دفتر يومية الإنهاء.</span><span class="sxs-lookup"><span data-stu-id="bd948-166">The system reverses the termination journal entry.</span></span> <span data-ttu-id="bd948-167">يتم تعيين الحقل **حالة الإيجار** لدفتر الإيجار إلى **مفتوح**.</span><span class="sxs-lookup"><span data-stu-id="bd948-167">The **Lease status** field for the lease book is set to **Open**.</span></span> <span data-ttu-id="bd948-168">لم يعد الإيجار معروضًا في صفحة **عمليات إنهاء الإيجار** ويمكن اقتراحه مرة أخرى للإنهاء.</span><span class="sxs-lookup"><span data-stu-id="bd948-168">The lease no longer appears on the **Lease terminations** page and can be proposed again for termination.</span></span>

## <a name="example-of-a-lease-termination"></a><span data-ttu-id="bd948-169">مثال على إنهاء التاجير</span><span class="sxs-lookup"><span data-stu-id="bd948-169">Example of a lease termination</span></span>

<span data-ttu-id="bd948-170">بالنسبة لهذا المثال، اقترن عقد الإيجار بأصل غير مخصص لا يقوم بتحويل ملكية الأصل أو منح المستأجر خيارًا لشراء الأصل.</span><span class="sxs-lookup"><span data-stu-id="bd948-170">For this example, the lease is associated with a non-specialized asset, and it doesn't transfer ownership of the asset or grant the lessee the option to purchase the asset.</span></span>

### <a name="setup"></a><span data-ttu-id="bd948-171">الإعداد</span><span class="sxs-lookup"><span data-stu-id="bd948-171">Setup</span></span>

<span data-ttu-id="bd948-172">توضح الجداول التالية القيم التي يتم تعيينها في علامات التبويب **عام** و **بنود جدول الدفع** لعقد الإيجار المستخدم في المثال.</span><span class="sxs-lookup"><span data-stu-id="bd948-172">The following tables show the values that are set on the **General** and **Payment schedule lines** tabs for the lease that is used in this example.</span></span>

<span data-ttu-id="bd948-173">**علامة التبويب عام**</span><span class="sxs-lookup"><span data-stu-id="bd948-173">**General tab**</span></span>

| <span data-ttu-id="bd948-174">الحقل</span><span class="sxs-lookup"><span data-stu-id="bd948-174">Field</span></span>                      | <span data-ttu-id="bd948-175">قيمة</span><span class="sxs-lookup"><span data-stu-id="bd948-175">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="bd948-176">القيمة العادلة للأصل</span><span class="sxs-lookup"><span data-stu-id="bd948-176">Fair value of the asset</span></span>    | <span data-ttu-id="bd948-177">600,000</span><span class="sxs-lookup"><span data-stu-id="bd948-177">600,000</span></span>          |
| <span data-ttu-id="bd948-178">عملة</span><span class="sxs-lookup"><span data-stu-id="bd948-178">Currency</span></span>                   | <span data-ttu-id="bd948-179">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="bd948-179">USD</span></span>              |
| <span data-ttu-id="bd948-180">التكاليف المباشرة لعقد الإيجار</span><span class="sxs-lookup"><span data-stu-id="bd948-180">Initial direct costs</span></span>       | <span data-ttu-id="bd948-181">1,000</span><span class="sxs-lookup"><span data-stu-id="bd948-181">1,000</span></span>            |
| <span data-ttu-id="bd948-182">سعر الفائدة على الاقتراض الإضافي</span><span class="sxs-lookup"><span data-stu-id="bd948-182">Incremental borrowing rate</span></span> | <span data-ttu-id="bd948-183">7%</span><span class="sxs-lookup"><span data-stu-id="bd948-183">7%</span></span>               |
| <span data-ttu-id="bd948-184">فاصل متراكب</span><span class="sxs-lookup"><span data-stu-id="bd948-184">Compounding interval</span></span>       | <span data-ttu-id="bd948-185">سنويُا</span><span class="sxs-lookup"><span data-stu-id="bd948-185">Annually</span></span>         |
| <span data-ttu-id="bd948-186">العمر الإنتاجي للأصل (أشهر)</span><span class="sxs-lookup"><span data-stu-id="bd948-186">Asset useful life (months)</span></span> | <span data-ttu-id="bd948-187">600</span><span class="sxs-lookup"><span data-stu-id="bd948-187">600</span></span>              |
| <span data-ttu-id="bd948-188">نوع الاستحقاق السنوي</span><span class="sxs-lookup"><span data-stu-id="bd948-188">Annuity type</span></span>               | <span data-ttu-id="bd948-189">الاستحقاق السنوي العادي</span><span class="sxs-lookup"><span data-stu-id="bd948-189">Ordinary annuity</span></span> |
| <span data-ttu-id="bd948-190">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="bd948-190">Commencement date</span></span>          | <span data-ttu-id="bd948-191">1/1/2019</span><span class="sxs-lookup"><span data-stu-id="bd948-191">1/1/2019</span></span>         |

<span data-ttu-id="bd948-192">**علامة التبويب بنود جدول الدفع**</span><span class="sxs-lookup"><span data-stu-id="bd948-192">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="bd948-193">الحقل</span><span class="sxs-lookup"><span data-stu-id="bd948-193">Field</span></span>             | <span data-ttu-id="bd948-194">قيمة</span><span class="sxs-lookup"><span data-stu-id="bd948-194">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="bd948-195">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="bd948-195">Start date</span></span>        | <span data-ttu-id="bd948-196">1/1/2019</span><span class="sxs-lookup"><span data-stu-id="bd948-196">1/1/2019</span></span>   |
| <span data-ttu-id="bd948-197">الفترة الزمنية</span><span class="sxs-lookup"><span data-stu-id="bd948-197">Period interval</span></span>   | <span data-ttu-id="bd948-198">شهري</span><span class="sxs-lookup"><span data-stu-id="bd948-198">Monthly</span></span>    |
| <span data-ttu-id="bd948-199">الفترات</span><span class="sxs-lookup"><span data-stu-id="bd948-199">Periods</span></span>           | <span data-ttu-id="bd948-200">120</span><span class="sxs-lookup"><span data-stu-id="bd948-200">120</span></span>        |
| <span data-ttu-id="bd948-201">تاريخ الانتهاء</span><span class="sxs-lookup"><span data-stu-id="bd948-201">End date</span></span>          | <span data-ttu-id="bd948-202">12/31/2028</span><span class="sxs-lookup"><span data-stu-id="bd948-202">12/31/2028</span></span> |
| <span data-ttu-id="bd948-203">تكرار الدفع</span><span class="sxs-lookup"><span data-stu-id="bd948-203">Payment frequency</span></span> | <span data-ttu-id="bd948-204">سنويُا</span><span class="sxs-lookup"><span data-stu-id="bd948-204">Annually</span></span>   |
| <span data-ttu-id="bd948-205">مبلغ الدفع</span><span class="sxs-lookup"><span data-stu-id="bd948-205">Payment amount</span></span>    | <span data-ttu-id="bd948-206">10,000</span><span class="sxs-lookup"><span data-stu-id="bd948-206">10,000</span></span>     |

### <a name="steps-for-terminating-the-lease"></a><span data-ttu-id="bd948-207">خطوات إنهاء الإيجار</span><span class="sxs-lookup"><span data-stu-id="bd948-207">Steps for terminating the lease</span></span>

1. <span data-ttu-id="bd948-208">بعد إنشاء عقد الإيجار كما هو موضح سابقًا في هذا الموضوع، انتقل إلى دفتر الإيجار، وقم بتأكيد جدول الدفع.</span><span class="sxs-lookup"><span data-stu-id="bd948-208">After you create the lease as described earlier in this topic, go to the lease book, and confirm the payment schedule.</span></span> <span data-ttu-id="bd948-209">ثم قم بترحيل إدخال دفتر يومية التقييم الأولي.</span><span class="sxs-lookup"><span data-stu-id="bd948-209">Then post the initial recognition journal entry.</span></span> <span data-ttu-id="bd948-210">يجب أن يكون حق استخدام الأصل الأولي 71,235.81 دولار، والتزامات الإيجار 70.235.81 دولار.</span><span class="sxs-lookup"><span data-stu-id="bd948-210">The initial ROU asset is $71,235.81, and lease liability should be $70,235.81.</span></span> <span data-ttu-id="bd948-211">بالنسبة لهذا المثال، تم تصنيف عقد الإيجار كعقد إيجار تشغيلي تحت موضوع صياغة مقاييس المحاسبية (ASC 842).</span><span class="sxs-lookup"><span data-stu-id="bd948-211">For this example, the lease was classified as an operating lease under Accounting Standards Codification Topic 842 (ASC 842).</span></span>
2. <span data-ttu-id="bd948-212">قم بتشغيل عملية دفتر يومية الدُفعة ثلاث مرات لمحاكاة فترة السنوات الثلاث لدفعات الإيجار ونفقات الفوائد ونفقات الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="bd948-212">Run the batch journal process three times to simulate the passage of three years for the lease payments, interest expenses, and depreciation expenses.</span></span>
3. <span data-ttu-id="bd948-213">بعد الانتهاء من تشغيل كافة وظائف الدُفعات الثلاث، ارجع إلى دفتر الإيجار، ثم افتح جداول حركات الالتزام والأصول لعرض قيمة الحمل الحالية الخاصة بحق استخدام الأصل والتزامات الإيجار.</span><span class="sxs-lookup"><span data-stu-id="bd948-213">After you've finished running all three batch jobs, go back to the lease book, and open the Liability and Asset transactions tables to view the current carrying value of the ROU asset and lease liability.</span></span> <span data-ttu-id="bd948-214">بعد ثلاث سنوات، يجب أن تكون قيمة المسؤولية هي -53,893.00 دولار تقريبًا، ويجب أن تكون قيمة الأصل 54,593.00 دولار تقريبًا.</span><span class="sxs-lookup"><span data-stu-id="bd948-214">After three years, the value of the liability should be approximately $-53,893.00, and the value of the asset should be approximately $54,593.00.</span></span>

    <span data-ttu-id="bd948-215">بعد مرور الثلاث سنوات، توافق الشركة والمؤجر بشكل متبادل على إنهاء الإيجار.</span><span class="sxs-lookup"><span data-stu-id="bd948-215">After the three years have passed, the business and lessor mutually agree to terminate the lease.</span></span> <span data-ttu-id="bd948-216">ولذلك، يجب أن تقوم الآن بإنهاء الإيجار.</span><span class="sxs-lookup"><span data-stu-id="bd948-216">Therefore, you must now terminate the lease.</span></span>

4. <span data-ttu-id="bd948-217">انتقل إلى الإيجار الذي يجب إنهاؤه، ثم، في جزء الإجراء، حدد **اقتراح الإنهاء**.</span><span class="sxs-lookup"><span data-stu-id="bd948-217">Go to the lease that must be terminated, and then, on the Action Pane, select **Termination proposal**.</span></span> 
5. <span data-ttu-id="bd948-218">في مربع الحوار الذي يظهر، في حقل **تاريخ السريان** و **تاريخ الترحيل**، أدخل **1/1/2021**.</span><span class="sxs-lookup"><span data-stu-id="bd948-218">In the dialog box that appears, in the **Effective date** and **Posting date** field, enter **1/1/2021**.</span></span>
6. <span data-ttu-id="bd948-219">حدد **اقتراح الإنهاء** لاقتراح الإيجار المراد إنهاؤه.</span><span class="sxs-lookup"><span data-stu-id="bd948-219">Select **Termination proposal** to propose the lease for termination.</span></span>

    <span data-ttu-id="bd948-220">تظهر صفحة **عمليات إنهاء الإيجار** وتعرض الإيجار الذي سيتم إنهاؤه.</span><span class="sxs-lookup"><span data-stu-id="bd948-220">The **Lease terminations** page appears and shows the lease that will be terminated.</span></span>

7. <span data-ttu-id="bd948-221">لعرض بنود الإنهاء، حدد معرف الإيجار للإيجار الذي تقترح إنهاؤه.</span><span class="sxs-lookup"><span data-stu-id="bd948-221">To view the termination lines, select the lease ID of the lease that you proposed for termination.</span></span> <span data-ttu-id="bd948-222">تعرض بنود الإنهاء قيم الحمل للإيجار.</span><span class="sxs-lookup"><span data-stu-id="bd948-222">The termination lines show the carrying values of the lease.</span></span> <span data-ttu-id="bd948-223">يوضح الجدول التالي القيم التي يجب أن تكون لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="bd948-223">The following table shows what these values should be for this example.</span></span> 

    | <span data-ttu-id="bd948-224">الحقل</span><span class="sxs-lookup"><span data-stu-id="bd948-224">Field</span></span>                                                 | <span data-ttu-id="bd948-225">قيمة</span><span class="sxs-lookup"><span data-stu-id="bd948-225">Value</span></span>      |
    |-------------------------------------------------------|------------|
    | <span data-ttu-id="bd948-226">الاحتفاظ برصيد الالتزام بعملة الحركة</span><span class="sxs-lookup"><span data-stu-id="bd948-226">Carrying balance of liability in transaction currency</span></span> | <span data-ttu-id="bd948-227">53,892.89 دولار</span><span class="sxs-lookup"><span data-stu-id="bd948-227">$53,892.89</span></span> |
    | <span data-ttu-id="bd948-228">حق استخدام الأصل بعمله الحركة</span><span class="sxs-lookup"><span data-stu-id="bd948-228">Right-of-use asset in transaction currency</span></span>            | <span data-ttu-id="bd948-229">71,235.81 دولار</span><span class="sxs-lookup"><span data-stu-id="bd948-229">$71,235.81</span></span> |
    | <span data-ttu-id="bd948-230">الإهلاك التراكمي بعملة الحركة</span><span class="sxs-lookup"><span data-stu-id="bd948-230">Accumulated depreciation in transaction currency</span></span>      | <span data-ttu-id="bd948-231">16,642.92 دولار</span><span class="sxs-lookup"><span data-stu-id="bd948-231">$16,642.92</span></span> |
    | <span data-ttu-id="bd948-232">المكسب (الخسارة) بعملة الحركة</span><span class="sxs-lookup"><span data-stu-id="bd948-232">Gain (loss) in transaction currency</span></span>                   | <span data-ttu-id="bd948-233">-700.00 دولار</span><span class="sxs-lookup"><span data-stu-id="bd948-233">$-700.00</span></span>   |

8. <span data-ttu-id="bd948-234">لترحيل إدخال دفتر يومية الإنهاء، حدد الإيجار في صفحة **عمليات إنهاء الإيجار**، ثم حدد **إنهاء**.</span><span class="sxs-lookup"><span data-stu-id="bd948-234">To post the termination journal entry, select the lease on the **Lease terminations** page, and then select **Terminate**.</span></span>
9. <span data-ttu-id="bd948-235">في مربع الحوار الذي يظهر، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bd948-235">In the dialog box that appears, select **OK**.</span></span>
10. <span data-ttu-id="bd948-236">لعرض إدخال دفتر يومية الإنهاء الذي تم إنشاؤه وترحيله، انتقل إلى دفتر يومية إيجار الأصل في دفتر الإيجار.</span><span class="sxs-lookup"><span data-stu-id="bd948-236">To view the termination journal entry that has been created and posted, go to the asset's leasing journal in the lease book.</span></span> <span data-ttu-id="bd948-237">يوضح الجدول التالي القيم التي يجب أن يظهر بها هذا الإدخال في هذا المثال.</span><span class="sxs-lookup"><span data-stu-id="bd948-237">The following table shows what this entry should look like for this example.</span></span>

    | <span data-ttu-id="bd948-238">الحركة</span><span class="sxs-lookup"><span data-stu-id="bd948-238">Transaction</span></span>                           | <span data-ttu-id="bd948-239">مدين</span><span class="sxs-lookup"><span data-stu-id="bd948-239">Debit (Dr.)</span></span> | <span data-ttu-id="bd948-240">دائن</span><span class="sxs-lookup"><span data-stu-id="bd948-240">Credit (Cr.)</span></span> |
    |---------------------------------------|-------------|--------------|
    | <span data-ttu-id="bd948-241">التزامات الإيجار المدينة</span><span class="sxs-lookup"><span data-stu-id="bd948-241">Dr. Lease liability</span></span>                   | <span data-ttu-id="bd948-242">53,892.89</span><span class="sxs-lookup"><span data-stu-id="bd948-242">53,892.89</span></span>   |              |
    | <span data-ttu-id="bd948-243">مدين الإهلاك التراكمي</span><span class="sxs-lookup"><span data-stu-id="bd948-243">Dr. Accumulated depreciation</span></span>          | <span data-ttu-id="bd948-244">16,642.92</span><span class="sxs-lookup"><span data-stu-id="bd948-244">16,642.92</span></span>   |              |
    | <span data-ttu-id="bd948-245">الربح/الخسارة المدينة عند تعديل عقد الإيجار</span><span class="sxs-lookup"><span data-stu-id="bd948-245">Dr. Gain (loss) on lease modification</span></span> | <span data-ttu-id="bd948-246">700.00</span><span class="sxs-lookup"><span data-stu-id="bd948-246">700.00</span></span>      |              |
    | <span data-ttu-id="bd948-247">أصل الإيجار الدائن</span><span class="sxs-lookup"><span data-stu-id="bd948-247">Cr. Lease asset</span></span>                       |             | <span data-ttu-id="bd948-248">71,235.81</span><span class="sxs-lookup"><span data-stu-id="bd948-248">71,235.81</span></span>    |

11. <span data-ttu-id="bd948-249">لعرض التأثير الصافي للإنهاء، حيث يكون حق استخدام الأصل التزامات الإيجار 0 (صفر)، افتح جداول حركات الالتزامات والأصول.</span><span class="sxs-lookup"><span data-stu-id="bd948-249">To view the net effect of the termination, where the ROU asset and lease liability will be 0 (zero), open the Liability and Asset transactions tables.</span></span>

<span data-ttu-id="bd948-250">يجب أن تكون حالة الإيجار الآن **تم إنهاؤه**.</span><span class="sxs-lookup"><span data-stu-id="bd948-250">The lease status should now be **Terminated**.</span></span> <span data-ttu-id="bd948-251">لن يتم ترحيل أي إدخالات إضافيه لدفتر اليومية مقابل هذا الإيجار إلا إذا تم إلغاء الإنهاء.</span><span class="sxs-lookup"><span data-stu-id="bd948-251">No additional journal entries will be posted against this lease unless the termination is reversed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
