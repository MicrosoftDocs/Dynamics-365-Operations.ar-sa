---
title: إضافة عقود الإيجار أو نسخها (المعاينة)
description: يصف هذا الموضوع كيفية إنشاء عقد إيجار جديد عن طريق إدخال معلومات له في معلومات تأجير الأصل أو نسخه من عقد إيجار موجود.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: abbf04d009a4b347792cd8b317e334da2a4cbbee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969593"
---
# <a name="add-or-copy-leases-preview"></a><span data-ttu-id="57613-103">إضافة عقود الإيجار أو نسخها (المعاينة)</span><span class="sxs-lookup"><span data-stu-id="57613-103">Add or copy leases (Preview)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57613-104">يشرح هذا الموضوع كيفية إنشاء عقد إيجار من البداية في تأجير الأصول، وكذلك كيفية إنشاء عقد إيجار عن طريق نسخ عقد إيجار موجود.</span><span class="sxs-lookup"><span data-stu-id="57613-104">This topic explains how to create a lease from scratch in Asset leasing, and also how to create a lease by copying an existing lease.</span></span> <span data-ttu-id="57613-105">تتضمن عملية إنشاء عقد إيجار من البداية إدخال المعلومات لعقد الإجار الجديد ثم إنشاء جدول عقد إيجار.</span><span class="sxs-lookup"><span data-stu-id="57613-105">The process for creating a lease from scratch involves entering information for the new lease and then creating a lease schedule.</span></span> <span data-ttu-id="57613-106">بعد أن يتم إعداد عقد إيجار واحد على الأقل، قد تجد أنه من الأسهل نسخ المعلومات من عقد إيجار موجود ومن ثم تحرير تلك المعلومات عندما تطلب إنشاء عقد إيجار جديد.</span><span class="sxs-lookup"><span data-stu-id="57613-106">After at least one lease has been set up, you might find it easier to copy the information from an existing lease and then edit that information as you require to create a new lease.</span></span>

## <a name="create-a-lease"></a><span data-ttu-id="57613-107">إنشاء عقد إيجار</span><span class="sxs-lookup"><span data-stu-id="57613-107">Create a lease</span></span>

<span data-ttu-id="57613-108">اتبع الخطوات التالية لإنشاء عقد إيجار في تأجير الأصل.</span><span class="sxs-lookup"><span data-stu-id="57613-108">Follow these steps to create a lease in Asset leasing.</span></span>

1. <span data-ttu-id="57613-109">في صفحة **ملخص عقد الإيجار**، في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="57613-109">On the **Lease summary** page, on the Action Pane, select **New**.</span></span>
2. <span data-ttu-id="57613-110">أدخل معلومات عقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="57613-110">Enter the lease information.</span></span> <span data-ttu-id="57613-111">الحقول المطلوبة يكون لها حدود حمراء.</span><span class="sxs-lookup"><span data-stu-id="57613-111">Fields that are required have red borders.</span></span>

## <a name="create-a-lease-schedule"></a><span data-ttu-id="57613-112">إنشاء جدول عقد إيجار</span><span class="sxs-lookup"><span data-stu-id="57613-112">Create a lease schedule</span></span>

<span data-ttu-id="57613-113">بعد الانتهاء من إدخال المعلومات الخاصة بعقد الإيجار، اتبع الخطوات التالية لإنشاء جدول عقد إيجار.</span><span class="sxs-lookup"><span data-stu-id="57613-113">After you've finished entering information for the lease, follow these steps to create a lease schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="57613-114">قد تتغير الأبعاد المالية استنادًا إلى أية أبعاد مالية مخصصة.</span><span class="sxs-lookup"><span data-stu-id="57613-114">The financial dimensions might change based on any custom financial dimensions.</span></span>

1. <span data-ttu-id="57613-115">حدد **إنشاء جداول** لإنشاء دفاتر عقود الإيجار.</span><span class="sxs-lookup"><span data-stu-id="57613-115">Select **Create schedules** to generate the lease books.</span></span> <span data-ttu-id="57613-116">تتضمن دفاتر عقود الإيجار جداول الدفع وإطفاء الدين والإهلاك والمصروفات.</span><span class="sxs-lookup"><span data-stu-id="57613-116">The lease books include the payment, amortization, depreciation, and expense schedules.</span></span>
2. <span data-ttu-id="57613-117">للوصول إلى دفاتر عقود الإيجار وعرض الجداول التي تم إنشاؤها حديثًا، حدد علامة التبويب **الدفاتر**.</span><span class="sxs-lookup"><span data-stu-id="57613-117">To access the lease books and view the newly created schedules, select the **Books** tab.</span></span>

    <span data-ttu-id="57613-118">تظهر صفحة **تفاصيل الدفاتر** كيفية حساب عقود الإيجار بواسطة الدفاتر التي تم تخصيصها له.</span><span class="sxs-lookup"><span data-stu-id="57613-118">The **Book details** page shows how the lease is accounted for by the books that have been allocated to it.</span></span> <span data-ttu-id="57613-119">من هنا، يمكنك عرض جداول عقود الإيجار.</span><span class="sxs-lookup"><span data-stu-id="57613-119">From here, you can view the lease schedules.</span></span>

    <span data-ttu-id="57613-120">يحتوي جدول الدفع على الإدخالات من علامة التبويب **‏‫بنود جدول الدفع‬** في الصفحة **إضافة عقد إيجار**.</span><span class="sxs-lookup"><span data-stu-id="57613-120">The payment schedule contains the inputs from the **Payment schedule lines** tab on the **Add lease** page.</span></span> <span data-ttu-id="57613-121">لا يزال بإمكانك تغيير كل مبلغ دفع ودفع متغير.</span><span class="sxs-lookup"><span data-stu-id="57613-121">You can still change each payment amount and variable payment.</span></span> <span data-ttu-id="57613-122">يتم حساب التزامات الإيجار استنادًا إلى جدول الدفع المعدل.</span><span class="sxs-lookup"><span data-stu-id="57613-122">The lease liability is calculated based on the modified payment schedule.</span></span>

