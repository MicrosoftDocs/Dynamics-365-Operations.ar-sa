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
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006310d07dfa5b75941ca248736800bbb9e8e7b7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969318"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="01c4e-103">إنشاء وتعيين سياسة تخصيص التكلفة إلى وحدة التحكم في التكلفة</span><span class="sxs-lookup"><span data-stu-id="01c4e-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="01c4e-104">استخدم هذا الإجراء لإنشاء سياسة توزيع التكلفة‬ والقواعد المناظرة وتعيينها إلى وحدة التحكم بالتكاليف.</span><span class="sxs-lookup"><span data-stu-id="01c4e-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="01c4e-105">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USP2.</span><span class="sxs-lookup"><span data-stu-id="01c4e-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="01c4e-106">إنشاء سياسة</span><span class="sxs-lookup"><span data-stu-id="01c4e-106">Create a policy</span></span>
1. <span data-ttu-id="01c4e-107">انتقل إلى محاسبة التكاليف > السياسات > سياسات توزيع التكاليف.</span><span class="sxs-lookup"><span data-stu-id="01c4e-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="01c4e-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="01c4e-108">Click New.</span></span>
3. <span data-ttu-id="01c4e-109">في الحقل "اسم السياسة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="01c4e-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="01c4e-110">في الحقل "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="01c4e-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="01c4e-111">حدد "المؤسسة".</span><span class="sxs-lookup"><span data-stu-id="01c4e-111">Select Organization.</span></span>  
5. <span data-ttu-id="01c4e-112">في الحقل "البعد الإحصائي"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="01c4e-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="01c4e-113">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="01c4e-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="01c4e-114">إنشاء قواعد التوزيع</span><span class="sxs-lookup"><span data-stu-id="01c4e-114">Create allocation rules</span></span>
1. <span data-ttu-id="01c4e-115">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="01c4e-115">Click New.</span></span>
2. <span data-ttu-id="01c4e-116">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="01c4e-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="01c4e-117">في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="01c4e-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="01c4e-118">حدد "إجمالي" في حقل "سلوك التكلفة".</span><span class="sxs-lookup"><span data-stu-id="01c4e-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="01c4e-119">في الحقل "أساس التوزيع"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="01c4e-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="01c4e-120">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="01c4e-120">Click New.</span></span>
7. <span data-ttu-id="01c4e-121">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="01c4e-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="01c4e-122">في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="01c4e-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="01c4e-123">حدد "إجمالي" في حقل "سلوك التكلفة".</span><span class="sxs-lookup"><span data-stu-id="01c4e-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="01c4e-124">في الحقل "أساس التوزيع"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="01c4e-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="01c4e-125">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="01c4e-125">Click New.</span></span>
12. <span data-ttu-id="01c4e-126">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="01c4e-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="01c4e-127">في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="01c4e-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="01c4e-128">حدد "إجمالي" في حقل "سلوك التكلفة".</span><span class="sxs-lookup"><span data-stu-id="01c4e-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="01c4e-129">في الحقل "أساس التوزيع"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="01c4e-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="01c4e-130">تابع حتى إنشاء كافة القواعد.</span><span class="sxs-lookup"><span data-stu-id="01c4e-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="01c4e-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="01c4e-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="01c4e-132">تعيين السياسة إلى وحدة التحكم بالتكاليف</span><span class="sxs-lookup"><span data-stu-id="01c4e-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="01c4e-133">انقر فوق "تعيينات السياسة" لوحدة التحكم بالتكاليف.</span><span class="sxs-lookup"><span data-stu-id="01c4e-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="01c4e-134">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="01c4e-134">Click New.</span></span>
3. <span data-ttu-id="01c4e-135">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="01c4e-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="01c4e-136">أدخل تاريخًا في الحقل "صالح بدءًا من تاريخ المحاسبة‬‬".</span><span class="sxs-lookup"><span data-stu-id="01c4e-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="01c4e-137">القواعد لها تاريخ سريان.</span><span class="sxs-lookup"><span data-stu-id="01c4e-137">The rules are date-effective.</span></span> <span data-ttu-id="01c4e-138">باستطاعة المستخدم أو النظام إنهاء تاريخ صلاحية القواعد إذا تم إنشاء إصدار أحدث.</span><span class="sxs-lookup"><span data-stu-id="01c4e-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="01c4e-139">في الحقل "وحدة التحكم بالتكاليف‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="01c4e-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="01c4e-140">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="01c4e-140">Click Save.</span></span>

