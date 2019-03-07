---
title: تسجيل ميزات للعاملين وإزالتها منهم
description: يوضح هذا الإجراء كيف يمكن تسجيل عامل واحد في ميزة واحدة أو أكثر، بالإضافة إلى كيفية تسجيل عاملين متعددين في إحدى الميزات.
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmWorkerEnrollment, HcmBenefitByEligibilityLookup, HcmMassBenefitEnrollment, HcmBenefitLookup, HcmMassBenefitEnrollmentResults
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32f0e641f5e6824df89112aa5ea21dc3a708efa0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "341846"
---
# <a name="enroll-and-remove-benefits-from-workers"></a><span data-ttu-id="9fd5a-103">تسجيل ميزات للعاملين وإزالتها منهم</span><span class="sxs-lookup"><span data-stu-id="9fd5a-103">Enroll and remove benefits from workers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9fd5a-104">يوضح هذا الإجراء كيف يمكن تسجيل عامل واحد في ميزة واحدة أو أكثر، بالإضافة إلى كيفية تسجيل عاملين متعددين في إحدى الميزات.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-104">This procedure demonstrates how a single worker can be enrolled in one or more benefits, as well as multiple workers can be enrolled in a benefit.</span></span> <span data-ttu-id="9fd5a-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="enroll-a-single-worker-in-benefits"></a><span data-ttu-id="9fd5a-106">تسجيل عامل واحد للحصول على الميزات</span><span class="sxs-lookup"><span data-stu-id="9fd5a-106">Enroll a single worker in benefits</span></span>
1. <span data-ttu-id="9fd5a-107">انتقل إلى الموارد البشرية > العاملون > الموظفون</span><span class="sxs-lookup"><span data-stu-id="9fd5a-107">Go to Human resources > Workers > Employees</span></span>
2. <span data-ttu-id="9fd5a-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9fd5a-109">انقر فوق "الميزات".</span><span class="sxs-lookup"><span data-stu-id="9fd5a-109">Click Benefits.</span></span>
4. <span data-ttu-id="9fd5a-110">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-110">Click New.</span></span>
5. <span data-ttu-id="9fd5a-111">في الحقل "الميزة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-111">In the Benefit field, enter or select a value.</span></span>
6. <span data-ttu-id="9fd5a-112">في الحقل "بداية التغطية"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-112">In the Coverage start date field, enter a date and time.</span></span>
7. <span data-ttu-id="9fd5a-113">في الحقل "نهاية التغطية"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-113">In the Coverage end date field, enter a date and time.</span></span>
8. <span data-ttu-id="9fd5a-114">قم بتوسيع القسم "المستفيدين" في حالة احتاج المستفيدون إلى إضافتهم للميزة.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-114">Expand the Beneficiaries section if beneficiaries need to be added to the benefit.</span></span> <span data-ttu-id="9fd5a-115">ويمكنك أيضا إضافة المعالين من هذه الصفحة للميزة أن أمكن.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-115">You can also add dependents from this page if applicable to the benefit.</span></span>
9. <span data-ttu-id="9fd5a-116">ويمكنك أيضا تحرير تفاصيل التسجيل في إحدى الميزات أو حذف تسجيل في هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-116">You can also edit the details of a benefit enrollment or delete an enrollment on this page.</span></span> <span data-ttu-id="9fd5a-117">عند الانتهاء من إجراء التغييرات على التسجيل في الميزات، أغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-117">When you have finished making changes to the benefit enrollment, close the page.</span></span>

## <a name="enroll-multiple-workers-in-a-benefit"></a><span data-ttu-id="9fd5a-118">تسجيل عدة عمال في أحد الميزات</span><span class="sxs-lookup"><span data-stu-id="9fd5a-118">Enroll multiple workers in a benefit</span></span>
1. <span data-ttu-id="9fd5a-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-119">Close the page.</span></span>
2. <span data-ttu-id="9fd5a-120">انتقل إلى الموارد البشرية > العاملون > الموظفون</span><span class="sxs-lookup"><span data-stu-id="9fd5a-120">Go to Human resources > Workers > Employees</span></span>
3. <span data-ttu-id="9fd5a-121">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="9fd5a-122">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-122">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="9fd5a-123">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-123">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="9fd5a-124">انقر فوق "التسجيل في الميزات".</span><span class="sxs-lookup"><span data-stu-id="9fd5a-124">Click Enroll in benefits.</span></span>
7. <span data-ttu-id="9fd5a-125">في الحقل "الميزة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-125">In the Benefit field, enter or select a value.</span></span>
8. <span data-ttu-id="9fd5a-126">في الحقل "بداية التغطية"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-126">In the Coverage start date field, enter a date and time.</span></span>
9. <span data-ttu-id="9fd5a-127">في الحقل "نهاية التغطية"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-127">In the Coverage end date field, enter a date and time.</span></span>
10. <span data-ttu-id="9fd5a-128">انقر فوق "تسجيل".</span><span class="sxs-lookup"><span data-stu-id="9fd5a-128">Click Enroll.</span></span>
11. <span data-ttu-id="9fd5a-129">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-129">Close the page.</span></span>
12. <span data-ttu-id="9fd5a-130">انتقل إلى الموارد البشرية > الميزات‬ > التسجيل > نتائج التسجيل في الميزات‬.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-130">Go to Human Resources > Benefits > Enrollment > Benefit enrollment results</span></span>
13. <span data-ttu-id="9fd5a-131">ابحث عن سجل نتائج الميزات الذي تبحث عنه.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-131">Find the benefit results record that you are looking for.</span></span>
14. <span data-ttu-id="9fd5a-132">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-132">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="9fd5a-133">تسمح لك هذه الصفحة بعرض الموظفين الذين تم تسجيلهم في الميزة بالإضافة إلى أي موظفين لم يكونوا مسجلين.</span><span class="sxs-lookup"><span data-stu-id="9fd5a-133">This page allows you to view which employees have been enrolled in the benefit, as well as any employees who were not enrolled.</span></span>

