---
title: تكوين أنواع الإجازة والغياب
description: إعداد أنواع الإجازات التي يمكن للموظفين القيام بها في Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df6e34fe6a23e6f0a8307a035752a35a15a3431c
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198040"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="3ad07-103">تكوين أنواع الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="3ad07-103">Configure leave and absence types</span></span>

<span data-ttu-id="3ad07-104">تحدد أنواع الإجازات في Dynamics 365 Human Resources أنواعًا مختلفة من حالات الغياب التي يمكن للموظفين الإبلاغ عنها.</span><span class="sxs-lookup"><span data-stu-id="3ad07-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="3ad07-105">يمكنك تكييف أنواع الإجازات وفقًا لاحتياجات مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="3ad07-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="3ad07-106">تشتمل أمثلة أنواع الإجازات على ما يلي:</span><span class="sxs-lookup"><span data-stu-id="3ad07-106">Examples of leave types include:</span></span>

- <span data-ttu-id="3ad07-107">زمن التوقف المدفوع (PTO)</span><span class="sxs-lookup"><span data-stu-id="3ad07-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="3ad07-108">إجازة دون راتب</span><span class="sxs-lookup"><span data-stu-id="3ad07-108">Unpaid leave</span></span>
- <span data-ttu-id="3ad07-109">إجازة مدفوعة الأجر</span><span class="sxs-lookup"><span data-stu-id="3ad07-109">Paid vacation</span></span>
- <span data-ttu-id="3ad07-110">إجازة مرضية</span><span class="sxs-lookup"><span data-stu-id="3ad07-110">Sick leave</span></span>
- <span data-ttu-id="3ad07-111">إجازة طبية</span><span class="sxs-lookup"><span data-stu-id="3ad07-111">Medical leave</span></span>
- <span data-ttu-id="3ad07-112">إجازة العائلية</span><span class="sxs-lookup"><span data-stu-id="3ad07-112">Family leave</span></span>
- <span data-ttu-id="3ad07-113">الإعاقة قصيرة الأجل</span><span class="sxs-lookup"><span data-stu-id="3ad07-113">Short-term disability</span></span>
- <span data-ttu-id="3ad07-114">إجازة Bereavement</span><span class="sxs-lookup"><span data-stu-id="3ad07-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="3ad07-115">إضافة نوع إجازة</span><span class="sxs-lookup"><span data-stu-id="3ad07-115">Add a leave type</span></span>

1. <span data-ttu-id="3ad07-116">في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="3ad07-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="3ad07-117">ضمن **الإعداد**، حدد **أنواع الإجازات والغياب**.</span><span class="sxs-lookup"><span data-stu-id="3ad07-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="3ad07-118">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="3ad07-118">Select **New**.</span></span>

4. <span data-ttu-id="3ad07-119">ادخل اسما لنوع الإجازة ضمن **النوع**، وحدد سير عمل من **معرف سير العمل**، وادخل وصفا ضمن **الوصف**.</span><span class="sxs-lookup"><span data-stu-id="3ad07-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="3ad07-120">في **عام**، حدد **بلا** أو **مجدول** أو **غير مجدول** من القائمة المنسدلة **الفئة**.</span><span class="sxs-lookup"><span data-stu-id="3ad07-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="3ad07-121">حدد كود دخل من القائمة المنسدلة **رمز الدخل**.</span><span class="sxs-lookup"><span data-stu-id="3ad07-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="3ad07-122">ضمن **كود السبب المطلوب**، حدد ما إذا كنت ترغب في طلب كود سبب ام لا.</span><span class="sxs-lookup"><span data-stu-id="3ad07-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="3ad07-123">إذا كنت ترغب في طلب أكواد سبب، فقد تحتاج إلى اضافتها.</span><span class="sxs-lookup"><span data-stu-id="3ad07-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="3ad07-124">ضمن **أكواد السبب**، حدد **إضافة**، وحدد كود السبب، ثم حدد خانة الاختيار **ممكن** بجوارها.</span><span class="sxs-lookup"><span data-stu-id="3ad07-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="3ad07-125">ضمن **تقييد الوصول إلى الأدوار المحددة**، اختر ما إذا كنت ترغب في تقييد الوصول ام لا.</span><span class="sxs-lookup"><span data-stu-id="3ad07-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="3ad07-126">ثم حدد ادوار الأمان ضمن **ادوار الأمان لنوع الإجازة هذا**.</span><span class="sxs-lookup"><span data-stu-id="3ad07-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="3ad07-127">يتم تحديد ادوار الأمان في سير العمل الذي حددته ضمن **معرف سير العمل** في هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="3ad07-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="3ad07-128">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="3ad07-128">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="3ad07-129">تكوين قواعد أنواع الإجازة</span><span class="sxs-lookup"><span data-stu-id="3ad07-129">Configure leave type rules</span></span>

