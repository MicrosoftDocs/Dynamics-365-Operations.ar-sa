---
title: إدارة سياسات شراء الإجازات وبيعها
description: يمكنك تمكين الموظفين من شراء الإجازات وبيعها في Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
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
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429003"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="7de09-103">إدارة سياسات شراء الإجازات وبيعها</span><span class="sxs-lookup"><span data-stu-id="7de09-103">Manage buy and sell leave policies</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="7de09-104">يمكنك تمكين الموظفين من شراء إجازة عن طريق إنشاء سياسة شراء الإجازات.</span><span class="sxs-lookup"><span data-stu-id="7de09-104">You can enable employees to buy leave by creating a buy leave policy.</span></span>  

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="7de09-105">تمكين الموظفين من شراء الإجازات وبيعها</span><span class="sxs-lookup"><span data-stu-id="7de09-105">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="7de09-106">في صفحة **معلمات الإجازة والغياب‬**، حدد **نعم** للخيار **السماح للموظفين بشراء الإجازات**.</span><span class="sxs-lookup"><span data-stu-id="7de09-106">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave**.</span></span> 

## <a name="create-a-buy-leave-policy"></a><span data-ttu-id="7de09-107">إنشاء سياسة شراء الإجازات</span><span class="sxs-lookup"><span data-stu-id="7de09-107">Create a buy leave policy</span></span>

1. <span data-ttu-id="7de09-108">في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="7de09-108">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="7de09-109">حدد **سياسة شراء الإجازات وبيعها‬**.</span><span class="sxs-lookup"><span data-stu-id="7de09-109">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="7de09-110">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="7de09-110">Select **New**.</span></span>

4. <span data-ttu-id="7de09-111">أدخل **اسم** و**وصف** السياسة تحت **سياسة شراء الإجازة وبيعها‬**.</span><span class="sxs-lookup"><span data-stu-id="7de09-111">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="7de09-112">حدد **نوع السياسة**.</span><span class="sxs-lookup"><span data-stu-id="7de09-112">Select a **Policy type**.</span></span> 

   <span data-ttu-id="7de09-113">أنواع السياسات المتاحة هي **المبلغ** و**عدد الساعات في الأسبوع**.</span><span class="sxs-lookup"><span data-stu-id="7de09-113">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="7de09-114">حدد **المبلغ** لإدخال **مبلغ ثابت** للمبالغ القصوى التي يمكن للموظفين شراؤها وبيعها.</span><span class="sxs-lookup"><span data-stu-id="7de09-114">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="7de09-115">إذا حددت **عدد الساعات في الأسبوع**‬، يتم استخدام وقت العمل المحدد في تقويم وقت العمل المعيّن للموظف لتحديد الحد الأقصى لمبلغ السياسة.</span><span class="sxs-lookup"><span data-stu-id="7de09-115">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="7de09-116">حدد **تاريخ بدء** و**تاريخ انتهاء** للسياسة.</span><span class="sxs-lookup"><span data-stu-id="7de09-116">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="7de09-117">ستتوفر الطلبات الخاصة بشراء الإجازة أو بيعها بحيث يمكن تقديمها خلال هذه الفترة الزمنية فقط.</span><span class="sxs-lookup"><span data-stu-id="7de09-117">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="7de09-118">ضمن **سياسة الشراء**، حدد **معادلة الوقت الكامل‬** (FTE) لتقسيم الحد الأقصى للمبلغ استنادًا إلى FTE المحدد في منصب الموظف.</span><span class="sxs-lookup"><span data-stu-id="7de09-118">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="7de09-119">إذا كان نوع السياسة **مبلغ**، فأدخل **الحد الأقصى للمبلغ الثابت**.</span><span class="sxs-lookup"><span data-stu-id="7de09-119">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

8. <span data-ttu-id="7de09-120">حدد **إضافة** لإضافة أنواع الإجازات لشرائها من قبل الموظفين.</span><span class="sxs-lookup"><span data-stu-id="7de09-120">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="7de09-121">يمكنك إضافة أنواع إجازات متعددة إلى السياسة.</span><span class="sxs-lookup"><span data-stu-id="7de09-121">You can add multiple leave types to the policy.</span></span> 

9. <span data-ttu-id="7de09-122">أدخل **أشهر الخدمة** لنوع الإجازة لتمكين أشهر خدمة مختلفة من تحديد الحد الأقصى الذي يسمح للموظف بشرائه.</span><span class="sxs-lookup"><span data-stu-id="7de09-122">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

10. <span data-ttu-id="7de09-123">أدخل **الحد الأقصى للمبلغ** لنوع الإجازة.</span><span class="sxs-lookup"><span data-stu-id="7de09-123">Enter the **Maximum amount** for the leave type.</span></span> 

11. <span data-ttu-id="7de09-124">أدخل **السعر** الذي سيشتري به الموظف الإجازة.</span><span class="sxs-lookup"><span data-stu-id="7de09-124">Enter the **Rate** at which the employee will buy the leave.</span></span> 

12. <span data-ttu-id="7de09-125">بشكل اختياري، أدخل **كود الأرباح‬** الذي‬ سيتم استخدامه لشراء الإجازة.</span><span class="sxs-lookup"><span data-stu-id="7de09-125">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

13. <span data-ttu-id="7de09-126">بشكل اختياري، عيّن ما إذا كان سيتم استخدام FTE لتحديد الحد الأقصى للمبلغ الخاص بنوع الإجازة.</span><span class="sxs-lookup"><span data-stu-id="7de09-126">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="7de09-127">إضافة سياسة شراء الإجازات وبيعها لخطة الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="7de09-127">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="7de09-128">في الصفحة **الإجازة والغياب**، حدد خطة الإجازة والغياب.</span><span class="sxs-lookup"><span data-stu-id="7de09-128">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="7de09-129">ضمن **القواعد**، حدد **سياسة شراء الإجازات وبيعها**.</span><span class="sxs-lookup"><span data-stu-id="7de09-129">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="7de09-130">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="7de09-130">See also</span></span>

[<span data-ttu-id="7de09-131">نظرة عامة على الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="7de09-131">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="7de09-132">تكوين أنواع الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="7de09-132">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="7de09-133">استحقاق خطط الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="7de09-133">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="7de09-134">شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="7de09-134">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

