---
title: تحديد أدوات اختيار المرشحين ونشرها
description: قد يكون البحث عن مجموعة مؤهلة تضم مرشحين لملء الوظائف الشاغرة صعبًا، لا سيما عندما يتطلب أحد المراكز مجموعة فريدة من المهارات.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmSkillMapping, HcmJobLookup, HcmSkillMappingLine, HcmPersonCertificate, CCHTMLPrintPreview
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51200a67a51097c438370866cb9d0ccbebe8392c
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/19/2019
ms.locfileid: "859081"
---
# <a name="identify-and-deploy-candidate-selection-tools"></a><span data-ttu-id="7a86c-103">تحديد أدوات اختيار المرشحين ونشرها</span><span class="sxs-lookup"><span data-stu-id="7a86c-103">Identify and deploy candidate selection tools</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7a86c-104">قد يكون البحث عن مجموعة مؤهلة تضم مرشحين لملء الوظائف الشاغرة صعبًا، لا سيما عندما يتطلب أحد المراكز مجموعة فريدة من المهارات.</span><span class="sxs-lookup"><span data-stu-id="7a86c-104">Finding a qualified pool of candidates to fill vacancies can be difficult, especially when a position requires a unique set of skills.</span></span>  <span data-ttu-id="7a86c-105">ومع ذلك، من المحتمل أن يكون قد تم توظيف مرشحين لديهم المهارات المطلوبة في مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="7a86c-105">However, candidates with the skills you need might already be employed in your organization.</span></span> <span data-ttu-id="7a86c-106">يمكنك البحث عن مجموعة مهارات معينة بين الموظفين الموجودين أو مقدمي الطلبات الجدد.</span><span class="sxs-lookup"><span data-stu-id="7a86c-106">You can search for a specific skill set among existing employees, or new applicants.</span></span> <span data-ttu-id="7a86c-107">يسمح هذا الأمر لمسؤول التعيين بجمع مقدمي الطلبات الذين تقدموا بطلبات ملء منصب مفتوح الآن أو في السابق وفحص مقدمي الطلبات هؤلاء، أو بالبحث عن المرشحين المحتملين من مجموعة موظفيهم الموجودة.</span><span class="sxs-lookup"><span data-stu-id="7a86c-107">This allows a recruiter to quickly gather and screen applicants who have applied for open position now or in the past, or to find potential candidates from their existing pool of employees.</span></span> <span data-ttu-id="7a86c-108">استخدم تسجيل هذه المهام لمعرفة كيف تساعد وظيفة تعيين المهارة في العثور على الشخص المناسب لمنصب مفتوح.</span><span class="sxs-lookup"><span data-stu-id="7a86c-108">Use this task recording to learn how the skill mapping functionality can help you find the right person for an open position.</span></span> <span data-ttu-id="7a86c-109">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="7a86c-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="7a86c-110">انتقل إلى الموارد البشرية > الاختصاصات > تحليل المهارات > ملفات تعريف تعيين المهارة.</span><span class="sxs-lookup"><span data-stu-id="7a86c-110">Go to Human resources > Competencies > Skill analysis > Skill mapping profiles.</span></span>
2. <span data-ttu-id="7a86c-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="7a86c-111">Click New.</span></span>
3. <span data-ttu-id="7a86c-112">في الحقل "تعيين المهارة"، أدخل اسمًا لتعيين المهارة الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="7a86c-112">In the Skill mapping field, enter a name for your skill mapping.</span></span>  <span data-ttu-id="7a86c-113">على سبيل المثال: محاسب.</span><span class="sxs-lookup"><span data-stu-id="7a86c-113">Example: Accountant.</span></span>
4. <span data-ttu-id="7a86c-114">في حقل "الوصف" ، أدخل وصفًا لتعيين المهارة.</span><span class="sxs-lookup"><span data-stu-id="7a86c-114">In the Description field, enter a description of the skill mapping..</span></span>
5. <span data-ttu-id="7a86c-115">في حقل "التاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="7a86c-115">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="7a86c-116">انقر فوق "استرداد ملف التعريف"</span><span class="sxs-lookup"><span data-stu-id="7a86c-116">Click Retrieve profile.</span></span>
    * <span data-ttu-id="7a86c-117">استخدم "استرداد ملف التعريف" لسحب بيانات الشهادة والمهارات والتعليم من شخص محدد أو وظيفة أو دورة تدريبية محددة كأساس للبحث.</span><span class="sxs-lookup"><span data-stu-id="7a86c-117">Use Retrieve profile to pull in the Certificate, Skill, and Education data from a selected Person, Job or Course as the basis for your search.</span></span>   <span data-ttu-id="7a86c-118">ثم يمكنك إضافة معايير أو إزالتها وتعيين ما إذا كانت المعايير اختيارية وترتيب أهمية المعايير.</span><span class="sxs-lookup"><span data-stu-id="7a86c-118">You can then add or remove criteria, state if the criteria is optional and rank the importance of the criteria.</span></span>  