4. <span data-ttu-id="57613-123">بعد الانتهاء من مراجعة جدول الدفع، حدد **تأكيد الجدول**.</span><span class="sxs-lookup"><span data-stu-id="57613-123">After you've finished reviewing the payment schedule, select **Confirm schedule**.</span></span> <span data-ttu-id="57613-124">بعد تأكيد الجدول، تصبح عقود الإيجار غير متوفرة لتحريرها.</span><span class="sxs-lookup"><span data-stu-id="57613-124">After the schedule is confirmed, the lease is no longer available for editing.</span></span>

    > [!NOTE]
    > <span data-ttu-id="57613-125">يقوم النظام تلقائيًا بحساب فترة الإيجار من بنود جدول الدفع على **الصفحة إضافة عقد الإيجار**.</span><span class="sxs-lookup"><span data-stu-id="57613-125">The system automatically calculates the lease term from the payment schedule lines on the **Add lease** page.</span></span>
    >
    > <span data-ttu-id="57613-126">لحساب فترة الإيجار بالشهور، يعثر النظام على الفرق بين تاريخ البدء وتاريخ الانتهاء لبند جدول دفع معين.</span><span class="sxs-lookup"><span data-stu-id="57613-126">To calculate the lease term in months, the system finds the difference between the start date and the end date for a specific payment schedule line.</span></span> <span data-ttu-id="57613-127">ثم ينتقل إلى بند جدول الدفع التالي ويبحث عن الفرق مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="57613-127">It then moves to the next payment schedule line and finds the difference again.</span></span> <span data-ttu-id="57613-128">وأخيرًا، يقوم النظام بجمع كافة المبالغ لتحديد شرط فترة الإيجار بالشهور.</span><span class="sxs-lookup"><span data-stu-id="57613-128">Finally, the system sums all the amounts to determine the lease term in months.</span></span>

5. <span data-ttu-id="57613-129">لعرض نفقات فوائد الفترة المحسوبة، افتح الصفحة **جدول إطفاء الدين للالتزام**.</span><span class="sxs-lookup"><span data-stu-id="57613-129">To view the calculated period interest expenses, open the **Liability amortization schedule** page.</span></span> <span data-ttu-id="57613-130">لعرض إهلاك القسط الثابت المحسوب، افتح الصفحة **جدول إهلاك الأصول**.</span><span class="sxs-lookup"><span data-stu-id="57613-130">To view calculated straight-line depreciation, open the **Asset depreciation schedule** page.</span></span>
6. <span data-ttu-id="57613-131">بعد الانتهاء من مراجعة المبلغ المحسوب، فإنه يمكنك إنشاء إدخال دفتر يومية التقييم الأولي في صفحة **التعرف المبدئي**.</span><span class="sxs-lookup"><span data-stu-id="57613-131">After you've finished reviewing the calculated amount, you can create the initial recognition journal entry on the **Initial recognition** page.</span></span> <span data-ttu-id="57613-132">تظهر رسالة توضح أنه قد تم إنشاء دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="57613-132">You receive a message that states that the journal has been created.</span></span>

    > [!NOTE]
    > <span data-ttu-id="57613-133">لا يتم ترحيل إدخال دفتر اليومية إلى دفتر الأستاذ العام حتى تقوم بترحيل الإدخال يدويًا.</span><span class="sxs-lookup"><span data-stu-id="57613-133">The journal entry isn't posted to General ledger until you manually post the entry.</span></span>

7. <span data-ttu-id="57613-134">لمراجعة إدخال التقييم الأولي المقترح قبل ترحيله، حدد **دفتر يومية تأجير الأصول**.</span><span class="sxs-lookup"><span data-stu-id="57613-134">To review the proposed initial recognition entry before you post it, select **Asset leasing journal**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="57613-135">لا يمكن إنشاء دفتر يومية تأجير الأصول يدويًا.</span><span class="sxs-lookup"><span data-stu-id="57613-135">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="57613-136">ويتم إنشاؤه تلقائيًا عند إنشاء جداول عقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="57613-136">It's automatically created when lease schedules are created.</span></span>

