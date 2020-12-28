---
title: إعداد التدرج الهرمي لفئات التدبير
description: يوضح هذا الإجراء كيفية إنشاء عقد جديد في تدرج هرمي لفئات التدبير وكيفية تكوين فئة تدبير لاستخدامها في عملية تدبير.
author: mkirknel
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e45c80718c73ad785643c2a5fc0e712b291104d5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421662"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="981e2-103">إعداد التدرج الهرمي لفئات التدبير</span><span class="sxs-lookup"><span data-stu-id="981e2-103">Set up a procurement category hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="981e2-104">يوضح هذا الإجراء كيفية إنشاء عقد جديد في تدرج هرمي لفئات التدبير وكيفية تكوين فئة تدبير لاستخدامها في عملية تدبير.</span><span class="sxs-lookup"><span data-stu-id="981e2-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="981e2-105">وعادة ما تُنفذ هذه المهام عن طريق إدارة شراء.</span><span class="sxs-lookup"><span data-stu-id="981e2-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="981e2-106">قبل أن تتمكن من البدء في هذا الإجراء، يجب أن يكون هناك تدرج هرمي للفئات من نوع التدبير.</span><span class="sxs-lookup"><span data-stu-id="981e2-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="981e2-107">إذا كنت تستخدم شركة عرض تقديمي للبيانات، يمكنك تنفيذ هذا الإجراء في شركة USMF.</span><span class="sxs-lookup"><span data-stu-id="981e2-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="981e2-108">أضف فئة تدبير جديدة.</span><span class="sxs-lookup"><span data-stu-id="981e2-108">Add a new procurement category</span></span>
1. <span data-ttu-id="981e2-109">انتقل إلى **جزء التنقل > الوحدات النمطية > التدبير والتوريد‬ > الشحن > فئات التدبير‬**.</span><span class="sxs-lookup"><span data-stu-id="981e2-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="981e2-110">في جزء الإجراءات، حدد **تحرير التدرج الهرمي للفئات**.</span><span class="sxs-lookup"><span data-stu-id="981e2-110">On the Action Pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="981e2-111">يتم عرض التدرج الهرمي الحالي لفئات التدبير في الجانب الأيسر من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="981e2-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="981e2-112">أنت على وشك تعديل هرم فئات التدبير:</span><span class="sxs-lookup"><span data-stu-id="981e2-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="981e2-113">في جزء الإجراءات، حدد **عقدة الفئة الجديدة‬**.</span><span class="sxs-lookup"><span data-stu-id="981e2-113">On the Action Pane, select **New category node**.</span></span> <span data-ttu-id="981e2-114">يحدد النظام العقدة العليا بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="981e2-114">The system selects the top node by default.</span></span> <span data-ttu-id="981e2-115">إذا كنت تنفذ هذا الإجراء كدليل مهمة، يمكنك النقر فوق الزر "إلغاء التأمين" وتحديد عقدة أصلية أخرى لإدراج العقدة الجديدة بها.</span><span class="sxs-lookup"><span data-stu-id="981e2-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="981e2-116">بمجرد أن يتم ذلك، قم بتأمين "دليل المهمة" مرة أخرى وانقر فوق "عقدة الفئة الجديدة".</span><span class="sxs-lookup"><span data-stu-id="981e2-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="981e2-117">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="981e2-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="981e2-118">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="981e2-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="981e2-119">في حقل **الاسم المألوف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="981e2-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="981e2-120">الاسم المألوف اختياري.</span><span class="sxs-lookup"><span data-stu-id="981e2-120">The friendly name is optional.</span></span> <span data-ttu-id="981e2-121">سيُعرض في عمليات البحث عن الفئات مع اسم الفئة.</span><span class="sxs-lookup"><span data-stu-id="981e2-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="981e2-122">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="981e2-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="981e2-123">إضافة منتجات إلى فئة التدبير الجديدة</span><span class="sxs-lookup"><span data-stu-id="981e2-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="981e2-124">انتقل إلى **التدبير والتوريد > الشحن > فئات التوريد**.</span><span class="sxs-lookup"><span data-stu-id="981e2-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="981e2-125">حدد العقدة التي أضفتها للتو.</span><span class="sxs-lookup"><span data-stu-id="981e2-125">Select the node you just added.</span></span> <span data-ttu-id="981e2-126">إذا كنت تنفذ هذا الإجراء كدليل مهمة، فقد تحتاج إلى إلغاء تأمين دليل المهمة لتحديد العقدة.</span><span class="sxs-lookup"><span data-stu-id="981e2-126">If you're running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="981e2-127">قم بتبديل توسيع القسم **المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="981e2-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="981e2-128">حدد **إضافة** لربط المنتجات بفئة التدبير.</span><span class="sxs-lookup"><span data-stu-id="981e2-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="981e2-129">حدد المنتجات التي تريد إضافتها إلى فئة التدبير.</span><span class="sxs-lookup"><span data-stu-id="981e2-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="981e2-130">حدد السهم لإضافة المنتجات إلى جدول **المحدد**.</span><span class="sxs-lookup"><span data-stu-id="981e2-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="981e2-131">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="981e2-131">Select **OK**.</span></span>
