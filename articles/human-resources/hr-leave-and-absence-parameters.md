---
title: تكوين مُحددات الإجازة والغياب
description: تتيح تحديد معلمات الموارد البشرية للإجازات والغياب في Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1b2de94f9d9ac1ada16b6ef0e7628edbc9d683f
ms.sourcegitcommit: d02fae79d5c02a4bc4f4b16a410c2f5ce026c204
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2021
ms.locfileid: "4997091"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="20962-103">تكوين مُحددات الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="20962-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="20962-104">قبل إعداد خطط الإجازات والإجازات في Dynamics 365 Human Resources، من الأفضل التحقق من الإعدادات لكافة المحددات المتعلقة بالموارد البشرية، بما في ذلك:</span><span class="sxs-lookup"><span data-stu-id="20962-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="20962-105">التسلسل الرقمي لطلبات الإجازات</span><span class="sxs-lookup"><span data-stu-id="20962-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="20962-106">إعدادات قانون الأسرة والإجازات الطبية (FMLA)</span><span class="sxs-lookup"><span data-stu-id="20962-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="20962-107">إعدادات الخدمة الذاتية للموظفين لطلبات الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="20962-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="20962-108">معلمات الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="20962-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="20962-109">عرض محددات الموارد البشرية وتغييرها</span><span class="sxs-lookup"><span data-stu-id="20962-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="20962-110">في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="20962-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="20962-111">ضمن **الإعداد**، حدد **محددات الموارد البشرية**.</span><span class="sxs-lookup"><span data-stu-id="20962-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="20962-112">في علامة التبويب **التسلسلات الرقمية**، تحقق من **كود التسلسل الرقمي** لـ **معرف طلب الإجازة** وقم بالتغيير حسب الضرورة.</span><span class="sxs-lookup"><span data-stu-id="20962-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="20962-113">يحدد هذا الإعداد التسلسل المستخدم لتعيين المعرفات تلقائيا لطلبات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="20962-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="20962-114">في علامة التبويب **FMLA**، تحقق من إعدادات FMLA وقم بتغييرها حسب الضرورة.</span><span class="sxs-lookup"><span data-stu-id="20962-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="20962-115">في علامة التبويب **الخدمة الذاتية للموظفين**، حدد ما إذا كان بإمكان المديرين إدخال الإجازات وطلبات الغياب نيابة عن موظفيهم.</span><span class="sxs-lookup"><span data-stu-id="20962-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="20962-116">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="20962-116">Select **Save**.</span></span>

>[!IMPORTANT]
><span data-ttu-id="20962-117">عرض الإجازة والغياب عبر الشركات قيد المعاينة حاليًا.</span><span class="sxs-lookup"><span data-stu-id="20962-117">Viewing leave and absence across companies is currently in preview.</span></span> <span data-ttu-id="20962-118">ستحتاج إلى تمكينها في بيئة **الحماية** لعرض خيار الإجازة والغياب.</span><span class="sxs-lookup"><span data-stu-id="20962-118">You'll need to enable it in your **Sandbox** environment to display the option for leave and absence.</span></span> <span data-ttu-id="20962-119">لمزيد من المعلومات حول تمكين ميزات المعاينة، راجع [إدارة الميزات](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="20962-119">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="view-and-change-human-resources-shared-parameters"></a><span data-ttu-id="20962-120">عرض معلمات Human Resources وتغييرها</span><span class="sxs-lookup"><span data-stu-id="20962-120">View and change Human resources shared parameters</span></span>

1. <span data-ttu-id="20962-121">في صفحة **إدارة العاملين**، حدد علامة التبويب **ارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="20962-121">On the **Personnel management** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="20962-122">ضمن **الإعداد**، حدد **معلمات Human Resources المشتركة**.</span><span class="sxs-lookup"><span data-stu-id="20962-122">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="20962-123">في علامة التبويب **الوصول المتقدم**، حدد **نعم** لـ **تمكين طريقة عرض الإجازات عبر الشركات** للسماح بعرض الإجازة في الشركة.</span><span class="sxs-lookup"><span data-stu-id="20962-123">On the **Advance access** tab, select **Yes** for **Enable cross company leave view** to allow leave to be viewed across company.</span></span>

4. <span data-ttu-id="20962-124">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="20962-124">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="20962-125">عرض وتغيير معلمات الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="20962-125">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="20962-126">في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="20962-126">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="20962-127">ضمن **الإعداد**، حدد **معلمات الإجازة والغياب**.</span><span class="sxs-lookup"><span data-stu-id="20962-127">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="20962-128">على علامة التبويب **عام**، عيّن المعلمات التالية:</span><span class="sxs-lookup"><span data-stu-id="20962-128">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="20962-129">قم بتعيين **وحدة الإجازة والغياب** إلى ساعات أو أيام.</span><span class="sxs-lookup"><span data-stu-id="20962-129">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="20962-130">إذا اخترت الأيام، فيمكنك تحديد **تمكين تعريف نصف اليوم** للسماح للموظفين باختيار النصف الأول أو النص الثاني لليوم في طلبات الإجازة.</span><span class="sxs-lookup"><span data-stu-id="20962-130">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="20962-131">حدد **تاريخ سريان أشهر الخدمة** التي يجب تعيينها عندما تسري معدلات الاستحقاق لخطط الإجازة باستخدام أشهر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="20962-131">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="20962-132">حدد **حساب الرصيد** لعرض الأرصدة اعتبارًا من اليوم أو من فترة الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="20962-132">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="20962-133">إذا حددت **الرصيد اعتبارًا من اليوم**، فسيعرض الرصيد إجمالي كافة الاستحقاقات والتسويات والطلبات اعتبارًا من اليوم.</span><span class="sxs-lookup"><span data-stu-id="20962-133">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="20962-134">إذا حدد **الرصيد اعتبارًا من فترة الاستحقاق**، فسيعرض الرصيد إجمالي كافة الاستحقاقات والتسويات والطلبات اعتبارًا من فترة الاستحقاق المحددة بواسطة التكرار في خطة الإجازة.</span><span class="sxs-lookup"><span data-stu-id="20962-134">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="20962-135">قم بتعيين وقت البدء للوظيفة الدفعية انتهاء موازنة محولة.</span><span class="sxs-lookup"><span data-stu-id="20962-135">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="20962-136">حدد **نعم** لـ **السماح للموظفين بشراء إجازة** و **السماح للموظفين ببيع إجازة**.</span><span class="sxs-lookup"><span data-stu-id="20962-136">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="20962-137">إذا قمت بتحديد **نعم** لهذه الخيارات، يُمكنك إنشاء سياسات شراء وبيع الإجازة وتمكين الموظفين من إرسال طلبات شراء وبيع الإجازة.</span><span class="sxs-lookup"><span data-stu-id="20962-137">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="20962-138">تكوين معلمات التقويم</span><span class="sxs-lookup"><span data-stu-id="20962-138">Configure calendar parameters</span></span>

1. <span data-ttu-id="20962-139">في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="20962-139">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="20962-140">ضمن **الإعداد**، حدد **معلمات الإجازة والغياب**.</span><span class="sxs-lookup"><span data-stu-id="20962-140">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="20962-141">في علامة التبويب **تقويم**، وقم بتغيير الإعدادات حسب الضرورة.</span><span class="sxs-lookup"><span data-stu-id="20962-141">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="20962-142">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="20962-142">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="20962-143">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="20962-143">See also</span></span>

- [<span data-ttu-id="20962-144">نظرة عامة على الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="20962-144">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
