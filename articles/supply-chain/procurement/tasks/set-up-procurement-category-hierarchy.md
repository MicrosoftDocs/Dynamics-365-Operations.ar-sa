---
title: إعداد التدرج الهرمي لفئات التدبير
description: يوضح هذا الإجراء كيفية إنشاء عقد جديد في تدرج هرمي لفئات التدبير وكيفية تكوين فئة تدبير لاستخدامها في عملية تدبير.
author: mkirknel
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7010a1c612b9b3884c675f578657d951da06c38
ms.sourcegitcommit: 25fe679b73663fda6b5b3c32646026d0993a9f00
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/12/2019
ms.locfileid: "1995272"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="5dbbb-103">إعداد التدرج الهرمي لفئات التدبير</span><span class="sxs-lookup"><span data-stu-id="5dbbb-103">Set up a procurement category hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5dbbb-104">يوضح هذا الإجراء كيفية إنشاء عقد جديد في تدرج هرمي لفئات التدبير وكيفية تكوين فئة تدبير لاستخدامها في عملية تدبير.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="5dbbb-105">وعادة ما تُنفذ هذه المهام عن طريق إدارة شراء.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="5dbbb-106">قبل أن تتمكن من البدء في هذا الإجراء، يجب أن يكون هناك تدرج هرمي للفئات من نوع التدبير.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="5dbbb-107">إذا كنت تستخدم شركة عرض تقديمي للبيانات، يمكنك تنفيذ هذا الإجراء في شركة USMF.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="5dbbb-108">أضف فئة تدبير جديدة.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-108">Add a new procurement category</span></span>
1. <span data-ttu-id="5dbbb-109">انتقل إلى **جزء التنقل > الوحدات النمطية > التدبير والتوريد‬ > الشحن > فئات التدبير‬**.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="5dbbb-110">في جزء الإجراءات، حدد **تحرير التدرج الهرمي للفئات**.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-110">On the action pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="5dbbb-111">يتم عرض التدرج الهرمي الحالي لفئات التدبير في الجانب الأيسر من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="5dbbb-112">أنت على وشك تعديل هرم فئات التدبير:</span><span class="sxs-lookup"><span data-stu-id="5dbbb-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="5dbbb-113">في جزء الإجراءات، حدد **عقدة الفئة الجديدة‬**.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-113">On the action pane, select **New category node**.</span></span> <span data-ttu-id="5dbbb-114">يحدد النظام العقدة العليا بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-114">The system selects the top node by default.</span></span> <span data-ttu-id="5dbbb-115">إذا كنت تنفذ هذا الإجراء كدليل مهمة، يمكنك النقر فوق الزر "إلغاء التأمين" وتحديد عقدة أصلية أخرى لإدراج العقدة الجديدة بها.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="5dbbb-116">بمجرد أن يتم ذلك، قم بتأمين "دليل المهمة" مرة أخرى وانقر فوق "عقدة الفئة الجديدة".</span><span class="sxs-lookup"><span data-stu-id="5dbbb-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="5dbbb-117">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="5dbbb-118">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="5dbbb-119">في حقل **الاسم المألوف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="5dbbb-120">الاسم المألوف اختياري.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-120">The friendly name is optional.</span></span> <span data-ttu-id="5dbbb-121">سيُعرض في عمليات البحث عن الفئات مع اسم الفئة.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="5dbbb-122">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="5dbbb-123">إضافة منتجات إلى فئة التدبير الجديدة</span><span class="sxs-lookup"><span data-stu-id="5dbbb-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="5dbbb-124">انتقل إلى **التدبير والتوريد > الشحن > فئات التوريد**.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="5dbbb-125">حدد العقدة التي أضفتها للتو.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-125">Select the node you just added.</span></span> <span data-ttu-id="5dbbb-126">إذا كنت تنفذ هذا الإجراء كدليل مهمة، فقد تحتاج إلى إلغاء تأمين دليل المهمة لتحديد العقدة.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-126">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="5dbbb-127">قم بتبديل توسيع القسم **المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="5dbbb-128">حدد **إضافة** لربط المنتجات بفئة التدبير.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="5dbbb-129">حدد المنتجات التي تريد إضافتها إلى فئة التدبير.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="5dbbb-130">حدد السهم لإضافة المنتجات إلى جدول **المحدد**.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="5dbbb-131">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5dbbb-131">Select **OK**.</span></span>
