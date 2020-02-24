---
title: " دفع المنتجات من مركز توزيع إلى متجر باستخدام دفع المشتري"
description: يتناول هذا الإجراء الخطوات اللازمة لإنشاء ومعالجة ‏‫توزيع المشتريات‬ لتوزيع المنتجات من موقع واحد إلى متجر واحد أو أكثر.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailBuyersPush, InventLocationIdLookup, InventItemIdLookupSimple, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62eeb29e348c558e8954f656b89d90792b0c347b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021461"
---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a><span data-ttu-id="88d03-103"> دفع المنتجات من مركز توزيع إلى متجر باستخدام دفع المشتري</span><span class="sxs-lookup"><span data-stu-id="88d03-103">Push products from distribution center to store using buyer's push</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="88d03-104">يتناول هذا الإجراء الخطوات اللازمة لإنشاء ومعالجة ‏‫توزيع المشتريات‬ لتوزيع المنتجات من موقع واحد إلى متجر واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="88d03-104">This procedure walks through the steps to create and process a Buyer´s push to distribute products from one location to one or many stores.</span></span> <span data-ttu-id="88d03-105">يمكن للمستخدم تحديد تكوينات متعددة وامتلاك النظام الذي يقترح كيفية توزيع المنتجات أو إدخال مكان توزيع المنتجات يدويًا وكمية المنتجات التي يتم توزيعها على كل متجر.</span><span class="sxs-lookup"><span data-stu-id="88d03-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="88d03-106">لا يتضمن هذا الإجراء عملية إعداد البيانات التي يمكن استخدامها في ‏‫توزيع المشتريات‬، مثل قواعد التزويد والتدرجات الهرمية للمؤسسات وتخزين الأوزان.</span><span class="sxs-lookup"><span data-stu-id="88d03-106">This procedure doesn't include setup of data that can be used in the Buyer´s push, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="88d03-107">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="88d03-107">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="88d03-108">انتقل إلى توزيع المشتريات.</span><span class="sxs-lookup"><span data-stu-id="88d03-108">Go to Buyer's push.</span></span>
2. <span data-ttu-id="88d03-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="88d03-109">Click New.</span></span>
3. <span data-ttu-id="88d03-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="88d03-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="88d03-111">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="88d03-111">In the Site field, enter or select a value.</span></span>
5. <span data-ttu-id="88d03-112">في حقل "المستودع"، أدخل مستودعًا يحتوي على منتجات بكميات فعلية أو حدده.</span><span class="sxs-lookup"><span data-stu-id="88d03-112">In the Warehouse field, enter or select a warehouse that has products with on-hand quantities.</span></span>
6. <span data-ttu-id="88d03-113">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="88d03-113">Click Add.</span></span>
7. <span data-ttu-id="88d03-114">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="88d03-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="88d03-115">في حقل "رقم الصنف"، أدخل منتجًا أو حدده.</span><span class="sxs-lookup"><span data-stu-id="88d03-115">In the Item number field, enter or select a product.</span></span>
9. <span data-ttu-id="88d03-116">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="88d03-116">Click Add.</span></span>
10. <span data-ttu-id="88d03-117">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="88d03-117">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="88d03-118">في حقل "رقم الصنف"، أدخل منتجًا متغيرًا أو حدده.</span><span class="sxs-lookup"><span data-stu-id="88d03-118">In the Item number field, enter or select a variant product.</span></span>
    * <span data-ttu-id="88d03-119">عند إدخال منتج متغير، سيتم إنشاء بنود لكل متغير.</span><span class="sxs-lookup"><span data-stu-id="88d03-119">When entering a variant product, lines will be created for each variant.</span></span>  
12. <span data-ttu-id="88d03-120">في القائمة، ضع علامة تمييز أمام الصف.</span><span class="sxs-lookup"><span data-stu-id="88d03-120">In the list, mark a row.</span></span>
13. <span data-ttu-id="88d03-121">في حقل "الكمية الموزعة"، اكتب عدد المنتجات المحددة التي تريد توزيعها.</span><span class="sxs-lookup"><span data-stu-id="88d03-121">In the Pushed quantity field, type how many of the selected product you want to distribute.</span></span>
14. <span data-ttu-id="88d03-122">في حقل "‏‫كمية إضافية للتوزيع"، أدخل كمية المنتجات التي لها كمية متوفرة لتوزيعها.</span><span class="sxs-lookup"><span data-stu-id="88d03-122">In the Additional quantity to push field, enter the quantity of the products that have available quantity to distribute.</span></span>
15. <span data-ttu-id="88d03-123">في حقل "التوزيع"، أدخل "‏‫وزن الموقع".</span><span class="sxs-lookup"><span data-stu-id="88d03-123">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="88d03-124">يمكنك تحديد الأنواع الأخرى لاستخدام قواعد أخرى للتوزيع.</span><span class="sxs-lookup"><span data-stu-id="88d03-124">You can select the other types to use other rules for the distribution.</span></span>  
16. <span data-ttu-id="88d03-125">في حقل "‏‫التدرج الهرمي للتزويد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="88d03-125">In the Replenishment hierarchy field, select a value.</span></span>
17. <span data-ttu-id="88d03-126">حدد "نعم" في حقل "‏‫مراعاة عمليات الفرز‬".</span><span class="sxs-lookup"><span data-stu-id="88d03-126">Select Yes in the Respect assortments field.</span></span>
18. <span data-ttu-id="88d03-127">انقر فوق حساب الكميات وقم بمراجعة الكميات التي تم إضافتها إلى الصفوف في قسم المستودع.</span><span class="sxs-lookup"><span data-stu-id="88d03-127">Click Calculate quantities and review the quantities that are added to the rows in the Warehouse section.</span></span>
19. <span data-ttu-id="88d03-128">انقر فوق إنشاء أمر.</span><span class="sxs-lookup"><span data-stu-id="88d03-128">Click Create order.</span></span>
20. <span data-ttu-id="88d03-129">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="88d03-129">Click Yes.</span></span>