7. <span data-ttu-id="7a86c-119">انقر فوق "وظيفة".</span><span class="sxs-lookup"><span data-stu-id="7a86c-119">Click Job.</span></span>
8. <span data-ttu-id="7a86c-120">في حقل "الوظيفة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="7a86c-120">In the Job field, enter or select a value.</span></span>
9. <span data-ttu-id="7a86c-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7a86c-121">Click OK.</span></span>
10. <span data-ttu-id="7a86c-122">وسّع علامة التبويب السريعة نطاق وأضف أي معلومات إضافية، مثل القسم‬.</span><span class="sxs-lookup"><span data-stu-id="7a86c-122">Expand the range fast tab, and add any additional information, such as department.</span></span>
11. <span data-ttu-id="7a86c-123">وسّع علامة التبويب السريعة "الشهادات" لعرض الشهادات أو تحريرها.</span><span class="sxs-lookup"><span data-stu-id="7a86c-123">Expand the certificates fast tab to view or edit the certificates.</span></span>
12. <span data-ttu-id="7a86c-124">وسّع علامة التبويب السريعة "المهارات" لعرض المهارات أو تحريرها.</span><span class="sxs-lookup"><span data-stu-id="7a86c-124">Expand the Skills fast tab to view or edit the skills.</span></span>
13. <span data-ttu-id="7a86c-125">وسّع علامة التبويب السريعة "التعليم‬" لعرض معايير التعليم‬ أو تحريرها.</span><span class="sxs-lookup"><span data-stu-id="7a86c-125">Expand the Education fast tab to view or edit the education criteria.</span></span>
14. <span data-ttu-id="7a86c-126">انقر فوق "تنفيذ".</span><span class="sxs-lookup"><span data-stu-id="7a86c-126">Click Execute.</span></span>
15. <span data-ttu-id="7a86c-127">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7a86c-127">Click OK.</span></span>
16. <span data-ttu-id="7a86c-128">انقر فوق "نتيجة".</span><span class="sxs-lookup"><span data-stu-id="7a86c-128">Click Result.</span></span>
17. <span data-ttu-id="7a86c-129">انقر فوق "نتيجة".</span><span class="sxs-lookup"><span data-stu-id="7a86c-129">Click Result.</span></span>
18. <span data-ttu-id="7a86c-130">وانقر فوق استئناف.</span><span class="sxs-lookup"><span data-stu-id="7a86c-130">Click Resume.</span></span>
19. <span data-ttu-id="7a86c-131">انقر فوق "الشهادات"</span><span class="sxs-lookup"><span data-stu-id="7a86c-131">Click Certificates.</span></span>
    * <span data-ttu-id="7a86c-132">يمكنك النفاذ إلى كل شخص مدرج اسمه ومشاهدة مزيد من التفاصيل بشأن التعليم والمهارات والخبرة المهنية إلخ.</span><span class="sxs-lookup"><span data-stu-id="7a86c-132">You can drill further into each person listed and see details regarding their education, skills, professional experience etc.</span></span>  
20. <span data-ttu-id="7a86c-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7a86c-133">Close the page.</span></span>
21. <span data-ttu-id="7a86c-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7a86c-134">Close the page.</span></span>
22. <span data-ttu-id="7a86c-135">حدد النتيجة مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="7a86c-135">Select result again.</span></span>
23. <span data-ttu-id="7a86c-136">انقر فوق "التقرير".</span><span class="sxs-lookup"><span data-stu-id="7a86c-136">Click Report.</span></span>
    * <span data-ttu-id="7a86c-137">يسرد التقرير أفضل المطابقات في أعلى التقرير.</span><span class="sxs-lookup"><span data-stu-id="7a86c-137">The report will list the best matches at the top of the report.</span></span>  <span data-ttu-id="7a86c-138">ويمكنك أن ترى ما إذا تم ذكر عنصر فجوة.</span><span class="sxs-lookup"><span data-stu-id="7a86c-138">You can see that there is a gap element listed.</span></span>  <span data-ttu-id="7a86c-139">هذا هو الفرق بين المستوى الذي تم إدراجه في تعيين المهارة، ومستوى المهارة التي تم تعيينها إلى الشخص.</span><span class="sxs-lookup"><span data-stu-id="7a86c-139">This is the difference between the level that was listed on the skill mapping, and the level of the skill that is assigned to the person.</span></span>  
24. <span data-ttu-id="7a86c-140">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7a86c-140">Close the page.</span></span>
25. <span data-ttu-id="7a86c-141">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="7a86c-141">Click Save.</span></span>

