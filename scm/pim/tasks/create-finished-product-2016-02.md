--- 
title: "إنشاء منتج نهائي (فبراير 2016 فقط)"
description: "تركز هذه المهمة على إنشاء منتج نهائي."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: a14b56b508e5d46bb2898828bd30fdf6c3c14023
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2017

---
# <a name="create-a-finished-product-february-2016-only"></a><span data-ttu-id="0dd15-103">إنشاء منتج نهائي (فبراير 2016 فقط)</span><span class="sxs-lookup"><span data-stu-id="0dd15-103">Create a finished product (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0dd15-104">تركز هذه المهمة على إنشاء منتج نهائي.</span><span class="sxs-lookup"><span data-stu-id="0dd15-104">This task focuses on creating a finished product.</span></span> <span data-ttu-id="0dd15-105">إنها المهمة الأولى في سلسلة حسابات قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="0dd15-105">It is the first task in the BOM calculation series.</span></span> <span data-ttu-id="0dd15-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="0dd15-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="0dd15-107">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="0dd15-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="0dd15-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="0dd15-108">Click New.</span></span>
3. <span data-ttu-id="0dd15-109">في الحقل "رقم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0dd15-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="0dd15-110">للعرض التوضيحي، اكتب BOM_1.</span><span class="sxs-lookup"><span data-stu-id="0dd15-110">For the demonstration, type BOM_1.</span></span>  
4. <span data-ttu-id="0dd15-111">في الحقل "مجموعة النموذج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0dd15-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="0dd15-112">حدد "STD".</span><span class="sxs-lookup"><span data-stu-id="0dd15-112">Select STD.</span></span> <span data-ttu-id="0dd15-113">يشير الاختصار STD إلى التكلفة القياسية وهو النموذج الأكثر استخدامًا عند العمل مع حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="0dd15-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="0dd15-114">في حقل "مجموعة الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0dd15-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="0dd15-115">على سبيل المثال، حدد "الصوت".</span><span class="sxs-lookup"><span data-stu-id="0dd15-115">For example, select Audio.</span></span> <span data-ttu-id="0dd15-116">ليس لذلك أي تأثير على حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="0dd15-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="0dd15-117">في الحقل "مجموعة بُعد التخزين"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0dd15-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="0dd15-118">حدد SiteWH.</span><span class="sxs-lookup"><span data-stu-id="0dd15-118">Select SiteWH.</span></span> <span data-ttu-id="0dd15-119">سيتم استخدام الموقع والمستودع فقط للعرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="0dd15-119">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="0dd15-120">في الحقل "مجموعة بُعد التعقب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0dd15-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="0dd15-121">لن يتم استخدام أبعاد التعقب لهذا المثال، حدد "بلا".</span><span class="sxs-lookup"><span data-stu-id="0dd15-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="0dd15-122">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="0dd15-122">Click OK.</span></span>
9. <span data-ttu-id="0dd15-123">في جزء الإجراءات‬، انقر فوق "إدارة المخزون".</span><span class="sxs-lookup"><span data-stu-id="0dd15-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="0dd15-124">انقر فوق "إعدادات الأوامر الافتراضية".</span><span class="sxs-lookup"><span data-stu-id="0dd15-124">Click Default order settings.</span></span>
11. <span data-ttu-id="0dd15-125">في الحقل "نوع الأمر الافتراضي"، حدد "الإنتاج".</span><span class="sxs-lookup"><span data-stu-id="0dd15-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="0dd15-126">لأن هذا المنتج عبارة عن منتج نهائي سيتم إنتاجه، حدد "الإنتاج".</span><span class="sxs-lookup"><span data-stu-id="0dd15-126">Because this is a finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="0dd15-127">في الحقل "موقع الشراء"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0dd15-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="0dd15-128">للعرض توضيحي، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="0dd15-128">For the demonstration, select Site 1.</span></span>  
13. <span data-ttu-id="0dd15-129">في الحقل "موقع المخزون، أدخل القيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0dd15-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="0dd15-130">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="0dd15-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="0dd15-131">في الحقل "موقع المبيعات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0dd15-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="0dd15-132">بالنسبة إلى هذا المثال، حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="0dd15-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="0dd15-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0dd15-133">Close the page.</span></span>


