---
title: إنشاء مواصفات التشغيلة لمنتج
description: يوضح هذا الإجراء كيفية إنشاء مواصفات التشغيلة وتعيين نطاقات القيم الافتراضية وتضمين السمة في مجموعة.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b1583bb581845aa60591436ffb8851bd52c359a5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208284"
---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="6a3b2-103">إنشاء مواصفات التشغيلة لمنتج</span><span class="sxs-lookup"><span data-stu-id="6a3b2-103">Create batch attributes for a product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6a3b2-104">يوضح هذا الإجراء كيفية إنشاء مواصفات التشغيلة وتعيين نطاقات القيم الافتراضية وتضمين السمة في مجموعة.</span><span class="sxs-lookup"><span data-stu-id="6a3b2-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="6a3b2-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي شركة USP2.</span><span class="sxs-lookup"><span data-stu-id="6a3b2-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="6a3b2-106">انتقل إلى إدارة المخزون > إعداد > الدُفعة‬‬ > سمات الدُفعة‬.</span><span class="sxs-lookup"><span data-stu-id="6a3b2-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="6a3b2-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="6a3b2-107">Click New.</span></span>
3. <span data-ttu-id="6a3b2-108">في الحقل "السمة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6a3b2-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="6a3b2-109">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6a3b2-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6a3b2-110">في الحقل "نوع السمة"، حدد "كسر‬".</span><span class="sxs-lookup"><span data-stu-id="6a3b2-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="6a3b2-111">يستخدم هذا الإجراء نوع الكسر لتمكين القيم العشرية.</span><span class="sxs-lookup"><span data-stu-id="6a3b2-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="6a3b2-112">يمكنك تحديد أنواع سمات أخرى.</span><span class="sxs-lookup"><span data-stu-id="6a3b2-112">You can select other attribute types.</span></span> <span data-ttu-id="6a3b2-113">إذا قمت بتحديد نوع "التعداد"، فيجب إدخال قيم في قائمة التعداد قبل أن تتمكن من إدخال قيمة في الحقل "الهدف".</span><span class="sxs-lookup"><span data-stu-id="6a3b2-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="6a3b2-114">في الحقل "الحد الأدنى‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="6a3b2-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="6a3b2-115">في الحقل "الحد الأقصى، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="6a3b2-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="6a3b2-116">في الحقل "الزيادة‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="6a3b2-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="6a3b2-117">في الحقل "الهدف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6a3b2-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="6a3b2-118">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="6a3b2-118">Click Save.</span></span>
11. <span data-ttu-id="6a3b2-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6a3b2-119">Close the page.</span></span>
12. <span data-ttu-id="6a3b2-120">انتقل إلى إدارة المخزون > إعداد > الدُفعة‬‬ > مجموعات مواصفات التشغيلة‬.‬</span><span class="sxs-lookup"><span data-stu-id="6a3b2-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="6a3b2-121">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="6a3b2-121">Click New.</span></span>
14. <span data-ttu-id="6a3b2-122">في الحقل "مجموعة السمات‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6a3b2-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="6a3b2-123">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6a3b2-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="6a3b2-124">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="6a3b2-124">Click Save.</span></span>
17. <span data-ttu-id="6a3b2-125">انقر فوق سمات المجموعة .</span><span class="sxs-lookup"><span data-stu-id="6a3b2-125">Click Group attributes.</span></span>
18. <span data-ttu-id="6a3b2-126">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="6a3b2-126">Click New.</span></span>
19. <span data-ttu-id="6a3b2-127">في الحقل "السمة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="6a3b2-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="6a3b2-128">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="6a3b2-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="6a3b2-129">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6a3b2-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6a3b2-130">يمكن تضمين سمة في أي من المجموعات.</span><span class="sxs-lookup"><span data-stu-id="6a3b2-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="6a3b2-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="6a3b2-131">Click Save.</span></span>
23. <span data-ttu-id="6a3b2-132">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6a3b2-132">Close the page.</span></span>