8. <span data-ttu-id="57613-137">عند الانتهاء من مراجعة إدخال دفتر يومية التقييم المبدئي وتجهيزه لترحيله، حدد **ترحيل** للتعرف على أصل حق استخدام الأصل (ROU) والتزامات الإيجار في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="57613-137">When you've finished reviewing the initial recognition journal entry and are ready to post it, select **Post** to recognize the right-of-use (ROU) asset and lease liability in General ledger.</span></span>

## <a name="copy-a-lease"></a><span data-ttu-id="57613-138">نسخ عقد الإيجار</span><span class="sxs-lookup"><span data-stu-id="57613-138">Copy a lease</span></span>

<span data-ttu-id="57613-139">يتيح لك تأجير الأصل نسخ تفاصيل عقد الإيجار لإنشاء عقد إيجار جديد له المعلومات نفسها.</span><span class="sxs-lookup"><span data-stu-id="57613-139">Asset leasing lets you copy the details of a lease to create a new lease that has the same information.</span></span> <span data-ttu-id="57613-140">يمكنك بعد ذلك تغيير حقول عقد الإيجار قبل إنشاء الجداول لعقد الإيجار المنسوخ.</span><span class="sxs-lookup"><span data-stu-id="57613-140">You can then change the lease fields before you create the schedules for the copied lease.</span></span>

1. <span data-ttu-id="57613-141">في الصفحة **ملخص عقد الإيجار**، حدد عقد الإيجار المراد نفسه، ثم، في جزء الإجراء، حدد **نسخ عقد الإيجار**.</span><span class="sxs-lookup"><span data-stu-id="57613-141">On the **Lease summary** page, select the lease to copy, and then, on the Action Pane, select **Copy lease**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="57613-142">في حالة إيقاف تشغيل المعلمة **يدوي** للتسلسل الرقمي لمعرفات عقد الإيجار، فإنه يتم إنشاء الرقم التالي في التسلسل تلقائيًا كمعرف عقد الإيجار لعقد الإيجار المنسوخ.</span><span class="sxs-lookup"><span data-stu-id="57613-142">If the **Manual** parameter is turned off for the number sequence for lease IDs, the next number in the sequence is automatically generated as the lease ID of the copied lease.</span></span> <span data-ttu-id="57613-143">في حالة تشغيل المعلمة **يدوي**، فإنك تستلم رسالة تطالبك بإدخال معرف عقد الإيجار قبل متابعة نسخ عقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="57613-143">If the **Manual** parameter is turned on, you receive a message that prompts you to enter the lease ID before you proceed to copy the lease.</span></span>

2. <span data-ttu-id="57613-144">حدد **نسخ**.</span><span class="sxs-lookup"><span data-stu-id="57613-144">Select **Copy**.</span></span> <span data-ttu-id="57613-145">يتم نسخ تفاصيل عقد الإيجار من عقد الإيجار المحدد إلى عقد إيجار جديد.</span><span class="sxs-lookup"><span data-stu-id="57613-145">The lease details from the selected lease are copied to a new lease.</span></span> <span data-ttu-id="57613-146">يمكنك بعد ذلك تحرير تفاصيل عقد الإيجار الجديد قبل حفظه وإنشاء جداول عقود الإيجار.</span><span class="sxs-lookup"><span data-stu-id="57613-146">You can then edit the details of the new lease before you save it and create the lease schedules.</span></span>

## <a name="asset-leasing-journal"></a><span data-ttu-id="57613-147">دفتر يومية تأجير الأصول</span><span class="sxs-lookup"><span data-stu-id="57613-147">Asset leasing journal</span></span>

<span data-ttu-id="57613-148">يتم تضمين كافة إدخالات دفتر اليومية التي تم إنشاؤها في تأجير الأصول في دفتر يومية تأجير الأصول.</span><span class="sxs-lookup"><span data-stu-id="57613-148">All journal entries that are created in Asset leasing are contained in the Asset leasing journal.</span></span> <span data-ttu-id="57613-149">في الصفحة **دفتر يومية تأجير الأصول** (**تأجير الأصول \> إدخالات دفتر اليومية \> دفتر يومية تأجير الأصول**)، فإنه يمكنك التصفية عن طريق حالة الترحيل وعرض إدخالات دفتر اليومية المحددة والإيصالات ونشر إدخالات دفتر اليومية غير المنشورة.</span><span class="sxs-lookup"><span data-stu-id="57613-149">On the **Asset leasing journal** page (**Asset leasing \> Journal entries \> Asset leasing journal**), you can filter by posting status, view specific journal entries and the vouchers, and post unposted journal entries.</span></span>

> [!NOTE]
> <span data-ttu-id="57613-150">لا يمكن إنشاء دفتر يومية تأجير الأصول يدويًا.</span><span class="sxs-lookup"><span data-stu-id="57613-150">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="57613-151">ويتم إنشاؤه تلقائيًا عند إنشاء جداول عقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="57613-151">It's automatically created when lease schedules are created.</span></span>
