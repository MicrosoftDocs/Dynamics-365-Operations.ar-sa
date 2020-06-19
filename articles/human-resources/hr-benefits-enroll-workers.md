---
title: تسجيل ميزات للعاملين وإزالتها منهم
description: يوضح هذا الإجراء كيف يمكن تسجيل عامل واحد في ميزة واحدة أو أكثر، بالإضافة إلى كيفية تسجيل عاملين متعددين في إحدى الميزات.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmWorkerEnrollment, HcmBenefitByEligibilityLookup, HcmMassBenefitEnrollment, HcmBenefitLookup, HcmMassBenefitEnrollmentResults, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 36fd724ff27cbb646f3f8a35ca1b30dc86a5afe4
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430775"
---
# <a name="enroll-and-remove-benefits-from-workers"></a><span data-ttu-id="cbb51-103">تسجيل ميزات للعاملين وإزالتها منهم</span><span class="sxs-lookup"><span data-stu-id="cbb51-103">Enroll and remove benefits from workers</span></span>



<span data-ttu-id="cbb51-104">يوضح هذا الإجراء كيف يمكن تسجيل عامل واحد في ميزة واحدة أو أكثر، بالإضافة إلى كيفية تسجيل عاملين متعددين في إحدى الميزات.</span><span class="sxs-lookup"><span data-stu-id="cbb51-104">This procedure demonstrates how a single worker can be enrolled in one or more benefits, as well as multiple workers can be enrolled in a benefit.</span></span> <span data-ttu-id="cbb51-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="cbb51-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="enroll-a-single-worker-in-benefits"></a><span data-ttu-id="cbb51-106">تسجيل عامل واحد للحصول على الميزات</span><span class="sxs-lookup"><span data-stu-id="cbb51-106">Enroll a single worker in benefits</span></span>
1. <span data-ttu-id="cbb51-107">انتقل إلى الموارد البشرية > العاملون > الموظفون</span><span class="sxs-lookup"><span data-stu-id="cbb51-107">Go to Human resources > Workers > Employees</span></span>
2. <span data-ttu-id="cbb51-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="cbb51-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="cbb51-109">انقر فوق "الميزات".</span><span class="sxs-lookup"><span data-stu-id="cbb51-109">Click Benefits.</span></span>
4. <span data-ttu-id="cbb51-110">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="cbb51-110">Click New.</span></span>
5. <span data-ttu-id="cbb51-111">في الحقل "الميزة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cbb51-111">In the Benefit field, enter or select a value.</span></span>
6. <span data-ttu-id="cbb51-112">في الحقل "بداية التغطية"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="cbb51-112">In the Coverage start date field, enter a date and time.</span></span>
7. <span data-ttu-id="cbb51-113">في الحقل "نهاية التغطية"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="cbb51-113">In the Coverage end date field, enter a date and time.</span></span>
8. <span data-ttu-id="cbb51-114">قم بتوسيع القسم "المستفيدين" في حالة احتاج المستفيدون إلى إضافتهم للميزة.</span><span class="sxs-lookup"><span data-stu-id="cbb51-114">Expand the Beneficiaries section if beneficiaries need to be added to the benefit.</span></span> <span data-ttu-id="cbb51-115">ويمكنك أيضا إضافة المعالين من هذه الصفحة للميزة أن أمكن.</span><span class="sxs-lookup"><span data-stu-id="cbb51-115">You can also add dependents from this page if applicable to the benefit.</span></span>
9. <span data-ttu-id="cbb51-116">ويمكنك أيضا تحرير تفاصيل التسجيل في إحدى الميزات أو حذف تسجيل في هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cbb51-116">You can also edit the details of a benefit enrollment or delete an enrollment on this page.</span></span> <span data-ttu-id="cbb51-117">عند الانتهاء من إجراء التغييرات على التسجيل في الميزات، أغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cbb51-117">When you have finished making changes to the benefit enrollment, close the page.</span></span>

## <a name="enroll-multiple-workers-in-a-benefit"></a><span data-ttu-id="cbb51-118">تسجيل عدة عمال في أحد الميزات</span><span class="sxs-lookup"><span data-stu-id="cbb51-118">Enroll multiple workers in a benefit</span></span>
1. <span data-ttu-id="cbb51-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cbb51-119">Close the page.</span></span>
2. <span data-ttu-id="cbb51-120">انتقل إلى الموارد البشرية > العاملون > الموظفون</span><span class="sxs-lookup"><span data-stu-id="cbb51-120">Go to Human resources > Workers > Employees</span></span>
3. <span data-ttu-id="cbb51-121">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cbb51-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="cbb51-122">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="cbb51-122">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="cbb51-123">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="cbb51-123">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="cbb51-124">انقر فوق "التسجيل في الميزات".</span><span class="sxs-lookup"><span data-stu-id="cbb51-124">Click Enroll in benefits.</span></span>
7. <span data-ttu-id="cbb51-125">في الحقل "الميزة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cbb51-125">In the Benefit field, enter or select a value.</span></span>
8. <span data-ttu-id="cbb51-126">في الحقل "بداية التغطية"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="cbb51-126">In the Coverage start date field, enter a date and time.</span></span>
9. <span data-ttu-id="cbb51-127">في الحقل "نهاية التغطية"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="cbb51-127">In the Coverage end date field, enter a date and time.</span></span>
10. <span data-ttu-id="cbb51-128">انقر فوق "تسجيل".</span><span class="sxs-lookup"><span data-stu-id="cbb51-128">Click Enroll.</span></span>
11. <span data-ttu-id="cbb51-129">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cbb51-129">Close the page.</span></span>
12. <span data-ttu-id="cbb51-130">انتقل إلى الموارد البشرية > الميزات‬ > التسجيل > نتائج التسجيل في الميزات‬.</span><span class="sxs-lookup"><span data-stu-id="cbb51-130">Go to Human Resources > Benefits > Enrollment > Benefit enrollment results</span></span>
13. <span data-ttu-id="cbb51-131">ابحث عن سجل نتائج الميزات الذي تبحث عنه.</span><span class="sxs-lookup"><span data-stu-id="cbb51-131">Find the benefit results record that you are looking for.</span></span>
14. <span data-ttu-id="cbb51-132">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cbb51-132">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="cbb51-133">تسمح لك هذه الصفحة بعرض الموظفين الذين تم تسجيلهم في الميزة بالإضافة إلى أي موظفين لم يكونوا مسجلين.</span><span class="sxs-lookup"><span data-stu-id="cbb51-133">This page allows you to view which employees have been enrolled in the benefit, as well as any employees who were not enrolled.</span></span>

