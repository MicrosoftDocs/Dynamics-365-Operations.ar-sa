---
title: " تعديلات سعر البيع بالتجزئة"
description: سيتناول هذا الإجراء إنشاء تعديل سعر التجارة.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailDiscountPriceGroup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7443f69473c0aad478d47f80f284b1156bad9c24
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4962975"
---
# <a name="retail-price-adjustments"></a><span data-ttu-id="66751-103"> تعديلات سعر البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="66751-103">Retail price adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66751-104">سيتناول هذا الإجراء إنشاء تعديل سعر التجارة.</span><span class="sxs-lookup"><span data-stu-id="66751-104">This procedure will walk through creating a commerce price adjustment.</span></span> <span data-ttu-id="66751-105">ويمكن أن يقوم تعديل الأسعار بتعيين سعر بيع أحد الأصناف مباشرة، أو تعديل سعر بيعه الأساسي أو سعر البيع حسب الاتفاقية التجارية.</span><span class="sxs-lookup"><span data-stu-id="66751-105">A price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="66751-106">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="66751-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="66751-107">انقر فوق "إدارة التسعير والخصومات".</span><span class="sxs-lookup"><span data-stu-id="66751-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="66751-108">انقر فوق علامة التبويب تعديلات الأسعار.</span><span class="sxs-lookup"><span data-stu-id="66751-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="66751-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="66751-109">Click New.</span></span>
    * <span data-ttu-id="66751-110">من هنا يمكنك إنشاء كافة قواعد السعر والخصم الأكثر استخدامًا، بما في ذلك الخصومات وتعديلات الأسعار ودفاتر يومية الاتفاقيات التجارية وقواعد تسعير الفئات.</span><span class="sxs-lookup"><span data-stu-id="66751-110">From here you can create all of the most commonly used price and discount rules, including discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="66751-111">انقر فوق تعديل السعر.</span><span class="sxs-lookup"><span data-stu-id="66751-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="66751-112">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="66751-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="66751-113">قم بتوسيع القسم "البنود".</span><span class="sxs-lookup"><span data-stu-id="66751-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="66751-114">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="66751-114">Click Add.</span></span>
    * <span data-ttu-id="66751-115">بالنسبة لهذا المثال، أدخل "81126" في حقل "المنتج".</span><span class="sxs-lookup"><span data-stu-id="66751-115">For this example, enter '81126' in the Product field.</span></span> <span data-ttu-id="66751-116">ثم، أدخل "10.0" في حقل "‏‫النسبة المئوية‬ للخصم‬".</span><span class="sxs-lookup"><span data-stu-id="66751-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="66751-117">سيقلل تعديل السعر من نوع ‏‫النسبة المئوية للخصم سعر المبيعات الأساسي أو سعر المبيعات حسب الاتفاقية التجارية‬.</span><span class="sxs-lookup"><span data-stu-id="66751-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="66751-118">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="66751-118">Click Add.</span></span>
    * <span data-ttu-id="66751-119">بالنسبة لهذا المثال، أدخل "81125" في حقل "المنتج".</span><span class="sxs-lookup"><span data-stu-id="66751-119">For this example, enter '81125' in the Product field.</span></span> <span data-ttu-id="66751-120">ثم حدد "مبلغ الخصم النقدي" في حقل "طريقة الخصم".</span><span class="sxs-lookup"><span data-stu-id="66751-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="66751-121">وأخيرًا، أدخل "5.0" في حقل "‏‫مبلغ الخصم النقدي‬".</span><span class="sxs-lookup"><span data-stu-id="66751-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="66751-122">نوع خصم مبلغ الخصم النقدي هو المبلغ المخصوم من السعر الأساسي أو سعر الاتفاقية التجارية.</span><span class="sxs-lookup"><span data-stu-id="66751-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="66751-123">انقر فوق "مجموعات الأسعار".</span><span class="sxs-lookup"><span data-stu-id="66751-123">Click Price groups.</span></span>
    * <span data-ttu-id="66751-124">حدد "RP هيوستن" في حقل "مجموعة الأسعار".</span><span class="sxs-lookup"><span data-stu-id="66751-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="66751-125">وهذا سيقوم بإقران تعديل السعر بمتجر هيوستن.</span><span class="sxs-lookup"><span data-stu-id="66751-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="66751-126">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="66751-126">Click Save.</span></span>
11. <span data-ttu-id="66751-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="66751-127">Close the page.</span></span>
12. <span data-ttu-id="66751-128">في حقل "الحالة"، حدد "ممكَّن".</span><span class="sxs-lookup"><span data-stu-id="66751-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="66751-129">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="66751-129">Click Save.</span></span>
14. <span data-ttu-id="66751-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="66751-130">Close the page.</span></span>
15. <span data-ttu-id="66751-131">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="66751-131">Refresh the page.</span></span>

