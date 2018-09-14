--- 
title: "عملية استحقاق الميزات"
description: "يوضح هذا الإجراء كيف تعمل عملية استحقاق المزايا."
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: edfb5872b0c64d59b842f6e532a17605e5ff6fbb
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="fd424-103">عملية استحقاق الميزات</span><span class="sxs-lookup"><span data-stu-id="fd424-103">Benefit eligibility process</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fd424-104">يوضح هذا الإجراء كيف تعمل عملية استحقاق المزايا.</span><span class="sxs-lookup"><span data-stu-id="fd424-104">This procedure hows the benefit eligibility process works.</span></span> <span data-ttu-id="fd424-105">عند اكتمال العملية، يمكنك عرض النتائج.</span><span class="sxs-lookup"><span data-stu-id="fd424-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="fd424-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="fd424-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="fd424-107">انتقل إلى الموارد البشرية > الميزات‬ > الميزات‬.</span><span class="sxs-lookup"><span data-stu-id="fd424-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="fd424-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="fd424-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="fd424-109">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="fd424-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="fd424-110">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="fd424-110">Click Edit.</span></span>
5. <span data-ttu-id="fd424-111">في حقل الأهلية، حدد "على أساس القاعدة".</span><span class="sxs-lookup"><span data-stu-id="fd424-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="fd424-112">في حقل نوع القاعدة، حدد قاعدة سياسة المزايا التي ترغب في تطبيقها على المزايا.</span><span class="sxs-lookup"><span data-stu-id="fd424-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="fd424-113">في جزء الإجراءات، انقر فوق "ميزة".</span><span class="sxs-lookup"><span data-stu-id="fd424-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="fd424-114">انقر فوق "إنشاء ‏‫حدث استحقاق" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="fd424-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="fd424-115">في حقل "الحدث"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="fd424-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="fd424-116">في حقل "الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="fd424-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="fd424-117">في حقل "نوع الحدث"، حدد "‏‫تسجيل مفتوح‬".</span><span class="sxs-lookup"><span data-stu-id="fd424-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="fd424-118">في الحقل "بداية التغطية"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="fd424-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="fd424-119">في حقل "‏‫تاريخ بدء فترة التسجيل‬‬"، أدخل التاريخ والوقت.</span><span class="sxs-lookup"><span data-stu-id="fd424-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="fd424-120">في حقل "‏‫الأيام المتبقية للتسجيل"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="fd424-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="fd424-121">انقر فوق "إنشاء حدث".</span><span class="sxs-lookup"><span data-stu-id="fd424-121">Click Create event.</span></span>
16. <span data-ttu-id="fd424-122">انقر فوق "إضافة" ‏‫في علامة التبويب السريعة "العاملون".</span><span class="sxs-lookup"><span data-stu-id="fd424-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="fd424-123">في حقل "عرض حسب النوع"، حدد "الموظفون".</span><span class="sxs-lookup"><span data-stu-id="fd424-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="fd424-124">في حقل "عرض حسب الكيان القانوني"، حدد "الكيان القانوني الحالي".</span><span class="sxs-lookup"><span data-stu-id="fd424-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="fd424-125">في القائمة، قم بوضع علامة أو إلغاء علامة كل الصفوف.</span><span class="sxs-lookup"><span data-stu-id="fd424-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="fd424-126">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="fd424-126">Click OK.</span></span>
21. <span data-ttu-id="fd424-127">انقر فوق "معالجة".</span><span class="sxs-lookup"><span data-stu-id="fd424-127">Click Process.</span></span>
22. <span data-ttu-id="fd424-128">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="fd424-128">Click OK.</span></span>
23. <span data-ttu-id="fd424-129">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fd424-129">Refresh the page.</span></span>
24. <span data-ttu-id="fd424-130">انقر فوق "إظهار النتائج".</span><span class="sxs-lookup"><span data-stu-id="fd424-130">Click Show results.</span></span>
25. <span data-ttu-id="fd424-131">فتح عامل تصفية عمود الحالة.</span><span class="sxs-lookup"><span data-stu-id="fd424-131">Open Status column filter.</span></span>
26. <span data-ttu-id="fd424-132">فرز من A إلى Z</span><span class="sxs-lookup"><span data-stu-id="fd424-132">Sort A to Z</span></span>


