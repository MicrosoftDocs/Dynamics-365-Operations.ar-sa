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
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad95752ce40faaa84747dac9bfbf2887f7a5af42
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440094"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="4c081-103">إنشاء وتعيين سياسة تخصيص التكلفة إلى وحدة التحكم في التكلفة</span><span class="sxs-lookup"><span data-stu-id="4c081-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4c081-104">استخدم هذا الإجراء لإنشاء سياسة توزيع التكلفة‬ والقواعد المناظرة وتعيينها إلى وحدة التحكم بالتكاليف.</span><span class="sxs-lookup"><span data-stu-id="4c081-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="4c081-105">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USP2.</span><span class="sxs-lookup"><span data-stu-id="4c081-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="4c081-106">إنشاء سياسة</span><span class="sxs-lookup"><span data-stu-id="4c081-106">Create a policy</span></span>
1. <span data-ttu-id="4c081-107">انتقل إلى محاسبة التكاليف > السياسات > سياسات توزيع التكاليف.</span><span class="sxs-lookup"><span data-stu-id="4c081-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="4c081-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="4c081-108">Click New.</span></span>
3. <span data-ttu-id="4c081-109">في الحقل "اسم السياسة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="4c081-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="4c081-110">في الحقل "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4c081-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="4c081-111">حدد "المؤسسة".</span><span class="sxs-lookup"><span data-stu-id="4c081-111">Select Organization.</span></span>  
5. <span data-ttu-id="4c081-112">في الحقل "البعد الإحصائي"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4c081-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="4c081-113">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="4c081-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="4c081-114">إنشاء قواعد التوزيع</span><span class="sxs-lookup"><span data-stu-id="4c081-114">Create allocation rules</span></span>
1. <span data-ttu-id="4c081-115">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="4c081-115">Click New.</span></span>
2. <span data-ttu-id="4c081-116">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4c081-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="4c081-117">في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4c081-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="4c081-118">حدد "إجمالي" في حقل "سلوك التكلفة".</span><span class="sxs-lookup"><span data-stu-id="4c081-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="4c081-119">في الحقل "أساس التوزيع"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="4c081-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="4c081-120">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="4c081-120">Click New.</span></span>
7. <span data-ttu-id="4c081-121">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4c081-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="4c081-122">في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4c081-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="4c081-123">حدد "إجمالي" في حقل "سلوك التكلفة".</span><span class="sxs-lookup"><span data-stu-id="4c081-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="4c081-124">في الحقل "أساس التوزيع"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="4c081-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="4c081-125">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="4c081-125">Click New.</span></span>
12. <span data-ttu-id="4c081-126">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4c081-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="4c081-127">في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4c081-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="4c081-128">حدد "إجمالي" في حقل "سلوك التكلفة".</span><span class="sxs-lookup"><span data-stu-id="4c081-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="4c081-129">في الحقل "أساس التوزيع"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="4c081-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="4c081-130">تابع حتى إنشاء كافة القواعد.</span><span class="sxs-lookup"><span data-stu-id="4c081-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="4c081-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="4c081-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="4c081-132">تعيين السياسة إلى وحدة التحكم بالتكاليف</span><span class="sxs-lookup"><span data-stu-id="4c081-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="4c081-133">انقر فوق "تعيينات السياسة" لوحدة التحكم بالتكاليف.</span><span class="sxs-lookup"><span data-stu-id="4c081-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="4c081-134">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="4c081-134">Click New.</span></span>
3. <span data-ttu-id="4c081-135">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4c081-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="4c081-136">أدخل تاريخًا في الحقل "صالح بدءًا من تاريخ المحاسبة‬‬".</span><span class="sxs-lookup"><span data-stu-id="4c081-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="4c081-137">القواعد لها تاريخ سريان.</span><span class="sxs-lookup"><span data-stu-id="4c081-137">The rules are date-effective.</span></span> <span data-ttu-id="4c081-138">باستطاعة المستخدم أو النظام إنهاء تاريخ صلاحية القواعد إذا تم إنشاء إصدار أحدث.</span><span class="sxs-lookup"><span data-stu-id="4c081-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="4c081-139">في الحقل "وحدة التحكم بالتكاليف‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4c081-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="4c081-140">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="4c081-140">Click Save.</span></span>

