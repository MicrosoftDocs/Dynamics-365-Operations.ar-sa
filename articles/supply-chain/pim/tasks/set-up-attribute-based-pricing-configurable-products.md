---
title: إعداد تسعير يستند إلى سمة للمنتجات القابلة للتكوين
description: يوضح هذا الموضوع كيفية إعداد تسعير يستند إلى سمة.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e540e0f25afa65e84cdb11fb0c56437b72891f9f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220742"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="13b11-103">إعداد تسعير يستند إلى سمة للمنتجات القابلة للتكوين</span><span class="sxs-lookup"><span data-stu-id="13b11-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="13b11-104">يوضح هذا الموضوع كيفية إعداد تسعير يستند إلى سمة.</span><span class="sxs-lookup"><span data-stu-id="13b11-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="13b11-105">كشرط مسبق، يجب أن يتوفر لديك نموذج تكوين منتج لديه مكون واحد أو أكثر وسمة واحدة أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="13b11-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="13b11-106">يستخدم هذا المثال نموذج مكبر الصوت المتطور في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="13b11-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="13b11-107">يستخدم مدير المنتج عادةً هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="13b11-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="13b11-108">إنشاء نموذج سعر جديد</span><span class="sxs-lookup"><span data-stu-id="13b11-108">Create a new price model</span></span>
1. <span data-ttu-id="13b11-109">حدد **تعريف نموذج متغير المنتج‬** في الصفحة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="13b11-109">Select **Product variant model definition** on the home page.</span></span>
2. <span data-ttu-id="13b11-110">حدد **نماذج تكوين المنتج** في قسم **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="13b11-110">Select **Product configuration models** in the **links** section.</span></span>
3. <span data-ttu-id="13b11-111">في القائمة، حدد **مكبر الصوت المتطور** ولكن لا تنقر فوق الارتباط الخاص بالاسم.</span><span class="sxs-lookup"><span data-stu-id="13b11-111">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
4. <span data-ttu-id="13b11-112">في جزء الإجراءات، حدد **النموذج**.</span><span class="sxs-lookup"><span data-stu-id="13b11-112">On the Action Pane, select **Model**.</span></span>
5. <span data-ttu-id="13b11-113">حدد **نماذج الأسعار**.</span><span class="sxs-lookup"><span data-stu-id="13b11-113">Select **Price models**.</span></span>
6. <span data-ttu-id="13b11-114">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="13b11-114">Select **New**.</span></span>
7. <span data-ttu-id="13b11-115">في الحقل **اسم نموذج السعر**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="13b11-115">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="13b11-116">استخدم اسمًا يسهّل التعرف على النموذج.</span><span class="sxs-lookup"><span data-stu-id="13b11-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="13b11-117">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="13b11-117">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="13b11-118">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="13b11-118">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="13b11-119">إضافة عناصر السعر</span><span class="sxs-lookup"><span data-stu-id="13b11-119">Add price elements</span></span>
1. <span data-ttu-id="13b11-120">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="13b11-120">Select **Edit**.</span></span> <span data-ttu-id="13b11-121">بإمكان كل مكون في نموذج المنتج أن يكون له عنصر سعر أساسي وأي عدد من قواعد تعبير السعر.</span><span class="sxs-lookup"><span data-stu-id="13b11-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="13b11-122">يمكنك أيضًا إضافة أسعار بعملات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="13b11-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="13b11-123">في حقل **‏‫تعبير السعر الأساسي**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="13b11-123">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="13b11-124">على سبيل المثال، اكتب "100".</span><span class="sxs-lookup"><span data-stu-id="13b11-124">For example, type 100.</span></span> <span data-ttu-id="13b11-125">بإمكان تعبير السعر الأساسي أن يكون عبارة عن قيمة رقمية، أو بإمكانه أن يتكون من عملية حسابية تتضمن سمة واحدة أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="13b11-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="13b11-126">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="13b11-126">Select **Add**.</span></span>
4. <span data-ttu-id="13b11-127">في حقل **الاسم**، اكتب `Rosewood`.</span><span class="sxs-lookup"><span data-stu-id="13b11-127">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="13b11-128">يساعد اسم تعبير السعر على تحديد ما يمثله عنصر السعر.</span><span class="sxs-lookup"><span data-stu-id="13b11-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="13b11-129">في هذا المثال، نقوم بإنشاء عنصر سعر لخيار خزانة مكبر صوت من خشب الورد.</span><span class="sxs-lookup"><span data-stu-id="13b11-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="13b11-130">حدد **تحرير الشرط**.</span><span class="sxs-lookup"><span data-stu-id="13b11-130">Select **Edit condition**.</span></span> <span data-ttu-id="13b11-131">يساعد شرط السعر على ضمان تضمين عنصر تعبير السعر في سعر المبيعات فقط في حالة وجود مجموعة محددة من السمات.</span><span class="sxs-lookup"><span data-stu-id="13b11-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="13b11-132">في الحقل **ConstraintBody**، أدخل `CabinetFinish=="Rosewood"`.</span><span class="sxs-lookup"><span data-stu-id="13b11-132">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="13b11-133">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="13b11-133">Select **OK**.</span></span>
8. <span data-ttu-id="13b11-134">في حقل **التعبير**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="13b11-134">In the **Expression** field, type a value.</span></span> <span data-ttu-id="13b11-135">على سبيل المثال، اكتب `50`.</span><span class="sxs-lookup"><span data-stu-id="13b11-135">For example, type `50`.</span></span> 
9. <span data-ttu-id="13b11-136">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="13b11-136">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]