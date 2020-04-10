---
title: إنشاء وتعيين سياسة تخصيص التكلفة إلى وحدة التحكم في التكلفة
description: استخدم هذا الإجراء لإنشاء سياسة توزيع التكلفة‬ والقواعد المناظرة وتعيينها إلى وحدة التحكم بالتكاليف.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a4ba39b5dbba20a58066054da2e24613381cfaa
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144417"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="3a781-103">إنشاء وتعيين سياسة تخصيص التكلفة إلى وحدة التحكم في التكلفة</span><span class="sxs-lookup"><span data-stu-id="3a781-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3a781-104">استخدم هذا الإجراء لإنشاء سياسة توزيع التكلفة‬ والقواعد المناظرة وتعيينها إلى وحدة التحكم بالتكاليف.</span><span class="sxs-lookup"><span data-stu-id="3a781-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="3a781-105">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USP2.</span><span class="sxs-lookup"><span data-stu-id="3a781-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="3a781-106">إنشاء سياسة</span><span class="sxs-lookup"><span data-stu-id="3a781-106">Create a policy</span></span>
1. <span data-ttu-id="3a781-107">انتقل إلى محاسبة التكاليف > السياسات > سياسات توزيع التكاليف.</span><span class="sxs-lookup"><span data-stu-id="3a781-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="3a781-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3a781-108">Click New.</span></span>
3. <span data-ttu-id="3a781-109">في الحقل "اسم السياسة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3a781-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="3a781-110">في الحقل "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a781-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="3a781-111">حدد "المؤسسة".</span><span class="sxs-lookup"><span data-stu-id="3a781-111">Select Organization.</span></span>  
5. <span data-ttu-id="3a781-112">في الحقل "البعد الإحصائي"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a781-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="3a781-113">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3a781-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="3a781-114">إنشاء قواعد التوزيع</span><span class="sxs-lookup"><span data-stu-id="3a781-114">Create allocation rules</span></span>
1. <span data-ttu-id="3a781-115">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3a781-115">Click New.</span></span>
2. <span data-ttu-id="3a781-116">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3a781-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="3a781-117">في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a781-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="3a781-118">حدد "إجمالي" في حقل "سلوك التكلفة".</span><span class="sxs-lookup"><span data-stu-id="3a781-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="3a781-119">في الحقل "أساس التوزيع"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="3a781-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="3a781-120">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3a781-120">Click New.</span></span>
7. <span data-ttu-id="3a781-121">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3a781-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="3a781-122">في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a781-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="3a781-123">حدد "إجمالي" في حقل "سلوك التكلفة".</span><span class="sxs-lookup"><span data-stu-id="3a781-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="3a781-124">في الحقل "أساس التوزيع"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="3a781-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="3a781-125">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3a781-125">Click New.</span></span>
12. <span data-ttu-id="3a781-126">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3a781-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="3a781-127">في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a781-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="3a781-128">حدد "إجمالي" في حقل "سلوك التكلفة".</span><span class="sxs-lookup"><span data-stu-id="3a781-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="3a781-129">في الحقل "أساس التوزيع"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="3a781-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="3a781-130">تابع حتى إنشاء كافة القواعد.</span><span class="sxs-lookup"><span data-stu-id="3a781-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="3a781-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3a781-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="3a781-132">تعيين السياسة إلى وحدة التحكم بالتكاليف</span><span class="sxs-lookup"><span data-stu-id="3a781-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="3a781-133">انقر فوق "تعيينات السياسة" لوحدة التحكم بالتكاليف.</span><span class="sxs-lookup"><span data-stu-id="3a781-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="3a781-134">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3a781-134">Click New.</span></span>
3. <span data-ttu-id="3a781-135">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3a781-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="3a781-136">أدخل تاريخًا في الحقل "صالح بدءًا من تاريخ المحاسبة‬‬".</span><span class="sxs-lookup"><span data-stu-id="3a781-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="3a781-137">القواعد لها تاريخ سريان.</span><span class="sxs-lookup"><span data-stu-id="3a781-137">The rules are date-effective.</span></span> <span data-ttu-id="3a781-138">باستطاعة المستخدم أو النظام إنهاء تاريخ صلاحية القواعد إذا تم إنشاء إصدار أحدث.</span><span class="sxs-lookup"><span data-stu-id="3a781-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="3a781-139">في الحقل "وحدة التحكم بالتكاليف‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3a781-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="3a781-140">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3a781-140">Click Save.</span></span>

