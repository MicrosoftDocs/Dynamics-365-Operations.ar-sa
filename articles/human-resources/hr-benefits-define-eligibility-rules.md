---
title: تحديد قواعد وسياسات استحقاق الفائدة
description: يوضح لك هذا المقال كيف يمكنك إنشاء قواعد وسياسات أهلية الميزة ثم تعيين القواعد للمزايا.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: fa507591fc89eaebf617deedb15b15a0f93f971d
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008027"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="b2391-103">تحديد قواعد وسياسات استحقاق الفائدة</span><span class="sxs-lookup"><span data-stu-id="b2391-103">Define benefit eligibility rules and policies</span></span>

<span data-ttu-id="b2391-104">يوضح لك هذا المقال كيف يمكنك إنشاء قواعد وسياسات أهلية الميزة ثم تعيين القواعد للمزايا.</span><span class="sxs-lookup"><span data-stu-id="b2391-104">This article shows you how you can create benefit eligibility rules and policies and then assign rules to Benefits.</span></span>  

<span data-ttu-id="b2391-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا التسجيل هي USMF.</span><span class="sxs-lookup"><span data-stu-id="b2391-105">The demo data company used to create this recording is USMF.</span></span>


## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="b2391-106">إنشاء نوع قاعدة سياسة استحقاق المزايا‬</span><span class="sxs-lookup"><span data-stu-id="b2391-106">Create benefit eligibility policy rule type</span></span>
1. <span data-ttu-id="b2391-107">انتقل إلى الموارد البشرية > الميزات > الأهلية > أنواع قواعد سياسات استحقاق الميزات.</span><span class="sxs-lookup"><span data-stu-id="b2391-107">Go to Human resources > Benefits > Eligibility > Benefit eligibility policy rule types.</span></span>
2. <span data-ttu-id="b2391-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b2391-108">Click New.</span></span>
3. <span data-ttu-id="b2391-109">في الحقل "اسم القاعدة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b2391-109">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="b2391-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b2391-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b2391-111">في الحقل "اسم الاستعلام"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="b2391-111">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="b2391-112">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b2391-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="b2391-113">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b2391-113">Click Save.</span></span>
8. <span data-ttu-id="b2391-114">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b2391-114">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="b2391-115">سياسة استحقاق المزايا</span><span class="sxs-lookup"><span data-stu-id="b2391-115">Benefit eligibility policy</span></span>
1. <span data-ttu-id="b2391-116">انتقل إلى الموارد البشرية > الميزات > الأهلية > سياسات استحقاق الميزات‬.</span><span class="sxs-lookup"><span data-stu-id="b2391-116">Go to Human resources > Benefits > Eligibility > Benefit eligibility policies.</span></span>
2. <span data-ttu-id="b2391-117">حدد سياسة ميزات موجودة.</span><span class="sxs-lookup"><span data-stu-id="b2391-117">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="b2391-118">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b2391-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b2391-119">بدّل توسيع المقاطع "مؤسسات السياسات‬‬".</span><span class="sxs-lookup"><span data-stu-id="b2391-119">Toggle the expansion of the Policy organizations sections.</span></span>  <span data-ttu-id="b2391-120">هنا يمكنك إضافة أي من المؤسسات التي تريد تضمينها في السياسة أو إزالتها.</span><span class="sxs-lookup"><span data-stu-id="b2391-120">Here you can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="b2391-121">قم بتوسيع المقطع "قواعد السياسة‬" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="b2391-121">Expand or collapse the Policy rules section.</span></span>
6. <span data-ttu-id="b2391-122">في القائمة، ابحث عن "قاعدة السياسة" التي تم إنشاؤها في السابق.</span><span class="sxs-lookup"><span data-stu-id="b2391-122">In the list find the policy rule previously created.</span></span>
7. <span data-ttu-id="b2391-123">انقر فوق "إنشاء قاعدة السياسة".</span><span class="sxs-lookup"><span data-stu-id="b2391-123">Click Create policy rule.</span></span>
8. <span data-ttu-id="b2391-124">في الحقل "تاريخ السريان"، أدخل التاريخ الذي تريد أن تصبح فيه السياسة سارية المفعول.</span><span class="sxs-lookup"><span data-stu-id="b2391-124">In the Effective date field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="b2391-125">يسمح لك إعداد تواريخ السريان والانتهاء بإجراء تغييرات مستقبلية على قواعد السياسة وإزالة الحاجة إلى الرجوع إلى السياسة عندما تريد أن تصبح هذه التغييرات نافذة المفعول.</span><span class="sxs-lookup"><span data-stu-id="b2391-125">Setting effective and end dates allows you to make future changes to policy rules and removing the need to come back to the policy when you want those changes to take effect.</span></span>  
9. 
    * <span data-ttu-id="b2391-126">على سبيل المثال، إذا أردت تطبيق القاعدة فقط على "مديري المبيعات"، فيمكنك إنشاء عبارة Where للقول: حيث يساوي وصف المنصب "مدير المبيعات".</span><span class="sxs-lookup"><span data-stu-id="b2391-126">For example if you wanted the rule to only apply to Sales Managers you could create the Where clause to say: Where position description equals Sales Manager.</span></span>  <span data-ttu-id="b2391-127">يمكنك أن تضيف معًا عبارات And أو Or وعبارات Where متعددة في القاعدة.</span><span class="sxs-lookup"><span data-stu-id="b2391-127">You can And or Or multiple Where statements together in the rule.</span></span>  
10. <span data-ttu-id="b2391-128">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b2391-128">Click OK.</span></span>
11. <span data-ttu-id="b2391-129">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b2391-129">Close the page.</span></span>
12. <span data-ttu-id="b2391-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b2391-130">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="b2391-131">تعيين قاعدة لميزة</span><span class="sxs-lookup"><span data-stu-id="b2391-131">Assign rule to benefit</span></span>
1. <span data-ttu-id="b2391-132">انتقل إلى الموارد البشرية > الميزات‬ > الميزات‬.</span><span class="sxs-lookup"><span data-stu-id="b2391-132">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="b2391-133">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="b2391-133">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b2391-134">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b2391-134">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b2391-135">قم بتوسيع القسم "قواعد الاستحقاق" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="b2391-135">Expand or collapse the Eligibility rules section.</span></span>
5. <span data-ttu-id="b2391-136">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="b2391-136">Click Edit.</span></span>
6. <span data-ttu-id="b2391-137">في حقل "الأهلية"، حدد "على أساس القاعدة" من القائمة.</span><span class="sxs-lookup"><span data-stu-id="b2391-137">In the Eligibility field, select Rule based from the list.</span></span>
7. <span data-ttu-id="b2391-138">في الحقل "نوع القاعدة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="b2391-138">In the Rule type field, click the drop down button to open the lookup.</span></span>
8. <span data-ttu-id="b2391-139">في القائمة، ابحث عن القاعدة التي تم إنشاؤها في السابق وحددها.</span><span class="sxs-lookup"><span data-stu-id="b2391-139">In the list find and select the rule you previously created.</span></span>
9. <span data-ttu-id="b2391-140">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b2391-140">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="b2391-141">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b2391-141">Click Save.</span></span>
11. <span data-ttu-id="b2391-142">وقم بغلق النموذج.</span><span class="sxs-lookup"><span data-stu-id="b2391-142">Close the form.</span></span>

