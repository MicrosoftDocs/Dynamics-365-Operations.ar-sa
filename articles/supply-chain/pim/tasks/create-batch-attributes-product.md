--- 
title: "إنشاء مواصفات التشغيلة لمنتج"
description: "يوضح هذا الإجراء كيفية إنشاء مواصفات التشغيلة وتعيين نطاقات القيم الافتراضية وتضمين السمة في مجموعة."
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fcd0afb8005f1712b08f0854613573ef04c0cad6
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="1300b-103">إنشاء مواصفات التشغيلة لمنتج</span><span class="sxs-lookup"><span data-stu-id="1300b-103">Create batch attributes for a product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1300b-104">يوضح هذا الإجراء كيفية إنشاء مواصفات التشغيلة وتعيين نطاقات القيم الافتراضية وتضمين السمة في مجموعة.</span><span class="sxs-lookup"><span data-stu-id="1300b-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="1300b-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي شركة USP2.</span><span class="sxs-lookup"><span data-stu-id="1300b-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="1300b-106">انتقل إلى إدارة المخزون > إعداد > الدُفعة‬‬ > سمات الدُفعة‬.</span><span class="sxs-lookup"><span data-stu-id="1300b-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="1300b-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="1300b-107">Click New.</span></span>
3. <span data-ttu-id="1300b-108">في الحقل "السمة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1300b-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="1300b-109">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1300b-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1300b-110">في الحقل "نوع السمة"، حدد "كسر‬".</span><span class="sxs-lookup"><span data-stu-id="1300b-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="1300b-111">يستخدم هذا الإجراء نوع الكسر لتمكين القيم العشرية.</span><span class="sxs-lookup"><span data-stu-id="1300b-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="1300b-112">يمكنك تحديد أنواع سمات أخرى.</span><span class="sxs-lookup"><span data-stu-id="1300b-112">You can select other attribute types.</span></span> <span data-ttu-id="1300b-113">إذا قمت بتحديد نوع "التعداد"، فيجب إدخال قيم في قائمة التعداد قبل أن تتمكن من إدخال قيمة في الحقل "الهدف".</span><span class="sxs-lookup"><span data-stu-id="1300b-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="1300b-114">في الحقل "الحد الأدنى‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1300b-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="1300b-115">في الحقل "الحد الأقصى، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1300b-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="1300b-116">في الحقل "الزيادة‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1300b-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="1300b-117">في الحقل "الهدف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1300b-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="1300b-118">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="1300b-118">Click Save.</span></span>
11. <span data-ttu-id="1300b-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1300b-119">Close the page.</span></span>
12. <span data-ttu-id="1300b-120">انتقل إلى إدارة المخزون > إعداد > الدُفعة‬‬ > مجموعات مواصفات التشغيلة‬.‬</span><span class="sxs-lookup"><span data-stu-id="1300b-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="1300b-121">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="1300b-121">Click New.</span></span>
14. <span data-ttu-id="1300b-122">في الحقل "مجموعة السمات‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1300b-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="1300b-123">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1300b-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="1300b-124">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="1300b-124">Click Save.</span></span>
17. <span data-ttu-id="1300b-125">انقر فوق سمات المجموعة .</span><span class="sxs-lookup"><span data-stu-id="1300b-125">Click Group attributes.</span></span>
18. <span data-ttu-id="1300b-126">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="1300b-126">Click New.</span></span>
19. <span data-ttu-id="1300b-127">في الحقل "السمة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="1300b-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="1300b-128">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="1300b-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="1300b-129">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1300b-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1300b-130">يمكن تضمين سمة في أي من المجموعات.</span><span class="sxs-lookup"><span data-stu-id="1300b-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="1300b-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="1300b-131">Click Save.</span></span>
23. <span data-ttu-id="1300b-132">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1300b-132">Close the page.</span></span>


