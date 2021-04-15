---
title: تحديد قواعد وسياسات استحقاق الفائدة
description: يوضح لك هذا المقال كيف يمكنك إنشاء قواعد وسياسات أهلية الميزة ثم تعيين القواعد للمزايا.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: df517e1ab72634cb434411fab3bd92bf34c7e609
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805936"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="19953-103">تحديد قواعد وسياسات استحقاق الفائدة</span><span class="sxs-lookup"><span data-stu-id="19953-103">Define benefit eligibility rules and policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="19953-104">يوضح لك هذا الموضوع كيف يمكنك إنشاء قواعد وسياسات أهلية الميزة ثم تعيين القواعد للمزايا.</span><span class="sxs-lookup"><span data-stu-id="19953-104">This topic shows you how you can create benefit eligibility rules and policies and then assign rules to benefits.</span></span>  

## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="19953-105">إنشاء نوع قاعدة سياسة استحقاق المزايا‬</span><span class="sxs-lookup"><span data-stu-id="19953-105">Create benefit eligibility policy rule type</span></span>

1. <span data-ttu-id="19953-106">انتقل إلى **الموارد البشرية > الميزات > الأهلية > أنواع قواعد سياسات استحقاق الميزات**.</span><span class="sxs-lookup"><span data-stu-id="19953-106">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policy rule types**.</span></span>
2. <span data-ttu-id="19953-107">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="19953-107">Select **New**.</span></span>
3. <span data-ttu-id="19953-108">في حقل **‏‫اسم القاعدة**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="19953-108">In the **Rule name** field, enter a value.</span></span>
4. <span data-ttu-id="19953-109">في حقل **الوصف**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="19953-109">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="19953-110">في الحقل  **اسم الاستعلام**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="19953-110">In the **Query name** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="19953-111">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="19953-111">In the list, select the link in the selected row.</span></span>
7. <span data-ttu-id="19953-112">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="19953-112">Select **Save**.</span></span>
8. <span data-ttu-id="19953-113">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="19953-113">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="19953-114">سياسة استحقاق المزايا</span><span class="sxs-lookup"><span data-stu-id="19953-114">Benefit eligibility policy</span></span>

1. <span data-ttu-id="19953-115">انتقل إلى **الموارد البشرية > الميزات > الأهلية > سياسات استحقاق الميزات‬**.</span><span class="sxs-lookup"><span data-stu-id="19953-115">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policies**.</span></span>
2. <span data-ttu-id="19953-116">حدد سياسة ميزات موجودة.</span><span class="sxs-lookup"><span data-stu-id="19953-116">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="19953-117">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="19953-117">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="19953-118">قم بتبديل توسيع الأقسام **مؤسسات السياسات‬‬**.</span><span class="sxs-lookup"><span data-stu-id="19953-118">Toggle the expansion of the **Policy organizations** sections.</span></span> <span data-ttu-id="19953-119">يمكنك إضافة أي من المؤسسات التي تريد تضمينها في السياسة أو إزالتها.</span><span class="sxs-lookup"><span data-stu-id="19953-119">You can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="19953-120">قم بتوسيع المقطع **قواعد السياسة‬** أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="19953-120">Expand or collapse the **Policy rules** section.</span></span>
6. <span data-ttu-id="19953-121">في القائمة، ابحث عن "قاعدة السياسة" التي تم إنشاؤها في السابق.</span><span class="sxs-lookup"><span data-stu-id="19953-121">In the list, find the policy rule previously created.</span></span>
7. <span data-ttu-id="19953-122">حدد **إنشاء قاعدة السياسة**.</span><span class="sxs-lookup"><span data-stu-id="19953-122">Select **Create policy rule**.</span></span>
8. <span data-ttu-id="19953-123">في الحقل **تاريخ السريان**، أدخل التاريخ الذي تريد أن تصبح فيه السياسة سارية المفعول.</span><span class="sxs-lookup"><span data-stu-id="19953-123">In the **Effective date** field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="19953-124">يسمح لك إعداد تواريخ السريان والانتهاء بإجراء تغييرات مستقبلية على قواعد السياسة ومن ثم لا تحتاج إلى الرجوع إلى السياسة عندما تريد أن تصبح هذه التغييرات نافذة المفعول.</span><span class="sxs-lookup"><span data-stu-id="19953-124">Setting effective end dates allows you to make future changes to policy rules so you don't need to come back to the policy when you want those changes to take effect.</span></span>  
9. <span data-ttu-id="19953-125">إذا لزم الأمر ، قم بإضافة جملة where إلى حقل **إضافة شرط**.</span><span class="sxs-lookup"><span data-stu-id="19953-125">If needed, add a where clause to the **Add condition** field.</span></span>
    * <span data-ttu-id="19953-126">على سبيل المثال، إذا أردت تطبيق القاعدة فقط على "مديري المبيعات"، فيمكنك إنشاء عبارة where للقول: حيث يساوي وصف المنصب "مدير المبيعات".</span><span class="sxs-lookup"><span data-stu-id="19953-126">For example if you wanted the rule to only apply to Sales Managers you could create the where clause to say: Where position description equals Sales Manager.</span></span> <span data-ttu-id="19953-127">يمكنك أن تضيف عبارات where متعددة في القاعدة.</span><span class="sxs-lookup"><span data-stu-id="19953-127">You can add multiple where statements together in the rule.</span></span>  
10. <span data-ttu-id="19953-128">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="19953-128">Select **OK**.</span></span>
11. <span data-ttu-id="19953-129">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="19953-129">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="19953-130">تعيين قاعدة لميزة</span><span class="sxs-lookup"><span data-stu-id="19953-130">Assign rule to benefit</span></span>

1. <span data-ttu-id="19953-131">انتقل إلى **الموارد البشرية > الميزات‬ > الميزات‬**.</span><span class="sxs-lookup"><span data-stu-id="19953-131">Go to **Human resources > Benefits > Benefits**.</span></span>
2. <span data-ttu-id="19953-132">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="19953-132">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="19953-133">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="19953-133">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="19953-134">قم بتوسيع القسم **قواعد الاستحقاق** أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="19953-134">Expand or collapse the **Eligibility rules** section.</span></span>
5. <span data-ttu-id="19953-135">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="19953-135">Select **Edit**.</span></span>
6. <span data-ttu-id="19953-136">في حقل **الأهلية**، حدد القاعدة.</span><span class="sxs-lookup"><span data-stu-id="19953-136">In the **Eligibility** field, select the rule.</span></span>
7. <span data-ttu-id="19953-137">في الحقل **نوع القاعدة**، حدد القاعدة التي أنشأتها في السابق.</span><span class="sxs-lookup"><span data-stu-id="19953-137">In the **Rule type** field, select the rule you previously created.</span></span>
9. <span data-ttu-id="19953-138">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="19953-138">In the list, select the link in the selected row.</span></span>
10. <span data-ttu-id="19953-139">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="19953-139">Select **Save**.</span></span>
11. <span data-ttu-id="19953-140">وقم بغلق النموذج.</span><span class="sxs-lookup"><span data-stu-id="19953-140">Close the form.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]