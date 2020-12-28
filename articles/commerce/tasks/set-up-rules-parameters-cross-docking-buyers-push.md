---
title: " إعداد قواعد ومعلمات لتوزيع البضائع ودفع المشتري"
description: يوضح هذا الإجراء الخطوات اللازمة لإنشاء قواعد تزويد.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bccd92946783628dce37c3fd018e4dd927efd49
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409922"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="9c5e0-103"> إعداد قواعد ومعلمات لتوزيع البضائع ودفع المشتري</span><span class="sxs-lookup"><span data-stu-id="9c5e0-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c5e0-104">يوضح هذا الإجراء الخطوات اللازمة لإنشاء قواعد تزويد.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="9c5e0-105">يمكن استخدام قواعد التزويد للتحكم في كيفية توزيع المنتجات للمتاجر عند استخدام ‏‫توزيع البضائع‬ و‏‫توزيع المشتريات.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="9c5e0-106">يمكن إعداد قواعد التزويد للمتاجر أو مجموعات المتاجر.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="9c5e0-107">سيتحكم الوزن المحدد لكل بند في القاعدة في كيف سيتم توزيع كميات المنتجات بين المتاجر عند استخدام قواعد التزويد كطريقة التوزيع في توزيع البضائع وتوزيع المشتريات.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="9c5e0-108">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="9c5e0-109">انتقل إلى قواعد التزويد.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="9c5e0-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="9c5e0-110">Click New.</span></span>
3. <span data-ttu-id="9c5e0-111">في حقل "قاعدة التزويد"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="9c5e0-112">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9c5e0-113">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="9c5e0-113">Click Save.</span></span>
6. <span data-ttu-id="9c5e0-114">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-114">Click Add.</span></span>
7. <span data-ttu-id="9c5e0-115">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9c5e0-116">يمكنك اختيار ‏‫التدرج الهرمي للتزويد‬ أو القناة للنوع.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="9c5e0-117">تتحكم القيمة فيما إذا كان التحديد في الاسم سيكون تدرجًا هرميًا من القنوات أو قناة معينة.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="9c5e0-118">بالنسبة لهذا المثال، اترك القيمة معينة كتدرج هرمي للتزويد.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="9c5e0-119">في حقل "الاسم"، حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="9c5e0-120">يتم ملء قيمة الوزن الافتراضي من الوزن المحدد في المستودع.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="9c5e0-121">يمكن استخدام هذا الوزن لقاعدة التزويد أو يمكنك إدخال وزن جديد في حقل الوزن.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="9c5e0-122">في حقل "الوزن"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="9c5e0-123">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-123">Click Add.</span></span>
11. <span data-ttu-id="9c5e0-124">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="9c5e0-125">في حقل "النوع"، حدد "القناة".</span><span class="sxs-lookup"><span data-stu-id="9c5e0-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="9c5e0-126">في الحقل "الاسم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="9c5e0-127">في حقل "الوزن"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="9c5e0-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="9c5e0-128">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="9c5e0-128">Click Save.</span></span>

