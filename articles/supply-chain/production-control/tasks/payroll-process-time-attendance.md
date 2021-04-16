---
title: تمكين عملية المرتبات للوقت والحضور
description: يوضح هذا الإجراء كيفية تمكين عملية مرتبات الوقت والحضور‬.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 411b5c3f1a486a30ec7d8d2c3896dacbf97b39ed
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821022"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="6c35d-103">تمكين عملية المرتبات للوقت والحضور</span><span class="sxs-lookup"><span data-stu-id="6c35d-103">Enable the payroll process for time and attendance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6c35d-104">يوضح هذا الإجراء كيفية تمكين عملية مرتبات الوقت والحضور‬.</span><span class="sxs-lookup"><span data-stu-id="6c35d-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="6c35d-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="6c35d-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="6c35d-106">إنشاء نوع دفع مع معدل دفع ذي صلة</span><span class="sxs-lookup"><span data-stu-id="6c35d-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="6c35d-107">التوقيت والحضور > إعداد > كشف الرواتب‬ > أنواع الدفع</span><span class="sxs-lookup"><span data-stu-id="6c35d-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="6c35d-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="6c35d-108">Click New.</span></span>
3. <span data-ttu-id="6c35d-109">في حقل "نوع الدفع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6c35d-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="6c35d-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6c35d-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6c35d-111">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="6c35d-111">Click Save.</span></span>
6. <span data-ttu-id="6c35d-112">انقر فوق "المعدلات‬".</span><span class="sxs-lookup"><span data-stu-id="6c35d-112">Click Rates.</span></span>
    * <span data-ttu-id="6c35d-113">يتم إعداد معدلات لأنواع الدفع لفترات زمنية محددة، ويمكن إنشاء معدلات فردية للموظفين.</span><span class="sxs-lookup"><span data-stu-id="6c35d-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="6c35d-114">ليس من الضروري دائمًا إنشاء معدلات لأنواع الدفع في التوقيت والحضور.</span><span class="sxs-lookup"><span data-stu-id="6c35d-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="6c35d-115">ربما توجد هذه المعلومات مسبقًا في نظام الرواتب المستخدم لإنشاء أجور الموظفين.</span><span class="sxs-lookup"><span data-stu-id="6c35d-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="6c35d-116">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="6c35d-116">Click New.</span></span>
8. <span data-ttu-id="6c35d-117">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6c35d-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="6c35d-118">أدخل رقمًا في الحقل "المعدل‬".</span><span class="sxs-lookup"><span data-stu-id="6c35d-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="6c35d-119">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="6c35d-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="6c35d-120">إنشاء اتفاقية دفع</span><span class="sxs-lookup"><span data-stu-id="6c35d-120">Create a pay agreement</span></span>
1. <span data-ttu-id="6c35d-121">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6c35d-121">Close the page.</span></span>
2. <span data-ttu-id="6c35d-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6c35d-122">Close the page.</span></span>
3. <span data-ttu-id="6c35d-123">انتقل إلى "اتفاقيات الدفع".</span><span class="sxs-lookup"><span data-stu-id="6c35d-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="6c35d-124">التوقيت والحضور > إعداد > اتفاقيات الدفع</span><span class="sxs-lookup"><span data-stu-id="6c35d-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="6c35d-125">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="6c35d-125">Click New.</span></span>
5. <span data-ttu-id="6c35d-126">في حقل "اتفاقية الدفع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6c35d-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="6c35d-127">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6c35d-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="6c35d-128">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="6c35d-128">Click Save.</span></span>
8. <span data-ttu-id="6c35d-129">انقر فوق "بنود الاتفاقية".</span><span class="sxs-lookup"><span data-stu-id="6c35d-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="6c35d-130">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="6c35d-130">Click New.</span></span>
10. <span data-ttu-id="6c35d-131">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6c35d-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="6c35d-132">في الحقل "نوع ملف التعريف‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6c35d-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="6c35d-133">في الحقل "نوع الدفع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6c35d-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="6c35d-134">إعداد اتفاقية دفع لعامل التوقيت والتسجيل</span><span class="sxs-lookup"><span data-stu-id="6c35d-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="6c35d-135">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6c35d-135">Close the page.</span></span>
2. <span data-ttu-id="6c35d-136">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6c35d-136">Close the page.</span></span>
3. <span data-ttu-id="6c35d-137">انتقل إلى "عاملو التسجيل الزمني".</span><span class="sxs-lookup"><span data-stu-id="6c35d-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="6c35d-138">التوقيت والحضور > إعداد > عاملو التسجيل الزمني‬</span><span class="sxs-lookup"><span data-stu-id="6c35d-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="6c35d-139">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6c35d-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="6c35d-140">انقر فوق علامة التبويب "التوظيف‬‬".</span><span class="sxs-lookup"><span data-stu-id="6c35d-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="6c35d-141">وسّع مقطع "التسجيل الزمني‬".</span><span class="sxs-lookup"><span data-stu-id="6c35d-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="6c35d-142">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="6c35d-142">Click Edit.</span></span>
8. <span data-ttu-id="6c35d-143">في الحقل "اتفاقية الدفع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6c35d-143">In the Pay agreement field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]