1. <span data-ttu-id="3ad07-130">تعيين خيارات التقريب لنوع الإجازة .</span><span class="sxs-lookup"><span data-stu-id="3ad07-130">Set rounding options for the leave type.</span></span> <span data-ttu-id="3ad07-131">تتضمن الخيارات **بلا**، و**لأعلى** و**لأسفل** و**الأقرب**.</span><span class="sxs-lookup"><span data-stu-id="3ad07-131">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="3ad07-132">يمكنك أيضا تعيين دقه التقريب لنوع الإجازة .</span><span class="sxs-lookup"><span data-stu-id="3ad07-132">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="3ad07-133">قم بتعيين **تصحيح الإجازة** لنوع العطلة.</span><span class="sxs-lookup"><span data-stu-id="3ad07-133">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="3ad07-134">عند تحديد هذا الخيار ، تستخدم Human Resources عدد العطلات التي تقع في يوم العمل لتحديد كيفيه استحقاق الوقت لنوع الإجازة .</span><span class="sxs-lookup"><span data-stu-id="3ad07-134">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="3ad07-135">على سبيل المثال، إذا كان يوم عيد الميلاد يوم الاثنين ، فإن Human Resources سيطرح يومًا واحدًا من نوع الإجازة عند معالجه الاستحقاقات.</span><span class="sxs-lookup"><span data-stu-id="3ad07-135">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="3ad07-136">يمكنك تعيين العطلات في تقويم وقت العمل.</span><span class="sxs-lookup"><span data-stu-id="3ad07-136">You set holidays in the working time calendar.</span></span> <span data-ttu-id="3ad07-137">لمزيد من المعلومات، راجع [إنشاء تقويم وقت العمل](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="3ad07-137">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
## <a name="configure-preview-features"></a><span data-ttu-id="3ad07-138">تكوين ميزات المعاينة</span><span class="sxs-lookup"><span data-stu-id="3ad07-138">Configure preview features</span></span>

<span data-ttu-id="3ad07-139">إذا قمت بتمكين ميزات المعاينة للإجازة والغياب، فانك تحتاج إلى تكوين إعدادات لها أيضا.</span><span class="sxs-lookup"><span data-stu-id="3ad07-139">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

1. <span data-ttu-id="3ad07-140">اختر نوع الإجازة لأرصدة الإجازة التي يجب نقلها إليه.</span><span class="sxs-lookup"><span data-stu-id="3ad07-140">Choose the leave type for carry forward balances to be transferred to.</span></span> <span data-ttu-id="3ad07-141">يمكنك أيضًا إنشاء نوع إجازة جديد لنقل الإجازات.</span><span class="sxs-lookup"><span data-stu-id="3ad07-141">You can also create a new leave type for carry forward.</span></span> 

## <a name="see-also"></a><span data-ttu-id="3ad07-142">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="3ad07-142">See also</span></span>

- [<span data-ttu-id="3ad07-143">نظرة عامة على الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="3ad07-143">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="3ad07-144">إنشاء خطة الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="3ad07-144">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="3ad07-145">إنشاء تقويم مواعيد العمل</span><span class="sxs-lookup"><span data-stu-id="3ad07-145">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
