--- 
title: "تحديد قواعد وسياسات استحقاق الفائدة"
description: "سيظهر هذا التسجيل كيفية إنشاء قواعد وسياسات استحقاق الميزات، ثم تعيين قواعد للميزات."
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d0978d8c76990c6f9e041289581c28556c83e524
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="8dc75-103">تحديد قواعد وسياسات استحقاق الفائدة</span><span class="sxs-lookup"><span data-stu-id="8dc75-103">Define benefit eligibility rules and policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8dc75-104">سيظهر هذا التسجيل كيفية إنشاء قواعد وسياسات استحقاق الميزات، ثم تعيين قواعد للميزات.</span><span class="sxs-lookup"><span data-stu-id="8dc75-104">This recording will show you how you can create benefit eligibility rules and policies and then assign rules to Benefits.</span></span>  

<span data-ttu-id="8dc75-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا التسجيل هي USMF.</span><span class="sxs-lookup"><span data-stu-id="8dc75-105">The demo data company used to create this recording is USMF.</span></span>


## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="8dc75-106">إنشاء نوع قاعدة سياسة استحقاق المزايا‬</span><span class="sxs-lookup"><span data-stu-id="8dc75-106">Create benefit eligibility policy rule type</span></span>
1. <span data-ttu-id="8dc75-107">انتقل إلى الموارد البشرية > الميزات > الأهلية > أنواع قواعد سياسات استحقاق الميزات.</span><span class="sxs-lookup"><span data-stu-id="8dc75-107">Go to Human resources > Benefits > Eligibility > Benefit eligibility policy rule types.</span></span>
2. <span data-ttu-id="8dc75-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="8dc75-108">Click New.</span></span>
3. <span data-ttu-id="8dc75-109">في الحقل "اسم القاعدة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="8dc75-109">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="8dc75-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="8dc75-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8dc75-111">في الحقل "اسم الاستعلام"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="8dc75-111">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="8dc75-112">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8dc75-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="8dc75-113">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="8dc75-113">Click Save.</span></span>
8. <span data-ttu-id="8dc75-114">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8dc75-114">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="8dc75-115">سياسة استحقاق المزايا</span><span class="sxs-lookup"><span data-stu-id="8dc75-115">Benefit eligibility policy</span></span>
1. <span data-ttu-id="8dc75-116">انتقل إلى الموارد البشرية > الميزات > الأهلية > سياسات استحقاق الميزات‬.</span><span class="sxs-lookup"><span data-stu-id="8dc75-116">Go to Human resources > Benefits > Eligibility > Benefit eligibility policies.</span></span>
2. <span data-ttu-id="8dc75-117">حدد سياسة ميزات موجودة.</span><span class="sxs-lookup"><span data-stu-id="8dc75-117">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="8dc75-118">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8dc75-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8dc75-119">بدّل توسيع المقاطع "مؤسسات السياسات‬‬".</span><span class="sxs-lookup"><span data-stu-id="8dc75-119">Toggle the expansion of the Policy organizations sections.</span></span>  <span data-ttu-id="8dc75-120">هنا يمكنك إضافة أي من المؤسسات التي تريد تضمينها في السياسة أو إزالتها.</span><span class="sxs-lookup"><span data-stu-id="8dc75-120">Here you can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="8dc75-121">قم بتوسيع المقطع "قواعد السياسة‬" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="8dc75-121">Expand or collapse the Policy rules section.</span></span>
6. <span data-ttu-id="8dc75-122">في القائمة، ابحث عن "قاعدة السياسة" التي تم إنشاؤها في السابق.</span><span class="sxs-lookup"><span data-stu-id="8dc75-122">In the list find the policy rule previously created.</span></span>
7. <span data-ttu-id="8dc75-123">انقر فوق "إنشاء قاعدة السياسة".</span><span class="sxs-lookup"><span data-stu-id="8dc75-123">Click Create policy rule.</span></span>
8. <span data-ttu-id="8dc75-124">في الحقل "تاريخ السريان"، أدخل التاريخ الذي تريد أن تصبح فيه السياسة سارية المفعول.</span><span class="sxs-lookup"><span data-stu-id="8dc75-124">In the Effective date field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="8dc75-125">يسمح لك إعداد تواريخ السريان والانتهاء بإجراء تغييرات مستقبلية على قواعد السياسة وإزالة الحاجة إلى الرجوع إلى السياسة عندما تريد أن تصبح هذه التغييرات نافذة المفعول.</span><span class="sxs-lookup"><span data-stu-id="8dc75-125">Setting effective and end dates allows you to make future changes to policy rules and removing the need to come back to the policy when you want those changes to take effect.</span></span>  
9. 
    * <span data-ttu-id="8dc75-126">على سبيل المثال، إذا أردت تطبيق القاعدة فقط على "مديري المبيعات"، فيمكنك إنشاء عبارة Where للقول: حيث يساوي وصف المنصب "مدير المبيعات".</span><span class="sxs-lookup"><span data-stu-id="8dc75-126">For example if you wanted the rule to only apply to Sales Managers you could create the Where clause to say: Where position description equals Sales Manager.</span></span>  <span data-ttu-id="8dc75-127">يمكنك أن تضيف معًا عبارات And أو Or وعبارات Where متعددة في القاعدة.</span><span class="sxs-lookup"><span data-stu-id="8dc75-127">You can And or Or multiple Where statements together in the rule.</span></span>  
10. <span data-ttu-id="8dc75-128">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="8dc75-128">Click OK.</span></span>
11. <span data-ttu-id="8dc75-129">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8dc75-129">Close the page.</span></span>
12. <span data-ttu-id="8dc75-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8dc75-130">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="8dc75-131">تعيين قاعدة لميزة</span><span class="sxs-lookup"><span data-stu-id="8dc75-131">Assign rule to benefit</span></span>
1. <span data-ttu-id="8dc75-132">انتقل إلى الموارد البشرية > الميزات‬ > الميزات‬.</span><span class="sxs-lookup"><span data-stu-id="8dc75-132">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="8dc75-133">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="8dc75-133">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8dc75-134">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8dc75-134">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8dc75-135">قم بتوسيع القسم "قواعد الاستحقاق" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="8dc75-135">Expand or collapse the Eligibility rules section.</span></span>
5. <span data-ttu-id="8dc75-136">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="8dc75-136">Click Edit.</span></span>
6. <span data-ttu-id="8dc75-137">في حقل "الأهلية"، حدد "على أساس القاعدة" من القائمة.</span><span class="sxs-lookup"><span data-stu-id="8dc75-137">In the Eligibility field, select Rule based from the list.</span></span>
7. <span data-ttu-id="8dc75-138">في الحقل "نوع القاعدة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="8dc75-138">In the Rule type field, click the drop down button to open the lookup.</span></span>
8. <span data-ttu-id="8dc75-139">في القائمة، ابحث عن القاعدة التي تم إنشاؤها في السابق وحددها.</span><span class="sxs-lookup"><span data-stu-id="8dc75-139">In the list find and select the rule you previously created.</span></span>
9. <span data-ttu-id="8dc75-140">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8dc75-140">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="8dc75-141">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="8dc75-141">Click Save.</span></span>
11. <span data-ttu-id="8dc75-142">وقم بغلق النموذج.</span><span class="sxs-lookup"><span data-stu-id="8dc75-142">Close the form.</span></span>


