--- 
title: " تعديلات سعر البيع بالتجزئة"
description: "سيتناول هذا الإجراء إنشاء تعديل سعر البيع بالتجزئة."
author: josaw1
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: edfb9a1515f0af7d3272ea3fbb362bd0e6b0f129
ms.contentlocale: ar-sa
ms.lasthandoff: 02/07/2018

---
# <a name="retail-price-adjustments"></a><span data-ttu-id="b0a13-103"> تعديلات سعر البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="b0a13-103">Retail price adjustments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b0a13-104">سيتناول هذا الإجراء إنشاء تعديل سعر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="b0a13-104">This procedure will walk through creating a retail price adjustment.</span></span> <span data-ttu-id="b0a13-105">ويمكن أن يقوم تعديل سعر البيع بالتجزئة بتعيين سعر بيع أحد الأصناف مباشرة، أو تعديل سعر بيعه الأساسي أو سعر البيع حسب الاتفاقية التجارية.</span><span class="sxs-lookup"><span data-stu-id="b0a13-105">A retail price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="b0a13-106">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="b0a13-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="b0a13-107">انقر فوق "إدارة التسعير والخصومات".</span><span class="sxs-lookup"><span data-stu-id="b0a13-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="b0a13-108">انقر فوق علامة التبويب تعديلات الأسعار.</span><span class="sxs-lookup"><span data-stu-id="b0a13-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="b0a13-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b0a13-109">Click New.</span></span>
    * <span data-ttu-id="b0a13-110">من هنا يمكنك إنشاء كافة قواعد السعر والخصم الأكثر استخدامًا، بما في ذلك خصومات البيع بالتجزئة وتعديلات الأسعار ودفاتر يومية الاتفاقيات التجارية وقواعد تسعير الفئات.</span><span class="sxs-lookup"><span data-stu-id="b0a13-110">From here you can create all of the most commonly used price and discount rules, including retail discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="b0a13-111">انقر فوق تعديل السعر.</span><span class="sxs-lookup"><span data-stu-id="b0a13-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="b0a13-112">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b0a13-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="b0a13-113">قم بتوسيع القسم "البنود".</span><span class="sxs-lookup"><span data-stu-id="b0a13-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="b0a13-114">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="b0a13-114">Click Add.</span></span>
    * <span data-ttu-id="b0a13-115">بالنسبة لهذا المثال، أدخل "81126" في حقل "المنتج".</span><span class="sxs-lookup"><span data-stu-id="b0a13-115">For this example, enter '81126' in the Product field.</span></span>    <span data-ttu-id="b0a13-116">ثم، أدخل "10.0" في حقل "‏‫النسبة المئوية‬ للخصم‬".</span><span class="sxs-lookup"><span data-stu-id="b0a13-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="b0a13-117">سيقلل تعديل السعر من نوع ‏‫النسبة المئوية للخصم سعر المبيعات الأساسي أو سعر المبيعات حسب الاتفاقية التجارية‬.</span><span class="sxs-lookup"><span data-stu-id="b0a13-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="b0a13-118">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="b0a13-118">Click Add.</span></span>
    * <span data-ttu-id="b0a13-119">بالنسبة لهذا المثال، أدخل "81125" في حقل "المنتج".</span><span class="sxs-lookup"><span data-stu-id="b0a13-119">For this example, enter '81125' in the Product field.</span></span>    <span data-ttu-id="b0a13-120">ثم حدد "مبلغ الخصم النقدي" في حقل "طريقة الخصم".</span><span class="sxs-lookup"><span data-stu-id="b0a13-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="b0a13-121">وأخيرًا، أدخل "5.0" في حقل "‏‫مبلغ الخصم النقدي‬".</span><span class="sxs-lookup"><span data-stu-id="b0a13-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="b0a13-122">نوع خصم مبلغ الخصم النقدي هو المبلغ المخصوم من السعر الأساسي أو سعر الاتفاقية التجارية.</span><span class="sxs-lookup"><span data-stu-id="b0a13-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="b0a13-123">انقر فوق "مجموعات الأسعار".</span><span class="sxs-lookup"><span data-stu-id="b0a13-123">Click Price groups.</span></span>
    * <span data-ttu-id="b0a13-124">حدد "RP هيوستن" في حقل "مجموعة الأسعار".</span><span class="sxs-lookup"><span data-stu-id="b0a13-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="b0a13-125">وهذا سيقوم بإقران تعديل السعر بمتجر هيوستن.</span><span class="sxs-lookup"><span data-stu-id="b0a13-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="b0a13-126">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b0a13-126">Click Save.</span></span>
11. <span data-ttu-id="b0a13-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b0a13-127">Close the page.</span></span>
12. <span data-ttu-id="b0a13-128">في حقل "الحالة"، حدد "ممكَّن".</span><span class="sxs-lookup"><span data-stu-id="b0a13-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="b0a13-129">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b0a13-129">Click Save.</span></span>
14. <span data-ttu-id="b0a13-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b0a13-130">Close the page.</span></span>
15. <span data-ttu-id="b0a13-131">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b0a13-131">Refresh the page.</span></span>


