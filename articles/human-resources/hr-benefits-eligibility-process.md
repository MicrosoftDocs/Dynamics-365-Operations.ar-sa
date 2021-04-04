---
title: عملية استحقاق الميزات
description: يوضح هذا الإجراء كيف تعمل عملية استحقاق الميزات.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 3720adf26d2cb942bc5d9f6988641bf5e504a852
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465116"
---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="7e440-103">عملية استحقاق الميزات</span><span class="sxs-lookup"><span data-stu-id="7e440-103">Benefit eligibility process</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7e440-104">يوضح هذا الإجراء كيف تعمل عملية استحقاق الميزات.</span><span class="sxs-lookup"><span data-stu-id="7e440-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="7e440-105">عند اكتمال العملية، يمكنك عرض النتائج.</span><span class="sxs-lookup"><span data-stu-id="7e440-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="7e440-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="7e440-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="7e440-107">انتقل إلى الموارد البشرية > الميزات‬ > الميزات‬.</span><span class="sxs-lookup"><span data-stu-id="7e440-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="7e440-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="7e440-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7e440-109">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="7e440-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7e440-110">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="7e440-110">Click Edit.</span></span>
5. <span data-ttu-id="7e440-111">في حقل الأهلية، حدد "على أساس القاعدة".</span><span class="sxs-lookup"><span data-stu-id="7e440-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="7e440-112">في حقل نوع القاعدة، حدد قاعدة سياسة الميزات التي ترغب في تطبيقها على الميزات.</span><span class="sxs-lookup"><span data-stu-id="7e440-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="7e440-113">في جزء الإجراءات، انقر فوق "ميزة".</span><span class="sxs-lookup"><span data-stu-id="7e440-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="7e440-114">انقر فوق "إنشاء ‏‫حدث استحقاق" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="7e440-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="7e440-115">في حقل "الحدث"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7e440-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="7e440-116">في حقل "الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7e440-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="7e440-117">في حقل "نوع الحدث"، حدد "‏‫تسجيل مفتوح‬".</span><span class="sxs-lookup"><span data-stu-id="7e440-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="7e440-118">في الحقل "بداية التغطية"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="7e440-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="7e440-119">في حقل "‏‫تاريخ بدء فترة التسجيل‬‬"، أدخل التاريخ والوقت.</span><span class="sxs-lookup"><span data-stu-id="7e440-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="7e440-120">في حقل "‏‫الأيام المتبقية للتسجيل"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="7e440-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="7e440-121">انقر فوق "إنشاء حدث".</span><span class="sxs-lookup"><span data-stu-id="7e440-121">Click Create event.</span></span>
16. <span data-ttu-id="7e440-122">انقر فوق "إضافة" ‏‫في علامة التبويب السريعة "العاملون".</span><span class="sxs-lookup"><span data-stu-id="7e440-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="7e440-123">في حقل "عرض حسب النوع"، حدد "الموظفون".</span><span class="sxs-lookup"><span data-stu-id="7e440-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="7e440-124">في حقل "عرض حسب الكيان القانوني"، حدد "الكيان القانوني الحالي".</span><span class="sxs-lookup"><span data-stu-id="7e440-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="7e440-125">في القائمة، قم بوضع علامة أو إلغاء علامة كل الصفوف.</span><span class="sxs-lookup"><span data-stu-id="7e440-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="7e440-126">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7e440-126">Click OK.</span></span>
21. <span data-ttu-id="7e440-127">انقر فوق "معالجة".</span><span class="sxs-lookup"><span data-stu-id="7e440-127">Click Process.</span></span>
22. <span data-ttu-id="7e440-128">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7e440-128">Click OK.</span></span>
23. <span data-ttu-id="7e440-129">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7e440-129">Refresh the page.</span></span>
24. <span data-ttu-id="7e440-130">انقر فوق "إظهار النتائج".</span><span class="sxs-lookup"><span data-stu-id="7e440-130">Click Show results.</span></span>
25. <span data-ttu-id="7e440-131">فتح عامل تصفية عمود الحالة.</span><span class="sxs-lookup"><span data-stu-id="7e440-131">Open Status column filter.</span></span>
26. <span data-ttu-id="7e440-132">فرز من A إلى Z</span><span class="sxs-lookup"><span data-stu-id="7e440-132">Sort A to Z</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]