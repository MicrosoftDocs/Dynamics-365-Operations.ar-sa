---
title: إدارة سياسات شراء الإجازات وبيعها
description: يمكنك تمكين الموظفين من شراء الإجازات وبيعها في Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 89563204cf1423ddce47d7bacace8f14edf87005
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115986"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="52147-103">إدارة سياسات شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="52147-103">Manage buy and sell leave policies</span></span>

<span data-ttu-id="52147-104">يمكنك تمكين الموظفين من شراء إجازة وبيعها عن طريق إنشاء سياسة شراء وبيع الإجازات.</span><span class="sxs-lookup"><span data-stu-id="52147-104">You can enable employees to buy and sell leave by creating a buy and sell leave policy.</span></span> <span data-ttu-id="52147-105">يُمكنك تكوين هذه السياسات لاستخدام سير العمل في عمليات الاعتماد وتعيين الحد الأقصى للمبالغ والنسب المئوية وتعيين النسب المئوية للشراء والبيع.</span><span class="sxs-lookup"><span data-stu-id="52147-105">You can configure these policies to use workflow for approvals, set maximum amounts and rates, and set rates for buying and selling.</span></span> 

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="52147-106">تمكين الموظفين من شراء الإجازات وبيعها</span><span class="sxs-lookup"><span data-stu-id="52147-106">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="52147-107">في صفحة **مُعلمات الإجازة والغياب**، حدد **نعم** لـ **السماح للموظفين بشراء الإجازة** و **السماح للموظفين ببيع الإجازة**.</span><span class="sxs-lookup"><span data-stu-id="52147-107">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span>

## <a name="create-a-buy-and-sell-leave-policy"></a><span data-ttu-id="52147-108">إنشاء سياسة شراء وبيع الإجازات</span><span class="sxs-lookup"><span data-stu-id="52147-108">Create a buy and sell leave policy</span></span>

1. <span data-ttu-id="52147-109">في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="52147-109">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="52147-110">حدد **سياسة شراء الإجازات وبيعها‬**.</span><span class="sxs-lookup"><span data-stu-id="52147-110">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="52147-111">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="52147-111">Select **New**.</span></span>

4. <span data-ttu-id="52147-112">أدخل **اسم** و **وصف** السياسة تحت **سياسة شراء الإجازة وبيعها‬**.</span><span class="sxs-lookup"><span data-stu-id="52147-112">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="52147-113">حدد **نوع السياسة**.</span><span class="sxs-lookup"><span data-stu-id="52147-113">Select a **Policy type**.</span></span> 

   <span data-ttu-id="52147-114">أنواع السياسات المتاحة هي **المبلغ** و **عدد الساعات في الأسبوع**.</span><span class="sxs-lookup"><span data-stu-id="52147-114">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="52147-115">حدد **المبلغ** لإدخال **مبلغ ثابت** للمبالغ القصوى التي يمكن للموظفين شراؤها وبيعها.</span><span class="sxs-lookup"><span data-stu-id="52147-115">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="52147-116">إذا حددت **عدد الساعات في الأسبوع**‬، يتم استخدام وقت العمل المحدد في تقويم وقت العمل المعيّن للموظف لتحديد الحد الأقصى لمبلغ السياسة.</span><span class="sxs-lookup"><span data-stu-id="52147-116">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="52147-117">حدد **تاريخ بدء** و **تاريخ انتهاء** للسياسة.</span><span class="sxs-lookup"><span data-stu-id="52147-117">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="52147-118">ستتوفر الطلبات الخاصة بشراء الإجازة أو بيعها بحيث يمكن تقديمها خلال هذه الفترة الزمنية فقط.</span><span class="sxs-lookup"><span data-stu-id="52147-118">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="52147-119">حدد **معرف سير العمل** للسياسة.</span><span class="sxs-lookup"><span data-stu-id="52147-119">Select a **Workflow ID** for the policy.</span></span> <span data-ttu-id="52147-120">سوف تستخدم أي طلبات شراء وبيع سير العمل هذا للمراجعة والاعتماد.</span><span class="sxs-lookup"><span data-stu-id="52147-120">Any buy and sell requests will use this workflow for review and approval.</span></span> 

8. <span data-ttu-id="52147-121">ضمن **سياسة الشراء**، حدد **معادلة الوقت الكامل‬** (FTE) لتقسيم الحد الأقصى للمبلغ استنادًا إلى FTE المحدد في منصب الموظف.</span><span class="sxs-lookup"><span data-stu-id="52147-121">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="52147-122">إذا كان نوع السياسة **مبلغ**، فأدخل **الحد الأقصى للمبلغ الثابت**.</span><span class="sxs-lookup"><span data-stu-id="52147-122">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

9. <span data-ttu-id="52147-123">حدد **إضافة** لإضافة أنواع الإجازات لشرائها من قبل الموظفين.</span><span class="sxs-lookup"><span data-stu-id="52147-123">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="52147-124">يمكنك إضافة أنواع إجازات متعددة إلى السياسة.</span><span class="sxs-lookup"><span data-stu-id="52147-124">You can add multiple leave types to the policy.</span></span> 

10. <span data-ttu-id="52147-125">أدخل **أشهر الخدمة** لنوع الإجازة لتمكين أشهر خدمة مختلفة من تحديد الحد الأقصى الذي يسمح للموظف بشرائه.</span><span class="sxs-lookup"><span data-stu-id="52147-125">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

11. <span data-ttu-id="52147-126">أدخل **الحد الأقصى للمبلغ** لنوع الإجازة.</span><span class="sxs-lookup"><span data-stu-id="52147-126">Enter the **Maximum amount** for the leave type.</span></span> 

12. <span data-ttu-id="52147-127">أدخل **السعر** الذي سيشتري به الموظف الإجازة.</span><span class="sxs-lookup"><span data-stu-id="52147-127">Enter the **Rate** at which the employee will buy the leave.</span></span> 

13. <span data-ttu-id="52147-128">بشكل اختياري، أدخل **كود الأرباح‬** الذي‬ سيتم استخدامه لشراء الإجازة.</span><span class="sxs-lookup"><span data-stu-id="52147-128">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

14. <span data-ttu-id="52147-129">بشكل اختياري، عيّن ما إذا كان سيتم استخدام FTE لتحديد الحد الأقصى للمبلغ الخاص بنوع الإجازة.</span><span class="sxs-lookup"><span data-stu-id="52147-129">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

15. <span data-ttu-id="52147-130">لإنشاء سياسة بيع، اتبع الخطوات من 8 إلى 14 ضمن **سياسة البيع**.</span><span class="sxs-lookup"><span data-stu-id="52147-130">To create a sell policy, follow steps 8 through 14 under **Sell policy**.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="52147-131">إضافة سياسة شراء الإجازات وبيعها لخطة الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="52147-131">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="52147-132">في الصفحة **الإجازة والغياب**، حدد خطة الإجازة والغياب.</span><span class="sxs-lookup"><span data-stu-id="52147-132">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="52147-133">ضمن **القواعد**، حدد **سياسة شراء الإجازات وبيعها**.</span><span class="sxs-lookup"><span data-stu-id="52147-133">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="52147-134">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="52147-134">See also</span></span>

[<span data-ttu-id="52147-135">نظرة عامة على الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="52147-135">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="52147-136">تكوين أنواع الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="52147-136">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="52147-137">استحقاق خطط الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="52147-137">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="52147-138">شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="52147-138">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

