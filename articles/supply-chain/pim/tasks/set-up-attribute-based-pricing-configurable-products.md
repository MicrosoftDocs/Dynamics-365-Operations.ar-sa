--- 
title: "إعداد تسعير يستند إلى سمة للمنتجات القابلة للتكوين"
description: "يوضح هذا الإجراء كيفية إعداد تسعير يستند إلى سمة."
author: ShylaThompson
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: f1eaa53a652a59d4d970781f734e1332aa762ca2
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="e500e-103">إعداد تسعير يستند إلى سمة للمنتجات القابلة للتكوين</span><span class="sxs-lookup"><span data-stu-id="e500e-103">Set up attribute-based pricing for configurable products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e500e-104">يوضح هذا الإجراء كيفية إعداد تسعير يستند إلى سمة.</span><span class="sxs-lookup"><span data-stu-id="e500e-104">This procedure shows how to set up attribute-based pricing.</span></span> <span data-ttu-id="e500e-105">كشرط مسبق، يجب أن يتوفر لديك نموذج تكوين منتج لديه مكون واحد أو أكثر وسمة واحدة أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="e500e-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="e500e-106">يستخدم هذا المثال نموذج مكبر الصوت المتطور في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="e500e-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="e500e-107">يستخدم مدير المنتج عادةً هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="e500e-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="e500e-108">إنشاء نموذج سعر جديد</span><span class="sxs-lookup"><span data-stu-id="e500e-108">Create a new price model</span></span>
1. <span data-ttu-id="e500e-109">انقر فوق "تعريف نموذج متغير المنتج"ز</span><span class="sxs-lookup"><span data-stu-id="e500e-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="e500e-110">انقر فوق "نماذج تكوين المنتجات".</span><span class="sxs-lookup"><span data-stu-id="e500e-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="e500e-111">في القائمة، حدد بند "مكبر الصوت المتطور"، ولكن لا تنقر فوق الارتباط الخاص بالاسم.</span><span class="sxs-lookup"><span data-stu-id="e500e-111">In the list, select the High End Speaker line, but don’t click the link for the name.</span></span>
4. <span data-ttu-id="e500e-112">في جزء الإجراءات، انقر فوق "النموذج".</span><span class="sxs-lookup"><span data-stu-id="e500e-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="e500e-113">انقر فوق "نماذج أسعار".</span><span class="sxs-lookup"><span data-stu-id="e500e-113">Click Price models.</span></span>
6. <span data-ttu-id="e500e-114">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e500e-114">Click New.</span></span>
7. <span data-ttu-id="e500e-115">في الحقل "اسم نموذج السعر"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e500e-115">In the Price model name field, type a value.</span></span>
    * <span data-ttu-id="e500e-116">استخدم اسمًا يسهّل التعرف على النموذج.</span><span class="sxs-lookup"><span data-stu-id="e500e-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="e500e-117">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e500e-117">In the Description field, type a value.</span></span>
9. <span data-ttu-id="e500e-118">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e500e-118">Click Save.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="e500e-119">إضافة عناصر السعر</span><span class="sxs-lookup"><span data-stu-id="e500e-119">Add price elements</span></span>
1. <span data-ttu-id="e500e-120">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="e500e-120">Click Edit.</span></span>
    * <span data-ttu-id="e500e-121">بإمكان كل مكون في نموذج المنتج أن يكون له عنصر سعر أساسي وأي عدد من قواعد تعبير السعر.</span><span class="sxs-lookup"><span data-stu-id="e500e-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="e500e-122">يمكنك أيضًا إضافة أسعار بعملات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="e500e-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="e500e-123">في حقل "‏‫تعبير السعر الأساسي"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e500e-123">In the Base price expression field, type a value.</span></span>
    * <span data-ttu-id="e500e-124">على سبيل المثال، اكتب "100".</span><span class="sxs-lookup"><span data-stu-id="e500e-124">For example, type 100.</span></span>   <span data-ttu-id="e500e-125">بإمكان تعبير السعر الأساسي أن يكون عبارة عن قيمة رقمية، أو بإمكانه أن يتكون من عملية حسابية تتضمن سمة واحدة أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="e500e-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="e500e-126">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="e500e-126">Click Add.</span></span>
4. <span data-ttu-id="e500e-127">في حقل "الاسم"، اكتب "خشب الورد".</span><span class="sxs-lookup"><span data-stu-id="e500e-127">In the Name field, type ‘Rosewood’.</span></span>
    * <span data-ttu-id="e500e-128">يساعد اسم تعبير السعر على تحديد ما يمثله عنصر السعر.</span><span class="sxs-lookup"><span data-stu-id="e500e-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="e500e-129">في هذا المثال، نقوم بإنشاء عنصر سعر لخيار خزانة مكبر صوت من خشب الورد.</span><span class="sxs-lookup"><span data-stu-id="e500e-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="e500e-130">انقر فوق "تحرير الشرط".</span><span class="sxs-lookup"><span data-stu-id="e500e-130">Click Edit condition.</span></span>
    * <span data-ttu-id="e500e-131">يساعد شرط السعر على ضمان تضمين عنصر تعبير السعر في سعر المبيعات فقط في حالة وجود مجموعة محددة من السمات.</span><span class="sxs-lookup"><span data-stu-id="e500e-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="e500e-132">في الحقل ConstraintBody، أدخل 'CabinetFinish=="Rosewood"'.</span><span class="sxs-lookup"><span data-stu-id="e500e-132">In the ConstraintBody field, enter 'CabinetFinish=="Rosewood"'.</span></span>
7. <span data-ttu-id="e500e-133">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="e500e-133">Click OK.</span></span>
8. <span data-ttu-id="e500e-134">في حقل "التعبير"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e500e-134">In the Expression field, type a value.</span></span>
    * <span data-ttu-id="e500e-135">على سبيل المثال، اكتب "50".</span><span class="sxs-lookup"><span data-stu-id="e500e-135">For example, type 50.</span></span>  
9. <span data-ttu-id="e500e-136">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e500e-136">Close the page.</span></span>
10. <span data-ttu-id="e500e-137">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e500e-137">Close the page.</span></span>


