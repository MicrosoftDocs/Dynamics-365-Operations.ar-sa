---
title: تسجيل ميزات للعاملين وإزالتها منهم
description: يوضح هذا الإجراء كيف يمكن تسجيل عامل واحد في ميزة واحدة أو أكثر، بالإضافة إلى كيفية تسجيل عاملين متعددين في إحدى الميزات.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmWorkerEnrollment, HcmBenefitByEligibilityLookup, HcmMassBenefitEnrollment, HcmBenefitLookup, HcmMassBenefitEnrollmentResults
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92da6d24f3fc4282de5673a8155b6ab6316e55aa
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510418"
---
# <a name="enroll-and-remove-benefits-from-workers"></a><span data-ttu-id="b2101-103">تسجيل ميزات للعاملين وإزالتها منهم</span><span class="sxs-lookup"><span data-stu-id="b2101-103">Enroll and remove benefits from workers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b2101-104">يوضح هذا الإجراء كيف يمكن تسجيل عامل واحد في ميزة واحدة أو أكثر، بالإضافة إلى كيفية تسجيل عاملين متعددين في إحدى الميزات.</span><span class="sxs-lookup"><span data-stu-id="b2101-104">This procedure demonstrates how a single worker can be enrolled in one or more benefits, as well as multiple workers can be enrolled in a benefit.</span></span> <span data-ttu-id="b2101-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="b2101-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="enroll-a-single-worker-in-benefits"></a><span data-ttu-id="b2101-106">تسجيل عامل واحد للحصول على الميزات</span><span class="sxs-lookup"><span data-stu-id="b2101-106">Enroll a single worker in benefits</span></span>
1. <span data-ttu-id="b2101-107">انتقل إلى الموارد البشرية > العاملون > الموظفون</span><span class="sxs-lookup"><span data-stu-id="b2101-107">Go to Human resources > Workers > Employees</span></span>
2. <span data-ttu-id="b2101-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="b2101-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b2101-109">انقر فوق "الميزات".</span><span class="sxs-lookup"><span data-stu-id="b2101-109">Click Benefits.</span></span>
4. <span data-ttu-id="b2101-110">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="b2101-110">Click New.</span></span>
5. <span data-ttu-id="b2101-111">في الحقل "الميزة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="b2101-111">In the Benefit field, enter or select a value.</span></span>
6. <span data-ttu-id="b2101-112">في الحقل "بداية التغطية"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="b2101-112">In the Coverage start date field, enter a date and time.</span></span>
7. <span data-ttu-id="b2101-113">في الحقل "نهاية التغطية"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="b2101-113">In the Coverage end date field, enter a date and time.</span></span>
8. <span data-ttu-id="b2101-114">قم بتوسيع القسم "المستفيدين" في حالة احتاج المستفيدون إلى إضافتهم للميزة.</span><span class="sxs-lookup"><span data-stu-id="b2101-114">Expand the Beneficiaries section if beneficiaries need to be added to the benefit.</span></span> <span data-ttu-id="b2101-115">ويمكنك أيضا إضافة المعالين من هذه الصفحة للميزة أن أمكن.</span><span class="sxs-lookup"><span data-stu-id="b2101-115">You can also add dependents from this page if applicable to the benefit.</span></span>
9. <span data-ttu-id="b2101-116">ويمكنك أيضا تحرير تفاصيل التسجيل في إحدى الميزات أو حذف تسجيل في هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b2101-116">You can also edit the details of a benefit enrollment or delete an enrollment on this page.</span></span> <span data-ttu-id="b2101-117">عند الانتهاء من إجراء التغييرات على التسجيل في الميزات، أغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b2101-117">When you have finished making changes to the benefit enrollment, close the page.</span></span>

## <a name="enroll-multiple-workers-in-a-benefit"></a><span data-ttu-id="b2101-118">تسجيل عدة عمال في أحد الميزات</span><span class="sxs-lookup"><span data-stu-id="b2101-118">Enroll multiple workers in a benefit</span></span>
1. <span data-ttu-id="b2101-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b2101-119">Close the page.</span></span>
2. <span data-ttu-id="b2101-120">انتقل إلى الموارد البشرية > العاملون > الموظفون</span><span class="sxs-lookup"><span data-stu-id="b2101-120">Go to Human resources > Workers > Employees</span></span>
3. <span data-ttu-id="b2101-121">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b2101-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b2101-122">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="b2101-122">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b2101-123">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="b2101-123">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="b2101-124">انقر فوق "التسجيل في الميزات".</span><span class="sxs-lookup"><span data-stu-id="b2101-124">Click Enroll in benefits.</span></span>
7. <span data-ttu-id="b2101-125">في الحقل "الميزة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="b2101-125">In the Benefit field, enter or select a value.</span></span>
8. <span data-ttu-id="b2101-126">في الحقل "بداية التغطية"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="b2101-126">In the Coverage start date field, enter a date and time.</span></span>
9. <span data-ttu-id="b2101-127">في الحقل "نهاية التغطية"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="b2101-127">In the Coverage end date field, enter a date and time.</span></span>
10. <span data-ttu-id="b2101-128">انقر فوق "تسجيل".</span><span class="sxs-lookup"><span data-stu-id="b2101-128">Click Enroll.</span></span>
11. <span data-ttu-id="b2101-129">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b2101-129">Close the page.</span></span>
12. <span data-ttu-id="b2101-130">انتقل إلى الموارد البشرية > الميزات‬ > التسجيل > نتائج التسجيل في الميزات‬.</span><span class="sxs-lookup"><span data-stu-id="b2101-130">Go to Human Resources > Benefits > Enrollment > Benefit enrollment results</span></span>
13. <span data-ttu-id="b2101-131">ابحث عن سجل نتائج الميزات الذي تبحث عنه.</span><span class="sxs-lookup"><span data-stu-id="b2101-131">Find the benefit results record that you are looking for.</span></span>
14. <span data-ttu-id="b2101-132">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b2101-132">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="b2101-133">تسمح لك هذه الصفحة بعرض الموظفين الذين تم تسجيلهم في الميزة بالإضافة إلى أي موظفين لم يكونوا مسجلين.</span><span class="sxs-lookup"><span data-stu-id="b2101-133">This page allows you to view which employees have been enrolled in the benefit, as well as any employees who were not enrolled.</span></span>

