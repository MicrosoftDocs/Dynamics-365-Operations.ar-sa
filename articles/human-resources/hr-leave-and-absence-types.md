---
title: تكوين أنواع الإجازة والغياب
description: إعداد أنواع الإجازات التي يمكن للموظفين القيام بها في Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 1748ec2a888a50af9b9260720dfd439adc4686f9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007998"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="96479-103">تكوين أنواع الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="96479-103">Configure leave and absence types</span></span>

<span data-ttu-id="96479-104">تحدد أنواع الإجازات في Dynamics 365 Human Resources أنواعًا مختلفة من حالات الغياب التي يمكن للموظفين الإبلاغ عنها.</span><span class="sxs-lookup"><span data-stu-id="96479-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="96479-105">يمكنك تكييف أنواع الإجازات وفقًا لاحتياجات مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="96479-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="96479-106">تشتمل أمثلة أنواع الإجازات على ما يلي:</span><span class="sxs-lookup"><span data-stu-id="96479-106">Examples of leave types include:</span></span>

- <span data-ttu-id="96479-107">زمن التوقف المدفوع (PTO)</span><span class="sxs-lookup"><span data-stu-id="96479-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="96479-108">إجازة دون راتب</span><span class="sxs-lookup"><span data-stu-id="96479-108">Unpaid leave</span></span>
- <span data-ttu-id="96479-109">إجازة مدفوعة الأجر</span><span class="sxs-lookup"><span data-stu-id="96479-109">Paid vacation</span></span>
- <span data-ttu-id="96479-110">إجازة مرضية</span><span class="sxs-lookup"><span data-stu-id="96479-110">Sick leave</span></span>
- <span data-ttu-id="96479-111">إجازة طبية</span><span class="sxs-lookup"><span data-stu-id="96479-111">Medical leave</span></span>
- <span data-ttu-id="96479-112">إجازة العائلية</span><span class="sxs-lookup"><span data-stu-id="96479-112">Family leave</span></span>
- <span data-ttu-id="96479-113">الإعاقة قصيرة الأجل</span><span class="sxs-lookup"><span data-stu-id="96479-113">Short-term disability</span></span>
- <span data-ttu-id="96479-114">إجازة Bereavement</span><span class="sxs-lookup"><span data-stu-id="96479-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="96479-115">إضافة نوع إجازة</span><span class="sxs-lookup"><span data-stu-id="96479-115">Add a leave type</span></span>

1. <span data-ttu-id="96479-116">في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="96479-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="96479-117">ضمن **الإعداد**، حدد **أنواع الإجازات والغياب**.</span><span class="sxs-lookup"><span data-stu-id="96479-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="96479-118">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="96479-118">Select **New**.</span></span>

4. <span data-ttu-id="96479-119">ادخل اسما لنوع الاجازه ضمن **النوع**، وحدد سير عمل من **معرف سير العمل**، وادخل وصفا ضمن **الوصف**.</span><span class="sxs-lookup"><span data-stu-id="96479-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="96479-120">في **عام**، حدد **بلا** أو **مجدول** أو **غير مجدول** من القائمة المنسدلة **الفئة**.</span><span class="sxs-lookup"><span data-stu-id="96479-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="96479-121">حدد كود دخل من القائمة المنسدلة **رمز الدخل**.</span><span class="sxs-lookup"><span data-stu-id="96479-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="96479-122">ضمن **كود السبب المطلوب**، حدد ما إذا كنت ترغب في طلب كود سبب ام لا.</span><span class="sxs-lookup"><span data-stu-id="96479-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="96479-123">إذا كنت ترغب في طلب أكواد سبب، فقد تحتاج إلى اضافتها.</span><span class="sxs-lookup"><span data-stu-id="96479-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="96479-124">ضمن **أكواد السبب**، حدد **إضافة**، وحدد كود السبب، ثم حدد خانة الاختيار **ممكن** بجوارها.</span><span class="sxs-lookup"><span data-stu-id="96479-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="96479-125">ضمن **تقييد الوصول إلى الأدوار المحددة**، اختر ما إذا كنت ترغب في تقييد الوصول ام لا.</span><span class="sxs-lookup"><span data-stu-id="96479-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="96479-126">ثم حدد ادوار الأمان ضمن **ادوار الأمان لنوع الإجازة هذا**.</span><span class="sxs-lookup"><span data-stu-id="96479-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="96479-127">يتم تحديد ادوار الأمان في سير العمل الذي حددته ضمن **معرف سير العمل** في هذا الاجراء.</span><span class="sxs-lookup"><span data-stu-id="96479-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="96479-128">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="96479-128">Select **Save**.</span></span>

## <a name="configure-preview-features"></a><span data-ttu-id="96479-129">تكوين ميزات المعاينة</span><span class="sxs-lookup"><span data-stu-id="96479-129">Configure preview features</span></span>

<span data-ttu-id="96479-130">إذا قمت بتمكين ميزات المعاينة للإجازة والغياب، فانك تحتاج إلى تكوين إعدادات لها أيضا.</span><span class="sxs-lookup"><span data-stu-id="96479-130">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

1. <span data-ttu-id="96479-131">تعيين خيارات التقريب لنوع الاجازه.</span><span class="sxs-lookup"><span data-stu-id="96479-131">Set rounding options for the leave type.</span></span> <span data-ttu-id="96479-132">تتضمن الخيارات **بلا**، و**لأعلى** و**لأسفل** و**الأقرب**.</span><span class="sxs-lookup"><span data-stu-id="96479-132">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="96479-133">يمكنك أيضا تعيين دقه التقريب لنوع الاجازه.</span><span class="sxs-lookup"><span data-stu-id="96479-133">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="96479-134">قم بتعيين **تصحيح الإجازة** لنوع العطلة.</span><span class="sxs-lookup"><span data-stu-id="96479-134">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="96479-135">عند تحديد هذا الخيار ، تستخدم Human Resources عدد العطلات التي تقع في يوم العمل لتحديد كيفيه استحقاق الوقت لنوع الاجازه.</span><span class="sxs-lookup"><span data-stu-id="96479-135">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="96479-136">علي سبيل المثال ، إذا كان يوم عيد الميلاد يوم الاثنين ، فان Human Resources ستطرح يوم واحد من نوع الاجازه عند معالجه الاستحقاقات.</span><span class="sxs-lookup"><span data-stu-id="96479-136">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="96479-137">يمكنك تعيين العطلات في تقويم وقت العمل.</span><span class="sxs-lookup"><span data-stu-id="96479-137">You set holidays in the working time calendar.</span></span> <span data-ttu-id="96479-138">لمزيد من المعلومات، راجع [إنشاء تقويم وقت العمل](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="96479-138">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="96479-139">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="96479-139">See also</span></span>

- [<span data-ttu-id="96479-140">نظرة عامة على الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="96479-140">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="96479-141">إنشاء خطة إجازة وغياب</span><span class="sxs-lookup"><span data-stu-id="96479-141">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="96479-142">إنشاء تقويم مواعيد العمل</span><span class="sxs-lookup"><span data-stu-id="96479-142">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)