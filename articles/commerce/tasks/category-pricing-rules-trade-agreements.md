---
title: " قواعد تسعير الفئات لإنشاء اتفاقيات التجارة"
description: يوضح هذا الإجراء كيفية إنشاء اتفاقيات تجارية على أسعار المبيعات باستخدام قاعدة تسعير الفئات.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPricingDiscountCategoryPriceRule, RetailCategoryPriceRule, EcoResCategorySingleLookup, RetailCategoryPriceWizard, PriceDiscAdm, PriceDiscAdmTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21b1986aa36aab23f50a5af434435f9e93318e45
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409950"
---
# <a name="category-pricing-rules-to-create-trade-agreements"></a><span data-ttu-id="e3f02-103"> قواعد تسعير الفئات لإنشاء اتفاقيات التجارة</span><span class="sxs-lookup"><span data-stu-id="e3f02-103">Category pricing rules to create trade agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3f02-104">يوضح هذا الإجراء كيفية إنشاء اتفاقيات تجارية على أسعار المبيعات باستخدام قاعدة تسعير الفئات.</span><span class="sxs-lookup"><span data-stu-id="e3f02-104">This procedure demonstrates how to create sales price trade agreements using a category pricing rule.</span></span> <span data-ttu-id="e3f02-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USRT.‬</span><span class="sxs-lookup"><span data-stu-id="e3f02-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="e3f02-106">تم إعداد هذه المهمة لدور إدارة بضائع Commerce.</span><span class="sxs-lookup"><span data-stu-id="e3f02-106">This task is intended for the Commerce merchandising manager role.</span></span>

1. <span data-ttu-id="e3f02-107">انقر فوق "إدارة التسعير والخصومات".</span><span class="sxs-lookup"><span data-stu-id="e3f02-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="e3f02-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e3f02-108">Click New.</span></span>
3. <span data-ttu-id="e3f02-109">انقر فوق قاعدة أسعار الفئات.</span><span class="sxs-lookup"><span data-stu-id="e3f02-109">Click Category price rule.</span></span>
4. <span data-ttu-id="e3f02-110">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e3f02-110">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="e3f02-111">في حقل "‏‫كود الحساب‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="e3f02-111">In the Account code field, select an option.</span></span>
    * <span data-ttu-id="e3f02-112">يتم استخدام رمز حساب نوع "المجموعة" لإعداد الاتفاقيات التجارية لأسعار المبيعات المحددة للقنوات وبرامج الولاء والكتالوجات‬ والتبعيات‬.</span><span class="sxs-lookup"><span data-stu-id="e3f02-112">A "Group" type account code is used to set up sales price trade agreements that are specific for Channels, Loyalty programs, Catalogs, and Affiliations.</span></span>  
6. <span data-ttu-id="e3f02-113">في حقل "‏‫تحديد الحساب‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e3f02-113">In the Account selection field, enter or select a value.</span></span>
7. <span data-ttu-id="e3f02-114">في حقل "الفئة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e3f02-114">In the Category field, enter or select a value.</span></span>
8. <span data-ttu-id="e3f02-115">في حقل "‏‫المبلغ/النسبة المئوية‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e3f02-115">In the Amount/Percent field, enter a number.</span></span>
9. <span data-ttu-id="e3f02-116">في حقل "‏‫إصدار التقريب‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e3f02-116">In the Rounding version field, enter or select a value.</span></span>
10. <span data-ttu-id="e3f02-117">انقر فوق إنشاء اتفاقيات تجارية.</span><span class="sxs-lookup"><span data-stu-id="e3f02-117">Click Generate trade agreements.</span></span>
11. <span data-ttu-id="e3f02-118">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="e3f02-118">Click Next.</span></span>
12. <span data-ttu-id="e3f02-119">في الحقل "من تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="e3f02-119">In the From date field, enter a date.</span></span>
13. <span data-ttu-id="e3f02-120">في الحقل "إلى تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="e3f02-120">In the To date field, enter a date.</span></span>
14. <span data-ttu-id="e3f02-121">حدد "نعم" في حقل "‏‫بحث عن التالي‬".</span><span class="sxs-lookup"><span data-stu-id="e3f02-121">Select Yes in the Find next field.</span></span>
15. <span data-ttu-id="e3f02-122">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="e3f02-122">Click Next.</span></span>
16. <span data-ttu-id="e3f02-123">انقر فوق إنهاء.</span><span class="sxs-lookup"><span data-stu-id="e3f02-123">Click Finish.</span></span>
    * <span data-ttu-id="e3f02-124">وهذا يؤدي إلى إنشاء دفتر يومية للاتفاقية التجارية وفتحه للمراجعة.</span><span class="sxs-lookup"><span data-stu-id="e3f02-124">This creates a Trade agreement journal and opens it for your review.</span></span>  
17. <span data-ttu-id="e3f02-125">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e3f02-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e3f02-126">لا يتم ترحيل دفاتر يومية الاتفاقيات التجارية التي تم إنشاؤها من قواعد تسعير الفئات.</span><span class="sxs-lookup"><span data-stu-id="e3f02-126">The trade agreement journals created from the Category pricing rules aren't posted.</span></span> <span data-ttu-id="e3f02-127">يمكنك مراجعة الأسعار التي تم إنشاؤها وتحريرها قبل ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="e3f02-127">You can  review and edit the prices generated before posting them.</span></span>  
18. <span data-ttu-id="e3f02-128">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="e3f02-128">Click Edit.</span></span>
19. <span data-ttu-id="e3f02-129">في حقل "المبلغ بالعملة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e3f02-129">In the Amount in currency field, enter a number.</span></span>
20. <span data-ttu-id="e3f02-130">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="e3f02-130">Click Post.</span></span>
21. <span data-ttu-id="e3f02-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="e3f02-131">Click OK.</span></span>
22. <span data-ttu-id="e3f02-132">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e3f02-132">Close the page.</span></span>
23. <span data-ttu-id="e3f02-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e3f02-133">Close the page.</span></span>
24. <span data-ttu-id="e3f02-134">انقر فوق علامة التبويب قواعد أسعار الفئات.</span><span class="sxs-lookup"><span data-stu-id="e3f02-134">Click the Category price rules tab.</span></span>
    * <span data-ttu-id="e3f02-135">ستظهر قواعد تسعير الفئات الخاصة بالقنوات في هذه القائمة.</span><span class="sxs-lookup"><span data-stu-id="e3f02-135">Channel specific Category pricing rules will show in this list.</span></span>  

